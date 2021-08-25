---
description: Identifiziert die objektbezogenen Sicherheitsinformationen, die festgelegt oder abgefragt werden.
ms.assetid: e3e8b35d-9d18-4611-a898-72ca13e40d33
title: SECURITY_INFORMATION (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eda92db81cc2325dcc2eb084c06aa5ac7ca92475cca92d8221e394af9704c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907200"
---
# <a name="security_information"></a>\_SICHERHEITSINFORMATIONEN

Der **SECURITY \_ INFORMATION-Datentyp** identifiziert die objektbezogenen Sicherheitsinformationen, die festgelegt oder abgefragt werden. Diese Sicherheitsinformationen umfassen Folgendes:

-   Der Besitzer eines Objekts
-   Die primäre Gruppe eines Objekts
-   Die [*DACL (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) eines Objekts
-   Die [*Systemzugriffssteuerungsliste*](/windows/desktop/SecGloss/s-gly) (SACL) eines Objekts


```C++
typedef DWORD SECURITY_INFORMATION, *PSECURITY_INFORMATION;
```



## <a name="remarks"></a>Hinweise

Einige **SECURITY \_ INFORMATION-Member** funktionieren nur mit der [**SetNamedSecurityInfo-Funktion.**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) Diese Member werden nicht in der -Struktur zurückgegeben, die von anderen Sicherheitsfunktionen wie [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) oder [**ConvertStringSecurityDescriptorToSecurityDescriptor zurückgegeben wird.**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

Jedes Element von Sicherheitsinformationen wird durch ein Bitflag festgelegt. Jedes Bitflag kann einer der folgenden Werte sein. Weitere Informationen finden Sie unter den [**Funktionen SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask) und [**QuerySecurityAccessMask.**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask)



| Für abfragen/festlegen erforderliche Werte/Rechte                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ ATTRIBUTSICHERHEITSINFORMATIONEN<br/> Recht zum Abfragen erforderlich: **READ \_ CONTROL**<br/> Recht zum Festlegen erforderlich: **WRITE \_ DAC**<br/>                                                                                     | Die Ressourceneigenschaften des Objekts, auf das verwiesen wird. Die Ressourceneigenschaften werden in DEN ACE-Typen von SYSTEM \_ RESOURCE ATTRIBUTE in der \_ \_ SACL des Sicherheitsdeskriptors gespeichert.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003** und Windows XP: Dieses Bitflag ist nicht verfügbar.<br/> <br/>                 |
| \_ \_ SICHERUNGSSICHERHEITSINFORMATIONEN<br/> Recht zum Abfragen erforderlich: **READ \_ CONTROL** und **ACCESS SYSTEM \_ \_ SECURITY**<br/> Erforderliches Recht zum Festlegen: **WRITE \_ DAC** und **WRITE \_ OWNER** und **ACCESS SYSTEM \_ \_ SECURITY**<br/> | Alle Teile der Sicherheitsbeschreibung. Dies ist nützlich für die Sicherung und Wiederherstellung von Software, die die gesamte Sicherheitsbeschreibung beibehalten muss.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003** und Windows XP: Dieses Bitflag ist nicht verfügbar.<br/> <br/>                                                  |
| \_DACL-SICHERHEITSINFORMATIONEN \_<br/> Recht zum Abfragen erforderlich: **READ \_ CONTROL**<br/> Recht zum Festlegen erforderlich: **WRITE \_ DAC**<br/>                                                                                          | Auf die DACL des Objekts wird verwiesen.<br/>                                                                                                                                                                                                                                                                                                                        |
| \_ \_ GRUPPENSICHERHEITSINFORMATIONEN<br/> Recht zum Abfragen erforderlich: **READ \_ CONTROL**<br/> Recht zum Festlegen erforderlich: **WRITE \_ OWNER** <br/>                                                                                      | Auf den primären Gruppenbezeichner des Objekts wird verwiesen.<br/>                                                                                                                                                                                                                                                                                                    |
| \_ \_ BEZEICHNUNGSSICHERHEITSINFORMATIONEN<br/> Recht zum Abfragen erforderlich: **READ \_ CONTROL**<br/> Recht zum Festlegen erforderlich: **WRITE \_ OWNER** <br/>                                                                                      | Auf die obligatorische Integritätsbezeichnung wird verwiesen.<br/> Die obligatorische Integritätsbezeichnung ist ein ACE in der SACL des Objekts.<br/> **Windows Server 2003 und Windows XP:** Dieses Bitflag ist nicht verfügbar.<br/> <br/>                                                                                                                                    |
| \_ \_ BESITZERSICHERHEITSINFORMATIONEN<br/> Recht zum Abfragen erforderlich: **READ \_ CONTROL**<br/> Recht zum Festlegen erforderlich: **WRITE \_ OWNER** <br/>                                                                                      | Auf den Besitzerbezeichner des Objekts wird verwiesen.<br/>                                                                                                                                                                                                                                                                                                            |
| GESCHÜTZTE \_ \_ DACL-SICHERHEITSINFORMATIONEN \_<br/> Recht zum Abfragen erforderlich: Nicht verfügbar<br/> Recht zum Festlegen erforderlich: **WRITE \_ DAC**<br/>                                                                                   | Die DACL kann keine [*Zugriffssteuerungseinträge*](/windows/desktop/SecGloss/a-gly) (ACEs) erben.<br/>                                                                                                                                                                                                                   |
| GESCHÜTZTE \_ \_ SACL-SICHERHEITSINFORMATIONEN \_<br/> Recht zum Abfragen erforderlich: Nicht verfügbar<br/> Erforderliches Recht zum Festlegen: **ACCESS \_ SYSTEM \_ SECURITY**<br/>                                                                     | Die SACL kann keine ACEs erben.<br/>                                                                                                                                                                                                                                                                                                                                      |
| \_SACL-SICHERHEITSINFORMATIONEN \_<br/> Recht zum Abfragen erforderlich: **ACCESS \_ SYSTEM \_ SECURITY**<br/> Erforderliches Recht zum Festlegen: **ACCESS \_ SYSTEM \_ SECURITY**<br/>                                                                 | Auf die SACL des Objekts wird verwiesen.<br/>                                                                                                                                                                                                                                                                                                                        |
| \_ \_ BEREICHSSICHERHEITSINFORMATIONEN<br/> Recht zum Abfragen erforderlich: **READ \_ CONTROL**<br/> Erforderliches Recht zum Festlegen: **ACCESS \_ SYSTEM \_ SECURITY**<br/>                                                                           | Der Bezeichner der zentralen Zugriffsrichtlinie (CENTRAL ACCESS Policy, CAP), der für das Objekt gilt, auf das verwiesen wird. Jeder CAP-Bezeichner wird in einem ACE-Typ der SYSTEM \_ SCOPED \_ POLICY ID in \_ der \_ SACL der SD gespeichert.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003** und Windows XP: Dieses Bitflag ist nicht verfügbar.<br/> <br/> |
| UNGESCHÜTZTE \_ \_ DACL-SICHERHEITSINFORMATIONEN \_<br/> Recht zum Abfragen erforderlich: Nicht verfügbar<br/> Recht zum Festlegen erforderlich: **WRITE \_ DAC**<br/>                                                                                 | Die DACL erbt ACEs vom übergeordneten Objekt.<br/>                                                                                                                                                                                                                                                                                                                     |
| UNGESCHÜTZTE \_ \_ SACL-SICHERHEITSINFORMATIONEN \_<br/> Recht zum Abfragen erforderlich: Nicht verfügbar<br/> Erforderliches Recht zum Festlegen: **ACCESS \_ SYSTEM \_ SECURITY**<br/>                                                                   | Die SACL erbt ACEs vom übergeordneten Objekt.<br/>                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Winnt.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Zugriffssteuerung](access-control.md)
</dt> <dt>

[Grundlegende Access Control Strukturen](authorization-structures.md)
</dt> <dt>

[**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
</dt> <dt>

[**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)
</dt> <dt>

[**GetFileSecurity**](/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[**GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)
</dt> <dt>

[**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)
</dt> <dt>

[**GetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity)
</dt> <dt>

[**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)
</dt> <dt>

[**GetUserObjectSecurity**](/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity)
</dt> <dt>

[**QuerySecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask)
</dt> <dt>

[**SetFileSecurity**](/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya)
</dt> <dt>

[**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity)
</dt> <dt>

[**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)
</dt> <dt>

[**SetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)
</dt> <dt>

[**SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask)
</dt> <dt>

[**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[**SetUserObjectSecurity**](/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity)
</dt> <dt>

[**TreeResetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-treeresetnamedsecurityinfoa)
</dt> <dt>

[**TreeSetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-treesetnamedsecurityinfoa)
</dt> </dl>

 

