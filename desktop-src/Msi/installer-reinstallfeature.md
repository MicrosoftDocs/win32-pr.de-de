---
description: Die reinstallfeature-Methode des Installer-Objekts installiert Features neu oder korrigiert Probleme mit den installierten Funktionen.
ms.assetid: cfe2aef4-7742-49cd-b7a3-7d484e1f85e3
title: Installer. reinstallfeature-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6bac008ee7121bbcb985b9a8ff5ba02df122266
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371298"
---
# <a name="installerreinstallfeature-method"></a><span data-ttu-id="494c1-103">Installer. reinstallfeature-Methode</span><span class="sxs-lookup"><span data-stu-id="494c1-103">Installer.ReinstallFeature method</span></span>

<span data-ttu-id="494c1-104">Die **reinstallfeature** -Methode des [**Installer**](installer-object.md) -Objekts installiert Features neu oder korrigiert Probleme mit den installierten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="494c1-104">The **ReinstallFeature** method of the [**Installer**](installer-object.md) object reinstalls features or corrects problems with installed features.</span></span>

## <a name="syntax"></a><span data-ttu-id="494c1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="494c1-105">Syntax</span></span>


```JScript
Installer.ReinstallFeature(
  Product,
  Feature,
  ReinstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="494c1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="494c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="494c1-107">*Produkt*</span><span class="sxs-lookup"><span data-stu-id="494c1-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="494c1-108">Gibt den Produktcode des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="494c1-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="494c1-109">*Feature*</span><span class="sxs-lookup"><span data-stu-id="494c1-109">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="494c1-110">Gibt das neu zu installierende Feature an.</span><span class="sxs-lookup"><span data-stu-id="494c1-110">Specifies the feature to be reinstalled.</span></span> <span data-ttu-id="494c1-111">Das übergeordnete Feature oder die untergeordnete Funktion der angegebenen Funktion wird nicht neu installiert.</span><span class="sxs-lookup"><span data-stu-id="494c1-111">The parent feature or child feature of the specified feature is not reinstalled.</span></span> <span data-ttu-id="494c1-112">Um das übergeordnete oder untergeordnete Feature erneut zu installieren, müssen Sie die **reinstallfeature** -Methode für jeden separaten Befehl oder die [**reinstallproduct**](installer-reinstallproduct.md) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="494c1-112">To reinstall the parent or child feature, you must call the **ReinstallFeature** method for each separately or use the [**ReinstallProduct**](installer-reinstallproduct.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="494c1-113">*Rein Stall Mode*</span><span class="sxs-lookup"><span data-stu-id="494c1-113">*ReinstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="494c1-114">Gibt den Typ der erneuten Installation an.</span><span class="sxs-lookup"><span data-stu-id="494c1-114">Specifies the type of reinstallation.</span></span> <span data-ttu-id="494c1-115">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="494c1-115">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="494c1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="494c1-116">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="494c1-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="494c1-117">Meaning</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <span data-ttu-id="494c1-118"><dt>**msireinstallmudefilemissing**</dt></span><span class="sxs-lookup"><span data-stu-id="494c1-118"><dt>**msiReinstallModeFileMissing**</dt></span></span> </dl>                     | <span data-ttu-id="494c1-119">Wird nur neu installiert, wenn die Datei fehlt.</span><span class="sxs-lookup"><span data-stu-id="494c1-119">Reinstalls only if the file is missing.</span></span><br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <span data-ttu-id="494c1-120"><dt>**msireinstallmudefileolderversion**</dt></span><span class="sxs-lookup"><span data-stu-id="494c1-120"><dt>**msiReinstallModeFileOlderVersion**</dt></span></span> </dl> | <span data-ttu-id="494c1-121">Wird neu installiert, wenn die Datei fehlt oder eine ältere Version ist.</span><span class="sxs-lookup"><span data-stu-id="494c1-121">Reinstalls if the file is missing or is an older version.</span></span><br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <span data-ttu-id="494c1-122"><dt>**msireinstallmudefileequalversion**</dt></span><span class="sxs-lookup"><span data-stu-id="494c1-122"><dt>**msiReinstallModeFileEqualVersion**</dt></span></span> </dl> | <span data-ttu-id="494c1-123">Wird neu installiert, wenn die Datei fehlt oder eine gleichmäßige oder eine ältere Version ist.</span><span class="sxs-lookup"><span data-stu-id="494c1-123">Reinstalls if the file is missing or is an equal or older version.</span></span><br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <span data-ttu-id="494c1-124"><dt>**msireinstallmudefileexact**</dt></span><span class="sxs-lookup"><span data-stu-id="494c1-124"><dt>**msiReinstallModeFileExact**</dt></span></span> </dl>                             | <span data-ttu-id="494c1-125">Wird neu installiert, wenn die Datei fehlt oder eine exakte Version ist.</span><span class="sxs-lookup"><span data-stu-id="494c1-125">Reinstalls if the file is missing or is not an exact version.</span></span><br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <span data-ttu-id="494c1-126"><dt>**msireinstallmudefileverify**</dt></span><span class="sxs-lookup"><span data-stu-id="494c1-126"><dt>**msiReinstallModeFileVerify**</dt></span></span> </dl>                         | <span data-ttu-id="494c1-127">Prüft die Summe der ausführbaren Dateien und installiert sie neu, wenn Sie nicht vorhanden oder beschädigt sind.</span><span class="sxs-lookup"><span data-stu-id="494c1-127">Checks sum executables, and reinstalls if they are missing or corrupt.</span></span><br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <span data-ttu-id="494c1-128"><dt>**msireinstallmodefilereplace**</dt></span><span class="sxs-lookup"><span data-stu-id="494c1-128"><dt>**msiReinstallModeFileReplace**</dt></span></span> </dl>                     | <span data-ttu-id="494c1-129">Installiert alle Dateien unabhängig von der Version neu.</span><span class="sxs-lookup"><span data-stu-id="494c1-129">Reinstalls all files regardless of version.</span></span><br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <span data-ttu-id="494c1-130"><dt>**msireinstallmudeuserdata**</dt></span><span class="sxs-lookup"><span data-stu-id="494c1-130"><dt>**msiReinstallModeUserData**</dt></span></span> </dl>                                 | <span data-ttu-id="494c1-131">Stellt sicher, dass pro = Benutzer Registrierungseinträge erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="494c1-131">Ensures required per=user registry entries.</span></span><br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <span data-ttu-id="494c1-132"><dt>**msireinstallmodemachinedata**</dt></span><span class="sxs-lookup"><span data-stu-id="494c1-132"><dt>**msiReinstallModeMachineData**</dt></span></span> </dl>                     | <span data-ttu-id="494c1-133">Stellt die erforderlichen Anforderungen pro = Computer Registrierungseinträge sicher.</span><span class="sxs-lookup"><span data-stu-id="494c1-133">Ensures required per=machine registry entries.</span></span><br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <span data-ttu-id="494c1-134"><dt>**msireinstallmodeshortcut**</dt></span><span class="sxs-lookup"><span data-stu-id="494c1-134"><dt>**msiReinstallModeShortcut**</dt></span></span> </dl>                                 | <span data-ttu-id="494c1-135">Überprüft Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="494c1-135">Validates shortcuts.</span></span><br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <span data-ttu-id="494c1-136"><dt>**"msireinstallmodepackage"**</dt></span><span class="sxs-lookup"><span data-stu-id="494c1-136"><dt>**msiReinstallModePackage**</dt></span></span> </dl>                                     | <span data-ttu-id="494c1-137">Verwendet die Recache-Quelle, um das Paket zu installieren.</span><span class="sxs-lookup"><span data-stu-id="494c1-137">Uses the recache source to install the package.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="494c1-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="494c1-138">Return value</span></span>

<span data-ttu-id="494c1-139">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="494c1-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="494c1-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="494c1-140">Requirements</span></span>



| <span data-ttu-id="494c1-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="494c1-141">Requirement</span></span> | <span data-ttu-id="494c1-142">Wert</span><span class="sxs-lookup"><span data-stu-id="494c1-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="494c1-143">Version</span><span class="sxs-lookup"><span data-stu-id="494c1-143">Version</span></span><br/> | <span data-ttu-id="494c1-144">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="494c1-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="494c1-145">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="494c1-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="494c1-146">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="494c1-146">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="494c1-147">DLL</span><span class="sxs-lookup"><span data-stu-id="494c1-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="494c1-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="494c1-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="494c1-149">IID</span><span class="sxs-lookup"><span data-stu-id="494c1-149">IID</span></span><br/>     | <span data-ttu-id="494c1-150">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="494c1-150">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="494c1-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="494c1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="494c1-152">**Msireinstallfeature**</span><span class="sxs-lookup"><span data-stu-id="494c1-152">**MsiReinstallFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
</dt> <dt>

[<span data-ttu-id="494c1-153">Installations-und Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="494c1-153">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




