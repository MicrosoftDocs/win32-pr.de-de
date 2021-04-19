---
description: Für jedes Produkt, das im Patchpaket als berechtigt zum Empfangen des Patches aufgeführt ist, ruft die Applypatch-Methode des Installerobjekts eine Installation auf und legt die Patch-Eigenschaft auf den Pfad des Patchpakets fest.
ms.assetid: eee93b6d-f45b-40ae-8e17-cfe6f46b66f4
title: Installer. Applypatch-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyPatch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc1b7509ddb4c61fa84a4547dcd47f2c7637b913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368542"
---
# <a name="installerapplypatch-method"></a><span data-ttu-id="400ef-103">Installer. Applypatch-Methode</span><span class="sxs-lookup"><span data-stu-id="400ef-103">Installer.ApplyPatch method</span></span>

<span data-ttu-id="400ef-104">Für jedes Produkt, das im Patchpaket als berechtigt zum Empfangen des Patches aufgeführt ist, ruft die **Applypatch** -Methode des [**Installerobjekts**](installer-object.md) eine Installation auf und legt die [**Patch**](patch.md) -Eigenschaft auf den Pfad des Patchpakets fest.</span><span class="sxs-lookup"><span data-stu-id="400ef-104">For each product listed by the patch package as eligible to receive the patch, the **ApplyPatch** method of the [**Installer**](installer-object.md) object invokes an installation and sets the [**PATCH**](patch.md) property to the path of the patch package.</span></span>

## <a name="syntax"></a><span data-ttu-id="400ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="400ef-105">Syntax</span></span>


```JScript
Installer.ApplyPatch(
  PatchPackage,
  InstallPackage,
  InstallType,
  CommandLine
)
```



## <a name="parameters"></a><span data-ttu-id="400ef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="400ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="400ef-107">*Patchpaket*</span><span class="sxs-lookup"><span data-stu-id="400ef-107">*PatchPackage*</span></span> 
</dt> <dd>

<span data-ttu-id="400ef-108">Gibt einen Pfad zum Patchpaket an.</span><span class="sxs-lookup"><span data-stu-id="400ef-108">Specifies a path to the patch package.</span></span>

</dd> <dt>

<span data-ttu-id="400ef-109">*INSTALLPACKAGE*</span><span class="sxs-lookup"><span data-stu-id="400ef-109">*InstallPackage*</span></span> 
</dt> <dd>

<span data-ttu-id="400ef-110">Wenn *InstallType* auf msiinstalltypetworkimage festgelegt ist, gibt *INSTALLPACKAGE* den Pfad zu dem Produkt an, das gepatcht werden soll.</span><span class="sxs-lookup"><span data-stu-id="400ef-110">If *InstallType* is set to msiInstallTypeNetworkImage, *InstallPackage* specifies the path to the product that is to be patched.</span></span> <span data-ttu-id="400ef-111">Wenn *InstallType* auf msiinstalltypedefault und *INSTALLPACKAGE* auf 0 festgelegt ist, wendet das Installationsprogramm den Patch auf jedes berechtigte Produkt an, das im Patchpaket aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="400ef-111">If *InstallType* is set to msiInstallTypeDefault and *InstallPackage* is set to 0, the installer applies the patch to every eligible product listed in the patch package.</span></span>

<span data-ttu-id="400ef-112">Wenn *InstallType* den Wert msiinstalltypesingleinstance hat, wendet das Installationsprogramm den Patch auf das von *INSTALLPACKAGE* angegebene Produkt an.</span><span class="sxs-lookup"><span data-stu-id="400ef-112">If *InstallType* is msiInstallTypeSingleInstance, the installer applies the patch to the product specified by *InstallPackage*.</span></span> <span data-ttu-id="400ef-113">In diesem Fall werden andere im Patchpaket aufgelistete geeignete Produkte ignoriert, und der Parameter " *INSTALLPACKAGE* " enthält die auf NULL endenden Zeichenfolge, die den Produktcode der zu patchenden Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="400ef-113">In this case, other eligible products listed in the patch package are ignored and the *InstallPackage* parameter contains the null-terminated string representing the product code of the instance to patch.</span></span> <span data-ttu-id="400ef-114">Diese Art der Installation erfordert die Windows Installer Version, die in Windows Server 2003 oder höher oder Windows Installer XP SP1 oder höher enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="400ef-114">This type of installation requires the Windows Installer version shipped with the Windows Server 2003 or later or Windows Installer XP SP1 or later.</span></span>

</dd> <dt>

<span data-ttu-id="400ef-115">*InstallType*</span><span class="sxs-lookup"><span data-stu-id="400ef-115">*InstallType*</span></span> 
</dt> <dd>

