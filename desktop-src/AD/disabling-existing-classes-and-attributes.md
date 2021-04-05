---
title: Deaktivieren vorhandener Klassen und Attribute
description: Schema Ergänzungen sind permanent.
ms.assetid: 13ffd2f5-cf1d-4cde-a3d5-74cb5a44b6fc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74863d0d3c72f383259cfe262f4b7aa6fa27774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707715"
---
# <a name="disabling-existing-classes-and-attributes"></a>Deaktivieren vorhandener Klassen und Attribute

Schema Ergänzungen sind permanent. **AttributeSchema** -und **classSchema** -Objekte können nicht gelöscht werden. In einem verteilten System ist es schwierig sicherzustellen, dass keine Instanzen einer bestimmten Klasse oder eines Attributs vorhanden sind. Wenn Sie die Definition einer Klasse oder eines Attributs entfernen, werden vorhandene Instanzen dieser Klasse oder dieses Attributs beschädigt.

Sie können eine vorhandene Klasse oder ein vorhandenes Attribut deaktivieren, indem Sie es als "veraltet" markieren. Dies wirkt sich nicht auf vorhandene Instanzen der Klasse oder des Attributs aus, die so gekennzeichnet sind, verhindert jedoch die Erstellung neuer Instanzen.

Beim Deaktivieren von Schema Klassen und Attributen gelten die folgenden Einschränkungen:

-   Eine Klasse oder ein Attribut der Kategorie 1 kann nicht deaktiviert werden.
-   Ein Attribut, das ein Member einer Klasse ist, die nicht gleichzeitig deaktiviert ist, kann nicht deaktiviert werden. Dies liegt daran, dass ein Attribut möglicherweise für die (nicht deaktivierte) Klasse erforderlich ist, und durch das Deaktivieren des-Attributs wird verhindert, dass neue Instanzen der-Klasse erstellt werden.

Um ein Attribut zu deaktivieren, legen Sie das **isDefunct** -Attribut seines **attributeSchema** -Objekts auf " **true**" fest. Wenn ein Attribut deaktiviert ist, können keine neuen Instanzen des Attributs erstellt werden. Um das Attribut erneut zu aktivieren, legen Sie das **IsDebug** -Attribut auf " **false**" fest.

Um eine Klasse zu deaktivieren, legen Sie das **isDefunct** -Attribut seines **classSchema** -Objekts auf " **true**" fest. Wenn eine Klasse deaktiviert ist, können keine neuen Instanzen der Klasse erstellt werden. Zum erneuten Aktivieren der-Klasse legen Sie das **isDefunct** -Attribut auf " **false**" fest.

Das Festlegen von Schema Objekten als veraltet kann in Produktionsumgebungen nützlich sein. Wenn eine Testversion einer Schema Erweiterung nicht mehr benötigt wird, markieren Sie Sie als veraltet. Sie können es wiederherstellen, indem Sie das Attribut **IsOut** entfernen oder den Attribut Wert auf **false** festlegen. Dies schützt auch vor einem unbeabsichtigten Entfernen eines Schema Objekts, indem es auf "veraltet" festgelegt wird, da der Vorgang problemlos rückgängig gemacht werden kann.

Beachten Sie, dass der Active Directory Server vorhandene Instanzen eines Attributs oder einer Klasse nicht bereinigt, wenn Sie ein Schema Objekt defunct machen. Wenn Sie die **IsDebug** -Eigenschaft entfernen, werden alle Instanzen zu gültigen, normalen Objekten.

Die folgende Liste enthält weitere Konsequenzen, die das Markieren eines **attributeSchema** -oder **classSchema** -Objekts außer Kraft setzen:

-   Das Hinzufügen oder Ändern einer Instanz schlägt fehl.
-   Fehlercodes Verhalten sich so, als ob eine veraltete Klasse nie vorhanden wäre.
-   Suchen und löschen Verhalten sich so, als ob keine Schema Objekte außer Kraft gesetzt wurden.
-   Nur das Löschen des gesamten Attributs aus dem Objekt zulassen.

In der folgenden Liste sind zusätzliche Optionen in einer Produktionsumgebung enthalten, um die Auswirkungen von veralteten Schema Erweiterungen zu verringern:

-   Entfernen Sie alle " **mayhave** "-Attributwerte aus einer veralteten Klasse.
-   Reduzieren Sie die Größe aller **musthave** -Attributwerte von einer veralteten Klasse.
-   Entfernen eines veralteten Attributs aus dem globalen Katalog.
-   Entfernen eines veralteten Attributs aus einem beliebigen Index.

Weitere Optionen zum Entfernen unerwünschter Schema Änderungen in einer Produktionsumgebung sind für Entwickler die Verwendung eines privaten Domänen Controllers zum Testen. In diesem Fall können Sie folgende Aktionen ausführen:

-   Setzen Sie den Active Directory Server mit Dcpromo.exe, um den DC herabzusetzen. Nachdem die Herabstufung abgeschlossen ist, verwenden Sie Dcpromo.exe erneut, um den Server wieder zu einem Domänen Controller heraufzustufen. Der Entwickler kann dann LDIF-Skripts verwenden, um alle erforderlichen Klassen, Attribute und Objektinstanzen neu zu laden.
-   Verwenden Sie Ntbackup.exe, um eine Systemstatus Sicherung auf eine verfügbare Datenträger Partition auszuführen. Starten Sie den Wiederherstellungs Modus für den sicheren/Verzeichnisdienst wieder her.

Wenn Sie für Windows Server 2003-Betriebssysteme eine Klasse oder ein Attribut auf "veraltet" festlegen, können Sie die Werte für " **ldapDisplayName**", " **schemaIdGUID**", " **OID** " und " **mapiId** " des veralteten Schema Elements sofort wieder verwenden, wenn Sie eine neue Klasse oder ein neues Attribut erstellen, um es zu ersetzen. Die veraltete Version der Klasse oder des Attributs wird im Schema Container verwaltet, aber im MMC-Snap-in ausgeblendet. Wenn Sie das alte Schema Element reaktivieren möchten, legen Sie **IsDebug** auf **false** fest.

Im folgenden LDIF-Codebeispiel wird veranschaulicht, wie das **isDefunct** -Attribut geändert und der RDN so geändert wird, dass es nicht mit der neuen Klasse verwechselt wird, die Sie zum Ersetzen von erstellt haben.

``` syntax
 dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modify
   replace: isDefunct
   isDefunct: TRUE
   -

   dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modrdn
   newrdn: cn=MyClassOld
   deleteoldrdn: 1

   dn:
   changetype: modify
   add: schemaUpdateNow
   schemaUpdateNow: 1
   -
```

Verwenden Sie den folgenden Befehl, um das LDIF-Codebeispiel für eine Gesamtstruktur eines Computers auszuführen, auf dem Windows Server 2003-Betriebssysteme ausgeführt werden.

**LDIF/i/f RDN. ldf/c "DC = X" "DC = MyDomain, DC = com"**

(Wobei "DC = X" eine Konstante ist)

 

 




