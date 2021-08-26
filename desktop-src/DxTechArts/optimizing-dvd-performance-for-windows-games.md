---
title: Optimieren der DVD-Leistung für Windows Games
description: In diesem Artikel wird erläutert, wie Sie die DVD-Leistung für Windows optimieren.
ms.assetid: 01e8dc7d-4ba7-40dd-d845-a20000201ae1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe08ba6188df9b8bbc25a73595bf1509b257696955c1fcbd1ae98091b3c8aecf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042535"
---
# <a name="optimizing-dvd-performance-for-windows-games"></a>Optimieren der DVD-Leistung für Windows Games

Ein hoher Prozentsatz der Computer, auf denen Windows ausgeführt wird, verfügen über ein DVD-Laufwerk, und viele Spiele werden auf DVD veröffentlicht. Daher wird empfohlen, dass Sie sicherstellen, dass Ihre Spiele das DVD-Laufwerk voll ausnutzen. Wenn Sie verstehen, wie Daten von einer DVD gelesen werden und wie sich der Speicherort der Daten auf die Lesezeit auswirken, können Sie ladezeiten reduzieren und die Gesamtleistung während des Spiels verbessern. In diesem Artikel wird erläutert, wie Sie die DVD-Leistung für Windows optimieren.

-   [Grundlegendes Layout einer DVD](#basic-layout-of-a-dvd)
-   [Lesen von einer DVD](#reading-from-a-dvd)
-   [Lesen von Fehlern](#reading-errors)
-   [Datendurchsatz](#data-throughput)
-   [Beispiele für verschwendeten Durchsatz](#examples-of-wasted-throughput)
-   [Synchrones und asynchrones Lesen](#reading-synchronously-vs-asynchronously)
-   [Optimales Lesen](#reading-optimally)
-   [DVD-Kompatibilität](#dvd-compatibility)
-   [Zusammenfassung](#summary)

## <a name="basic-layout-of-a-dvd"></a>Grundlegendes Layout einer DVD

Diese Abbildung zeigt das grundlegende Layout einer DVD.

![DVD-Layout](images/dvdsector.png)

Daten auf einer DVD werden als fortlaufende Datenübertragung gespeichert, wie auf einer CD. Die Dateien werden jedoch in Blöcke und Sektoren zerbrochen. Dateien werden über ECC-Blöcke (Error Correction Code) verteilt, und jeder Block ist in 16 2-KB-Sektoren unterteilt (d. h. 32 KB Daten in jedem Block). Dateien werden entlang der Sektorgrenzen ausgerichtet, und nicht verwendeter Speicherplatz in einem Sektor bleibt leer. Wenn eine Datei nur 10 Bytes enthält, wird der Rest des Speicherplatzes in diesem 2-KB-Sektor verschwendet. daher bündeln Sie Dateien nach Möglichkeit in Schritten von 2 KB, um die beste Datendichte zu erhalten. Beachten Sie, dass diese Spezifikationen nur für DVD gelten und CD und HD-DVD unterschiedliche Spezifikationen haben.

## <a name="reading-from-a-dvd"></a>Lesen von einer DVD

Dies ist die Sequenz, die ein DVD-Laufwerk beim Empfang einer Anforderung zum Lesen von einer DVD ausgeführt wird:

1.  Ändern von Ebenen, falls erforderlich
2.  Seek
3.  Neukonzentrieren der optischen Aufnahmeeinheit (OPTICAL Pickup Unit, OPU) zum Lesen von Daten
4.  Überprüfen der tatsächlichen Position
5.  Anpassen und Wiederholen, bis die richtigen Daten gefunden werden

Laufwerklesevorgänge werden unterschiedlich quantisiert, je nachdem, ob es sich um Lesevorgänge auf logischen Laufwerken oder um Lesevorgänge auf physischen Laufwerken handelt. Leseanforderungen für logische Laufwerke können nur eine ganze Zahl von DVD-Sektoren lesen, während eine Leseanforderung für physische Laufwerke nur eine ganze Menge von ECC-Blöcken lesen kann. In der Regel empfängt das physische Laufwerk eine Leseanforderung. Es wird versucht, seinen Cache zu füllen. Die Cachegröße des DVD-Laufwerks hängt von den Spezifikationen des jeweiligen Laufwerks ab.

Wenn ein DVD-Laufwerk eine Leseanforderung erhält, die die Cachegröße überschreitet, wird die Anforderung in Anforderungen mit Cachegröße aufgeschlüsselt. Das Laufwerk sucht den ECC-Block, der den ersten Sektor der Anforderung enthält, und liest den gesamten ECC-Block. Die Laufwerkfirmware decodiert den ECC-Block und liest dann den nächsten ECC-Block. Der Prozess wird wiederholt, bis der Laufwerkcache gefüllt ist oder alle Anforderungen erfüllt sind. Der Kernel liest dann die decodierten Daten aus dem Laufwerkcache. Anschließend wird der Cache geleert und der nächste Lesevorgang gestartet, wenn Leseanforderungen verbleiben.

> [!Note]  
> Bei jedem Nichtcachelese wird der Laufwerkcache geleert.

 

## <a name="reading-errors"></a>Lesen von Fehlern

DVDs und DVD-Laufwerke sind nicht perfekt, und beim Lesen können Fehler auftreten. Wie CDs können Teile einer DVD unlesbar werden. Wenn ein Teil eines Blocks nicht lesbar ist, wird der gesamte Block als nicht lesbar betrachtet. Wenn ein Lesefehler auftritt, versucht das Laufwerk, den ECC-Block erneut zu lesen. Wenn der Block immer noch nicht lesbar ist, bricht das Laufwerk den Lesevorgang ab und gibt einen Wert an den Kernel zurück, der angibt, dass der Block nicht lesbar war. Der Kernel entscheidet dann, welcher Schritt als Nächstes ausgeführt werden soll. Der Kernel kann entweder die Anforderung erneut ausführen, den Lesemodus vollständig abbrechen oder das Laufwerk nach unten drehen und die Anforderung erneut ausführen.

## <a name="data-throughput"></a>Datendurchsatz

Der Datendurchsatz eines DVD-Laufwerks hängt von mehreren Faktoren ab: dem Speicherort der angeforderten Daten, der Bereinigung oder dem Scratch des Datenträgers, der Anzahl der Streams, die vom Datenträger gelesen werden, der Größe der Puffer, die diesen Datenströmen zugeordnet sind, und den Spezifikationen des einzelnen Laufwerks. Der Durchsatz hängt auch davon ab, ob das Laufwerk über eine konstante Winkelgeschwindigkeit (CAV) oder eine konstante lineare Geschwindigkeit (Constant Linear Velocity, CLV) verfügt. Wenn ein Laufwerk mit CAV gedreht wird, wird der Datenträger unabhängig davon, wo sich die optische Aufnahmeeinheit (Optical Pickup Unit, OPU) befindet, mit der gleichen Geschwindigkeit gedreht. Dies bedeutet, dass die Datenspur schneller über die OPU bewegt wird, wenn sich die OPU näher am äußeren Rand des Datenträgers bewegt. Bei CLV wird der Datenträger langsamer gedreht, wenn die OPU nach außen bewegt wird, sodass die Datenspur mit konstanter Geschwindigkeit über die OPU hinaus bewegt wird. Die DVD-Laufwerke auf den meisten PCs verwenden CLV.

Während das Laufwerk Ebenen sucht und ändert, können Daten nicht vom Datenträger gelesen werden. Es ist eine bewährte Methode, diese Vorgänge zu minimieren, insbesondere beim Lesen von Daten für einen anfänglichen Ladebildschirm.

## <a name="examples-of-wasted-throughput"></a>Beispiele für verschwendeten Durchsatz

Um zu verstehen, wie der Datendurchsatz verschwendet werden kann, ziehen Sie ein hypothetisches Laufwerk und eine DVD in Betracht. Angenommen, eine Datei in der Mitte des Datenträgers muss gelesen werden. Der Durchsatz aus diesem Bereich des Datenträgers beträgt ca. 8,25 MB/s. Wenn der Suchstrich eine Hälfte oder ein Drittel des vollen Strichs ist, beträgt die durchschnittliche Suchzeit 150 ms. In diesem Beispiel hätten 1,2 MB (150 ms × 8,25 MB/s) in der Zeit gelesen werden können, in der es nur gelangt hätte, um die OPU dort zu erhalten, wo sie lesen kann. Durch hinzufügen einer Ebenenänderung wird der verschwendete Durchsatz auf 1,8 MB (225 ms × 8,25 MB/s) erhöht.

Ein weiteres Beispiel, das den verschwendeten Durchsatz veranschaulicht, ist das Laden von 20 dateien mit schlechtem Standort von einem CAV-Laufwerk ohne Ebenenänderungen. Wenn die Suchzeit für jede Datei plus der Wartezeit vor dem Lesen von Daten ungefähr 200 ms beträgt, werden 4 Sekunden (20 Dateien × 200 ms) nur für die Suche nach den Daten benötigt. Wenn sich die Dateien auf dem äußeren Hüllenbereich befinden und mit einer Geschwindigkeit von 11× gelesen werden, beträgt der Durchsatz durchschnittlich 15,2 MB/s (11 Geschwindigkeit/12 Geschwindigkeit × 16 MB/s). Der verschwendete Durchsatz in diesem Beispiel beträgt ungefähr 60,8 MB (15,2 MB/s × 4 Sek.).

## <a name="reading-synchronously-vs-asynchronously"></a>Synchrones und asynchrones Lesen

Asynchrones Lesen ist effizienter als synchrones Lesen. Beim synchronen Lesen werden ein oder mehrere ECC-Datenblöcke in den Systemspeicher eingelesen, bevor sie in den Anwendungsspeicher kopiert werden. Im Gegensatz dazu kopiert das asynchrone Lesen decodierte ECC-Blöcke direkt in den Anwendungsspeicher, wodurch der L2-Cache vermieden wird und weniger CPU-Mehraufwand entsteht. Verwenden Sie zum asynchronen Lesen das FLAG FILE FLAG OVERLAPPED, wenn Sie die \_ \_ [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) zum Öffnen von Dateien verwenden. Die [**ReadFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-readfile) benötigt auch eine gültige OVERLAPPED-Struktur, die übergeben wird, um asynchrone E/A-Vorgänge durchzuführen.

Weitere Informationen zu asynchronen E/A-Vorgängen finden Sie unter [Synchrone und asynchrone E/A.](/windows/desktop/FileIO/synchronous-and-asynchronous-i-o)

## <a name="reading-optimally"></a>Optimales Lesen

Das beste Prinzip beim Lesen von einer DVD ist es, das Suchen und Lesen kleiner Datenmengen zu vermeiden. Wenn die menge der gelesenen Daten kleiner als die Kapazität eines ECC-Blocks ist ( weniger als 32 KB), wird der Rest des Blocks verschwendet. Da die Cachegrößen von Laufwerk zu Laufwerk variieren, müssen Entwickler eine Mindestmenge an Daten für Leseanforderungen festlegen und diese nicht verkleinern. Die Mindestgröße sollte ein ganzzahliges Vielfaches eines ECC-Blocks sein, um zu vermeiden, dass Zeit für das Lesen und Decodieren von Daten verstreicht, die nicht verwendet werden. Es ist auch wichtig, die Suche um jeden Preis zu vermeiden, da jede Zeit, die für die Suche ausgegeben wird, zeitaufwandt, keine Daten zu lesen.

## <a name="dvd-compatibility"></a>DVD-Kompatibilität

Es gibt einige wichtige Kompatibilitätsprobleme, die bei der Veröffentlichung auf DVD zu beachten sind. Erstens können DVD-Laufwerke auf Windows-basierten Computern in der Leistung variieren. Wenn ihre DVD also eine bestimmte Anforderung an den Durchsatz hat, ist es wichtig sicherzustellen, dass die Hardware Ihrer Benutzer diese Anforderungen erfüllt. Außerdem können mehrschichtige DVDs Kompatibilitätsprobleme auf einigen DVD-Laufwerken verursachen. Um diese Probleme zu vermeiden, empfiehlt es sich, vor der Veröffentlichung eine einschichtige DVD zu liefern oder eine mehrschichtige DVD auf den meisten Laufwerken gründlich zu testen.

## <a name="summary"></a>Zusammenfassung

Zur Verbesserung der DVD-Leistung können einige allgemeine Regeln angewendet werden. Die folgenden Techniken können dazu beitragen, den Durchsatz zu maximieren und verschwendete Daten zu reduzieren:

-   Vermeiden Von Lese-/Lese-Ungen, die kleiner als 32 KB sind
-   Auslegen von Daten zum Reduzieren oder Beseitigen von Suchern
-   Legen Sie Daten an ECC-Blockgrenzen fest.
-   Maximieren der Kapazität durch Bündeln kleiner Dateien in 2-KB-Blöcken und Reduzieren des Auf padding-Speicherplatzes in DVD-Sektoren
-   Asynchrones Lesen, um die CPU-Auslastung und übermäßige Speicherauslastung zu reduzieren
-   Vermeiden der Freigabe mehrschichtiger DVDs

 

 