---
description: Das System verwendet Objekte und Handles, um den Zugriff auf Systemressourcen aus zwei Hauptgründen zu regulieren.
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: Informationen zu Handles und Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c7474c11298166cc8d63032c6e1d8f84e6db249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959853"
---
# <a name="about-handles-and-objects"></a>Informationen zu Handles und Objekten

Das System verwendet Objekte und Handles, um den Zugriff auf Systemressourcen aus zwei Hauptgründen zu regulieren. Zunächst wird durch die Verwendung von-Objekten sichergestellt, dass Microsoft die Systemfunktionalität aktualisieren kann, solange die ursprüngliche Objektschnittstelle beibehalten wird. Wenn nachfolgende Versionen des Systems freigegeben werden, können Sie das aktualisierte Objekt mit geringem oder ohne zusätzliche Arbeit verwenden.

Zweitens ermöglicht die Verwendung von-Objekten das Nutzen der Windows-Sicherheit. Jedes-Objekt verfügt über eine eigene Zugriffs Steuerungs Liste (ACL), die die Aktionen angibt, die ein Prozess für das Objekt ausführen kann. Das System überprüft die ACL eines Objekts jedes Mal, wenn eine Anwendung ein Handle für das Objekt erstellt. Weitere Informationen finden Sie unter [Zugriffssteuerung](/windows/desktop/SecAuthZ/access-control).

-   [Objekt-Manager](object-manager.md)
-   [Objektschnittstelle](object-interface.md)
-   [Objektnamespaces](/windows/desktop/Sync/object-namespaces)
-   [Einschränkungen behandeln](handle-limitations.md)
-   [Behandlung von Vererbung](handle-inheritance.md)

 

 
