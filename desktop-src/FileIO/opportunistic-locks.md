---
description: Eine opistische Sperre (auch oplock genannt) ist eine Sperre, die von einem Client für eine Datei auf einem Server platziert wird.
ms.assetid: b4c2f5f0-a29b-4598-a49b-da99e93d2991
title: Deterministische Sperren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89d3e984c5a8a1a1dc9cc1cb0c0c56e92434433b334747e832ea7f3bdf62d3da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683400"
---
# <a name="opportunistic-locks"></a>Deterministische Sperren

Eine opistische Sperre (auch oplock genannt) ist eine Sperre, die von einem Client für eine Datei auf einem Server platziert wird. In den meisten Fällen fordert ein Client eine deterministische Sperre an, um Daten lokal zwischenspeichern zu können, wodurch der Netzwerkdatenverkehr reduziert und die offensichtliche Antwortzeit verbessert wird. Von Netzwerkumleitungen auf Clients mit Remoteservern sowie von Clientanwendungen auf lokalen Servern werden nicht-seitige Sperren verwendet.

Durch die verwendungsistischen Sperren werden das Zwischenspeichern von Daten und die Parallelität zwischen Clients und Servern und zwischen mehreren Clients koordiniert. Daten, die einheitlich sind, sind Daten, die im gesamten Netzwerk identisch sind. Anders ausgedrückt: Wenn Die Daten zusammenhängend sind, werden die Daten auf dem Server und allen Clients synchronisiert.

Bei menüistischen Sperren handelt es sich nicht um Befehle des Clients an den Server. Dabei handelt es sich um Anforderungen vom Client an den Server. Aus Sicht des Clients sind sie deterministisch. Das heißt, der Server gewährt solche Sperren immer dann, wenn andere Faktoren die Sperren ermöglichen.

Wenn eine lokale Anwendung Zugriff auf eine Remotedatei an benötigt, ist die Implementierung von deterministischen Sperren für die Anwendung transparent. Der Netzwerkumleitungsserver und der beteiligte Server öffnen und schließen die sperrbaren Sperren automatisch. Allerdings können auch deterministische Sperren verwendet werden, wenn eine lokale Anwendung Zugriff auf eine lokale Datei an benötigt und der Zugriff durch andere Anwendungen und Prozesse delegiert werden muss, um eine Beschädigung der Datei zu verhindern. In diesem Fall fordert die lokale Anwendung direkt eine deterministische Sperre vom lokalen Dateisystem an und speichert die Datei lokal zwischen. Bei dieser Verwendung ist die Sperre praktisch ein vom lokalen Server verwaltetes Semaphor und wird hauptsächlich für datenkoherische Zwecke in der Datei- und Dateizugriffsbenachrichtigung verwendet.

Bevor Sie in Ihrer Anwendung deterministische Sperren verwenden, sollten Sie mit den Dateizugriffs- und Freigabemodi vertraut sein, die unter Erstellen und Öffnen [von Dateien beschrieben sind.](creating-and-opening-files.md)

Die maximale Anzahl gleichzeitiger, gleichzeitiger sperren, die Sie erstellen können, ist nur durch die Menge des verfügbaren Arbeitsspeichers beschränkt.

Lokale Anwendungen sollten nicht versuchen, deterministische Sperren von Remoteservern an fordern. Ein Fehler wird von [**DeviceIoControl zurückgegeben,**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) wenn versucht wird, dies zu tun.

