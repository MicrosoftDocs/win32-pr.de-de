---
title: Farbkonvertierung und Farbübereinstimmung
description: Der Prozess der Konvertierung von Farben von einem Farb Raum in einen anderen wird als Farbkonvertierung bezeichnet.
ms.assetid: 52f68779-d4d6-4f1e-88a4-f872e9e90054
keywords:
- Windows Color System (WCS), Farbkonvertierung
- WCS (Windows Color System), Farbkonvertierung
- Bild Farbverwaltung, Farbkonvertierung
- Farbverwaltung, Farbkonvertierung
- Farben, Farbkonvertierung
- Farbkonvertierung
- Windows Color System (WCS), Farbabgleich
- WCS (Windows Color System), Farbabgleich
- Bild Farbverwaltung, Farbabgleich
- Farbverwaltung, Farb Übereinstimmung
- Farben, Farb Übereinstimmung
- Farb Übereinstimmung
- Windows Color System (WCS), Farbzuordnung
- WCS (Windows Color System), Farbzuordnung
- Bild Farbverwaltung, Farbzuordnung
- Farbverwaltung, Farbzuordnung
- Farben, Farbzuordnung
- Farbzuordnung
- weißer Punkt
- Colorants
- Gammakorrektur
- Farbskala
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74de95238472f58d49c5033a601c6d5458773c8
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "106355086"
---
# <a name="color-conversion-and-color-matching"></a>Farbkonvertierung und Farbübereinstimmung

Der Prozess der Konvertierung von Farben von einem [Farb Raum](c.md) in einen anderen wird als *Farbkonvertierung* bezeichnet. Alle Farben in einem Farbraum werden relativ zum [weißen Punkt](w.md)des Farb Raums korrigiert. Da der weiße Punkt eines Farbraum von Gerät zu Gerät abweicht, muss eine konvertierte Farbe dann mit der visuellen Farbe im Ziel Farbraum übereinstimmen. Dieser Vorgang wird als *Farbzuordnung* bezeichnet.

Wenn Sie z. b. über ein digitales Image verfügen, das Sie in der Anzeige erstellt haben, befindet es sich möglicherweise in einem geräteabhängigen RGB-Farbraum. Wenn Sie die Datei auf einem Drucker drucken möchten, muss Sie in den Farbraum der Drucker konvertiert werden. Da der Drucker wahrscheinlich einen geräteabhängigen CMYK-Farbraum verwendet, müssen alle RGB-Werte in CYMK konvertiert werden. Dies ist eine [Farbkonvertierung](c.md). Nachdem die Werte im Hinblick auf den CYMK-Bereich angegeben wurden, müssen Sie mit der nächstgelegenen Farbe übereinstimmen, die der Drucker liefern kann. Dies wird als Farbzuordnung oder [Farb](c.md)Vergleich bezeichnet.

Sowohl bei der Farbkonvertierung als auch bei der Farbzuordnung müssen verschiedene gerätespezifische Faktoren berücksichtigt werden. Beispielsweise sind die Bausteine von Bildschirmbildern Pixel. Jedes Pixel verfügt über eine festgelegte Anzahl von Bits zum Speichern des Farb-oder Farb Index Werts. Die Anzahl der Bits pro Pixel ist abhängig vom Typ der verwendeten Anzeige und dem angezeigten Anzeige Adapter und vom Modus, in dem der Adapter festgelegt ist. Die meisten Druckertypen verwenden verschiedene [Colorants](c.md) und Drucke bei bestimmten Auflösungen.

Außerdem unterscheiden sich die physischen farbiges Merkmale eines Geräts häufig auf verschiedenen Geräten. Wenn beispielsweise Farben von Computermonitoren erstellt werden, können Sie anders erscheinen als bei der Erstellung auf einem Druck Press. Ein Korrekturfaktor, der als *Gammakorrektur* bezeichnet wird, wird häufig verwendet, um derartige Unterschiede auszugleichen.

Das Ergebnis dieser geräteabhängigen Faktoren besteht darin, dass jedes Farbgerät über einen bestimmten Satz von Farben verfügt, die es ergeben kann. Dieser Farbsatz wird *als seine Spiel* Farbe bezeichnet. Zum Durchführen der Farbkonvertierung und der Farbzuordnung müssen die Farben in einem Bild aus dem Farbraum und dem Bereich des Quell Geräts in den Farbraum des Zielgeräts konvertiert werden. Sie werden dann mit dem Spiel des Zielgeräts abgeglichen.

 

 




