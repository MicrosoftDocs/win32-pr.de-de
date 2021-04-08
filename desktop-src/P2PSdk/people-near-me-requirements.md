---
description: Anforderungen an Personen in meiner Nähe
ms.assetid: c7ab73fc-56a6-4b6c-820a-3f8e4a97cfaf
title: Anforderungen an Personen in meiner Nähe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6afb97800041e0fcd9a10a6d95334b832fb363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865148"
---
# <a name="people-near-me-requirements"></a>Anforderungen an Personen in meiner Nähe

Damit Personen in [meiner](about-people-near-me.md) Umgebung nahtlose Konnektivität und einfache Zusammenarbeit mit Benutzern für Windows-Peer-Netzwerkanwendungen bereitstellen können, wird Folgendes erreicht:

### <a name="people-discovery"></a>Personen Ermittlung

Durch die Ermittlung von Personen kann ein Benutzer die Gruppe von Peers ermitteln und anzeigen, die sich im lokalen Subnetz befinden. Auf allen Computern im lokalen Subnetz müssen die Namen angemeldeter Peers angekündigt werden. Die nach einer Ermittlungs Abfrage aufgeführten Peers sind der Satz von Benutzern, die Windows Vista ausführen und die so konfiguriert sind, dass Sie anderen Benutzern mit " [Personen in meiner](about-people-near-me.md)Umgebung" einen Spitznamen ankündigen. Diese Funktion ist standardmäßig deaktiviert und muss vom angemeldeten Benutzer aktiviert werden.

> [!Note]  
> Remote Peers, die während des Ermittlungs Prozesses "Personen in meiner Umgebung" ermittelt wurden, sind nicht notwendigerweise die erwarteten Benutzer, die den ermittelten Peers zugeordnet sind.

 

### <a name="extended-data-discovery"></a>Erweiterte Daten Ermittlung

Die erweiterte Daten Ermittlung ermöglicht die Suche nach Benutzern, die bestimmte Interessen haben. Es ist auch möglich, dass Benutzer angeben, dass Sie zusätzliche Daten über sich selbst ankündigen möchten. Beispielsweise können die Daten zusätzlich zum Spitzname des angemeldeten Benutzers bestimmte berufliche Interessen auf einer Branchenkonferenz beschreiben.

### <a name="application-discovery"></a>Anwendungsermittlung

Die genaue Natur der von "Personen in meiner Umgebung" aktivierten Ad-hoc-Zusammenarbeit ist spezifisch für Anwendungen. Die Zusammenarbeit könnte z. b. eine Chat-oder Freigabe von Fotos sein, die beide bestimmte Anwendungen erfordern. Damit Benutzer in meiner Umgebung Kollaborations Aktivitäten aktivieren können, muss der Satz von Anwendungen, die für Personen in meiner Umgebung verfügbar sind, ebenfalls angekündigt und auffindbar sein.

### <a name="subscription"></a>Subscription

Mithilfe eines Abonnements können Anwendungen die Anwesenheits-, Anwendungs-und Objektänderungen einer Person nachverfolgen.

### <a name="invitation"></a>Einladung

Nachdem die Personen, Interessen und Anwendungen ermittelt wurden, kann die Zusammenarbeit mit der Peer-Zusammenarbeit mithilfe einer Anwendung "Personen in meiner Umgebung" eine Einladung und einen Akzeptanz Austausch beginnen. Der initiierende Peer sendet eine Einladungs Nachricht an einen anderen Peer oder Peers. Die Benutzer, die die Einladung erhalten, können die Einladung annehmen oder ablehnen. Wenn die Einladung akzeptiert wird, wird die entsprechende Peer Anwendung für die angeforderte Aktivität gestartet.

### <a name="add-as-a-contact"></a>Als Kontakt hinzufügen

Wenn Benutzer eine Zusammenarbeits Aktivität über Personen in meiner Umgebung einrichten und den Kontakt im Laufe der Zeit aufbewahren möchten, können Sie sich gegenseitig als Kontakt hinzufügen. Sobald dies erreicht ist, kann der Anwesenheitsstatus eines Benutzers (z. b. Online, offline oder entfernt) beobachtet und zu einem beliebigen Zeitpunkt über das Internet zu einer Kollaborations Aktivität eingeladen werden. Alle Aktivitäten, die mit der Person möglich waren, als Sie in der Nähe gefunden wurden, sind auch mit einem Kontakt über das Internet möglich.

### <a name="security"></a>Sicherheit

Um die Benutzer und die Daten zu schützen, die in einer Peer Zusammenarbeits Aktivität ausgetauscht werden, haben die Benutzer die Konfigurations Kontrolle darüber, was angekündigt wird. Benutzer müssen auch eine Einladung annehmen, bevor die Peer Zusammenarbeit beginnen kann. Die Zusammenarbeits Aktivität wird mit einem Secure Sockets Layer (SSL) verschlüsselten Kanal (auch als SChannel bezeichnet) verschlüsselt. SSL ist ein kryptografisches Protokoll zum Schutz der TCP-basierten Kommunikation. Weitere Informationen finden Sie unter [SChannel](windows-vista-components-for-people-near-me.md). Diese Anforderungen werden von einem neuen Satz von Komponenten in der [Windows-Peer-Netzwerk](what-is-peer-networking-.md)Architektur in Windows Vista unterstützt.

 

 



