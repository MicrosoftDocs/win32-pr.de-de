---
title: Schützen von Dateien mit DRM-Version 1
description: Schützen von Dateien mit DRM-Version 1
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
keywords:
- Windows Media-Format-SDK, erstellen geschützter Dateien
- Windows Media-Format-SDK, geschützte Dateien
- Advanced Systems Format (ASF), erstellen geschützter Dateien
- ASF (Advanced Systems Format), erstellen geschützter Dateien
- Advanced Systems Format (ASF), geschützte Dateien
- ASF (Advanced Systems Format), geschützte Dateien
- Advanced Systems Format (ASF), wmstubdrm. lib
- ASF (Advanced Systems Format), wmstubdrm. lib
- Wmstubdrm. lib, erstellen geschützter Dateien
- Wmstubdrm. lib, geschützte Dateien
- Digital Rights Management (DRM), wmstubdrm. lib
- DRM (Digital Rights Management), wmstubdrm. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3e4d1ae9c0d3835c20f75b4e61c262a85a26f4
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314518"
---
# <a name="protecting-files-with-drm-version-1"></a><span data-ttu-id="66335-115">Schützen von Dateien mit DRM-Version 1</span><span class="sxs-lookup"><span data-stu-id="66335-115">Protecting Files with DRM Version 1</span></span>

<span data-ttu-id="66335-116">Wenn diese Art von Schutz angewendet wird, wird eine DRM-Lizenz der Version 1 generiert, die nur auf dem Computer gültig ist, von dem aus die Lizenz Anforderung stammt.</span><span class="sxs-lookup"><span data-stu-id="66335-116">When this kind of protection is applied, a DRM version 1 license is generated that is valid only on the machine from which the license request was made.</span></span> <span data-ttu-id="66335-117">Da kein Schlüssel-oder Schlüssel-Seed festgelegt ist, gibt es keine Möglichkeit, Portable Lizenzen für Inhalte zu generieren, die mit dieser Technik geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="66335-117">Because no key or key seed is set, there is no way to generate portable licenses for content protected using this technique.</span></span> <span data-ttu-id="66335-118">Wenn Sie jedoch das Windows Media-Format SDK 7,1 oder höher verwenden, können die Lizenzen im Microsoft-Lizenz Migrationsdienst wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="66335-118">However, when using the Windows Media Format SDK 7.1 or later, the licenses are recoverable at the Microsoft License Migration service.</span></span>

<span data-ttu-id="66335-119">Führen Sie die folgenden Schritte aus, um die DRM-Dateien mit DRM-Version 1 zu schützen:</span><span class="sxs-lookup"><span data-stu-id="66335-119">To protect ASF files using DRM version 1, perform the following steps:</span></span>

