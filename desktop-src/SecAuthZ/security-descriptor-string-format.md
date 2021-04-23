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
# <a name="security-descriptor-string-format"></a><span data-ttu-id="351ff-103">Sicherheitsdeskriptor-Zeichenfolgenformat</span><span class="sxs-lookup"><span data-stu-id="351ff-103">Security Descriptor String Format</span></span>

<span data-ttu-id="351ff-104">Das **Sicherheitsbeschreibungszeichenfolgenformat** ist ein Textformat zum Speichern oder Transport von Informationen in einem Sicherheitsdeskriptor.</span><span class="sxs-lookup"><span data-stu-id="351ff-104">The **Security Descriptor String Format** is a text format for storing or transporting information in a security descriptor.</span></span> <span data-ttu-id="351ff-105">Die [**Funktionen ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) und [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) verwenden dieses Format.</span><span class="sxs-lookup"><span data-stu-id="351ff-105">The [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use this format.</span></span>

<span data-ttu-id="351ff-106">Das Format ist eine mit **NULL** beendete Zeichenfolge mit Token, um jede der vier Hauptkomponenten eines Sicherheitsdeskriptors anzugeben: Besitzer (O:), primäre Gruppe (G:), DACL (D:) und SACL (S:).</span><span class="sxs-lookup"><span data-stu-id="351ff-106">The format is a **null**-terminated string with tokens to indicate each of the four main components of a security descriptor: owner (O:), primary group (G:), DACL (D:), and SACL (S:).</span></span>

> [!Note]  
> <span data-ttu-id="351ff-107">[*Zugriffssteuerungseinträge*](/windows/desktop/SecGloss/a-gly) (ACCESS Control Entries, ACEs) und bedingte ACEs haben unterschiedliche Formate.</span><span class="sxs-lookup"><span data-stu-id="351ff-107">[*Access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and conditional ACEs have differing formats.</span></span> <span data-ttu-id="351ff-108">Informationen zu ACEs finden Sie unter [ACE-Zeichenfolgen.](ace-strings.md)</span><span class="sxs-lookup"><span data-stu-id="351ff-108">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="351ff-109">Informationen zu bedingten ACEs finden Sie unter [Sicherheitsbeschreibungsdefinitionssprache für bedingte ACEs.](security-descriptor-definition-language-for-conditional-aces-.md)</span><span class="sxs-lookup"><span data-stu-id="351ff-109">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span data-ttu-id="351ff-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>owner \_ sid</span><span class="sxs-lookup"><span data-stu-id="351ff-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>owner\_sid</span></span>
</dt> <dd>

<span data-ttu-id="351ff-111">Eine [SID-Zeichenfolge,](sid-strings.md) die den Besitzer des Objekts identifiziert.</span><span class="sxs-lookup"><span data-stu-id="351ff-111">A [SID string](sid-strings.md) that identifies the object's owner.</span></span>

</dd> <dt>

<span data-ttu-id="351ff-112"><span id="group_sid"></span><span id="GROUP_SID"></span>group \_ sid</span><span class="sxs-lookup"><span data-stu-id="351ff-112"><span id="group_sid"></span><span id="GROUP_SID"></span>group\_sid</span></span>
</dt> <dd>

<span data-ttu-id="351ff-113">Eine SID-Zeichenfolge, die die primäre Gruppe des Objekts identifiziert.</span><span class="sxs-lookup"><span data-stu-id="351ff-113">A SID string that identifies the object's primary group.</span></span>

</dd> <dt>

<span data-ttu-id="351ff-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>\_dacl-Flags</span><span class="sxs-lookup"><span data-stu-id="351ff-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>dacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="351ff-115">Sicherheitsdeskriptor-Steuerungsflags, die für die DACL gelten.</span><span class="sxs-lookup"><span data-stu-id="351ff-115">Security descriptor control flags that apply to the DACL.</span></span> <span data-ttu-id="351ff-116">Eine Beschreibung dieser Steuerelementflags finden Sie in der [**SetSecurityDescriptorControl-Funktion.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol)</span><span class="sxs-lookup"><span data-stu-id="351ff-116">For a description of these control flags, see the [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) function.</span></span> <span data-ttu-id="351ff-117">Die Dacl-Flagzeichenfolge kann eine Verkettung von \_ 0 (null) oder mehr der folgenden Zeichenfolgen sein.</span><span class="sxs-lookup"><span data-stu-id="351ff-117">The dacl\_flags string can be a concatenation of zero or more of the following strings.</span></span>



| <span data-ttu-id="351ff-118">Control</span><span class="sxs-lookup"><span data-stu-id="351ff-118">Control</span></span>               | <span data-ttu-id="351ff-119">Konstante in Sddl.h</span><span class="sxs-lookup"><span data-stu-id="351ff-119">Constant in Sddl.h</span></span>       | <span data-ttu-id="351ff-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="351ff-120">Meaning</span></span>                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| <span data-ttu-id="351ff-121">"P"</span><span class="sxs-lookup"><span data-stu-id="351ff-121">"P"</span></span>                   | <span data-ttu-id="351ff-122">SDDL \_ PROTECTED</span><span class="sxs-lookup"><span data-stu-id="351ff-122">SDDL\_PROTECTED</span></span>          | <span data-ttu-id="351ff-123">Das SE \_ DACL \_ PROTECTED-Flag ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="351ff-123">The SE\_DACL\_PROTECTED flag is set.</span></span>          |
| <span data-ttu-id="351ff-124">"AR"</span><span class="sxs-lookup"><span data-stu-id="351ff-124">"AR"</span></span>                  | <span data-ttu-id="351ff-125">SDDL \_ AUTO \_ INHERIT \_ REQ</span><span class="sxs-lookup"><span data-stu-id="351ff-125">SDDL\_AUTO\_INHERIT\_REQ</span></span> | <span data-ttu-id="351ff-126">Das SE \_ DACL \_ AUTO INHERIT \_ \_ REQ-Flag ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="351ff-126">The SE\_DACL\_AUTO\_INHERIT\_REQ flag is set.</span></span> |
| <span data-ttu-id="351ff-127">"KI"</span><span class="sxs-lookup"><span data-stu-id="351ff-127">"AI"</span></span>                  | <span data-ttu-id="351ff-128">SDDL \_ AUTOMATISCH \_ GEERBT</span><span class="sxs-lookup"><span data-stu-id="351ff-128">SDDL\_AUTO\_INHERITED</span></span>    | <span data-ttu-id="351ff-129">Das SE \_ DACL \_ AUTO \_ INHERITED-Flag ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="351ff-129">The SE\_DACL\_AUTO\_INHERITED flag is set.</span></span>    |
| <span data-ttu-id="351ff-130">"NO ACCESS CONTROL" (KEINE \_ \_ ZUGRIFFSSTEUERUNG)</span><span class="sxs-lookup"><span data-stu-id="351ff-130">"NO\_ACCESS\_CONTROL"</span></span> | <span data-ttu-id="351ff-131">SDDL \_ \_ NULL-ACL</span><span class="sxs-lookup"><span data-stu-id="351ff-131">SDDL\_NULL\_ACL</span></span>          | <span data-ttu-id="351ff-132">Die ACL ist NULL.</span><span class="sxs-lookup"><span data-stu-id="351ff-132">The ACL is null.</span></span>                              |



 

</dd> <dt>

<span data-ttu-id="351ff-133"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>\_sacl-Flags</span><span class="sxs-lookup"><span data-stu-id="351ff-133"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="351ff-134">Sicherheitsdeskriptor-Steuerungsflags, die für die SACL gelten.</span><span class="sxs-lookup"><span data-stu-id="351ff-134">Security descriptor control flags that apply to the SACL.</span></span> <span data-ttu-id="351ff-135">Die \_ Sacl-Flagzeichenfolge verwendet die gleichen Steuerbitzeichenfolgen wie die \_ Dacl-Flagzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="351ff-135">The sacl\_flags string uses the same control bit strings as the dacl\_flags string.</span></span>

</dd> <dt>

<span data-ttu-id="351ff-136"><span id="string_ace"></span><span id="STRING_ACE"></span>string \_ ace</span><span class="sxs-lookup"><span data-stu-id="351ff-136"><span id="string_ace"></span><span id="STRING_ACE"></span>string\_ace</span></span>
</dt> <dd>

<span data-ttu-id="351ff-137">Eine Zeichenfolge, die einen ACE in der DACL oder SACL des Sicherheitsdeskriptors beschreibt.</span><span class="sxs-lookup"><span data-stu-id="351ff-137">A string that describes an ACE in the security descriptor's DACL or SACL.</span></span> <span data-ttu-id="351ff-138">Eine Beschreibung des ACE-Zeichenfolgenformats finden Sie unter [ACE-Zeichenfolgen.](ace-strings.md)</span><span class="sxs-lookup"><span data-stu-id="351ff-138">For a description of the ACE string format, see [ACE strings](ace-strings.md).</span></span> <span data-ttu-id="351ff-139">Jede ACE-Zeichenfolge wird in Klammern (()) eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="351ff-139">Each ACE string is enclosed in parentheses (()).</span></span>

</dd> </dl>

<span data-ttu-id="351ff-140">Nicht benötigte Komponenten können aus der Sicherheitsbeschreibungszeichenfolge weggelassen werden.</span><span class="sxs-lookup"><span data-stu-id="351ff-140">Unneeded components can be omitted from the security descriptor string.</span></span> <span data-ttu-id="351ff-141">Wenn beispielsweise das SE \_ DACL \_ PRESENT-Flag nicht im Eingabesicherheitsdeskriptor festgelegt ist, enthält [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) keine D:-Komponente in der Ausgabezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="351ff-141">For example, if the SE\_DACL\_PRESENT flag is not set in the input security descriptor, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) does not include a D: component in the output string.</span></span> <span data-ttu-id="351ff-142">Sie können auch die [**SECURITY INFORMATION-Bitflags \_**](security-information.md) verwenden, um die Komponenten anzugeben, die in eine Sicherheitsbeschreibungszeichenfolge eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="351ff-142">You can also use the [**SECURITY\_INFORMATION**](security-information.md) bit flags to indicate the components to include in a security descriptor string.</span></span>

<span data-ttu-id="351ff-143">Das Format der Sicherheitsbeschreibungszeichenfolge unterstützt keine **NULL-ACLs.**</span><span class="sxs-lookup"><span data-stu-id="351ff-143">The security descriptor string format does not support **NULL** ACLs.</span></span>

<span data-ttu-id="351ff-144">Um eine leere ACL zu bezeichnen, enthält die Sicherheitsbeschreibungszeichenfolge das Token D: oder S: ohne zusätzliche Zeichenfolgeninformationen.</span><span class="sxs-lookup"><span data-stu-id="351ff-144">To denote an empty ACL, the security descriptor string includes the D: or S: token with no additional string information.</span></span>

<span data-ttu-id="351ff-145">Die Sicherheitsbeschreibungszeichenfolge speichert die [**SECURITY DESCRIPTOR CONTROL-Bits**](security-descriptor-control.md) auf unterschiedliche Weise.</span><span class="sxs-lookup"><span data-stu-id="351ff-145">The security descriptor string stores the [**SECURITY DESCRIPTOR CONTROL**](security-descriptor-control.md) bits in different ways.</span></span> <span data-ttu-id="351ff-146">Die SE DACL PRESENT- oder SE SACL PRESENT-Bits werden durch das Vorhandensein des \_ \_ Tokens \_ \_ D: oder S: in der Zeichenfolge angegeben.</span><span class="sxs-lookup"><span data-stu-id="351ff-146">The SE\_DACL\_PRESENT or SE\_SACL\_PRESENT bits are indicated by the presence of the D: or S: token in the string.</span></span> <span data-ttu-id="351ff-147">Andere Bits, die für die DACL oder SACL gelten, werden in \_ Dacl-Flags und Sacl-Flags \_ gespeichert.</span><span class="sxs-lookup"><span data-stu-id="351ff-147">Other bits that apply to the DACL or SACL are stored in dacl\_flags and sacl\_flags.</span></span> <span data-ttu-id="351ff-148">Die SE \_ OWNER \_ DEFAULTED-, SE \_ GROUP \_ DEFAULTED-, SE \_ DACL DEFAULTED- und SE SACL DEFAULTED-Bits werden nicht in einer \_ Sicherheitsbeschreibungszeichenfolge \_ \_ gespeichert.</span><span class="sxs-lookup"><span data-stu-id="351ff-148">The SE\_OWNER\_DEFAULTED, SE\_GROUP\_DEFAULTED, SE\_DACL\_DEFAULTED, and SE\_SACL\_DEFAULTED bits are not stored in a security descriptor string.</span></span> <span data-ttu-id="351ff-149">Das SE SELF RELATIVE-Bit wird nicht in der Zeichenfolge \_ \_ gespeichert, [**convertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) legt dieses Bit jedoch immer im Ausgabesicherheitsdeskriptor fest.</span><span class="sxs-lookup"><span data-stu-id="351ff-149">The SE\_SELF\_RELATIVE bit is not stored in the string, but [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) always sets this bit in the output security descriptor.</span></span>

<span data-ttu-id="351ff-150">Die folgenden Beispiele zeigen Sicherheitsbeschreibungszeichenfolgen und die Informationen in den zugeordneten Sicherheitsbeschreibungen.</span><span class="sxs-lookup"><span data-stu-id="351ff-150">The following examples show security descriptor strings and the information in the associated security descriptors.</span></span>

<span data-ttu-id="351ff-151">Zeichenfolge 1:</span><span class="sxs-lookup"><span data-stu-id="351ff-151">String 1:</span></span>


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



<span data-ttu-id="351ff-152">Sicherheitsbeschreibung 1:</span><span class="sxs-lookup"><span data-stu-id="351ff-152">Security Descriptor 1:</span></span>


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



<span data-ttu-id="351ff-153">Zeichenfolge 2:</span><span class="sxs-lookup"><span data-stu-id="351ff-153">String 2:</span></span>


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



<span data-ttu-id="351ff-154">Sicherheitsbeschreibung 2:</span><span class="sxs-lookup"><span data-stu-id="351ff-154">Security Descriptor 2:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="351ff-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="351ff-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="351ff-156">ACE-Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="351ff-156">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="351ff-157">Definitionssprache für Sicherheitsbeschreibungen für bedingte ACEs</span><span class="sxs-lookup"><span data-stu-id="351ff-157">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
