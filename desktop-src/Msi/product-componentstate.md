---
description: Die componentstate-Eigenschaft ist der Installationsstatus der Komponente für die Instanz dieses Produkts. Diese Eigenschaft ruft msiquerycomponentstate mit ProductCode, UserSID und Kontext des-Objekts auf.
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: Product. componentstate-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.ComponentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 240a854a899f46bf80703bbd6cfb6b1529848586
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365535"
---
# <a name="productcomponentstate-method"></a><span data-ttu-id="b2e64-103">Product. componentstate-Methode</span><span class="sxs-lookup"><span data-stu-id="b2e64-103">Product.ComponentState method</span></span>

<span data-ttu-id="b2e64-104">Die **componentstate** -Eigenschaft ist der Installationsstatus der Komponente für die Instanz dieses Produkts.</span><span class="sxs-lookup"><span data-stu-id="b2e64-104">The **ComponentState** property is the installation state of the component for the instance of this product.</span></span>

<span data-ttu-id="b2e64-105">Diese Eigenschaft ruft [**msiquerycomponentstate**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)mit ProductCode, UserSID und Kontext des-Objekts auf.</span><span class="sxs-lookup"><span data-stu-id="b2e64-105">This property calls [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea), with the ProductCode, UserSid, and Context of the object.</span></span> <span data-ttu-id="b2e64-106">Die Komponenten-ID-GUID wird als Parameter bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b2e64-106">The component Id GUID is provided as a parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2e64-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2e64-107">Syntax</span></span>


```JScript
Product.ComponentState(
  ID
)
```



## <a name="parameters"></a><span data-ttu-id="b2e64-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2e64-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2e64-109">*ID*</span><span class="sxs-lookup"><span data-stu-id="b2e64-109">*ID*</span></span> 
</dt> <dd>

<span data-ttu-id="b2e64-110">Komponenten Code-GUID der Komponente, wie Sie in der ComponentID-Spalte der [Component-Tabelle](component-table.md)gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="b2e64-110">Component code GUID of the component as found in the ComponentID column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2e64-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2e64-111">Return value</span></span>

<span data-ttu-id="b2e64-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b2e64-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2e64-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2e64-113">Remarks</span></span>

<span data-ttu-id="b2e64-114">Wenn der-Befehl erfolgreich ausgeführt wird, enthält die-Eigenschaft den Wert als **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="b2e64-114">If the call succeeds, the property contains the value as a **DWORD**.</span></span>



| <span data-ttu-id="b2e64-115">State</span><span class="sxs-lookup"><span data-stu-id="b2e64-115">State</span></span>                | <span data-ttu-id="b2e64-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b2e64-116">Meaning</span></span>                                            |
|----------------------|----------------------------------------------------|
| <span data-ttu-id="b2e64-117">InstallState \_ lokal</span><span class="sxs-lookup"><span data-stu-id="b2e64-117">INSTALLSTATE\_LOCAL</span></span>  | <span data-ttu-id="b2e64-118">Die Komponente wird lokal installiert.</span><span class="sxs-lookup"><span data-stu-id="b2e64-118">The component is installed locally.</span></span>                |
| <span data-ttu-id="b2e64-119">InstallState- \_ Quelle</span><span class="sxs-lookup"><span data-stu-id="b2e64-119">INSTALLSTATE\_SOURCE</span></span> | <span data-ttu-id="b2e64-120">Die Komponente wird zum Ausführen von der Quelle installiert.</span><span class="sxs-lookup"><span data-stu-id="b2e64-120">The component is installed to run from the source.</span></span> |



 

<span data-ttu-id="b2e64-121">Wenn der-Befehl fehlschlägt, enthält die-Eigenschaft einen Fehlercode aus [**msiquerycomponentstate**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).</span><span class="sxs-lookup"><span data-stu-id="b2e64-121">If the call fails, the property contains an error code from [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).</span></span>



