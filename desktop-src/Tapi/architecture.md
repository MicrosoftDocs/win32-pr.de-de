---
description: Die folgende Abbildung zeigt die allgemeine Architektur von Telefoniedienstanbietern und deren zugeordneten Benutzeroberflächen-DLLs (Dynamic Link Libraries).
ms.assetid: b5efe57a-19b8-49c5-810f-180633ed50d2
title: Architektur (telefonieapi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14423dba77af1ded38af4a6f2b896e76d28ca2cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353453"
---
# <a name="architecture-telephony-api"></a>Architektur (telefonieapi)

Die folgende Abbildung zeigt die allgemeine Architektur von Telefoniedienstanbietern und deren zugeordneten Benutzeroberflächen-DLLs (Dynamic Link Libraries).

![TSPS und zugehörige UI-DLLs](images/spuidl01.png)

Der Dienstanbieter besteht aus mindestens zwei Komponenten. Die Dienstanbieter-dll (in der Abbildung als Main bezeichnet). TSP) wird im Kontext des tapisrv-Prozesses ausgeführt und führt alle Aufgaben des Dienstanbieters aus, die nicht mit Benutzeroberflächen Elementen verknüpft sind, die mit der Verwendung des Geräts einer bestimmten Anwendung verknüpft sind (höchstwahrscheinlich in Verbindung mit nicht in der Abbildung dargestellten Komponenten auf niedrigerer Ebene). Im Gegensatz zu früheren Versionen von TAPI, bei denen der Code der Benutzeroberfläche in den Dienstanbieter integriert wurde (und aufgrund der vorherigen Architektur im Kontext der Anwendung ausgeführt wurde), muss der Dienstanbieter nun eine separate Komponente enthalten, die die Elemente der Benutzeroberfläche implementiert.

Die Benutzeroberflächen-DLL des Dienstanbieters muss Funktionen exportieren, die von TAPI aufgerufen werden, wenn die Anwendung TAPI-Funktionen aufruft, die Benutzeroberfläche generieren: [**tuispi \_ lineconfigdialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog), [**tuispi \_ lineconfigdialogedit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit), [**tuispi \_ phoneconfigdialog**](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog), [**tuispi \_ providerconfig**](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig), [**tuispi \_ providerinstall**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)und [**tuispi \_ providerremove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove). Jede dieser Funktionen umfasst als Parameter einen Zeiger auf eine Rückruffunktion in TAPI, den Typ " [**tuispidllcallback**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)", der von der Benutzeroberflächen-DLL verwendet werden kann, um bidirektional (senden und empfangen von Daten) mit der Dienstanbieter-dll, die im tapisrv-Prozess ausgeführt wird, zu kommunizieren. Wenn der Dienstanbieter jemals eine spontane Benutzeroberfläche generiert (z. b. das Dialogfeld Unimodem **Talk/hangup** ), in Verbindung mit jeder TSPI-Funktion, für die die Benutzeroberfläche nicht erwartet wird (z. b. eine Funktion, die nicht über einen *HWND* -Parameter verfügt), muss die Benutzeroberflächen-DLL [**tuispi \_ providergenericdialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) und [**tuispi \_**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)

> [!Note]  
> Die ursprünglichen TSPI-Funktionen für die Benutzeroberflächen Erstellung ( [**TSPI \_ lineconfigdialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog), [**TSPI \_ lineconfigdialogedit**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit), [**TSPI \_ phoneconfigdialog**](/windows/win32/api/tspi/nf-tspi-tspi_phoneconfigdialog), [**TSPI \_ providerconfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig), [**TSPI \_ providerinstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)und [**TSPI \_ providerremove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)) sind veraltet und werden von TAPI nie aufgerufen. Daher müssen diese nicht von der Dienstanbieter-dll exportiert werden. Wenn der Dienstanbieter jedoch als einer aufgeführt werden soll, der über die Telefonie-Systemsteuerung hinzugefügt werden kann, ein Dienstprogramm, das in den Versionen 1,4 und früher mit Windows-Telefoniefunktionen bereitgestellt wird. **TSPI \_ providerinstall** muss exportiert werden. wenn die Schaltfläche " [**Entfernen**](/windows/win32/api/tapi3if/nn-tapi3if-itcollection2) " in der System Steuerungs Option "Telefonie" aktiviert sein soll, wenn Sie ausgewählt ist, muss Sie " **TSPI \_ providerremove**" exportieren. wenn die Schaltfläche " **Setup** " in der Systemsteuerung "Telefonie" aktiviert werden soll, wenn Sie ausgewählt ist, muss Sie " **TSPI \_ providerconfig**" exportieren. Die Telefonie-Systemsteuerung prüft, ob diese Funktionen in der TSP-Datei des Dienstanbieters vorhanden sind, um die Benutzeroberfläche so anzupassen, dass Sie anzeigt, welche Vorgänge ausgeführt werden können.

 

Die Dienstanbieter-dll muss die [**TSPI \_ provideruiidentifizierung**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) -Funktion exportieren, die der tapisrv-Prozess verwendet, um den Namen der Benutzeroberflächen-DLL zu erhalten, die im Anwendungsprozess geladen werden soll. Es muss die [**TSPI \_ providergenericdialogdata**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) -Funktion exportieren, um Anforderungen von der Benutzeroberflächen-DLL zu empfangen und auf diese zu antworten, damit Daten angezeigt werden. Außerdem muss der [**TSPI \_ providerfredialoginstance**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance) -Prozess für den tapisrv-Prozess exportiert werden, um dem Dienstanbieter mitzuteilen, wann eine Zuordnung zur Erstellung einer spontanen Benutzeroberfläche in Verbindung mit einer Funktion veröffentlicht werden soll, die nicht als Darstellung der Benutzeroberfläche für den Benutzer definiert wurde. Die Dienstanbieter-dll kann Daten unidirektional mithilfe der neuen TSPI-Nachrichten [**Zeile \_ senddialoginstancedata**](line-senddialoginstancedata.md)an die Benutzeroberflächen-DLL senden.

Da die Namen der TSPI-und tuispi-Funktionen absichtlich als verschieden definiert werden, können die Dienstanbieter-dll und die UI-dll bei Bedarf dieselbe DLL-Datei sein. Bei der ordnungsgemäßen Segmentierung führt dies nicht unbedingt zu einer unnötigen Verwendung des Arbeitsspeichers im Anwendungskontext und kann den Installationsprozess für Dienstanbieter vereinfachen, die derzeit in einer einzigen dll implementiert werden können. TAPI ruft nur die Funktionen auf, die für den Kontext geeignet sind, in dem die dll verwendet wird.

Der Telefoniedienstanbieter und die Benutzeroberflächen-DLL müssen beide mit der Anforderung entworfen werden, dass die Benutzeroberflächen Funktionen gleichzeitig aus mehreren Anwendungs Prozessen aufgerufen werden können. Außerdem müssen Sie in Erwägung gezogen werden, dass sich die Anwendung und der TAPI-Dienst, unter denen der Telefoniedienstanbieter ausgeführt wird, auf separaten Computern auf einem LAN befinden können.

 

 
