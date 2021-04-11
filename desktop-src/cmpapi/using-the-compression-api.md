---
description: Viele Anwendungen müssen Verlust lose Datenkomprimierung und-Komprimierung verwenden. Die Komprimierungs-API vereinfacht dies durch die Bereitstellung von Windows-Komprimierungs Algorithmen über eine öffentliche API.
ms.assetid: D603A7DE-D4A1-4515-9702-B03C81504661
title: Verwenden der Komprimierungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01eff163f4ea1ccf03e1cd4ac9cb16a26afeb265
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127413"
---
# <a name="using-the-compression-api"></a>Verwenden der Komprimierungs-API

Viele Anwendungen müssen Verlust lose Datenkomprimierung und-Komprimierung verwenden. Die Komprimierungs-API vereinfacht dies durch die Bereitstellung von Windows-Komprimierungs Algorithmen über eine öffentliche API. Jeder Komprimierungs Algorithmus verfügt über eine Reihe von Eigenschaften, die das Verhalten steuern. Die Komprimierungs-API macht eine Schnittstelle verfügbar, die es dem Entwickler ermöglicht, die Werte dieser Eigenschaften festzulegen oder abzufragen. Alle Eigenschaften für die unterstützten Komprimierungs Algorithmen verfügen über Standardwerte, die häufig verwendete Werte dieser Eigenschaften darstellen. Wenn eine Eigenschaft sowohl für die Komprimierung als auch für die Komprimierung erforderlich ist, sind die Standardwerte identisch und stellen sicher, dass identische Werte für die Komprimierung und die Komprimierung verwendet werden.

## <a name="selecting-the-compression-algorithm"></a>Auswählen des Komprimierungs Algorithmus

Nachdem ein Entwickler entschieden hat, dass eine Anwendung Daten komprimieren oder Dekomprimieren muss, besteht der nächste Schritt darin, einen Komprimierungs Algorithmus auszuwählen. Dies hängt möglicherweise von Tests ab, um die optimale Kombination aus Geschwindigkeit, Komprimierungs Verhältnis und Arbeitsspeicher Anforderung für eine bestimmte Anwendung zu finden. Die folgende Liste enthält einen relativen Vergleich der Komprimierungs Algorithmen, die derzeit von der Komprimierungs-API unterstützt werden. Nicht jede Option ist für jeden Komprimierungs Algorithmus verfügbar, und der Vergleich ist ungefähre Werte, da die Leistung von den Eingabedaten abhängen kann.

Xpress (**Komprimierungs \_ Algorithmus \_ Xpress**)

