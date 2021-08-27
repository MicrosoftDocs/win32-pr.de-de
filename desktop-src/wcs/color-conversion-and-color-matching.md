---
title: Farbkonvertierung und Farbübereinstimmung
description: Der Prozess der Konvertierung von Farben von einem Farbraum in einen anderen wird als Farbkonvertierung bezeichnet.
ms.assetid: 52f68779-d4d6-4f1e-88a4-f872e9e90054
keywords:
- Windows Farbsystem (WCS), Farbkonvertierung
- WCS (Windows Color System), Farbkonvertierung
- Bildfarbverwaltung, Farbkonvertierung
- Farbverwaltung, Farbkonvertierung
- Farben,Farbkonvertierung
- Farbkonvertierung
- Windows Farbsystem (WCS), Farbabgleich
- WCS (Windows Color System), Farbabgleich
- Bildfarbverwaltung, Farbabgleich
- Farbverwaltung, Farbabgleich
- Farben,Farbabgleich
- Farbabgleich
- Windows Farbsystem (WCS), Farbzuordnung
- WCS (Windows Color System), Farbzuordnung
- Bildfarbverwaltung, Farbzuordnung
- Farbverwaltung, Farbzuordnung
- Farben,Farbzuordnung
- Farbzuordnung
- White Point
- Farbstoffe
- Gammakorrektur
- Gamut
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0071e15c2d572c134d61aee7a018b41c8d09507e87963eeeed1488909cdafeba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110800"
---
# <a name="color-conversion-and-color-matching"></a>Farbkonvertierung und Farbübereinstimmung

Der Prozess der Konvertierung von Farben von einem [Farbraum in](c.md) einen anderen wird als *Farbkonvertierung bezeichnet.* Alle Farben in einem Farbraum sind relativ zum Weißpunkt des [Farbraums festgelegt.](w.md) Da der Weißpunkt eines Farbraums von Gerät zu Gerät variiert, muss eine konvertierte Farbe dann mit ihrer visuell nächstgelegenen Farbe im Zielfarbraum übereinstimmen. Dieser Prozess wird als *Farbzuordnung bezeichnet.*

Wenn Sie beispielsweise über ein digitales Bild verfügen, das Sie auf Ihrer Anzeige erstellt haben, kann es sich in einem geräteabhängigen RGB-Farbraum finden. Wenn Sie sie auf einem Drucker drucken möchten, muss sie in den Farbraum des Druckers konvertiert werden. Da der Drucker wahrscheinlich einen geräteabhängigen CTERI-Farbraum verwendet, müssen alle RGB-Werte in CYMK konvertiert werden. Dies ist [die Farbkonvertierung.](c.md) Nachdem die Werte im Hinblick auf den CYMK-Raum angegeben wurden, müssen sie der farbe, die der Drucker am nächsten bringen kann, übereinstimmen. Dies wird als Farbzuordnung oder [Farbvergleich bezeichnet.](c.md)

Sowohl die Farbkonvertierung als auch die Farbzuordnung müssen eine Reihe gerätespezifischer Faktoren berücksichtigen. Die Bausteine von Bildschirmbildern sind beispielsweise Pixel. Jedes Pixel verfügt über eine bestimmte Anzahl von Bits, um seinen Farb- oder Farbindexwert zu speichern. Die Anzahl der Bits pro Pixel hängt vom Verwendeten Anzeige- und Anzeigeadaptertyp sowie vom Modus ab, auf den der Adapter festgelegt ist. Die meisten Druckertypen verwenden [unterschiedliche Farbmittel](c.md) und Drucke mit bestimmten Auflösungen.

Darüber hinaus unterscheiden sich die physischen Tonmerkmale eines Geräts häufig auf verschiedenen Geräten. Wenn beispielsweise Farben von Computermonitoren erzeugt werden, können sie anders erscheinen als bei einer Druckmaschine. Ein Korrekturfaktor, der als *Gammakorrektur* bezeichnet wird, wird häufig verwendet, um solche Unterschiede zu kompensieren.

Das Ergebnis dieser geräteabhängigen Faktoren ist, dass jedes Farbgerät über einen bestimmten Satz von Farben verfügt, die es erzeugen kann. Dieser Farbsatz wird als *gamut bezeichnet.* Zum Durchführen der Farbkonvertierung und Farbzuordnung müssen die Farben in einem Bild aus dem Farbraum und der Gamut des Quellgeräts in den Farbraum des Zielgeräts konvertiert werden. Sie werden dann mit dem Gamut des Zielgeräts übereinstimmen.

 

 




