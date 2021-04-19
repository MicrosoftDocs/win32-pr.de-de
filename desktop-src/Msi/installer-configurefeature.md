---
description: Mit der Methode "konfigurierte Funktion" des Installerobjekts wird der installierte Zustand einer Produkt Funktion konfiguriert.
ms.assetid: cc950951-3b43-4d86-9ff1-80aa2ccd11d5
title: Installer.Configurefeature-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 737019f5c404beabef404751e617be975b946c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370868"
---
# <a name="installerconfigurefeature-method"></a><span data-ttu-id="b6831-103">Installer.Configurefeature-Methode</span><span class="sxs-lookup"><span data-stu-id="b6831-103">Installer.ConfigureFeature method</span></span>

<span data-ttu-id="b6831-104">Mit der Methode " **konfigurierte Funktion" des Installerobjekts** wird der installierte Zustand einer Produkt Funktion konfiguriert. [](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="b6831-104">The **ConfigureFeature** method of the [**Installer**](installer-object.md) object configures the installed state of a product feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6831-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6831-105">Syntax</span></span>


```JScript
Installer.ConfigureFeature(
  Product,
  Feature,
  InstallState
)
```



## <a name="parameters"></a><span data-ttu-id="b6831-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6831-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6831-107">*Produkt*</span><span class="sxs-lookup"><span data-stu-id="b6831-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="b6831-108">Gibt den Produktcode des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="b6831-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="b6831-109">*Feature*</span><span class="sxs-lookup"><span data-stu-id="b6831-109">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="b6831-110">Gibt die Funktions-ID der Funktion an, die konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6831-110">Specifies the feature ID of the feature to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="b6831-111">*InstallState*</span><span class="sxs-lookup"><span data-stu-id="b6831-111">*InstallState*</span></span> 
</dt> <dd>

<span data-ttu-id="b6831-112">Gibt den Installationsstatus für das Feature an.</span><span class="sxs-lookup"><span data-stu-id="b6831-112">Specifies the installation state for the feature.</span></span> <span data-ttu-id="b6831-113">Dieser Parameter muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b6831-113">This parameter must be one of the following values.</span></span>



| <span data-ttu-id="b6831-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b6831-114">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="b6831-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b6831-115">Meaning</span></span>                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <span data-ttu-id="b6831-116"><dt>**msiinstallstateangekündigten**</dt></span><span class="sxs-lookup"><span data-stu-id="b6831-116"><dt>**msiInstallStateAdvertised**</dt></span></span> </dl> | <span data-ttu-id="b6831-117">Die Funktion wird angekündigt.</span><span class="sxs-lookup"><span data-stu-id="b6831-117">The feature is advertised</span></span><br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <span data-ttu-id="b6831-118"><dt>**msiinstallstatuelocal**</dt></span><span class="sxs-lookup"><span data-stu-id="b6831-118"><dt>**msiInstallStateLocal**</dt></span></span> </dl>                     | <span data-ttu-id="b6831-119">Das Feature wird lokal installiert.</span><span class="sxs-lookup"><span data-stu-id="b6831-119">The feature is installed locally.</span></span><br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <span data-ttu-id="b6831-120"><dt>**msiinstallstatemissing**</dt></span><span class="sxs-lookup"><span data-stu-id="b6831-120"><dt>**msiInstallStateAbsent**</dt></span></span> </dl>                 | <span data-ttu-id="b6831-121">Die Funktion ist deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="b6831-121">The feature is uninstalled.</span></span><br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <span data-ttu-id="b6831-122"><dt>**msiinstallstaatource**</dt></span><span class="sxs-lookup"><span data-stu-id="b6831-122"><dt>**msiInstallStateSource**</dt></span></span> </dl>                 | <span data-ttu-id="b6831-123">Das Feature wird zum Ausführen von der Quelle installiert.</span><span class="sxs-lookup"><span data-stu-id="b6831-123">The feature is installed to run from source.</span></span><br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <span data-ttu-id="b6831-124"><dt>**msiinstallstatedefault**</dt></span><span class="sxs-lookup"><span data-stu-id="b6831-124"><dt>**msiInstallStateDefault**</dt></span></span> </dl>             | <span data-ttu-id="b6831-125">Die Funktion wird am Standard Speicherort installiert.</span><span class="sxs-lookup"><span data-stu-id="b6831-125">The feature is installed to its default location.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6831-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6831-126">Return value</span></span>

<span data-ttu-id="b6831-127">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b6831-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6831-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6831-128">Requirements</span></span>



| <span data-ttu-id="b6831-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6831-129">Requirement</span></span> | <span data-ttu-id="b6831-130">Wert</span><span class="sxs-lookup"><span data-stu-id="b6831-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6831-131">Version</span><span class="sxs-lookup"><span data-stu-id="b6831-131">Version</span></span><br/> | <span data-ttu-id="b6831-132">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b6831-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b6831-133">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b6831-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b6831-134">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="b6831-134">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="b6831-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b6831-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="b6831-136"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6831-136"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="b6831-137">IID</span><span class="sxs-lookup"><span data-stu-id="b6831-137">IID</span></span><br/>     | <span data-ttu-id="b6831-138">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b6831-138">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="b6831-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6831-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6831-140">**Msikonfigurierfeature**</span><span class="sxs-lookup"><span data-stu-id="b6831-140">**MsiConfigureFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[<span data-ttu-id="b6831-141">Installations-und Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="b6831-141">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