| <span data-ttu-id="b2e64-122">Fehler</span><span class="sxs-lookup"><span data-stu-id="b2e64-122">Error</span></span>                     | <span data-ttu-id="b2e64-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b2e64-123">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e64-124">Fehler \_ Zugriff \_ verweigert</span><span class="sxs-lookup"><span data-stu-id="b2e64-124">ERROR\_ACCESS\_DENIED</span></span>     | <span data-ttu-id="b2e64-125">Der Aufrufprozess muss über Administratorrechte verfügen, um Informationen für einen anderen Benutzer als den aktuellen Benutzer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b2e64-125">The calling process must have administrative privileges to get information for a user other than the current user.</span></span> |
| <span data-ttu-id="b2e64-126">Fehler \_ hafte \_ Konfiguration</span><span class="sxs-lookup"><span data-stu-id="b2e64-126">ERROR\_BAD\_CONFIGURATION</span></span> | <span data-ttu-id="b2e64-127">Die Konfigurationsdaten sind beschädigt.</span><span class="sxs-lookup"><span data-stu-id="b2e64-127">The configuration data is corrupt.</span></span>                                                                                 |
| <span data-ttu-id="b2e64-128">Fehler bei \_ ungültigem \_ Parameter</span><span class="sxs-lookup"><span data-stu-id="b2e64-128">ERROR\_INVALID\_PARAMETER</span></span> | <span data-ttu-id="b2e64-129">An die Funktion wurde ein ungültiger Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="b2e64-129">An invalid parameter was passed to the function.</span></span>                                                                   |
| <span data-ttu-id="b2e64-130">Fehler \_ erfolgreich</span><span class="sxs-lookup"><span data-stu-id="b2e64-130">ERROR\_SUCCESS</span></span>            | <span data-ttu-id="b2e64-131">Die Funktion wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b2e64-131">The function completed successfully.</span></span>                                                                               |
| <span data-ttu-id="b2e64-132">\_unbekannter Fehler \_ Komponente.</span><span class="sxs-lookup"><span data-stu-id="b2e64-132">ERROR\_UNKNOWN\_COMPONENT</span></span> | <span data-ttu-id="b2e64-133">Die Komponenten-ID identifiziert keine bekannte Komponente.</span><span class="sxs-lookup"><span data-stu-id="b2e64-133">The component ID does not identify a known component.</span></span>                                                              |
| <span data-ttu-id="b2e64-134">Unbekannter Fehler. \_ \_</span><span class="sxs-lookup"><span data-stu-id="b2e64-134">ERROR\_UNKNOWN\_PRODUCT</span></span>   | <span data-ttu-id="b2e64-135">Der Produktcode identifiziert kein bekanntes Produkt.</span><span class="sxs-lookup"><span data-stu-id="b2e64-135">The product code does not identify a known product.</span></span>                                                                |
| <span data-ttu-id="b2e64-136">Fehler bei Fehler \_ Funktion \_</span><span class="sxs-lookup"><span data-stu-id="b2e64-136">ERROR\_FUNCTION\_FAILED</span></span>   | <span data-ttu-id="b2e64-137">Unerwarteter interner Fehler.</span><span class="sxs-lookup"><span data-stu-id="b2e64-137">An unexpected internal failure.</span></span>                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="b2e64-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2e64-138">Requirements</span></span>



| <span data-ttu-id="b2e64-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2e64-139">Requirement</span></span> | <span data-ttu-id="b2e64-140">Wert</span><span class="sxs-lookup"><span data-stu-id="b2e64-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e64-141">Version</span><span class="sxs-lookup"><span data-stu-id="b2e64-141">Version</span></span><br/> | <span data-ttu-id="b2e64-142">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b2e64-142">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b2e64-143">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b2e64-143">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b2e64-144">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b2e64-144">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="b2e64-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b2e64-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="b2e64-146"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2e64-146"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="b2e64-147">IID</span><span class="sxs-lookup"><span data-stu-id="b2e64-147">IID</span></span><br/>     | <span data-ttu-id="b2e64-148">IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b2e64-148">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="b2e64-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2e64-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e64-150">**Product**</span><span class="sxs-lookup"><span data-stu-id="b2e64-150">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="b2e64-151">**Msiquerycomponentstate**</span><span class="sxs-lookup"><span data-stu-id="b2e64-151">**MsiQueryComponentState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[<span data-ttu-id="b2e64-152">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b2e64-152">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




