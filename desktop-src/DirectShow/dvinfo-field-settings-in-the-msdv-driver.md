---
description: Dvinfo-Feld Einstellungen im msdv-Treiber
ms.assetid: f0723da5-4f53-4f83-a657-ae42815a784e
title: Dvinfo-Feld Einstellungen im msdv-Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4205a680833b0e2f8c6be2dc4cb65faa60515867
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746665"
---
# <a name="dvinfo-field-settings-in-the-msdv-driver"></a>Dvinfo-Feld Einstellungen im msdv-Treiber

In diesem Abschnitt wird beschrieben, wie der msdv-Treiber die [**dvinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) -Struktur füllt.

Die `DVINFO` -Struktur definiert den Format Block für PIN-Verbindungen zwischen msdv und anderen Filtern. Standardmäßig wird der DV-Splitter Filter bei der Erfassung von einem DV-Gerät verwendet, und der DV-MUX-Filter wird bei der Übertragung an das Gerät verwendet. Allerdings können Anwendungen ihre eigenen benutzerdefinierten Filter bereitstellen, daher ist es hilfreich zu verstehen, wie msdv den `DVINFO` Format Block auffüllt.

Die- `DVINFO` Struktur enthält die folgenden Informationen:

-   Zwei audiohilfsquelle (Aaux)-Quellpakete für den ersten und zweiten Audioblock.
-   Zwei Aaux-Quell Code Verwaltungs Pakete für den ersten und zweiten Audioblock.
-   Ein Video-Hilfsquelle (Vaux).
-   Ein Vaux-Quell Code Verwaltungspaket.

Jeder Frame in einem DV-Stream enthält Aaux-und Vaux-Pakete. Der `DVINFO` Format Block ist jedoch statisch und wird nur zum Einrichten der Pin-Verbindung verwendet. Wenn der msdv-Treiber eine Verbindung herstellt, prüft er keines der Aaux-oder Vaux-Pakete im Stream. Stattdessen wird ein Satz von Standardwerten basierend auf den folgenden Merkmalen des DV-Geräts verwendet:

-   Gibt an, ob das Gerät ein consumerformat (dvcr) oder ein Professional-Format (DVCPRO) unterstützt.
-   Der Signaltyp
-   Ob das Format ' NTSC ' oder ' PAL ' ist. (Wenn das Gerät diese Informationen nicht meldet, werden standardmäßig die NTSC-Einstellungen von msdv verwendet.)

Sobald das Streaming beginnt, liegt es in der Verantwortung der benutzermodusfilter, z. b. des DV-Splitters, den tatsächlichen Inhalt der einzelnen DV-Frames zu überprüfen. Da sich die Informationen von Frame zu Frame ändern können, muss der Filter möglicherweise eine dynamische Formatänderung durchführen. Wenn sich die Audiorate z. b. ändert, muss der Filter möglicherweise den Audiotyp erneut aushandeln.

Wenn Sie eine DV-Datei vom Typ "Type-1" erfassen, `DVINFO` wird die Struktur in die Datei als Datenstrom Format ("strauf") geschrieben. Diese Daten werden direkt aus dem von msdv bereitgestellten Format Block entnommen. Wie bereits erwähnt, kann sich der tatsächliche Inhalt des Streams unterscheiden. Es liegt in der Verantwortung der Anwendung, die Aaux-und Vaux-Pakete in jedem Frame zu untersuchen.

In den folgenden Themen finden Sie Tabellen, in denen alle von msdv verwendeten Felder aufgelistet sind.

-   [Aaux-Quelle (as)-Paket](aaux-source--as--pack.md)
-   [Aaux Source Control (ASC) Pack](aaux-source-control--asc--pack.md)
-   [Vaux-Quelle (VS)](vaux-source--vs--pack.md)
-   [Vaux-Quell Code Verwaltungspaket (VSC)](vaux-source-control--vsc--pack.md)

Beachten Sie beim Lesen dieser Tabellen die folgenden Spezifikationen:

-   IEC 61834
-   SMPTE 314m
-   SMPTE 370

In jeder Tabelle gibt die erste Spalte den Feldcode an, gefolgt von der Anzahl der Bits (in Klammern). Die restlichen Spalten gibt die Feldwerte an. Viele der Felder Aaux und Vaux sind für die PIN-Verbindung nicht relevant. in diesem Fall legt msdv einen Dummy-Wert fest. Der numerische Wert des gesamten Pakets wird unten in jeder Tabelle aufgeführt.

In den Hinweisen nach den einzelnen Tabellen finden Sie weitere Informationen über ausgewählte Felder. Ausführliche Beschreibungen finden Sie unter Spezifikationen. Außerdem haben einige Felder in SMPTE 314m/SMPTE 370 nicht dieselbe Bedeutung wie in IEC 61834.

> [!Note]  
> Derzeit werden von DirectShow keine DVCPRO-Formate unterstützt. Die für das DVCPRO-Formate aufgelisteten Werte werden für die zukünftige Verwendung definiert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[DV-Daten im AVI-Datei Format](dv-data-in-the-avi-file-format.md)
</dt> <dt>

[Msdv-Treiber](msdv-driver.md)
</dt> </dl>

 

 



