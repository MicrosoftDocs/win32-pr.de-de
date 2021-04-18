---
description: Erweiterte Konferenzen mithilfe von IP-basierten Netzwerken werden unter TAPI 3S Rendezvous-IP-telefoniekonferenz beschrieben. Das folgende Material bezieht sich auf die grundlegenden Konferenzen.
ms.assetid: f685097b-1b54-412b-999f-d9bdb3120ab9
title: Konferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ace4cb45bf74335298a3d4d262d064eb85c547f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354534"
---
# <a name="conference"></a>Konferenz

Erweiterte Konferenzen mithilfe von IP-basierten Netzwerken werden in der [Rendezvous-IP-Telefonkonferenz](rendezvous-ip-telephony-conferencing.md)von TAPI 3 beschrieben. Das folgende Material bezieht sich auf die grundlegenden Konferenzen.

Konferenzsitzungen sind Sitzungen, die mehr als zwei Parteien gleichzeitig enthalten. Sie können entweder mit einer externen serverbasierten Bridge oder mit einer Switch-basierten Konferenzbrücke eingerichtet werden.

In serverbasierten Konferenzsitzungen wählen alle beteiligten Parteien den Server aus, der die Mediendaten Ströme miteinander vermischt und jeden Teilnehmer an die Mischung sendet. Im Konferenzgespräch gibt es möglicherweise keine Vorstellung von einzelnen Parteien, sondern nur die eines einzelnen Aufrufes zwischen der Anwendung und dem Brücken Server. An TAPI scheint diese Art von Konferenz Anrufen eine normale 1-zu-eins-Verbindung zu sein.

Switchbasierte Konferenzen werden in Phasen fortgesetzt, von denen einige möglicherweise kombiniert werden, wenn Sie vom Dienstanbieter unterstützt werden:

1.  Initiieren Sie eine normale Kommunikationssitzung.
2.  Erstellen Sie eine Konferenz Sitzung mit dem ersten Mitglied der Partei, die Konferenz initiiert hat.
3.  Erstellen Sie eine Konferenz Beratungssitzung mit der Partei am anderen Ende der aktuellen Verbindung.
4.  Fügen Sie die-Beratungssitzung der Konferenz hinzu.

Nachdem eine Sitzung Mitglied einer Konferenz wird, wird der Status des Mitglieds auf "wird übertragen" zurückgesetzt. Der Status der Konferenz Sitzung wird in der Regel *verbunden*. Die Sitzungs-IDs für die Konferenz und alle hinzugefügten Parteien sind weiterhin gültig. Zustands Ereignisse können über alle Aufrufe empfangen werden. Wenn z. b. eines der Mitglieder die Verbindung trennt, um die Verbindung zu trennen, kann eine entsprechende Zustands Meldung die Anwendung über diesen Fakt informieren.

**TAPI 2. x:** Anwendungen können das Feature "keine Hold-Konferenz" von PBXs mithilfe der Option linecallparamflags \_ noholdconference verwenden. diese Funktion ermöglicht es, dass ein anderes Gerät (z. b. ein Supervisor-oder Aufzeichnungsgerät) im Hintergrund an die Zeile angefügt wird.

Beim Abbrechen der Beratungssitzung an den Drittanbieter einer Konferenz oder beim Entfernen der Drittpartei in einer zuvor eingerichteten Konferenz kann der Dienstanbieter die Konferenz freigeben und die Sitzung auf eine normale Verbindung mit zwei Parteien zurücksetzen. Wenn dies der Fall ist, geht die Konferenz Sitzung in den *Leerlauf* über, und die einzige verbleibende Sitzung wechselt von der Konferenz zum *verbundenen* Zustand.

Nicht alle Dienstanbieter unterstützen Konferenzen.

**TAPI 2. x:** Die [**linesetupconference**](/windows/win32/api/tapi/nf-tapi-linesetupconference) -Funktion nimmt den ursprünglichen Aufrufe der zwei Parteien als Eingabe an, ordnet einen Konferenzgespräch zu, verbindet den ursprünglichen aufrufungsort und ordnet einen Beratungs Rückruf zu, dessen Handle an die Anwendung zurückgegeben wird.

Wenn die Anwendung der Konferenz ein weiteres Mitglied hinzufügen soll, kann ein Wählvorgang für den Rückruf ausgeführt werden. Der Konferenz anrufhandle und die Verbindung zum Verbindungs Gespräch werden dann in der Funktion [**lineaddtoconference**](/windows/win32/api/tapi/nf-tapi-lineaddtoconference) verwendet. Konferenzmitglieder können auch mithilfe der [**lineprepareadddeconference**](/windows/win32/api/tapi/nf-tapi-lineprepareaddtoconference) -Funktion hinzugefügt werden, wenn Sie vom Dienstanbieter unterstützt wird.

Konferenzmitglieder werden mithilfe der [**lineremovefromconference**](/windows/win32/api/tapi/nf-tapi-lineremovefromconference) -Funktion entfernt, wenn Sie vom Dienstanbieter unterstützt wird.

Alternativ kann eine Konferenz mithilfe der [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer) -Funktion erstellt werden, die ein Beratungs-und Rückruf handle zurückgibt, und die Funktion [**linecompletetransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer) mit der konferenzoption (anstelle der [Übertragungs](transfer-ovr.md) Option).

**TAPI 3. x:** Die [**itbasiccallcontrol:: Conference**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-conference) -Methode nimmt die vorhandene Sitzung als Eingabe an und erstellt ein [callhub-Objekt](callhub-object.md) , wenn es noch nicht vorhanden ist. Die [**itbasiccallcontrol:: Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish) -Methode fügt den Callback-Aufruf zum callhub hinzu. Weitere Beratungssitzungen können mithilfe von " [**itaddress:: anatecall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)" erstellt und mithilfe der **Konferenz** -und **Abschluss** Methoden hinzugefügt werden.

> [!Note]  
> Die Funktionen des Geräts adressierte Geräte können die Anzahl der Parteien begrenzen, die in einem einzelnen-Befehl übertragen werden, und unabhängig davon, ob eine Konferenz mit einem normalen zwei Parteien-Rückruf beginnt.

 

 

 
