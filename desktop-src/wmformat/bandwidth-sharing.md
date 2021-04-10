---
title: Bandbreiten Freigabe
description: Bandbreiten Freigabe
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- Windows Media-Format-SDK, Bandbreiten Freigabe
- Advanced Systems Format (ASF), Bandbreiten Freigabe
- ASF (Advanced Systems Format), Bandbreiten Freigabe
- Windows Media-Format-SDK, Streams
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- Bandbreiten Freigabe, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2221d2fbc44654af7f12acf6e45fb85ca32b7d2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038576"
---
# <a name="bandwidth-sharing"></a>Bandbreiten Freigabe

Sie können Streams in einer Datei angeben, die, wenn Sie zusammengefasst werden, weniger Bandbreite als die Summe der angegebenen Bitraten kombiniert verwenden. Wenn Sie die Bandbreiten Freigabe im Profil angeben, verdeutlichen Sie, dass Anwendungen, die die verfügbare Bandbreite zum Streamen der Datei benötigt, nicht anders erscheinen.

Keines der Objekte des SDK für das Windows Media-Format ändert das Verhalten in Reaktion auf Informationen zur Bandbreiten Freigabe, die ausschließlich bereitgestellt werden, damit Lese Anwendungen es berücksichtigen können, wenn Sie bestimmen, ob eine Datei mit eingeschränkter Bandbreiten Übermittlung wiedergegeben werden kann.

Die Bandbreiten Freigabe wird mit einem Bandbreiten Freigabe Objekt konfiguriert und einem Profil hinzugefügt, bevor mit dem Schreiben einer Datei begonnen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen der ASF-Datei**](asf-file-features.md)
</dt> <dt>

[**Bandbreiten Freigabe Objekt**](bandwidth-sharing-object.md)
</dt> <dt>

[**Iwmbandwidthsharing-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing)
</dt> <dt>

[**IWMProfile3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)
</dt> <dt>

[**Verwenden der Bandbreiten Freigabe**](using-bandwidth-sharing.md)
</dt> </dl>

 

 




