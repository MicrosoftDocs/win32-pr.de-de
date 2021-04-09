---
description: Die globalen und lokalen Funktionen werden für das Portieren aus 16-Bit-Code oder für die Beibehaltung der Quell Code Kompatibilität mit 16-Bit-Fenstern unterstützt.
ms.assetid: 97707ce7-4c65-4d0e-ba69-47fdaee73a9b
title: Globale und lokale Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf356647f92f0e7d82e914a91020c438363ff082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862424"
---
# <a name="global-and-local-functions"></a>Globale und lokale Funktionen

Die globalen und lokalen Funktionen werden für das Portieren aus 16-Bit-Code oder für die Beibehaltung der Quell Code Kompatibilität mit 16-Bit-Fenstern unterstützt. Beginnend mit 32-Bit-Fenstern werden die globalen und lokalen Funktionen als Wrapper Funktionen implementiert, die die entsprechenden [Heap Funktionen](heap-functions.md) mithilfe eines Handles für den Standard Heap des Prozesses aufzurufen. Daher haben die globalen und lokalen Funktionen mehr Aufwand als andere Speicherverwaltungsfunktionen.

Die [Heap Funktionen](heap-functions.md) bieten mehr Features und Kontrolle als die globalen und lokalen Funktionen. Neue Anwendungen sollten die Heap Funktionen verwenden, es sei denn, in der Dokumentation wird ausdrücklich angegeben, dass eine globale oder lokale Funktion verwendet werden soll. Einige Windows-Funktionen weisen z. b. Arbeitsspeicher zu, der mit [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree)freigegeben werden muss, und die globalen Funktionen werden weiterhin mit dynamischer Datenaustausch (DDE), den Zwischenablage Funktionen und OLE-Datenobjekten verwendet. Eine umfassende Liste der globalen und lokalen Funktionen finden Sie in der Tabelle unter [Speicherverwaltungsfunktionen](memory-management-functions.md).

Die Windows-Speicherverwaltung stellt keinen separaten lokalen Heap und keinen globalen Heap bereit, wie es bei 16-Bit-Windows der gibt. Folglich sind die globalen und lokalen Funktions Familien gleichwertig, und die Entscheidung zwischen Ihnen ist eine persönliche Einstellung. Beachten Sie, dass die Änderung von einem 16-Bit-segmentierten Speichermodell zu einem virtuellen 32-Bit-Speichermodell einige der zugehörigen globalen und lokalen Funktionen und deren Optionen unnötig oder bedeutungslos gemacht hat. Beispielsweise gibt es keine Near-und Far-Zeiger mehr, da sowohl lokale als auch globale Zuordnungen 32-Bit-virtuelle Adressen zurückgeben.

Arbeitsspeicher Objekte, die von [**globalzuordc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) und [**localzuc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) zugeordnet werden, befinden sich in privaten, per Commit übergebenen Seiten mit Lese-/Schreibzugriff, auf die von anderen Prozessen Arbeitsspeicher, der mithilfe von **globalbelegc** mit **GMEM \_ ddeshare** belegt wird, wird nicht global gemeinsam genutzt, da er sich in 16-Bit-Fenstern befindet. Dieser Wert hat keine Auswirkung und ist nur aus Gründen der Kompatibilität verfügbar. Anwendungen, die gemeinsam genutzten Arbeitsspeicher für andere Zwecke benötigen, müssen Datei Zuordnung-Objekte verwenden. Mehrere Prozesse können eine Ansicht desselben Datei Zuordnungs Objekts zuordnen, um benannten gemeinsam genutzten Speicher bereitzustellen. Weitere Informationen finden Sie unter [Datei Zuordnung](file-mapping.md).

Speicher Belegungen werden nur durch den verfügbaren physischen Speicher beschränkt, einschließlich des Speichers in der Auslagerungs Datei auf dem Datenträger. Wenn Sie einen festgelegten Arbeitsspeicher zuordnen, geben [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) und [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) einen Zeiger zurück, der vom aufrufenden Prozess sofort für den Zugriff auf den Arbeitsspeicher verwendet werden kann. Wenn Sie Arbeitsspeicher zuweisen, ist der Rückgabewert ein handle. Um einen Zeiger auf ein bewegliches Speicher Objekt zu erhalten, verwenden Sie die Funktionen [**GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock) und [**locbelegck**](/windows/desktop/api/WinBase/nf-winbase-locallock) .

Die tatsächliche Größe des belegten Speichers kann größer als die angeforderte Größe sein. Verwenden Sie die [**globalsize**](/windows/desktop/api/WinBase/nf-winbase-globalsize) -oder [**localsize**](/windows/desktop/api/WinBase/nf-winbase-localsize) -Funktion, um die tatsächliche Anzahl der zugeordneten Bytes zu bestimmen. Wenn die zugeordnete Menge größer ist als der angeforderte Betrag, kann der Prozess den gesamten Betrag verwenden.

Die Funktionen [**globalrebelegc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc) und [**localrezuzuordnungs**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) ändern die Größe oder die Attribute eines Speicher Objekts, das von [**globalbelegc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) und [**localbelegc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)zugeordnet wird. Die Größe kann zunehmen oder verringern.

Die [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree) -und [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) -Funktionen geben Arbeitsspeicher frei, der von [**globalzuordc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**localbelegc**](/windows/desktop/api/WinBase/nf-winbase-localalloc), [**globalrebelegc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc)oder [**localrebelegc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc)zugeordnet wird. Um das angegebene Speicher Objekt zu verwerfen, ohne das Handle ungültig zu machen, verwenden Sie die [**globaldiscard**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard) -oder [**localdiscard**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) -Funktion. Das Handle kann später von **GlobalRealloc** oder **LocalReAlloc** verwendet werden, um einen neuen Speicherblock zuzuordnen, der dem gleichen Handle zugeordnet ist.

Um Informationen über ein angegebenes Speicher Objekt zurückzugeben, verwenden Sie die [**globalflags**](/windows/desktop/api/WinBase/nf-winbase-globalflags) -oder [**localflags**](/windows/desktop/api/WinBase/nf-winbase-localflags) -Funktion. Die Informationen enthalten die Sperr Anzahl des Objekts und zeigen an, ob das Objekt verworfen werden kann oder bereits verworfen wurde. Verwenden Sie die [**globalhandle**](/windows/desktop/api/WinBase/nf-winbase-globalhandle) -oder [**localhandle**](/windows/desktop/api/WinBase/nf-winbase-localhandle) -Funktion, um ein Handle für das Speicher Objekt zurückzugeben, das einem angegebenen Zeiger zugeordnet ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vergleichen von Speicher Belegungs Methoden](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 