<span data-ttu-id="400ef-116">Dieser Parameter gibt den Typ der zu patchenden Installation an.</span><span class="sxs-lookup"><span data-stu-id="400ef-116">This parameter specifies the type of installation to patch.</span></span> <span data-ttu-id="400ef-117">Der *InstallType* -Parameter wird ignoriert, wenn *INSTALLPACKAGE* ausgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="400ef-117">The *InstallType* parameter is ignored if *InstallPackage* is omitted.</span></span>



| <span data-ttu-id="400ef-118">Wert</span><span class="sxs-lookup"><span data-stu-id="400ef-118">Value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="400ef-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="400ef-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallTypeNetworkImage"></span><span id="msiinstalltypenetworkimage"></span><span id="MSIINSTALLTYPENETWORKIMAGE"></span><dl> <span data-ttu-id="400ef-120"><dt>**msiinstalltypetworkimage**</dt></span><span class="sxs-lookup"><span data-stu-id="400ef-120"><dt>**msiInstallTypeNetworkImage**</dt></span></span> </dl> | <span data-ttu-id="400ef-121">Gibt eine administrative Installation an.</span><span class="sxs-lookup"><span data-stu-id="400ef-121">Indicates a administrative installation.</span></span> <span data-ttu-id="400ef-122">In diesem Fall muss *INSTALLPACKAGE* auf einen Paketpfad festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="400ef-122">In this case, *InstallPackage* must be set to a package path.</span></span> <span data-ttu-id="400ef-123">Der Wert 1 für msiinstalltypetworkimage gibt eine administrative Installation an.</span><span class="sxs-lookup"><span data-stu-id="400ef-123">A value of 1 for msiInstallTypeNetworkImage specifies a administrative installation.</span></span><br/>                                                                                                                                                                                                                    |
| <span id="msiInstallTypeDefault"></span><span id="msiinstalltypedefault"></span><span id="MSIINSTALLTYPEDEFAULT"></span><dl> <span data-ttu-id="400ef-124"><dt>**msiinstalltypedefault**</dt></span><span class="sxs-lookup"><span data-stu-id="400ef-124"><dt>**msiInstallTypeDefault**</dt></span></span> </dl>                     | <span data-ttu-id="400ef-125">Sucht das System nach Produkten, die gepatcht werden.</span><span class="sxs-lookup"><span data-stu-id="400ef-125">Searches system for products to patch.</span></span> <span data-ttu-id="400ef-126">In diesem Fall muss *INSTALLPACKAGE* eine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="400ef-126">In this case, *InstallPackage* must be an empty string.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiInstallSingleInstance"></span><span id="msiinstallsingleinstance"></span><span id="MSIINSTALLSINGLEINSTANCE"></span><dl> <span data-ttu-id="400ef-127"><dt>**msiinstallsingleinstance**</dt></span><span class="sxs-lookup"><span data-stu-id="400ef-127"><dt>**msiInstallSingleInstance**</dt></span></span> </dl>         | <span data-ttu-id="400ef-128">Patchen Sie das von *INSTALLPACKAGE* angegebene Produkt.</span><span class="sxs-lookup"><span data-stu-id="400ef-128">Patch the product specified by *InstallPackage*.</span></span> <span data-ttu-id="400ef-129">*INSTALLPACKAGE* ist der Produktcode der zu patchenden Instanz.</span><span class="sxs-lookup"><span data-stu-id="400ef-129">*InstallPackage* is the product code of the instance to patch.</span></span> <span data-ttu-id="400ef-130">Diese Art der Installation erfordert die Windows Installer Version, die in Windows Server 2003 oder höher oder Windows Installer XP SP1 oder höher enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="400ef-130">This type of installation requires the Windows Installer version shipped with Windows Server 2003 or later or Windows Installer XP SP1 or later.</span></span> <span data-ttu-id="400ef-131">Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="400ef-131">For more information see, [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="400ef-132">*CommandLine*</span><span class="sxs-lookup"><span data-stu-id="400ef-132">*CommandLine*</span></span> 
</dt> <dd>

<span data-ttu-id="400ef-133">Gibt die Eigenschaften Einstellungen an, die in der Befehlszeile festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="400ef-133">Specifies property settings being set on the command line.</span></span> <span data-ttu-id="400ef-134">Siehe Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="400ef-134">See Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="400ef-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="400ef-135">Return value</span></span>

<span data-ttu-id="400ef-136">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="400ef-136">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="400ef-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="400ef-137">Remarks</span></span>

