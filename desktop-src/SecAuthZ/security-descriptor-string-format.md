---
description: Das Sicherheitsbeschreibungszeichenfolgenformat ist ein Textformat zum Speichern oder Transport von Informationen in einem Sicherheitsdeskriptor.
ms.assetid: 0a226629-084c-40c5-bdd4-ad7355c807cf
title: Sicherheitsdeskriptor-Zeichenfolgenformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42780c408908faf0a226584be7315ab6bf9e78e5
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925682"
---
# <a name="security-descriptor-string-format"></a>Sicherheitsdeskriptor-Zeichenfolgenformat

Das **Sicherheitsbeschreibungszeichenfolgenformat** ist ein Textformat zum Speichern oder Transport von Informationen in einem Sicherheitsdeskriptor. Die [**Funktionen ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) und [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) verwenden dieses Format.

Das Format ist eine mit **NULL** beendete Zeichenfolge mit Token, um jede der vier Hauptkomponenten eines Sicherheitsdeskriptors anzugeben: Besitzer (O:), primäre Gruppe (G:), DACL (D:) und SACL (S:).

> [!Note]  
> [*Zugriffssteuerungseinträge*](/windows/desktop/SecGloss/a-gly) (ACCESS Control Entries, ACEs) und bedingte ACEs haben unterschiedliche Formate. Informationen zu ACEs finden Sie unter [ACE-Zeichenfolgen.](ace-strings.md) Informationen zu bedingten ACEs finden Sie unter [Sicherheitsbeschreibungsdefinitionssprache für bedingte ACEs.](security-descriptor-definition-language-for-conditional-aces-.md)

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span id="owner_sid"></span><span id="OWNER_SID"></span>owner \_ sid
</dt> <dd>

Eine [SID-Zeichenfolge,](sid-strings.md) die den Besitzer des Objekts identifiziert.

</dd> <dt>

<span id="group_sid"></span><span id="GROUP_SID"></span>group \_ sid
</dt> <dd>

Eine SID-Zeichenfolge, die die primäre Gruppe des Objekts identifiziert.

</dd> <dt>

<span id="dacl_flags"></span><span id="DACL_FLAGS"></span>\_dacl-Flags
</dt> <dd>

Sicherheitsdeskriptor-Steuerungsflags, die für die DACL gelten. Eine Beschreibung dieser Steuerelementflags finden Sie in der [**SetSecurityDescriptorControl-Funktion.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) Die Dacl-Flagzeichenfolge kann eine Verkettung von \_ 0 (null) oder mehr der folgenden Zeichenfolgen sein.



| Control               | Konstante in Sddl.h       | Bedeutung                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| "P"                   | SDDL \_ PROTECTED          | Das SE \_ DACL \_ PROTECTED-Flag ist festgelegt.          |
| "AR"                  | SDDL \_ AUTO \_ INHERIT \_ REQ | Das SE \_ DACL \_ AUTO INHERIT \_ \_ REQ-Flag ist festgelegt. |
| "KI"                  | SDDL \_ AUTOMATISCH \_ GEERBT    | Das SE \_ DACL \_ AUTO \_ INHERITED-Flag ist festgelegt.    |
| "NO ACCESS CONTROL" (KEINE \_ \_ ZUGRIFFSSTEUERUNG) | SDDL \_ \_ NULL-ACL          | Die ACL ist NULL.                              |



 

</dd> <dt>

<span id="sacl_flags"></span><span id="SACL_FLAGS"></span>\_sacl-Flags
</dt> <dd>

Sicherheitsdeskriptor-Steuerungsflags, die für die SACL gelten. Die \_ Sacl-Flagzeichenfolge verwendet die gleichen Steuerbitzeichenfolgen wie die \_ Dacl-Flagzeichenfolge.

</dd> <dt>

<span id="string_ace"></span><span id="STRING_ACE"></span>string \_ ace
</dt> <dd>

Eine Zeichenfolge, die einen ACE in der DACL oder SACL des Sicherheitsdeskriptors beschreibt. Eine Beschreibung des ACE-Zeichenfolgenformats finden Sie unter [ACE-Zeichenfolgen.](ace-strings.md) Jede ACE-Zeichenfolge wird in Klammern (()) eingeschlossen.

</dd> </dl>

Nicht benötigte Komponenten können aus der Sicherheitsbeschreibungszeichenfolge weggelassen werden. Wenn beispielsweise das SE \_ DACL \_ PRESENT-Flag nicht im Eingabesicherheitsdeskriptor festgelegt ist, enthält [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) keine D:-Komponente in der Ausgabezeichenfolge. Sie können auch die [**SECURITY INFORMATION-Bitflags \_**](security-information.md) verwenden, um die Komponenten anzugeben, die in eine Sicherheitsbeschreibungszeichenfolge eingeschlossen werden sollen.

Das Format der Sicherheitsbeschreibungszeichenfolge unterstützt keine **NULL-ACLs.**

Um eine leere ACL zu bezeichnen, enthält die Sicherheitsbeschreibungszeichenfolge das Token D: oder S: ohne zusätzliche Zeichenfolgeninformationen.

Die Sicherheitsbeschreibungszeichenfolge speichert die [**SECURITY DESCRIPTOR CONTROL-Bits**](security-descriptor-control.md) auf unterschiedliche Weise. Die SE DACL PRESENT- oder SE SACL PRESENT-Bits werden durch das Vorhandensein des \_ \_ Tokens \_ \_ D: oder S: in der Zeichenfolge angegeben. Andere Bits, die für die DACL oder SACL gelten, werden in \_ Dacl-Flags und Sacl-Flags \_ gespeichert. Die SE \_ OWNER \_ DEFAULTED-, SE \_ GROUP \_ DEFAULTED-, SE \_ DACL DEFAULTED- und SE SACL DEFAULTED-Bits werden nicht in einer \_ Sicherheitsbeschreibungszeichenfolge \_ \_ gespeichert. Das SE SELF RELATIVE-Bit wird nicht in der Zeichenfolge \_ \_ gespeichert, [**convertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) legt dieses Bit jedoch immer im Ausgabesicherheitsdeskriptor fest.

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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ACE-Zeichenfolgen](ace-strings.md)
</dt> <dt>

[Definitionssprache für Sicherheitsbeschreibungen für bedingte ACEs](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
