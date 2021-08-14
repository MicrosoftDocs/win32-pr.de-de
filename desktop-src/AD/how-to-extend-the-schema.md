---
title: Erweitern des Schemas
description: Wenn die vorhandenen Klassen und/oder Attribute nicht mit dem Datentyp passen, den Sie speichern möchten, sollten Sie das Schema erweitern.
ms.assetid: 9a80ce29-8ff0-4324-8a2f-afd6c5d2272e
ms.tgt_platform: multiple
keywords:
- Schema AD , Erweitern
- Active Directory, Using, Schema
- Active Directory, Using, Schema, Extending the Schema, How to Extend
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc30f7292c1c1077cc4e44a9f022a430af87bc3efe876a5c197b3fe370d3b95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188158"
---
# <a name="how-to-extend-the-schema"></a>Erweitern des Schemas

Wenn die vorhandenen Klassen und/oder Attribute nicht mit dem Datentyp passen, den Sie speichern möchten, sollten Sie das Schema erweitern. Weitere Informationen zur Entscheidung, wann das Schema erweitert werden soll, finden Sie unter [Erweitern des Schemas.](extending-the-schema.md) Wenn Sie entschieden haben, dass eine Schemaerweiterung erforderlich ist, gehen Sie wie folgt vor, um das Schema zu erweitern.

## <a name="verify-active-directory-functionality-before-you-apply-any-schema-extensions"></a>Überprüfen sie die Active Directory-Funktionalität, bevor Sie Schemaerweiterungen anwenden.

Überprüfen Sie die Active Directory-Funktionalität, bevor Sie das Schema aktualisieren, um sicherzustellen, dass die Schemaerweiterung fehlerfrei fortgesetzt wird. Stellen Sie mindestens sicher, dass alle Domänencontroller für die Gesamtstruktur online sind und eine eingehende Replikation durchführen.

**So überprüfen Sie die Active Directory-Funktionalität, bevor Sie die Schemaerweiterung anwenden**

1.  Melden Sie sich bei einer Administrativen Arbeitsstation an, auf der das Windows Supporttool installiert Repadmin.exe.
    > [!Note]  
    > Die Supporttools befinden sich auf dem Installationsmedium des Betriebssystems im \\ Ordner Supporttools.

     

2.  Öffnen Sie eine Eingabeaufforderung, und wechseln Sie dann in den Ordner, in dem die Windows Supporttools installiert sind.
3.  Geben Sie Folgendes an der Eingabeaufforderung ein, und drücken Sie dann die EINGABETASTE:

    ``` syntax
    repadmin /replsum /bysrc /bydest /sort:delta
    ```

    Alle Domänencontroller sollten in der Spalte Fehler den Wert 0 anzeigen, und die größten Deltas (die die Anzahl der Änderungen angeben, die seit der letzten erfolgreichen Replikation an der Active Directory-Datenbank vorgenommen wurden) sollten kleiner oder ungefähr gleich der Replikationshäufigkeit der Standortverbindung sein, die vom Domänencontroller für die Replikation verwendet wird. Die Standardreplikationsrate beträgt 180 Minuten.

    Weitere Informationen zu zusätzlichen Schritten, die Sie ausführen können, um die Active Directory-Funktionalität zu überprüfen, bevor Sie die Schemaerweiterung anwenden, finden Sie [im Artikel 325379 im Microsoft Knowledge Base](https://support.microsoft.com/kb/325379/en-us).

**So erweitern Sie das Schema**

1.  Bestimmen Sie die -Methode der Erweiterung. Nachdem Sie Ihre Schemaänderungen sorgfältig entworfen haben, müssen Sie im nächsten Schritt entscheiden, welche Methode zum Erweitern des Schemas verwendet werden soll. Wählen Sie eine der folgenden Methoden:
    -   Manuelles Importieren von Dateien. Weitere Informationen finden Sie in der Dokumentation [unter Verwenden des LDIFDE-Tools.](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))
        > [!Note]  
        > Verwenden Sie LDIFDE nicht, um Windows \* SCH-LDF-Dateien zu importieren. Diese Dateien sind erforderlich, um das Active Directory-Schema zu erweitern, um Domänencontroller zu installieren, die eine neuere Version von Windows Server ausführen als die Version, die auf dem aktuellen Schemamaster ausgeführt wird. Wenn Sie das Schema erweitern müssen, um einen neuen Domänencontroller zu installieren, verwenden Sie Adprep.exe.

         

    -   Programmgesteuert mithilfe eines Installationsprogramms. Weitere Informationen finden Sie unter [Programmgesteuerte Erweiterung.](programmatic-extension.md)
2.  Aktivieren Sie Schemaänderungen. Weitere Informationen finden Sie unter [Prerequisites for Installing a Schema Extension (Voraussetzungen für die Installation einer Schemaerweiterung)](prerequisites-for-installing-a-schema-extension.md) und [Enabling Schema Changes at the Schema Master (Aktivieren von Schemaänderungen auf dem Schemamaster).](enabling-schema-changes-at-the-schema-master.md)
3.  Rufen Sie einen Objektbezeichner (OID) für Ihre neuen Attribute und/oder Klassen ab, wie unter [Abrufen eines Objektbezeichners](obtaining-an-object-identifier.md)beschrieben.
4.  Erstellen Sie neue Attribute und Klassen.
5.  Verwenden Sie Anzeigespezifizierer, um bei Bedarf neue Attribute und Klassen in die Benutzeroberfläche zu integrieren.
6.  Aktualisieren Sie den Schemacache wie unter [Aktualisieren des Schemacaches](updating-the-schema-cache.md)beschrieben.
7.  Überprüfen Sie die Schemaerweiterung mit LDP.exe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abrufen eines Objektbezeichners](obtaining-an-object-identifier.md)
</dt> <dt>

[Die neuen Befehlszeilentools für Active Directory in Windows Server 2003](https://support.microsoft.com/kb/298882)
</dt> <dt>

[Verwenden des LDIFDE-Tools](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))
</dt> <dt>

[Erweitern des Active Directory-Schemas](/previous-versions/ms806972(v=msdn.10))
</dt> <dt>

[Einschränkungen bei der Schemaerweiterung](restrictions-on-schema-extension.md)
</dt> </dl>

 

 