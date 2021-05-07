---
description: Das Zeichenfolgenformat der Sicherheitsbeschreibung ist ein Textformat zum Speichern oder Übertragen von Informationen in einem Sicherheitsdeskriptor.
ms.assetid: 0a226629-084c-40c5-bdd4-ad7355c807cf
title: Security Descriptor String Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7fd6e9e2387deee63b5046086ed167a29fa54b
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644202"
---
# <a name="security-descriptor-string-format"></a>Security Descriptor String Format

Das **Zeichenfolgenformat** der Sicherheitsbeschreibung ist ein Textformat zum Speichern oder Übertragen von Informationen in einem Sicherheitsdeskriptor. Die Funktionen [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) und [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) verwenden dieses Format.

Das Format ist eine **mit NULL** endende Zeichenfolge mit Token, die jede der vier Hauptkomponenten einer Sicherheitsbeschreibung angibt: Besitzer (O:), primäre Gruppe (G:), DACL (D:) und SACL (S:).

> [!Note]  
> [*Zugriffssteuerungseinträge (ACEs)*](/windows/desktop/SecGloss/a-gly) und bedingte ACEs weisen unterschiedliche Formate auf. AcEs finden Sie unter [ACE-Zeichenfolgen.](ace-strings.md) Informationen zu bedingten ACEs finden Sie unter [Sicherheitsbeschreibungsdefinitionssprache für bedingte ACEs.](security-descriptor-definition-language-for-conditional-aces-.md)

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span id="owner_sid"></span><span id="OWNER_SID"></span>\_Besitzer-SID
</dt> <dd>

Eine [SID-Zeichenfolge,](sid-strings.md) die den Besitzer des Objekts identifiziert.

</dd> <dt>

<span id="group_sid"></span><span id="GROUP_SID"></span>\_Gruppen-SID
</dt> <dd>

Eine SID-Zeichenfolge, die die primäre Gruppe des Objekts identifiziert.

</dd> <dt>

<span id="dacl_flags"></span><span id="DACL_FLAGS"></span>\_dacl-Flags
</dt> <dd>

Sicherheitsbeschreibungs-Steuerelementflags, die für die DACL gelten. Eine Beschreibung dieser Steuerelementflags finden Sie in der [**SetSecurityDescriptorControl-Funktion.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) Die \_ Dacl-Flagzeichenfolge kann eine Verkettung von 0 (null) oder mehr der folgenden Zeichenfolgen sein.



| Control               | Konstante in "Sddl.h"       | Bedeutung                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| "P"                   | SDDL \_ PROTECTED          | Das SE \_ DACL \_ PROTECTED-Flag ist festgelegt.          |
| "AR"                  | SDDL \_ AUTO \_ INHERIT \_ REQ | Das SE \_ DACL \_ AUTO INHERIT \_ \_ REQ-Flag ist festgelegt. |
| "KI"                  | SDDL \_ AUTOMATISCH \_ GEERBT    | Das SE \_ DACL \_ AUTO \_ INHERITED-Flag ist festgelegt.    |
| "KEINE \_ \_ ZUGRIFFSSTEUERUNG" | SDDL \_ \_ NULL-ACL          | Die ACL ist NULL. **Windows Server 2008, Windows Vista und Windows Server 2003:** Nicht verfügbar. |



 

</dd> <dt>

<span id="sacl_flags"></span><span id="SACL_FLAGS"></span>\_sacl-Flags
</dt> <dd>

Sicherheitsdeskriptor-Steuerelementflags, die für die SACL gelten. Die \_ Sacl-Flagzeichenfolge verwendet dieselben Steuerbitzeichenfolgen wie die \_ dacl-Flagzeichenfolge.

</dd> <dt>

<span id="string_ace"></span><span id="STRING_ACE"></span>string \_ ace
</dt> <dd>

Eine Zeichenfolge, die einen ACE in der DACL oder SACL des Sicherheitsdeskriptors beschreibt. Eine Beschreibung des ACE-Zeichenfolgenformats finden Sie unter [ACE-Zeichenfolgen.](ace-strings.md) Jede ACE-Zeichenfolge ist in Klammern (()) eingeschlossen.

</dd> </dl>

