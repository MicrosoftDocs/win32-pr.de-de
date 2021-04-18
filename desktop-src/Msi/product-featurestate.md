---
description: Die Eigenschaft "featurestate" ist der Installationsstatus des Features für die Instanz dieses Produkts. Diese Eigenschaft ruft "msiqueryfeaturestateex" mit "ProductCode", "UserSID" und dem Kontext des-Objekts auf. Die Funktions-ID wird als Parameter bereitgestellt.
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: Product. featurestate-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f7e602ce5d5b0a8e524f76144c7f1eff8876bb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366025"
---
# <a name="productfeaturestate-method"></a><span data-ttu-id="670ca-104">Product. featurestate-Methode</span><span class="sxs-lookup"><span data-stu-id="670ca-104">Product.FeatureState method</span></span>

<span data-ttu-id="670ca-105">Die Eigenschaft " **featurestate** " ist der Installationsstatus des Features für die Instanz dieses Produkts.</span><span class="sxs-lookup"><span data-stu-id="670ca-105">The **FeatureState** property is the installation state of the feature for the instance of this product.</span></span>

<span data-ttu-id="670ca-106">Diese Eigenschaft ruft " [**msiqueryfeaturestateex**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)" mit " *ProductCode*", " *UserSID* " und dem *Kontext* des-Objekts auf.</span><span class="sxs-lookup"><span data-stu-id="670ca-106">This property calls [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa), with the *ProductCode*, *UserSid* and *Context* of the object.</span></span> <span data-ttu-id="670ca-107">Die Funktions-ID wird als Parameter bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="670ca-107">The feature Id is provided as a parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="670ca-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="670ca-108">Syntax</span></span>


```JScript
Product.FeatureState(
  FeatureId
)
```



## <a name="parameters"></a><span data-ttu-id="670ca-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="670ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="670ca-110">*FeatureId*</span><span class="sxs-lookup"><span data-stu-id="670ca-110">*FeatureId*</span></span> 
</dt> <dd>