<span data-ttu-id="400ef-138">Da das Listen Trennzeichen für Transformationen, Quellen und Patches ein Semikolon ist, sollte dieses Zeichen nicht für Dateinamen oder Pfade verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="400ef-138">Because the list delimiter for transforms, sources, and patches is a semicolon, this character should not be used for file names or paths.</span></span>

<span data-ttu-id="400ef-139">Die Eigenschaft [**Neuinstallation**](reinstall.md) ist erforderlich, wenn ein [kleines Update](small-updates.md) oder ein kleines [Upgradepatch](minor-upgrades.md) angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="400ef-139">The [**REINSTALL**](reinstall.md) property is required when applying a [small update](small-updates.md) or [minor upgrade](minor-upgrades.md) patch.</span></span> <span data-ttu-id="400ef-140">Ohne diese Eigenschaft ist der Patch auf dem System registriert, kann aber keine Dateien aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="400ef-140">Without this property, the patch is registered on the system but cannot update files.</span></span>

<span data-ttu-id="400ef-141">**Windows Installer 2,0:** Sie müssen die Eigenschaft [**neu installieren**](reinstall.md) in der Befehlszeile festlegen, wenn Sie ein [kleines Update](small-updates.md) oder ein kleines [Upgradepatch](minor-upgrades.md) anwenden.</span><span class="sxs-lookup"><span data-stu-id="400ef-141">**Windows Installer 2.0:** You must set the [**REINSTALL**](reinstall.md) property on the command line when applying a [small update](small-updates.md) or [minor upgrade](minor-upgrades.md) patch.</span></span> <span data-ttu-id="400ef-142">Für Patches, die keinen [benutzerdefinierten Aktionstyp "51](custom-action-type-51.md) " verwenden, um die Eigenschaften " **REINSTALL** " und " [**REINSTALLMODE**](reinstallmode.md) " automatisch festzulegen, muss die Eigenschaft " **REINSTALL** " explizit mit dem *CommandLine* -Parameter festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="400ef-142">For patches that do not use a [Custom Action Type 51](custom-action-type-51.md) to automatically set the **REINSTALL** and [**REINSTALLMODE**](reinstallmode.md) properties, the **REINSTALL** property must be explicitly set with the *CommandLine* parameter.</span></span> <span data-ttu-id="400ef-143">Legen Sie die Eigenschaft **neu installieren** fest, um die vom Patch betroffenen Features aufzulisten, oder verwenden Sie die Standardeinstellung "REINSTALL = ALL".</span><span class="sxs-lookup"><span data-stu-id="400ef-143">Set the **REINSTALL** property to list the features affected by the patch, or use a practical default setting of "REINSTALL=ALL".</span></span> <span data-ttu-id="400ef-144">Der Standardwert der Eigenschaft **REINSTALLMODE** ist "omus".</span><span class="sxs-lookup"><span data-stu-id="400ef-144">The default value of the **REINSTALLMODE** property is "omus".</span></span>

<span data-ttu-id="400ef-145">**Windows Installer 3,0 und höher:** Ab Windows Installer Version 3,0 wird die Eigenschaft [**neu installieren**](reinstall.md) vom Installationsprogramm konfiguriert und muss nicht in der Befehlszeile festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="400ef-145">**Windows Installer 3.0 and later:** Beginning with Windows Installer version 3.0, the [**REINSTALL**](reinstall.md) property is configured by the installer and does not need to be set on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="400ef-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="400ef-146">Requirements</span></span>



| <span data-ttu-id="400ef-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="400ef-147">Requirement</span></span> | <span data-ttu-id="400ef-148">Wert</span><span class="sxs-lookup"><span data-stu-id="400ef-148">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="400ef-149">Version</span><span class="sxs-lookup"><span data-stu-id="400ef-149">Version</span></span><br/> | <span data-ttu-id="400ef-150">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="400ef-150">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="400ef-151">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="400ef-151">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="400ef-152">Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="400ef-152">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="400ef-153">DLL</span><span class="sxs-lookup"><span data-stu-id="400ef-153">DLL</span></span><br/>     | <dl> <span data-ttu-id="400ef-154"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="400ef-154"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="400ef-155">IID</span><span class="sxs-lookup"><span data-stu-id="400ef-155">IID</span></span><br/>     | <span data-ttu-id="400ef-156">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="400ef-156">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="400ef-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="400ef-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="400ef-158">**Msiapplypatch**</span><span class="sxs-lookup"><span data-stu-id="400ef-158">**MsiApplyPatch**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
</dt> <dt>

[<span data-ttu-id="400ef-159">Informationen zu Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="400ef-159">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="400ef-160">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="400ef-160">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