-   Sehr schnell mit geringen Ressourcenanforderungen
-   Verhältnis für mittlere Komprimierung
-   Hohe Komprimierungs-und Komprimierungs Geschwindigkeiten
-   Wenig Arbeitsspeicher erforderlich
-   Unterstützt die in der [**Klasse "Komprimieren von \_ Informations \_ Klassen**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) " verfügbare Option auf **\_ \_ Klassen \_ Ebene komprimieren** . Der Standardwert ist **(DWORD) 0**. Für einige Daten kann der Wert **(DWORD) 1** das Komprimierungs Verhältnis mit einer etwas langsameren Komprimierungs Geschwindigkeit verbessern.

Xpress mit Huffman Encoding (**Komprimieren von \_ Algorithmus \_ Xpress \_ Huff**)

-   Das Komprimierungs Verhältnis ist höher als der **Komprimierungs \_ Algorithmus \_ Xpress**
-   Verhältnis für mittlere Komprimierung
-   Geschwindigkeiten für mittlere bis hohe Komprimierung und-Komprimierung
-   Wenig Arbeitsspeicher erforderlich
-   Unterstützt die Option " **\_ Informationen auf \_ Klassen \_ Ebene komprimieren** " in der " [**Compress \_ Information \_ Class**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) "-Enumeration. Der Standardwert ist **(DWORD) 0**. Für einige Daten kann der Wert **(DWORD) 1** das Komprimierungs Verhältnis mit einer etwas langsameren Komprimierungs Geschwindigkeit verbessern.

mszip (**\_ Algorithmus mit \_ mszip komprimieren**)

-   Verwendet mehr Ressourcen als " **Komprimieren von \_ Algorithmus \_ Xpress \_ Huff** ".
-   Generiert einen komprimierten Block ähnlich RFC 1951.
-   Verhältnis zwischen mittlerer und hoher Komprimierung
-   Geschwindigkeit mittlerer Komprimierung und hohe Komprimierungs Geschwindigkeit
-   Mittlere Arbeitsspeicher Anforderung

lzms (**\_ Algorithmus- \_ lzms komprimieren**)

-   Guter Algorithmus, wenn die Größe der zu komprimierenden Daten größer als 2 MB ist.
-   Hohes Komprimierungs Verhältnis
-   Geschwindigkeit bei niedriger Komprimierung und hohe Komprimierungs Geschwindigkeit
-   Anforderung für mittlere und hohe Arbeitsspeicher
-   Unterstützt die Option " **\_ Informationen \_ Klassen \_ Block \_ Größe komprimieren** " in der " [**Compress \_ Information \_ Class**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) "-Enumeration. Eine minimale Größe von 1 MB wird empfohlen, um ein besseres Komprimierungs Verhältnis zu erzielen.

## <a name="deciding-which-compression-api-mode-to-use"></a>Entscheiden, welcher Komprimierungs-API-Modus verwendet werden soll

Nachdem ein Entwickler den Komprimierungs Algorithmus ausgewählt hat, ist die nächste Entscheidung, welche der beiden Modi der Komprimierungs-API verwendet werden soll: Puffer Modus oder Block Modus. Der Puffer Modus wurde zur einfachen Verwendung entwickelt und wird in den meisten Fällen empfohlen.

Der Puffer Modus teilt automatisch den Eingabepuffer in Blöcke einer Größe auf, die für den ausgewählten Komprimierungs Algorithmus geeignet ist. Der Puffer Modus formatiert und speichert automatisch die nicht komprimierte Puffergröße im komprimierten Puffer. Die Größe des komprimierten Puffers wird nicht automatisch gespeichert, und die Anwendung muss dies für die Komprimierung speichern. Schließen Sie das Flag zum **Komprimieren von \_ Rohdaten** nicht in den Algorithmusparameter ein, wenn Sie zum Verwenden des Puffer Modus "  [**kreatecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) " und " [**kreatede**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) Ein Codebeispiel für eine puffermodusanwendung finden Sie im Abschnitt [Verwenden der Komprimierungs-API im Puffer Modus](using-the-compression-api-in-buffer-mode.md) .

Der Block Modus ermöglicht es dem Entwickler, die Blockgröße zu steuern, erfordert jedoch mehr Arbeit durch die Anwendung. Wenn Sie den Block Modus verwenden, muss die Anwendung die Eingabedaten bei der Komprimierung in ordnungsgemäß formatierte Teile aufteilen und Sie dann beim Dekomprimieren wieder zusammensetzen. Der Block Modus schlägt fehl, wenn die Größe des Eingabe Puffers größer als die interne Blockgröße des Komprimierungs Algorithmus ist. Die interne Blockgröße beträgt 32 KB für mszip und 1 GB für die Xpress-Komprimierungs Algorithmen. Die interne Blockgröße für lzms kann bis zu 64 GB mit einer entsprechenden Erhöhung der Arbeitsspeicher Nutzung konfiguriert werden. Die Größe des komprimierten Puffers wird nicht automatisch gespeichert, und die Anwendung muss dies auch für die Komprimierung speichern. Der Wert des *uncompressedbuffersize* -Parameters von [**Decompress**](/windows/desktop/api/compressapi/nf-compressapi-decompress) muss genau gleich der ursprünglichen Größe der nicht komprimierten Daten und nicht nur der Größe des Ausgabepuffers sein. Dies bedeutet, dass Ihre Anwendung bei Verwendung des Block Modus die genaue ursprüngliche Größe der nicht komprimierten Daten sowie die komprimierten Daten und die komprimierte Größe speichern sollte. Schließen Sie das Flag zum **Komprimieren von \_ Rohdaten** in den Algorithmusparameter ein, wenn Sie sowohl " [**kreatecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) " als auch " [**anatedekompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) " für  Ein Codebeispiel für eine blockmodusanwendung finden Sie im Abschnitt [using the Compression API in Block Mode](using-the-compression-api-in-block-mode.md) .

## <a name="custom-memory-allocation"></a>Benutzerdefinierte Speicher Belegung

Puffer-und blockmodusanwendungen haben die Möglichkeit, eine benutzerdefinierte Speicher Belegungs Routine anzugeben, wenn Sie " [**kreatecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) " und " [**kreatedekompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor)" aufrufen. Der *allocationroutinen* -Parameter gibt die Struktur der [**komprimieren- \_ Zuordnungs \_ Routinen**](/windows/desktop/api/compressapi/ns-compressapi-compress_allocation_routines) an, die die Speicher Belegungs Routine enthält. Die Anwendung kann dann die Blockgröße für den Kompressor mithilfe von [**setcompressorinformation**](/windows/desktop/api/compressapi/nf-compressapi-setcompressorinformation)festlegen. Ein Beispiel für eine einfache, angepasste Zuordnungs Routine finden Sie im Abschnitt [Verwenden des Komprimierungs-API im Block Modus](using-the-compression-api-in-block-mode.md) .

 

 