1.  <span data-ttu-id="66335-120">Verknüpfen Sie die Datei wmstubdrm. lib mit Ihrem Projekt, und aufheben Sie ggf. die Verknüpfung von Wmvcore. lib.</span><span class="sxs-lookup"><span data-stu-id="66335-120">Link the WMStubDRM.lib file to your project and, if necessary, unlink wmvcore.lib.</span></span>
2.  <span data-ttu-id="66335-121">Rufen Sie die [**wmkreatewriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) -Funktion auf, um den Writer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="66335-121">Call the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function to create the writer.</span></span> <span data-ttu-id="66335-122">Das erste Argument ist reserviert und muss auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="66335-122">The first argument is reserved and must be set to **NULL**.</span></span>
3.  <span data-ttu-id="66335-123">Legen Sie ein Profil fest, das der Writer verwenden soll, indem Sie [**iwmwriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) oder [**iwmwriter:: setprofilebyid**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="66335-123">Set a profile for the writer to use by calling [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) or [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid).</span></span> <span data-ttu-id="66335-124">Sie müssen ein Profil im Writer festlegen, bevor Sie DRM-Attribute festlegen.</span><span class="sxs-lookup"><span data-stu-id="66335-124">You must set a profile in the writer before setting any DRM attributes.</span></span> <span data-ttu-id="66335-125">DRM wird nur für Profile unterstützt, die die Windows Media Audio oder Windows Media Video Codecs verwenden.</span><span class="sxs-lookup"><span data-stu-id="66335-125">DRM is supported only for profiles that use the Windows Media Audio or Windows Media Video codecs.</span></span>
4.  <span data-ttu-id="66335-126">Legen Sie mithilfe der [**iwmheaderinfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) -Methode die folgenden DRM-Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="66335-126">Using the [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) method, set the following DRM properties.</span></span> <span data-ttu-id="66335-127">Die **Eigenschaft \_ DRM verwenden** weist die DRM-Komponenten an, den Inhalt mithilfe der DRM-Version 1 zu schützen.</span><span class="sxs-lookup"><span data-stu-id="66335-127">The **Use\_DRM** property instructs the DRM components to protect the content using DRM version 1.</span></span> <span data-ttu-id="66335-128">Die Eigenschaft **DRM- \_ Flags** gibt die Rechte an, die in die lokale Lizenz eingeschlossen werden sollen, die für den Inhalt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="66335-128">The **DRM\_Flags** property specifies the rights to be included in the local license that will be created for the content.</span></span> <span data-ttu-id="66335-129">Der Wert der **DRM- \_ Ebene** wird auch in der Lizenz gespeichert. er gibt die minimale Ebene an, die für den Zugriff auf den Inhalt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="66335-129">The **DRM\_LEVEL** value is also stored in the license; it specifies the minimum level required to access the content.</span></span> <span data-ttu-id="66335-130">150 ist die empfohlene Stufe für den Inhalt von DRM-Version 1.</span><span class="sxs-lookup"><span data-stu-id="66335-130">150 is the recommended level for DRM version 1 content.</span></span>

    | <span data-ttu-id="66335-131">Attribut</span><span class="sxs-lookup"><span data-stu-id="66335-131">Attribute</span></span>      | <span data-ttu-id="66335-132">Wert</span><span class="sxs-lookup"><span data-stu-id="66335-132">Value</span></span>                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | <span data-ttu-id="66335-133">**Verwenden von \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="66335-133">**Use\_DRM**</span></span>   | <span data-ttu-id="66335-134">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="66335-134">**TRUE**</span></span>                                                                                    |
    | <span data-ttu-id="66335-135">**DRM- \_ Flags**</span><span class="sxs-lookup"><span data-stu-id="66335-135">**DRM\_Flags**</span></span> | <span data-ttu-id="66335-136">WMT \_ right \_ Playback \| WMT \_ right \_ Copy \_ to \_ Non \_ SDMI \_ Device \| WMT \_ right \_ Copy \_ to \_ CD</span><span class="sxs-lookup"><span data-stu-id="66335-136">WMT\_RIGHT\_PLAYBACK \| WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE \| WMT\_RIGHT\_COPY\_TO\_CD</span></span> |
    | <span data-ttu-id="66335-137">**DRM- \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="66335-137">**DRM\_LEVEL**</span></span> | <span data-ttu-id="66335-138">150</span><span class="sxs-lookup"><span data-stu-id="66335-138">150</span></span>                                                                                         |

    

     

<span data-ttu-id="66335-139">Der folgende Beispielcode zeigt, wie ein DRM-fähiger Writer für DRM-Version 1 erstellt und die DRM-Eigenschaften festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="66335-139">The following example code shows how to create a DRM-enabled writer for DRM version 1 and set the DRM properties.</span></span> <span data-ttu-id="66335-140">Die Fehlerüberprüfung wurde aus Gründen der Verdeutlichung ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="66335-140">Error checking has been omitted for the sake of clarify.</span></span>


```C++
BOOL  fUseDRM    = TRUE;
// These are the rights we will apply to the file. See WMT_RIGHTS for
// the full set of possible rights.

DWORD dwDRMFlags = WMT_RIGHT_PLAYBACK | 
                   WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE | 
                   WMT_RIGHT_COPY_TO_CD;

// Set the minimum required DRM level low enough
// to allow older players to access the content.
DWORD dwDRMLevel = 150;

IWMDRMWriter*  pWMDRMWriter  = NULL;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer object.
hr = WMCreateWriter( NULL, &pWMDRMWriter);

// Obtain the IWMHeaderInfo interface.
hr = pWMDRMWriter -> QueryInterface(IID_IWMHeaderInfo, 
                                   (void**) &pWMHeaderInfo);

// Tell the SDK runtime to protect the file using DRM version 1.
hr= pWMHeaderInfo-> SetAttribute(0,
                                 g_wszWMUse_DRM,
                                 WMT_TYPE_BOOL,
                                 (BYTE*)&fUseDRM,
                                 sizeof(BOOL));

// Specify the rights that will be stored in the local license that is
// created automatically for the content.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Flags, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMFlags,
                                 sizeof(DWORD) );

// Set the DRM_Level attribute in the file's DRM header.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Level, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMLevel,
                                 sizeof(DWORD) );
```



 

 




