---
description: Die patchproperty-Eigenschaft ruft Informationen zu einem bestimmten Patch ab, der auf eine bestimmte Instanz des Produkts angewendet wird. Diese Eigenschaft ruft msigetpatchinfoex auf.
ms.assetid: c58897de-c30b-4269-9926-040613052616
title: Patch. patchproperty-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.PatchProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2ffabcfbfd7e8e97bef97e4e04fbe95fc720eea1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372569"
---
# <a name="patchpatchproperty-method"></a><span data-ttu-id="d9763-104">Patch. patchproperty-Methode</span><span class="sxs-lookup"><span data-stu-id="d9763-104">Patch.PatchProperty method</span></span>

<span data-ttu-id="d9763-105">Die **patchproperty** -Eigenschaft ruft Informationen zu einem bestimmten Patch ab, der auf eine bestimmte Instanz des Produkts angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9763-105">The **PatchProperty** property gets information about a specific patch applied to a specific instance of the product.</span></span> <span data-ttu-id="d9763-106">Diese Eigenschaft ruft [**msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)auf.</span><span class="sxs-lookup"><span data-stu-id="d9763-106">This property calls [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="d9763-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9763-107">Syntax</span></span>


```JScript
Patch.PatchProperty(
  szProperty
)
```



## <a name="parameters"></a><span data-ttu-id="d9763-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9763-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9763-109">*szProperty*</span><span class="sxs-lookup"><span data-stu-id="d9763-109">*szProperty*</span></span> 
</dt> <dd>

