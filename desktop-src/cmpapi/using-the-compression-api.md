---
description: Viele Anwendungen müssen verlustfreie Datenkomprimierung und Dekomprimierung verwenden. Die Komprimierungs-API vereinfacht dies, indem Windows Komprimierungsalgorithmen über eine öffentliche API verfügbar gemacht werden.
ms.assetid: D603A7DE-D4A1-4515-9702-B03C81504661
title: Verwenden der Komprimierungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fedc1d57ad48196290500383686b35f557c87c34099aad842b1e8ff18f00d318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551384"
---
# <a name="using-the-compression-api"></a>Verwenden der Komprimierungs-API

Viele Anwendungen müssen verlustfreie Datenkomprimierung und Dekomprimierung verwenden. Die Komprimierungs-API vereinfacht dies, indem Windows Komprimierungsalgorithmen über eine öffentliche API verfügbar gemacht werden. Jeder Komprimierungsalgorithmus verfügt über einen Satz von Eigenschaften, der sein Verhalten steuert. Die Komprimierungs-API macht eine Schnittstelle verfügbar, mit der der Entwickler die Werte dieser Eigenschaften festlegen oder abfragen kann. Alle Eigenschaften für die unterstützten Komprimierungsalgorithmen verfügen über Standardwerte, die häufig verwendete Werte dieser Eigenschaften darstellen. Wenn eine Eigenschaft sowohl für die Komprimierung als auch für die Dekomprimierung erforderlich ist, sind die Standardwerte identisch, um sicherzustellen, dass identische Werte für die Komprimierung und Dekomprimierung verwendet werden.

## <a name="selecting-the-compression-algorithm"></a>Auswählen des Komprimierungsalgorithmus

Nachdem ein Entwickler entschieden hat, dass eine Anwendung Daten komprimieren oder dekomprimieren muss, besteht der nächste Schritt in der Auswahl eines Komprimierungsalgorithmus. Dies kann von Tests abhängen, um die beste Kombination aus Geschwindigkeit, Komprimierungsverhältnis und Arbeitsspeicheranforderungen für eine bestimmte Anwendung zu finden. Die folgende Liste enthält einen relativen Vergleich der Komprimierungsalgorithmen, die derzeit von der Komprimierungs-API unterstützt werden. Nicht jede Option ist für jeden Komprimierungsalgorithmus verfügbar, und der Vergleich ist ungefähr, da die Leistung von den Eingabedaten abhängen kann.

XPRESS (**COMPRESS \_ ALGORITHM \_ XPRESS**)

-   Sehr schnell mit geringen Ressourcenanforderungen
-   Mittleres Komprimierungsverhältnis
-   Hohe Komprimierungs- und Dekomprimierungsgeschwindigkeiten
-   Geringer Arbeitsspeicherbedarf
-   Unterstützt die **OPTION COMPRESS INFORMATION CLASS \_ \_ \_ LEVEL,** die in der [**COMPRESS INFORMATION \_ \_ CLASS-Enumeration verfügbar**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) ist. Der Standardwert ist **(DWORD)0.** Bei einigen Daten kann der **Wert (DWORD)1** das Komprimierungsverhältnis mit einer etwas langsameren Komprimierungsgeschwindigkeit verbessern.

XPRESS mit Huffman-Codierung (**COMPRESS \_ ALGORITHM \_ XPRESS \_ HUFF**)

-   Komprimierungsverhältnis ist höher als **COMPRESS \_ ALGORITHM \_ XPRESS**
-   Mittleres Komprimierungsverhältnis
-   Mittlere bis hohe Komprimierungs- und Dekomprimierungsgeschwindigkeiten
-   Geringer Arbeitsspeicherbedarf
-   Unterstützt die **OPTION COMPRESS INFORMATION CLASS \_ \_ \_ LEVEL** in der [**COMPRESS INFORMATION \_ \_ CLASS-Enumeration.**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) Der Standardwert ist **(DWORD)0.** Bei einigen Daten kann der **Wert (DWORD)1** das Komprimierungsverhältnis mit einer etwas langsameren Komprimierungsgeschwindigkeit verbessern.

MSZIP (**COMPRESS \_ ALGORITHM \_ MSZIP**)

-   Verwendet mehr Ressourcen als **COMPRESS \_ ALGORITHM \_ XPRESS \_ HUFF**
-   Generiert einen komprimierten Block, der RFC 1951 ähnelt.
-   Mittleres bis hohes Komprimierungsverhältnis
-   Mittlere Komprimierungsgeschwindigkeit und hohe Dekomprimierungsgeschwindigkeit
-   Mittlerer Arbeitsspeicherbedarf

LZMS (**COMPRESS \_ ALGORITHM \_ LZMS**)