Nicht mehr verwendete Komponenten können in der Sicherheitsbeschreibungszeichenfolge weggelassen werden. Wenn das SE DACL PRESENT-Flag beispielsweise nicht im Eingabesicherheitsdeskriptor festgelegt ist, enthält \_ \_ [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) keine D:-Komponente in der Ausgabezeichenfolge. Sie können auch die [**SECURITY INFORMATION-Bitflags \_**](security-information.md) verwenden, um die Komponenten anzugeben, die in eine Sicherheitsbeschreibungszeichenfolge eingeschlossen werden sollen.

Das Format der Sicherheitsbeschreibungszeichenfolge unterstützt keine **NULL-ACLs.**

Um eine leere ACL zu kennzeichnen, enthält die Sicherheitsbeschreibungszeichenfolge das Token D: oder S: ohne zusätzliche Zeichenfolgeninformationen.

Die Sicherheitsbeschreibungszeichenfolge speichert die [**SECURITY DESCRIPTOR**](security-descriptor-control.md) CONTROL-Bits auf unterschiedliche Weise. Die SE \_ DACL \_ PRESENT- oder SE \_ SACL \_ PRESENT-Bits werden durch das Vorhandensein des Tokens D: oder S: in der Zeichenfolge angegeben. Andere Bits, die für die DACL oder SACL gelten, werden in \_ Dacl-Flags und \_ sacl-Flags gespeichert. Die \_ Bits SE OWNER \_ DEFAULTED, SE \_ GROUP \_ DEFAULTED, SE \_ DACL \_ DEFAULTED und SE \_ SACL \_ DEFAULTED werden nicht in einer Sicherheitsbeschreibungszeichenfolge gespeichert. Das SE \_ SELF \_ RELATIVE-Bit wird nicht in der Zeichenfolge gespeichert, aber [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) legt dieses Bit immer im Ausgabesicherheitsdeskriptor fest.

Die folgenden Beispiele zeigen Sicherheitsbeschreibungszeichenfolgen und die Informationen in den zugeordneten Sicherheitsbeschreibungen.

Zeichenfolge 1:


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



Sicherheitsbeschreibung 1:


```C++
    Revision:  0x00000001
    Control:   0x0004
        SE_DACL_PRESENT
    Owner: (S-1-5-32-548)
    PrimaryGroup: (S-1-5-21-397955417-626881126-188441444-512)
DACL
    Revision: 0x02
    Size:     0x001c
    AceCount: 0x0001
    Ace[00]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x100e003f
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            GENERIC_ALL
                            Others(0x0000003f)
        Ace Sid      : (S-1-0-0)
SACL
    Not present
```



Zeichenfolge 2:


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



Sicherheitsbeschreibung 2:


```C++
    Revision:  0x00000001
    Control:   0x0014
        SE_DACL_PRESENT
        SE_SACL_PRESENT
    Owner: (S-1-5-21-397955417-626881126-188441444-512)
    PrimaryGroup: (S-1-5-21-397955417-626881126-188441444-512)
DACL
    Revision: 0x04
    Size:     0x0104
    AceCount: 0x0007
    Ace[00]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x000f003f
                            DELETE
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            Others(0x0000003f)
        Ace Sid:       (S-1-5-18)
    Ace[01]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0024
        InheritFlags:  0x00
        Access Mask:   0x000f003f
                            DELETE
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            Others(0x0000003f)
        Ace Sid:       (S-1-5-21-397955417-626881126-188441444-512)
    Ace[02]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_USER
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[03]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_GROUP
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[04]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_LOCALGROUP
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[05]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_PRINT_QUEUE
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-550)
    Ace[06]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x00020014
                            READ_CONTROL
                            Others(0x00000014)
        Ace Sid:       (S-1-5-11)
    SACL
        Revision: 0x02
        Size:     0x001c
        AceCount: 0x0001
        Ace[00]
            AceType:       0x02 (SYSTEM_AUDIT_ACE_TYPE)
            AceSize:       0x0014
            InheritFlags:  0xc0
                SUCCESSFUL_ACCESS_ACE_FLAG
                FAILED_ACCESS_ACE_FLAG
            Access Mask:    0x000d002b
                                DELETE
                                WRITE_DAC
                                WRITE_OWNER
                                Others(0x0000002b)
            Ace Sid:       (S-1-1-0)
```



## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[ACE-Zeichenfolgen](ace-strings.md)
</dt> <dt>

[Sicherheitsdeskriptordefinitionssprache für bedingte ACEs](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
