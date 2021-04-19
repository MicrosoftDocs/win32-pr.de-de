---
description: Verarbeiten von Daten
ms.assetid: 823615df-ce50-4e20-957a-f83d3be66658
title: Verarbeiten von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbece449df36c2de88414f313d477b8a16ba896
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343138"
---
# <a name="processing-data"></a>Verarbeiten von Daten

**Die Mediendaten werden verarbeitet.**

Wenn der Filtermedien Daten analysiert, dürfen Sie keine Header oder anderen selbst beschreibenden Daten im Inhalt als vertrauenswürdig einstufen. Geben Sie z. b. keine Vertrauenswürdigkeit von Größen Werten an, die in AVI-Riff Blöcken oder MPEG-Paketen angezeigt werden. Häufige Beispiele für diese Art von Fehler sind:

-   Lesen von *n* Bytes an Daten, bei denen der Wert von *N* aus dem Inhalt stammt, ohne die tatsächliche Puffergröße zu *überprüfen.*
-   Springen zu einem Byte Offset innerhalb eines Puffers, ohne zu überprüfen, ob der Offset innerhalb des Puffers liegt.

Eine weitere häufige Fehler Klasse besteht darin, dass die im Inhalt gefundenen Format Beschreibungen nicht überprüft werden. Beispiel:

-   Auf eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur kann eine Farbtabelle folgen. Die **BitmapInfo** -Struktur wird als **BITMAPINFOHEADER** -Struktur, gefolgt von einem Array von **rgbquad** -Werten, die die Farbtabelle bilden, definiert. Die Größe des Arrays wird durch den Wert von " **biclrused**" bestimmt. Kopieren Sie niemals eine Farbtabelle in eine **BitmapInfo** , ohne zuvor die Größe des Puffers zu überprüfen, der für die **BitmapInfo** -Struktur reserviert wurde.
-   Einer [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur können zusätzliche Formatierungsinformationen an die Struktur angehängt werden. Der **CBSIZE** -Member gibt die Größe der zusätzlichen Informationen an.

Während der Pin-Verbindung sollte ein Filter überprüfen, ob alle Format Strukturen wohl geformt sind und sinnvolle Werte enthalten. Falls nicht, lehnen Sie die Verbindung ab. Im Code, der die Format Struktur überprüft, achten Sie besonders auf den arithmetischen Überlauf. In einem **BITMAPINFOHEADER** sind z. b. Breite und Höhe 32 **-Bit-** Werte, aber die Bildgröße (die eine Funktion des Produkts zweier ist) ist nur ein **DWORD** -Wert.

Wenn die Format Daten aus der Quelle größer sind als der zugeordnete Puffer, kürzen Sie die Quelldaten nicht, um Sie in den Puffer zu kopieren. Dadurch kann eine Struktur erstellt werden, deren implizite Größe größer ist als die tatsächliche Größe. Beispielsweise kann ein Bitmapheader eine Palettentabelle angeben, die nicht mehr vorhanden ist. Ordnen Sie stattdessen den Puffer neu zu, oder führen Sie einfach die Verbindung aus.

**Fehler beim Streaming**

Wenn das Diagramm ausgeführt wird und der Filter falsch formatierten Inhalt empfängt, sollte das Streaming beendet werden. Führen Sie folgende Schritte aus:

-   Gibt einen Fehlercode von **Receive** zurück.
-   Nennen Sie [**IPin:: EndOfStream für den downstreamfilter**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .
-   Aufrufen von [**cbasefilter:: notifyEvent**](cbasefilter-notifyevent.md) zum Veröffentlichen eines [**EC \_ errorabort**](ec-errorabort.md) -Ereignisses.

**Formatieren von Änderungen**

Für Filter zum Ändern von Formaten in der Mitte des Streams sind mehrere Mechanismen vorhanden. Jede dieser Komponenten umfasst mehr als einen Schritt, der das Potenzial für falsche Annahmen erzeugt. Wenn der Filter eine Anforderung für eine Änderung des dynamischen Formats erhält, muss die Anforderung entweder abgelehnt werden, oder das neue Format wird beim Eintreffen berücksichtigt. Ändern Sie auch nie Formate, es sei denn, der andere Filter stimmt überein. Weitere Informationen finden Sie unter [dynamische Format Änderungen](dynamic-format-changes.md).

 

 
