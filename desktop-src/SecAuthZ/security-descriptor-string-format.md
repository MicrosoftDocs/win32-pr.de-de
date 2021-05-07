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
# <a name="security-descriptor-string-format"></a><span data-ttu-id="52758-103">Security Descriptor String Format</span><span class="sxs-lookup"><span data-stu-id="52758-103">Security Descriptor String Format</span></span>

<span data-ttu-id="52758-104">Das **Zeichenfolgenformat** der Sicherheitsbeschreibung ist ein Textformat zum Speichern oder Übertragen von Informationen in einem Sicherheitsdeskriptor.</span><span class="sxs-lookup"><span data-stu-id="52758-104">The **Security Descriptor String Format** is a text format for storing or transporting information in a security descriptor.</span></span> <span data-ttu-id="52758-105">Die Funktionen [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) und [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) verwenden dieses Format.</span><span class="sxs-lookup"><span data-stu-id="52758-105">The [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use this format.</span></span>

<span data-ttu-id="52758-106">Das Format ist eine **mit NULL** endende Zeichenfolge mit Token, die jede der vier Hauptkomponenten einer Sicherheitsbeschreibung angibt: Besitzer (O:), primäre Gruppe (G:), DACL (D:) und SACL (S:).</span><span class="sxs-lookup"><span data-stu-id="52758-106">The format is a **null**-terminated string with tokens to indicate each of the four main components of a security descriptor: owner (O:), primary group (G:), DACL (D:), and SACL (S:).</span></span>

> [!Note]  
> <span data-ttu-id="52758-107">[*Zugriffssteuerungseinträge (ACEs)*](/windows/desktop/SecGloss/a-gly) und bedingte ACEs weisen unterschiedliche Formate auf.</span><span class="sxs-lookup"><span data-stu-id="52758-107">[*Access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and conditional ACEs have differing formats.</span></span> <span data-ttu-id="52758-108">AcEs finden Sie unter [ACE-Zeichenfolgen.](ace-strings.md)</span><span class="sxs-lookup"><span data-stu-id="52758-108">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="52758-109">Informationen zu bedingten ACEs finden Sie unter [Sicherheitsbeschreibungsdefinitionssprache für bedingte ACEs.](security-descriptor-definition-language-for-conditional-aces-.md)</span><span class="sxs-lookup"><span data-stu-id="52758-109">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span data-ttu-id="52758-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>\_Besitzer-SID</span><span class="sxs-lookup"><span data-stu-id="52758-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>owner\_sid</span></span>
</dt> <dd>

<span data-ttu-id="52758-111">Eine [SID-Zeichenfolge,](sid-strings.md) die den Besitzer des Objekts identifiziert.</span><span class="sxs-lookup"><span data-stu-id="52758-111">A [SID string](sid-strings.md) that identifies the object's owner.</span></span>

</dd> <dt>

<span data-ttu-id="52758-112"><span id="group_sid"></span><span id="GROUP_SID"></span>\_Gruppen-SID</span><span class="sxs-lookup"><span data-stu-id="52758-112"><span id="group_sid"></span><span id="GROUP_SID"></span>group\_sid</span></span>
</dt> <dd>

<span data-ttu-id="52758-113">Eine SID-Zeichenfolge, die die primäre Gruppe des Objekts identifiziert.</span><span class="sxs-lookup"><span data-stu-id="52758-113">A SID string that identifies the object's primary group.</span></span>

</dd> <dt>

<span data-ttu-id="52758-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>\_dacl-Flags</span><span class="sxs-lookup"><span data-stu-id="52758-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>dacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="52758-115">Sicherheitsbeschreibungs-Steuerelementflags, die für die DACL gelten.</span><span class="sxs-lookup"><span data-stu-id="52758-115">Security descriptor control flags that apply to the DACL.</span></span> <span data-ttu-id="52758-116">Eine Beschreibung dieser Steuerelementflags finden Sie in der [**SetSecurityDescriptorControl-Funktion.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol)</span><span class="sxs-lookup"><span data-stu-id="52758-116">For a description of these control flags, see the [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) function.</span></span> <span data-ttu-id="52758-117">Die \_ Dacl-Flagzeichenfolge kann eine Verkettung von 0 (null) oder mehr der folgenden Zeichenfolgen sein.</span><span class="sxs-lookup"><span data-stu-id="52758-117">The dacl\_flags string can be a concatenation of zero or more of the following strings.</span></span>



| <span data-ttu-id="52758-118">Control</span><span class="sxs-lookup"><span data-stu-id="52758-118">Control</span></span>               | <span data-ttu-id="52758-119">Konstante in "Sddl.h"</span><span class="sxs-lookup"><span data-stu-id="52758-119">Constant in Sddl.h</span></span>       | <span data-ttu-id="52758-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="52758-120">Meaning</span></span>                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| <span data-ttu-id="52758-121">"P"</span><span class="sxs-lookup"><span data-stu-id="52758-121">"P"</span></span>                   | <span data-ttu-id="52758-122">SDDL \_ PROTECTED</span><span class="sxs-lookup"><span data-stu-id="52758-122">SDDL\_PROTECTED</span></span>          | <span data-ttu-id="52758-123">Das SE \_ DACL \_ PROTECTED-Flag ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="52758-123">The SE\_DACL\_PROTECTED flag is set.</span></span>          |
| <span data-ttu-id="52758-124">"AR"</span><span class="sxs-lookup"><span data-stu-id="52758-124">"AR"</span></span>                  | <span data-ttu-id="52758-125">SDDL \_ AUTO \_ INHERIT \_ REQ</span><span class="sxs-lookup"><span data-stu-id="52758-125">SDDL\_AUTO\_INHERIT\_REQ</span></span> | <span data-ttu-id="52758-126">Das SE \_ DACL \_ AUTO INHERIT \_ \_ REQ-Flag ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="52758-126">The SE\_DACL\_AUTO\_INHERIT\_REQ flag is set.</span></span> |
| <span data-ttu-id="52758-127">"KI"</span><span class="sxs-lookup"><span data-stu-id="52758-127">"AI"</span></span>                  | <span data-ttu-id="52758-128">SDDL \_ AUTOMATISCH \_ GEERBT</span><span class="sxs-lookup"><span data-stu-id="52758-128">SDDL\_AUTO\_INHERITED</span></span>    | <span data-ttu-id="52758-129">Das SE \_ DACL \_ AUTO \_ INHERITED-Flag ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="52758-129">The SE\_DACL\_AUTO\_INHERITED flag is set.</span></span>    |
| <span data-ttu-id="52758-130">"KEINE \_ \_ ZUGRIFFSSTEUERUNG"</span><span class="sxs-lookup"><span data-stu-id="52758-130">"NO\_ACCESS\_CONTROL"</span></span> | <span data-ttu-id="52758-131">SDDL \_ \_ NULL-ACL</span><span class="sxs-lookup"><span data-stu-id="52758-131">SDDL\_NULL\_ACL</span></span>          | <span data-ttu-id="52758-132">Die ACL ist NULL.</span><span class="sxs-lookup"><span data-stu-id="52758-132">The ACL is null.</span></span> <span data-ttu-id="52758-133">**Windows Server 2008, Windows Vista und Windows Server 2003:** Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="52758-133">**Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span> |



 

</dd> <dt>

<span data-ttu-id="52758-134"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>\_sacl-Flags</span><span class="sxs-lookup"><span data-stu-id="52758-134"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="52758-135">Sicherheitsdeskriptor-Steuerelementflags, die für die SACL gelten.</span><span class="sxs-lookup"><span data-stu-id="52758-135">Security descriptor control flags that apply to the SACL.</span></span> <span data-ttu-id="52758-136">Die \_ Sacl-Flagzeichenfolge verwendet dieselben Steuerbitzeichenfolgen wie die \_ dacl-Flagzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="52758-136">The sacl\_flags string uses the same control bit strings as the dacl\_flags string.</span></span>

</dd> <dt>

<span data-ttu-id="52758-137"><span id="string_ace"></span><span id="STRING_ACE"></span>string \_ ace</span><span class="sxs-lookup"><span data-stu-id="52758-137"><span id="string_ace"></span><span id="STRING_ACE"></span>string\_ace</span></span>
</dt> <dd>

<span data-ttu-id="52758-138">Eine Zeichenfolge, die einen ACE in der DACL oder SACL des Sicherheitsdeskriptors beschreibt.</span><span class="sxs-lookup"><span data-stu-id="52758-138">A string that describes an ACE in the security descriptor's DACL or SACL.</span></span> <span data-ttu-id="52758-139">Eine Beschreibung des ACE-Zeichenfolgenformats finden Sie unter [ACE-Zeichenfolgen.](ace-strings.md)</span><span class="sxs-lookup"><span data-stu-id="52758-139">For a description of the ACE string format, see [ACE strings](ace-strings.md).</span></span> <span data-ttu-id="52758-140">Jede ACE-Zeichenfolge ist in Klammern (()) eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="52758-140">Each ACE string is enclosed in parentheses (()).</span></span>

</dd> </dl>

<span data-ttu-id="52758-141">Nicht mehr verwendete Komponenten können in der Sicherheitsbeschreibungszeichenfolge weggelassen werden.</span><span class="sxs-lookup"><span data-stu-id="52758-141">Unneeded components can be omitted from the security descriptor string.</span></span> <span data-ttu-id="52758-142">Wenn das SE DACL PRESENT-Flag beispielsweise nicht im Eingabesicherheitsdeskriptor festgelegt ist, enthält \_ \_ [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) keine D:-Komponente in der Ausgabezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="52758-142">For example, if the SE\_DACL\_PRESENT flag is not set in the input security descriptor, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) does not include a D: component in the output string.</span></span> <span data-ttu-id="52758-143">Sie können auch die [**SECURITY INFORMATION-Bitflags \_**](security-information.md) verwenden, um die Komponenten anzugeben, die in eine Sicherheitsbeschreibungszeichenfolge eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="52758-143">You can also use the [**SECURITY\_INFORMATION**](security-information.md) bit flags to indicate the components to include in a security descriptor string.</span></span>

<span data-ttu-id="52758-144">Das Format der Sicherheitsbeschreibungszeichenfolge unterstützt keine **NULL-ACLs.**</span><span class="sxs-lookup"><span data-stu-id="52758-144">The security descriptor string format does not support **NULL** ACLs.</span></span>

<span data-ttu-id="52758-145">Um eine leere ACL zu kennzeichnen, enthält die Sicherheitsbeschreibungszeichenfolge das Token D: oder S: ohne zusätzliche Zeichenfolgeninformationen.</span><span class="sxs-lookup"><span data-stu-id="52758-145">To denote an empty ACL, the security descriptor string includes the D: or S: token with no additional string information.</span></span>

<span data-ttu-id="52758-146">Die Sicherheitsbeschreibungszeichenfolge speichert die [**SECURITY DESCRIPTOR**](security-descriptor-control.md) CONTROL-Bits auf unterschiedliche Weise.</span><span class="sxs-lookup"><span data-stu-id="52758-146">The security descriptor string stores the [**SECURITY DESCRIPTOR CONTROL**](security-descriptor-control.md) bits in different ways.</span></span> <span data-ttu-id="52758-147">Die SE \_ DACL \_ PRESENT- oder SE \_ SACL \_ PRESENT-Bits werden durch das Vorhandensein des Tokens D: oder S: in der Zeichenfolge angegeben.</span><span class="sxs-lookup"><span data-stu-id="52758-147">The SE\_DACL\_PRESENT or SE\_SACL\_PRESENT bits are indicated by the presence of the D: or S: token in the string.</span></span> <span data-ttu-id="52758-148">Andere Bits, die für die DACL oder SACL gelten, werden in \_ Dacl-Flags und \_ sacl-Flags gespeichert.</span><span class="sxs-lookup"><span data-stu-id="52758-148">Other bits that apply to the DACL or SACL are stored in dacl\_flags and sacl\_flags.</span></span> <span data-ttu-id="52758-149">Die \_ Bits SE OWNER \_ DEFAULTED, SE \_ GROUP \_ DEFAULTED, SE \_ DACL \_ DEFAULTED und SE \_ SACL \_ DEFAULTED werden nicht in einer Sicherheitsbeschreibungszeichenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="52758-149">The SE\_OWNER\_DEFAULTED, SE\_GROUP\_DEFAULTED, SE\_DACL\_DEFAULTED, and SE\_SACL\_DEFAULTED bits are not stored in a security descriptor string.</span></span> <span data-ttu-id="52758-150">Das SE \_ SELF \_ RELATIVE-Bit wird nicht in der Zeichenfolge gespeichert, aber [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) legt dieses Bit immer im Ausgabesicherheitsdeskriptor fest.</span><span class="sxs-lookup"><span data-stu-id="52758-150">The SE\_SELF\_RELATIVE bit is not stored in the string, but [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) always sets this bit in the output security descriptor.</span></span>

<span data-ttu-id="52758-151">Die folgenden Beispiele zeigen Sicherheitsbeschreibungszeichenfolgen und die Informationen in den zugeordneten Sicherheitsbeschreibungen.</span><span class="sxs-lookup"><span data-stu-id="52758-151">The following examples show security descriptor strings and the information in the associated security descriptors.</span></span>

<span data-ttu-id="52758-152">Zeichenfolge 1:</span><span class="sxs-lookup"><span data-stu-id="52758-152">String 1:</span></span>


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



<span data-ttu-id="52758-153">Sicherheitsbeschreibung 1:</span><span class="sxs-lookup"><span data-stu-id="52758-153">Security Descriptor 1:</span></span>


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



<span data-ttu-id="52758-154">Zeichenfolge 2:</span><span class="sxs-lookup"><span data-stu-id="52758-154">String 2:</span></span>


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



<span data-ttu-id="52758-155">Sicherheitsbeschreibung 2:</span><span class="sxs-lookup"><span data-stu-id="52758-155">Security Descriptor 2:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="52758-156">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="52758-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52758-157">ACE-Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="52758-157">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="52758-158">Sicherheitsdeskriptordefinitionssprache für bedingte ACEs</span><span class="sxs-lookup"><span data-stu-id="52758-158">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
