---
title: Verwenden von Profilen mit dem Writer
description: Verwenden von Profilen mit dem Writer
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- Windows Medienformat-SDK, Schreiben von ASF-Dateien
- Windows Medienformat-SDK, Erstellen von ASF-Dateien
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), Schreiben von Dateien
- ASF (Advanced Systems Format), Schreiben von Dateien
- Advanced Systems Format (ASF), Erstellen von Dateien
- ASF (Advanced Systems Format), Erstellen von Dateien
- Profile,Erstellen von ASF-Dateien
- Profile,Schreiben von ASF-Dateien
- Profile,ASF-Dateierstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0184469215dd109bcc4ca120e2db9cbead8b9bd250cb017456f9d7d08ea46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027268"
---
# <a name="to-use-profiles-with-the-writer"></a>Verwenden von Profilen mit dem Writer

Der Writer verwendet Profildaten zum Erstellen von ASF-Dateien. Sie müssen ein Profil für die Verwendung angeben, bevor Sie etwas anderes mit dem Writer machen.

Sie können ein Systemprofil für die Verwendung mit dem Writer festlegen, indem Sie die Profil-ID an die [**IWMWriter::SetProfileByID-Methode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) übergeben.

Um ein benutzerdefiniertes Profil für die Verwendung mit dem Writer anzugeben, müssen Sie eine [**IWMProfile-Schnittstelle**](iwmprofile.md) für ein Objekt abrufen, das die gewünschten Profildaten enthält. Hierzu können Sie eine der Lademethoden der [**IWMProfileManager-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) verwenden. Nachdem Sie über eine gültige **IWMProfile-Schnittstelle** verfügen, können Sie einen Zeiger darauf an die [**IWMWriter::SetProfile-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) übergeben. Weitere Informationen zu Profileinstellungen finden Sie unter [Arbeiten mit Profilen.](working-with-profiles.md)

Wenn Sie änderungen am Profilobjekt mithilfe der **IWMProfile-Schnittstelle** vornehmen, nachdem Sie das Profil im Writer festgelegt haben, müssen Sie **SetProfile** erneut aufrufen. Ander denn, die Änderungen werden nicht im Writer widergespiegelt. Beim Aufrufen von **SetProfile werden** jedoch alle Headerattribute zurückgesetzt. Legen Sie daher nach dem Aufruf dieser Methode alle erforderlichen Headerattribute fest.

Die folgende Beispielfunktion legt das Profil auf "Windows Media Video 8 for Dial-up Modems (56 KBit/s)" fest:


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
> Es gibt keine vordefinierten Systemprofile, die die Codecs Windows Medienaudio und Video 9-Serie verwenden. Weitere Informationen finden Sie unter [Wiederverwendung von Streamkonfigurationen.](reusing-stream-configurations.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




