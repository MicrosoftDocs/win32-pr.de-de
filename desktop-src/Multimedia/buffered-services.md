---
title: Gepufferte Dienste
description: Gepufferte Dienste
ms.assetid: 4816ab05-42fc-4c22-b753-8fd153d88c27
keywords:
- Multimedia-Datei-e/a, gepufferte Dienste
- Datei-e/a, gepufferte Dienste
- Eingabe und Ausgabe (e/a), gepufferte Dienste
- E/a (Eingabe und Ausgabe), gepufferte Dienste
- gepufferte e/a
- mmioopen-Funktion
- Interner e/a-Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d014ed765609dd43886cc7b33987f8fd5ac7e65a
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "103961047"
---
# <a name="buffered-services"></a>Gepufferte Dienste

Der meiste Aufwand in Datei-e/a tritt beim Zugriff auf das Medien Gerät auf. Wenn Sie viele kleine Informationsblöcke lesen oder schreiben, kann das Gerät für jeden Lese-oder Schreibvorgang viel Zeit für die Umstellung auf den physischen Speicherort auf den Medien aufwenden. In diesem Fall können Sie eine bessere Leistung erzielen, indem Sie gepufferte Datei-e/a-Dienste verwenden. Mit gepufferter e/a behält der Datei-e/a-Manager einen Zwischenpuffer bei, der größer ist als die Informationsblöcke, die Sie lesen oder schreiben. Es greift nur auf das Gerät zu, wenn der Puffer ausgefüllt oder auf den Datenträger geschrieben werden muss.

Bevor Sie die gepufferte Datei-e/a einrichten und verwenden, müssen Sie entscheiden, ob der Datei-e/a-Manager oder die Anwendung den Puffer zuordnen soll. Es ist einfacher, dem Datei-e/a-Manager den Puffer zuzuweisen. Sie können jedoch zulassen, dass die Anwendung den Puffer zuweist, wenn Sie direkt auf den Puffer zugreifen oder eine Speicherdatei öffnen möchten. Weitere Informationen zur Verwendung von Speicherdateien finden Sie unter [Durchführen von Speicherdatei-e/](performing-memory-file-i-o.md)a. Ein Beispiel für den direkten Zugriff auf einen e/a-Puffer finden Sie unter [zugreifen auf einen Datei-e/a-Puffer](accessing-a-file-i-o-buffer.md) .

Ein Puffer, der vom Datei-e/a-Manager zugeordnet wird, wird als interner e/a-Puffer bezeichnet. Wenn Sie eine Datei für gepufferte e/a-Vorgänge mit einem internen Puffer öffnen möchten, geben Sie das MMIO- \_ allocbuf-Flag an, wenn Sie die Datei mit der [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) -Funktion öffnen. Die folgende Abbildung zeigt den ursprünglichen Zustand des Datei-e/a-Puffers, nachdem eine Datei für einen gepufferten Lesevorgang geöffnet wurde. Die Pufferung ist transparent – Sie lesen und suchen, als wären Sie nicht gepufferte e/a-Vorgänge verwendet. Die **mmioopen** -Funktion hat pchnext und *pchendread* so festgelegt, dass Sie auf den Anfang des Datei-e/a-Puffers zeigen.

![Screenshot mit "pchendread" und "pchnext", die auf den Anfang des Datei-e/a-Puffers zeigen.](images/mmio7.gif)

Die folgende Abbildung zeigt den ursprünglichen Zustand des Datei-e/a-Puffers, nachdem eine Datei für einen gepufferten Schreibvorgang geöffnet wurde. Die **mmioopen** -Funktion hat **pchnext** auf den Anfang des Datei-e/a-Puffers und **pchendwrite** festgelegt, um auf das Ende des Puffers zu zeigen.

![Screenshot, der ' pchnext ' am Anfang des Datei-e/a-Puffers und ' pchendwrite ' am Ende anzeigt.](images/mmio11.gif)

Die Standardgröße des internen e/a-Puffers beträgt 8K. Wenn diese Größe nicht ausreicht, können Sie die [**mmiosetbuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) -Funktion verwenden, um die Puffergröße zu ändern. Sie können diese Funktion auch verwenden, um die Pufferung für eine Datei zu aktivieren, die für nicht gepufferte e/a-Vorgänge geöffnet wurde, oder um einen eigenen Puffer zur Verwendung als Speicherdatei bereitzustellen.

Mithilfe der [**mmioflush**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush) -Funktion können Sie erzwingen, dass der Inhalt eines e/a-Puffers auf den Datenträger geschrieben wird. Wenn Sie jedoch eine Datei mithilfe der [**mmioclose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) -Funktion schließen, müssen Sie **mmioflush** nicht zum leeren eines e/a-Puffers aufzurufen – die **mmioclose** -Funktion leert Sie automatisch. Wenn nicht genügend Speicherplatz zur Verfügung steht, kann **mmioflush** fehlschlagen, auch wenn die vorherigen Aufrufe der [**mmiowrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) -Funktion erfolgreich waren. Ebenso kann **mmioclose** fehlschlagen, wenn es den e/a-Puffer leert.

