---
title: Geräteabhängige Farbräume
description: Die meisten Farbräume sind geräteabhängig.
ms.assetid: 657ec64b-8605-4d05-a7d6-9f8bb71e6a71
keywords:
- Windows Farbsystem (WCS), geräteabhängige Farbräume
- WCS (Windows Color System), geräteabhängige Farbräume
- Bildfarbverwaltung, geräteabhängige Farbräume
- Farbverwaltung, geräteabhängige Farbräume
- Farben,geräteabhängige Farbräume
- Farbräume, geräteabhängig
- Geräteabhängige Farbräume
- White Point
- Farbstoffe
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe10ad9d48e750f9869b113a45f1235d2aa692532702ea4443ec3629d32276ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593620"
---
# <a name="device-dependent-color-spaces"></a>Geräteabhängige Farbräume

Die [meisten Farbräume](c.md) sind geräteabhängig. Auch wenn ein bestimmtes Gerät, z. B. ein Drucker, den C STANDARDWERT-Farbraum verwenden kann, unterscheiden sich die Farben, die es für bestimmte CKOMBINATION-Werte rendert, häufig geringfügig von allen anderen Druckertypen. Genau aus diesem Grund ist das WCS 1.0-Farbverwaltungssystem so nützlich.

Alle Farbräume verfügen über *einen weißen Punkt,* der als weißstes Weiß definiert ist, das in diesem Farbraum erzeugt werden kann. Da sich Geräte voneinander unterscheiden können, können sich auch ihre Weißpunkte unterscheiden. Alle Farben, die ein Gerät erzeugen kann, sind relativ zu seinem Weißpunkt. Daher muss ein Farbverwaltungssystem in der Lage sein, den Weißpunkt eines Farbraums einem anderen zu zuordnen und die relativen Positionen aller Farben zu erhalten. Es muss auch in der Lage sein, eine Farbe in einem Farbraum der nächstgelegenen Übereinstimmung in einem anderen Farbraum zu zuordnen, unabhängig von den Unterschieden in den weißen Punkten. WCS 1.0 kann diese beiden Aufgaben ausführen.

Der RGB-Farbraum wird häufig auf Computermonitoren verwendet. Daher ist es geräteabhängig. Drucker verwenden in der Regel [CANTI-Farbmittel.](c.md) Jeder Drucker implementiert eine eigene Version des CKOMBINATION-Farbraums. Digitale Bilder speichern möglicherweise keine Farben in ihnen. Sie können Indexnummern in einer Palette von Farben speichern. Das Ergebnis ist, dass es für einzelne Anwendungsentwickler sehr schwierig ist, eine standardisierte Methode zum Verschieben von Farbbildern von einem Gerät auf ein anderes zu verwenden oder zur Verfügung zu stellen. Bildverarbeitungsexperten sind häufig frustriert, wenn sie ein Grafikbild auf einem Computerbildschirm erstellen und es beim Drucken sehr unterschiedlich sehen. WCS 1.0 erfüllt diese Anforderungen an die Bildverarbeitung.

 

 




