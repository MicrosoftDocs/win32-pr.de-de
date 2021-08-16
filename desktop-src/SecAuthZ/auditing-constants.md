---
description: Stellt Kategorien und Unterkategorien von Audit Policy-Ereignissen dar.
ms.assetid: e3b12139-947d-4922-91fd-f9833c069011
title: Überwachungskonst constants (Ntsecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 316dcd969ebba3cf571c7851a6d628617e4a261aea83c26b2524e3edcc0e4b79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784308"
---
# <a name="auditing-constants"></a>Überwachungskonst constants

Die folgenden Konstanten stellen Kategorien und Unterkategorien von Audit-Policy-Ereignissen dar.

Die folgenden Konstanten stellen Kategorien von Überwachungsrichtlinieereignissen dar. Diese Konstanten werden als **GUID-Strukturen** in "Ntsecapi.h" definiert.

<dl> <dt>

<span id="Audit_System"></span><span id="audit_system"></span><span id="AUDIT_SYSTEM"></span>**\_Überwachungssystem**
</dt> <dd> <dl> <dt>

69979848-797a-11d9-bed3-505054503030
</dt> <dt>



Es wird versucht, den Computer herunter- oder neu zu starten. Überwachen Sie außerdem Ereignisse, die sich auf die Systemsicherheit oder das Sicherheitsprotokoll auswirken.


</dt> </dl> </dd> <dt>

<span id="Audit_Logon"></span><span id="audit_logon"></span><span id="AUDIT_LOGON"></span>**Anmeldung \_ überwachen**
</dt> <dd> <dl> <dt>

69979849-797a-11d9-bed3-505054503030
</dt> <dt>



Es wird versucht, sich beim System an- oder abzumelden. Außerdem versucht die Überwachung, eine Netzwerkverbindung herzustellen.


</dt> </dl> </dd> <dt>

<span id="Audit_ObjectAccess"></span><span id="audit_objectaccess"></span><span id="AUDIT_OBJECTACCESS"></span>**ObjectAccess \_ überwachen**
</dt> <dd> <dl> <dt>

6997984a-797a-11d9-bed3-505054503030
</dt> <dt>



Überwacht Versuche, auf sicherungsfähige Objekte zu zugreifen.


</dt> </dl> </dd> <dt>

<span id="Audit_PrivilegeUse"></span><span id="audit_privilegeuse"></span><span id="AUDIT_PRIVILEGEUSE"></span>**Audit \_ PrivilegeUse**
</dt> <dd> <dl> <dt>

6997984b-797a-11d9-bed3-505054503030
</dt> <dt>



Versucht zu überwachen, Berechtigungen [*zu verwenden.*](/windows/desktop/SecGloss/p-gly)


</dt> </dl> </dd> <dt>

<span id="Audit_DetailedTracking"></span><span id="audit_detailedtracking"></span><span id="AUDIT_DETAILEDTRACKING"></span>**\_DetailedTracking überwachen**
</dt> <dd> <dl> <dt>

6997984c-797a-11d9-bed3-505054503030
</dt> <dt>



Überwachungsspezifische Ereignisse, z. B. Programmaktivierung, einige Formen der Duplizierung, indirekter Zugriff auf ein Objekt und Prozessabschaltung.


</dt> </dl> </dd> <dt>

<span id="Audit_PolicyChange"></span><span id="audit_policychange"></span><span id="AUDIT_POLICYCHANGE"></span>**Überwachen \_ von PolicyChange**
</dt> <dd> <dl> <dt>

6997984d-797a-11d9-bed3-505054503030
</dt> <dt>



Versucht, [**Richtlinienobjektregeln**](/windows/desktop/SecMgmt/the-policy-object-type) zu ändern.


</dt> </dl> </dd> <dt>

<span id="Audit_AccountManagement"></span><span id="audit_accountmanagement"></span><span id="AUDIT_ACCOUNTMANAGEMENT"></span>**AccountManagement \_ überwachen**
</dt> <dd> <dl> <dt>

6997984e-797a-11d9-bed3-505054503030
</dt> <dt>



Es wird versucht, Benutzer- oder Gruppenkonten zu erstellen, zu löschen oder zu ändern. Überwachen Sie außerdem Kennwortänderungen.


</dt> </dl> </dd> <dt>

<span id="Audit_DirectoryServiceAccess"></span><span id="audit_directoryserviceaccess"></span><span id="AUDIT_DIRECTORYSERVICEACCESS"></span>**Verzeichnis \_ überwachenServiceAccess**
</dt> <dd> <dl> <dt>

6997984f-797a-11d9-bed3-505054503030
</dt> <dt>



Versucht, auf den Verzeichnisdienst zu zugreifen, wird überwacht.


</dt> </dl> </dd> <dt>

<span id="Audit_AccountLogon"></span><span id="audit_accountlogon"></span><span id="AUDIT_ACCOUNTLOGON"></span>**Konto \_ überwachenLogon**
</dt> <dd> <dl> <dt>

69979850-797a-11d9-bed3-505054503030
</dt> <dt>



Überwachen Sie Anmeldeversuche von privilegierten Konten, die sich beim Domänencontroller anmelden. Diese Überwachungsereignisse werden generiert, wenn sich Schlüsselverteilungscenter [*Kerberos-Datenbank*](/windows/desktop/SecGloss/k-gly) (KDC) beim Domänencontroller anmeldet.


</dt> </dl> </dd> </dl>

Die folgenden Konstanten stellen Unterkategorien von Audit-Policy-Ereignissen dar. Diese Konstanten werden als **GUID-Strukturen** in "Ntsecapi.h" definiert.

<dl> <span id="Audit_System_SecurityStateChange"></span><span id="audit_system_securitystatechange"></span><span id="AUDIT_SYSTEM_SECURITYSTATECHANGE"></span>**Überwachen \_ System \_ SecurityStateChange** (0cce9210-69ae-11d9-bed3-505054503030) <span id="Audit_System_SecuritySubsystemExtension"></span> <span id="audit_system_securitysubsystemextension"></span> <span id="AUDIT_SYSTEM_SECURITYSUBSYSTEMEXTENSION"></span> **Audit System \_ \_ SecuritySubsystemExtension** (0cce9211-69ae-11d9-bed3-505054503030) <span id="Audit_System_Integrity"></span> <span id="audit_system_integrity"></span> <span id="AUDIT_SYSTEM_INTEGRITY"></span> **\_ \_ Systemintegrität** überwachen (0cce921) 2-69ae-11d9-bed3-505054503030) <span id="Audit_System_IPSecDriverEvents"></span> <span id="audit_system_ipsecdriverevents"></span> <span id="AUDIT_SYSTEM_IPSECDRIVEREVENTS"></span> **Audit System \_ \_ IPSecDriverEvents** (0cce9213-69ae-11d9-bed3-505054503030) <span id="Audit_System_Others"></span> <span id="audit_system_others"></span> <span id="AUDIT_SYSTEM_OTHERS"></span> **Audit System \_ \_ Others** (0cce9214-69ae-11d9-bed3-505054503030) Anmeldung überwachen <span id="Audit_Logon_Logon"></span> <span id="audit_logon_logon"></span> <span id="AUDIT_LOGON_LOGON"></span> (0cce9215-69ae-11d9-bed3-505054503030) **\_ \_** <span id="Audit_Logon_Logoff"></span> <span id="audit_logon_logoff"></span> <span id="AUDIT_LOGON_LOGOFF"></span> **\_ \_ Logoff** überwachen (0cce9216-69ae-11d9-bed3-505054503030) Audit <span id="Audit_Logon_AccountLockout"></span> <span id="audit_logon_accountlockout"></span> <span id="AUDIT_LOGON_ACCOUNTLOCKOUT"></span> **\_ Logon \_ AccountLockout** (0cce9217-69ae-11d9-bed3-505054503030) <span id="Audit_Logon_IPSecMainMode"></span> <span id="audit_logon_ipsecmainmode"></span> <span id="AUDIT_LOGON_IPSECMAINMODE"></span> **\_ Audit Logon \_ IPSecMainMode** (0cce9218-69ae-11d9-bed3-505054503030) <span id="Audit_Logon_IPSecQuickMode"></span> <span id="audit_logon_ipsecquickmode"></span> <span id="AUDIT_LOGON_IPSECQUICKMODE"></span> **Überwachen \_ Logon \_ IPSecQuickMode** (0cce9219-69ae-11d9-bed3-505054503030) <span id="Audit_Logon_IPSecUserMode"></span> <span id="audit_logon_ipsecusermode"></span> <span id="AUDIT_LOGON_IPSECUSERMODE"></span> **Audit \_ Logon \_ IPSecUserMode** (0cce921a-69ae-11d9-bed3-505054503030) Audit <span id="Audit_Logon_SpecialLogon"></span> <span id="audit_logon_speciallogon"></span> <span id="AUDIT_LOGON_SPECIALLOGON"></span> **\_ Logon \_ SpecialLogon** (0cce921b-69ae-11d9-bed3-505054503030) <span id="Audit_Logon_Others"></span> <span id="audit_logon_others"></span> <span id="AUDIT_LOGON_OTHERS"></span> **Audit \_ Logon \_ Others** (0cce921c-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_FileSystem"></span> <span id="audit_objectaccess_filesystem"></span> <span id="AUDIT_OBJECTACCESS_FILESYSTEM"></span> **Audit \_ ObjectAccess \_ FileSystem** (0cce921d-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_Registry"></span> <span id="audit_objectaccess_registry"></span> <span id="AUDIT_OBJECTACCESS_REGISTRY"></span> **\_ ObjectAccess \_ Registry** überwachen (0cce921e-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_Kernel"></span> <span id="audit_objectaccess_kernel"></span> <span id="AUDIT_OBJECTACCESS_KERNEL"></span> **Audit \_ ObjectAccess \_ Kernel** (0cce921f-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_Sam"></span> <span id="audit_objectaccess_sam"></span> <span id="AUDIT_OBJECTACCESS_SAM"></span> **\_ ObjectAccess \_ Sam** (0cce9220-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_CertificationServices"></span> <span id="audit_objectaccess_certificationservices"></span> <span id="AUDIT_OBJECTACCESS_CERTIFICATIONSERVICES"></span> **Audit \_ ObjectAccess \_ CertificationServices** ( 0cce9221-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_ApplicationGenerated"></span> <span id="audit_objectaccess_applicationgenerated"></span> <span id="AUDIT_OBJECTACCESS_APPLICATIONGENERATED"></span> **Audit \_ ObjectAccess \_ ApplicationGenerated** (0cce9222-69ae-11d9-bed3-505054503030) Audit ObjectAccess Handle (505054503030) Audit ObjectAccess Handle (505054503030) Audit ObjectAccess Handle (0cce9221-69ae-bed3-505054503030) Audit ObjectAccess Handle (0cce9221-69ae-11d9-bed3-505054503030) Audit ObjectAccess Handle (0cce9221-bed3-505054503030) Audit ObjectAccess Handle (0cce9221-69ae-bed3-505054503030)0cce9223-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_Handle"></span> <span id="audit_objectaccess_handle"></span> <span id="AUDIT_OBJECTACCESS_HANDLE"></span> **\_ \_** <span id="Audit_ObjectAccess_Share"></span> <span id="audit_objectaccess_share"></span> <span id="AUDIT_OBJECTACCESS_SHARE"></span> **\_ ObjectAccess \_ Share** überwachen (0cce9224-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_FirewallPacketDrops"></span> <span id="audit_objectaccess_firewallpacketdrops"></span> <span id="AUDIT_OBJECTACCESS_FIREWALLPACKETDROPS"></span> **Audit \_ ObjectAccess \_ FirewallPacketDrops** (0cce9225-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_FirewallConnection"></span> <span id="audit_objectaccess_firewallconnection"></span> <span id="AUDIT_OBJECTACCESS_FIREWALLCONNECTION"></span> **Audit \_ ObjectAccess \_ FirewallConnection** (0cce9226-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_Other"></span> <span id="audit_objectaccess_other"></span> <span id="AUDIT_OBJECTACCESS_OTHER"></span> **Audit \_ ObjectAccess \_ Andere** (0cce9227-69ae-11d9-bed3-505054503030) Audit <span id="Audit_PrivilegeUse_Sensitive"></span> <span id="audit_privilegeuse_sensitive"></span> <span id="AUDIT_PRIVILEGEUSE_SENSITIVE"></span> **\_ \_ PrivilegeUse Sensitive** (0cce9228-69ae-11d9-bed3-50505450303030) Audit <span id="Audit_PrivilegeUse_NonSensitive"></span> <span id="audit_privilegeuse_nonsensitive"></span> <span id="AUDIT_PRIVILEGEUSE_NONSENSITIVE"></span> **\_ PrivilegeUse \_ NonSensitive** (0cce9229-69ae-11d9-bed3-505054503030) <span id="Audit_PrivilegeUse_Others"></span> <span id="audit_privilegeuse_others"></span> <span id="AUDIT_PRIVILEGEUSE_OTHERS"></span> **Audit \_ \_ PrivilegeUse Others** (0cce922a-69ae-11d9-bed3-505054503030) <span id="Audit_DetailedTracking_ProcessCreation"></span> <span id="audit_detailedtracking_processcreation"></span> <span id="AUDIT_DETAILEDTRACKING_PROCESSCREATION"></span> **\_ DetailedTracking \_ Process überwachenCreation** (0cce922b-69ae-11d9-bed3-505054503030) <span id="Audit_DetailedTracking_ProcessTermination"></span> <span id="audit_detailedtracking_processtermination"></span> <span id="AUDIT_DETAILEDTRACKING_PROCESSTERMINATION"></span> **Audit \_ DetailedTracking \_ ProcessTermination** (0cce922c-69ae-11d9-bed3-505054503030) <span id="Audit_DetailedTracking_DpapiActivity"></span> <span id="audit_detailedtracking_dpapiactivity"></span> <span id="AUDIT_DETAILEDTRACKING_DPAPIACTIVITY"></span> **Audit \_ DetailedTracking \_ DpapiActivity** (0cce922d-69ae-11d9-bed3-505054503030) <span id="Audit_DetailedTracking_RpcCall"></span> <span id="audit_detailedtracking_rpccall"></span> <span id="AUDIT_DETAILEDTRACKING_RPCCALL"></span> **\_ Audit DetailedTracking \_ RpcCall** (0cce922e-69ae-11d9-bed3-505054503030) <span id="Audit_PolicyChange_AuditPolicy"></span> <span id="audit_policychange_auditpolicy"></span> <span id="AUDIT_POLICYCHANGE_AUDITPOLICY"></span> **Audit \_ PolicyChange \_ AuditPolicy** (0cce922f-69ae-11d9-bed3-505054503030) <span id="Audit_PolicyChange_AuthenticationPolicy"></span> <span id="audit_policychange_authenticationpolicy"></span> <span id="AUDIT_POLICYCHANGE_AUTHENTICATIONPOLICY"></span> **\_ Audit PolicyChange \_ AuthenticationPolicy** (0cce9230-69ae-11d9-bed3-505054503030) <span id="Audit_PolicyChange_AuthorizationPolicy"></span> <span id="audit_policychange_authorizationpolicy"></span> <span id="AUDIT_POLICYCHANGE_AUTHORIZATIONPOLICY"></span> **Audit \_ PolicyChange \_ AuthorizationPolicy** (0cce9231-69ae-11d9-bed3-505054503030) <span id="Audit_PolicyChange_MpsscvRulePolicy"></span> <span id="audit_policychange_mpsscvrulepolicy"></span> <span id="AUDIT_POLICYCHANGE_MPSSCVRULEPOLICY"></span> **\_ Audit PolicyChange \_ MpsscvRulePolicy** (0cce9232-69ae-11d9-bed3-5)05054503030) <span id="Audit_PolicyChange_WfpIPSecPolicy"></span> <span id="audit_policychange_wfpipsecpolicy"></span> <span id="AUDIT_POLICYCHANGE_WFPIPSECPOLICY"></span> **Audit \_ PolicyChange \_ WfpIPSecPolicy** (0cce9233-69ae-11d9-bed3-505054503030) <span id="Audit_PolicyChange_Others"></span> <span id="audit_policychange_others"></span> <span id="AUDIT_POLICYCHANGE_OTHERS"></span> Audit PolicyChange Others (0cce9234-69ae-0cce9234-69ae-0) Audit **\_ PolicyChange Others11d9-bed3-505054503030) \_** <span id="Audit_AccountManagement_UserAccount"></span> <span id="audit_accountmanagement_useraccount"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_USERACCOUNT"></span> **\_ Audit AccountManagement \_ UserAccount** (0cce9235-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_ComputerAccount"></span> <span id="audit_accountmanagement_computeraccount"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_COMPUTERACCOUNT"></span> **\_ Audit AccountManagement \_ ComputerAccount** (0cce9236)-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_SecurityGroup"></span> <span id="audit_accountmanagement_securitygroup"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_SECURITYGROUP"></span> **\_ AccountManagement \_ SecurityGroup** überwachen (0cce9237-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_DistributionGroup"></span> <span id="audit_accountmanagement_distributiongroup"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_DISTRIBUTIONGROUP"></span> **\_ AccountManagement \_ DistributionGroup überwachen**(0cce9238-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_ApplicationGroup"></span> <span id="audit_accountmanagement_applicationgroup"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_APPLICATIONGROUP"></span> **\_ AccountManagement \_ ApplicationGroup** überwachen (0cce9239-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_Others"></span> <span id="audit_accountmanagement_others"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_OTHERS"></span> **\_ AccountManagement \_ andere** überwachen (0cc)e923a-69ae-11d9-bed3-505054503030) <span id="Audit_DSAccess_DSAccess"></span> <span id="audit_dsaccess_dsaccess"></span> <span id="AUDIT_DSACCESS_DSACCESS"></span> **\_ Audit DSAccess \_ DSAccess** (0cce923b-69ae-11d9-bed3-505054503030) <span id="Audit_DsAccess_AdAuditChanges"></span> <span id="audit_dsaccess_adauditchanges"></span> <span id="AUDIT_DSACCESS_ADAUDITCHANGES"></span> **Audit \_ DsAccess AdAuditChanges () Audit DsAccess \_ AdAuditChanges** () 0cce923c-69ae-11d9-bed3-505054503030) Audit <span id="Audit_Ds_Replication"></span> <span id="audit_ds_replication"></span> <span id="AUDIT_DS_REPLICATION"></span> **\_ Ds \_ Replication** (0cce923d-69ae-11d9-bed3-505054503030) <span id="Audit_Ds_DetailedReplication"></span> <span id="audit_ds_detailedreplication"></span> <span id="AUDIT_DS_DETAILEDREPLICATION"></span> **Audit Ds DetailedReplication (0) Audit \_ Ds \_ DetailedReplication** (0)cce923e-69ae-11d9-bed3-505054503030) <span id="Audit_AccountLogon_CredentialValidation"></span> <span id="audit_accountlogon_credentialvalidation"></span> <span id="AUDIT_ACCOUNTLOGON_CREDENTIALVALIDATION"></span> **Audit \_ AccountLogon \_ CredentialValidation** (0cce923f-69ae-11d9-bed3-505054503030) <span id="Audit_AccountLogon_Kerberos"></span> <span id="audit_accountlogon_kerberos"></span> <span id="AUDIT_ACCOUNTLOGON_KERBEROS"></span> **Audit \_ AccountLogon \_ Kerberos** (0cce9240-69ae-11d9-bed3-505054503030) <span id="Audit_AccountLogon_Others"></span> <span id="audit_accountlogon_others"></span> <span id="AUDIT_ACCOUNTLOGON_OTHERS"></span> **Audit \_ AccountLogon \_ Others** (0cce9241-69ae-11d9-bed3-505054503030) <span id="Audit_AccountLogon_KerbCredentialValidation"></span> <span id="audit_accountlogon_kerbcredentialvalidation"></span> <span id="AUDIT_ACCOUNTLOGON_KERBCREDENTIALVALIDATION"></span> **Audit \_ AccountLogon \_ KerbCredentialValidation** (0cce9242-69ae-11d9-bed3-505054503030) <span id="Audit_Logon_NPS"></span> <span id="audit_logon_nps"></span> <span id="AUDIT_LOGON_NPS"></span> **\_ Logon \_ NPS** überwachen (0cce9243-69ae-11d9-bed3-505054503030)
</dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntsecapi.h</dt> </dl> |



 

