---
title: Kopieren von Streams mithilfe von nicht komprimierten Beispielen
description: Kopieren von Streams mithilfe von nicht komprimierten Beispielen
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- Windows Media-Format-SDK, Kopieren von Streams
- Advanced Systems Format (ASF), Kopieren von Streams
- ASF (Advanced Systems Format), Kopieren von Streams
- Streams, Kopieren mithilfe von entkomprimierten Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c5c0f98b02090d98814983ad518ee3cd7e5d8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340238"
---
# <a name="copying-streams-using-decompressed-samples"></a>Kopieren von Streams mithilfe von nicht komprimierten Beispielen

Es wird dringend empfohlen, Datenströme nicht mithilfe von dekomprimierten Beispielen aus einer Datei in eine andere Datei zu kopieren. Durch das Dekomprimieren und Erneutes Komprimieren von Beispielen wird die Qualität der Ausgabe herabgestuft. Wenn Sie die Beispiele Dekomprimieren und Sie dann in einen anderen Stream kopieren müssen, kann es schwierig sein, mit Qualitäts basierten, VBR-codierten Streams (Variable Bitrate) zu tun.

Wenn der Codec das Komprimieren eines Qualitäts basierten VBR-Streams beendet, zeichnet er die Bitrate und das Puffer Fenster des resultierenden Inhalts auf. Wenn Sie eine Datei mit einem Stream lesen, der mit einer qualitativ hochwertigen VBR-Codierung codiert ist, werden von dem vom Reader erhaltenen Profil sowohl die Bitrate als auch das Puffer Fenster sowie die maximale Bitrate und das maximale Puffer Fenster festgeschrieben. Diese Konfiguration im Profil weist normalerweise einen Bitraten-Stream mit eingeschränkter Bitrate auf. Wenn Sie das Profil für den Writer festlegen, wird daher ein Vorverarbeitungs Durchlauf für den Datenstrom erwartet, da VBR-Streams mit Bitrate-Einschränkung eine zwei-Pass-Codierung erfordern. Der Stream sollte so behandelt werden, als ob es sich um einen eingeschränkten VBR-Stream mit Bitraten handelt, und die Beispiele für die Vorverarbeitung bereitstellen. Da Sie die Werte verwenden, die nach dem Codieren des Inhalts auf einer bestimmten Qualitätsstufe zurückgegeben werden, stellen diese Werte die gewünschte Qualitätsstufe dar. Natürlich wird die Qualität der neu codierten Ausgabe nach wie vor durch die erneute Codierung etwas beeinträchtigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Kopieren von Daten aus einer Datei in eine andere**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Kopieren von Streams, ohne die Daten zu entkomprimieren**](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 




