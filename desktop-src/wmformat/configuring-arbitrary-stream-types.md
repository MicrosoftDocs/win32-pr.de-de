---
title: Konfigurieren beliebiger Streamtypen
description: Konfigurieren beliebiger Streamtypen
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- Streams, konfigurieren beliebiger Streamtypen
- Codecs, konfigurieren beliebiger Streamtypen
- Streams, genprofile
- Codecs, genprofile
- Genprofile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e04751bd33da6599fd7ff3766c4dc8350889c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340621"
---
# <a name="configuring-arbitrary-stream-types"></a>Konfigurieren beliebiger Streamtypen

Die meisten willkürlichen Streamtypen benötigen nur eine Bitrate, ein Puffer Fenster und einen richtigen großen Medientyp in der [**WM \_ - \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur. Für einige beliebige Typen ist jedoch eine zusätzliche Konfiguration erforderlich.

Wenn Sie Probleme beim Konfigurieren eines Streams haben, finden Sie weitere Informationen in der Beispielanwendung genprofile, die in diesem SDK enthalten ist. Die in genprofile definierte Bibliothek enthält Code zum Einschließen aller Arten von Streams. Weitere Informationen zu genprofile und den anderen Beispielen finden Sie unter [Beispielanwendungen](sample-applications.md).

In den folgenden Abschnitten wird beschrieben, wie beliebige Streamtypen konfiguriert werden.



| `Section`                                                                                                                                        | BESCHREIBUNG                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Konfigurieren von Skript Datenströmen](configuring-script-streams.md)                                                                                   | Beschreibt das Konfigurieren von Skript Datenströmen.                                                  |
| [Konfigurieren von Datei Übertragungsdaten strömen](configuring-file-transfer-streams.md)                                                                     | Beschreibt, wie Datei Übertragungsdaten Ströme konfiguriert werden.                                           |
| [Konfigurieren von Webstreams](configuring-web-streams.md)                                                                                         | Beschreibt, wie Webstreams konfiguriert werden.                                                     |
| [Konfigurieren von Textstreams](configuring-text-streams.md)                                                                                       | Beschreibt das Konfigurieren von Textstreams.                                                    |
| [Konfigurieren von benutzerdefinierten beliebigen Streams](configuring-custom-arbitrary-streams.md)                                                               | Beschreibt, wie Streams für benutzerdefinierte beliebige Streamtypen konfiguriert werden.                       |
| [Berechnen von Bitraten-und Puffer Fenster Werten für beliebige Streams](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | Beschreibt, wie die Bitraten-und Puffer Fenster Einstellungen für einen beliebigen Datenstrom berechnet werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beliebige Streams**](arbitrary-streams.md)
</dt> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> </dl>

 

 