<span data-ttu-id="670ca-111">Funktions-ID, die in der Funktions Spalte der [Featuretabelle](feature-table.md)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="670ca-111">Feature Id appearing in the Feature column of the [Feature Table](feature-table.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="670ca-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="670ca-112">Return value</span></span>

<span data-ttu-id="670ca-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="670ca-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="670ca-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="670ca-114">Remarks</span></span>

<span data-ttu-id="670ca-115">Wenn der-Befehl erfolgreich ausgeführt wird, enthält die-Eigenschaft den Wert als **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="670ca-115">If the call succeeds, the property contains the value as a **DWORD**.</span></span>



| <span data-ttu-id="670ca-116">State</span><span class="sxs-lookup"><span data-stu-id="670ca-116">State</span></span>                    | <span data-ttu-id="670ca-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="670ca-117">Meaning</span></span>                                      |
|--------------------------|----------------------------------------------|
| <span data-ttu-id="670ca-118">InstallState \_ angekündigt</span><span class="sxs-lookup"><span data-stu-id="670ca-118">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="670ca-119">Diese Funktion wird angekündigt.</span><span class="sxs-lookup"><span data-stu-id="670ca-119">This feature is advertised.</span></span>                  |
| <span data-ttu-id="670ca-120">InstallState \_ lokal</span><span class="sxs-lookup"><span data-stu-id="670ca-120">INSTALLSTATE\_LOCAL</span></span>      | <span data-ttu-id="670ca-121">Das Feature wird lokal installiert.</span><span class="sxs-lookup"><span data-stu-id="670ca-121">The feature is installed locally.</span></span>            |
| <span data-ttu-id="670ca-122">InstallState- \_ Quelle</span><span class="sxs-lookup"><span data-stu-id="670ca-122">INSTALLSTATE\_SOURCE</span></span>     | <span data-ttu-id="670ca-123">Das Feature wird zum Ausführen von der Quelle installiert.</span><span class="sxs-lookup"><span data-stu-id="670ca-123">The feature is installed to run from source.</span></span> |



 

<span data-ttu-id="670ca-124">Wenn der-Befehl fehlschlägt, enthält die-Eigenschaft einen Fehlercode von [**msiqueryfeaturestateex**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).</span><span class="sxs-lookup"><span data-stu-id="670ca-124">If the call fails, the property contains an error code from [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).</span></span>



| <span data-ttu-id="670ca-125">Fehler</span><span class="sxs-lookup"><span data-stu-id="670ca-125">Error</span></span>                     | <span data-ttu-id="670ca-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="670ca-126">Meaning</span></span>                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="670ca-127">Fehler \_ Zugriff \_ verweigert</span><span class="sxs-lookup"><span data-stu-id="670ca-127">ERROR\_ACCESS\_DENIED</span></span>     | <span data-ttu-id="670ca-128">Der Aufrufprozess muss über Administratorrechte verfügen, um Informationen zu einem Produkt zu erhalten, das für einen anderen Benutzer als den aktuellen Benutzer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="670ca-128">The calling process must have administrative privileges to get information for a product installed for a user other than the current user.</span></span> |
| <span data-ttu-id="670ca-129">Fehler \_ hafte \_ Konfiguration</span><span class="sxs-lookup"><span data-stu-id="670ca-129">ERROR\_BAD\_CONFIGURATION</span></span> | <span data-ttu-id="670ca-130">Die Konfigurationsdaten sind beschädigt.</span><span class="sxs-lookup"><span data-stu-id="670ca-130">The configuration data is corrupt.</span></span>                                                                                                         |
| <span data-ttu-id="670ca-131">Fehler bei \_ ungültigem \_ Parameter</span><span class="sxs-lookup"><span data-stu-id="670ca-131">ERROR\_INVALID\_PARAMETER</span></span> | <span data-ttu-id="670ca-132">An die Funktion wurde ein ungültiger Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="670ca-132">An invalid parameter was passed to the function.</span></span>                                                                                           |
| <span data-ttu-id="670ca-133">Fehler \_ erfolgreich</span><span class="sxs-lookup"><span data-stu-id="670ca-133">ERROR\_SUCCESS</span></span>            | <span data-ttu-id="670ca-134">Die Funktion wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="670ca-134">The function completed successfully.</span></span>                                                                                                       |
| <span data-ttu-id="670ca-135">Unbekannter Fehler. \_ \_</span><span class="sxs-lookup"><span data-stu-id="670ca-135">ERROR\_UNKNOWN\_FEATURE</span></span>   | <span data-ttu-id="670ca-136">Die Funktions-ID identifiziert keine bekannte Funktion.</span><span class="sxs-lookup"><span data-stu-id="670ca-136">The feature ID does not identify a known feature.</span></span>                                                                                          |
| <span data-ttu-id="670ca-137">Unbekannter Fehler. \_ \_</span><span class="sxs-lookup"><span data-stu-id="670ca-137">ERROR\_UNKNOWN\_PRODUCT</span></span>   | <span data-ttu-id="670ca-138">Der Produktcode identifiziert kein bekanntes Produkt.</span><span class="sxs-lookup"><span data-stu-id="670ca-138">The product code does not identify a known product.</span></span>                                                                                        |
| <span data-ttu-id="670ca-139">Fehler bei Fehler \_ Funktion \_</span><span class="sxs-lookup"><span data-stu-id="670ca-139">ERROR\_FUNCTION\_FAILED</span></span>   | <span data-ttu-id="670ca-140">Unerwarteter interner Fehler.</span><span class="sxs-lookup"><span data-stu-id="670ca-140">An unexpected internal failure.</span></span>                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="670ca-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="670ca-141">Requirements</span></span>



| <span data-ttu-id="670ca-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="670ca-142">Requirement</span></span> | <span data-ttu-id="670ca-143">Wert</span><span class="sxs-lookup"><span data-stu-id="670ca-143">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="670ca-144">Version</span><span class="sxs-lookup"><span data-stu-id="670ca-144">Version</span></span><br/> | <span data-ttu-id="670ca-145">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="670ca-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="670ca-146">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="670ca-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="670ca-147">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="670ca-147">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="670ca-148">DLL</span><span class="sxs-lookup"><span data-stu-id="670ca-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="670ca-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="670ca-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="670ca-150">IID</span><span class="sxs-lookup"><span data-stu-id="670ca-150">IID</span></span><br/>     | <span data-ttu-id="670ca-151">IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="670ca-151">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="670ca-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="670ca-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="670ca-153">**Product**</span><span class="sxs-lookup"><span data-stu-id="670ca-153">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="670ca-154">**Msiqueryfeaturestateex**</span><span class="sxs-lookup"><span data-stu-id="670ca-154">**MsiQueryFeatureStateEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[<span data-ttu-id="670ca-155">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="670ca-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




