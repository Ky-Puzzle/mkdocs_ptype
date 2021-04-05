### AC-3: Access Enforcement 
 
Control: The information system enforces approved authorizations for logical access to information
and system resources in accordance with applicable access control policies.

Supplemental Guidance: [Access control policies](access_control.md) (e.g., identity-based policies, role-based policies,
control matrices, cryptography) control access between active entities or subjects (i.e., users or
processes acting on behalf of users) and passive entities or objects (e.g., devices, files, records,
domains) in information systems. In addition to enforcing authorized access at the information
system level and recognizing that information systems can host many applications and services in
support of organizational missions and business operations, access enforcement mechanisms can
also be employed at the application and service level to provide increased information security.

Related controls: [AC-2](ac2-account_management.md), [AC-4, AC-5, AC-6, AC-16, AC-17, AC-18, AC-19, AC-20, AC-21, AC22](access_control.md), [AU-9](audit_and_accountabilty.md), [CM-5, CM-6, CM-11](configuration_management.md), [MA-3, MA-4, MA-5](maintenance.md), [PE-3](physical_and_environmental_protection).
Control Enhancements:

(1) ACCESS ENFORCEMENT | RESTRICTED ACCESS TO PRIVILEGED FUNCTIONS
[Withdrawn: Incorporated into AC-6].

(2) ACCESS ENFORCEMENT | DUAL AUTHORIZATION

The information system enforces dual authorization for [Assignment: organization-defined
privileged commands and/or other organization-defined actions].
Supplemental Guidance: Dual authorization mechanisms require the approval of two authorized
individuals in order to execute. Organizations do not require dual authorization mechanisms
when immediate responses are necessary to ensure public and environmental safety. Dual
authorization may also be known as two-person control. Related controls: [CP-9](contingency_planning.md), [MP-6](media_protection.md).

(3) ACCESS ENFORCEMENT | MANDATORY ACCESS CONTROL

The information system enforces [Assignment: organization-defined mandatory access control
policy] over all subjects and objects where the policy:

(a) Is uniformly enforced across all subjects and objects within the boundary of the information
system;

(b) Specifies that a subject that has been granted access to information is constrained from doing
any of the following;

	(1) Passing the information to unauthorized subjects or objects;
	(2) Granting its privileges to other subjects;
	(3) Changing one or more security attributes on subjects, objects, the information system, or
	information system components;
	(4) Choosing the security attributes and attribute values to be associated with newly created
	or modified objects; or
	(5) Changing the rules governing access control; and
	
(c) Specifies that [Assignment: organization-defined subjects] may explicitly be granted
[Assignment: organization-defined privileges (i.e., they are trusted subjects)] such that they
are not limited by some or all of the above constraints.

