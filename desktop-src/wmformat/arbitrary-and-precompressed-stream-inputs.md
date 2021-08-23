---
title: Beliebige und vorkomprimierte Streameingaben
description: Beliebige und vorkomprimierte Streameingaben
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- Advanced Systems Format (ASF), beliebige Datenstromeingaben
- ASF (Advanced Systems Format), beliebige Datenstromeingaben
- Profile, beliebige Datenstromeingaben
- Codecs, beliebige Streameingaben
- Advanced Systems Format (ASF), vorkomprimierte Streameingaben
- ASF (Advanced Systems Format), vorkomprimierte Streameingaben
- Profile, vorkomprimierte Streameingaben
- Codecs, vorkomprimierte Streameingaben
- Vorkomprimierte Streameingaben
- Beliebige Datenstromeingaben
- Streams, beliebige Datenstromeingaben
- Streams, vorkomprimierte Streameingaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb0129362e8dc01b7ccf3faabbf10e22ffd4eccc082782796059b3cf4578c33a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119448270"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a>Beliebige und vorkomprimierte Streameingaben

Nur Eingaben, die von einem der Windows Mediencodecs komprimiert werden sollen, verfügen über mehrere mögliche Eingaben. Die anderen möglichen Eingabetypen sind beliebige Eingaben und vorkomprimierte Eingaben. Die Anforderungen für Eingabeformate für diese Typen werden in diesem Abschnitt beschrieben.

## <a name="arbitrary-stream-inputs"></a>Beliebige Datenstromeingaben

Eingaben für beliebige Streamtypen entsprechen den im Profil beschriebenen Streamformaten. Sie sollten keine Eingabeformate für diese Typen festlegen müssen.

## <a name="precompressed-stream-inputs"></a>Vorkomprimierte Streameingaben

Beim Kopieren eines Streams aus einer Datei in eine andere übergeben Sie Beispiele, die bereits komprimiert sind. In diesem Fall müssen Sie das Eingabeeigenschaftenobjekt auf **NULL** festlegen, um den Writer darüber zu informieren, dass die übergebenen Daten nicht überprüft werden müssen. Um das Eingabeformat auf **NULL** festzulegen, rufen [**Sie IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) auf, und übergeben **Sie NULL** als zweiten Parameter. Wenn Sie diese Methode mit einem **NULL-Parameter** aufrufen, müssen Sie den Aufruf vor dem Aufruf von [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)vornehmen.

Wenn Sie vorkomprimierte Streams verwenden, müssen Sie Codecinformationen vor dem Schreiben manuell in den Dateiheader kopieren. Rufen Sie zum Abrufen der Codecinformationen [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) und [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) auf, um die Codecs aufzulisten, die der Datei im Reader zugeordnet sind. Wählen Sie die Codecinformationen aus, die der Streamkonfiguration des vorkomprimierten Streams entsprechen. Legen Sie dann die Codecinformationen im Writer fest, indem [**Sie IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo)aufrufen und die vom Reader abgerufenen Informationen übergeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Eingaben**](working-with-inputs.md)
</dt> </dl>

 

 




