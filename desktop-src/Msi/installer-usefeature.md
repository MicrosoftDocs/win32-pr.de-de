---
description: Die usefeature-Methode des Installer-Objekts erhöht den Verwendungs Zähler für eine bestimmte Funktion und gibt den Installationsstatus für diese Funktion zurück. Diese Methode sollte verwendet werden, um anzugeben, dass die Absicht einer Anwendung ist, eine Funktion zu verwenden.
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: Installer. usefeature-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UseFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 355e7f4e64a5cb69ffc0371473cb0db1ac6313a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362089"
---
# <a name="installerusefeature-method"></a><span data-ttu-id="ad80f-104">Installer. usefeature-Methode</span><span class="sxs-lookup"><span data-stu-id="ad80f-104">Installer.UseFeature method</span></span>

<span data-ttu-id="ad80f-105">Die **usefeature** -Methode des [**Installer**](installer-object.md) -Objekts erhöht den Verwendungs Zähler für eine bestimmte Funktion und gibt den Installationsstatus für diese Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="ad80f-105">The **UseFeature** method of the [**Installer**](installer-object.md) object increments the usage count for a particular feature and returns the installation state for that feature.</span></span> <span data-ttu-id="ad80f-106">Diese Methode sollte verwendet werden, um anzugeben, dass die Absicht einer Anwendung ist, eine Funktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad80f-106">This method should be used to indicate an application's intent to use a feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad80f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad80f-107">Syntax</span></span>


```JScript
Installer.UseFeature(
  Product,
  Feature,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="ad80f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad80f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad80f-109">*Produkt*</span><span class="sxs-lookup"><span data-stu-id="ad80f-109">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="ad80f-110">Gibt den Produktcode des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="ad80f-110">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="ad80f-111">*Feature*</span><span class="sxs-lookup"><span data-stu-id="ad80f-111">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="ad80f-112">Identifiziert die zu verwendende Funktion.</span><span class="sxs-lookup"><span data-stu-id="ad80f-112">Identifies the feature to be used.</span></span>

</dd> <dt>

<span data-ttu-id="ad80f-113">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="ad80f-113">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="ad80f-114">Dieser Parameter muss " *msiinstallmudenoerkennungs*" lauten.</span><span class="sxs-lookup"><span data-stu-id="ad80f-114">This parameter must be *msiInstallModeNoDetection*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad80f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad80f-115">Return value</span></span>

<span data-ttu-id="ad80f-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ad80f-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad80f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad80f-117">Remarks</span></span>

<span data-ttu-id="ad80f-118">Die **usefeature** -Methode sollte nur für Funktionen verwendet werden, die bekanntermaßen veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="ad80f-118">The **UseFeature** method should only be used on features known to be published.</span></span> <span data-ttu-id="ad80f-119">Die Anwendung sollte den Status der Funktion ermitteln, indem Sie entweder die [**featurestate**](installer-featurestate.md) -Eigenschaft oder die [**Features**](installer-features.md) -Eigenschaft oder deren API-Entsprechungen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ad80f-119">The application should determine the status of the feature by calling either the [**FeatureState**](installer-featurestate.md) property or [**Features**](installer-features.md) property or their API equivalents.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad80f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad80f-120">Requirements</span></span>



| <span data-ttu-id="ad80f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad80f-121">Requirement</span></span> | <span data-ttu-id="ad80f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ad80f-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad80f-123">Version</span><span class="sxs-lookup"><span data-stu-id="ad80f-123">Version</span></span><br/> | <span data-ttu-id="ad80f-124">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ad80f-124">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ad80f-125">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ad80f-125">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ad80f-126">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="ad80f-126">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ad80f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ad80f-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="ad80f-128"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad80f-128"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ad80f-129">IID</span><span class="sxs-lookup"><span data-stu-id="ad80f-129">IID</span></span><br/>     | <span data-ttu-id="ad80f-130">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ad80f-130">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="ad80f-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad80f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad80f-132">**Msiusefeatureex**</span><span class="sxs-lookup"><span data-stu-id="ad80f-132">**MsiUseFeatureEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 




