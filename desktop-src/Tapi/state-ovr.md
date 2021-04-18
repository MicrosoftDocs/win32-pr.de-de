---
description: Sitzungs-oder Aufrufstatus gibt den aktuellen Status einer Sitzung an, z \# . b. &0034; Angebot&\# 0034; oder &\# 0034; verbunden. &\# 0034; Die ordnungsgemäße Handhabung von Zustandsinformationen ist entscheidend für die ordnungsgemäße Funktionsweise der meisten TAPI-Anwendungen.
ms.assetid: a6a49b77-4e9b-4f23-bfe6-26f26549b18f
title: State
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88fb9c482fcb9e432b5bfb5d36f77cd09f538086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352361"
---
# <a name="state"></a>State

Sitzungs-oder Aufrufstatus gibt den aktuellen Status einer Sitzung an, z. b. "Angebot" oder "verbunden". Die ordnungsgemäße Handhabung von Zustandsinformationen ist entscheidend für die ordnungsgemäße Funktionsweise der meisten TAPI-Anwendungen. Beispielsweise kann der Antwort Vorgang nur für eine angebotene Sitzung ausgeführt werden, aber eine Übertragung schlägt fehl, wenn sich die Sitzung in diesem Zustand befindet.

Der Status einer Sitzung ändert sich aufgrund von Ereignissen. Ereignisse können angefordert oder nicht angefordert werden. Angeforderte *Ereignisse* werden von der Anwendung verursacht, die die Sitzung steuert, z. b. Wenn ein TAPI-Sitzungs Vorgang aufgerufen wird. Nicht *angeforderte Ereignisse* werden durch den Schalter, das Telefon Netzwerk, die Benutzer Schaltflächen auf dem lokalen Telefon oder die Aktionen der Remote Partei verursacht.

Wenn ein Dienstanbieter eine Änderung des Sitzungs Zustands erkennt, meldet er die Änderung an TAPI, und TAPI gibt eine Ereignis Benachrichtigung an alle Besitzer-und Überwachungsanwendungen aus. Die Anwendung muss auf diese Benachrichtigungen entsprechend reagieren. Informationen zum Steuern der an eine Anwendung gemeldeten Ereignisse finden Sie unter Ereignis Benachrichtigung unter [TAPI-Initialisierung](tapi-initialization.md) .

Eine Anwendung sollte immer Zustands Ereignis Benachrichtigungen verarbeiten. Zustandsübergänge, die für eine physische Konfiguration gültig sind, sind möglicherweise für einen anderen ungültig. Betrachten Sie z. b. eine Linie, die physisch sowohl auf dem Computer als auch an einem separaten Telefon Satz beendet wird, wobei eine Partei Zeilen Konfiguration zwischen dem Computer und dem Telefon Satz erstellt wird. Eine Anwendung, die auf dem Computer ausgeführt wird, kennt möglicherweise keine Telefon Satz Aktivitäten. Das heißt, die Zeile wird möglicherweise verwendet, ohne dass der Dienstanbieter Sie kennt. Eine Anwendung, die versucht, einen ausgehenden-Befehl zu erstellen, kann die Darstellung eines Ansehens von TAPI erfolgreich zuordnen, dies führt jedoch dazu, dass der aktive-Befehl in der Zeile freigegeben wird Das Blind Senden einer DTMF-Wähl Zeichenfolge, ohne zuerst auf einen Wählton zu prüfen, führt möglicherweise nicht zum beabsichtigten (oder höflichen) Verhalten

Eine Anwendung sollte nicht einen strengen Fortschritt von einem Zustand zu einem anderen annehmen. Zustands Ereignisse werden empfangen und asynchron weitergeleitet, und Benachrichtigungen können nicht in einer vorhersagbaren Reihenfolge empfangen werden. Daher sollten Aufrufe von Zustands Benachrichtigungen so angezeigt werden, dass die Anwendung den neuen Status des Aufrufes anzeigt, anstatt die Übergänge zwischen zwei Zuständen zu melden.

Alle Telefoniedienstanbieter müssen diese Informationen bereitstellen.

* * TAPI 2. x: * *[**linegetcallstatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**line \_ CallState**](./line-callstate.md) -Meldung, [linecallstate- \_ Konstanten](./linecallstate--constants.md)

**TAPI 3. x: **[**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** cil \_ callid** -Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**itcallstateevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) -Benachrichtigung, [**Aufruf \_ Status**](/windows/desktop/api/Tapi3if/ne-tapi3if-call_state) Enumerator

 

 
