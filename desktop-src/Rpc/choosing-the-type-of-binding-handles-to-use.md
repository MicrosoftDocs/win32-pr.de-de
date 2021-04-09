---
title: Auswählen des Typs der zu verwendenden Bindungs Handles
description: Auswählen des Typs der zu verwendenden Bindungs Handles
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dd07716b3618766b3ea8aa07fb766f154285207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036676"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a>Auswählen des Typs der zu verwendenden Bindungs Handles

**Bewährte Methoden:** Wenn Sie wissen, welcher Server von der Anwendung verwendet werden soll, verwenden Sie explizite Handles. Wenn Sie dies nicht tun, verwenden Sie jedes Mal explizite Handles, oder verwenden Sie generische Handles mit **\_ Bindungs** -und **\_ Bindung** -Routinen.

Verwenden Sie keine impliziten Handles oder automatischen Handles. Implizite Handles sind nicht Thread sicher, und auch wenn die Thread Sicherheit unnötig erscheinen mag, könnte Sie später erforderlich werden. Automatische Handles haben einen hohen Verwaltungsaufwand und erfordern eine Menge an Setup, um ordnungsgemäß zu funktionieren. Die Suchfunktionen wurden durch Active Directory Dienste abgelöst.

Explizite Handles sind sehr effizient, und viele attraktive Funktionen sind nur für explizite Handles verfügbar. Wenn z. b. mehrere RPC-Aufrufe an denselben Server weitergeben, können Sie das Bindungs handle einmal erstellen und alle Aufrufe damit ausführen. Diese Vorgehensweise ist viel effizienter als jede andere Methode. Wenn der Server, zu dem der-Vorgang gehört, unbekannt ist, erstellen Sie für jeden-Rückruf ein explizites Bindungs handle, oder verwenden Sie generische Bindungs Handles.

In Microsoft™ Windows XP ist die RPC-Laufzeit sehr effizient bei der Wiederverwendung und Zwischenspeicherung von aufrufen. Wenn also der Aufruf von " *n*+ 1" auf dem gleichen Server wie der *n*-te Aufruf läuft, verwendet RPC die für den *n*-ten Aufruf zugeordneten Ressourcen erneut, wodurch die Notwendigkeit zum Zwischenspeichern von Bindungs Handles umgangen wird, um die Leistung zu verbessern.

 

 




