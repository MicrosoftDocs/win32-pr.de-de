---
title: Empfehlungen für Schemaerweiterungsanwendungen
description: Dieses Thema enthält Empfehlungen für Schemaerweiterungsanwendungen.
ms.assetid: 615e927e-a113-4557-b354-55a208a649eb
ms.tgt_platform: multiple
keywords:
- Empfehlungen für Schemaerweiterungsanwendungen AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0a01e68fbe9751b778caa2404d02afb1ddd7704457c9cf0aedcc914387ab5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025268"
---
# <a name="recommendations-for-schema-extension-applications"></a>Empfehlungen für Schemaerweiterungsanwendungen

Zusätzlich zu den Voraussetzungen werden die folgenden bewährten Methoden für Schemaerweiterungsanwendungen empfohlen:

-   Suchen Sie den Schemamaster. Binden Sie an das Schema auf dem Domänencontroller, der der Schemamaster ist. Vermeiden Sie unnötige Änderungen der Schemamasterrolle zwischen DCs. So binden Sie an den Schemacontainer auf dem Schemamaster. Weitere Informationen finden Sie unter [Voraussetzungen für die Installation einer Schemaerweiterung.](prerequisites-for-installing-a-schema-extension.md)
-   Überprüfen Sie vor dem Ausführen einer Aktion die **allowedChildClassesEffective-Eigenschaft** des Schemacontainers, um sicherzustellen, dass Sie Attribute und/oder Klassen erstellen können. Wenn **attributeSchema** und **classSchema** keine Werte in dieser Eigenschaft sind, verfügen Sie nicht über ausreichende Rechte zum Hinzufügen von Attributen oder Klassen zum Schema. Weitere Informationen finden Sie unter [Beispielcode für die Überprüfung auf Rechte zum Erstellen von Schemaobjekten.](example-code-for-checking-for-rights-to-create-schema-objects.md)
-   Stellen Sie sicher, dass die Zulässige Schemaaktualisierung in der Registrierung des Schemamasters entsprechend festgelegt ist. Um diesen Wert zu erstellen oder festzulegen, stellen Sie ihn im Rahmen der Bereinigungsroutine Ihrer Anwendung in den ursprünglichen Zustand zurück. Weitere Informationen zum Überprüfen und Festlegen dieses Werts finden Sie unter [Enabling Schema Changes at the Schema Master](enabling-schema-changes-at-the-schema-master.md).
-   Stellen Sie vor dem Hinzufügen von Attributen oder Klassen sicher, dass sie noch nicht vorhanden sind. Wenn sie vorhanden sind, stellen Sie sicher, dass es sich um die gleichen Attribute oder Klassen handelt, die Sie hinzufügen, und nicht um ein Attribut oder eine Klasse, die von einer Person mit unterschiedlicher Syntax und Eigenschaften erstellt wurde, die mit Ihren Attributen oder Klassen nicht kompatibel sind.

    Fragen Sie für Attribute **cn**, **attributeID**, **governsID,** **lDAPDisplayName** und **schemaIDGUID** ab, um sicherzustellen, dass sie nicht bereits verwendet werden. Wenn Sie eine Reihe von verknüpften Attributen hinzufügen (eine Weiterleitungslink, eine Zurück-Verknüpfung), stellen Sie sicher, dass die **linkID-Attribute** nicht bereits verwendet werden. Abfrage für **governsID,** da der Objektbezeichner (OID) für Attribute und Klassen eindeutig sein muss.

    Fragen Sie für Klassen **nach cn**, **governsID,** **attributeID,** **lDAPDisplayName** und **schemaIDGUID** ab, um sicherzustellen, dass sie nicht bereits verwendet werden. Fragen Sie **attributeID** ab, da die OID zwischen Klassen und Attributen eindeutig sein muss.

    Weitere Informationen zur Überprüfung auf Namenskonflikte finden Sie unter [Beispielcode zum Erkennen von Schemabenennungskonflikten.](example-code-for-detecting-schema-naming-collisions.md)

    Wenn Attribute oder Klassen vorhanden sind, die mit ihren neuen Attributen oder Klassen in Konflikt stehen, sollte Ihre Anwendung ihre Schemaänderungen nicht anwenden.

-   Wenn ein solcher Konflikt vorhanden ist, sollte Ihre Anwendung Ihre Schemaänderungen nicht anwenden. Möglicherweise muss der Schemaadministrator den Konflikt beheben und die Anwendung dann erneut ausführen. Alternativ kann ein anderer **lDAPDisplayName** verwendet werden. Allerdings müssen alle Anwendungen, die das Attribut oder Objekt verwenden, diese Änderung berücksichtigen. Um OID-Konflikte zu vermeiden, rufen Sie eine OID von einer ISO-Namensregistrierungsstelle ab.
-   Wenn Ihre Anwendung von Attributen oder Klassen abhängig ist, die sie hinzugefügt hat, aktualisieren Sie den Schemacache, bevor Sie die neuen Attribute oder Klassen hinzufügen, die von diesen Attributen oder Klassen abhängig sind. Beachten Sie, dass das **schemaUpdateNow-Betriebsattribut** synchron ist. Das heißt, der Aufruf der [**IADs::P ut-Methode**](/windows/desktop/api/iads/nf-iads-iads-put) wird blockiert, bis der Schemacache aktualisiert wird. Wenn der Aufruf zurückgegeben wird, wurde der Schemacache aktualisiert, und auf die neuen Attribute und/oder Klassen kann zugegriffen werden.

    Weitere Informationen zum Aktualisieren des Schemacaches finden Sie unter [Beispielcode zum Aktualisieren des Schemacaches.](example-code-for-updating-the-schema-cache.md)

 

 