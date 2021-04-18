---
description: Die productstate-Eigenschaft ist eine schreibgeschützte Eigenschaft, die die Installations Zustandsinformationen für ein Produkt zurückgibt.
ms.assetid: 9ae3bc86-aa13-41b3-b058-4037607f7dd5
title: Installer. productstate-Eigenschaften Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cdd1397def1cd25405d0a80a6d5cfde2ee6ef77e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368576"
---
# <a name="installerproductstate-property-method"></a><span data-ttu-id="85654-103">Installer. productstate-Eigenschaften Methode</span><span class="sxs-lookup"><span data-stu-id="85654-103">Installer.ProductState Property method</span></span>

<span data-ttu-id="85654-104">Die **productstate-Eigenschaft** ist eine schreibgeschützte Eigenschaft, die die Installations Zustandsinformationen für ein Produkt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="85654-104">The **ProductState property** is a read-only property that returns the install state information for a product.</span></span>

## <a name="syntax"></a><span data-ttu-id="85654-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="85654-105">Syntax</span></span>


```JScript
Installer.ProductState Property(
  Product
)
```



## <a name="parameters"></a><span data-ttu-id="85654-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85654-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85654-107">*Produkt*</span><span class="sxs-lookup"><span data-stu-id="85654-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="85654-108">Gibt den Produktcode des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="85654-108">Specifies the product code of the product.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85654-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85654-109">Return value</span></span>

<span data-ttu-id="85654-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="85654-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85654-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85654-111">Remarks</span></span>

<span data-ttu-id="85654-112">Gibt einen der in der folgenden Tabelle aufgeführten Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="85654-112">Returns one of the values shown in the following table.</span></span>



| <span data-ttu-id="85654-113">Installationsstatus</span><span class="sxs-lookup"><span data-stu-id="85654-113">Installation state</span></span>        | <span data-ttu-id="85654-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85654-114">Description</span></span>                                      |
|---------------------------|--------------------------------------------------|
| <span data-ttu-id="85654-115">msiinstallstatemissing</span><span class="sxs-lookup"><span data-stu-id="85654-115">msiInstallStateAbsent</span></span>     | <span data-ttu-id="85654-116">Das Produkt wird für einen anderen Benutzer installiert.</span><span class="sxs-lookup"><span data-stu-id="85654-116">The product is installed for a different user.</span></span>   |
| <span data-ttu-id="85654-117">msiinstallstatedefault</span><span class="sxs-lookup"><span data-stu-id="85654-117">msiInstallStateDefault</span></span>    | <span data-ttu-id="85654-118">Das Produkt ist für den aktuellen Benutzer installiert.</span><span class="sxs-lookup"><span data-stu-id="85654-118">The product is installed for the current user.</span></span>   |
| <span data-ttu-id="85654-119">msiinstallstateangekündigten</span><span class="sxs-lookup"><span data-stu-id="85654-119">msiInstallStateAdvertised</span></span> | <span data-ttu-id="85654-120">Das Produkt wird angekündigt, aber nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="85654-120">The product is advertised but not installed.</span></span>     |
| <span data-ttu-id="85654-121">msiinstallstatueingevalidarg</span><span class="sxs-lookup"><span data-stu-id="85654-121">msiInstallStateInvalidArg</span></span> | <span data-ttu-id="85654-122">An die Funktion wurde ein ungültiger Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="85654-122">An invalid parameter was passed to the function.</span></span> |
| <span data-ttu-id="85654-123">msiinstallstateunknown</span><span class="sxs-lookup"><span data-stu-id="85654-123">msiInstallStateUnknown</span></span>    | <span data-ttu-id="85654-124">Das Produkt ist weder angekündigt noch installiert.</span><span class="sxs-lookup"><span data-stu-id="85654-124">The product is neither advertised nor installed.</span></span> |
| <span data-ttu-id="85654-125">msiinstallstatebadconfig</span><span class="sxs-lookup"><span data-stu-id="85654-125">msiInstallStateBadConfig</span></span>  | <span data-ttu-id="85654-126">Die Konfigurationsdaten sind beschädigt.</span><span class="sxs-lookup"><span data-stu-id="85654-126">The configuration data is corrupt.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="85654-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85654-127">Requirements</span></span>



| <span data-ttu-id="85654-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85654-128">Requirement</span></span> | <span data-ttu-id="85654-129">Wert</span><span class="sxs-lookup"><span data-stu-id="85654-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85654-130">Version</span><span class="sxs-lookup"><span data-stu-id="85654-130">Version</span></span><br/> | <span data-ttu-id="85654-131">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="85654-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="85654-132">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="85654-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="85654-133">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="85654-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="85654-134">DLL</span><span class="sxs-lookup"><span data-stu-id="85654-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="85654-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85654-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="85654-136">IID</span><span class="sxs-lookup"><span data-stu-id="85654-136">IID</span></span><br/>     | <span data-ttu-id="85654-137">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="85654-137">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="85654-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85654-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85654-139">**Msiqueryproductstate**</span><span class="sxs-lookup"><span data-stu-id="85654-139">**MsiQueryProductState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




