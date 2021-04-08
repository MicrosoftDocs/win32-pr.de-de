---
description: Windows-Peer Komponenten für "Personen in meiner Umgebung"
ms.assetid: aa9e7d4d-4131-4578-8bd1-298f04b826f9
title: Windows-Peer Komponenten für "Personen in meiner Umgebung"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c780ccad1abd5ce04c1672f66561285831e5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959774"
---
# <a name="windows-peer-components-for-people-near-me"></a>Windows-Peer Komponenten für "Personen in meiner Umgebung"

Innerhalb der ausführbaren Windows-Peer-Netzwerkdatei (P2phost.exe) werden in der [Architektur "Personen in meiner](people-near-me-architecture.md) Umgebung" die folgenden Komponenten verwendet:

### <a name="people-near-me"></a>Personen in meiner Umgebung

Die Komponente "Personen in meiner Umgebung" (PNM) initiiert die Ermittlung mithilfe der Webdienst Ermittlung im lokalen Subnetz für die Benutzernamen von PNM-fähigen Computern.

### <a name="people-near-me-publisher"></a>"Personen in meiner Umgebung"

Die Verleger Komponente "Personen in meiner Umgebung" veröffentlicht die Spitznamen angemeldeter Benutzer, um die Verfügbarkeit für andere Computer mit PNM im lokalen Subnetz anzugeben. Der angemeldete Benutzer muss seinen Spitznamen vor der Ankündigung veröffentlichen. Der Spitzname wird im Subnetz mithilfe der Webdienst Ermittlung veröffentlicht. Darüber hinaus können auch Objekte und Anwendungen veröffentlicht werden. Der Benutzer muss jedoch die Objekt-und Anwendungs Veröffentlichung für die Bereiche "**Personen in meiner** Umgebung" oder "**alle**" angeben.

### <a name="people-near-me-enumerator"></a>Enumerator "Personen in meiner Umgebung"

Die enumeratorkomponente "Personen in meiner Umgebung" listet die Benutzer auf, die sich im lokalen Subnetz befinden. Mithilfe dieser Liste sendet die Webdienst Ermittlung eine Multicast Abfrage und empfängt die Antworten. Nachdem die Liste der Spitznamen abgerufen wurde, kann eine Anwendung die API verwenden, um weitere Daten abzurufen, die vom Benutzer veröffentlicht werden (der mithilfe von [SChannel](windows-vista-components-for-people-near-me.md)verschlüsselt wurde), z. b. die Liste der registrierten Anwendungen und alle Objekte, die veröffentlicht werden.

Der Such-und enumerationsprozess wird nicht automatisch durchgeführt, sondern muss von einem Benutzer oder einer Anwendung explizit initiiert werden, indem er sich bei PNM anmeldet. Die Suchergebnisse sind die Liste der Spitznamen anderer Benutzer im gleichen Subnetz, die ihre Spitznamen mithilfe der PNM-API ankündigen.

### <a name="publication-manager"></a>Veröffentlichungs-Manager

Die Veröffentlichungs-Manager-Komponente ist für das Veröffentlichen von Anwesenheits-, Anwendungs-oder Objekt Updates für Kontakte oder Personen in meiner Nähe zuständig, die Daten abonniert oder abgerufen haben.

### <a name="peer-signaling"></a>Peer Signalisierung

Die Peer Signalisierungs Komponente behandelt die Erstellung von Verbindungen zwischen Peers und Exchange-Daten. Für Personen in meiner Umgebung wird Peer Signalisierung verwendet, wenn ein Benutzer oder eine Anwendung die unicastabfrage an einen bestimmten Computer für seinen öffentlichen Schlüssel, seine Anwendungen und Objekte sendet.

### <a name="receive-invitation-handlerux"></a>Einladungs Handler/UX empfangen

Die Komponente empfangende Einladungs Handler/UX empfängt eine eingehende Einladung von einer anderen Person, fordert den Benutzer auf, zu bestimmen, ob die der Einladung zugeordnete Anwendung gestartet werden soll, und startet dann die Anwendung basierend auf dem Benutzer, der die Einladung annimmt. Eine Einladung ist eine Nachricht von einer anderen Person zum Initiieren von Kollaborations Aktivitäten mithilfe einer bestimmten Anwendung, die auf den Computern der Benutzer installiert ist und von dem Benutzer angekündigt wird, der eingeladen wird.

### <a name="peer-security"></a>Peer Sicherheit

Wenn Anwesenheit, Anwendung und Objekt gesendet werden, werden die Informationen über einen SSL-Kanal ([SChannel](windows-vista-components-for-people-near-me.md)) verschlüsselt. Der initiierende Computer verwendet den öffentlichen Schlüssel des eingeladenen Computers, um einen geheimen Schlüssel auszuhandeln, der zum Verschlüsseln der nachfolgenden Daten verwendet wird, die zwischen den beiden Peers gesendet werden.

 

 



