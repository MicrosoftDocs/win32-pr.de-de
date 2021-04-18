---
description: Die schreibgeschützte featurestate-Eigenschaft gibt den installierten Zustand einer Funktion zurück.
ms.assetid: a3d30296-191e-4446-b5b1-a92f8991926a
title: Installer. featurestate (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cf6fe61899ea1daac37fd678e9f0e70dfcc3af69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365185"
---
# <a name="installerfeaturestate-property"></a><span data-ttu-id="16a94-103">Installer. featurestate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="16a94-103">Installer.FeatureState property</span></span>

<span data-ttu-id="16a94-104">Die schreibgeschützte **featurestate** -Eigenschaft gibt den installierten Zustand einer Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="16a94-104">The read-only **FeatureState** property returns the installed state of a feature.</span></span>

<span data-ttu-id="16a94-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="16a94-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="16a94-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="16a94-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureState
```



## <a name="property-value"></a><span data-ttu-id="16a94-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="16a94-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="16a94-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16a94-108">Remarks</span></span>

<span data-ttu-id="16a94-109">Diese Eigenschaft gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="16a94-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="16a94-110">Wert</span><span class="sxs-lookup"><span data-stu-id="16a94-110">Value</span></span>                     | <span data-ttu-id="16a94-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16a94-111">Description</span></span>                                      |
|---------------------------|--------------------------------------------------|
| <span data-ttu-id="16a94-112">msiinstallstatemissing</span><span class="sxs-lookup"><span data-stu-id="16a94-112">msiInstallStateAbsent</span></span>     | <span data-ttu-id="16a94-113">Das Feature ist nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="16a94-113">The feature is not installed.</span></span>                    |
| <span data-ttu-id="16a94-114">msiinstallstateangekündigten</span><span class="sxs-lookup"><span data-stu-id="16a94-114">msiInstallStateAdvertised</span></span> | <span data-ttu-id="16a94-115">Die Funktion wird angekündigt.</span><span class="sxs-lookup"><span data-stu-id="16a94-115">The feature is advertised.</span></span>                       |
| <span data-ttu-id="16a94-116">msiinstallstatuelocal</span><span class="sxs-lookup"><span data-stu-id="16a94-116">msiInstallStateLocal</span></span>      | <span data-ttu-id="16a94-117">Das Feature wird für die lokale Installation installiert.</span><span class="sxs-lookup"><span data-stu-id="16a94-117">The feature is installed to run locally.</span></span>         |
| <span data-ttu-id="16a94-118">msiinstallstaatource</span><span class="sxs-lookup"><span data-stu-id="16a94-118">msiInstallStateSource</span></span>     | <span data-ttu-id="16a94-119">Das Feature wird zum Ausführen von der Quelle installiert.</span><span class="sxs-lookup"><span data-stu-id="16a94-119">The feature is installed to run from source.</span></span>     |
| <span data-ttu-id="16a94-120">msiinstallstatueingevalidarg</span><span class="sxs-lookup"><span data-stu-id="16a94-120">msiInstallStateInvalidArg</span></span> | <span data-ttu-id="16a94-121">An die Funktion wurde ein ungültiger Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="16a94-121">An invalid parameter was passed to the function.</span></span> |
| <span data-ttu-id="16a94-122">msiinstallstateunknown</span><span class="sxs-lookup"><span data-stu-id="16a94-122">msiInstallStateUnknown</span></span>    | <span data-ttu-id="16a94-123">Der Produktcode oder die featurekennung ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="16a94-123">The product code or feature ID is unknown.</span></span>       |
| <span data-ttu-id="16a94-124">msiinstallstatebadconfig</span><span class="sxs-lookup"><span data-stu-id="16a94-124">msiInstallStateBadConfig</span></span>  | <span data-ttu-id="16a94-125">Die Konfigurationsdaten sind beschädigt.</span><span class="sxs-lookup"><span data-stu-id="16a94-125">The configuration data is corrupt.</span></span>               |



 

 

<span data-ttu-id="16a94-126">Die **featurestate** -Eigenschaft überprüft nicht, ob auf die Funktion zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="16a94-126">The **FeatureState** property does not validate that the feature is accessible.</span></span>

## <a name="requirements"></a><span data-ttu-id="16a94-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16a94-127">Requirements</span></span>



| <span data-ttu-id="16a94-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16a94-128">Requirement</span></span> | <span data-ttu-id="16a94-129">Wert</span><span class="sxs-lookup"><span data-stu-id="16a94-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16a94-130">Version</span><span class="sxs-lookup"><span data-stu-id="16a94-130">Version</span></span><br/> | <span data-ttu-id="16a94-131">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="16a94-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="16a94-132">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="16a94-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="16a94-133">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="16a94-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="16a94-134">DLL</span><span class="sxs-lookup"><span data-stu-id="16a94-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="16a94-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16a94-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="16a94-136">IID</span><span class="sxs-lookup"><span data-stu-id="16a94-136">IID</span></span><br/>     | <span data-ttu-id="16a94-137">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="16a94-137">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="16a94-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16a94-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16a94-139">**MsiQueryFeatureState**</span><span class="sxs-lookup"><span data-stu-id="16a94-139">**MsiQueryFeatureState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




