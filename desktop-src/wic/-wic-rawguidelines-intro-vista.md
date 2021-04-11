---
description: Rohbild Formate in Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Rohbild Formate in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c48b4e3ab5b0d373dbc0313267e58177b189538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217373"
---
# <a name="raw-image-formats-in-windows-vista"></a>Rohbild Formate in Windows Vista

Windows Vista Explorer, Windows Vista Photo Gallery, Window Live Photo Gallery und Windows 7 Photo Viewer verwenden Windows Imaging Component (WIC) und unterstützen daher Rohbild Formate, wenn geeignete Codecs auf dem Computer installiert sind.

Da WIC eine erweiterbare Imaging-Architektur ist, kann jede WIC-Anwendung neue Bildformate nutzen, sobald neue Codecs auf dem System installiert sind. Dadurch ist WIC ideal als Plug & Play Lösung für die Rohbild Formate, die Digitalkameras erzeugt. Mithilfe von WIC können Windows-Anwendungen immer Unterstützung für neue Kameramodelle erhalten, wenn aktualisierte Codecs verfügbar gemacht werden (im Idealfall mit neuen Kameras). Die Codec-Autoren können diese Szenarios unterstützen, indem Sie WIC-Schnittstellen implementieren, die allen Image Typen gemeinsam sind, wie in diesem Dokument ausführlicher beschrieben.

Heutzutage haben die meisten gängigen Consumeranwendungen keine besonderen Kenntnisse von Rohbild Formaten und machen keine Benutzeroberfläche für die Anpassung der rohverarbeitungs Einstellungen verfügbar.

Zur Unterstützung spezieller Abbild Erstellungs Anwendungen müssen auch unformatierte Codec-Autoren die [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Schnittstelle implementieren. Diese Schnittstelle stellt besondere Features für unformatierte Images zur Verfügung, z. b. die Möglichkeit, gängige Bild Anpassungen vorzunehmen und unformatierte Bilder in angegebene Farben in rot-grün-blau (RGB) zu verarbeiten.

Einige andere WIC-Schnittstellen sind wichtig für unformatierte Codec-Autoren zur Implementierung von. Diese werden in dieser Reihe von Themen ausführlicher erläutert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC-Richtlinien für Kamera Rohbild Formate](-wic-rawguidelines.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



