---
description: Die sourcelistinfo-Eigenschaft des Product-Objekts Ruft die Quell Informations Eigenschaften für ein Produkt ab und legt Sie fest. Diese Eigenschaft ruft msisourcelistgetinfo oder msisourcelist* tinfo auf. Dies ist eine Lese-oder Schreib Eigenschaft.
ms.assetid: 3a2c4af5-592f-4acd-b7d8-df163e00b1e2
title: Product. sourcelistinfo-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 23fff0cd478a8345e72b79632817e856c40eb7b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371439"
---
# <a name="productsourcelistinfo-property"></a><span data-ttu-id="7c0c5-105">Product. sourcelistinfo-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7c0c5-105">Product.SourceListInfo property</span></span>

<span data-ttu-id="7c0c5-106">Die **sourcelistinfo** -Eigenschaft des [**Product**](product-object.md) -Objekts Ruft die Quell Informations Eigenschaften für ein Produkt ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-106">The **SourceListInfo** property of the [**Product**](product-object.md) object gets and sets the source information properties for a product.</span></span> <span data-ttu-id="7c0c5-107">Diese Eigenschaft ruft [**msisourcelistgetinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) oder [**msisourcelist* tinfo*\*](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)auf.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-107">This property calls [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) or [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span></span> <span data-ttu-id="7c0c5-108">Dies ist eine Lese-oder Schreib Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-108">This is a read or write property.</span></span>

<span data-ttu-id="7c0c5-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c0c5-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c0c5-110">Syntax</span></span>


```JScript
propVal = Product.SourceListInfo
```



## <a name="property-value"></a><span data-ttu-id="7c0c5-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7c0c5-111">Property value</span></span>

<span data-ttu-id="7c0c5-112">Der Name der Quell Informations Eigenschaften für ein Produkt, das abgefragt oder festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-112">The name of the source information properties for a product to query or set.</span></span> <span data-ttu-id="7c0c5-113">Mögliche Werte finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-113">For possible values, see the Remarks section of this topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c0c5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c0c5-114">Remarks</span></span>

<span data-ttu-id="7c0c5-115">Es können nicht alle Eigenschaften festgelegt werden, die abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-115">Not all properties that can be retrieved can be set.</span></span> <span data-ttu-id="7c0c5-116">Der *szProperty* -Parameter kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-116">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="7c0c5-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7c0c5-117">Property</span></span>         | <span data-ttu-id="7c0c5-118">Kann festgelegt werden?</span><span class="sxs-lookup"><span data-stu-id="7c0c5-118">Can set?</span></span> | <span data-ttu-id="7c0c5-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7c0c5-119">Meaning</span></span>                                                                                                                                                                                                                                                        |
|------------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c0c5-120">Mediapackagepath</span><span class="sxs-lookup"><span data-stu-id="7c0c5-120">MediaPackagePath</span></span> | <span data-ttu-id="7c0c5-121">J</span><span class="sxs-lookup"><span data-stu-id="7c0c5-121">Y</span></span>        | <span data-ttu-id="7c0c5-122">Der Pfad relativ zum Stammverzeichnis des-Installationsmediums.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-122">The path relative to the root of the installation media.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="7c0c5-123">Diskprompt</span><span class="sxs-lookup"><span data-stu-id="7c0c5-123">DiskPrompt</span></span>       | <span data-ttu-id="7c0c5-124">J</span><span class="sxs-lookup"><span data-stu-id="7c0c5-124">Y</span></span>        | <span data-ttu-id="7c0c5-125">Die Eingabe Aufforderungs Vorlage, die verwendet wird, wenn der Benutzer zur Eingabe eines Installationsmediums</span><span class="sxs-lookup"><span data-stu-id="7c0c5-125">The prompt template used when prompting the user for installation media.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="7c0c5-126">LastUsedSource</span><span class="sxs-lookup"><span data-stu-id="7c0c5-126">LastUsedSource</span></span>   | <span data-ttu-id="7c0c5-127">J</span><span class="sxs-lookup"><span data-stu-id="7c0c5-127">Y</span></span>        | <span data-ttu-id="7c0c5-128">Der zuletzt verwendete Quell Speicherort für das Produkt.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-128">The most recently used source location for the product.</span></span> <span data-ttu-id="7c0c5-129">Wenn Sie diese Eigenschaft festlegen, legen Sie den Quell Speicherort für eine Netzwerkquelle oder "u;" für den URL-Typ als Präfix für den Quell Speicherort fest.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-129">When you set this property, prefix the source location with "n;" for a network source or "u;" for URL type.</span></span> <span data-ttu-id="7c0c5-130">Beispiel: "n; \\ \\ Scratch \\ Scratch \\ MySource "und" u; " https://MyServer/MyFolder/MySource .</span><span class="sxs-lookup"><span data-stu-id="7c0c5-130">For example, "n;\\\\scratch\\scratch\\MySource" and "u;https://MyServer/MyFolder/MySource".</span></span> |
| <span data-ttu-id="7c0c5-131">Lastusedtype</span><span class="sxs-lookup"><span data-stu-id="7c0c5-131">LastUsedType</span></span>     | <span data-ttu-id="7c0c5-132">N</span><span class="sxs-lookup"><span data-stu-id="7c0c5-132">N</span></span>        | <span data-ttu-id="7c0c5-133">"n", wenn die zuletzt verwendete Quelle ein Netzwerk Speicherort ist.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-133">"n" if the last-used source is a network location.</span></span> <span data-ttu-id="7c0c5-134">"u", wenn die zuletzt verwendete Quelle ein URL-Speicherort war.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-134">"u" if the last used source was a URL location.</span></span> <span data-ttu-id="7c0c5-135">"m", wenn die zuletzt verwendete Quelle Medien war.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-135">"m" if the last used source was media.</span></span> <span data-ttu-id="7c0c5-136">Leere Zeichenfolge (""), wenn keine zuletzt verwendete Quelle vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-136">Empty string ("") if there is no last used source.</span></span>                                                                   |
| <span data-ttu-id="7c0c5-137">PackageName</span><span class="sxs-lookup"><span data-stu-id="7c0c5-137">PackageName</span></span>      | <span data-ttu-id="7c0c5-138">J</span><span class="sxs-lookup"><span data-stu-id="7c0c5-138">Y</span></span>        | <span data-ttu-id="7c0c5-139">Der Name des Windows Installer Pakets oder Patchpakets in der Quelle.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-139">The name of the Windows Installer package or patch package on the source.</span></span>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="7c0c5-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c0c5-140">Requirements</span></span>



| <span data-ttu-id="7c0c5-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c0c5-141">Requirement</span></span> | <span data-ttu-id="7c0c5-142">Wert</span><span class="sxs-lookup"><span data-stu-id="7c0c5-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c0c5-143">Version</span><span class="sxs-lookup"><span data-stu-id="7c0c5-143">Version</span></span><br/> | <span data-ttu-id="7c0c5-144">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7c0c5-145">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7c0c5-146">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7c0c5-146">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="7c0c5-147">DLL</span><span class="sxs-lookup"><span data-stu-id="7c0c5-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="7c0c5-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c0c5-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="7c0c5-149">IID</span><span class="sxs-lookup"><span data-stu-id="7c0c5-149">IID</span></span><br/>     | <span data-ttu-id="7c0c5-150">IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7c0c5-150">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="7c0c5-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c0c5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c0c5-152">**Product**</span><span class="sxs-lookup"><span data-stu-id="7c0c5-152">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="7c0c5-153">**Msisourcelistgetinfo**</span><span class="sxs-lookup"><span data-stu-id="7c0c5-153">**MsiSourceListGetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[<span data-ttu-id="7c0c5-154">**Msisourcelisteintinfo**</span><span class="sxs-lookup"><span data-stu-id="7c0c5-154">**MsiSourceListSetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[<span data-ttu-id="7c0c5-155">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7c0c5-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




