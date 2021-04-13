---
title: Schreiben von komprimierten Beispielen
description: Schreiben von komprimierten Beispielen
ms.assetid: f85ca719-1b9d-404f-b2b1-c9e3524e4bc6
keywords:
- Advanced Systems Format (ASF), Schreiben von komprimierten Beispielen
- ASF (Advanced Systems Format), Schreiben von komprimierten Beispielen
- Advanced Systems Format (ASF), übergeben von komprimierten Beispielen
- ASF (Advanced Systems Format), übergeben von komprimierten Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c43fed30aa89e83c157479257e78fbab4acd98
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104472252"
---
# <a name="writing-compressed-samples"></a>Schreiben von komprimierten Beispielen

Für einige Audiodaten und Videostreams empfiehlt es sich, bereits komprimierte Beispiele zu übergeben, anstatt Rohdaten zu übergeben. Diese Funktion wird verwendet, um einen vorhandenen Stream zu kopieren oder um mit einem Drittanbieter-Codec komprimierte Beispiele zu schreiben. Der Prozess zum Schreiben eines komprimierten Beispiels ist mit dem Schreiben eines unkomprimierten Beispiels identisch, mit dem Unterschied, dass Sie anstelle von [**iwmwriter:: writesample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)den Wert [**iwmwriteradvanced:: writestreamsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) verwenden. Weitere Informationen zum Schreiben von nicht komprimierten Beispielen finden [Sie unter so schreiben Sie Beispiele](to-write-samples.md).

Wenn Sie komprimierte Beispiele für CBR-profile schreiben, löscht der Writer ggf. einige Beispiele, damit der Inhalt innerhalb der angegebenen Bitrate und Puffer Fenster Werte aufbewahrt wird. Für VBR werden von dem Writer keine Stichproben gelöscht, aber es gibt keine Möglichkeit, sicherzustellen, dass die Werte für Bitrate und Puffer Fenster korrekt sind.

Wenn Sie einen Stream aus einer Datei in eine andere kopieren, sollten Sie das Datenstrom-Konfigurationsobjekt immer aus dem Profil der ursprünglichen Datei in das Profil der neuen Datei kopieren. Dadurch wird sichergestellt, dass Sie über die richtigen Bitrate-und Puffer Fenster Informationen verfügen. Wenn Sie einen komprimierten Stream in einen Stream kopieren, für den ein niedrigeres Puffer Fenster festgelegt ist, werden beim Schreiben von Dateien Stichproben gelöscht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




