---
description: Codec-Verfügbarkeit und Platt Form Unterstützung
ms.assetid: 6b3d09c9-e91f-4c62-92f7-c2643e51987f
title: Codec-Verfügbarkeit und Platt Form Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc485c5f8db9ff7883263cd614578705eccd3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217375"
---
# <a name="codec-availability-and-platform-support"></a>Codec-Verfügbarkeit und Platt Form Unterstützung

Microsoft empfiehlt, dass Kamerahersteller aktualisierte Rohdaten von Windows Imaging Component (WIC) in der Software Verteilung mit neuen Kameras einschließen und dass der aktualisierte Codec mit der Standardinstallation der Hersteller Software Windows 7, Windows Vista und Windows XP installiert wird. Kamerahersteller sollten auch den neuesten WIC-Codec als Download von den Support Websites bereitstellen.

## <a name="codec-discovery"></a>Codec-Ermittlung

Microsoft geht wie folgt vor, um den Benutzern zu helfen, für Codec-Downloads auf die Websites der Anbieter zuzugreifen:

-   Wenn ein Benutzer in Windows-Explorer auf eine nicht erkannte Datei doppelklickt (der Standardfall, wenn sich eine Rohdatendatei auf dem Computer befindet, aber der Codec noch nicht installiert ist), wird in einem Dialogfeld gemeldet, dass die Datei nicht erkannt wird, und es wird gefragt, ob der Benutzer ein Programm suchen möchte, das die Datei versteht. Microsoft verwaltet einen vorhandenen Umleitungs Dienst, um Benutzer an die Websites des Anbieters weiterzuleiten, die das Programm bereitstellen können, um die Datei zu verstehen. Diese Funktion ist in Windows XP und Windows Vista vorhanden.
-   Die Windows-Fotogalerie, die Windows Live-Fotogalerie und der Windows 7 Photo Viewer erkennen einen Satz von Dateierweiterungen als Rohdatendateien. Wenn Dateien aus diesem Satz in Ordnern gefunden werden, die von einer dieser Anwendungen untersucht werden, und ein Codec für die Datei noch nicht installiert ist, wird ein Dialogfeld angezeigt, wie im vorherigen Abschnitt beschrieben.

Weitere Informationen zur Codec-Ermittlung finden Sie unter Support für Codec-Verfügbarkeit und-Plattform.

## <a name="windows-xp-platform-support"></a>Windows XP-Platt Form Unterstützung

Microsoft hat Windows XP SP3 mit WIC und einen eigenständigen WIC-Installer für Windows XP SP2 veröffentlicht. Diese verwenden WIC-Codecs, um die Unterstützung für Miniaturansichten und Vorschau auf diesen Plattformen zu ermöglichen. Daher ist es wichtig, dass Codec-Downloads und-Installationen unter Windows 7, Windows Vista und Windows XP unterstützt und getestet werden.

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

 

 



