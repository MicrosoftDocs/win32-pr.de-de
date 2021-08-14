---
title: Gepufferte Dienste
description: Gepufferte Dienste
ms.assetid: 4816ab05-42fc-4c22-b753-8fd153d88c27
keywords:
- Multimediadatei-E/A, gepufferte Dienste
- Datei-E/A, gepufferte Dienste
- Eingabe und Ausgabe (E/A), gepufferte Dienste
- E/A (Eingabe und Ausgabe), gepufferte Dienste
- Gepufferte E/A
- mmioOpen-Funktion
- Interner E/A-Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67f8e7c11dbc90f7090bc8fcee114ebfac79f9bd54d834203f4b8e7bf893f591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117989380"
---
# <a name="buffered-services"></a>Gepufferte Dienste

Der größte Teil des Mehraufwands bei Datei-E/A tritt beim Zugriff auf das Mediengerät auf. Wenn Sie viele kleine Informationsblöcke lesen oder schreiben, kann das Gerät viel Zeit damit verbringen, für jeden Lese- oder Schreibvorgang an den physischen Speicherort auf den Medien zu verschieben. In diesem Fall können Sie eine bessere Leistung erzielen, indem Sie gepufferte Datei-E/A-Dienste verwenden. Bei gepufferten E/A-Daten verwaltet der Datei-E/A-Manager einen Zwischenpuffer, der größer als die Informationsblöcke ist, die Sie lesen oder schreiben. Sie greifen nur dann auf das Gerät zu, wenn der Puffer von dem Datenträger gefüllt oder auf den Datenträger geschrieben werden muss.

Bevor Sie gepufferte Datei-E/A einrichten und verwenden, müssen Sie entscheiden, ob der Datei-E/A-Manager oder die Anwendung den Puffer zuordnen soll. Es ist einfacher, den Datei-E/A-Manager den Puffer zuordnen zu lassen. Sie können es der Anwendung jedoch gestatten, den Puffer zu reservieren, wenn Sie direkt auf den Puffer zugreifen oder eine Speicherdatei öffnen möchten. Weitere Informationen zur Verwendung von Speicherdateien finden Sie unter [Ausführen von Speicherdatei-E/A.](performing-memory-file-i-o.md) Ein Beispiel für den direkten Zugriff auf einen E/A-Puffer finden Sie unter [Zugreifen auf einen Datei-E/A-Puffer.](accessing-a-file-i-o-buffer.md)

Ein vom Datei-E/A-Manager zugeordneter Puffer wird als interner E/A-Puffer bezeichnet. Um eine Datei für gepufferte E/A mithilfe eines internen Puffers zu öffnen, geben Sie das MMIO ALLOCBUF-Flag an, wenn Sie die Datei mit der \_ [**mmioOpen-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) öffnen. Die folgende Abbildung zeigt den Anfangszustand des Datei-E/A-Puffers, nachdem eine Datei für einen gepufferten Lesevorgang geöffnet wurde. Die Pufferung ist transparent– Sie lesen und suchen, als würden Sie ungepufferte E/A verwenden. Die **mmioOpen-Funktion** hat pchNext und *pchEndRead* so festgelegt, dass sie auf den Anfang des Datei-E/A-Puffers zeigen.

![Screenshot: "pchEndRead" und "pchNext" zeigen auf den Anfang des Datei-E/A-Puffers.](images/mmio7.gif)

Die folgende Abbildung zeigt den Anfangszustand des Datei-E/A-Puffers, nachdem eine Datei für einen gepufferten Schreibvorgang geöffnet wurde. Die **mmioOpen-Funktion** hat **pchNext** so festgelegt, dass auf den Anfang des Datei-E/A-Puffers und **pchEndWrite** auf das Ende des Puffers zeigen.

![Screenshot: "pchNext" am Anfang des Datei-E/A-Puffers und "pchEndWrite" am Ende](images/mmio11.gif)

Die Standardgröße des internen E/A-Puffers beträgt 8.000. Wenn diese Größe nicht ausreicht, können Sie die [**mmioSetBuffer-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) verwenden, um die Puffergröße zu ändern. Sie können diese Funktion auch verwenden, um die Pufferung für eine Datei zu aktivieren, die für ungepufferte E/A geöffnet wurde, oder um einen eigenen Puffer für die Verwendung als Speicherdatei zur Verfügung zu haben.

Sie können erzwingen, dass der Inhalt eines E/A-Puffers mithilfe der [**mmioFlush-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush) auf den Datenträger geschrieben wird. Wenn Sie jedoch eine Datei mithilfe der [**mmioClose-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) schließen, müssen Sie **mmioFlush** nicht aufrufen, um einen E/A-Puffer zu leeren– die **mmioClose-Funktion** leert ihn automatisch. Wenn der Speicherplatz nicht mehr verfügbar ist, kann **mmioFlush** fehlschlagen, selbst wenn die vorherigen Aufrufe der [**mmioWrite-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) erfolgreich waren. Auf ähnliche Weise **kann mmioClose** fehlschlagen, wenn der E/A-Puffer geleert wird.

