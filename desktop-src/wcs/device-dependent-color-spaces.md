---
title: Geräteabhängige Farbräume
description: Die meisten Farbbereiche sind Geräte abhängig.
ms.assetid: 657ec64b-8605-4d05-a7d6-9f8bb71e6a71
keywords:
- Windows Color System (WCS), Geräte abhängige Farbbereiche
- WCS (Windows Color System), Geräte abhängige Farbbereiche
- Bild Farbverwaltung, Geräte abhängige Farbbereiche
- Farbverwaltung, Geräte abhängige Farbbereiche
- Farben, Geräte abhängige Farbbereiche
- Farbbereiche, Geräte abhängig
- Geräte abhängige Farbbereiche
- weißer Punkt
- Colorants
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1523ee6ba81dcdc3b69a468546871cfd21913
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "106366346"
---
# <a name="device-dependent-color-spaces"></a>Geräteabhängige Farbräume

Die meisten [Farbbereiche](c.md) sind Geräte abhängig. Obwohl ein bestimmtes Gerät (z. b. ein Drucker) den CMYK-Farbraum verwenden kann, sind die Farben, die für bestimmte CMYK-Werte gerendert werden, oft etwas anders als alle anderen Druckertypen. Der Grund hierfür ist, dass das WCS 1,0 Color Management System so nützlich ist.

Alle Farbbereiche verfügen über einen *weißen Punkt*, der als whitetestweiß definiert ist, das in diesem Farbraum erstellt werden kann. Da sich die Geräte voneinander unterscheiden können, können sich auch die zugehörigen weißen Punkte unterscheiden. Alle Farben, die von einem Gerät erzeugt werden können, sind relativ zum weißen Punkt. Daher muss ein Farb Verwaltungssystem in der Lage sein, den weißen Punkt eines Farbraum einer anderen Farbe zuzuordnen und die relativen Positionen aller Farben beizubehalten. Es muss auch in der Lage sein, eine Farbe in einem Farbraum der nächstgelegenen Entsprechung in einem anderen Farbraum zuzuordnen, unabhängig von den Unterschieden in den weißen Punkten. WCS 1,0 ist in der Lage, beide Aufgaben auszuführen.

Der RGB-Farbraum wird häufig für Computer Monitore verwendet. Daher ist es Geräte abhängig. Drucker verwenden normalerweise CMYK- [Colorants](c.md). Jeder Drucker implementiert seine eigene Version des CMYK-Farbraum. In digitalen Images werden die darin gespeicherten Farben möglicherweise nicht gespeichert. Sie können Indexnummern in einer Palette von Farben speichern. Das Ergebnis ist, dass es für einzelne Anwendungsentwickler sehr schwierig ist, eine standardisierte Methode zum Verschieben von Farbbildern von einem Gerät zu einem anderen zu verwenden oder bereitzustellen. Abbild Fachleute treten häufig die Frustration auf, wenn ein Grafik Bild auf einem Computerbildschirm erstellt wird und es beim Drucken sehr unterschiedlich ist. WCS 1,0 behandelt diese Abbild Erstellungs Anforderungen.

 

 




