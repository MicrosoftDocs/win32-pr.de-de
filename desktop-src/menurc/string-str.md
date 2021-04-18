---
title: Zeichen folgen Struktur
description: Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Sie enthält eine Zeichenfolge, die einen bestimmten Aspekt einer Datei beschreibt, z. b. die Version einer Datei, die Copyright Hinweise oder ihre Marken.
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- Zeichen folgen Struktur-Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7035223082a9e446caebd6e07d3d55c84536d09f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337302"
---
# <a name="string-structure"></a><span data-ttu-id="d8e4f-105">Zeichen folgen Struktur</span><span class="sxs-lookup"><span data-stu-id="d8e4f-105">String structure</span></span>

<span data-ttu-id="d8e4f-106">Stellt die Organisation von Daten in einer Datei Versions Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="d8e4f-107">Sie enthält eine Zeichenfolge, die einen bestimmten Aspekt einer Datei beschreibt, z. b. die Version einer Datei, die Copyright Hinweise oder ihre Marken.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-107">It contains a string that describes a specific aspect of a file, for example, a file's version, its copyright notices, or its trademarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8e4f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8e4f-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  WORD  Value;
} String;
```



## <a name="members"></a><span data-ttu-id="d8e4f-109">Member</span><span class="sxs-lookup"><span data-stu-id="d8e4f-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="d8e4f-110">**wlength**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="d8e4f-111">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d8e4f-112">Die Länge dieser **Zeichen** folgen Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-112">The length, in bytes, of this **String** structure.</span></span>

</dd> <dt>

<span data-ttu-id="d8e4f-113">**wvaluelength**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="d8e4f-114">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d8e4f-115">Die Größe des **Wertmembers** in Wörtern.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-115">The size, in words, of the **Value** member.</span></span>

</dd> <dt>

<span data-ttu-id="d8e4f-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="d8e4f-117">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d8e4f-118">Der Typ der Daten in der Versions Ressource.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-118">The type of data in the version resource.</span></span> <span data-ttu-id="d8e4f-119">Dieser Member ist 1, wenn die Versions Ressource Textdaten enthält, und 0, wenn die Versions Ressource binäre Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="d8e4f-120">**szkey**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="d8e4f-121">Typ: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="d8e4f-122">Eine beliebige Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-122">An arbitrary Unicode string.</span></span> <span data-ttu-id="d8e4f-123">Der **szkey** -Member kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-123">The **szKey** member can be one or more of the following values.</span></span> <span data-ttu-id="d8e4f-124">Diese Werte sind nur Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-124">These values are guidelines only.</span></span>

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span data-ttu-id="d8e4f-125"><span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Iny**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-125"><span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Comments**</span></span>


</dt> <dd>

<span data-ttu-id="d8e4f-126">Der **Wert** Mitglied enthält alle zusätzlichen Informationen, die zu Diagnose Zwecken angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-126">The **Value** member contains any additional information that should be displayed for diagnostic purposes.</span></span> <span data-ttu-id="d8e4f-127">Diese Zeichenfolge kann eine beliebige Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-127">This string can be an arbitrary length.</span></span>

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span data-ttu-id="d8e4f-128"><span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**CompanyName**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-128"><span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**CompanyName**</span></span>


</dt> <dd>

<span data-ttu-id="d8e4f-129">Der **Wert** Mitglied identifiziert das Unternehmen, das die Datei erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-129">The **Value** member identifies the company that produced the file.</span></span> <span data-ttu-id="d8e4f-130">Beispiel: "Microsoft Corporation" oder "Standard Microsystems Corporation, Inc."</span><span class="sxs-lookup"><span data-stu-id="d8e4f-130">For example, "Microsoft Corporation" or "Standard Microsystems Corporation, Inc."</span></span>

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span data-ttu-id="d8e4f-131"><span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-131"><span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**</span></span>


</dt> <dd>

<span data-ttu-id="d8e4f-132">Das **Wertmember** beschreibt die Datei so, dass Sie Benutzern angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-132">The **Value** member describes the file in such a way that it can be presented to users.</span></span> <span data-ttu-id="d8e4f-133">Diese Zeichenfolge wird möglicherweise in einem Listenfeld angezeigt, wenn der Benutzer die zu installierenden Dateien auswählt.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-133">This string may be presented in a list box when the user is choosing files to install.</span></span> <span data-ttu-id="d8e4f-134">Beispiel: "Tastaturtreiber für im Stil Formatierungs Tastatur" oder "Microsoft Word für Windows".</span><span class="sxs-lookup"><span data-stu-id="d8e4f-134">For example, "Keyboard driver for AT-style keyboards" or "Microsoft Word for Windows".</span></span>

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span data-ttu-id="d8e4f-135"><span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**File Version**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-135"><span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**</span></span>


</dt> <dd>

<span data-ttu-id="d8e4f-136">Der **Wertmember** identifiziert die Version dieser Datei.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-136">The **Value** member identifies the version of this file.</span></span> <span data-ttu-id="d8e4f-137">Der **Wert** könnte z. b. "3.00 a" oder "5.00. RC2" lauten.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-137">For example, **Value** could be "3.00A" or "5.00.RC2".</span></span>

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span data-ttu-id="d8e4f-138"><span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-138"><span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**</span></span>


</dt> <dd>

<span data-ttu-id="d8e4f-139">Der **Wertmember** identifiziert den internen Namen der Datei, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-139">The **Value** member identifies the file's internal name, if one exists.</span></span> <span data-ttu-id="d8e4f-140">Diese Zeichenfolge kann z. b. den Modulnamen für eine DLL, den Namen eines virtuellen Geräts für ein virtuelles Windows-Gerät oder einen Gerätenamen für einen MS-DOS-Gerätetreiber enthalten.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-140">For example, this string could contain the module name for a DLL, a virtual device name for a Windows virtual device, or a device name for a MS-DOS device driver.</span></span>

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span data-ttu-id="d8e4f-141"><span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-141"><span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**</span></span>


</dt> <dd>

<span data-ttu-id="d8e4f-142">Der **Wert** Mitglied beschreibt alle Copyright Hinweise, Marken und registrierten Marken, die auf die Datei angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-142">The **Value** member describes all copyright notices, trademarks, and registered trademarks that apply to the file.</span></span> <span data-ttu-id="d8e4f-143">Dies sollte den vollständigen Text aller Hinweise, rechtliche Symbole, Copyright-Datumsangaben, Markennummern usw. umfassen.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-143">This should include the full text of all notices, legal symbols, copyright dates, trademark numbers, and so on.</span></span> <span data-ttu-id="d8e4f-144">In englischer Sprache sollte diese Zeichenfolge das folgende Format aufweisen: "Copyright Microsoft Corp. 1990 1994".</span><span class="sxs-lookup"><span data-stu-id="d8e4f-144">In English, this string should be in the format "Copyright Microsoft Corp. 1990  1994".</span></span>

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span data-ttu-id="d8e4f-145"><span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**Legalmarken**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-145"><span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**</span></span>


</dt> <dd>

<span data-ttu-id="d8e4f-146">Der **Wert** Mitglied beschreibt alle Marken und registrierten Marken, die auf die Datei angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-146">The **Value** member describes all trademarks and registered trademarks that apply to the file.</span></span> <span data-ttu-id="d8e4f-147">Dies sollte den vollständigen Text aller Hinweise, rechtliche Symbole, Markennummern usw. umfassen.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-147">This should include the full text of all notices, legal symbols, trademark numbers, and so on.</span></span> <span data-ttu-id="d8e4f-148">Im Deutschen sollte diese Zeichenfolge das folgende Format aufweisen: "Windows ist eine Marke der Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="d8e4f-148">In English, this string should be in the format "Windows is a trademark of Microsoft Corporation".</span></span>

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span data-ttu-id="d8e4f-149"><span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**Optio**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-149"><span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**</span></span>


</dt> <dd>

<span data-ttu-id="d8e4f-150">Das **Wertmember** identifiziert den ursprünglichen Namen der Datei ohne einen Pfad.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-150">The **Value** member identifies the original name of the file, not including a path.</span></span> <span data-ttu-id="d8e4f-151">Dadurch kann eine Anwendung ermitteln, ob eine Datei von einem Benutzer umbenannt wurde.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-151">This enables an application to determine whether a file has been renamed by a user.</span></span> <span data-ttu-id="d8e4f-152">Dieser Name ist möglicherweise nicht MS-DOS 8,3-Format, wenn die Datei für ein nicht-FAT-Dateisystem spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-152">This name may not be MS-DOS 8.3-format if the file is specific to a non-FAT file system.</span></span>

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span data-ttu-id="d8e4f-153"><span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-153"><span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**</span></span>


</dt> <dd>

<span data-ttu-id="d8e4f-154">Das **Wertmember** beschreibt, von wem, wo und warum diese private Version der Datei erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-154">The **Value** member describes by whom, where, and why this private version of the file was built.</span></span> <span data-ttu-id="d8e4f-155">Diese Zeichenfolge sollte nur vorhanden sein, wenn das **vs \_ FF \_ PrivateBuild** -Flag im **dwFileFlags** -Member der [**vs \_ FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) -Struktur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-155">This string should only be present if the **VS\_FF\_PRIVATEBUILD** flag is set in the **dwFileFlags** member of the [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure.</span></span> <span data-ttu-id="d8e4f-156">Der **Wert** könnte z. b. "von Oscar auf \\ OSCAR2 erstellt" lauten.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-156">For example, **Value** could be "Built by OSCAR on \\OSCAR2".</span></span>

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span data-ttu-id="d8e4f-157"><span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**ProductName**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-157"><span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**ProductName**</span></span>


</dt> <dd>

<span data-ttu-id="d8e4f-158">Der **Wertmember** identifiziert den Namen des Produkts, mit dem diese Datei verteilt wird.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-158">The **Value** member identifies the name of the product with which this file is distributed.</span></span> <span data-ttu-id="d8e4f-159">Diese Zeichenfolge könnte z. b. "Microsoft Windows" lauten.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-159">For example, this string could be "Microsoft Windows".</span></span>

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span data-ttu-id="d8e4f-160"><span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-160"><span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**</span></span>


</dt> <dd>

<span data-ttu-id="d8e4f-161">Das **Wertmember** identifiziert die Version des Produkts, mit dem diese Datei verteilt wird.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-161">The **Value** member identifies the version of the product with which this file is distributed.</span></span> <span data-ttu-id="d8e4f-162">Der **Wert** könnte z. b. "3.00 a" oder "5.00. RC2" lauten.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-162">For example, **Value** could be "3.00A" or "5.00.RC2".</span></span>

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span data-ttu-id="d8e4f-163"><span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-163"><span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**</span></span>


</dt> <dd>

<span data-ttu-id="d8e4f-164">Das **Wertmember** beschreibt, wie sich diese Version der Datei von der normalen Version unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-164">The **Value** member describes how this version of the file differs from the normal version.</span></span> <span data-ttu-id="d8e4f-165">Dieser Eintrag sollte nur vorhanden sein, wenn das **vs \_ FF \_ SpecialBuild** -Flag im **dwFileFlags** -Member der [**vs \_ FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) -Struktur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-165">This entry should only be present if the **VS\_FF\_SPECIALBUILD** flag is set in the **dwFileFlags** member of the [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure.</span></span> <span data-ttu-id="d8e4f-166">Der **Wert** könnte z. b. "private Build for Olivetti lösen von Maus Problemen auf M250 und M250E Computers" lauten.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-166">For example, **Value** could be "Private build for Olivetti solving mouse problems on M250 and M250E computers".</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d8e4f-167">**Auffüllen**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-167">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="d8e4f-168">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-168">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d8e4f-169">So viele Null-Wörter, wie erforderlich, um den **Wertmember** an einer 32-Bit-Grenze auszurichten.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-169">As many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="d8e4f-170">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-170">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="d8e4f-171">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-171">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d8e4f-172">Eine NULL terminierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-172">A zero-terminated string.</span></span> <span data-ttu-id="d8e4f-173">Weitere Informationen finden Sie in der Beschreibung des **szkey** -Members.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-173">See the **szKey** member description for more information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8e4f-174">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8e4f-174">Remarks</span></span>

<span data-ttu-id="d8e4f-175">Diese Struktur ist keine echte C-Sprachstruktur, da Sie Member variabler Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-175">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="d8e4f-176">Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versions Ressource erstellt und wird nicht in den Header Dateien angezeigt, die im Windows Software Development Kit (SDK) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-176">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="d8e4f-177">Eine **Zeichen** folgen Struktur kann einen **szkey** -Wert von haben, z. b. "CompanyName" und den **Wert** "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="d8e4f-177">A **String** structure may have an **szKey** value of, for example, "CompanyName" and a **Value** of "Microsoft Corporation".</span></span> <span data-ttu-id="d8e4f-178">Eine andere **Zeichen** folgen Struktur mit dem gleichen **szkey** -Wert könnte den **Wert** "Microsoft GmbH" enthalten.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-178">Another **String** structure with the same **szKey** value could contain a **Value** of "Microsoft GmbH".</span></span> <span data-ttu-id="d8e4f-179">Dies kann vorkommen, wenn die zweite **Zeichen** folgen Struktur einer [**STRINGTABLE**](stringtable.md) -Struktur zugeordnet wäre, deren **szkey** -Wert 040704b0 ist, d. h. Deutsch/Unicode.</span><span class="sxs-lookup"><span data-stu-id="d8e4f-179">This might occur if the second **String** structure were associated with a [**StringTable**](stringtable.md) structure whose **szKey** value is 040704b0   that is, German/Unicode.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8e4f-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8e4f-180">Requirements</span></span>



| <span data-ttu-id="d8e4f-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8e4f-181">Requirement</span></span> | <span data-ttu-id="d8e4f-182">Wert</span><span class="sxs-lookup"><span data-stu-id="d8e4f-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d8e4f-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8e4f-183">Minimum supported client</span></span><br/> | <span data-ttu-id="d8e4f-184">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8e4f-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d8e4f-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8e4f-185">Minimum supported server</span></span><br/> | <span data-ttu-id="d8e4f-186">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8e4f-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d8e4f-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8e4f-187">See also</span></span>

<dl> <dt>

<span data-ttu-id="d8e4f-188">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-188">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d8e4f-189">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-189">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="d8e4f-190">**VS \_ fixedfileingefo**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-190">**VS\_FIXEDFILEINFO**</span></span>](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[<span data-ttu-id="d8e4f-191">**Stringfileingefo**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-191">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="d8e4f-192">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-192">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="d8e4f-193">**Licher**</span><span class="sxs-lookup"><span data-stu-id="d8e4f-193">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d8e4f-194">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="d8e4f-194">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





