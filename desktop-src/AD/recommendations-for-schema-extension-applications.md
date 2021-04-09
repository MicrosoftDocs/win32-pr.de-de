---
title: Empfehlungen für Schema Erweiterungs Anwendungen
description: Dieses Thema enthält Empfehlungen für Schema Erweiterungs Anwendungen.
ms.assetid: 615e927e-a113-4557-b354-55a208a649eb
ms.tgt_platform: multiple
keywords:
- Empfehlungen für Schema Erweiterungs Anwendungen AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2393211eb910ce4bc490667398da7f38d212ddcf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101430"
---
# <a name="recommendations-for-schema-extension-applications"></a>Empfehlungen für Schema Erweiterungs Anwendungen

Zusätzlich zu den Voraussetzungen werden die folgenden bewährten Methoden für Schema Erweiterungs Anwendungen empfohlen:

-   Suchen Sie den Schema Master. Binden Sie an das Schema auf dem Domänen Controller, der der Schema Master ist. Vermeiden Sie unnötige Änderungen an der Schema Master Rolle zwischen DCS. Zum Binden an den Schema Container auf dem Schema Master. Weitere Informationen finden Sie unter [Voraussetzungen für das Installieren einer Schema Erweiterung](prerequisites-for-installing-a-schema-extension.md).
-   Bevor Sie eine Aktion ausführen, überprüfen Sie die Eigenschaft " **zudem** Schema Container", um zu überprüfen, ob Sie Attribute und/oder Klassen erstellen können. Wenn **attributeSchema** und **classSchema** keine Werte in dieser Eigenschaft sind, verfügen Sie nicht über ausreichende Rechte zum Hinzufügen von Attributen oder Klassen zum Schema. Weitere Informationen finden Sie unter [Beispiel Code für die Überprüfung der Rechte zum Erstellen von Schema Objekten](example-code-for-checking-for-rights-to-create-schema-objects.md).
-   Stellen Sie sicher, dass die zulässige Schema Aktualisierung in der Registrierung des Schema Masters ordnungsgemäß festgelegt ist. Um diesen Wert zu erstellen oder festzulegen, stellen Sie ihn im Rahmen der Bereinigungs Routine Ihrer Anwendung in seinem ursprünglichen Zustand wieder her. Weitere Informationen zum Überprüfen und Festlegen dieses Werts finden Sie unter [Aktivieren von Schema Änderungen am Schema Master](enabling-schema-changes-at-the-schema-master.md).
-   Bevor Sie Attribute oder Klassen hinzufügen, stellen Sie sicher, dass Sie nicht bereits vorhanden sind. Wenn Sie vorhanden sind, überprüfen Sie, ob es sich um die gleichen Attribute oder Klassen handelt, die Sie hinzufügen, und nicht um ein Attribut oder eine Klasse, die von einem Benutzer mit unterschiedlicher Syntax und Eigenschaften erstellt werden, die nicht mit ihren Attributen

    Fragen Sie für Attribute nach **CN**, **attributeId**, **governsId**, **ldapDisplayName** und **schemaIdGUID** ab, um sicherzustellen, dass Sie nicht bereits verwendet werden. Wenn Sie einen Satz verknüpfter Attribute (einen vorwärts Link, einen Back-Link) hinzufügen, stellen Sie sicher, dass die **linkid** s nicht bereits verwendet werden. Eine Abfrage für die **governsId** , da der Objekt Bezeichner (OID) unter Attributen und Klassen eindeutig sein muss.

    Fragen Sie für Klassen nach **CN**, **governsId**, **attributeId**, **ldapDisplayName** und **schemaIdGUID** ab, um sicherzustellen, dass Sie nicht bereits verwendet werden. Die Abfrage von **attributeId** , da die OID in Klassen und Attributen eindeutig sein muss.

    Weitere Informationen zum Überprüfen von Namenskollisionen finden Sie unter [Beispiel Code zum Erkennen von Schema Namenskollisionen](example-code-for-detecting-schema-naming-collisions.md).

    Wenn Attribute oder Klassen vorhanden sind, die mit den neuen Attributen oder Klassen in Konflikt stehen, sollte Ihre Anwendung ihre Schema Änderungen nicht anwenden.

-   Wenn eine solche Kollision vorhanden ist, sollte Ihre Anwendung ihre Schema Änderungen nicht anwenden. Der Schema Administrator muss möglicherweise die Kollision auflösen und die Anwendung dann erneut ausführen. Alternativ kann ein anderer **ldapDisplayName** verwendet werden. Allerdings müssen alle Anwendungen, die das-Attribut oder das-Objekt verwenden, diese Änderung beachten. Um OID-Konflikte zu vermeiden, sollten Sie eine OID von einer ISO-namens Registrierungsstelle abrufen.
-   Wenn Ihre Anwendung von Attributen oder Klassen abhängig ist, die Sie hinzugefügt hat, aktualisieren Sie den Schema Cache, bevor Sie die neuen Attribute oder Klassen hinzufügen, die von diesen Attributen oder Klassen abhängig sind. Beachten Sie, dass das Attribut " **schemaUpdateNow** Operational" synchron ist. Das heißt, der [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) -Methodenaufrufe wird blockiert, bis der Schema Cache aktualisiert wird. Wenn der Aufruf zurückgegeben wird, wurde der Schema Cache aktualisiert, und die neuen Attribute und/oder Klassen können aufgerufen werden.

    Weitere Informationen zum Aktualisieren des Schema Caches finden Sie unter [Beispiel Code zum Aktualisieren des Schema Caches](example-code-for-updating-the-schema-cache.md).

 

 