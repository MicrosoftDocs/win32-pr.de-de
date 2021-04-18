---
title: Dienste für den Ressourcenaustausch-Datei Format
description: Dienste für den Ressourcenaustausch-Datei Format
ms.assetid: 8526794b-7b40-470f-94f7-935d7dbf9151
keywords:
- Multimedia-Datei-e/a, Ressourcenaustausch Dateiformat (Riff)
- Datei-e/a, Ressourcenaustausch Dateiformat (Riff)
- Eingabe und Ausgabe (e/a), Ressourcenaustausch Dateiformat (Riff)
- E/a (Eingabe und Ausgabe), Format der Ressourcenaustausch Datei (Riff)
- mmioopen-Funktion
- Format der Ressourcenaustausch Datei (Riff)
- Riff (Ressourcenaustausch-Dateiformat)
- Riff-e/a
- Riff Block
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cca3792ccded248951065c7b69f2e50d27e0ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314679"
---
# <a name="resource-interchange-file-format-services"></a>Dienste für den Ressourcenaustausch-Datei Format

Das bevorzugte Format für Multimedia-Dateien ist das Ressourcenaustausch Dateiformat (Riff). Die Datei-e/a-Funktionen der Riff Datei funktionieren mit den grundlegenden gepufferten und nicht gepufferten Datei-e/a Sie können die Riff Dateien auf die gleiche Weise wie andere Dateitypen öffnen, lesen und schreiben. Ausführliche Informationen zu Riff finden Sie unter [avifile-Funktionen und-Makros](avifile-functions-and-macros.md).

In den Riff Dateien werden vier Zeichen Codes verwendet, um Dateielemente zu identifizieren. Diese Codes sind 32-Bit-Mengen, die eine Sequenz von einem bis vier alphanumerischen ASCII-Zeichen darstellen, die auf der rechten Seite mit Leerzeichen aufgefüllt werden. Der Datentyp für vier Zeichen Codes ist **FourCC**. Verwenden Sie das [**mmiofourcc**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) -Makro, um vier Zeichen in einen vierstelligen Code zu konvertieren. Verwenden Sie die [**mmiostringdefourcc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) -Funktion, um eine mit NULL endende Zeichenfolge in einen aus vier Zeichen bestehende Code zu konvertieren.

Der grundlegende *Baustein einer Riff Datei ist ein Segment*. Ein Block ist eine logische Einheit von Multimedia-Daten, wie z. b. einem einzelnen Frame in einem Videoclip. Jeder Block enthält die folgenden Felder:

-   Ein aus vier Zeichen bestehende Code, der den Block Bezeichner angibt.
-   Ein Double Word-Wert, der die Größe des Datenelements im Block angibt.
-   Ein Datenfeld

Die folgende Abbildung zeigt einen "Riff"-Block, der zwei Teilsegmente enthält.

![der Riff Block, der zwei unter Segmente enthält.](images/mmio1.gif)

Ein Block, der in einem anderen Block enthalten ist, ist ein *Teil*. Die einzigen Blöcke, die Teilsegmente enthalten dürfen, sind diejenigen mit dem Block Bezeichner "Riff" oder "List". Ein Block, der einen anderen Block enthält, wird als über *geordneter* Block bezeichnet. Der erste Block in einer Riff Datei muss ein "Riff"-Block sein. Alle anderen Blöcke in der Datei sind Teilsegmente des "Riff"-Blocks.

"Riff"-Blöcke enthalten ein zusätzliches Feld in den ersten vier Bytes des Daten Felds. Dieses zusätzliche Feld stellt den *Formulartyp* des Felds bereit. Der Formulartyp ist ein aus vier Zeichen bestehende Code, der das Format der in der Datei gespeicherten Daten identifiziert. Beispielsweise weisen Microsoft Waveform-Audiodateien den Formulartyp "Wave" auf.

"List"-Blöcke enthalten auch ein zusätzliches Feld in den ersten vier Bytes des Daten Felds. Dieses zusätzliche Feld enthält den *Listentyp* des Felds. Der Listentyp ist ein aus vier Zeichen bestehende Code, der den Inhalt der Liste identifiziert. Beispielsweise kann ein "List"-Block mit dem Listentyp "Info" "iCop"-und "ICRD"-Blöcke enthalten, die Informationen zu Urheberrechten und Erstellungsdatum enthalten. In der folgenden Abbildung ist ein "Riff"-Block dargestellt, der einen "List"-Block und einen anderen Unterbereich enthält (der "List"-Block enthält zwei Teilsegmente).

![der Riff Block, der ein Listen Segment Bild enthält.](images/mmio2.gif)

Multimedia-Datei-e/a-Dienste enthalten zwei Funktionen, die Sie verwenden können, um zwischen Blöcken in einer Riff Datei zu navigieren: [**mmioascend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) und [**mmioabstieg**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend). Sie können diese Funktionen als Suchfunktionen auf hoher Ebene verwenden. Wenn Sie in einen Block absteigen, wird die Dateiposition auf das Datenfeld des Blocks (8 Bytes vom Anfang des Blocks) festgelegt. Für die Blöcke "Riff" und "List" wird die Dateiposition auf den Speicherort festgelegt, der auf den Typ oder den Auflistungstyp folgt (12 Bytes vom Anfang des Blocks). Wenn Sie aus einem Block aufsteigen, wird die Dateiposition auf den Speicherort festgelegt, der dem Ende des Blocks folgt.

Um einen neuen Block zu erstellen, verwenden Sie die [**mmiokreatechunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) -Funktion, um einen Block Header an der aktuellen Position in einer geöffneten Datei zu schreiben. Die Funktionen **mmioascend**, **mmiodescenund** **mmiokreatechunk** verwenden die [**mmckinfo**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) -Struktur zum angeben und Abrufen von Informationen zu "Riff"-Blöcken.

 

 