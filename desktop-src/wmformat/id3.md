---
title: ID3-Unterstützung
description: ID3 ist eine Organisation, die eine Reihe von Standards für die Einbeziehung von Metadaten in MPEG Layer-3-Audiodateien (MP3) definiert hat.
ms.assetid: 8c1f1114-48d8-4dce-b7ab-0293265a875c
keywords:
- Windows Medienformat-SDK, ID3-Unterstützung
- Advanced Systems Format (ASF), ID3-Unterstützung
- ASF (Advanced Systems Format), ID3-Unterstützung
- Metadata,ID3
- ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c92fb9282483b6fd01b1149220e5f30421c3c1285bd533d64afef91709314e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702981"
---
# <a name="id3-support"></a>ID3-Unterstützung

ID3 ist eine Organisation, die eine Reihe von Standards für die Einbeziehung von Metadaten in MPEG Layer-3-Audiodateien (MP3) definiert hat. Die Objekte des Windows Media Format SDK bieten Unterstützung für ID3-kompatible Attribute. Drei verschiedene ID3-Versionen werden unterstützt: ID3v1.x, ID3v2.2 und ID3v2.3/v2,4. Eine Liste der Attribute, die ID3-Frames gleichsetzen, finden Sie unter [ID3 Tag Support](id3-tag-support.md).

Sofern nicht anders angegeben, wird von den Objekten dieses SDK keine Überprüfung der ID3-Framedaten durchgeführt. Beispielsweise speichert das Metadatenattribut [**\_ WM/Synchronised**](wm-lyrics-synchronised.md) die Musiktitel mit entsprechenden Zeitstempeln. Beim Schreiben eines **WM/Wms \_ Synchronised-Attributs** überprüfen die Objekte dieses SDK nicht, ob die Zeitstempel in chronologischer Reihenfolge sind, oder führen eine Validierung jeglicher Art durch.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Attribute**](attributes.md)
</dt> <dt>

[**Metadatenfeatures**](metadata-features.md)
</dt> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