Supplemental Guidance: [Mandatory access control](access_control.md) as defined in this control enhancement is
synonymous with [nondiscretionary access control](access_control.md), and is not constrained only to certain
historical uses (e.g., implementations using the [Bell-LaPadula Model](https://en.wikipedia.org/wiki/Bell%E2%80%93LaPadula_model)). The above class of
[mandatory access control](access_control.md) policies constrains what actions subjects can take with information
obtained from data objects for which they have already been granted access, thus preventing
the subjects from passing the information to unauthorized subjects and objects. This class of
mandatory access control policies also constrains what actions subjects can take with respect
to the propagation of access control privileges; that is, a subject with a privilege cannot pass
that privilege to other subjects. The policy is uniformly enforced over all subjects and objects
to which the information system has control. Otherwise, the access control policy can be
circumvented. This enforcement typically is provided via an implementation that meets the
reference monitor concept (see [AC-25](access_control.md)). The policy is bounded by the information system
boundary (i.e., once the information is passed outside of the control of the system, additional
means may be required to ensure that the constraints on the information remain in effect). The
trusted subjects described above are granted privileges consistent with the concept of least
privilege (see [AC-6](access_control.md)). Trusted subjects are only given the minimum privileges relative to the
above policy necessary for satisfying organizational mission/business needs. The control is
most applicable when there is some policy mandate (e.g., law, Executive Order, directive, or
regulation) that establishes a policy regarding access to sensitive/classified information and
some users of the information system are not authorized access to all sensitive/classified
information resident in the information system. This control can operate in conjunction with
[AC-3 (4)](ac3-access_enforcement.md). A subject that is constrained in its operation by policies governed by this control is
still able to operate under the less rigorous constraints of [AC-3 (4)](ac3-access_enforcement.md), but policies governed by
this control take precedence over the less rigorous constraints of [AC-3 (4)](ac3-access_enforcement.md). For example,
while a mandatory access control policy imposes a constraint preventing a subject from
passing information to another subject operating at a different sensitivity label, AC-3 (4)
permits the subject to pass the information to any subject with the same sensitivity label as the
subject. Related controls: [AC-25](access_control.md), [SC-11](systems_and_communications_protection.md).

(4) ACCESS ENFORCEMENT | DISCRETIONARY [ACCESS CONTROL](access_control.md)
The information system enforces [Assignment: organization-defined discretionary access control
policy] over defined subjects and objects where the policy specifies that a subject that has been
granted access to information can do one or more of the following:

(a) Pass the information to any other subjects or objects;

(b) Grant its privileges to other subjects;

(c) Change security attributes on subjects, objects, the information system, or the information
system’s components;

(d) Choose the security attributes to be associated with newly created or revised objects; or

(e) Change the rules governing access control.

Supplemental Guidance: When discretionary [access control](access_control.md) policies are implemented, subjects
are not constrained with regard to what actions they can take with information for which they
have already been granted access. Thus, subjects that have been granted access to information
are not prevented from passing (i.e., the subjects have the discretion to pass) the information
to other subjects or objects. This control enhancement can operate in conjunction with [AC-3](ac3-access_enforcement.md)
(3). A subject that is constrained in its operation by policies governed by AC-3 (3) is still able
to operate under the less rigorous constraints of this control enhancement. Thus, while AC-3
(3) imposes constraints preventing a subject from passing information to another subject
operating at a different sensitivity level, [AC-3 (4)](ac3-access_enforcement.md) permits the subject to pass the information
to any subject at the same sensitivity level. The policy is bounded by the information system
boundary. Once the information is passed outside of the control of the information system,
additional means may be required to ensure that the constraints remain in effect. While the
older, more traditional definitions of [discretionary access control](ac3-access_enforcement.md) require identity-based access
control, that limitation is not required for this use of discretionary access control.

(5) ACCESS ENFORCEMENT | SECURITY-RELEVANT INFORMATION
The information system prevents access to [Assignment: organization-defined security-relevant
information] except during secure, non-operable system states.

Supplemental Guidance: Security-relevant information is any information within information
systems that can potentially impact the operation of security functions or the provision of
security services in a manner that could result in failure to enforce system security policies or
maintain the isolation of code and data. Security-relevant information includes, for example,
filtering rules for routers/firewalls, cryptographic key management information, configuration
parameters for security services, and access control lists. Secure, non-operable system states
include the times in which information systems are not performing mission/business-related
processing (e.g., the system is off-line for maintenance, troubleshooting, boot-up, shut down).
Related control: [CM-3](configuration_management.md).

(6) ACCESS ENFORCEMENT | PROTECTION OF USER AND SYSTEM INFORMATION
[Withdrawn: Incorporated into [MP-4](media_protection.md) and [SC-28](systems_and_communications_protection.md)].

(7) ACCESS ENFORCEMENT | ROLE-BASED [ACCESS CONTROL](access_control.md)

The information system enforces a role-based access control policy over defined subjects and
objects and controls access based upon [Assignment: organization-defined roles and users
authorized to assume such roles].

Supplemental Guidance: Role-based [access control](access_control.md) (RBAC) is an access control policy that
restricts information system access to authorized users. Organizations can create specific roles
based on job functions and the authorizations (i.e., privileges) to perform needed operations
on organizational information systems associated with the organization-defined roles. When
users are assigned to the organizational roles, they inherit the authorizations or privileges
defined for those roles. RBAC simplifies privilege administration for organizations because
privileges are not assigned directly to every user (which can be a significant number of

individuals for mid- to large-size organizations) but are instead acquired through role
assignments. RBAC can be implemented either as a mandatory or discretionary form of
access control. For organizations implementing RBAC with mandatory [access controls](access_control.md), the
requirements in [AC-3](access_control.md) (3) define the scope of the subjects and objects covered by the policy.

(8) ACCESS ENFORCEMENT | REVOCATION OF ACCESS AUTHORIZATIONS

The information system enforces the revocation of access authorizations resulting from changes
to the security attributes of subjects and objects based on [Assignment: organization-defined rules
governing the timing of revocations of access authorizations].

Supplemental Guidance: Revocation of access rules may differ based on the types of access
revoked. For example, if a subject (i.e., user or process) is removed from a group, access may
not be revoked until the next time the object (e.g., file) is opened or until the next time the
subject attempts a new access to the object. Revocation based on changes to security labels
may take effect immediately. Organizations can provide alternative approaches on how to
make revocations immediate if information systems cannot provide such capability and
immediate revocation is necessary.

(9) ACCESS ENFORCEMENT | CONTROLLED RELEASE

The information system does not release information outside of the established system boundary
unless:

(a) The receiving [Assignment: organization-defined information system or system component]
provides [Assignment: organization-defined security safeguards]; and

(b) [Assignment: organization-defined security safeguards] are used to validate the
appropriateness of the information designated for release.

Supplemental Guidance: Information systems can only protect organizational information
within the confines of established system boundaries. Additional security safeguards may be
needed to ensure that such information is adequately protected once it is passed beyond the
established information system boundaries. Examples of information leaving the system
boundary include transmitting information to an external information system or printing the
information on one of its printers. In cases where the information system is unable to make a
determination of the adequacy of the protections provided by entities outside its boundary, as
a mitigating control, organizations determine procedurally whether the external information
systems are providing adequate security. The means used to determine the adequacy of the
security provided by external information systems include, for example, conducting
inspections or periodic testing, establishing agreements between the organization and its
counterpart organizations, or some other process. The means used by external entities to
protect the information received need not be the same as those used by the organization, but
the means employed are sufficient to provide consistent adjudication of the security policy to
protect the information. This control enhancement requires information systems to employ
technical or procedural means to validate the information prior to releasing it to external
systems. For example, if the information system passes information to another system
controlled by another organization, technical means are employed to validate that the security
attributes associated with the exported information are appropriate for the receiving system.
Alternatively, if the information system passes information to a printer in organizationcontrolled space, procedural means can be employed to ensure that only appropriately
authorized individuals gain access to the printer. This control enhancement is most applicable
when there is some policy mandate (e.g., law, Executive Order, directive, or regulation) that
establishes policy regarding access to the information, and that policy applies beyond the
realm of a particular information system or organization.

(10) ACCESS ENFORCEMENT | AUDITED OVERRIDE OF [ACCESS CONTROL](access_control.md)MECHANISMS

The organization employs an audited override of automated access control mechanisms under
[Assignment: organization-defined conditions].

Supplemental Guidance: Related controls: [AU-2, AU-6](audit_and_accountabilty.md).