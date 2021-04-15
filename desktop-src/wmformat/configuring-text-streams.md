---
title: Konfigurieren von Textstreams
description: Konfigurieren von Textstreams
ms.assetid: d99baac5-69e5-4e0a-9cd6-35b288d8181a
keywords:
- Streams, Konfigurieren von Textstreams
- Codecs, Konfigurieren von Textstreams
- Textstreams, konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460369eaae02f636f8ddda8bcca4f29ecfc2e1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471301"
---
# <a name="configuring-text-streams"></a>Konfigurieren von Textstreams

Textstreams entsprechen im Wesentlichen den benutzerdefinierten beliebigen Datenströmen. Einem Textstream sind keine Konfigurationsinformationen zugeordnet, um den Typ der Text Codierung zu identifizieren, sodass das Writer-Objekt keine Beispiele überprüfen kann.

Um einen Textstream zu konfigurieren, müssen Sie sicherstellen, dass die [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur einen wichtigen Medientyp von wmmediatype \_ Text enthält. Außerdem müssen Sie für den Stream eine Bitrate und ein Puffer Fenster festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Berechnen von Bitraten-und Puffer Fenster Werten für beliebige Streams**](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md)
</dt> <dt>

[**Allgemeine Konfiguration für alle Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren beliebiger Streamtypen**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Textstreams**](text-streams.md)
</dt> </dl>

 

 




