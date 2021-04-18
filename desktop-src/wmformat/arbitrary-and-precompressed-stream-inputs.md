---
title: Beliebige und vorkomprimierte streameingaben
description: Beliebige und vorkomprimierte streameingaben
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- Advanced Systems Format (ASF), beliebige streameingaben
- ASF (Advanced Systems Format), beliebige streameingaben
- Profile, beliebige streameingaben
- Codecs, beliebige streameingaben
- Advanced Systems Format (ASF), vorkomprimierte streameingaben
- ASF (Advanced Systems Format), vorkomprimierte streameingaben
- Profile, vorkomprimierte streameingaben
- Codecs, vorkomprimierte streameingaben
- vorkomprimierte streameingaben
- beliebige Datenstrom Eingaben
- Streams, beliebige streameingaben
- Streams, vorkomprimierte streameingaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1c95fe992c7638ac923ac07ce159fb5dc4126
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "106338445"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a>Beliebige und vorkomprimierte streameingaben

Nur Eingaben, die von einem der Windows Media-Codecs komprimiert werden, verfügen über mehrere mögliche Eingaben. Die anderen Typen möglicher Eingaben sind willkürliche Eingaben und vorkomprimierte Eingaben. Die Anforderungen für die Eingabeformate für diese Typen werden in diesem Abschnitt beschrieben.

## <a name="arbitrary-stream-inputs"></a>Beliebige Datenstrom Eingaben

Eingaben für beliebige Streamtypen sind identisch mit den im Profil beschriebenen Datenstrom Formaten. Sie sollten keine Eingabeformate für diese Typen festlegen.

## <a name="precompressed-stream-inputs"></a>Vorkomprimierte streameingaben

Wenn Sie einen Stream aus einer Datei in eine andere kopieren, übergeben Sie bereits komprimierte Beispiele. In diesem Fall müssen Sie das Eingabe Eigenschafts Objekt auf **null** festlegen, um den Writer darüber zu informieren, dass die übergebenen Daten nicht überprüft werden müssen. Um das Eingabeformat auf **null** festzulegen, nennen Sie [**iwmwriter:: SetInput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) Eigenschaften, und übergeben Sie **null** als zweiten Parameter. Wenn Sie diese Methode mit einem **null** -Parameter aufrufen, müssen Sie den Aufruf vor dem Aufrufen von [**beginwriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)durchführen.

Wenn Sie vorkomprimierte Streams verwenden, müssen Sie vor dem Schreiben manuell Codec-Informationen in den Dateiheader kopieren. Rufen Sie zum Abrufen der Codec-Informationen [**IWMHeaderInfo2:: getcodecinfocount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) und [**IWMHeaderInfo2:: getcodecinfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) auf, um die Codecs aufzulisten, die der Datei im Reader zugeordnet sind. Wählen Sie die Codec-Informationen aus, die der Datenstrom Konfiguration des vorkomprimierten Streams entsprechen. Legen Sie dann die Codec-Informationen im Writer durch Aufrufen von [**IWMHeaderInfo3:: addcodecinfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo)fest, und übergeben Sie dabei die Informationen, die vom Reader abgerufen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Eingaben**](working-with-inputs.md)
</dt> </dl>

 

 




