---
title: Bandbreitenfreigabe
description: Bandbreitenfreigabe
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- Windows Medienformat-SDK, Bandbreitenfreigabe
- Advanced Systems Format (ASF), Bandbreitenfreigabe
- ASF (Advanced Systems Format), Bandbreitenfreigabe
- Windows Medienformat-SDK,Streams
- Advanced Systems Format (ASF),streams
- ASF (Advanced Systems Format), Streams
- Bandbreitenfreigabe, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b01ff94e82f2ce3609a93278fef30c68e1a59445eea22f68f4b0a5d92371a19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709410"
---
# <a name="bandwidth-sharing"></a>Bandbreitenfreigabe

Sie können Streams in einer Datei angeben, die zusammen eine geringere Bandbreite als die Summe der angegebenen Bitraten zusammen verwenden. Indem Sie die Bandbreitenfreigabe im Profil angeben, verdeutlichen Sie beim Lesen von Anwendungen, dass die verfügbare Bandbreite, die zum Streamen der Datei erforderlich ist, nicht dem ist, was sie andernfalls erscheinen könnte.

Keines der Objekte des Windows Media Format SDK ändert sein Verhalten als Reaktion auf Informationen zur Bandbreitenfreigabe, die ausschließlich bereitgestellt werden, sodass Leseanwendungen dies berücksichtigen können, wenn sie bestimmen, ob eine Datei mit eingeschränkter Bandbreitenbereitstellung abgespielt werden kann.

Die Bandbreitenfreigabe wird mit einem Bandbreitenfreigabeobjekt konfiguriert und einem Profil hinzugefügt, bevor mit dem Schreiben einer Datei beginnt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ASF-Dateifeatures**](asf-file-features.md)
</dt> <dt>

[**Bandwidth Sharing Object**](bandwidth-sharing-object.md)
</dt> <dt>

[**IWMBandwidthSharing-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing)
</dt> <dt>

[**IWMProfile3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)
</dt> <dt>

[**Verwenden der Bandbreitenfreigabe**](using-bandwidth-sharing.md)
</dt> </dl>

 

 




