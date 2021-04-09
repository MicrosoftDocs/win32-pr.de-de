---
title: Verwenden von Profilen mit dem Writer
description: Verwenden von Profilen mit dem Writer
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- Windows Media-Format-SDK, Schreiben von ASF-Dateien
- Windows Media-Format-SDK, Erstellen von ASF-Dateien
- Windows Media-Format-SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), Schreiben von Dateien
- ASF (Advanced Systems Format), Schreiben von Dateien
- Advanced Systems Format (ASF), Erstellen von Dateien
- ASF (Advanced Systems Format), Erstellen von Dateien
- Profile, Erstellen von ASF-Dateien
- Profile, Schreiben von ASF-Dateien
- Profile, Erstellung von ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d027e6ea0e669d2a5206901faefab1f5a9583153
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104038675"
---
# <a name="to-use-profiles-with-the-writer"></a><span data-ttu-id="00714-113">Verwenden von Profilen mit dem Writer</span><span class="sxs-lookup"><span data-stu-id="00714-113">To Use Profiles with the Writer</span></span>

<span data-ttu-id="00714-114">Der Writer verwendet Profildaten zum Erstellen von ASF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="00714-114">The writer uses profile data to create ASF files.</span></span> <span data-ttu-id="00714-115">Sie müssen ein Profil angeben, das Sie verwenden möchten, bevor Sie mit dem Writer andere Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="00714-115">You must specify a profile for use before doing anything else with the writer.</span></span>

<span data-ttu-id="00714-116">Sie können ein Systemprofil für die Verwendung mit dem Writer festlegen, indem Sie die Profil-ID an die [**iwmwriter:: setprofilebyid**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="00714-116">You can set a system profile for use with the writer by passing the profile ID to the [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) method.</span></span>

<span data-ttu-id="00714-117">Um ein benutzerdefiniertes Profil für die Verwendung mit dem Writer anzugeben, müssen Sie eine [**iwmprofile**](iwmprofile.md) -Schnittstelle für ein Objekt abrufen, das die gewünschten Profildaten enthält.</span><span class="sxs-lookup"><span data-stu-id="00714-117">To specify a custom profile for use with the writer, you must obtain an [**IWMProfile**](iwmprofile.md) interface to an object containing the desired profile data.</span></span> <span data-ttu-id="00714-118">Hierfür können Sie eine der Methoden zum Laden der [**iwmprofilemanager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) -Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="00714-118">You can use one of the loading methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface to accomplish this.</span></span> <span data-ttu-id="00714-119">Nachdem Sie über eine gültige **iwmprofile** -Schnittstelle verfügen, können Sie einen Zeiger darauf an die [**iwmwriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="00714-119">After you have a valid **IWMProfile** interface, you can pass a pointer to it to the [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) method.</span></span> <span data-ttu-id="00714-120">Weitere Informationen zu Profileinstellungen finden Sie unter [Arbeiten mit Profilen](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="00714-120">For more information about profile settings, see [Working with Profiles](working-with-profiles.md).</span></span>

<span data-ttu-id="00714-121">Wenn Sie Änderungen am Profil Objekt mithilfe der **iwmprofile** -Schnittstelle vornehmen, nachdem Sie das Profil im Writer festgelegt haben, müssen Sie **setprofile** erneut aufrufen. andernfalls werden die Änderungen nicht im Writer widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="00714-121">If you make changes to the profile object by using the **IWMProfile** interface after setting the profile in the writer, you must call **SetProfile** again, or else the changes will not be reflected in the writer.</span></span> <span data-ttu-id="00714-122">Wenn Sie **setprofile** aufrufen, werden allerdings alle Header Attribute zurückgesetzt. Achten Sie daher darauf, dass Sie nach dem Aufrufen dieser Methode alle erforderlichen Header Attribute festlegen.</span><span class="sxs-lookup"><span data-stu-id="00714-122">However, calling **SetProfile** will reset all header attributes, so be sure to set any required header attributes after calling this method.</span></span>

<span data-ttu-id="00714-123">Mit der folgenden Beispiel Funktion wird das Profil auf "Windows Media Video 8 für Einwählmodems (56 Kbit/s)" festgelegt:</span><span class="sxs-lookup"><span data-stu-id="00714-123">The following example function sets the profile to "Windows Media Video 8 for Dial-up Modems (56 Kbps)":</span></span>


```C++
#include <wmsysprf.h>

HRESULT SetProfileExample()
{
  HRESULT hr;
  IWMWriter *pWriter = NULL;
  hr = WMCreateWriter(NULL, &pWriter);
  if (FAILED(hr)) return hr;
  hr = pWriter->SetProfileByID(WMProfile_V80_56Video);
  return hr;
}

```



> [!Note]  
> <span data-ttu-id="00714-124">Es gibt keine vordefinierten Systemprofile, die die Codecs Windows Media Audio und der Video 9-Serie verwenden.</span><span class="sxs-lookup"><span data-stu-id="00714-124">There are no predefined system profiles that use the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="00714-125">Weitere Informationen finden Sie unter [wieder verwenden von streamkonfigurationen](reusing-stream-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="00714-125">For more information, see [Reusing Stream Configurations](reusing-stream-configurations.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="00714-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00714-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00714-127">**Iwmwriter:: setprofilebyid**</span><span class="sxs-lookup"><span data-stu-id="00714-127">**IWMWriter::SetProfileByID**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[<span data-ttu-id="00714-128">**Arbeiten mit Profilen**</span><span class="sxs-lookup"><span data-stu-id="00714-128">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> <dt>

[<span data-ttu-id="00714-129">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="00714-129">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




