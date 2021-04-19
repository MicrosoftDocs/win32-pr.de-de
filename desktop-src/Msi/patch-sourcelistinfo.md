---
description: Die sourcelistinfo-Eigenschaft des Patch-Objekts Ruft die Quell Informations Eigenschaften für einen Patch ab und legt Sie fest. Diese Eigenschaft ruft msisourcelistgetinfo oder msisourcelist* tinfo auf. Dies ist eine Lese-oder Schreib Eigenschaft.
ms.assetid: a07f2cc8-fee2-4703-89ea-769921713268
title: Patch. sourcelistinfo (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22f4428decca7629f9d4049a2d3f52dfe8b8775a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354070"
---
# <a name="patchsourcelistinfo-property"></a><span data-ttu-id="372eb-105">Patch. sourcelistinfo (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="372eb-105">Patch.SourceListInfo property</span></span>

<span data-ttu-id="372eb-106">Die **sourcelistinfo** -Eigenschaft des [**Patch**](patch-object.md) -Objekts Ruft die Quell Informations Eigenschaften für einen Patch ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="372eb-106">The **SourceListInfo** property of the [**Patch**](patch-object.md) object gets and sets the source information properties for a patch.</span></span> <span data-ttu-id="372eb-107">Diese Eigenschaft ruft [**msisourcelistgetinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) oder [**msisourcelist* tinfo*\*](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)auf.</span><span class="sxs-lookup"><span data-stu-id="372eb-107">This property call [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) or [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span></span> <span data-ttu-id="372eb-108">Dies ist eine Lese-oder Schreib Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="372eb-108">This is a read or write property.</span></span>

<span data-ttu-id="372eb-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="372eb-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="372eb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="372eb-110">Syntax</span></span>


```JScript
propVal = Patch.SourceListInfo
```



## <a name="property-value"></a><span data-ttu-id="372eb-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="372eb-111">Property value</span></span>

<span data-ttu-id="372eb-112">Der Name der Quell Informations Eigenschaften für einen Patch, der abgefragt oder festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="372eb-112">The name of the source information properties for a patch to query or set.</span></span> <span data-ttu-id="372eb-113">Mögliche Werte finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="372eb-113">For possible values, see the Remarks section of this topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="372eb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="372eb-114">Remarks</span></span>

<span data-ttu-id="372eb-115">Es können nicht alle Eigenschaften festgelegt werden, die abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="372eb-115">Not all properties that can be retrieved can be set.</span></span> <span data-ttu-id="372eb-116">Der *szProperty* -Parameter kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="372eb-116">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="372eb-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="372eb-117">Property</span></span>         | <span data-ttu-id="372eb-118">Kann festgelegt werden?</span><span class="sxs-lookup"><span data-stu-id="372eb-118">Can set?</span></span> | <span data-ttu-id="372eb-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="372eb-119">Meaning</span></span>                                                                                                                                                                                                                                                           |
|------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="372eb-120">Mediapackagepath</span><span class="sxs-lookup"><span data-stu-id="372eb-120">MediaPackagePath</span></span> | <span data-ttu-id="372eb-121">J</span><span class="sxs-lookup"><span data-stu-id="372eb-121">Y</span></span>        | <span data-ttu-id="372eb-122">Der Pfad relativ zum Stammverzeichnis des-Installationsmediums.</span><span class="sxs-lookup"><span data-stu-id="372eb-122">The path relative to the root of the installation media.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="372eb-123">Diskprompt</span><span class="sxs-lookup"><span data-stu-id="372eb-123">DiskPrompt</span></span>       | <span data-ttu-id="372eb-124">J</span><span class="sxs-lookup"><span data-stu-id="372eb-124">Y</span></span>        | <span data-ttu-id="372eb-125">Die Eingabe Aufforderungs Vorlage, die verwendet wird, wenn der Benutzer zur Eingabe eines Installationsmediums</span><span class="sxs-lookup"><span data-stu-id="372eb-125">The prompt template used when prompting the user for installation media.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="372eb-126">LastUsedSource</span><span class="sxs-lookup"><span data-stu-id="372eb-126">LastUsedSource</span></span>   | <span data-ttu-id="372eb-127">J</span><span class="sxs-lookup"><span data-stu-id="372eb-127">Y</span></span>        | <span data-ttu-id="372eb-128">Der zuletzt verwendete Quell Speicherort für den Patch.</span><span class="sxs-lookup"><span data-stu-id="372eb-128">The most recently used source location for the patch.</span></span> <span data-ttu-id="372eb-129">Wenn Sie diese Eigenschaft festlegen, legen Sie den Quell Speicherort für eine Netzwerkquelle oder "u;" für den URL-Typ als Präfix für den Quell Speicherort fest.</span><span class="sxs-lookup"><span data-stu-id="372eb-129">When you set this property, prefix the source location with "n;" for a network source or "u;" for URL type.</span></span> <span data-ttu-id="372eb-130">Verwenden Sie z. b. "n; \\ \\ Scratch Scratch- \\ \\ Test "oder" u; " https://microsoft.com/Patches/Office/SP1 .</span><span class="sxs-lookup"><span data-stu-id="372eb-130">For example, use "n;\\\\scratch\\scratch\\test" or "u;https://microsoft.com/Patches/Office/SP1".</span></span> |
| <span data-ttu-id="372eb-131">Lastusedtype</span><span class="sxs-lookup"><span data-stu-id="372eb-131">LastUsedType</span></span>     | <span data-ttu-id="372eb-132">N</span><span class="sxs-lookup"><span data-stu-id="372eb-132">N</span></span>        | <span data-ttu-id="372eb-133">"n", wenn die zuletzt verwendete Quelle ein Netzwerk Speicherort ist.</span><span class="sxs-lookup"><span data-stu-id="372eb-133">"n" if the last-used source is a network location.</span></span> <span data-ttu-id="372eb-134">"u", wenn die zuletzt verwendete Quelle ein URL-Speicherort war.</span><span class="sxs-lookup"><span data-stu-id="372eb-134">"u" if the last used source was a URL location.</span></span> <span data-ttu-id="372eb-135">"m", wenn die zuletzt verwendete Quelle Medien war.</span><span class="sxs-lookup"><span data-stu-id="372eb-135">"m" if the last used source was media.</span></span> <span data-ttu-id="372eb-136">Leere Zeichenfolge (""), wenn keine zuletzt verwendete Quelle vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="372eb-136">Empty string ("") if there is no last used source.</span></span>                                                                      |
| <span data-ttu-id="372eb-137">PackageName</span><span class="sxs-lookup"><span data-stu-id="372eb-137">PackageName</span></span>      | <span data-ttu-id="372eb-138">J</span><span class="sxs-lookup"><span data-stu-id="372eb-138">Y</span></span>        | <span data-ttu-id="372eb-139">Der Name des Windows Installer Pakets oder Patchpakets in der Quelle.</span><span class="sxs-lookup"><span data-stu-id="372eb-139">The name of the Windows Installer package or patch package on the source.</span></span>                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="372eb-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="372eb-140">Requirements</span></span>



| <span data-ttu-id="372eb-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="372eb-141">Requirement</span></span> | <span data-ttu-id="372eb-142">Wert</span><span class="sxs-lookup"><span data-stu-id="372eb-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="372eb-143">Version</span><span class="sxs-lookup"><span data-stu-id="372eb-143">Version</span></span><br/> | <span data-ttu-id="372eb-144">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="372eb-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="372eb-145">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="372eb-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="372eb-146">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="372eb-146">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="372eb-147">DLL</span><span class="sxs-lookup"><span data-stu-id="372eb-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="372eb-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="372eb-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="372eb-149">IID</span><span class="sxs-lookup"><span data-stu-id="372eb-149">IID</span></span><br/>     | <span data-ttu-id="372eb-150">IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="372eb-150">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="372eb-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="372eb-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="372eb-152">**Patch**</span><span class="sxs-lookup"><span data-stu-id="372eb-152">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="372eb-153">**Msisourcelistgetinfo**</span><span class="sxs-lookup"><span data-stu-id="372eb-153">**MsiSourceListGetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[<span data-ttu-id="372eb-154">**Msisourcelisteintinfo**</span><span class="sxs-lookup"><span data-stu-id="372eb-154">**MsiSourceListSetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[<span data-ttu-id="372eb-155">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="372eb-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




