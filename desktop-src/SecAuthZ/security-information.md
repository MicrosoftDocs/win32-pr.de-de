---
description: Identifiziert die objektbezogenen Sicherheitsinformationen, die festgelegt oder abgefragt werden.
ms.assetid: e3e8b35d-9d18-4611-a898-72ca13e40d33
title: SECURITY_INFORMATION (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaad4b9f61a20b26397081433b88782dcbc33f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214820"
---
# <a name="security_information"></a>Sicherheits \_ Informationen

Der Datentyp **Sicherheits \_ Informationen** identifiziert die objektbezogenen Sicherheitsinformationen, die festgelegt oder abgefragt werden. Diese Sicherheitsinformationen umfassen Folgendes:

-   Der Besitzer eines Objekts.
-   Die primäre Gruppe eines Objekts.
-   Die freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) eines Objekts.
-   Die [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) eines Objekts


```C++
typedef DWORD SECURITY_INFORMATION, *PSECURITY_INFORMATION;
```



## <a name="remarks"></a>Bemerkungen

Einige Mitglieder von **Sicherheits \_ Informationen** arbeiten nur mit der Funktion [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) . Diese Member werden in der Struktur, die von anderen Sicherheitsfunktionen wie [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) oder [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)zurückgegeben wird, nicht zurückgegeben.

Jedes Element von Sicherheitsinformationen wird durch ein Bitflag angegeben. Jedes Bitflag kann einen der folgenden Werte aufweisen. Weitere Informationen finden Sie unter den Funktionen [**setsecurityaccessmask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask) und [**querysecurityaccessmask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask) .



