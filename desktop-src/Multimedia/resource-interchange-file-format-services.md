---
title: Ressourcenaustausch-Dateiformatdienste
description: Ressourcenaustausch-Dateiformatdienste
ms.assetid: 8526794b-7b40-470f-94f7-935d7dbf9151
keywords:
- Multimediadatei-E/A, Ressourcenaustauschdateiformat (RESOURCE INTERCHANGE)
- Datei-E/A, Ressourcenaustauschdateiformat (FILE)
- Eingabe und Ausgabe (E/A), Ressourcenaustauschdateiformat (FORMAT)
- E/A (Eingabe und Ausgabe), Dateiformat für Ressourcenaustausch (Resource Interchange File Format,DATEIERWEITERUNG)
- mmioOpen-Funktion
- Resource Interchange File Format (ENDE)
- RAFF (Dateiformat für Ressourcenaustausch)
- ORGANISATIONS-E/A
- blockunk (blockunk)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5967165996b2a7fb9ed9b40c9a1f3c5608cd3bb4eb1e6cf05ae351f6ce6f2a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801927"
---
# <a name="resource-interchange-file-format-services"></a>Ressourcenaustausch-Dateiformatdienste

Das bevorzugte Format für Multimediadateien ist das RESOURCE INTERCHANGE-Dateiformat (Resource Interchange File Format). Die E/A-Funktionen für DIE -Datei funktionieren mit den grundlegenden gepufferten und ungepufferten Datei-E/A-Diensten. Sie können DIE-Dateien auf die gleiche Weise wie andere Dateitypen öffnen, lesen und schreiben. Ausführliche Informationen zu AVI finden Sie unter [AVIFile-Funktionen und -Makros.](avifile-functions-and-macros.md)

DIE-Dateien verwenden Vier-Zeichen-Codes, um Dateielemente zu identifizieren. Diese Codes sind 32-Bit-Mengen, die eine Sequenz von einem bis vier alphanumerischen ASCII-Zeichen darstellen, die rechts mit Leerzeichen auffüllt werden. Der Datentyp für Vier-Zeichen-Codes ist **FOURCC.** Verwenden Sie das [**Makro mmioFOURCC,**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) um vier Zeichen in einen Vier-Zeichen-Code zu konvertieren. Verwenden Sie die [**mmioStringToFOURCC-Funktion,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) um eine auf NULL terminierte Zeichenfolge in einen code mit vier Zeichen zu konvertieren.

Der grundlegende Baustein einerUNK-Datei ist ein *Block*. Ein Block ist eine logische Einheit von Multimediadaten, z. B. ein einzelner Frame in einem Videoclip. Jeder Block enthält die folgenden Felder:

-   Ein code mit vier Zeichen, der den Blockbezeichner ankn.)
-   Ein Doublewordwert, der die Größe des Datenmitglieds im Block ankn.)
-   Ein Datenfeld

In der folgenden Abbildung ist ein Block "UNK" dargestellt, der zwei Unterchunks enthält.

![-Block, der zwei Unterchunkbilder enthält](images/mmio1.gif)

Ein in einem anderen Block enthaltener Block ist ein *Unterchunk.* Die einzigen Chunks, die Unterchunks enthalten dürfen, sind diejenigen mit dem Blockbezeichner "BEZEICHNER" oder "LIST". Ein Block, der einen anderen Block enthält, wird als *übergeordneter Block bezeichnet.* Der erste Block in einerUNK-Datei muss ein BLOCK VOM-Block sein. Alle anderen Chunks in der Datei sind Teilchunks des BLOCKES.

DIE-Blocke enthalten ein zusätzliches Feld in den ersten vier Bytes des Datenfelds. Dieses zusätzliche Feld gibt den *Formulartyp des* Felds an. Der Formulartyp ist ein code mit vier Zeichen, der das Format der in der Datei gespeicherten Daten identifiziert. Microsoft Waveform-Audiodateien haben beispielsweise den Formulartyp "WAVE".

"LIST"-Chunks enthalten auch ein zusätzliches Feld in den ersten vier Bytes des Datenfelds. Dieses zusätzliche Feld enthält den *Listentyp* des Felds. Der Listentyp ist ein code mit vier Zeichen, der den Inhalt der Liste identifiziert. Beispielsweise kann ein List-Block mit dem Listentyp "INFO" die Chunks "ICOP" und "ICRD" enthalten, die Copyright- und Erstellungsdatumsinformationen bereitstellen. Die folgende Abbildung zeigt einen Block "UNK", der einen LIST-Block und einen anderen Unterchunk enthält (der List-Block enthält zwei Unterchunks).

![-Block, der ein Listen chunk-Bild enthält](images/mmio2.gif)

Multimediadatei-E/A-Dienste enthalten zwei Funktionen, die Sie verwenden können, um zwischen Blocken in einerÄND-Datei zu navigieren: [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) und [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend). Sie können diese Funktionen als Suchfunktionen auf hoher Ebene verwenden. Wenn Sie in einen Block absteigen, wird die Dateiposition auf das Datenfeld des Blockes festgelegt (8 Bytes ab dem Anfang des Blockes). Für DIE- und LIST-Chunks wird die Dateiposition auf den Speicherort festgelegt, der dem Formulartyp oder Listentyp folgt (12 Byte ab dem Anfang des Blockes). Wenn Sie aus einem Block aufsteigen, wird die Dateiposition auf den Speicherort nach dem Ende des Blockes festgelegt.

Um einen neuen Block zu erstellen, verwenden Sie die [**mmioCreateChunk-Funktion,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) um einen Blockheader an der aktuellen Position in einer geöffneten Datei zu schreiben. Die **MmioAscend-,** **mmioDescend-** und **mmioCreateChunk-Funktionen** verwenden die [**MMCKINFO-Struktur,**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) um Informationen zu "ÄND"-Blocken anzugeben und abzurufen.

 

 