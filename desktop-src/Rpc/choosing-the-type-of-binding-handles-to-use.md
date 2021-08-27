---
title: Auswählen des Zu verwendenden Bindungshandlestyps
description: Auswählen des Zu verwendenden Bindungshandlestyps
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd35286a5bb88be3094238e0e4c43b701826bca0a7e5ad02d35c5f87f0cbdaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022920"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a>Auswählen des Zu verwendenden Bindungshandlestyps

**Bewährte Methode:** Wenn Sie wissen, welcher Server von der Anwendung verwendet wird, verwenden Sie explizite Handles. Verwenden Sie andernfalls jedes Mal explizite Handles oder generische Handles mit **\_ Bindungs-** und **\_ Bindungsroutinen.**

Verwenden Sie keine impliziten Handles oder automatischen Handles. Implizite Handles sind nicht threadsicher, und obwohl threadsicherheit unnötig erscheinen mag, kann sie später erforderlich werden. Automatische Handles haben einen hohen Mehraufwand und erfordern viel Setup, um ordnungsgemäß zu funktionieren. Ihre Suchfunktionen wurden durch Active Directory-Dienste ersetzt.

Explizite Handles sind äußerst effizient, und viele attraktive Funktionen sind nur für explizite Handles verfügbar. Wenn beispielsweise mehrere RPC-Aufrufe an denselben Server gesendet werden, können Sie das Bindungshandle einmal erstellen und alle Aufrufe damit vornehmen. Dieser Ansatz ist viel effizienter als jede andere Methode. Wenn der Server, an den der Aufruf gesendet wird, unbekannt ist, erstellen Sie ein explizites Bindungshandle für jeden Aufruf, oder verwenden Sie generische Bindungshandles.

In Microsoft™ Windows XP ist die RPC-Laufzeit bei der erneuten Verwendung und Zwischenspeicherung von Aufrufen recht effizient. Wenn der n+1.-Aufruf also auf demselben Server wie der n-ten Aufruf endet, verwendet RPC die ressourcen, die für den *n-ten* Aufruf zugeordnet sind, um die Notwendigkeit zu umgehen, Bindungshandles zwischenzuspeichern, um die Leistung zu verbessern.  

 

 




