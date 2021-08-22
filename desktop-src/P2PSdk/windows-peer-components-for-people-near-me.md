---
description: Windows Peerkomponenten für Personen in meiner Umgebung
ms.assetid: aa9e7d4d-4131-4578-8bd1-298f04b826f9
title: Windows Peerkomponenten für Personen in meiner Umgebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762ea58aa9738bfe01e23844dd146e4de8a6a5f76433ef969b60b30fb5886db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011498"
---
# <a name="windows-peer-components-for-people-near-me"></a>Windows Peerkomponenten für Personen in meiner Umgebung

Innerhalb der ausführbaren Windows peer networking (P2phost.exe) verwendet die Personen in meiner Umgebung [Architecture](people-near-me-architecture.md) die folgenden Komponenten:

### <a name="people-near-me"></a>Personen in meiner Umgebung

Die Personen in meiner Umgebung -Komponente (PNM) initiiert die Ermittlung mithilfe der Webdienstermittlung im lokalen Subnetz für die Benutzernamen von PNM-fähigen Computern.

### <a name="people-near-me-publisher"></a>Personen in meiner Umgebung Publisher

Die Personen in meiner Umgebung Publisher-Komponente veröffentlicht die Spitznamen angemeldeter Benutzer, um die Verfügbarkeit für andere Computer mithilfe von PNM im lokalen Subnetz anzugeben. Der angemeldete Benutzer muss seinen Spitznamen veröffentlichen, bevor er angekündigt wird. Der Spitzname wird im Subnetz mithilfe der Webdienstermittlung veröffentlicht. Darüber hinaus können Objekte und Anwendungen auch veröffentlicht werden. Der Benutzer muss jedoch die Objekt- und Anwendungsveröffentlichung für die Bereiche **"Personen in meiner Umgebung"** oder **"Alle"** angeben.

### <a name="people-near-me-enumerator"></a>Personen in meiner Umgebung-Enumerator

Die Personen in meiner Umgebung Enumeratorkomponente listet die Benutzerliste im lokalen Subnetz auf. Anhand dieser Liste sendet die Webdienstermittlung eine Multicastabfrage und empfängt die Antworten. Nachdem die Liste der Spitznamen abgerufen wurde, kann eine Anwendung die API verwenden, um weitere Vom Benutzer veröffentlichte Daten abzurufen (die mithilfe von [SChannel](windows-vista-components-for-people-near-me.md)verschlüsselt werden), z. B. die Liste der registrierten Anwendungen und alle objekte, die veröffentlicht werden.

Der Such- und Enumerationsprozess erfolgt nicht automatisch, sondern muss explizit von einem Benutzer oder einer Anwendung initiiert werden, indem er sich bei PNM anmeldet. Bei den Suchergebnissen handelt es sich um die Liste der Spitznamen anderer Benutzer im gleichen Subnetz, die ihre Spitznamen mithilfe der PNM-API bekannt geben.

### <a name="publication-manager"></a>Veröffentlichungs-Manager

Die Veröffentlichungs-Manager-Komponente ist für die Veröffentlichung von Anwesenheits-, Anwendungs- oder Objektupdates für Kontakte oder Personen in meiner Nähe verantwortlich, die abonniert sind oder Daten erhalten.

### <a name="peer-signaling"></a>Peersignalisierung

Die Peersignalisierungskomponente übernimmt die Erstellung von Verbindungen zwischen Peers zum Austauschen von Daten. Für Personen in meiner Umgebung wird Peersignalisierung verwendet, wenn ein Benutzer oder eine Anwendung die Unicastabfrage für den öffentlichen Schlüssel, die Anwendungen und die Objekte an einen bestimmten Computer sendet.

### <a name="receive-invitation-handlerux"></a>Empfangen des Einladungshandlers/der Beux

Die Komponente Receive Invitation Handler/UX empfängt eine eingehende Einladung von einer anderen Person, fordert den Benutzer auf, zu bestimmen, ob er die der Einladung zugeordnete Anwendung starten möchte, und startet dann die Anwendung basierend auf dem Benutzer, der die Einladung akzeptiert. Eine Einladung ist eine Nachricht von einer anderen Person, um eine Zusammenarbeitsaktivität mithilfe einer bestimmten Anwendung zu initiieren, die auf den Computern beider Benutzer installiert und vom eingeladenen Benutzer angekündigt wird.

### <a name="peer-security"></a>Peersicherheit

Wenn Anwesenheit, Anwendung und Objekt gesendet werden, werden die Informationen mithilfe eines SSL-Kanals ([Schannel ) verschlüsselt.](windows-vista-components-for-people-near-me.md) Der initiierende Computer verwendet den öffentlichen Schlüssel des eingeladenen Computers, um einen geheimen Schlüssel auszuhandeln, der zum Verschlüsseln der nachfolgenden Daten verwendet wird, die zwischen den beiden Peers gesendet werden.

 

 



