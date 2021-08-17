---
title: Kopieren von Streams mit dekomprimierten Beispielen
description: Kopieren von Streams mit dekomprimierten Beispielen
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- Windows Medienformat-SDK, Kopieren von Datenströmen
- Advanced Systems Format (ASF), Kopieren von Datenströmen
- ASF (Advanced Systems Format), Kopieren von Datenströmen
- Streams,Kopieren mit dekomprimierten Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e044d2a1d456c14c2e2d069e0a117ab6f6de218c062771da9c24bf887ddfdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848806"
---
# <a name="copying-streams-using-decompressed-samples"></a>Kopieren von Streams mit dekomprimierten Beispielen

Es wird dringend empfohlen, Streams nicht mit dekomprimierten Beispielen aus einer Datei in eine andere zu kopieren. Der Prozess des Dekomprimierens und Erneutkomprimierens von Stichproben beeinträchtigt die Qualität der Ausgabe. Wenn Sie Ihre Beispiele dekomprimieren und dann in einen anderen Stream kopieren müssen, können probleme mit qualitätsbasierten VBR-codierten Datenströmen (Variable Bit Rate, variable Bitrate) auftreten.

Wenn der Codec die Komprimierung eines qualitätsbasierten VBR-Streams abgeschlossen hat, zeichnet er die Bitrate und das Pufferfenster des resultierenden Inhalts auf. Wenn Sie eine Datei lesen, die einen mit qualitätsbasierten VBR codierten Stream enthält, notiert das vom Reader erhaltene Profil die Bitrate und das Pufferfenster sowie die maximale Bitrate und das maximale Pufferfenster. Diese Konfiguration im Profil gibt normalerweise einen Stream mit eingeschränkter Bitrate für variable Bitrate an. Wenn Sie das Profil für den Writer festlegen, wird daher ein Vorverarbeitungslauf für den Stream erwartet, da vbr-Streams mit eingeschränkter Bitrate eine Zwei-Durchlauf-Codierung erfordern. Sie sollten den Stream so behandeln, als wäre er ein vbr-Stream mit eingeschränkter Bitrate und liefert die Beispiele für die Vorverarbeitung. Da Sie die Werte verwenden, die nach dem Codieren des Inhalts auf einer bestimmten Qualitätsebene zurückgegeben werden, stellen diese Werte die gewünschte Qualitätsstufe dar. Die Qualität der neu codierten Ausgabe wird durch die neu codierte Codierung natürlich trotzdem etwas beeinträchtigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Kopieren von Daten aus einer Datei in eine andere**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Kopieren von Streams ohne Dekomprimieren der Daten**](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 




