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
# <a name="security-descriptor-string-format"></a><span data-ttu-id="26665-103">Format der Sicherheits Deskriptor-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="26665-103">Security Descriptor String Format</span></span>

<span data-ttu-id="26665-104">Das **Format der Sicherheits Deskriptor-Zeichen** Folge ist ein Text Format zum Speichern oder Transportieren von Informationen in einer Sicherheits Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="26665-104">The **Security Descriptor String Format** is a text format for storing or transporting information in a security descriptor.</span></span> <span data-ttu-id="26665-105">Die [**convertsecuritydescriptortostringsecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) -Funktion und die [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) -Funktion verwenden dieses Format.</span><span class="sxs-lookup"><span data-stu-id="26665-105">The [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use this format.</span></span>

<span data-ttu-id="26665-106">Das Format ist eine **null**-terminierte Zeichenfolge mit Token zum Angeben der vier Hauptkomponenten einer Sicherheits Beschreibung: Owner (O:), Primary Group (G:), DACL (D:) und SACL (S:)).</span><span class="sxs-lookup"><span data-stu-id="26665-106">The format is a **null**-terminated string with tokens to indicate each of the four main components of a security descriptor: owner (O:), primary group (G:), DACL (D:), and SACL (S:).</span></span>

> [!Note]  
> <span data-ttu-id="26665-107">[*Zugriffs Steuerungs Einträge*](/windows/desktop/SecGloss/a-gly) (ACEs) und bedingte ACEs haben unterschiedliche Formate.</span><span class="sxs-lookup"><span data-stu-id="26665-107">[*Access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and conditional ACEs have differing formats.</span></span> <span data-ttu-id="26665-108">Informationen zu ACEs finden Sie unter [ACE](ace-strings.md)-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="26665-108">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="26665-109">Informationen zu bedingten ACEs finden Sie unter [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="26665-109">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span data-ttu-id="26665-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>Besitzer- \_ sid</span><span class="sxs-lookup"><span data-stu-id="26665-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>owner\_sid</span></span>
</dt> <dd>

<span data-ttu-id="26665-111">Eine [sid-Zeichenfolge](sid-strings.md) , die den Besitzer des Objekts identifiziert.</span><span class="sxs-lookup"><span data-stu-id="26665-111">A [SID string](sid-strings.md) that identifies the object's owner.</span></span>

</dd> <dt>

<span data-ttu-id="26665-112"><span id="group_sid"></span><span id="GROUP_SID"></span>Gruppen- \_ sid</span><span class="sxs-lookup"><span data-stu-id="26665-112"><span id="group_sid"></span><span id="GROUP_SID"></span>group\_sid</span></span>
</dt> <dd>

<span data-ttu-id="26665-113">Eine SID-Zeichenfolge, die die primäre Gruppe des Objekts identifiziert.</span><span class="sxs-lookup"><span data-stu-id="26665-113">A SID string that identifies the object's primary group.</span></span>

</dd> <dt>

<span data-ttu-id="26665-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>DACL- \_ Flags</span><span class="sxs-lookup"><span data-stu-id="26665-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>dacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="26665-115">Sicherheitsbeschreibungssteuerungflags, die auf die DACL angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="26665-115">Security descriptor control flags that apply to the DACL.</span></span> <span data-ttu-id="26665-116">Eine Beschreibung dieser steuerungflags finden Sie unter der [**setsecuritydescriptorcontrol**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="26665-116">For a description of these control flags, see the [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) function.</span></span> <span data-ttu-id="26665-117">Die DACL- \_ Flags-Zeichenfolge kann eine Verkettung von NULL oder mehr der folgenden Zeichen folgen sein.</span><span class="sxs-lookup"><span data-stu-id="26665-117">The dacl\_flags string can be a concatenation of zero or more of the following strings.</span></span>



| <span data-ttu-id="26665-118">Control</span><span class="sxs-lookup"><span data-stu-id="26665-118">Control</span></span>               | <span data-ttu-id="26665-119">Konstante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="26665-119">Constant in Sddl.h</span></span>       | <span data-ttu-id="26665-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="26665-120">Meaning</span></span>                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| <span data-ttu-id="26665-121">Cker</span><span class="sxs-lookup"><span data-stu-id="26665-121">"P"</span></span>                   | <span data-ttu-id="26665-122">SDDL- \_ geschützt</span><span class="sxs-lookup"><span data-stu-id="26665-122">SDDL\_PROTECTED</span></span>          | <span data-ttu-id="26665-123">Das SE \_ DACL \_ Protected-Flag ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="26665-123">The SE\_DACL\_PROTECTED flag is set.</span></span>          |
| <span data-ttu-id="26665-124">Tempel</span><span class="sxs-lookup"><span data-stu-id="26665-124">"AR"</span></span>                  | <span data-ttu-id="26665-125">Automatische SDDL- \_ \_ Vererbung \_</span><span class="sxs-lookup"><span data-stu-id="26665-125">SDDL\_AUTO\_INHERIT\_REQ</span></span> | <span data-ttu-id="26665-126">Das \_ \_ Flag für die automatische Vererbung von SE DACL \_ \_ wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="26665-126">The SE\_DACL\_AUTO\_INHERIT\_REQ flag is set.</span></span> |
| <span data-ttu-id="26665-127">Serei</span><span class="sxs-lookup"><span data-stu-id="26665-127">"AI"</span></span>                  | <span data-ttu-id="26665-128">SDDL \_ automatisch \_ geerbt</span><span class="sxs-lookup"><span data-stu-id="26665-128">SDDL\_AUTO\_INHERITED</span></span>    | <span data-ttu-id="26665-129">Das \_ \_ Flag für die automatische Vererbung von SE DACL \_ wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="26665-129">The SE\_DACL\_AUTO\_INHERITED flag is set.</span></span>    |
| <span data-ttu-id="26665-130">"keine \_ Zugriffs \_ Steuerung"</span><span class="sxs-lookup"><span data-stu-id="26665-130">"NO\_ACCESS\_CONTROL"</span></span> | <span data-ttu-id="26665-131">SSDL- \_ NULL- \_ ACL</span><span class="sxs-lookup"><span data-stu-id="26665-131">SSDL\_NULL\_ACL</span></span>          | <span data-ttu-id="26665-132">Die ACL ist NULL.</span><span class="sxs-lookup"><span data-stu-id="26665-132">The ACL is null.</span></span>                              |



 

</dd> <dt>

<span data-ttu-id="26665-133"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>SACL- \_ Flags</span><span class="sxs-lookup"><span data-stu-id="26665-133"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="26665-134">Sicherheitsbeschreibungssteuerungflags, die auf die SACL angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="26665-134">Security descriptor control flags that apply to the SACL.</span></span> <span data-ttu-id="26665-135">Die SACL- \_ Flags-Zeichenfolge verwendet dieselben Steuerungs Bitzeichenfolgen wie die DACL- \_ Flags-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="26665-135">The sacl\_flags string uses the same control bit strings as the dacl\_flags string.</span></span>

</dd> <dt>

<span data-ttu-id="26665-136"><span id="string_ace"></span><span id="STRING_ACE"></span>String- \_ ACE</span><span class="sxs-lookup"><span data-stu-id="26665-136"><span id="string_ace"></span><span id="STRING_ACE"></span>string\_ace</span></span>
</dt> <dd>

<span data-ttu-id="26665-137">Eine Zeichenfolge, die einen ACE in der DACL oder SACL der Sicherheits Beschreibung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="26665-137">A string that describes an ACE in the security descriptor's DACL or SACL.</span></span> <span data-ttu-id="26665-138">Eine Beschreibung des ACE-Zeichen folgen Formats finden Sie unter [ACE](ace-strings.md)-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="26665-138">For a description of the ACE string format, see [ACE strings](ace-strings.md).</span></span> <span data-ttu-id="26665-139">Jede ACE-Zeichenfolge wird in Klammern (()) eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="26665-139">Each ACE string is enclosed in parentheses (()).</span></span>

</dd> </dl>

<span data-ttu-id="26665-140">Nicht benötigte Komponenten können aus der Sicherheits beschreibungzeichenfolge ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="26665-140">Unneeded components can be omitted from the security descriptor string.</span></span> <span data-ttu-id="26665-141">Wenn z. \_ b. das Flag "SE DACL \_ Present" nicht in der Eingabe Sicherheits Beschreibung festgelegt ist, enthält [**convertsecuritydescriptortostringsecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) keine "D:"-Komponente in der Ausgabe Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="26665-141">For example, if the SE\_DACL\_PRESENT flag is not set in the input security descriptor, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) does not include a D: component in the output string.</span></span> <span data-ttu-id="26665-142">Sie können auch die Bitflags für [**Sicherheits \_ Informationen**](security-information.md) verwenden, um die Komponenten anzugeben, die in eine Sicherheits Beschreibungszeichenfolge eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="26665-142">You can also use the [**SECURITY\_INFORMATION**](security-information.md) bit flags to indicate the components to include in a security descriptor string.</span></span>

<span data-ttu-id="26665-143">Das Format der Sicherheits Deskriptor-Zeichenfolge unterstützt keine **null** -ACLs.</span><span class="sxs-lookup"><span data-stu-id="26665-143">The security descriptor string format does not support **NULL** ACLs.</span></span>

<span data-ttu-id="26665-144">Um eine leere Zugriffs Steuerungs Liste anzugeben, enthält die sicherheitsbeschreibungerzeichenfolge das Token "D:" oder "S:" ohne zusätzliche Zeichen folgen Informationen.</span><span class="sxs-lookup"><span data-stu-id="26665-144">To denote an empty ACL, the security descriptor string includes the D: or S: token with no additional string information.</span></span>

<span data-ttu-id="26665-145">In der Sicherheits beschreibungenzeichenfolge werden die Bits der [**Sicherheits Deskriptor-Steuer**](security-descriptor-control.md) Elemente auf verschiedene Weise gespeichert</span><span class="sxs-lookup"><span data-stu-id="26665-145">The security descriptor string stores the [**SECURITY DESCRIPTOR CONTROL**](security-descriptor-control.md) bits in different ways.</span></span> <span data-ttu-id="26665-146">Die vorhandene SE-DACL, die vorhandene Bits enthalten, \_ \_ \_ \_ wird durch das vorhanden sein des D:-oder S:-Tokens in der Zeichenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="26665-146">The SE\_DACL\_PRESENT or SE\_SACL\_PRESENT bits are indicated by the presence of the D: or S: token in the string.</span></span> <span data-ttu-id="26665-147">Andere Bits, die für die DACL oder SACL gelten, werden in DACL \_ -Flags und SACL- \_ Flags gespeichert.</span><span class="sxs-lookup"><span data-stu-id="26665-147">Other bits that apply to the DACL or SACL are stored in dacl\_flags and sacl\_flags.</span></span> <span data-ttu-id="26665-148">Der Standard \_ -SE-Besitzer, die standardmäßig SE \_ \_ \_ -Gruppe, die SE DACL-Standardeinstellungen und die standardmäßigen \_ \_ SE \_ SACL- \_ Bits werden nicht in einer Sicherheits Deskriptorzeichenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="26665-148">The SE\_OWNER\_DEFAULTED, SE\_GROUP\_DEFAULTED, SE\_DACL\_DEFAULTED, and SE\_SACL\_DEFAULTED bits are not stored in a security descriptor string.</span></span> <span data-ttu-id="26665-149">Das SE \_ Self \_ relative Bit ist nicht in der Zeichenfolge gespeichert, aber [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) legt dieses Bit immer in der Ausgabe Sicherheits Beschreibung fest.</span><span class="sxs-lookup"><span data-stu-id="26665-149">The SE\_SELF\_RELATIVE bit is not stored in the string, but [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) always sets this bit in the output security descriptor.</span></span>

<span data-ttu-id="26665-150">In den folgenden Beispielen werden sicherheitsbeschreibungerzeichenfolgen und die Informationen in den zugeordneten Sicherheits Deskriptoren gezeigt.</span><span class="sxs-lookup"><span data-stu-id="26665-150">The following examples show security descriptor strings and the information in the associated security descriptors.</span></span>

<span data-ttu-id="26665-151">Zeichenfolge 1:</span><span class="sxs-lookup"><span data-stu-id="26665-151">String 1:</span></span>


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



<span data-ttu-id="26665-152">Sicherheits Beschreibung 1:</span><span class="sxs-lookup"><span data-stu-id="26665-152">Security Descriptor 1:</span></span>


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



<span data-ttu-id="26665-153">Zeichenfolge 2:</span><span class="sxs-lookup"><span data-stu-id="26665-153">String 2:</span></span>


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



<span data-ttu-id="26665-154">Sicherheits Beschreibung 2:</span><span class="sxs-lookup"><span data-stu-id="26665-154">Security Descriptor 2:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="26665-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26665-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26665-156">ACE-Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="26665-156">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="26665-157">Sicherheits Deskriptor-Definitions Sprache für bedingte ACEs</span><span class="sxs-lookup"><span data-stu-id="26665-157">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
