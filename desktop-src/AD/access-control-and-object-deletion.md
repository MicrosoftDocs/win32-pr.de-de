---
title: Löschen von Access Control und Objekten
description: Mit Active Directory können Sie ein Objekt löschen, wenn Sie über Lösch Zugriff auf das Objekt verfügen, oder wenn Sie über einen unter \_ \_ \_ \_ geordneten Zugriff auf den Objekttyp des übergeordneten Containers verfügen.
ms.assetid: 87027c25-e3c9-4bad-8df3-cb6205e40ef6
ms.tgt_platform: multiple
keywords:
- AD-Access Control und Objekt Löschung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bddcd2b563e144743689f2a26c17bd417db14ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724376"
---
# <a name="access-control-and-object-deletion"></a>Löschen von Access Control und Objekten

Active Directory Domain Services können Sie ein Objekt löschen, wenn Sie über eine der folgenden Zugriffsrechte verfügen:

-   Löschen Sie den Zugriff auf das Objekt selbst.
-   ADS \_ right \_ DS \_ Löschen \_ des untergeordneten Zugriffs für diesen Objekttyp für den übergeordneten Container

Beachten Sie, dass das System die Sicherheits Beschreibung für das Objekt und dessen übergeordnetes Element überprüft, bevor der Löschvorgang verweigert wird. Dies bedeutet, dass ein ACE, der den Lösch Zugriff für einen Benutzer explizit verweigert, keine Auswirkung hat, wenn der Benutzer \_ Zugriff auf das übergeordnete Element untergeordneter Elemente hat. Ebenso kann ein ACE, der \_ den Zugriff auf das übergeordnete Element löschen verweigert, überschrieben werden, wenn für das Objekt selbst der Lösch Zugriff zulässig ist.

Zum Ausführen eines Struktur-DELETE-Vorgangs (z. b. mit der [**iadsdeleteops::D eleteobject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) -Methode) benötigen Sie ADS, die den \_ \_ \_ \_ Zugriff auf das Objekt mit der rechten DS-Berechtigung "Löschen" haben. Wenn Sie über dieses Zugriffsrecht verfügen, können Sie das Objekt und alle untergeordneten Objekte unabhängig von den Schutzmaßnahmen für die untergeordneten Objekte löschen. Um eine Struktur zu löschen, wenn Sie nicht über Werbeeinblendungen zum \_ \_ Löschen der Struktur verfügen \_ \_ , müssen Sie die Struktur rekursiv durchlaufen und die einzelnen Objekte einzeln löschen. In diesem Fall müssen Sie \_ für jedes Objekt in der Struktur über den erforderlichen untergeordneten Zugriff zum Löschen oder Löschen verfügen.

> [!WARNING]
> Wenn Benutzer über ADS verfügen, die über die Berechtigung zum \_ \_ \_ Löschen \_ von Struktur Zugriff für ein Objekt verfügen, können Sie dadurch eine gesamte Unterstruktur löschen, einschließlich aller untergeordneten Objekte. Aus diesem Grund können Sie das Aufheben der Zugriffsberechtigung "Unterstruktur löschen" für alle Benutzer eines übergeordneten Containers in Erwägung gezogen.

 

 

 