| Zum Abfragen/festlegen Erforderlicher Wert/Rechte                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Attribut \_ Sicherheits \_ Informationen<br/> Zum Abfragen erforderliches Recht: **Read- \_ Steuer** Element<br/> Zum Festlegen erforderliches Recht **: \_ DAC schreiben**<br/>                                                                                     | Die Ressourcen Eigenschaften des Objekts, auf das verwiesen wird. Die Ressourcen Eigenschaften werden im System \_ Ressourcen \_ Attribut- \_ ACE-Typ in der SACL der Sicherheits Beschreibung gespeichert.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieses Bitflag ist nicht verfügbar.<br/> <br/>                 |
| \_Sicherheits \_ Informationen zur Sicherung<br/> Zum Abfragen erforderliches Recht **: \_ Lese** -und **Zugriffs \_ System \_ Sicherheit**<br/> Zum Festlegen der Rechte erforderlich: **Schreiben von \_ DAC** und **Schreiben von \_ Besitzer** -und **Zugriffs \_ System \_ Sicherheit**<br/> | Alle Teile der Sicherheits Beschreibung. Dies ist nützlich für Sicherungs-und Wiederherstellungssoftware, die die gesamte Sicherheits Beschreibung beibehalten muss.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieses Bitflag ist nicht verfügbar.<br/> <br/>                                                  |
| DACL- \_ Sicherheits \_ Informationen<br/> Zum Abfragen erforderliches Recht: **Read- \_ Steuer** Element<br/> Zum Festlegen erforderliches Recht **: \_ DAC schreiben**<br/>                                                                                          | Auf die DACL des Objekts wird verwiesen.<br/>                                                                                                                                                                                                                                                                                                                        |
| Gruppen \_ Sicherheits \_ Informationen<br/> Zum Abfragen erforderliches Recht: **Read- \_ Steuer** Element<br/> Zum Festlegen von rechten erforderlich: **Schreib \_ Besitzer** <br/>                                                                                      | Auf den primären Gruppen Bezeichner des Objekts wird verwiesen.<br/>                                                                                                                                                                                                                                                                                                    |
| \_Sicherheits \_ Informationen zur Bezeichnung<br/> Zum Abfragen erforderliches Recht: **Read- \_ Steuer** Element<br/> Zum Festlegen von rechten erforderlich: **Schreib \_ Besitzer** <br/>                                                                                      | Es wird auf die obligatorische Integritäts Bezeichnung verwiesen.<br/> Die obligatorische Integritäts Bezeichnung ist ein ACE in der SACL des Objekts.<br/> **Windows Server 2003 und Windows XP:** Dieses Bitflag ist nicht verfügbar.<br/> <br/>                                                                                                                                    |
| \_Sicherheits \_ Informationen für den Besitzer<br/> Zum Abfragen erforderliches Recht: **Read- \_ Steuer** Element<br/> Zum Festlegen von rechten erforderlich: **Schreib \_ Besitzer** <br/>                                                                                      | Auf den Besitzer Bezeichner des Objekts wird verwiesen.<br/>                                                                                                                                                                                                                                                                                                            |
| geschützte \_ DACL- \_ Sicherheits \_ Informationen<br/> Zum Abfragen erforderliches Recht: nicht verfügbar<br/> Zum Festlegen erforderliches Recht **: \_ DAC schreiben**<br/>                                                                                   | Die DACL kann keine [*Zugriffs Steuerungs Einträge*](/windows/desktop/SecGloss/a-gly) (ACEs) erben.<br/>                                                                                                                                                                                                                   |
| geschützte \_ SACL- \_ Sicherheits \_ Informationen<br/> Zum Abfragen erforderliches Recht: nicht verfügbar<br/> Zum Festlegen des Zugriffs auf **\_ System \_ Sicherheit** erforderlich.<br/>                                                                     | Die SACL kann keine ACEs erben.<br/>                                                                                                                                                                                                                                                                                                                                      |
| SACL- \_ Sicherheits \_ Informationen<br/> Zum Abfragen erforderliches Recht: Zugriff auf die **\_ System \_ Sicherheit**<br/> Zum Festlegen des Zugriffs auf **\_ System \_ Sicherheit** erforderlich.<br/>                                                                 | Auf die SACL des Objekts wird verwiesen.<br/>                                                                                                                                                                                                                                                                                                                        |
| Informationen zur Bereichs \_ Sicherheit \_<br/> Zum Abfragen erforderliches Recht: **Read- \_ Steuer** Element<br/> Zum Festlegen des Zugriffs auf **\_ System \_ Sicherheit** erforderlich.<br/>                                                                           | Der Bezeichner für die zentrale Zugriffs Richtlinie (Cap), der auf das Objekt anwendbar ist, auf das verwiesen wird. Jeder Cap-Bezeichner wird in einem \_ Richtlinien-ID-ACE-Typ der System weiten \_ Richtlinie \_ \_ in der SACL der SD gespeichert.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieses Bitflag ist nicht verfügbar.<br/> <br/> |
| ungeschützte \_ DACL- \_ Sicherheits \_ Informationen<br/> Zum Abfragen erforderliches Recht: nicht verfügbar<br/> Zum Festlegen erforderliches Recht **: \_ DAC schreiben**<br/>                                                                                 | Die DACL erbt ACEs von dem übergeordneten Objekt.<br/>                                                                                                                                                                                                                                                                                                                     |
| ungeschützte \_ SACL- \_ Sicherheits \_ Informationen<br/> Zum Abfragen erforderliches Recht: nicht verfügbar<br/> Zum Festlegen des Zugriffs auf **\_ System \_ Sicherheit** erforderlich.<br/>                                                                   | Die SACL erbt ACEs von dem übergeordneten Objekt.<br/>                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>WinNT. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Zugriffssteuerung](access-control.md)
</dt> <dt>

[Grundlegende Access Control Strukturen](authorization-structures.md)
</dt> <dt>

[**Convertsecuritydescriptortostringsecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
</dt> <dt>

[**Wurde von convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)
</dt> <dt>

[**Getfilesecurity**](/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[**Getkernelobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)
</dt> <dt>

[**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)
</dt> <dt>

[**GetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity)
</dt> <dt>

[**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)
</dt> <dt>

[**Getuserobjectsecurity**](/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity)
</dt> <dt>

[**Querysecurityaccessmask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask)
</dt> <dt>

[**Setfilesecurity**](/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya)
</dt> <dt>

[**Setkernelobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity)
</dt> <dt>

[**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)
</dt> <dt>

[**Setprivateobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)
</dt> <dt>

[**Setsecurityaccessmask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask)
</dt> <dt>

[**Setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[**Setuserobjectsecurity**](/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity)
</dt> <dt>

[**Treeresetnamedsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-treeresetnamedsecurityinfoa)
</dt> <dt>

[**Treesetnamedsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-treesetnamedsecurityinfoa)
</dt> </dl>

 