-   Ein guter Algorithmus, wenn die Größe der zu komprimierenden Daten über 2 MB liegt.
-   Hohes Komprimierungsverhältnis
-   Niedrige Komprimierungsgeschwindigkeit und hohe Dekomprimierungsgeschwindigkeit
-   Mittlerer bis hoher Arbeitsspeicherbedarf
-   Unterstützt die **OPTION COMPRESS INFORMATION CLASS BLOCK \_ \_ \_ \_ SIZE** in der [**COMPRESS INFORMATION \_ \_ CLASS-Enumeration.**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) Es wird eine Mindestgröße von 1 MB empfohlen, um ein besseres Komprimierungsverhältnis zu erhalten.

## <a name="deciding-which-compression-api-mode-to-use"></a>Entscheidung für den zu verwendenden Komprimierungs-API-Modus

Nachdem ein Entwickler den Komprimierungsalgorithmus ausgewählt hat, ist die nächste Entscheidung, welcher der beiden Modi der Komprimierungs-API verwendet werden soll: Puffermodus oder Blockmodus. Der Puffermodus wurde zur einfacheren Verwendung entwickelt und wird in den meisten Fällen empfohlen.

Der Puffermodus teilt den Eingabepuffer automatisch in Blöcke einer Größe auf, die für den ausgewählten Komprimierungsalgorithmus geeignet ist. Der Puffermodus formatiert und speichert die unkomprimierte Puffergröße automatisch im komprimierten Puffer. Die Größe des komprimierten Puffers wird nicht automatisch gespeichert, und die Anwendung muss diesen für die Dekomprimierung speichern. Schließen Sie das **COMPRESS \_ RAW-Flag** nicht in den *Algorithmusparameter* ein, wenn Sie [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) und [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) aufrufen, um den Puffermodus zu verwenden. Ein Codebeispiel für eine Puffermodusanwendung finden Sie im Abschnitt [Verwenden der Komprimierungs-API im Puffermodus.](using-the-compression-api-in-buffer-mode.md)

Mit dem Blockmodus kann der Entwickler die Blockgröße steuern, erfordert jedoch mehr Arbeit durch die Anwendung. Bei Verwendung des Blockmodus muss die Anwendung die Eingabedaten beim Komprimieren in Teile mit entsprechender Größe unterteilen und die Teile dann beim Dekomprimieren wieder zusammenlegen. Der Blockmodus schlägt fehl, wenn die Größe des Eingabepuffers größer als die interne Blockgröße des Komprimierungsalgorithmus ist. Die interne Blockgröße beträgt 32 KB für MSZIP und 1 GB für die XPRESS-Komprimierungsalgorithmen. Die interne Blockgröße für LZMS kann bis zu 64 GB bei entsprechender Zunahme der Arbeitsspeichernutzung konfiguriert werden. Die Größe des komprimierten Puffers wird nicht automatisch gespeichert, und die Anwendung muss diesen auch für die Dekomprimierung speichern. Der Wert des *UncompressedBufferSize-Parameters* von [**Decompress**](/windows/desktop/api/compressapi/nf-compressapi-decompress) muss genau der ursprünglichen Größe der nicht komprimierten Daten und nicht nur der Größe des Ausgabepuffers entspricht. Dies bedeutet, dass Ihre Anwendung bei Verwendung des Blockmodus die genaue ursprüngliche Größe der unkomprimierten Daten sowie die komprimierten Daten und die komprimierte Größe speichern sollte. Schließen Sie **das COMPRESS \_ RAW-Flag** in den *Algorithmusparameter* ein, wenn Sie [**sowohl CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) als auch [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) aufrufen, um den Blockmodus zu verwenden. Ein Codebeispiel für eine Blockmodusanwendung finden Sie im Abschnitt [Verwenden der Komprimierungs-API im Blockmodus.](using-the-compression-api-in-block-mode.md)

## <a name="custom-memory-allocation"></a>Benutzerdefinierte Speicherzuweisung

Puffer- und Blockmodusanwendungen haben die Möglichkeit, eine benutzerdefinierte Speicherbelegungsroutine anzugeben, wenn sie [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) und [**CreateDecompressor aufrufen.**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) Der *AllocationRoutines-Parameter* gibt die [**COMPRESS ALLOCATION \_ \_ ROUTINES-Struktur**](/windows/desktop/api/compressapi/ns-compressapi-compress_allocation_routines) an, die die Speicherbelegungsroutine enthält. Die Anwendung kann dann mit [**SetCompressorInformation**](/windows/desktop/api/compressapi/nf-compressapi-setcompressorinformation)die Blockgröße für die -Gruppe festlegen. Ein Beispiel [für eine einfache benutzerdefinierte Zuordnungsroutine finden](using-the-compression-api-in-block-mode.md) Sie im Abschnitt Verwenden der Komprimierungs-API im Blockmodus.

 

 