Für Anwendungen werden nur sehr eingeschränkte sperren verwendet. Die einzige praktische Verwendung besteht im Testen eines Netzwerkumleitungs- oder Server-Handlers für die deterministische Sperre. Dateisysteme implementieren in der Regel Unterstützung für deterministische Sperren. Anwendungen lassen die verwaltung von sperrenden Dateisystemen in der Regel den Dateisystemtreibern überlassen. Jeder, der ein Dateisystem verwendet, sollte das [Installable File System (IFS)-Kit verwenden.](https://www.microsoft.com/whdc/devtools/ifskit/default.mspx) Jeder, der einen anderen Gerätetreiber als ein installierbares Dateisystem entwickelt, sollte das [Windows Driver Kit (WDK) verwenden.](https://www.microsoft.com/?ref=go)

Die deterministischen Sperren und die zugehörigen Vorgänge sind eine Obermenge des deterministischen Sperranteils des CIFS-Protokolls (Common Internet File System), einem Internet Draft. Das CIFS-Protokoll ist eine erweiterte Version des Server Message Block -Protokolls (SMB). Weitere Informationen finden Sie unter [Übersicht über das Microsoft SMB-Protokoll und das CIFS-Protokoll.](microsoft-smb-protocol-and-cifs-protocol-overview.md) Der CIFS-Internetentwurf identifiziert explizit, dass eine CIFS-Implementierung möglicherweise durch unermage gewährungszusagente sperrende Sperren implementiert wird.

In den folgenden Themen werden die deterministischen Sperren identifiziert.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                               | Beschreibung                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Lokales Zwischenspeichern](local-caching.md)<br/>                                                                       | *Das lokale Zwischenspeichern* von Daten ist eine Technik, die verwendet wird, um den Netzwerkzugriff auf Datendateien zu beschleunigen. Dies umfasst nach Möglichkeit das Zwischenspeichern von Daten auf Clients und nicht auf Servern.<br/>                                                                                                                           |
| [Datenkoherenz](data-coherency.md)<br/>                                                                     | Wenn die Daten zusammenhängend sind, werden die Daten auf dem Server und allen Clients synchronisiert. Eine Art von Softwaresystem, das Datenkoherenz bietet, ist ein Revisionskontrollsystem (Revision Control System, RCS).<br/>                                                                                                              |
| [Anfordern einer deterministischen Sperre](how-to-request-an-opportunistic-lock.md)<br/>                         | Die verwendungsistischen Sperren werden angefordert, indem zuerst eine Datei mit Berechtigungen und Flags geöffnet wird, die für die Anwendung geeignet sind, die die Datei öffnet. Alle Dateien, für die die sperrende Methode angefordert wird, müssen für überlappende (asynchrone) Vorgänge geöffnet werden.<br/>                                |
| [Serverantwort auf offene Anforderungen für gesperrte Dateien](server-response-to-open-requests-on-locked-files.md)<br/> | Sie können die Auswirkungen Ihrer Anwendung auf andere Clients und deren Auswirkungen auf Ihre Anwendung minimieren, indem Sie so viel Freigabe wie möglich gewähren, die erforderliche Mindestzugriffsebene anfordern und die am wenigsten intrusivste, für Ihre Anwendung geeignete, deterministische Sperre verwenden.<br/> |
| [Typen von deterministischen Sperren](types-of-opportunistic-locks.md)<br/>                                         | Beschreibt die sperrenden Sperre für Ebene 1, Ebene 2, Batch und Filter.<br/>                                                                                                                                                                                                                     |
| [Breaking Deterministic Locks](breaking-opportunistic-locks.md)<br/>                                         | Das Brechen einer deterministischen Sperre ist der Prozess, bei dem die Sperre eines Clients für eine Datei herabgestuft wird, sodass ein anderer Client die Datei mit oder ohne eine deterministische Sperre öffnen kann.<br/>                                                                                                     |
| [Beispiele für die deterministische Sperre](opportunistic-lock-examples.md)<br/>                                           | Diagramme von Ansichten des Netzwerkdatenverkehrs für eine deterministische Sperre der Ebene 1, eine batch-sperre und eine filterbasierte Sperre.<br/>                                                                                                                                                       |
| [Deterministische Sperrvorgänge](opportunistic-lock-operations.md)<br/>                                       | Wenn eine Anwendung mithilfe der [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) mit dem **Flag FILE FLAG \_ \_ OVERLAPPED** für überlappende (asynchrone) Eingaben und Ausgaben geöffnet werden muss, müssen alle Dateien, für die sie Sperren an fordert, geöffnet werden.<br/>                                   |



 

Weitere Informationen zu deterministischen Sperren finden Sie im CIFS Internet Draft-Dokument. Alle Abweichungen zwischen diesem Thema und dem aktuellen CIFS Internet Draft sollten zugunsten des CIFS Internet Draft behoben werden.

 

