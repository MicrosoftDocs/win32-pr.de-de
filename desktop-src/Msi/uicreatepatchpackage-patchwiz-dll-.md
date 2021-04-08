---
description: Die uikreatepatchpackage-Funktion nimmt eine Paket Erstellungs Datei (PCP-Datei) an und generiert ein Windows Installer Patchpaket (MSP-Paket).
ms.assetid: 77fedb80-b664-417d-879b-846e74cc4c23
title: Uikreatepatchpackage (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bcda07d74ffc32c76809037d9ac90cf11ea25c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861900"
---
# <a name="uicreatepatchpackage-patchwizdll"></a><span data-ttu-id="6def1-103">Uikreatepatchpackage (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="6def1-103">UiCreatePatchPackage (Patchwiz.dll)</span></span>

<span data-ttu-id="6def1-104">Die uikreatepatchpackage-Funktion nimmt eine Paket Erstellungs Datei (PCP-Datei) an und generiert ein Windows Installer Patchpaket (MSP-Paket).</span><span class="sxs-lookup"><span data-stu-id="6def1-104">The UiCreatePatchPackage function takes a package creation file (.pcp file) and generates a Windows Installer patch package (.msp package).</span></span> <span data-ttu-id="6def1-105">Das Aufrufen von [Msimsp.exe](msimsp-exe.md) ist die empfohlene Methode für die Verwendung von [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="6def1-105">Calling [Msimsp.exe](msimsp-exe.md) is the recommended method for using [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="6def1-106">Die [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion ist in Version 4,0 von Patchwiz.dll verfügbar und erweitert die Funktionalität der uikreatepatchpackage-Funktion.</span><span class="sxs-lookup"><span data-stu-id="6def1-106">The [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function is available in version 4.0 of Patchwiz.dll and extends the functionality of the UiCreatePatchPackage function.</span></span>

``` syntax
UINT UiCreatePatchPackage(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  Bool fRemoveTempFolderContents  
);
```

## <a name="parameters"></a><span data-ttu-id="6def1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6def1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6def1-108"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szpcppath*</span><span class="sxs-lookup"><span data-stu-id="6def1-108"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span></span>
</dt> <dd>

<span data-ttu-id="6def1-109">Vollständiger Pfad zur Eigenschaften Datei für die Patcherstellung (PCP-Datei) für diesen Patch.</span><span class="sxs-lookup"><span data-stu-id="6def1-109">Full path to the patch creation properties file (.pcp file) for this patch.</span></span>

</dd> <dt>

<span data-ttu-id="6def1-110"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szpatchpfad*</span><span class="sxs-lookup"><span data-stu-id="6def1-110"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span></span>
</dt> <dd>

<span data-ttu-id="6def1-111">Vollständiger Pfad zum Windows Installer Patchpaket (MSP-Datei), das erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6def1-111">Full path to the Windows Installer patch package (.msp file) that is to be created.</span></span> <span data-ttu-id="6def1-112">Dieser Parameter kann **null** oder eine leere Zeichenfolge sein, wird jedoch möglicherweise nicht ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="6def1-112">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="6def1-113">Wenn Sie **null** oder eine leere Zeichenfolge ist, verwendet die Funktion den Wert von "patchoutputpath" in der [Properties-Tabelle (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="6def1-113">If it is **NULL** or an empty string, the function uses the value of PatchOutputPath in the [Properties Table (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="6def1-114"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szlogpath*</span><span class="sxs-lookup"><span data-stu-id="6def1-114"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span></span>
</dt> <dd>

<span data-ttu-id="6def1-115">Vollständiger Pfad zu einer Text Protokolldatei, die angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6def1-115">Full path to a text log file that will be appended.</span></span> <span data-ttu-id="6def1-116">Dieser Parameter kann **null** oder eine leere Zeichenfolge sein, wird jedoch möglicherweise nicht ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="6def1-116">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="6def1-117"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndstatus*</span><span class="sxs-lookup"><span data-stu-id="6def1-117"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span></span>
</dt> <dd>

<span data-ttu-id="6def1-118">Handle für ein Fenster, in dem der Status Text angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6def1-118">Handle to a window that displays the status text.</span></span> <span data-ttu-id="6def1-119">Dieser Parameter kann **null** oder eine leere Zeichenfolge sein, wird jedoch möglicherweise nicht ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="6def1-119">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="6def1-120"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*sztempfolder*</span><span class="sxs-lookup"><span data-stu-id="6def1-120"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span></span>
</dt> <dd>

<span data-ttu-id="6def1-121">Speicherort für temporäre Dateien.</span><span class="sxs-lookup"><span data-stu-id="6def1-121">Location for temporary files.</span></span> <span data-ttu-id="6def1-122">Dieser Parameter kann **null** oder eine leere Zeichenfolge sein, wird jedoch möglicherweise nicht ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="6def1-122">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="6def1-123">Der Standard Speicherort ist% tmp% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="6def1-123">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="6def1-124"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fremuvetempfoldercontents*</span><span class="sxs-lookup"><span data-stu-id="6def1-124"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span></span>
</dt> <dd>

<span data-ttu-id="6def1-125">Wenn **true**, entfernen Sie den temporären Ordner und seinen gesamten Inhalt, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6def1-125">If **TRUE**, remove the temporary folder and all of its contents if present.</span></span> <span data-ttu-id="6def1-126">Wenn **false** und der Ordner vorhanden ist, schlägt die Funktion fehl.</span><span class="sxs-lookup"><span data-stu-id="6def1-126">If **FALSE**, and folder is present, the function fails.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="6def1-127">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="6def1-127">Return Values</span></span>

<span data-ttu-id="6def1-128">Weitere Informationen finden Sie in der Tabelle unter [Rückgabewerte für uikreatepatchpackage](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="6def1-128">See the table in [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6def1-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6def1-129">Remarks</span></span>

<span data-ttu-id="6def1-130">Ein Beispiel für das Erstellen einer PCP-Datei und die Verwendung von uikreatepatchpackage zum Generieren eines Windows Installer Patchpakets finden Sie im Abschnitt [ein Beispiel für ein kleines Update Patching](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="6def1-130">For an example of authoring a .pcp file and using UiCreatePatchPackage to generate a Windows Installer patch package, see the section [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="6def1-131">Zum Erstellen eines Patches ist ein nicht komprimiertes Setup Image erforderlich, z. b. ein administratives Image oder ein nicht komprimiertes Setup-Image von einer CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="6def1-131">Creating a patch requires an uncompressed setup image, such as an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="6def1-132">Uikreatepatchpackage generiert keine binären Patches für Dateien in den CAB-Dateien.</span><span class="sxs-lookup"><span data-stu-id="6def1-132">UiCreatePatchPackage does not generate binary patches for files in cabinets.</span></span>

 

 



