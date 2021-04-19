---
title: Optimieren der DVD-Leistung für Windows-Spiele
description: In diesem Artikel wird erläutert, wie Sie die DVD-Leistung für Windows-Spiele optimieren.
ms.assetid: 01e8dc7d-4ba7-40dd-d845-a20000201ae1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb15063d0441423ccb3a9f67db84caa134f801c6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341731"
---
# <a name="optimizing-dvd-performance-for-windows-games"></a>Optimieren der DVD-Leistung für Windows-Spiele

Ein hoher Prozentsatz an Computern, auf denen Windows ausgeführt wird, verfügt über ein DVD-Laufwerk, und viele Spiele werden auf DVD ausgeliefert. Daher wird empfohlen, dass Sie sicherstellen, dass Ihre Spiele das DVD-Laufwerk vollständig nutzen. Wenn Sie wissen, wie Daten von einer DVD gelesen werden und wie sich der Speicherort der Daten auf die Lesezeit auswirkt, können Sie die Ladezeiten reduzieren und die Gesamtleistung während der Spiel Wiedergabe verbessern. In diesem Artikel wird erläutert, wie Sie die DVD-Leistung für Windows-Spiele optimieren.

-   [Grundlegendes Layout einer DVD](#basic-layout-of-a-dvd)
-   [Lesen von einer DVD](#reading-from-a-dvd)
-   [Lesefehler](#reading-errors)
-   [Datendurchsatz](#data-throughput)
-   [Beispiele für den Verlust von Durchsatz](#examples-of-wasted-throughput)
-   [Synchrones lesen im Vergleich zu asynchron](#reading-synchronously-vs-asynchronously)
-   [Optimaler Lesevorgang](#reading-optimally)
-   [DVD-Kompatibilität](#dvd-compatibility)
-   [Zusammenfassung](#summary)

## <a name="basic-layout-of-a-dvd"></a>Grundlegendes Layout einer DVD

Diese Abbildung zeigt das grundlegende Layout einer DVD.

![DVD-Layout](images/dvdsector.png)

Daten auf einer DVD werden als fortlaufende Spirale, wie auf einer CD, gespeichert. die Dateien werden jedoch in Blöcke und Sektoren aufgeteilt. Dateien werden auf ECC-Blöcke (Error Correction Code) verteilt, und jeder Block ist in Sektoren mit 16 2 KB (d. h. 32 KB an Daten in jedem Block) aufgeteilt. Dateien werden entlang der Sektorgrenzen ausgerichtet, und nicht verwendeter Speicherplatz in einem Sektor bleibt leer. Wenn eine Datei nur 10 Bytes hat, wird der restliche Speicherplatz in diesem 2-KB-Sektor verschwendet. Wenn möglich, bündeln Sie Dateien in Schritten von 2 KB, um die beste Datendichte zu erzielen. Beachten Sie, dass diese Spezifikationen nur für DVDs gelten und für CD und HD-DVD verschiedene Spezifikationen gelten.

## <a name="reading-from-a-dvd"></a>Lesen von einer DVD

Hier ist die Sequenz, die ein DVD-Laufwerk ausführt, wenn eine Anforderung zum Lesen von einer DVD empfangen wird:

1.  Ändern von Ebenen bei Bedarf
2.  Seek
3.  Neufokussieren der optischen Pickup Unit (opu) zum Lesen von Daten
4.  Überprüfen der tatsächlichen Position
5.  Anpassen und wiederholen, bis die richtigen Daten gefunden werden

Laufwerks Lesevorgänge werden unterschiedlich quantifisiert, abhängig davon, ob es sich um logische Laufwerk Lesevorgänge oder um Lesevorgänge physischer Laufwerke handelt. Logische Laufwerks Lesevorgänge können nur eine ganzzahlige Menge von DVD-Sektoren lesen, während eine Lese Anforderung eines physischen Laufwerks nur eine ganzzahlige Menge von ECC-Blöcken lesen kann. In der Regel empfängt das physische Laufwerk eine Lese Anforderung. Es wird versucht, den Cache zu füllen. Die Cache Größe des DVD-Laufwerks hängt von den Spezifikationen der einzelnen Laufwerke ab.

Wenn ein DVD-Laufwerk eine Lese Anforderung erhält, die die Cache Größe überschreitet, wird die Anforderung in Anforderungen im Cache abgegliedert. Das Laufwerk sucht den ECC-Block, der den ersten Sektor der Anforderung enthält, und liest den gesamten ECC-Block. Die Laufwerks Firmware decodiert den ECC-Block und liest dann den nächsten ECC-Block. Der Prozess wird wiederholt, bis der Laufwerks Cache ausgefüllt ist oder alle Anforderungen erfüllt sind. Der Kernel liest dann die decodierten Daten aus dem Laufwerks Cache. Dann leert der Cache den Cache und startet den nächsten Lesevorgang, wenn Lese Anforderungen übrig bleiben.

> [!Note]  
> Jeder nicht zwischengespeicherte Lesevorgang leert den Laufwerk Cache.

 

## <a name="reading-errors"></a>Lesefehler

DVDs und DVD-Laufwerke sind nicht perfekt, und während des Lesens können Fehler auftreten. Ebenso wie CDs können Teile einer DVD von Staub oder Kratzern unlesbar werden. Wenn ein beliebiger Teil eines Blocks nicht lesbar ist, gilt der gesamte Block als nicht lesbar. Wenn ein Lesefehler auftritt, versucht das Laufwerk, den ECC-Block erneut zu lesen. Wenn der Block weiterhin unlesbar ist, bricht das Laufwerk den Lesevorgang ab und gibt einen Wert an den Kernel zurück, der angibt, dass der Block nicht lesbar ist. Der Kernel entscheidet dann, welcher Schritt als nächstes ausgeführt werden soll. Der Kernel kann die Anforderung entweder erneut ausgeben, den Lesevorgang vollständig abbrechen oder das Laufwerk nach unten drehen und die Anforderung erneut ausgeben.

## <a name="data-throughput"></a>Datendurchsatz

Der Datendurchsatz eines DVD-Laufwerks hängt von mehreren Faktoren ab: dem Speicherort der angeforderten Daten, der Bereinigung oder der Datenträger Bereinigung auf dem Datenträger, der Anzahl der Streams, die vom Datenträger gelesen werden, der Größe der Puffer, die diesen Streams zugeordnet sind, und den Spezifikationen des einzelnen Laufwerks. Der Durchsatz hängt auch davon ab, ob das Laufwerk über Konstante Angular Velocity (CAV) oder Konstante Lineare Geschwindigkeit (CLV) verfügt. Wenn ein Laufwerk mit CAV Spinnt, wird die Festplatte unabhängig davon, wo sich die "optische Pickup Unit (opu)" befindet, mit derselben Geschwindigkeit geöffnet. Dies bedeutet, dass die Daten nach der opu schneller verschoben werden, da sich die opu näher am äußeren Rand der Platte nähert. Mit CLV wird die Diskette langsamer, wenn die opu nach außen bewegt wird, sodass die Datenverfolgung mit einer konstanten Geschwindigkeit hinter der opu bewegt wird. Die DVD-Laufwerke in den meisten PCs verwenden CLV.

Während das Laufwerk die Ebenen sucht und ändert, können Daten nicht von der Festplatte gelesen werden. Es empfiehlt sich, diese Vorgänge zu minimieren, insbesondere beim Lesen von Daten für einen anfänglichen Ladebildschirm.

## <a name="examples-of-wasted-throughput"></a>Beispiele für den Verlust von Durchsatz

Um zu verstehen, wie Datendurchsatz verschwendet werden kann, sollten Sie ein hypothetisches Laufwerk und eine DVD in Erwägung gezogen Nehmen wir an, dass eine Datei in der Mitte der CD gelesen werden muss. Der Durchsatz von diesem Bereich der Festplatte beträgt ungefähr 8,25 MB/Sek. Wenn der Such Strich eine Hälfte oder ein Drittel von voll ist, beträgt die durchschnittliche Suchzeit 150 ms. In diesem Beispiel konnten 1,2 MB (150 MS × 8,25 MB/Sek.) in der Zeit gelesen werden, in der die opu zum Lesen der opu benötigt wurde. Durch das Hinzufügen einer ebenenänderung wird der verschwendete Durchsatz auf 1,8 MB (225 ms × 8,25 MB/Sek.) erhöht.

Ein weiteres Beispiel, in dem der Verlust von Durchsatz veranschaulicht wird, ist das Laden von 20 Dateien, die sich aus einem CAV-Laufwerk ohne Änderungen Wenn die Suchzeit für jede Datei zuzüglich der Latenzzeit vor dem Lesen von Daten ungefähr 200 MS beträgt, werden 4 Sekunden (20 Dateien × 200 MS) für die Suche nach den Daten aufgewendet. Wenn sich die Dateien auf dem äußeren Durchschnitt befinden und mit 11 × Geschwindigkeit gelesen werden, liegt der Durchsatz bei einem Durchsatz von 15,2 MB/Sek. (11 Geschwindigkeit/12 Geschwindigkeit × 16 MB/Sek.). Der in diesem Beispiel verschwendete Durchsatz beträgt ungefähr 60,8 MB (15,2 MB/s × 4 Sek.).

## <a name="reading-synchronously-vs-asynchronously"></a>Synchrones lesen im Vergleich zu asynchron

Asynchrone Lesevorgänge sind effizienter als synchrone Lesevorgänge. Beim synchronen lesen werden ein oder mehrere ECC-Datenblöcke in den Systemspeicher gelesen, bevor Sie in den Anwendungs Speicher kopiert werden. Im Gegensatz dazu kopiert das asynchrone Lesen decodierte ECC-Blöcke direkt in den Anwendungs Speicher, wodurch der L2-Cache vermieden wird und weniger CPU-Aufwand entsteht. Verwenden Sie zum asynchronen Lesen das überlappende Flag für das \_ Dateiflag, \_ Wenn Sie die Funktion "up [**File**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " verwenden, um Dateien zu öffnen. Die Funktion "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " benötigt außerdem eine gültige überlappende Struktur, die zum Ausführen von asynchronen e/a-Vorgängen übergangen wird.

Weitere Informationen zu asynchronen e/a-Vorgängen finden Sie unter [synchrone und asynchrone e/a-](/windows/desktop/FileIO/synchronous-and-asynchronous-i-o)Vorgänge.

## <a name="reading-optimally"></a>Optimaler Lesevorgang

Das beste Prinzip beim Lesen von einer DVD besteht darin, das Suchen und Lesen kleiner Datenmengen zu vermeiden. Wenn die Menge der gelesenen Daten kleiner ist als die Kapazität eines ECC-Blocks – weniger als 32 KB – wird der restliche Block verschwendet. Da die Cache Größen von Laufwerk zu Laufwerk variieren, müssen Entwickler mindestens eine Datenmenge für Lese Anforderungen festlegen und nicht kleiner als das. Die minimale Größe muss ein ganzzahliges Vielfaches eines ECC-Blocks sein, um zu vermeiden, dass beim Lesen und Decodieren von Daten, die nicht verwendet werden, Zeit verschwendet Es ist auch wichtig, die Suche nach allen Kosten zu vermeiden, da bei jeder Suche Zeit die Zeit aufgewendet wird, mit der keine Daten gelesen werden.

## <a name="dvd-compatibility"></a>DVD-Kompatibilität

Es gibt einige wichtige Kompatibilitätsprobleme, die bei der Freigabe auf DVD zu beachten sind. Erstens können DVD-Laufwerke auf Windows-basierten Computern die Leistung variieren. Wenn also die DVD eine bestimmte Anforderung für den Durchsatz hat, ist es wichtig sicherzustellen, dass die Hardware Ihrer Benutzer diese Anforderungen erfüllt. Außerdem können mehrschichtige DVDs Kompatibilitätsprobleme auf einigen DVD-Laufwerken verursachen. Um diese Probleme zu vermeiden, empfiehlt es sich, eine DVD mit einer einzelnen Ebene zu übermitteln oder eine mehrschichtige DVD vor der Freigabe gründlich auf einem Großteil der Laufwerke zu testen.

## <a name="summary"></a>Zusammenfassung

Um die DVD-Leistung zu verbessern, können einige allgemeine Regeln angewendet werden. Mithilfe der folgenden Verfahren können Sie den Durchsatz maximieren und verschwendete Daten verringern:

-   Vermeiden von Lesevorgängen, die kleiner als 32 KB sind
-   Daten anordnen, um Suchvorgänge zu reduzieren oder auszuschließen
-   Layout von Daten an ECC-Block Grenzen
-   Maximieren Sie die Kapazität, indem Sie kleine Dateien in Blöcke mit 2 KB bündeln, und reduzieren Sie den Leerraum in DVD-Sektoren.
-   Asynchron lesen, um die CPU-Auslastung und übermäßig hohe Speicherauslastung zu reduzieren
-   Vermeiden Sie das Freigeben von mehrschichtigen DVDs

 

 