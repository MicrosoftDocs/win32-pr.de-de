---
description: Erläutert die Zeichen folgen, die in einem Zugriffs Steuerungs Eintrag verwendet werden.
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: ACE-Zeichen folgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a35bde18a1ca3ac416faa42e3b693e26305beb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756185"
---
# <a name="ace-strings"></a><span data-ttu-id="83039-103">ACE-Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="83039-103">ACE Strings</span></span>

<span data-ttu-id="83039-104">Die [Security Deskriptor Definition Language](security-descriptor-definition-language.md) (SDDL) verwendet ACE-Zeichen folgen in den DACL-und SACL-Komponenten einer [*sicherheitsbeschreibungerzeichenfolge*](/windows/desktop/SecGloss/s-gly) .</span><span class="sxs-lookup"><span data-stu-id="83039-104">The [security descriptor definition language](security-descriptor-definition-language.md) (SDDL) uses ACE strings in the DACL and SACL components of a [*security descriptor*](/windows/desktop/SecGloss/s-gly) string.</span></span>

<span data-ttu-id="83039-105">Wie in den Beispielen für das [Format der Sicherheits Deskriptor-Zeichen](security-descriptor-string-format.md) Folge gezeigt, wird jeder ACE in einer sicherheitsbeschreibungerzeichenfolge in Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="83039-105">As shown in the [Security Descriptor String Format](security-descriptor-string-format.md) examples, each ACE in a security descriptor string is enclosed in parentheses.</span></span> <span data-ttu-id="83039-106">Die Felder des ACE liegen in der folgenden Reihenfolge vor und sind durch Semikolons (;) getrennt.</span><span class="sxs-lookup"><span data-stu-id="83039-106">The fields of the ACE are in the following order and are separated by semicolons (;).</span></span>

