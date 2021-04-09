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
# <a name="to-use-profiles-with-the-writer"></a>Verwenden von Profilen mit dem Writer

Der Writer verwendet Profildaten zum Erstellen von ASF-Dateien. Sie müssen ein Profil angeben, das Sie verwenden möchten, bevor Sie mit dem Writer andere Aktionen ausführen.

Sie können ein Systemprofil für die Verwendung mit dem Writer festlegen, indem Sie die Profil-ID an die [**iwmwriter:: setprofilebyid**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) -Methode übergeben.

Um ein benutzerdefiniertes Profil für die Verwendung mit dem Writer anzugeben, müssen Sie eine [**iwmprofile**](iwmprofile.md) -Schnittstelle für ein Objekt abrufen, das die gewünschten Profildaten enthält. Hierfür können Sie eine der Methoden zum Laden der [**iwmprofilemanager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) -Schnittstelle verwenden. Nachdem Sie über eine gültige **iwmprofile** -Schnittstelle verfügen, können Sie einen Zeiger darauf an die [**iwmwriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) -Methode übergeben. Weitere Informationen zu Profileinstellungen finden Sie unter [Arbeiten mit Profilen](working-with-profiles.md).

Wenn Sie Änderungen am Profil Objekt mithilfe der **iwmprofile** -Schnittstelle vornehmen, nachdem Sie das Profil im Writer festgelegt haben, müssen Sie **setprofile** erneut aufrufen. andernfalls werden die Änderungen nicht im Writer widergespiegelt. Wenn Sie **setprofile** aufrufen, werden allerdings alle Header Attribute zurückgesetzt. Achten Sie daher darauf, dass Sie nach dem Aufrufen dieser Methode alle erforderlichen Header Attribute festlegen.

Mit der folgenden Beispiel Funktion wird das Profil auf "Windows Media Video 8 für Einwählmodems (56 Kbit/s)" festgelegt:


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
> Es gibt keine vordefinierten Systemprofile, die die Codecs Windows Media Audio und der Video 9-Serie verwenden. Weitere Informationen finden Sie unter [wieder verwenden von streamkonfigurationen](reusing-stream-configurations.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmwriter:: setprofilebyid**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