Anwendungen, die leistungsempfindlich sind, z. B. solche, die Daten in Echtzeit von einer CD-ROM streamen, können die E/A-Leistung von Dateien optimieren, indem sie direkt auf den E/A-Puffer zugreifen. Wenn Sie sich dafür entscheiden, sollten Sie vorsichtig sein, da Sie einige der Sicherheitsvorkehrungen und Fehlerüberprüfungen umgehen, die vom Datei-E/A-Manager bereitgestellt werden.

Der Multimediadatei-E/A-Manager verwendet die [**MMIOINFO-Struktur,**](/previous-versions//dd757322(v=vs.85)) um Zustandsinformationen zu einer geöffneten Datei zu verwalten. Sie verwenden drei Member in dieser Struktur, um den E/A-Puffer zu lesen und zu schreiben: **pchNext,** **pchEndRead** und **pchEndWrite**. Der **pchNext-Member** zeigt auf die nächste Position im Puffer, die gelesen oder geschrieben werden soll. Sie müssen diesen Member erhöhen, wenn Sie den Puffer lesen und schreiben. Das **pchEndRead-Member** identifiziert das letzte gültige Zeichen, das Sie aus dem Puffer lesen können. Ebenso identifiziert dieser Member die letzte Position im Puffer, die Sie schreiben können. Genauer gesagt zeigen **sowohl pchEndRead** als auch **pchEndWrite** auf den Speicherort, der auf die letzten gültigen Daten im Puffer folgt. Verwenden Sie [**die Funktionen mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) und [**mmioSetInfo,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) um Zustandsinformationen zum Datei-E/A-Puffer abzurufen und zu festlegen. Die folgende Abbildung zeigt den Status des E/A-Puffers, nachdem die Anwendung **mmioAdvance** während eines Lesevorganges aufruft. Die **mmioAdvance-Funktion** füllt den Puffer aus und legt den **pchEndRead-Zeiger** auf das Ende des Puffers fest.

![Screenshot: "pchNext" am Anfang des Datei-E/A-Puffers und "pchEndRead" am Ende](images/mmio8.gif)

In der folgenden Abbildung liest die Anwendung aus dem E/A-Puffer an der von **pchNext** angegebenen Position und zeigt den Zeiger an.

![Screenshot: "pchNext" in der Mitte des Datei-E/A-Puffers und "pchEndRead" am Ende](images/mmio9.gif)

Analog dazu schreibt die Anwendung bei einem Schreibvorgang in den E/A-Puffer und gibt den **pchNext-Zeiger** weiter, wie in der folgenden Abbildung dargestellt.

![Screenshot: "pchNext" in der Mitte des Datei-E/A-Puffers und "pchEndWrite" am Ende](images/mmio12.gif)

Nachdem die Anwendung den Puffer auffüllt, ruft sie **mmioAdvance** auf, um den Puffer auf den Datenträger zu leeren. Die **mmioAdvance-Funktion** setzt **pchNext** zurück, um auf den Anfang des Puffers zu zeigen, wie in der folgenden Abbildung dargestellt.

![Screenshot: "pchNext" am Anfang des Datei-E/A-Puffers, der Puffer in der Mitte von E O F und "pchEndWrite" am Ende des Puffers.](images/mmio13.gif)

Wenn Sie das Ende des E/A-Puffers erreichen, müssen Sie den Puffer so vorn ansetzen, dass er vom Datenträger auffüllt, wenn Sie ihn lesen, oder ihn beim Schreiben auf den Datenträger leeren. Verwenden Sie die [**mmioAdvance-Funktion,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance) um einen E/A-Puffer nach vorn zu setzen. Verwenden Sie **mmioAdvance** mit dem MMIO READ-Flag, um einen E/A-Puffer vom \_ Datenträger zu füllen. Wenn nicht genügend Daten in der Datei vorhanden sind, um den Puffer zu füllen, zeigt das **pchEndRead-Element** der **MMIOINFO-Struktur** auf den Speicherort nach dem letzten gültigen Byte im Puffer. Um einen Puffer auf den Datenträger zu leeren, legen Sie das MMIO DIRTY-Flag im \_ **dwFlags-Element** der **MMIOINFO-Struktur** fest, und rufen Sie **dann mmioAdvance** mit dem MMIO \_ WRITE-Flag auf.

Während eines Lesevorgang legt die **mmioAdvance-Funktion** beispielsweise **pchEndRead** so fest, dass er auf das Ende gültiger Daten im Puffer zeigt, wie in der folgenden Abbildung dargestellt.

![Screenshot: "pchNext" am Anfang des Datei-E/A-Puffers, der Puffer am Ende der E O F und "pchEndRead" am Ende des Puffers.](images/mmio10.gif)

Entsprechend ruft die Anwendung während eines Schreibvorgang **mmioAdvance** auf, um den Puffer zu leeren und **pchNext** an das Ende gültiger Daten im Puffer zu übertragen, wie in der folgenden Abbildung dargestellt.

![Datei-E/A-Pufferbild](images/mmio14.gif)

 

 