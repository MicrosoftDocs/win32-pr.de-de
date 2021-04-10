---
description: Das Format der Sicherheits Deskriptor-Zeichenfolge ist ein Text Format zum Speichern oder Transportieren von Informationen in einer Sicherheits Beschreibung.
ms.assetid: 0a226629-084c-40c5-bdd4-ad7355c807cf
title: Format der Sicherheits Deskriptor-Zeichenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f5182de796ee8d3c61f079d3704ab29ad552457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863008"
---
# <a name="security-descriptor-string-format"></a>Format der Sicherheits Deskriptor-Zeichenfolge

Das **Format der Sicherheits Deskriptor-Zeichen** Folge ist ein Text Format zum Speichern oder Transportieren von Informationen in einer Sicherheits Beschreibung. Die [**convertsecuritydescriptortostringsecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) -Funktion und die [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) -Funktion verwenden dieses Format.

Das Format ist eine **null**-terminierte Zeichenfolge mit Token zum Angeben der vier Hauptkomponenten einer Sicherheits Beschreibung: Owner (O:), Primary Group (G:), DACL (D:) und SACL (S:)).

> [!Note]  
> [*Zugriffs Steuerungs Einträge*](/windows/desktop/SecGloss/a-gly) (ACEs) und bedingte ACEs haben unterschiedliche Formate. Informationen zu ACEs finden Sie unter [ACE](ace-strings.md)-Zeichen folgen. Informationen zu bedingten ACEs finden Sie unter [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span id="owner_sid"></span><span id="OWNER_SID"></span>Besitzer- \_ sid
</dt> <dd>

Eine [sid-Zeichenfolge](sid-strings.md) , die den Besitzer des Objekts identifiziert.

</dd> <dt>

<span id="group_sid"></span><span id="GROUP_SID"></span>Gruppen- \_ sid
</dt> <dd>

Eine SID-Zeichenfolge, die die primäre Gruppe des Objekts identifiziert.

</dd> <dt>

<span id="dacl_flags"></span><span id="DACL_FLAGS"></span>DACL- \_ Flags
</dt> <dd>

Sicherheitsbeschreibungssteuerungflags, die auf die DACL angewendet werden. Eine Beschreibung dieser steuerungflags finden Sie unter der [**setsecuritydescriptorcontrol**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) -Funktion. Die DACL- \_ Flags-Zeichenfolge kann eine Verkettung von NULL oder mehr der folgenden Zeichen folgen sein.



| Control               | Konstante in SDDL. h       | Bedeutung                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| Cker                   | SDDL- \_ geschützt          | Das SE \_ DACL \_ Protected-Flag ist festgelegt.          |
| Tempel                  | Automatische SDDL- \_ \_ Vererbung \_ | Das \_ \_ Flag für die automatische Vererbung von SE DACL \_ \_ wird festgelegt. |
| Serei                  | SDDL \_ automatisch \_ geerbt    | Das \_ \_ Flag für die automatische Vererbung von SE DACL \_ wird festgelegt.    |
| "keine \_ Zugriffs \_ Steuerung" | SSDL- \_ NULL- \_ ACL          | Die ACL ist NULL.                              |



 

</dd> <dt>

<span id="sacl_flags"></span><span id="SACL_FLAGS"></span>SACL- \_ Flags
</dt> <dd>

Sicherheitsbeschreibungssteuerungflags, die auf die SACL angewendet werden. Die SACL- \_ Flags-Zeichenfolge verwendet dieselben Steuerungs Bitzeichenfolgen wie die DACL- \_ Flags-Zeichenfolge.

</dd> <dt>

<span id="string_ace"></span><span id="STRING_ACE"></span>String- \_ ACE
</dt> <dd>

Eine Zeichenfolge, die einen ACE in der DACL oder SACL der Sicherheits Beschreibung beschreibt. Eine Beschreibung des ACE-Zeichen folgen Formats finden Sie unter [ACE](ace-strings.md)-Zeichen folgen. Jede ACE-Zeichenfolge wird in Klammern (()) eingeschlossen.

</dd> </dl>

Nicht benötigte Komponenten können aus der Sicherheits beschreibungzeichenfolge ausgelassen werden. Wenn z. \_ b. das Flag "SE DACL \_ Present" nicht in der Eingabe Sicherheits Beschreibung festgelegt ist, enthält [**convertsecuritydescriptortostringsecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) keine "D:"-Komponente in der Ausgabe Zeichenfolge. Sie können auch die Bitflags für [**Sicherheits \_ Informationen**](security-information.md) verwenden, um die Komponenten anzugeben, die in eine Sicherheits Beschreibungszeichenfolge eingeschlossen werden sollen.

Das Format der Sicherheits Deskriptor-Zeichenfolge unterstützt keine **null** -ACLs.

Um eine leere Zugriffs Steuerungs Liste anzugeben, enthält die sicherheitsbeschreibungerzeichenfolge das Token "D:" oder "S:" ohne zusätzliche Zeichen folgen Informationen.

In der Sicherheits beschreibungenzeichenfolge werden die Bits der [**Sicherheits Deskriptor-Steuer**](security-descriptor-control.md) Elemente auf verschiedene Weise gespeichert Die vorhandene SE-DACL, die vorhandene Bits enthalten, \_ \_ \_ \_ wird durch das vorhanden sein des D:-oder S:-Tokens in der Zeichenfolge angezeigt. Andere Bits, die für die DACL oder SACL gelten, werden in DACL \_ -Flags und SACL- \_ Flags gespeichert. Der Standard \_ -SE-Besitzer, die standardmäßig SE \_ \_ \_ -Gruppe, die SE DACL-Standardeinstellungen und die standardmäßigen \_ \_ SE \_ SACL- \_ Bits werden nicht in einer Sicherheits Deskriptorzeichenfolge gespeichert. Das SE \_ Self \_ relative Bit ist nicht in der Zeichenfolge gespeichert, aber [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) legt dieses Bit immer in der Ausgabe Sicherheits Beschreibung fest.

In den folgenden Beispielen werden sicherheitsbeschreibungerzeichenfolgen und die Informationen in den zugeordneten Sicherheits Deskriptoren gezeigt.

Zeichenfolge 1:


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



Sicherheits Beschreibung 1:


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



Sicherheits Beschreibung 2:


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

[ACE-Zeichen folgen](ace-strings.md)
</dt> <dt>

[Sicherheits Deskriptor-Definitions Sprache für bedingte ACEs](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
