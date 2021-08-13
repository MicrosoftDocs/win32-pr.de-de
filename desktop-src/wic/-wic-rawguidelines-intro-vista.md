---
description: RAW-Bildformate in Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: RAW-Bildformate in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88026e85780706ca2bd5f23f5ca43ec49ae614d4c65e42ec19367b01b3f43423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709858"
---
# <a name="raw-image-formats-in-windows-vista"></a>RAW-Bildformate in Windows Vista

Windows Vista Explorer , Windows Vista Fotogalerie, Window Live Fotogalerie und die Windows 7 Bildanzeige alle Windows Imaging Component (WIC) verwenden und unterstützen daher RAW-Bildformate, wenn geeignete Codecs auf dem Computer installiert sind.

Da es sich bei WIC um eine erweiterbare Imagearchitektur handelt, kann jede WIC-Anwendung neue Bildformate nutzen, sobald neue Codecs auf dem System installiert sind. Dadurch eignet sich WIC ideal als Plug & Play Lösung für die RAW-Bildformate, die Digitalkameras erzeugen. Über WIC können Windows Anwendungen Unterstützung für neue Kameramodelle erhalten, wenn aktualisierte Codecs verfügbar gemacht werden (idealerweise im Lieferumfang mit neuen Kameras). Codecautoren können diese Szenarien unterstützen, indem sie WIC-Schnittstellen implementieren, die allen Bildtypen gemeinsam sind, wie in diesem Dokument ausführlicher beschrieben.

Heutzutage haben die meisten gängigen Consumeranwendungen keine besonderen Kenntnisse über RAW-Bildformate und stellen keine Benutzeroberfläche zum Anpassen von RAW-Verarbeitungseinstellungen zur Verfügung.

Zur Unterstützung spezialisierter Bildverarbeitungsanwendungen müssen RAW-Codecautoren jedoch auch die [**IWICDevelopRaw-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) implementieren. Diese Schnittstelle macht spezielle Features für RAW-Bilder verfügbar, z. B. die Möglichkeit, allgemeine Bildanpassungen vorzunehmen und RAW-Bilder in angegebenen RGB-Farbräumen (Rot-Grün-Blau) zu verarbeiten (entwickeln).

Einige andere WIC-Schnittstellen sind wichtig, damit RAW-Codecautoren implementieren können. Diese werden in dieser Reihe von Themen ausführlicher erläutert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC Guidelines for Camera RAW Image Formats](-wic-rawguidelines.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



