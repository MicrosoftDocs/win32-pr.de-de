---
description: Ein Satz von Bitflags, die die Bedeutung einer Sicherheits Beschreibung oder ihrer Komponenten qualifizieren.
ms.assetid: 9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2
title: SECURITY_DESCRIPTOR_CONTROL (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3def788407093d0a487640d1ad0e445b61fe20e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347228"
---
# <a name="security_descriptor_control"></a>Sicherheits \_ Deskriptor- \_ Steuerelement

Der Datentyp der **\_ sicherheitsbeschreibungssteuerung \_** ist ein Satz von Bitflags, die die Bedeutung einer [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) oder ihrer Komponenten qualifizieren. Jede Sicherheits Beschreibung verfügt über ein **Steuer** Element, das die **Sicherheits \_ Deskriptor- \_ Steuerungs** Bits speichert.


```C++
typedef WORD SECURITY_DESCRIPTOR_CONTROL, *PSECURITY_DESCRIPTOR_CONTROL;
```



## <a name="remarks"></a>Bemerkungen

Um die Steuerungs Bits einer Sicherheits Beschreibung abzurufen, müssen Sie die [**getsecuritydescriptorcontrol**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) -Funktion aufrufen. Verwenden Sie zum Festlegen der Steuerungs Bits einer Sicherheits Beschreibung die Funktionen zum Ändern von Sicherheits Beschreibungen. Eine Liste dieser Funktionen finden Sie im Abschnitt "Siehe auch".

Anwendungen können die [**setsecuritydescriptorcontrol**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) -Funktion verwenden, um die Steuerungs Bits festzulegen, die sich auf die automatische Vererbung von ACEs beziehen.

Der Steuerelement Wert, der von der [**getsecuritydescriptorcontrol**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) -Funktion abgerufen wird, kann eine Kombination der folgenden Bitflags für **\_ sicherheitsbeschreibungssteuerelemente \_** enthalten.



| Wert                                                     | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SE \_ DACL \_ Auto \_ erben von \_ req<br/> 0x0100<br/> | Gibt einen erforderlichen [*Sicherheits Deskriptor*](/windows/desktop/SecGloss/s-gly) an, in dem die freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) so eingerichtet ist, dass die Automatische Propagierung von vererbbaren [*Zugriffs Steuerungs Einträgen*](/windows/desktop/SecGloss/a-gly) (ACEs) an vorhandene untergeordnete Objekte unterstützt wird.<br/> Für [*Zugriffs Steuerungs Listen*](/windows/desktop/SecGloss/a-gly) (ACLs), die die automatische Vererbung unterstützen, wird dieses Bit immer festgelegt. Geschützte Server können die [**converttoautovererprivateobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) -Funktion aufrufen, um eine Sicherheits Beschreibung zu konvertieren und dieses Flag festzulegen. <br/> |
| SE \_ DACL \_ automatisch \_ geerbt<br/> 0x0400<br/>    | Gibt eine Sicherheits Beschreibung an, in der die freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) so eingerichtet ist, dass die Automatische Propagierung von vererbbaren [*Zugriffs Steuerungs Einträgen*](/windows/desktop/SecGloss/a-gly) (ACEs) an vorhandene untergeordnete Objekte unterstützt wird.<br/> Für [*Zugriffs Steuerungs Listen*](/windows/desktop/SecGloss/a-gly) (ACLs), die die automatische Vererbung unterstützen, wird dieses Bit immer festgelegt. Geschützte Server können die [**converttoautovererprivateobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) -Funktion aufrufen, um eine Sicherheits Beschreibung zu konvertieren und dieses Flag festzulegen. <br/>                                                                                                  |
| SE \_ DACL \_ default<br/> 0x0008<br/>          | Gibt eine Sicherheits Beschreibung mit einer Standard-DACL an. Wenn z. b. der Ersteller eines Objekts keine DACL angibt, empfängt das Objekt die Standard-DACL vom [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) des Erstellers. Dieses Flag kann beeinflussen, wie das System die DACL in Bezug auf die ACE-Vererbung behandelt. Das System ignoriert dieses Flag, wenn das \_ Flag "SE DACL \_ Present" nicht festgelegt ist.<br/> Dieses Flag wird verwendet, um zu bestimmen, wie die endgültige DACL des Objekts berechnet werden soll, und wird nicht physisch in der Sicherheits beschreibungssteuerung des Sicherungs fähigen Objekts gespeichert.<br/> Um dieses Flag festzulegen, verwenden Sie die Funktion [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) .<br/>                                                                                                                                                                      |
| SE \_ DACL \_ vorhanden<br/> 0x0004<br/>            | Gibt eine Sicherheits Beschreibung an, die über eine DACL verfügt. Wenn dieses Flag nicht festgelegt ist oder wenn dieses Flag festgelegt ist und die DACL **null** ist, ermöglicht die Sicherheits Beschreibung den vollständigen Zugriff auf alle.<br/> Dieses Flag wird zum Speichern der von einem Aufrufer angegebenen Sicherheitsinformationen verwendet, bis die Sicherheits Beschreibung einem Sicherungs fähigen Objekt zugeordnet ist. Nachdem die Sicherheits Beschreibung einem Sicherungs fähigen Objekt zugeordnet ist, wird das Flag für die SE \_ DACL \_ Present immer im Sicherheits beschreibungssteuerelement festgelegt.<br/> Um dieses Flag festzulegen, verwenden Sie die Funktion [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) .<br/>                                                                                                                                                                                                                                                                                                   |
| SE \_ DACL \_ Protected<br/> 0x1000<br/>          | Verhindert, dass die DACL der Sicherheits Beschreibung durch vererbbare ACEs geändert wird. Um dieses Flag festzulegen, verwenden Sie die [**setsecuritydescriptorcontrol**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) -Funktion.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| standardmäßig für SE- \_ Gruppe \_<br/> 0x0002<br/>         | Gibt an, dass die [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID) der Sicherheits beschreibungergruppe von einem Standardmechanismus bereitgestellt wurde. Dieses Flag kann von einem Ressourcen-Manager zur Identifizierung von Objekten verwendet werden, deren sicherheitsbeschreibungsgruppe durch einen Standardmechanismus festgelegt wurde. Um dieses Flag festzulegen, verwenden Sie die Funktion [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Standard der SE- \_ Besitzer \_<br/> 0x0001<br/>         | Gibt an, dass die SID des Besitzers der Sicherheits Beschreibung von einem Standardmechanismus bereitgestellt wurde. Dieses Flag kann von einem Ressourcen-Manager zur Identifizierung von Objekten verwendet werden, deren Besitzer von einem Standardmechanismus festgelegt wurde. Um dieses Flag festzulegen, verwenden Sie die Funktion [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SE \_ RM- \_ Steuerelement \_ gültig<br/> 0x4000<br/>       | Gibt an, dass das Resource Manager-Steuerelement gültig ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| SE \_ SACL \_ Auto \_ erben von \_ req<br/> 0x0200<br/> | Gibt einen erforderlichen Sicherheits Deskriptor an, in dem die [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) so eingerichtet ist, dass die automatische Weitergabe von vererbbaren ACEs an vorhandene untergeordnete Objekte unterstützt wird.<br/> Das System legt dieses Bit fest, wenn es den automatischen Vererbungs Algorithmus für das-Objekt und dessen vorhandene untergeordnete Objekte ausführt. Um eine Sicherheits Beschreibung zu konvertieren und dieses Flag festzulegen, können geschützte Server die [**converttoautovererprivateobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) -Funktion aufrufen.<br/>                                                                                                                                                                                                                                                                                   |
| SE \_ SACL \_ automatisch \_ geerbt<br/> 0x0800<br/>    | Gibt eine Sicherheits Beschreibung an, in der die [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) zur Unterstützung der automatischen Propagierung von vererbbaren ACEs an vorhandene untergeordnete Objekte eingerichtet ist.<br/> Das System legt dieses Bit fest, wenn es den automatischen Vererbungs Algorithmus für das-Objekt und dessen vorhandene untergeordnete Objekte ausführt. Um eine Sicherheits Beschreibung zu konvertieren und dieses Flag festzulegen, können geschützte Server die [**converttoautovererprivateobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) -Funktion aufrufen. <br/>                                                                                                                                                                                                                                                                                           |
| SE \_ SACL \_ default<br/> 0x0008<br/>          | Die SACL wurde von einem Standardmechanismus anstelle des ursprünglichen [*Anbieters*](/windows/desktop/SecGloss/p-gly) der Sicherheits Beschreibung bereitgestellt. Dieses Flag kann beeinflussen, wie das System die SACL behandelt, in Bezug auf die ACE-Vererbung. Das System ignoriert dieses Flag, wenn das \_ Flag für die SE SACL \_ Present nicht festgelegt ist. Um dieses Flag festzulegen, verwenden Sie die [**setsecuritydescriptorsacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) -Funktion.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| SE \_ SACL \_ vorhanden<br/> 0x0010<br/>            | Gibt eine Sicherheits Beschreibung an, die eine SACL aufweist. Um dieses Flag festzulegen, verwenden Sie die [**setsecuritydescriptorsacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) -Funktion.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SE \_ SACL \_ Protected<br/> 0x2000<br/>          | Verhindert, dass die SACL der Sicherheits Beschreibung durch vererbbare ACEs geändert wird. Um dieses Flag festzulegen, verwenden Sie die [**setsecuritydescriptorcontrol**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) -Funktion.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SE \_ Self \_ relative<br/> 0x8000<br/>           | Gibt einen [*selbst relativen Sicherheits Deskriptor*](/windows/desktop/SecGloss/s-gly)an. Wenn dieses Flag nicht festgelegt ist, hat die Sicherheits Beschreibung das absolute Format. Weitere Informationen finden Sie unter [absolute und Self-Relative Sicherheits Deskriptoren](absolute-and-self-relative-security-descriptors.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>WinNT. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Access Control auf niedriger Ebene](low-level-access-control.md)
</dt> <dt>

[Grundlegende Access Control Strukturen](authorization-structures.md)
</dt> <dt>

[**ConvertTo autovererprivateobjectsecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity)
</dt> <dt>

[**Getsecuritydescriptor Control**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol)
</dt> <dt>

[**Getsecuritydescriptor DACL**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)
</dt> <dt>

[**Getsecuritydescriptorgroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup)
</dt> <dt>

[**GetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)
</dt> <dt>

[**Getsecuritydescriptor SACL**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)
</dt> <dt>

[**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol)
</dt> <dt>

[**"SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)
</dt> <dt>

[**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)
</dt> <dt>

[**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)
</dt> <dt>

[**SETSECURITYDESCRIPTOR SACL**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)
</dt> </dl>

 

