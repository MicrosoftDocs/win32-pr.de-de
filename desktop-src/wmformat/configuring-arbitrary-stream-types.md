---
title: Konfigurieren beliebiger Streamtypen
description: Konfigurieren beliebiger Streamtypen
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- Streams,Konfigurieren beliebiger Streamtypen
- Codecs,Konfigurieren beliebiger Streamtypen
- streams,GenProfile
- codecs,GenProfile
- GenProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260219e408872dc21ecf82bd64b59b6c12b014c6e073a687a1b55957b290b76f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548049"
---
# <a name="configuring-arbitrary-stream-types"></a>Konfigurieren beliebiger Streamtypen

Die meisten beliebigen Streamtypen benötigen lediglich eine Bitrate, ein Pufferfenster und einen geeigneten Hauptmedientyp in der [**WM \_ MEDIA \_ TYPE-Struktur.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Einige beliebige Typen erfordern jedoch eine zusätzliche Konfiguration.

Wenn Sie Probleme beim Konfigurieren eines Streams haben, lesen Sie die Beispielanwendung GenProfile, die in diesem SDK enthalten ist. Die in GenProfile definierte Bibliothek enthält Code für das Ein- und Ein-/Aus- aller Typen von Streams. Weitere Informationen zu GenProfile und den anderen Beispielen finden Sie unter [Beispielanwendungen](sample-applications.md).

In den folgenden Abschnitten wird beschrieben, wie beliebige Streamtypen konfiguriert werden.



| `Section`                                                                                                                                        | BESCHREIBUNG                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Konfigurieren von Streams](configuring-script-streams.md)                                                                                   | Beschreibt, wie Skriptstreams konfiguriert werden.                                                  |
| [Konfigurieren von Dateiübertragungs-Streams](configuring-file-transfer-streams.md)                                                                     | Beschreibt, wie Dateiübertragungsstreams konfiguriert werden.                                           |
| [Konfigurieren von Streams](configuring-web-streams.md)                                                                                         | Beschreibt, wie Webstreams konfiguriert werden.                                                     |
| [Konfigurieren von Text Streams](configuring-text-streams.md)                                                                                       | Beschreibt, wie Textstreams konfiguriert werden.                                                    |
| [Konfigurieren benutzerdefinierter Streams](configuring-custom-arbitrary-streams.md)                                                               | Beschreibt, wie Streams für benutzerdefinierte beliebige Streamtypen konfiguriert werden.                       |
| [Berechnen von Bitrate- und Pufferfensterwerten für beliebige Streams](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | Beschreibt, wie die Bitrate und die Pufferfenstereinstellungen für einen beliebigen Stream berechnet werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beliebige Streams**](arbitrary-streams.md)
</dt> <dt>

[**Konfigurieren Streams**](configuring-streams.md)
</dt> </dl>

 

 




