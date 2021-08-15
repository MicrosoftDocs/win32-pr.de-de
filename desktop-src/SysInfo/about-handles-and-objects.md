---
description: Das System verwendet Objekte und Handles, um den Zugriff auf Systemressourcen aus zwei Hauptgründen zu steuern.
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: Informationen zu Handles und Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eee99e0568a0535462e89bfd5de71e12cfaf4a588a605f190dba41ce0ef2535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959048"
---
# <a name="about-handles-and-objects"></a>Informationen zu Handles und Objekten

Das System verwendet Objekte und Handles, um den Zugriff auf Systemressourcen aus zwei Hauptgründen zu steuern. Erstens stellt die Verwendung von -Objekten sicher, dass Microsoft die Systemfunktionalität aktualisieren kann, solange die ursprüngliche Objektschnittstelle beibehalten wird. Wenn nachfolgende Versionen des Systems veröffentlicht werden, können Sie das aktualisierte Objekt mit wenig oder gar keiner zusätzlichen Arbeit verwenden.

Zweitens können Sie durch die Verwendung von -Objekten die Vorteile der Windows nutzen. Jedes Objekt verfügt über eine eigene Zugriffssteuerungsliste (Access Control List, ACL), die die Aktionen angibt, die ein Prozess für das Objekt ausführen kann. Das System überprüft die ACL eines Objekts jedes Mal, wenn eine Anwendung ein Handle für das Objekt erstellt. Weitere Informationen finden Sie unter [Zugriffssteuerung](/windows/desktop/SecAuthZ/access-control).

-   [Objekt-Manager](object-manager.md)
-   [Objektschnittstelle](object-interface.md)
-   [Objektnamespaces](/windows/desktop/Sync/object-namespaces)
-   [Einschränkungen bei der Handhabung](handle-limitations.md)
-   [Behandeln der Vererbung](handle-inheritance.md)

 

 
