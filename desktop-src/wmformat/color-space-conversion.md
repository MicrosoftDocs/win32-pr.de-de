---
title: Farb Raum Konvertierung
description: Farb Raum Konvertierung
ms.assetid: f5f1ec99-b3b9-4420-bf64-3872d9bbe650
keywords:
- Windows Media-Format-SDK, Farb Raum Konvertierung
- Advanced Systems Format (ASF), Farb Raum Konvertierung
- ASF (Advanced Systems Format), Farb Raum Konvertierung
- Farb Raum Konvertierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc284995cbc72aee148e12977dad9f4476b29c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206749"
---
# <a name="color-space-conversion"></a>Farb Raum Konvertierung

Häufig gibt es einen Unterschied zwischen der Farbtiefe des komprimierten Video Formats im Profil und dem Eingabeformat. In diesem Fall muss das Quellvideo konvertiert werden, damit es dem Farbraum des Ziels entspricht. Der Writer verarbeitet diesen Prozess und kommuniziert mit einem internen Farb Raum Konverter.

Der Reader kommuniziert auch mit dem Farb Raum Konverter, um den Unterschied zwischen dem komprimierten Format und dem Ausgabeformat abzugleichen.

Wie bei allen Transformationen, die für Daten ausgeführt werden, kann durch die Umwandlung zwischen Farbtiefen die Qualität der Ausgabe verringert werden. Wenn möglich, sollten Sie Eingabe-und Ausgabeformate mit der gleichen Farbtiefe wie das komprimierte Format verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen zum Schreiben von Dateien**](file-writing-features.md)
</dt> <dt>

[**Arbeiten mit Eingaben**](working-with-inputs.md)
</dt> <dt>

[**Arbeiten mit Ausgaben**](working-with-outputs.md)
</dt> </dl>

 

 