Anwendungen, die Leistungs abhängig sind, z. b. solche, die Daten in Echtzeit von einer CD-ROM streamen, können die Datei-e/a-Leistung optimieren, indem Sie direkt auf den e/a-Puffer zugreifen. Wenn Sie dies tun, sollten Sie vorsichtig vorgehen, da Sie einige der Sicherheitsvorkehrungen und die Fehlerüberprüfung des Datei-e/a-Managers umgehen.

Der Multimedia-Datei-e/a-Manager verwendet die [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur, um Zustandsinformationen zu einer geöffneten Datei beizubehalten. Sie verwenden drei Member in dieser Struktur, um den e/a-Puffer zu lesen und zu schreiben: **pchnext**, **pchendread** und **pchendwrite**. Der **pchnext** -Member verweist auf die nächste Position im Puffer, die gelesen oder geschrieben werden soll. Sie müssen diesen Member erhöhen, während Sie den Puffer lesen und schreiben. Der **pchendread** -Member identifiziert das letzte gültige Zeichen, das Sie aus dem Puffer lesen können. Ebenso identifiziert dieser Member den letzten Speicherort im Puffer, den Sie schreiben können. Genauer ist, zeigen sowohl **pchendread** als auch **pchendwrite** auf den Speicherort, der den letzten gültigen Daten im Puffer folgt. Verwenden Sie die Funktionen [**mmiogetinfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) und [**mmiosetinfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) , um Zustandsinformationen zum Datei-e/a-Puffer abzurufen und festzulegen. Die folgende Abbildung zeigt den Status des e/a-Puffers, nachdem die Anwendung während eines Lesevorgangs **mmioadvance** aufgerufen hat. Die **mmioadvance** -Funktion füllt den Puffer auf und legt den **pchendread** -Zeiger auf das Ende des Puffers fest.

![Screenshot, der "pchnext" am Anfang des Datei-e/a-Puffers und "pchendread" am Ende anzeigt.](images/mmio8.gif)

In der folgenden Abbildung liest die Anwendung aus dem e/a-Puffer an dem Speicherort, der von **pchnext** angegeben wird, und verschiebt den Zeiger.

![Screenshot, der ' pchnext ' in der Mitte des Datei-e/a-Puffers und ' pchendread ' am Ende anzeigt.](images/mmio9.gif)

Ebenso schreibt die Anwendung bei einem Schreibvorgang in den e/a-Puffer und erhöht den **pchnext** -Zeiger, wie in der folgenden Abbildung dargestellt.

![Screenshot, der ' pchnext ' in der Mitte des Datei-e/a-Puffers und ' pchendwrite ' am Ende anzeigt.](images/mmio12.gif)

Nachdem die Anwendung den Puffer ausgefüllt hat, wird **mmioadvance** aufgerufen, um den Puffer auf den Datenträger zu leeren. Die **mmioadvance** -Funktion setzt **pchnext** auf den Anfang des Puffers zurück, wie in der folgenden Abbildung dargestellt.

![Screenshot, der ' pchnext ' am Anfang des Datei-E/a-Puffers, den Puffer in der Mitte von E O F und ' pchendwrite ' am Ende des Puffers anzeigt.](images/mmio13.gif)

Wenn Sie das Ende des e/a-Puffers erreichen, müssen Sie den Puffer so verschieben, dass er vom Datenträger ausgefüllt wird, wenn Sie ihn lesen oder auf den Datenträger leeren, wenn Sie schreiben. Verwenden Sie die [**mmioadvance**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance) -Funktion, um einen e/a-Puffer zu verbessern. Um einen e/a-Puffer von der Festplatte zu füllen, verwenden Sie **mmioadvance** mit dem MMIO- \_ leseflag. Wenn nicht genügend Daten in der Datei vorhanden sind, um den Puffer auszufüllen, verweist der **pchendread** -Member der **mmioinfo** -Struktur auf den Speicherort, der dem letzten gültigen Byte im Puffer folgt. Um einen Puffer auf den Datenträger zu leeren, legen Sie das MMIO \_ -Flag "Dirty" im **dwFlags** -Member der **mmioinfo** -Struktur fest, und geben Sie dann **mmioadvance** mit dem MMIO- \_ Schreib Flag ein.

Beispielsweise legt die **mmioadvance** -Funktion während eines Lesevorgangs **pchendread** so fest, dass Sie auf das Ende gültiger Daten im Puffer zeigt, wie in der folgenden Abbildung dargestellt.

![Screenshot, der ' pchnext ' am Anfang des Datei-E/a-Puffers, den Puffer am Ende von E O F und ' pchendread ' am Ende des Puffers anzeigt.](images/mmio10.gif)

Ebenso Ruft die Anwendung während eines Schreibvorgangs **mmioadvance** auf, um den Puffer zu leeren und **pchnext** an das Ende der gültigen Daten im Puffer zu verschieben, wie in der folgenden Abbildung dargestellt.

![Datei-e/a-Puffer Image](images/mmio14.gif)

 

 