<span data-ttu-id="d9763-110">Der *szProperty* -Parameter kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d9763-110">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="d9763-111">Name</span><span class="sxs-lookup"><span data-stu-id="d9763-111">Name</span></span>          | <span data-ttu-id="d9763-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d9763-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9763-113">Localpackage</span><span class="sxs-lookup"><span data-stu-id="d9763-113">LocalPackage</span></span>  | <span data-ttu-id="d9763-114">Dient zum erhalten der vom Produkt verwendeten zwischengespeicherten Patchdatei.</span><span class="sxs-lookup"><span data-stu-id="d9763-114">Get the cached patch file used by the product.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="d9763-115">Transformationen</span><span class="sxs-lookup"><span data-stu-id="d9763-115">Transforms</span></span>    | <span data-ttu-id="d9763-116">Holen Sie sich den Satz von patchtransformationen, die bei der letzten Patchinstallation auf das Produkt angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d9763-116">Get the set of patch transforms applied to the product by the last patch installation.</span></span> <span data-ttu-id="d9763-117">Dieser Wert ist möglicherweise nicht für pro-Benutzer-nicht verwaltete Anwendungen verfügbar, wenn der Benutzer nicht am Computer angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="d9763-117">This value may not be available for per-user-unmanaged applications if the user is not logged in to the computer.</span></span>                                                                                                                     |
| <span data-ttu-id="d9763-118">InstallDate</span><span class="sxs-lookup"><span data-stu-id="d9763-118">InstallDate</span></span>   | <span data-ttu-id="d9763-119">Das Datum der Anwendung des Patches auf das Produkt erhalten.</span><span class="sxs-lookup"><span data-stu-id="d9763-119">Get the date when the patch was applied to the product.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d9763-120">Deinstallierbaren</span><span class="sxs-lookup"><span data-stu-id="d9763-120">Uninstallable</span></span> | <span data-ttu-id="d9763-121">Gibt "1" zurück, wenn der Patch so gekennzeichnet ist, dass er vom Produkt deinstalliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d9763-121">Returns "1" if the patch is marked as possible to uninstall from the product.</span></span> <span data-ttu-id="d9763-122">In diesem Fall kann das Installationsprogramm die Deinstallation weiterhin blockieren, wenn dieser Patch von einem anderen Patch benötigt wird, der nicht deinstalliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d9763-122">In this case, the installer can still block the uninstallation if this patch is required by another patch that cannot be uninstalled.</span></span>                                                                                                          |
| <span data-ttu-id="d9763-123">State</span><span class="sxs-lookup"><span data-stu-id="d9763-123">State</span></span>         | <span data-ttu-id="d9763-124">Gibt "1" zurück, wenn dieser Patch aktuell auf das Produkt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9763-124">Returns "1" if this patch is currently applied to the product.</span></span> <span data-ttu-id="d9763-125">Gibt "2" zurück, wenn dieser Patch durch einen anderen Patch ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="d9763-125">Returns "2" if this patch has been superseded by another patch.</span></span> <span data-ttu-id="d9763-126">Gibt "4" zurück, wenn dieser Patch von einem anderen Patch veraltet gemacht wurde.</span><span class="sxs-lookup"><span data-stu-id="d9763-126">Returns "4" if this patch has been made obsolete by another patch.</span></span> <span data-ttu-id="d9763-127">Diese Werte entsprechen den Konstanten, die vom *dwfilter* -Parameter von [**msienüberpatchesex**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9763-127">These values correspond to the constants used by the *dwFilter* parameter of [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span></span> |
| <span data-ttu-id="d9763-128">DisplayName</span><span class="sxs-lookup"><span data-stu-id="d9763-128">DisplayName</span></span>   | <span data-ttu-id="d9763-129">Hiermit wird der registrierte Anzeige Name für den Patch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d9763-129">Get the registered display name for the patch.</span></span> <span data-ttu-id="d9763-130">Bei Patches, die die DisplayName-Eigenschaft in der [MsiPatchMetadata](msipatchmetadata-table.md) -Tabelle nicht enthalten, ist der zurückgegebene Anzeige Name eine leere Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="d9763-130">For patches that do not include the DisplayName property in the [MsiPatchMetadata](msipatchmetadata-table.md) table, the returned display name is an empty string ("").</span></span>                                                                                                      |
| <span data-ttu-id="d9763-131">MoreInfoUrl</span><span class="sxs-lookup"><span data-stu-id="d9763-131">MoreInfoURL</span></span>   | <span data-ttu-id="d9763-132">Die registrierte Support Informations-URL für den Patch erhalten.</span><span class="sxs-lookup"><span data-stu-id="d9763-132">Get the registered support information URL for the patch.</span></span> <span data-ttu-id="d9763-133">Bei Patches, die die MoreInfoUrl-Eigenschaft in der [MsiPatchMetadata](msipatchmetadata-table.md) -Tabelle nicht enthalten, ist die zurückgegebene URL der Unterstützungs Informationen eine leere Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="d9763-133">For patches that do not include the MoreInfoURL property in the [MsiPatchMetadata](msipatchmetadata-table.md) table, the returned support information URL is an empty string ("").</span></span>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9763-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9763-134">Return value</span></span>

<span data-ttu-id="d9763-135">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d9763-135">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9763-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9763-136">Remarks</span></span>

<span data-ttu-id="d9763-137">Diese Methode kann den Fehler "Unbekannter Patch" zurückgeben \_ \_ , wenn das [**Patch**](patch-object.md) -Objekt mit einer leeren Zeichenfolge für " *ProductCode*" initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d9763-137">This method can return ERROR\_UNKNOWN\_PATCH, if the [**Patch**](patch-object.md) object is initialized with an empty string for *ProductCode*.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9763-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9763-138">Requirements</span></span>



| <span data-ttu-id="d9763-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9763-139">Requirement</span></span> | <span data-ttu-id="d9763-140">Wert</span><span class="sxs-lookup"><span data-stu-id="d9763-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9763-141">Version</span><span class="sxs-lookup"><span data-stu-id="d9763-141">Version</span></span><br/> | <span data-ttu-id="d9763-142">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d9763-142">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d9763-143">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d9763-143">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d9763-144">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d9763-144">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="d9763-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d9763-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="d9763-146"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9763-146"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="d9763-147">IID</span><span class="sxs-lookup"><span data-stu-id="d9763-147">IID</span></span><br/>     | <span data-ttu-id="d9763-148">IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d9763-148">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="d9763-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9763-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9763-150">**Patch**</span><span class="sxs-lookup"><span data-stu-id="d9763-150">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="d9763-151">**Msienum patchesex**</span><span class="sxs-lookup"><span data-stu-id="d9763-151">**MsiEnumPatchesEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[<span data-ttu-id="d9763-152">**Msigetpatchinfoex**</span><span class="sxs-lookup"><span data-stu-id="d9763-152">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="d9763-153">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d9763-153">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




