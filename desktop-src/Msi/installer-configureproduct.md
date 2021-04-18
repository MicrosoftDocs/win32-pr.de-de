---
description: Mit der Methode "Konfigurations Methode" des Installerobjekts wird ein Produkt installiert oder deinstalliert.
ms.assetid: 1215a03f-6c96-4416-881f-0071c1b3c5df
title: Installer.Configureproduct-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 989855508215b2cd5d04bff7903628513314b9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361077"
---
# <a name="installerconfigureproduct-method"></a><span data-ttu-id="b5e5c-103">Installer.Configureproduct-Methode</span><span class="sxs-lookup"><span data-stu-id="b5e5c-103">Installer.ConfigureProduct method</span></span>

<span data-ttu-id="b5e5c-104">Mit der Methode "Konfigurations Methode" des **Installerobjekts** wird ein Produkt installiert oder deinstalliert. [](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="b5e5c-104">The **ConfigureProduct** method of the [**Installer**](installer-object.md) object installs or uninstalls a product.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5e5c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5e5c-105">Syntax</span></span>


```JScript
Installer.ConfigureProduct(
  Product,
  InstallLevel,
  InstallState
)
```



## <a name="parameters"></a><span data-ttu-id="b5e5c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5e5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5e5c-107">*Produkt*</span><span class="sxs-lookup"><span data-stu-id="b5e5c-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="b5e5c-108">Gibt den Produktcode des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="b5e5c-109">*InstallLevel*</span><span class="sxs-lookup"><span data-stu-id="b5e5c-109">*InstallLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="b5e5c-110">Gibt die Standardkonfiguration für die Installation des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-110">Specifies the default installation configuration of the product.</span></span> <span data-ttu-id="b5e5c-111">Der Parameter "INSTALLLEVEL" wird ignoriert, und alle Funktionen werden installiert, wenn der Parameter "InstallState" auf einen anderen Wert als "msiinstallstatedefault" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-111">The InstallLevel parameter is ignored and all features are installed if the InstallState parameter is set to any other value than msiInstallStateDefault.</span></span>

<span data-ttu-id="b5e5c-112">Dieser Parameter muss entweder 0 (Installation mithilfe der erstellten Funktionsebenen), 65535 (alle Features installieren) oder ein Wert zwischen 0 und 65535 sein, um eine Teilmenge der verfügbaren Features zu installieren.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-112">This parameter must be either 0 (install using authored feature levels), 65535 (install all features), or a value between 0 and 65535 to install a subset of available features.</span></span>

</dd> <dt>

<span data-ttu-id="b5e5c-113">*InstallState*</span><span class="sxs-lookup"><span data-stu-id="b5e5c-113">*InstallState*</span></span> 
</dt> <dd>

<span data-ttu-id="b5e5c-114">Gibt den Installationsstatus für das Feature an.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-114">Specifies the installation state for the feature.</span></span> <span data-ttu-id="b5e5c-115">Dieser Parameter muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-115">This parameter must be one of the following values.</span></span>



| <span data-ttu-id="b5e5c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b5e5c-116">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="b5e5c-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b5e5c-117">Meaning</span></span>                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <span data-ttu-id="b5e5c-118"><dt>**msiinstallstateangekündigten**</dt></span><span class="sxs-lookup"><span data-stu-id="b5e5c-118"><dt>**msiInstallStateAdvertised**</dt></span></span> </dl> | <span data-ttu-id="b5e5c-119">Die Funktion wird angekündigt.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-119">The feature is advertised</span></span><br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <span data-ttu-id="b5e5c-120"><dt>**msiinstallstatuelocal**</dt></span><span class="sxs-lookup"><span data-stu-id="b5e5c-120"><dt>**msiInstallStateLocal**</dt></span></span> </dl>                     | <span data-ttu-id="b5e5c-121">Das Feature wird lokal installiert.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-121">The feature is installed locally.</span></span><br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <span data-ttu-id="b5e5c-122"><dt>**msiinstallstatemissing**</dt></span><span class="sxs-lookup"><span data-stu-id="b5e5c-122"><dt>**msiInstallStateAbsent**</dt></span></span> </dl>                 | <span data-ttu-id="b5e5c-123">Die Funktion ist deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-123">The feature is uninstalled.</span></span><br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <span data-ttu-id="b5e5c-124"><dt>**msiinstallstaatource**</dt></span><span class="sxs-lookup"><span data-stu-id="b5e5c-124"><dt>**msiInstallStateSource**</dt></span></span> </dl>                 | <span data-ttu-id="b5e5c-125">Das Feature wird zum Ausführen von der Quelle installiert.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-125">The feature is installed to run from source.</span></span><br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <span data-ttu-id="b5e5c-126"><dt>**msiinstallstatedefault**</dt></span><span class="sxs-lookup"><span data-stu-id="b5e5c-126"><dt>**msiInstallStateDefault**</dt></span></span> </dl>             | <span data-ttu-id="b5e5c-127">Die Funktion wird am Standard Speicherort installiert.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-127">The feature is installed to its default location.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5e5c-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5e5c-128">Return value</span></span>

<span data-ttu-id="b5e5c-129">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-129">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5e5c-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5e5c-130">Remarks</span></span>

<span data-ttu-id="b5e5c-131">Die Methode " **Konfigurations** Methode" zeigt die Benutzeroberfläche mithilfe der aktuellen Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-131">The **ConfigureProduct** method displays the user interface using current settings.</span></span> <span data-ttu-id="b5e5c-132">Die Benutzeroberflächen Einstellungen können geändert werden, indem Sie die [**uilevel-Eigenschaft (Installer-Objekt)**](installer-uilevel.md) vor dem Aufrufen der Methode " **Konfigurations** Methode" ändern.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-132">User interface settings can be changed by modifying the [**UILevel property (Installer object)**](installer-uilevel.md) before calling the **ConfigureProduct** method.</span></span>

<span data-ttu-id="b5e5c-133">Wenn der Parameter " *InstallState* " auf einen anderen Wert als "msiinstallstatedefault" festgelegt ist, wird der Parameter " *INSTALLLEVEL* " ignoriert, und alle Features des Produkts werden installiert.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-133">If the *InstallState* parameter is set to any other value than msiInstallStateDefault, the *InstallLevel* parameter is ignored and all features of the product are installed.</span></span> <span data-ttu-id="b5e5c-134">Verwenden Sie die Methode " [**Konfigurierung**](installer-configurefeature.md) ", um die Installation einzelner Funktionen zu steuern, wenn der Parameter " *InstallState* " nicht auf "msiinstallstatedefault" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-134">Use the [**ConfigureFeature**](installer-configurefeature.md) method to control the installation of individual features when the *InstallState* parameter is not set to msiInstallStateDefault.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5e5c-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5e5c-135">Requirements</span></span>



| <span data-ttu-id="b5e5c-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5e5c-136">Requirement</span></span> | <span data-ttu-id="b5e5c-137">Wert</span><span class="sxs-lookup"><span data-stu-id="b5e5c-137">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5e5c-138">Version</span><span class="sxs-lookup"><span data-stu-id="b5e5c-138">Version</span></span><br/> | <span data-ttu-id="b5e5c-139">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-139">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b5e5c-140">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b5e5c-140">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b5e5c-141">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5e5c-141">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="b5e5c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b5e5c-142">DLL</span></span><br/>     | <dl> <span data-ttu-id="b5e5c-143"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5e5c-143"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="b5e5c-144">IID</span><span class="sxs-lookup"><span data-stu-id="b5e5c-144">IID</span></span><br/>     | <span data-ttu-id="b5e5c-145">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b5e5c-145">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="b5e5c-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5e5c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5e5c-147">**Msikonfigurireproduct**</span><span class="sxs-lookup"><span data-stu-id="b5e5c-147">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
</dt> <dt>

[<span data-ttu-id="b5e5c-148">Installations-und Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="b5e5c-148">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




