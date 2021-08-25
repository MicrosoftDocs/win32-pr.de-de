---
description: Die globalen und lokalen Funktionen werden zum Portieren von 16-Bit-Code oder zur Aufrechterhaltung der Quellcodekompatibilität mit 16-Bit-Windows unterstützt.
ms.assetid: 97707ce7-4c65-4d0e-ba69-47fdaee73a9b
title: Globale und lokale Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71d7832f90a420e6be87fe6599cc8c9e4722ddf45b789663ed9b39eab4e5449
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869694"
---
# <a name="global-and-local-functions"></a>Globale und lokale Funktionen

Die globalen und lokalen Funktionen werden zum Portieren von 16-Bit-Code oder zur Aufrechterhaltung der Quellcodekompatibilität mit 16-Bit-Windows unterstützt. Ab 32-Bit-Windows werden die globalen und lokalen Funktionen als Wrapperfunktionen implementiert, die die entsprechenden [Heapfunktionen](heap-functions.md) mithilfe eines Handles für den Standardheap des Prozesses aufrufen. Daher haben die globalen und lokalen Funktionen einen größeren Mehraufwand als andere Speicherverwaltungsfunktionen.

Die [Heapfunktionen](heap-functions.md) bieten mehr Features und Kontrolle als die globalen und lokalen Funktionen. Neue Anwendungen sollten die Heapfunktionen verwenden, es sei denn, in der Dokumentation ist ausdrücklich angegeben, dass eine globale oder lokale Funktion verwendet werden soll. Beispielsweise weisen einige Windows-Funktionen Arbeitsspeicher zu, der mit [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree)freigegeben werden muss, und die globalen Funktionen werden weiterhin mit dynamische Daten Exchange (DDE), den Zwischenablagefunktionen und OLE-Datenobjekten verwendet. Eine vollständige Liste der globalen und lokalen Funktionen finden Sie in der Tabelle unter [Speicherverwaltungsfunktionen.](memory-management-functions.md)

Windows Speicherverwaltung bietet keinen separaten lokalen Heap und globalen Heap, wie dies Windows mit 16-Bit-Windows. Daher sind die globalen und lokalen Funktionsfamilien gleichwertig, und die Wahl zwischen ihnen ist eine Frage der persönlichen Präferenz. Beachten Sie, dass die Änderung von einem segmentierten 16-Bit-Speichermodell in ein 32-Bit-Modell für virtuellen Speicher einige der zugehörigen globalen und lokalen Funktionen und deren Optionen unnötig oder bedeutungslos gemacht hat. Es gibt z. B. keine nah- und fernen Zeiger mehr, da sowohl lokale als auch globale Zuordnungen virtuelle 32-Bit-Adressen zurückgeben.

Speicherobjekte, die von [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) und [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) zugeordnet werden, befinden sich auf privaten Seiten mit Lese-/Schreibzugriff, auf die von anderen Prozessen nicht zugegriffen werden kann. Arbeitsspeicher, der mit **globalAlloc** mit **GMEM \_ DDESHARE** belegt wird, wird nicht global freigegeben, da er sich in 16-Bit-Windows befindet. Dieser Wert hat keine Auswirkungen und ist nur aus Kompatibilitätsgründen verfügbar. Anwendungen, die freigegebenen Arbeitsspeicher für andere Zwecke benötigen, müssen Dateizuordnungsobjekte verwenden. Mehrere Prozesse können eine Ansicht desselben Dateizuordnungsobjekts zuordnen, um benannten freigegebenen Arbeitsspeicher bereitzustellen. Weitere Informationen finden Sie unter [Dateizuordnung.](file-mapping.md)

Speicherbelegungen sind nur durch den verfügbaren physischen Arbeitsspeicher beschränkt, einschließlich des Speichers in der Auslagerungsdatei auf dem Datenträger. Wenn Sie festen Arbeitsspeicher zuweisen, geben [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) und [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) einen Zeiger zurück, den der aufrufende Prozess sofort für den Zugriff auf den Arbeitsspeicher verwenden kann. Wenn Sie verschiebebaren Speicher zuordnen, ist der Rückgabewert ein Handle. Um einen Zeiger auf ein verschiebbares Speicherobjekt abzurufen, verwenden Sie die Funktionen [**GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock) und [**LocalLock.**](/windows/desktop/api/WinBase/nf-winbase-locallock)

Die tatsächliche Größe des zugeordneten Arbeitsspeichers kann größer als die angeforderte Größe sein. Verwenden Sie die [**GlobalSize-**](/windows/desktop/api/WinBase/nf-winbase-globalsize) oder [**LocalSize-Funktion,**](/windows/desktop/api/WinBase/nf-winbase-localsize) um die tatsächliche Anzahl der zugeordneten Bytes zu bestimmen. Wenn der zugeordnete Betrag größer als der angeforderte Betrag ist, kann der Prozess den gesamten Betrag verwenden.

Die Funktionen [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc) und [**LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) ändern die Größe oder die Attribute eines Speicherobjekts, das von [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) und [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)zugeordnet wird. Die Größe kann sich erhöhen oder verringern.

Die Funktionen [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree) und [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) geben Arbeitsspeicher frei, der von [**GlobalAlloc,**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) [**LocalAlloc,**](/windows/desktop/api/WinBase/nf-winbase-localalloc) [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc)oder [**LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc)belegt wird. Verwenden Sie die [**GlobalDiscard-**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard) oder [**LocalDiscard-Funktion,**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) um das angegebene Speicherobjekt zu verwerfen, ohne das Handle ungültig zu machen. Das Handle kann später von **GlobalReAlloc** oder **LocalReAlloc** verwendet werden, um einen neuen Speicherblock zuzuweisen, der dem gleichen Handle zugeordnet ist.

Verwenden Sie die [**GlobalFlags-**](/windows/desktop/api/WinBase/nf-winbase-globalflags) oder [**LocalFlags-Funktion,**](/windows/desktop/api/WinBase/nf-winbase-localflags) um Informationen zu einem angegebenen Speicherobjekt zurückzugeben. Die Informationen enthalten die Sperrenanzahl des Objekts und geben an, ob das Objekt verwerfbar ist oder bereits verworfen wurde. Verwenden Sie die [**GlobalHandle-**](/windows/desktop/api/WinBase/nf-winbase-globalhandle) oder [**LocalHandle-Funktion,**](/windows/desktop/api/WinBase/nf-winbase-localhandle) um ein Handle für das Speicherobjekt zurückzugeben, das einem angegebenen Zeiger zugeordnet ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vergleichen von Speicherbelegungsmethoden](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 
