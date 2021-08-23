---
description: Verarbeiten von Daten
ms.assetid: 823615df-ce50-4e20-957a-f83d3be66658
title: Verarbeiten von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff417b3e37c3be43c42fd0cf8545bce6bfb00caa361d34d8044d690169f7c97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748170"
---
# <a name="processing-data"></a>Verarbeiten von Daten

**Analyse von Mediendaten**

Wenn Ihr Filter Mediendaten analysiert, sollten Sie Headern oder anderen selbstbeschreibenden Daten im Inhalt nicht vertrauen. Vertrauenswürdige Größenwerte, die in AVI- oder MPEG-Paketen angezeigt werden, sind beispielsweise nicht vertrauenswürdig. Häufige Beispiele für diese Art von Fehler sind:

-   Lesen *von N* Bytes von Daten, wobei der Wert *von N* aus dem Inhalt stammt, ohne *N* mit der tatsächlichen Größe des Puffers zu überprüfen.
-   Springen zu einem Byteoffset innerhalb eines Puffers, ohne zu überprüfen, ob der Offset innerhalb des Puffers liegt.

Eine weitere häufige Fehlerklasse besteht darin, keine Formatbeschreibungen zu überprüfen, die im Inhalt gefunden werden. Beispiel:

-   Auf [**eine BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) kann eine Farbtabelle folgen. Die **BITMAPINFO-Struktur** wird als **BITMAPINFOHEADER-Struktur** definiert, gefolgt von einem Array von **RGBQUAD-Werten,** aus denen die Farbtabelle besteht. Die Größe des Arrays wird durch den Wert von **biClrUsed bestimmt.** Kopieren Sie niemals eine Farbtabelle in **bitmapinfo,** ohne zuerst die Größe des Puffers zu überprüfen, der der **BITMAPINFO-Struktur zugeordnet** wurde.
-   An [**eine WAVEFORMATEX-Struktur**](/previous-versions/dd757713(v=vs.85)) werden möglicherweise zusätzliche Formatinformationen angefügt. Der **cbSize-Member** gibt die Größe der zusätzlichen Informationen an.

Während der Stecknadelverbindung sollte ein Filter überprüfen, ob alle Formatstrukturen wohlgeformt sind und sinnvolle Werte enthalten. Falls nicht, lehnen Sie die Verbindung ab. Achten Sie im Code, der die Formatstruktur überprüft, besonders auf arithmetischen Überlauf. In einem **BITMAPINFOHEADER** sind z. B. die Breite  und Höhe 32-Bit-Werte, aber die Bildgröße (die eine Funktion des Produkts der beiden ist) ist nur ein **DWORD-Wert.**

Wenn formatierte Daten aus der Quelle größer als der zugeordnete Puffer sind, sollten Sie die Quelldaten nicht abschneiden, um sie in den Puffer zu kopieren. Dadurch kann eine -Struktur erstellt werden, deren implizite Größe größer als die tatsächliche Größe ist. Beispielsweise kann ein Bitmapheader eine Palettentabelle angeben, die nicht mehr vorhanden ist. Verwenden Sie stattdessen den Puffer neu, oder führen Sie einfach zu einem Fehler bei der Verbindung.

**Fehler während des Streamings**

Wenn das Diagramm ausgeführt wird und Ihr Filter falsch formatierten Inhalt empfängt, sollte er das Streaming beenden. Gehen Sie wie folgt vor:

-   Gibt einen Fehlercode von **Receive zurück.**
-   Rufen [**Sie IPin::EndOfStream für**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) den Downstreamfilter auf.
-   Rufen [**Sie CBaseFilter::NotifyEvent auf,**](cbasefilter-notifyevent.md) um ein [**EC \_ ERRORABORT-Ereignis**](ec-errorabort.md) zu veröffentlichen.

**Formatänderungen**

Es gibt mehrere Mechanismen für Filter zum Ändern von Formaten während des Streams. Jeder dieser Schritte umfasst mehr als einen Schritt, wodurch das Potenzial für falsche Akzeptanzen entsteht. Wenn Ihr Filter eine Anforderung für eine dynamische Formatänderung erhält, muss er die Anforderung entweder ablehnen oder das neue Format beim Eintreffen nicht mehr verwenden. Wechseln Sie auf ähnliche Weise niemals zwischen Formaten, es sei denn, der andere Filter stimmt zu. Weitere Informationen finden Sie unter [Dynamische Formatänderungen.](dynamic-format-changes.md)

 

 
