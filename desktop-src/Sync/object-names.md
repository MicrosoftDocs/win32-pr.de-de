---
description: Benannte Objekte bieten eine einfache Möglichkeit für Prozesse, Objekt Handles gemeinsam zu nutzen.
ms.assetid: 00a00227-45fc-49a1-8ff5-aeccb172d16a
title: Objektnamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee746150a41f335a4073cb4b5ba282d17ad706f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368912"
---
# <a name="object-names"></a>Objektnamen

Benannte Objekte bieten eine einfache Möglichkeit für Prozesse, Objekt Handles gemeinsam zu nutzen. Nachdem ein Prozess ein benanntes Ereignis, Mutex, Semaphore oder Timer-Objekt erstellt hat, können andere Prozesse den Namen verwenden, um die entsprechende Funktion ( [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa), [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw), [**opensemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)oder [**openwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw)) aufzurufen, um ein Handle für das Objekt zu öffnen. Beim Namensvergleich wird zwischen Groß-und Kleinschreibung

Die Namen von Ereignissen, Semaphore, Mutex, wabbarer Timer, Datei Zuordnung und Auftrags Objekten verwenden denselben Namespace. Wenn Sie versuchen, ein Objekt mit einem Namen zu erstellen, der von einem Objekt eines anderen Typs verwendet wird, tritt bei der Funktion ein Fehler auf, und [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ein **\_ ungültiges \_ handle** zurück. Verwenden Sie daher beim Erstellen benannter Objekte eindeutige Namen, und überprüfen Sie die Funktions Rückgabewerte auf Fehler mit doppelten Namen.

Wenn Sie versuchen, ein Objekt mit einem Namen zu erstellen, der von einem Objekt desselben Typs verwendet wird, wird die Funktion erfolgreich ausgeführt, und es wird ein Handle an das vorhandene Objekt zurückgegeben, und [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen Fehler zurück, der **\_ bereits \_ vorhanden** ist. Wenn z. b. der in einem Aufrufen der Funktion " [**-Funktion"**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) angegebene Name mit dem Namen eines vorhandenen Mutex-Objekts übereinstimmt, gibt die Funktion ein Handle an das vorhandene Objekt zurück. In diesem Fall entspricht der aufzurufende Aufrufs von " **kreatemutex** " dem Aufrufen der [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) -Funktion. Wenn Sie mehrere Prozesse verwenden, ist die Verwendung von " **kreatemutex** " für denselben Mutex gleichbedeutend mit einem Prozess, bei dem "up- **Mutex** " aufgerufen wird, während die anderen Prozesse **OpenMutex** aufrufen, mit dem Unterschied, dass Sie nicht sicherstellen müssen, dass der Erstellungsprozess Wenn Sie diese Technik für Mutex-Objekte verwenden, sollte jedoch keiner der aufrufenden Prozesse den unmittelbaren Besitz des Mutex anfordern. Wenn mehrere Prozesse den unmittelbaren Besitz anfordern, kann es schwierig sein, vorherzusagen, welcher Prozess tatsächlich den anfänglichen Besitz erhält.

Eine Terminaldiensteumgebung verfügt über einen globalen Namespace für Ereignisse, Semaphore, Mutexen, wabbare Timer, Datei Mapping-Objekte und Auftrags Objekte. Außerdem verfügt jede Terminal Dienste-Client Sitzung über einen eigenen separaten Namespace für diese Objekte. Terminal Dienste-Client Prozesse können Objektnamen mit einem \\ Präfix "Global" oder "local \\ " verwenden, um explizit ein Objekt im globalen Namespace oder im Sitzungs Namespace zu erstellen. Weitere Informationen finden Sie unter [Kernel Object Namespaces](../termserv/kernel-object-namespaces.md). Die schnelle Benutzerumschaltung wird mithilfe von Terminal Dienste-Sitzungen implementiert (jeder Benutzer meldet sich in einer anderen Sitzung an). Kernel Objektnamen müssen den für Terminal Dienste beschriebenen Richtlinien entsprechen, damit Anwendungen mehrere Benutzer unterstützen können.

Synchronisierungs Objekte können in einem privaten Namespace erstellt werden. Weitere Informationen finden Sie unter [objektnamespaces](object-namespaces.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von benannten Objekten](using-named-objects.md)
</dt> </dl>

 

 
