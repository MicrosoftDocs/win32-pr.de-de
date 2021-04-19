---
description: Mit der reinstallproduct-Methode des Installer-Objekts wird ein Produkt neu installiert, oder Installationsprobleme in einem installierten Produkt werden korrigiert.
ms.assetid: ff933cce-9f27-4215-9291-dd860d9c4d08
title: Installer. reinstallproduct-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1570f5a0dc607b4a011a5b4276a243c59a64392d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355927"
---
# <a name="installerreinstallproduct-method"></a><span data-ttu-id="a4688-103">Installer. reinstallproduct-Methode</span><span class="sxs-lookup"><span data-stu-id="a4688-103">Installer.ReinstallProduct method</span></span>

<span data-ttu-id="a4688-104">Mit der **reinstallproduct** -Methode des [**Installer**](installer-object.md) -Objekts wird ein Produkt neu installiert, oder Installationsprobleme in einem installierten Produkt werden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="a4688-104">The **ReinstallProduct** method of the [**Installer**](installer-object.md) object reinstalls a product or corrects installation problems in an installed product.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4688-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4688-105">Syntax</span></span>


```JScript
Installer.ReinstallProduct(
  Product,
  ReinstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="a4688-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4688-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4688-107">*Produkt*</span><span class="sxs-lookup"><span data-stu-id="a4688-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="a4688-108">Gibt den Produktcode des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="a4688-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="a4688-109">*Rein Stall Mode*</span><span class="sxs-lookup"><span data-stu-id="a4688-109">*ReinstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="a4688-110">Gibt den Typ der erneuten Installation an.</span><span class="sxs-lookup"><span data-stu-id="a4688-110">Specifies the type of reinstallation.</span></span> <span data-ttu-id="a4688-111">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a4688-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="a4688-112">Wert</span><span class="sxs-lookup"><span data-stu-id="a4688-112">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="a4688-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a4688-113">Meaning</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <span data-ttu-id="a4688-114"><dt>**msireinstallmudefilemissing**</dt></span><span class="sxs-lookup"><span data-stu-id="a4688-114"><dt>**msiReinstallModeFileMissing**</dt></span></span> </dl>                     | <span data-ttu-id="a4688-115">Wird nur neu installiert, wenn die Datei fehlt.</span><span class="sxs-lookup"><span data-stu-id="a4688-115">Reinstalls only if the file is missing.</span></span><br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <span data-ttu-id="a4688-116"><dt>**msireinstallmudefileolderversion**</dt></span><span class="sxs-lookup"><span data-stu-id="a4688-116"><dt>**msiReinstallModeFileOlderVersion**</dt></span></span> </dl> | <span data-ttu-id="a4688-117">Wird neu installiert, wenn die Datei fehlt oder eine ältere Version ist.</span><span class="sxs-lookup"><span data-stu-id="a4688-117">Reinstalls if the file is missing or is an older version.</span></span><br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <span data-ttu-id="a4688-118"><dt>**msireinstallmudefileequalversion**</dt></span><span class="sxs-lookup"><span data-stu-id="a4688-118"><dt>**msiReinstallModeFileEqualVersion**</dt></span></span> </dl> | <span data-ttu-id="a4688-119">Wird neu installiert, wenn die Datei fehlt oder eine gleichmäßige oder eine ältere Version ist.</span><span class="sxs-lookup"><span data-stu-id="a4688-119">Reinstalls if the file is missing or is an equal or older version.</span></span><br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <span data-ttu-id="a4688-120"><dt>**msireinstallmudefileexact**</dt></span><span class="sxs-lookup"><span data-stu-id="a4688-120"><dt>**msiReinstallModeFileExact**</dt></span></span> </dl>                             | <span data-ttu-id="a4688-121">Wird neu installiert, wenn die Datei fehlt oder eine exakte Version ist.</span><span class="sxs-lookup"><span data-stu-id="a4688-121">Reinstalls if the file is missing or is not an exact version.</span></span><br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <span data-ttu-id="a4688-122"><dt>**msireinstallmudefileverify**</dt></span><span class="sxs-lookup"><span data-stu-id="a4688-122"><dt>**msiReinstallModeFileVerify**</dt></span></span> </dl>                         | <span data-ttu-id="a4688-123">Prüft die Summe der ausführbaren Dateien und installiert sie neu, wenn Sie nicht vorhanden oder beschädigt sind.</span><span class="sxs-lookup"><span data-stu-id="a4688-123">Checks sum executables, and reinstalls if they are missing or corrupt.</span></span><br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <span data-ttu-id="a4688-124"><dt>**msireinstallmodefilereplace**</dt></span><span class="sxs-lookup"><span data-stu-id="a4688-124"><dt>**msiReinstallModeFileReplace**</dt></span></span> </dl>                     | <span data-ttu-id="a4688-125">Installiert alle Dateien unabhängig von der Version neu.</span><span class="sxs-lookup"><span data-stu-id="a4688-125">Reinstalls all files regardless of version.</span></span><br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <span data-ttu-id="a4688-126"><dt>**msireinstallmudeuserdata**</dt></span><span class="sxs-lookup"><span data-stu-id="a4688-126"><dt>**msiReinstallModeUserData**</dt></span></span> </dl>                                 | <span data-ttu-id="a4688-127">Stellt sicher, dass pro = Benutzer Registrierungseinträge erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a4688-127">Ensures required per=user registry entries.</span></span><br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <span data-ttu-id="a4688-128"><dt>**msireinstallmodemachinedata**</dt></span><span class="sxs-lookup"><span data-stu-id="a4688-128"><dt>**msiReinstallModeMachineData**</dt></span></span> </dl>                     | <span data-ttu-id="a4688-129">Stellt die erforderlichen Anforderungen pro = Computer Registrierungseinträge sicher.</span><span class="sxs-lookup"><span data-stu-id="a4688-129">Ensures required per=machine registry entries.</span></span><br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <span data-ttu-id="a4688-130"><dt>**msireinstallmodeshortcut**</dt></span><span class="sxs-lookup"><span data-stu-id="a4688-130"><dt>**msiReinstallModeShortcut**</dt></span></span> </dl>                                 | <span data-ttu-id="a4688-131">Überprüft Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="a4688-131">Validates shortcuts.</span></span><br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <span data-ttu-id="a4688-132"><dt>**"msireinstallmodepackage"**</dt></span><span class="sxs-lookup"><span data-stu-id="a4688-132"><dt>**msiReinstallModePackage**</dt></span></span> </dl>                                     | <span data-ttu-id="a4688-133">Verwendet die Recache-Quelle, um das Paket zu installieren.</span><span class="sxs-lookup"><span data-stu-id="a4688-133">Uses the recache source to install the package.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4688-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4688-134">Return value</span></span>

<span data-ttu-id="a4688-135">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a4688-135">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4688-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4688-136">Requirements</span></span>



| <span data-ttu-id="a4688-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4688-137">Requirement</span></span> | <span data-ttu-id="a4688-138">Wert</span><span class="sxs-lookup"><span data-stu-id="a4688-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4688-139">Version</span><span class="sxs-lookup"><span data-stu-id="a4688-139">Version</span></span><br/> | <span data-ttu-id="a4688-140">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a4688-140">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a4688-141">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a4688-141">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a4688-142">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="a4688-142">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a4688-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a4688-143">DLL</span></span><br/>     | <dl> <span data-ttu-id="a4688-144"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4688-144"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a4688-145">IID</span><span class="sxs-lookup"><span data-stu-id="a4688-145">IID</span></span><br/>     | <span data-ttu-id="a4688-146">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a4688-146">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="a4688-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4688-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4688-148">**Msireinstallproduct**</span><span class="sxs-lookup"><span data-stu-id="a4688-148">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
</dt> <dt>

[<span data-ttu-id="a4688-149">Installations-und Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="a4688-149">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




