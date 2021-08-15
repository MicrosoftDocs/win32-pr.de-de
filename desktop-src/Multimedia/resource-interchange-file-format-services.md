---
title: Formatdienste für Ressourcenaustauschdateien
description: Formatdienste für Ressourcenaustauschdateien
ms.assetid: 8526794b-7b40-470f-94f7-935d7dbf9151
keywords:
- Multimediadatei-E/A, Resource Interchange File Format (DOSSIER)
- Datei-E/A, Resource Interchange File Format (DOSSIER)
- Eingabe und Ausgabe (E/A), Resource Interchange File Format (DOSSIER)
- E/A (Eingabe und Ausgabe), Resource Interchange File Format (DOSSIER)
- mmioOpen-Funktion
- Resource Interchange File Format (DOSSIER)
- PROTOKOLLDATEI (Resource Interchange File Format)
- IGE E/A
- UNK-Block
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5967165996b2a7fb9ed9b40c9a1f3c5608cd3bb4eb1e6cf05ae351f6ce6f2a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801927"
---
# <a name="resource-interchange-file-format-services"></a>Formatdienste für Ressourcenaustauschdateien

Das bevorzugte Format für Multimediadateien ist das RESOURCE INTERCHANGE-Dateiformat (RESOURCE Interchange File Format). Die PROTOKOLLDATEI-E/A-Funktionen funktionieren mit den grundlegenden gepufferten und nicht gepufferten Datei-E/A-Diensten. Sie können CSV-Dateien auf die gleiche Weise wie andere Dateitypen öffnen, lesen und schreiben. Ausführliche Informationen zu CSV finden Sie unter [AVIFile Functions and Macros ( AVIFile-Funktionen und -Makros).](avifile-functions-and-macros.md)

FÜR DATEIEN werden Vier-Zeichen-Codes verwendet, um Dateielemente zu identifizieren. Diese Codes sind 32-Bit-Mengen, die eine Sequenz von ein bis vier alphanumerischen ASCII-Zeichen darstellen, die auf der rechten Seite mit Leerzeichen aufgefüllt sind. Der Datentyp für Vier-Zeichen-Codes ist **FOURCC.** Verwenden Sie das [**MmioFOURCC-Makro,**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) um vier Zeichen in einen vierstelligen Code zu konvertieren. Verwenden Sie die [**MmioStringToFOURCC-Funktion,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) um eine auf NULL endende Zeichenfolge in einen vierstelligen Code zu konvertieren.

Der grundlegende Baustein einer CSV-Datei ist ein *Block*. Ein Block ist eine logische Einheit von Multimediadaten, z. B. ein einzelner Frame in einem Videoclip. Jeder Block enthält die folgenden Felder:

-   Ein vierstelliger Code, der den Blockbezeichner angibt
-   Ein Doublewordwert, der die Größe des Datenmembers im Block angibt.
-   Ein Datenfeld

Die folgende Abbildung zeigt einen BLOCK "CSV", der zwei Teilblöcke enthält.

![Chunk, der zwei Teilblöcke enthält Bild](images/mmio1.gif)

Ein Block, der in einem anderen Block enthalten ist, ist ein *Unterkunk.* Die einzigen Blöcke, die Teilblöcke enthalten dürfen, sind diejenigen mit dem Blockbezeichner "CSV" oder "LIST". Ein Block, der einen anderen Block enthält, wird als *übergeordneter Block* bezeichnet. Der erste Block in einer CSV-Datei muss ein "DOSSIER"-Block sein. Alle anderen Blöcke in der Datei sind Teilblöcke des Segmentes "CSV".

"IGE"-Blöcke enthalten ein zusätzliches Feld in den ersten vier Bytes des Datenfelds. Dieses zusätzliche Feld stellt den *Formulartyp* des Felds bereit. Der Formulartyp ist ein vierstelliger Code, der das Format der in der Datei gespeicherten Daten identifiziert. Beispielsweise weisen Microsoft Waveform-Audiodateien den Formulartyp "WAVE" auf.

"LIST"-Blöcke enthalten auch ein zusätzliches Feld in den ersten vier Bytes des Datenfelds. Dieses zusätzliche Feld enthält den *Listentyp* des Felds. Der Listentyp ist ein vierstelliger Code, der den Inhalt der Liste identifiziert. Beispielsweise kann ein "LIST"-Block mit dem Listentyp "INFO" "ICOP" und "ICRD"-Blöcke enthalten, die Copyright- und Erstellungsdatumsinformationen bereitstellen. Die folgende Abbildung zeigt einen BLOCK "BESTEHT", der einen "LIST"-Block und einen anderen Unterchunk enthält (der "LIST"-Block enthält zwei Unterblöcke).

![Chunk, der ein Listenblöckenbild enthält](images/mmio2.gif)

Multimediadatei-E/A-Dienste enthalten zwei Funktionen, mit denen Sie zwischen Blöcken in einer PROTOKOLLDATEI navigieren können: [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) und [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend). Sie können diese Funktionen als Suchfunktionen auf hoher Ebene verwenden. Wenn Sie in einen Block absteigen, wird die Dateiposition auf das Datenfeld des Blockes festgelegt (8 Bytes vom Anfang des Blockes). Für die Blöcke "ERFOLGT" und "LIST" wird die Dateiposition auf den Speicherort festgelegt, der dem Formulartyp oder Listentyp folgt (12 Bytes vom Anfang des Blöckes). Wenn Sie aus einem Block aufsteigen, wird die Dateiposition auf den Speicherort nach dem Ende des Blockes festgelegt.

Um einen neuen Block zu erstellen, verwenden Sie die [**mmioCreateChunk-Funktion,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) um einen Blockheader an der aktuellen Position in einer geöffneten Datei zu schreiben. Die **MmioAscend-,** **mmioDescend-** und **mmioCreateChunk-Funktionen** verwenden die [**MMCKINFO-Struktur,**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) um Informationen zu DEN SEGMENTEN anzugeben und abzurufen.

 

 