> [!Note]  
> <span data-ttu-id="83039-107">Es gibt ein anderes Format für bedingte [*Zugriffs Steuerungs Einträge*](/windows/desktop/SecGloss/a-gly) (ACEs) als andere ACE-Typen.</span><span class="sxs-lookup"><span data-stu-id="83039-107">There is a different format for conditional [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) than other ACE types.</span></span> <span data-ttu-id="83039-108">Informationen zu bedingten ACEs finden Sie unter [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="83039-108">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a><span data-ttu-id="83039-109">Felder</span><span class="sxs-lookup"><span data-stu-id="83039-109">Fields</span></span>

<dl> <dt>

<span data-ttu-id="83039-110"><span id="ace_type"></span><span id="ACE_TYPE"></span>**ACE- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="83039-110"><span id="ace_type"></span><span id="ACE_TYPE"></span>**ace\_type**</span></span>
</dt> <dd>

<span data-ttu-id="83039-111">Eine Zeichenfolge, die den Wert des **AceType** -Members der [**ACE- \_ Header**](/windows/desktop/api/Winnt/ns-winnt-ace_header) Struktur angibt.</span><span class="sxs-lookup"><span data-stu-id="83039-111">A string that indicates the value of the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="83039-112">Die ACE-Typzeichenfolge kann eine der folgenden Zeichen folgen sein, die in SDDL. h definiert sind.</span><span class="sxs-lookup"><span data-stu-id="83039-112">The ACE type string can be one of the following strings defined in Sddl.h.</span></span>



| <span data-ttu-id="83039-113">ACE-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="83039-113">ACE type string</span></span> | <span data-ttu-id="83039-114">Konstante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="83039-114">Constant in Sddl.h</span></span>                      | <span data-ttu-id="83039-115">AceType-Wert</span><span class="sxs-lookup"><span data-stu-id="83039-115">AceType value</span></span>                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83039-116">„A“</span><span class="sxs-lookup"><span data-stu-id="83039-116">"A"</span></span>             | <span data-ttu-id="83039-117">SDDL- \_ Zugriff \_ zulässig</span><span class="sxs-lookup"><span data-stu-id="83039-117">SDDL\_ACCESS\_ALLOWED</span></span>                   | <span data-ttu-id="83039-118">Zugriffs zulässiger \_ \_ ACE- \_ Typ</span><span class="sxs-lookup"><span data-stu-id="83039-118">ACCESS\_ALLOWED\_ACE\_TYPE</span></span>                                                                                                                                         |
| <span data-ttu-id="83039-119">"D"</span><span class="sxs-lookup"><span data-stu-id="83039-119">"D"</span></span>             | <span data-ttu-id="83039-120">SDDL- \_ Zugriff \_ verweigert</span><span class="sxs-lookup"><span data-stu-id="83039-120">SDDL\_ACCESS\_DENIED</span></span>                    | <span data-ttu-id="83039-121">ACE-Typ "Zugriff \_ verweigert" \_ \_</span><span class="sxs-lookup"><span data-stu-id="83039-121">ACCESS\_DENIED\_ACE\_TYPE</span></span>                                                                                                                                          |
| <span data-ttu-id="83039-122">OA</span><span class="sxs-lookup"><span data-stu-id="83039-122">"OA"</span></span>            | <span data-ttu-id="83039-123">SDDL- \_ Objekt \_ Zugriff \_ zulässig</span><span class="sxs-lookup"><span data-stu-id="83039-123">SDDL\_OBJECT\_ACCESS\_ALLOWED</span></span>           | <span data-ttu-id="83039-124">Zugriffs zulässiger \_ \_ Objekt-ACE- \_ \_ Typ</span><span class="sxs-lookup"><span data-stu-id="83039-124">ACCESS\_ALLOWED\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                 |
| <span data-ttu-id="83039-125">Gen</span><span class="sxs-lookup"><span data-stu-id="83039-125">"OD"</span></span>            | <span data-ttu-id="83039-126">SDDL- \_ Objekt \_ Zugriff \_ verweigert</span><span class="sxs-lookup"><span data-stu-id="83039-126">SDDL\_OBJECT\_ACCESS\_DENIED</span></span>            | <span data-ttu-id="83039-127">Zugriffs \_ Verweigerungs \_ Objekt- \_ ACE- \_ Typ</span><span class="sxs-lookup"><span data-stu-id="83039-127">ACCESS\_DENIED\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                  |
| <span data-ttu-id="83039-128">Thaus</span><span class="sxs-lookup"><span data-stu-id="83039-128">"AU"</span></span>            | <span data-ttu-id="83039-129">SDDL \_ -Überwachung</span><span class="sxs-lookup"><span data-stu-id="83039-129">SDDL\_AUDIT</span></span>                             | <span data-ttu-id="83039-130">Systemüberwachungs- \_ \_ ACE- \_ Typ</span><span class="sxs-lookup"><span data-stu-id="83039-130">SYSTEM\_AUDIT\_ACE\_TYPE</span></span>                                                                                                                                           |
| <span data-ttu-id="83039-131">Irdische</span><span class="sxs-lookup"><span data-stu-id="83039-131">"AL"</span></span>            | <span data-ttu-id="83039-132">SDDL- \_ Alarm</span><span class="sxs-lookup"><span data-stu-id="83039-132">SDDL\_ALARM</span></span>                             | <span data-ttu-id="83039-133">Systemalarm- \_ \_ ACE- \_ Typ</span><span class="sxs-lookup"><span data-stu-id="83039-133">SYSTEM\_ALARM\_ACE\_TYPE</span></span>                                                                                                                                           |
| <span data-ttu-id="83039-134">Klägerin</span><span class="sxs-lookup"><span data-stu-id="83039-134">"OU"</span></span>            | <span data-ttu-id="83039-135">SDDL- \_ Objektüberwachung \_</span><span class="sxs-lookup"><span data-stu-id="83039-135">SDDL\_OBJECT\_AUDIT</span></span>                     | <span data-ttu-id="83039-136">Systemüberwachungs \_ \_ Objekt-ACE- \_ \_ Typ</span><span class="sxs-lookup"><span data-stu-id="83039-136">SYSTEM\_AUDIT\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                   |
| <span data-ttu-id="83039-137">Übernachten</span><span class="sxs-lookup"><span data-stu-id="83039-137">"OL"</span></span>            | <span data-ttu-id="83039-138">SDDL- \_ Objekt \_ Alarm</span><span class="sxs-lookup"><span data-stu-id="83039-138">SDDL\_OBJECT\_ALARM</span></span>                     | <span data-ttu-id="83039-139">\_Systemalarm \_ - \_ Objekttyp \_</span><span class="sxs-lookup"><span data-stu-id="83039-139">SYSTEM\_ALARM\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                   |
| <span data-ttu-id="83039-140">150</span><span class="sxs-lookup"><span data-stu-id="83039-140">"ML"</span></span>            | <span data-ttu-id="83039-141">erforderliche SDDL- \_ \_ Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="83039-141">SDDL\_MANDATORY\_LABEL</span></span>                  | <span data-ttu-id="83039-142">\_systemobligatorischer \_ Bezeichnung \_ ACE- \_ Typ</span><span class="sxs-lookup"><span data-stu-id="83039-142">SYSTEM\_MANDATORY\_LABEL\_ACE\_TYPE</span></span>                                                                                                                                |
| <span data-ttu-id="83039-143">Geleitet</span><span class="sxs-lookup"><span data-stu-id="83039-143">"XA"</span></span>            | <span data-ttu-id="83039-144">SDDL- \_ Rückruf \_ Zugriff \_ zulässig</span><span class="sxs-lookup"><span data-stu-id="83039-144">SDDL\_CALLBACK\_ACCESS\_ALLOWED</span></span>         | <span data-ttu-id="83039-145">Zugriffs zulässiger \_ \_ Rückruf \_ \_ -ACE **-Typ Windows Vista und Windows Server 2003:** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83039-145">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE **Windows Vista and Windows Server 2003:** Not available.</span></span><br/>                                                           |
| <span data-ttu-id="83039-146">XD</span><span class="sxs-lookup"><span data-stu-id="83039-146">"XD"</span></span>            | <span data-ttu-id="83039-147">SDDL- \_ Rückruf \_ Zugriff \_ verweigert</span><span class="sxs-lookup"><span data-stu-id="83039-147">SDDL\_CALLBACK\_ACCESS\_DENIED</span></span>          | <span data-ttu-id="83039-148">\_Rückruf-Rückruf für den Zugriff verweigert \_ \_ \_ **: Windows Vista und Windows Server 2003:** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83039-148">ACCESS\_DENIED\_CALLBACK\_ACE\_TYPE **Windows Vista and Windows Server 2003:** Not available.</span></span><br/>                                                            |
| <span data-ttu-id="83039-149">RA</span><span class="sxs-lookup"><span data-stu-id="83039-149">"RA"</span></span>            | <span data-ttu-id="83039-150">SDDL- \_ Ressourcen \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="83039-150">SDDL\_RESOURCE\_ATTRIBUTE</span></span>               | <span data-ttu-id="83039-151">System \_ Ressourcen \_ Attribut- \_ ACE- \_ Typ **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83039-151">SYSTEM\_RESOURCE\_ATTRIBUTE\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/> |
| <span data-ttu-id="83039-152">El</span><span class="sxs-lookup"><span data-stu-id="83039-152">"SP"</span></span>            | <span data-ttu-id="83039-153">SDDL-Bereichs bezogene \_ \_ Richtlinien- \_ ID</span><span class="sxs-lookup"><span data-stu-id="83039-153">SDDL\_SCOPED\_POLICY\_ID</span></span>                | <span data-ttu-id="83039-154">System weite \_ \_ Richtlinien- \_ ID \_ ACE \_ Type **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83039-154">SYSTEM\_SCOPED\_POLICY\_ID\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>  |
| <span data-ttu-id="83039-155">Distrikt</span><span class="sxs-lookup"><span data-stu-id="83039-155">"XU"</span></span>            | <span data-ttu-id="83039-156">SDDL- \_ Rückruf Überwachung \_</span><span class="sxs-lookup"><span data-stu-id="83039-156">SDDL\_CALLBACK\_AUDIT</span></span>                   | <span data-ttu-id="83039-157">\_ \_ Rückruf-ACE für System Überwachung \_ \_ **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83039-157">SYSTEM\_AUDIT\_CALLBACK\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>     |
| <span data-ttu-id="83039-158">D</span><span class="sxs-lookup"><span data-stu-id="83039-158">"ZA"</span></span>            | <span data-ttu-id="83039-159">SDDL- \_ Rückruf \_ Objekt \_ Zugriff \_ zulässig</span><span class="sxs-lookup"><span data-stu-id="83039-159">SDDL\_CALLBACK\_OBJECT\_ACCESS\_ALLOWED</span></span> | <span data-ttu-id="83039-160">Zugriffs zulässiger \_ \_ Rückruf \_ -ACE- \_ Typ **: Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83039-160">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>   |



 

> [!Note]  
> <span data-ttu-id="83039-161">Wenn der **ACE- \_ Typ** Access \_ Allowed \_ Object \_ \_ -ACE-Typ ist und weder für die **Objekt- \_ GUID** noch für die **Vererbungs \_ Objekt- \_ GUID** eine [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) angegeben ist, konvertiert [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) den **ACE- \_ Typ** in den \_ zulässigen ACE- \_ \_ Typ.</span><span class="sxs-lookup"><span data-stu-id="83039-161">If **ace\_type** is ACCESS\_ALLOWED\_OBJECT\_ACE\_TYPE and neither **object\_guid** nor **inherit\_object\_guid** has a [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) specified, then [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) converts **ace\_type** to ACCESS\_ALLOWED\_ACE\_TYPE.</span></span>

 

</dd> <dt>

<span data-ttu-id="83039-162"><span id="ace_flags"></span><span id="ACE_FLAGS"></span>**ACE- \_ Flags**</span><span class="sxs-lookup"><span data-stu-id="83039-162"><span id="ace_flags"></span><span id="ACE_FLAGS"></span>**ace\_flags**</span></span>
</dt> <dd>

<span data-ttu-id="83039-163">Eine Zeichenfolge, die den Wert des **AceFlags** -Members der [**ACE- \_ Header**](/windows/desktop/api/Winnt/ns-winnt-ace_header) Struktur angibt.</span><span class="sxs-lookup"><span data-stu-id="83039-163">A string that indicates the value of the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="83039-164">Die ACE-Flags-Zeichenfolge kann eine Verkettung der folgenden Zeichen folgen sein, die in SDDL. h definiert sind.</span><span class="sxs-lookup"><span data-stu-id="83039-164">The ACE flags string can be a concatenation of the following strings defined in Sddl.h.</span></span>



| <span data-ttu-id="83039-165">ACE Flags-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="83039-165">ACE flags string</span></span> | <span data-ttu-id="83039-166">Konstante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="83039-166">Constant in Sddl.h</span></span>       | <span data-ttu-id="83039-167">Aceflag-Wert</span><span class="sxs-lookup"><span data-stu-id="83039-167">AceFlag value</span></span>                 |
|------------------|--------------------------|-------------------------------|
| <span data-ttu-id="83039-168">RKI</span><span class="sxs-lookup"><span data-stu-id="83039-168">"CI"</span></span>             | <span data-ttu-id="83039-169">SDDL- \_ Container \_ erben</span><span class="sxs-lookup"><span data-stu-id="83039-169">SDDL\_CONTAINER\_INHERIT</span></span> | <span data-ttu-id="83039-170">Container \_ erben ( \_ ACE)</span><span class="sxs-lookup"><span data-stu-id="83039-170">CONTAINER\_INHERIT\_ACE</span></span>       |
| <span data-ttu-id="83039-171">Zählen</span><span class="sxs-lookup"><span data-stu-id="83039-171">"OI"</span></span>             | <span data-ttu-id="83039-172">SDDL- \_ Objekt \_ erben</span><span class="sxs-lookup"><span data-stu-id="83039-172">SDDL\_OBJECT\_INHERIT</span></span>    | <span data-ttu-id="83039-173">Objekt \_ erben ( \_ ACE)</span><span class="sxs-lookup"><span data-stu-id="83039-173">OBJECT\_INHERIT\_ACE</span></span>          |
| <span data-ttu-id="83039-174">Ecken</span><span class="sxs-lookup"><span data-stu-id="83039-174">"NP"</span></span>             | <span data-ttu-id="83039-175">SDDL \_ nicht weitergegeben \_</span><span class="sxs-lookup"><span data-stu-id="83039-175">SDDL\_NO\_PROPAGATE</span></span>      | <span data-ttu-id="83039-176">kein \_ propagieren- \_ \_ ACE erben</span><span class="sxs-lookup"><span data-stu-id="83039-176">NO\_PROPAGATE\_INHERIT\_ACE</span></span>   |
| <span data-ttu-id="83039-177">Brasilianer</span><span class="sxs-lookup"><span data-stu-id="83039-177">"IO"</span></span>             | <span data-ttu-id="83039-178">nur SDDL \_ erben \_</span><span class="sxs-lookup"><span data-stu-id="83039-178">SDDL\_INHERIT\_ONLY</span></span>      | <span data-ttu-id="83039-179">\_nur \_ ACE erben</span><span class="sxs-lookup"><span data-stu-id="83039-179">INHERIT\_ONLY\_ACE</span></span>            |
| <span data-ttu-id="83039-180">„ID“</span><span class="sxs-lookup"><span data-stu-id="83039-180">"ID"</span></span>             | <span data-ttu-id="83039-181">SDDL \_ geerbt</span><span class="sxs-lookup"><span data-stu-id="83039-181">SDDL\_INHERITED</span></span>          | <span data-ttu-id="83039-182">geerbte \_ ACE</span><span class="sxs-lookup"><span data-stu-id="83039-182">INHERITED\_ACE</span></span>                |
| <span data-ttu-id="83039-183">SAS</span><span class="sxs-lookup"><span data-stu-id="83039-183">"SA"</span></span>             | <span data-ttu-id="83039-184">SDDL-Überwachung \_ \_ erfolgreich</span><span class="sxs-lookup"><span data-stu-id="83039-184">SDDL\_AUDIT\_SUCCESS</span></span>     | <span data-ttu-id="83039-185">RAS-Flag für erfolgreiches \_ zugreifen \_ \_</span><span class="sxs-lookup"><span data-stu-id="83039-185">SUCCESSFUL\_ACCESS\_ACE\_FLAG</span></span> |
| <span data-ttu-id="83039-186">Übergangs</span><span class="sxs-lookup"><span data-stu-id="83039-186">"FA"</span></span>             | <span data-ttu-id="83039-187">Fehler bei SDDL-Überwachung. \_ \_</span><span class="sxs-lookup"><span data-stu-id="83039-187">SDDL\_AUDIT\_FAILURE</span></span>     | <span data-ttu-id="83039-188">fehlerhafter \_ Access- \_ ACE- \_ Flag</span><span class="sxs-lookup"><span data-stu-id="83039-188">FAILED\_ACCESS\_ACE\_FLAG</span></span>     |



 

</dd> <dt>

<span data-ttu-id="83039-189"><span id="rights"></span><span id="RIGHTS"></span>**Ansprüchen**</span><span class="sxs-lookup"><span data-stu-id="83039-189"><span id="rights"></span><span id="RIGHTS"></span>**rights**</span></span>
</dt> <dd>

<span data-ttu-id="83039-190">Eine Zeichenfolge, die die vom ACE kontrollierten [Zugriffsrechte](access-rights-and-access-masks.md) angibt.</span><span class="sxs-lookup"><span data-stu-id="83039-190">A string that indicates the [access rights](access-rights-and-access-masks.md) controlled by the ACE.</span></span> <span data-ttu-id="83039-191">Diese Zeichenfolge kann eine hexadezimale Zeichen folgen Darstellung der Zugriffsrechte sein, z. b. "0x7800003F", oder es kann sich um eine Verkettung der folgenden Zeichen folgen handeln.</span><span class="sxs-lookup"><span data-stu-id="83039-191">This string can be a hexadecimal string representation of the access rights, such as "0x7800003F", or it can be a concatenation of the following strings.</span></span>



### <a name="generic-access-rights"></a><span data-ttu-id="83039-192">Generische Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="83039-192">Generic access rights</span></span>

| <span data-ttu-id="83039-193">Zugriffsrechte Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="83039-193">Access rights string</span></span> | <span data-ttu-id="83039-194">Konstante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="83039-194">Constant in Sddl.h</span></span> | <span data-ttu-id="83039-195">Zugriffsrechte Wert</span><span class="sxs-lookup"><span data-stu-id="83039-195">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="83039-196">Gas</span><span class="sxs-lookup"><span data-stu-id="83039-196">"GA"</span></span>                 | <span data-ttu-id="83039-197">SDDL, \_ generisch \_</span><span class="sxs-lookup"><span data-stu-id="83039-197">SDDL\_GENERIC\_ALL</span></span> | <span data-ttu-id="83039-198">generisch \_ alle</span><span class="sxs-lookup"><span data-stu-id="83039-198">GENERIC\_ALL</span></span>       |
| <span data-ttu-id="83039-199">G</span><span class="sxs-lookup"><span data-stu-id="83039-199">"GR"</span></span>                 | <span data-ttu-id="83039-200">allgemeiner SDDL- \_ \_ Lesevorgang</span><span class="sxs-lookup"><span data-stu-id="83039-200">SDDL\_GENERIC\_READ</span></span> | <span data-ttu-id="83039-201">generischer \_ Lesevorgang</span><span class="sxs-lookup"><span data-stu-id="83039-201">GENERIC\_READ</span></span>     |
| <span data-ttu-id="83039-202">GW</span><span class="sxs-lookup"><span data-stu-id="83039-202">"GW"</span></span>                 | <span data-ttu-id="83039-203">generischer SDDL- \_ \_ Schreibvorgang</span><span class="sxs-lookup"><span data-stu-id="83039-203">SDDL\_GENERIC\_WRITE</span></span> | <span data-ttu-id="83039-204">generischer \_ Schreibvorgang</span><span class="sxs-lookup"><span data-stu-id="83039-204">GENERIC\_WRITE</span></span> |
| <span data-ttu-id="83039-205">GX</span><span class="sxs-lookup"><span data-stu-id="83039-205">"GX"</span></span>                 | <span data-ttu-id="83039-206">Allgemeine SDDL- \_ \_ Ausführung</span><span class="sxs-lookup"><span data-stu-id="83039-206">SDDL\_GENERIC\_EXECUTE</span></span> | <span data-ttu-id="83039-207">generisch \_ Ausführen</span><span class="sxs-lookup"><span data-stu-id="83039-207">GENERIC\_EXECUTE</span></span> |


### <a name="standard-access-rights"></a><span data-ttu-id="83039-208">Standard Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="83039-208">Standard access rights</span></span>

| <span data-ttu-id="83039-209">Zugriffsrechte Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="83039-209">Access rights string</span></span> | <span data-ttu-id="83039-210">Konstante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="83039-210">Constant in Sddl.h</span></span> | <span data-ttu-id="83039-211">Zugriffsrechte Wert</span><span class="sxs-lookup"><span data-stu-id="83039-211">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="83039-212">RC</span><span class="sxs-lookup"><span data-stu-id="83039-212">"RC"</span></span>                 | <span data-ttu-id="83039-213">SDDL- \_ Lese \_ Steuerelement</span><span class="sxs-lookup"><span data-stu-id="83039-213">SDDL\_READ\_CONTROL</span></span> | <span data-ttu-id="83039-214">Lese \_ Steuerelement</span><span class="sxs-lookup"><span data-stu-id="83039-214">READ\_CONTROL</span></span>      |
| <span data-ttu-id="83039-215">Berichteten</span><span class="sxs-lookup"><span data-stu-id="83039-215">"SD"</span></span>                 | <span data-ttu-id="83039-216">SDDL- \_ Standard \_ Delete</span><span class="sxs-lookup"><span data-stu-id="83039-216">SDDL\_STANDARD\_DELETE</span></span> | <span data-ttu-id="83039-217">Delete</span><span class="sxs-lookup"><span data-stu-id="83039-217">DELETE</span></span>          |
| <span data-ttu-id="83039-218">Zel</span><span class="sxs-lookup"><span data-stu-id="83039-218">"WD"</span></span>                 | <span data-ttu-id="83039-219">SDDL- \_ Schreib- \_ DAC</span><span class="sxs-lookup"><span data-stu-id="83039-219">SDDL\_WRITE\_DAC</span></span> | <span data-ttu-id="83039-220">\_DAC schreiben</span><span class="sxs-lookup"><span data-stu-id="83039-220">WRITE\_DAC</span></span>            |
| <span data-ttu-id="83039-221">WO</span><span class="sxs-lookup"><span data-stu-id="83039-221">"WO"</span></span>                 | <span data-ttu-id="83039-222">SDDL- \_ Schreib \_ Besitzer</span><span class="sxs-lookup"><span data-stu-id="83039-222">SDDL\_WRITE\_OWNER</span></span> | <span data-ttu-id="83039-223">\_Besitzer schreiben</span><span class="sxs-lookup"><span data-stu-id="83039-223">WRITE\_OWNER</span></span>        |

### <a name="directory-service-object-access-rights"></a><span data-ttu-id="83039-224">Verzeichnisdienst-Objekt Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="83039-224">Directory service object access rights</span></span>

| <span data-ttu-id="83039-225">Zugriffsrechte Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="83039-225">Access rights string</span></span> | <span data-ttu-id="83039-226">Konstante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="83039-226">Constant in Sddl.h</span></span> | <span data-ttu-id="83039-227">Zugriffsrechte Wert</span><span class="sxs-lookup"><span data-stu-id="83039-227">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="83039-228">Neutraler</span><span class="sxs-lookup"><span data-stu-id="83039-228">"RP"</span></span>                 | <span data-ttu-id="83039-229">SDDL- \_ Lese \_ Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="83039-229">SDDL\_READ\_PROPERTY</span></span> | <span data-ttu-id="83039-230">ADS \_ right \_ DS \_ Read \_ Prop</span><span class="sxs-lookup"><span data-stu-id="83039-230">ADS\_RIGHT\_DS\_READ\_PROP</span></span> |
| <span data-ttu-id="83039-231">UA</span><span class="sxs-lookup"><span data-stu-id="83039-231">"WP"</span></span>                 | <span data-ttu-id="83039-232">SDDL- \_ Schreib \_ Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="83039-232">SDDL\_WRITE\_PROPERTY</span></span> | <span data-ttu-id="83039-233">ADS \_ right \_ DS \_ Schreib \_ Prop</span><span class="sxs-lookup"><span data-stu-id="83039-233">ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="83039-234">125</span><span class="sxs-lookup"><span data-stu-id="83039-234">"CC"</span></span>                 | <span data-ttu-id="83039-235">untergeordnetes SDDL-Element \_ Erstellen \_</span><span class="sxs-lookup"><span data-stu-id="83039-235">SDDL\_CREATE\_CHILD</span></span> | <span data-ttu-id="83039-236">ADS \_ right \_ DS \_ Create \_ Child</span><span class="sxs-lookup"><span data-stu-id="83039-236">ADS\_RIGHT\_DS\_CREATE\_CHILD</span></span> |
| <span data-ttu-id="83039-237">DC</span><span class="sxs-lookup"><span data-stu-id="83039-237">"DC"</span></span>                 | <span data-ttu-id="83039-238">SDDL \_ Delete \_ Child</span><span class="sxs-lookup"><span data-stu-id="83039-238">SDDL\_DELETE\_CHILD</span></span> | <span data-ttu-id="83039-239">ADS \_ right \_ DS \_ Delete \_ Child</span><span class="sxs-lookup"><span data-stu-id="83039-239">ADS\_RIGHT\_DS\_DELETE\_CHILD</span></span> |
| <span data-ttu-id="83039-240">LTE</span><span class="sxs-lookup"><span data-stu-id="83039-240">"LC"</span></span>                 | <span data-ttu-id="83039-241">untergeordnete SDDL- \_ Listen \_</span><span class="sxs-lookup"><span data-stu-id="83039-241">SDDL\_LIST\_CHILDREN</span></span> | <span data-ttu-id="83039-242">Liste der AD \_ right \_ actrl \_ DS \_</span><span class="sxs-lookup"><span data-stu-id="83039-242">ADS\_RIGHT\_ACTRL\_DS\_LIST</span></span> |
| <span data-ttu-id="83039-243">Erstellung</span><span class="sxs-lookup"><span data-stu-id="83039-243">"SW"</span></span>                 | <span data-ttu-id="83039-244">SDDL \_ selbst \_ schreiben</span><span class="sxs-lookup"><span data-stu-id="83039-244">SDDL\_SELF\_WRITE</span></span>    | <span data-ttu-id="83039-245">ADS \_ right \_ DS \_ selbst</span><span class="sxs-lookup"><span data-stu-id="83039-245">ADS\_RIGHT\_DS\_SELF</span></span> |
| <span data-ttu-id="83039-246">Siehe</span><span class="sxs-lookup"><span data-stu-id="83039-246">"LO"</span></span>                  | <span data-ttu-id="83039-247">SDDL- \_ Listen \_ Objekt</span><span class="sxs-lookup"><span data-stu-id="83039-247">SDDL\_LIST\_OBJECT</span></span> | <span data-ttu-id="83039-248">ADS \_ right \_ DS \_ List- \_ Objekt</span><span class="sxs-lookup"><span data-stu-id="83039-248">ADS\_RIGHT\_DS\_LIST\_OBJECT</span></span> |
| <span data-ttu-id="83039-249">DT</span><span class="sxs-lookup"><span data-stu-id="83039-249">"DT"</span></span>                 | <span data-ttu-id="83039-250">SDDL- \_ Lösch Struktur \_</span><span class="sxs-lookup"><span data-stu-id="83039-250">SDDL\_DELETE\_TREE</span></span> | <span data-ttu-id="83039-251">ADS \_ right \_ DS \_ Delete \_ Tree</span><span class="sxs-lookup"><span data-stu-id="83039-251">ADS\_RIGHT\_DS\_DELETE\_TREE</span></span> |
| <span data-ttu-id="83039-252">Programmiert</span><span class="sxs-lookup"><span data-stu-id="83039-252">"CR"</span></span>                  | <span data-ttu-id="83039-253">SDDL- \_ Steuerungs \_ Zugriff</span><span class="sxs-lookup"><span data-stu-id="83039-253">SDDL\_CONTROL\_ACCESS</span></span> | <span data-ttu-id="83039-254">Anzeigen des Zugriffs auf die \_ \_ DS- \_ Steuerung \_</span><span class="sxs-lookup"><span data-stu-id="83039-254">ADS\_RIGHT\_DS\_CONTROL\_ACCESS</span></span> |

### <a name="file-access-rights"></a><span data-ttu-id="83039-255">Dateizugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="83039-255">File access rights</span></span>

| <span data-ttu-id="83039-256">Zugriffsrechte Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="83039-256">Access rights string</span></span> | <span data-ttu-id="83039-257">Konstante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="83039-257">Constant in Sddl.h</span></span> | <span data-ttu-id="83039-258">Zugriffsrechte Wert</span><span class="sxs-lookup"><span data-stu-id="83039-258">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="83039-259">Übergangs</span><span class="sxs-lookup"><span data-stu-id="83039-259">"FA"</span></span>                 | <span data-ttu-id="83039-260">SDDL- \_ Datei \_ alle</span><span class="sxs-lookup"><span data-stu-id="83039-260">SDDL\_FILE\_ALL</span></span>    | <span data-ttu-id="83039-261">voll \_ Zugriff auf Datei \_</span><span class="sxs-lookup"><span data-stu-id="83039-261">FILE\_ALL\_ACCESS</span></span>   |
| <span data-ttu-id="83039-262">Fr</span><span class="sxs-lookup"><span data-stu-id="83039-262">"FR"</span></span>                 | <span data-ttu-id="83039-263">SDDL- \_ Datei \_ Lesen</span><span class="sxs-lookup"><span data-stu-id="83039-263">SDDL\_FILE\_READ</span></span>   | <span data-ttu-id="83039-264">\_generischer Datei \_ Lesevorgang</span><span class="sxs-lookup"><span data-stu-id="83039-264">FILE\_GENERIC\_READ</span></span> |
| <span data-ttu-id="83039-265">WL</span><span class="sxs-lookup"><span data-stu-id="83039-265">"FW"</span></span>                 | <span data-ttu-id="83039-266">SDDL- \_ Datei \_ Schreibvorgänge</span><span class="sxs-lookup"><span data-stu-id="83039-266">SDDL\_FILE\_WRITE</span></span>  | <span data-ttu-id="83039-267">\_generischer Datei \_ Schreibvorgang</span><span class="sxs-lookup"><span data-stu-id="83039-267">FILE\_GENERIC\_WRITE</span></span> |
| <span data-ttu-id="83039-268">Designer</span><span class="sxs-lookup"><span data-stu-id="83039-268">"FX"</span></span>                 | <span data-ttu-id="83039-269">SDDL- \_ Datei \_ Ausführen</span><span class="sxs-lookup"><span data-stu-id="83039-269">SDDL\_FILE\_EXECUTE</span></span> | <span data-ttu-id="83039-270">\_generische Datei \_ Ausführung</span><span class="sxs-lookup"><span data-stu-id="83039-270">FILE\_GENERIC\_EXECUTE</span></span> |


### <a name="registry-key-access-rights"></a><span data-ttu-id="83039-271">Zugriffsrechte für den Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="83039-271">Registry key access rights</span></span>

| <span data-ttu-id="83039-272">Zugriffsrechte Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="83039-272">Access rights string</span></span> | <span data-ttu-id="83039-273">Konstante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="83039-273">Constant in Sddl.h</span></span> | <span data-ttu-id="83039-274">Zugriffsrechte Wert</span><span class="sxs-lookup"><span data-stu-id="83039-274">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="83039-275">At</span><span class="sxs-lookup"><span data-stu-id="83039-275">"KA"</span></span>                 | <span data-ttu-id="83039-276">Alle SDDL- \_ Schlüssel \_</span><span class="sxs-lookup"><span data-stu-id="83039-276">SDDL\_KEY\_ALL</span></span>     | <span data-ttu-id="83039-277">Schlüssel \_ \_ Zugriff</span><span class="sxs-lookup"><span data-stu-id="83039-277">KEY\_ALL\_ACCESS</span></span>   |
| <span data-ttu-id="83039-278">Stechen</span><span class="sxs-lookup"><span data-stu-id="83039-278">"KR"</span></span>                 | <span data-ttu-id="83039-279">SDDL- \_ Schlüssel \_ Lesen</span><span class="sxs-lookup"><span data-stu-id="83039-279">SDDL\_KEY\_READ</span></span>    | <span data-ttu-id="83039-280">Schlüssel \_ Lesevorgang</span><span class="sxs-lookup"><span data-stu-id="83039-280">KEY\_READ</span></span>          |
| <span data-ttu-id="83039-281">132</span><span class="sxs-lookup"><span data-stu-id="83039-281">"KW"</span></span>                 | <span data-ttu-id="83039-282">SDDL- \_ Schlüssel \_ Schreibvorgang</span><span class="sxs-lookup"><span data-stu-id="83039-282">SDDL\_KEY\_WRITE</span></span>   | <span data-ttu-id="83039-283">Schlüssel \_ Schreibvorgang</span><span class="sxs-lookup"><span data-stu-id="83039-283">KEY\_WRITE</span></span>         |
| <span data-ttu-id="83039-284">"Kx"</span><span class="sxs-lookup"><span data-stu-id="83039-284">"KX"</span></span>                 | <span data-ttu-id="83039-285">SDDL- \_ Schlüssel \_ Ausführung</span><span class="sxs-lookup"><span data-stu-id="83039-285">SDDL\_KEY\_EXECUTE</span></span> | <span data-ttu-id="83039-286">Schlüssel \_ Ausführung</span><span class="sxs-lookup"><span data-stu-id="83039-286">KEY\_EXECUTE</span></span>       |

### <a name="mandatory-label-rights"></a><span data-ttu-id="83039-287">Obligatorische Bezeichnungs Rechte</span><span class="sxs-lookup"><span data-stu-id="83039-287">Mandatory label rights</span></span>

| <span data-ttu-id="83039-288">Zugriffsrechte Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="83039-288">Access rights string</span></span> | <span data-ttu-id="83039-289">Konstante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="83039-289">Constant in Sddl.h</span></span> | <span data-ttu-id="83039-290">Zugriffsrechte Wert</span><span class="sxs-lookup"><span data-stu-id="83039-290">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="83039-291">Nr.</span><span class="sxs-lookup"><span data-stu-id="83039-291">"NR"</span></span>                 | <span data-ttu-id="83039-292">SDDL wird \_ nicht \_ gelesen \_</span><span class="sxs-lookup"><span data-stu-id="83039-292">SDDL\_NO\_READ\_UP</span></span> | <span data-ttu-id="83039-293">obligatorische Bezeichnung "System" wird \_ \_ \_ nicht \_ gelesen \_</span><span class="sxs-lookup"><span data-stu-id="83039-293">SYSTEM\_MANDATORY\_LABEL\_NO\_READ\_UP</span></span> |
| <span data-ttu-id="83039-294">AUT</span><span class="sxs-lookup"><span data-stu-id="83039-294">"NW"</span></span>                 | <span data-ttu-id="83039-295">SDDL \_ nicht \_ schreiben \_</span><span class="sxs-lookup"><span data-stu-id="83039-295">SDDL\_NO\_WRITE\_UP</span></span> | <span data-ttu-id="83039-296">erforderliche \_ System \_ Bezeichnung \_ kein \_ schreiben \_</span><span class="sxs-lookup"><span data-stu-id="83039-296">SYSTEM\_MANDATORY\_LABEL\_NO\_WRITE\_UP</span></span> |
| <span data-ttu-id="83039-297">NX</span><span class="sxs-lookup"><span data-stu-id="83039-297">"NX"</span></span>                 | <span data-ttu-id="83039-298">SDDL wird \_ nicht \_ ausgeführt \_</span><span class="sxs-lookup"><span data-stu-id="83039-298">SDDL\_NO\_EXECUTE\_UP</span></span> | <span data-ttu-id="83039-299">\_obligatorische System \_ Bezeichnung " \_ kein \_ Ausführen \_ "</span><span class="sxs-lookup"><span data-stu-id="83039-299">SYSTEM\_MANDATORY\_LABEL\_NO\_EXECUTE\_UP</span></span> |
</dd> <dt>

<span data-ttu-id="83039-300"><span id="object_guid"></span><span id="OBJECT_GUID"></span>**Objekt- \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="83039-300"><span id="object_guid"></span><span id="OBJECT_GUID"></span>**object\_guid**</span></span>
</dt> <dd>

<span data-ttu-id="83039-301">Eine Zeichen folgen Darstellung einer GUID, die den Wert des **ObjectType** -Members einer Objekt spezifischen ACE-Struktur angibt, z. b. [**Access \_ Allowed-Objekt- \_ \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace).</span><span class="sxs-lookup"><span data-stu-id="83039-301">A string representation of a GUID that indicates the value of the **ObjectType** member of an object-specific ACE structure, such as [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace).</span></span> <span data-ttu-id="83039-302">Die GUID-Zeichenfolge verwendet das Format, das von der [**UUIDToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="83039-302">The GUID string uses the format returned by the [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) function.</span></span>

<span data-ttu-id="83039-303">In der folgenden Tabelle werden einige häufig verwendete Objekt-GUIDs aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="83039-303">The following table lists some commonly used object GUIDs.</span></span>



| <span data-ttu-id="83039-304">Rechte und GUID</span><span class="sxs-lookup"><span data-stu-id="83039-304">Rights and GUID</span></span>                         | <span data-ttu-id="83039-305">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="83039-305">Permission</span></span>      |
|-----------------------------------------|-----------------|
| <span data-ttu-id="83039-306">CR; ab721a53-1e2f-11D0-9819-00aa0040529b</span><span class="sxs-lookup"><span data-stu-id="83039-306">CR;ab721a53-1e2f-11d0-9819-00aa0040529b</span></span> | <span data-ttu-id="83039-307">Kennwort ändern</span><span class="sxs-lookup"><span data-stu-id="83039-307">Change password</span></span> |
| <span data-ttu-id="83039-308">CR; 00299570-246d-11D0-A768-00aa006e0529</span><span class="sxs-lookup"><span data-stu-id="83039-308">CR;00299570-246d-11d0-a768-00aa006e0529</span></span> | <span data-ttu-id="83039-309">Kennwort zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="83039-309">Reset password</span></span>  |



 

</dd> <dt>

<span data-ttu-id="83039-310"><span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**\_Objekt- \_ GUID erben**</span><span class="sxs-lookup"><span data-stu-id="83039-310"><span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**inherit\_object\_guid**</span></span>
</dt> <dd>

<span data-ttu-id="83039-311">Eine Zeichen folgen Darstellung einer GUID, die den Wert des **erstellitedobjecttype** -Members einer Objekt spezifischen ACE-Struktur angibt.</span><span class="sxs-lookup"><span data-stu-id="83039-311">A string representation of a GUID that indicates the value of the **InheritedObjectType** member of an object-specific ACE structure.</span></span> <span data-ttu-id="83039-312">Die GUID-Zeichenfolge verwendet das [**UUIDToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) -Format.</span><span class="sxs-lookup"><span data-stu-id="83039-312">The GUID string uses the [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) format.</span></span>

</dd> <dt>

<span data-ttu-id="83039-313"><span id="account_sid"></span><span id="ACCOUNT_SID"></span>**Konto- \_ sid**</span><span class="sxs-lookup"><span data-stu-id="83039-313"><span id="account_sid"></span><span id="ACCOUNT_SID"></span>**account\_sid**</span></span>
</dt> <dd>

<span data-ttu-id="83039-314">[Sid-Zeichenfolge](sid-strings.md) , die den Vertrauens [nehmer des ACE](trustees.md) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="83039-314">[SID string](sid-strings.md) that identifies the [trustee](trustees.md) of the ACE.</span></span>

</dd> <dt>

<span data-ttu-id="83039-315"><span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**Ressourcen \_ Attribut**</span><span class="sxs-lookup"><span data-stu-id="83039-315"><span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**resource\_attribute**</span></span>
</dt> <dd>

<span data-ttu-id="83039-316">\[Optional \] : das Ressourcen \_ Attribut gilt nur für Resource ACEs und ist optional.</span><span class="sxs-lookup"><span data-stu-id="83039-316">\[OPTIONAL\] The resource\_attribute is only for resource ACEs and is optional.</span></span> <span data-ttu-id="83039-317">Eine Zeichenfolge, die den Datentyp angibt.</span><span class="sxs-lookup"><span data-stu-id="83039-317">A string that indicates the data type.</span></span> <span data-ttu-id="83039-318">Der ACE-Datentyp des Ressourcen Attributs kann einer der folgenden Datentypen sein, die in "SDDL. h" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="83039-318">The resource attribute ace data type can be one of the following data types defined in Sddl.h.</span></span>

<span data-ttu-id="83039-319">Das \# Zeichen "" ist in Ressourcen Attributen mit "0" Synonym.</span><span class="sxs-lookup"><span data-stu-id="83039-319">The "\#" sign is synonymous with "0" in resource attributes.</span></span> <span data-ttu-id="83039-320">Beispiel: d:Ai (XA; oici; FA;;; WD; (octetstringtype = = \# 1 \# 2 \# 3 \# \# )) entspricht und wird als d:Ai (XA; oici; FA;;;) interpretiert. WD; (octetstringtype = = \# 01020300)).</span><span class="sxs-lookup"><span data-stu-id="83039-320">For example, D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#1\#2\#3\#\#)) is equivalent to and interpreted as D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#01020300)).</span></span>

<span data-ttu-id="83039-321">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** Ressourcen Attribute sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83039-321">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Resource attributes are not available.</span></span>



| <span data-ttu-id="83039-322">Ressourcen Attribut-ACE-Datentyp Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="83039-322">Resource attribute ace data type string</span></span> | <span data-ttu-id="83039-323">Konstante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="83039-323">Constant in Sddl.h</span></span> | <span data-ttu-id="83039-324">Datentyp</span><span class="sxs-lookup"><span data-stu-id="83039-324">Data type</span></span>        |
|-----------------------------------------|--------------------|------------------|
| <span data-ttu-id="83039-325">Kriegs</span><span class="sxs-lookup"><span data-stu-id="83039-325">"TI"</span></span>                                    | <span data-ttu-id="83039-326">SDDL \_ int</span><span class="sxs-lookup"><span data-stu-id="83039-326">SDDL\_INT</span></span>          | <span data-ttu-id="83039-327">Ganze Zahl mit Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="83039-327">Signed integer</span></span>   |
| <span data-ttu-id="83039-328">Di</span><span class="sxs-lookup"><span data-stu-id="83039-328">"TU"</span></span>                                    | <span data-ttu-id="83039-329">SDDL- \_ uint</span><span class="sxs-lookup"><span data-stu-id="83039-329">SDDL\_UINT</span></span>         | <span data-ttu-id="83039-330">Ganze Zahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="83039-330">Unsigned integer</span></span> |
| <span data-ttu-id="83039-331">TS</span><span class="sxs-lookup"><span data-stu-id="83039-331">"TS"</span></span>                                    | <span data-ttu-id="83039-332">SDDL \_ wstring</span><span class="sxs-lookup"><span data-stu-id="83039-332">SDDL\_WSTRING</span></span>      | <span data-ttu-id="83039-333">Breite Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="83039-333">Wide string</span></span>      |
| <span data-ttu-id="83039-334">CT</span><span class="sxs-lookup"><span data-stu-id="83039-334">"TD"</span></span>                                    | <span data-ttu-id="83039-335">SDDL- \_ sid</span><span class="sxs-lookup"><span data-stu-id="83039-335">SDDL\_SID</span></span>          | <span data-ttu-id="83039-336">SID</span><span class="sxs-lookup"><span data-stu-id="83039-336">SID</span></span>              |
| <span data-ttu-id="83039-337">Llte</span><span class="sxs-lookup"><span data-stu-id="83039-337">"TX"</span></span>                                    | <span data-ttu-id="83039-338">SDDL- \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="83039-338">SDDL\_BLOB</span></span>         | <span data-ttu-id="83039-339">Oktett-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="83039-339">Octet string</span></span>     |
| <span data-ttu-id="83039-340">T</span><span class="sxs-lookup"><span data-stu-id="83039-340">"TB"</span></span>                                    | <span data-ttu-id="83039-341">SDDL- \_ boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="83039-341">SDDL\_BOOLEAN</span></span>      | <span data-ttu-id="83039-342">Boolean</span><span class="sxs-lookup"><span data-stu-id="83039-342">Boolean</span></span>          |



 

</dd> </dl>

<span data-ttu-id="83039-343">Das folgende Beispiel zeigt eine ACE-Zeichenfolge für einen Zugriffs zulässigen ACE.</span><span class="sxs-lookup"><span data-stu-id="83039-343">The following example shows an ACE string for an access-allowed ACE.</span></span> <span data-ttu-id="83039-344">Es handelt sich nicht um einen Objekt spezifischen ACE, d. h., er enthält keine Informationen in den **Objekt- \_ GUID** und **erbt \_ Objekt- \_ GUID** -Felder.</span><span class="sxs-lookup"><span data-stu-id="83039-344">It is not an object-specific ACE, so it has no information in the **object\_guid** and **inherit\_object\_guid** fields.</span></span> <span data-ttu-id="83039-345">Das Feld **ACE \_ Flags** ist ebenfalls leer, was darauf hinweist, dass keines der ACE-Flags festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="83039-345">The **ace\_flags** field is also empty, which indicates that none of the ACE flags are set.</span></span>


```C++
(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-1-0)
```



<span data-ttu-id="83039-346">Die oben gezeigte ACE-Zeichenfolge beschreibt die folgenden ACE-Informationen.</span><span class="sxs-lookup"><span data-stu-id="83039-346">The ACE string shown above describes the following ACE information.</span></span>


```C++
AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
AceFlags:      0x00
Access Mask:   0x100e003f
                    READ_CONTROL
                    WRITE_DAC
                    WRITE_OWNER
                    GENERIC_ALL
                    Other access rights(0x0000003f)
Ace Sid      : (S-1-1-0)
```



<span data-ttu-id="83039-347">Im folgenden Beispiel wird eine Datei veranschaulicht, die mit Ressourcen Ansprüchen für Windows und Structured Query Language (SQL) klassifiziert ist, wobei das Geheimnis auf hohe geschäftliche Auswirkung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="83039-347">The following example shows a file classified with resource claims for Windows and Structured Query Language (SQL) with Secrecy set to High Business Impact.</span></span>


```C++
(RA;CI;;;;S-1-1-0; ("Project",TS,0,"Windows","SQL")) 
(RA;CI;;;;S-1-1-0; ("Secrecy",TU,0,3))
```



<span data-ttu-id="83039-348">Die oben gezeigte ACE-Zeichenfolge beschreibt die folgenden ACE-Informationen.</span><span class="sxs-lookup"><span data-stu-id="83039-348">The ACE string shown above describes the following ACE information.</span></span>


```C++
AceType:       0x12 (SYSTEM_RESOURCE_ATTRIBUTE_ACE_TYPE)
AceFlags:      0x1  (SDDL_CONTAINER_INHERIT)
Access Mask:   0x0
Ace Sid      : (S-1-1-0)
Resource Attributes: Project has the strings Windows and SQL, Secrecy has the unsigned int value of 3
```



<span data-ttu-id="83039-349">Weitere Informationen finden Sie unter [Sicherheits Deskriptor-Zeichen folgen Format](security-descriptor-string-format.md) und [sid](sid-strings.md)-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="83039-349">For more information, see [Security Descriptor String Format](security-descriptor-string-format.md) and [SID Strings](sid-strings.md).</span></span> <span data-ttu-id="83039-350">Informationen zu bedingten ACEs finden Sie unter [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="83039-350">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="83039-351">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="83039-351">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="83039-352">[\[MS-DYP \] : Beschreibung der Sicherheits Beschreibungssprache](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="83039-352">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

