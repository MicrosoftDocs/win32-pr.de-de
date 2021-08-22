---
description: Personen in meiner Umgebung Anforderungen
ms.assetid: c7ab73fc-56a6-4b6c-820a-3f8e4a97cfaf
title: Personen in meiner Umgebung Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ebbb904175184b6e9d06c807aa4b4ed645c93633114d6b9b64085e34dfa3683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518350"
---
# <a name="people-near-me-requirements"></a>Personen in meiner Umgebung Anforderungen

Damit [Personen in meiner Umgebung](about-people-near-me.md) nahtlose Konnektivität und einfache Zusammenarbeit für Benutzer für Peernetzwerkanwendungen Windows, wird Folgendes erreicht:

### <a name="people-discovery"></a>Personenermittlung

Mit der Personenermittlung kann ein Benutzer die Peers im lokalen Subnetz finden und anzeigen. Alle Computer im lokalen Subnetz müssen die Namen der angemeldeten Peers anmelden. Bei den peers, die nach einer Ermittlungsabfrage aufgelistet werden, handelt es sich um die Gruppe von Benutzern, die Windows Vista ausführen und so konfiguriert sind, dass sie anderen Benutzern mithilfe von [Personen in meiner Umgebung.](about-people-near-me.md) Diese Funktion ist standardmäßig deaktiviert und muss vom angemeldeten Benutzer aktiviert werden.

> [!Note]  
> Remote-Peers, die während Personen in meiner Umgebung Ermittlungsvorgang gefunden wurden, sind nicht unbedingt die erwarteten Benutzer, die den gefundenen Peers zugeordnet sind.

 

### <a name="extended-data-discovery"></a>Erweiterte Datenermittlung

Die erweiterte Datenermittlung ermöglicht die Suche nach Benutzern, die bestimmte Interessen haben. Es ist auch möglich, dass Benutzer angeben, dass sie zusätzliche Daten über sich selbst ankn geben möchten. Die Daten könnten z. B. bestimmte professionelle Interessen auf einer Branchenkonferenz beschreiben, zusätzlich zum Spitznamen des angemeldeten Benutzers.

### <a name="application-discovery"></a>Anwendungsermittlung

Die genaue Art der Ad-hoc-Zusammenarbeit, die von Personen in meiner Umgebung aktiviert wird, ist anwendungsspezifisch. Die Zusammenarbeit kann z. B. das Chatten oder Freigeben von Fotos sein, die beide bestimmte Anwendungen erfordern. Damit Personen in meiner Umgebung Zusammenarbeitsaktivitäten aktivieren können, müssen die Anwendungen, die für Personen in meiner Umgebung verfügbar sind, ebenfalls angekündigt und erkennbar sein.

### <a name="subscription"></a>Subscription

Mithilfe eines Abonnements können Anwendungen abonnieren, um die Anwesenheit, Anwendungen und Objektänderungen einer Person nachverfolgung zu verfolgen.

### <a name="invitation"></a>Einladung

Nachdem die Personen, Interessen und Anwendungen entdeckt wurden, kann die Peerzusammenarbeit mithilfe einer Personen in meiner Umgebung-Anwendung einen Einladungs- und Akzeptanzaustausch starten. Der initiierende Peer sendet eine Einladungsnachricht an einen anderen Peer oder andere Peers. Die Benutzer, die die Einladung erhalten, können die Einladung annehmen oder ablehnen. Wenn die Einladung akzeptiert wird, wird die entsprechende Peeranwendung für die angeforderte Aktivität gestartet.

### <a name="add-as-a-contact"></a>Als Kontakt hinzufügen

Wenn Benutzer eine Zusammenarbeitsaktivität über Personen in meiner Umgebung einrichten und den Kontakt im Laufe der Zeit erhalten möchten, können sie sich gegenseitig als Kontakt hinzufügen. Sobald dies erreicht ist, können sie den Anwesenheitsstatus eines Benutzers (z. B. online, offline oder weg) beobachten und ihn jederzeit zu einer Zusammenarbeitsaktivität über das Internet einladen. Jede Aktivität, die mit der Person möglich war, als sie sich in der Nähe befand, ist auch mit einem Kontakt über das Internet möglich.

### <a name="security"></a>Sicherheit

Um die Benutzer und die Daten zu schützen, die in einer Peerzusammenarbeitsaktivität ausgetauscht werden, haben Benutzer die Konfigurationssteuerung darüber, was angekündigt wird. Benutzer müssen auch eine Einladung annehmen, bevor die Peerzusammenarbeit beginnen kann. Die Zusammenarbeitsaktivität wird mit einem Secure Sockets Layer (SSL) verschlüsselten Kanal (auch als Schannel bekannt) verschlüsselt. SSL ist ein kryptografisches Protokoll zum Schutz der TCP-basierten Kommunikation. Weitere Informationen finden Sie unter [SChannel](windows-vista-components-for-people-near-me.md). Diese Anforderungen werden von einer neuen Gruppe von Komponenten in der Windows [Peernetzwerkarchitektur](what-is-peer-networking-.md)in Windows Vista unterstützt.

 

 



