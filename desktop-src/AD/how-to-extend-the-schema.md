---
title: Erweitern des Schemas
description: Wenn die vorhandenen Klassen und/oder Attribute nicht in den Datentyp passen, den Sie speichern möchten, können Sie das Schema erweitern.
ms.assetid: 9a80ce29-8ff0-4324-8a2f-afd6c5d2272e
ms.tgt_platform: multiple
keywords:
- Schema-AD, erweitern
- Active Directory, verwenden von, Schema
- Active Directory, verwenden von Schema, Erweitern des Schemas, Erweitern des Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437b23229182e6ec6f94b500feb764b4bbcf06e7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724496"
---
# <a name="how-to-extend-the-schema"></a>Erweitern des Schemas

Wenn die vorhandenen Klassen und/oder Attribute nicht in den Datentyp passen, den Sie speichern möchten, können Sie das Schema erweitern. Weitere Informationen zur Entscheidung, wann das Schema erweitert werden soll, finden Sie unter [Erweitern des Schemas](extending-the-schema.md). Wenn Sie entschieden haben, dass eine Schema Erweiterung erforderlich ist, verwenden Sie das folgende Verfahren, um das Schema zu erweitern.

## <a name="verify-active-directory-functionality-before-you-apply-any-schema-extensions"></a>Überprüfen der Active Directory Funktionalität vor dem Anwenden von Schema Erweiterungen

Überprüfen Sie Active Directory Funktionalität, bevor Sie das Schema aktualisieren, um sicherzustellen, dass die Schema Erweiterung ohne Fehler fortgesetzt wird. Stellen Sie mindestens sicher, dass alle Domänen Controller für die Gesamtstruktur online sind und die eingehende Replikation durchgeführt wird.

**So überprüfen Sie Active Directory Funktionalität vor dem Anwenden der Schema Erweiterung**

1.  Melden Sie sich bei einer administrativen Arbeitsstation an, auf der das Windows-Support Tool Repadmin.exe installiert ist.
    > [!Note]  
    > Die Support Tools befinden sich im Ordner "Support Tools" auf dem Installationsmedium des Betriebssystems \\ .

     

2.  Öffnen Sie eine Eingabeaufforderung, und ändern Sie dann die Verzeichnisse in den Ordner, in dem die Windows-Support Tools installiert sind.
3.  Geben Sie Folgendes an der Eingabeaufforderung ein, und drücken Sie dann die EINGABETASTE:

    ``` syntax
    repadmin /replsum /bysrc /bydest /sort:delta
    ```

    Auf allen Domänen Controllern sollte in der Spalte Fehler der Wert 0 angezeigt werden, und die größten Delta-Daten (die angeben, wie viele Änderungen seit der letzten erfolgreichen Replikation an der Active Directory Datenbank vorgenommen wurden) sollten kleiner oder ungefähr gleich der Replikations Häufigkeit der Standort Verknüpfung sein, die vom Domänen Controller für die Replikation verwendet wird. Die Standardreplikationsrate beträgt 180 Minuten.

    Weitere Informationen zu zusätzlichen Schritten, die Sie ausführen können, um Active Directory Funktionalität zu überprüfen, bevor Sie die Schema Erweiterung anwenden, finden Sie [im Artikel 325379 in der Microsoft Knowledge Base](https://support.microsoft.com/kb/325379/en-us).

**So erweitern Sie das Schema**

1.  Bestimmen Sie die Erweiterungsmethode. Nachdem Sie die Schema Änderungen sorgfältig entworfen haben, besteht der nächste Schritt in der Entscheidung, welche Methode zum Erweitern des Schemas verwendet werden soll. Wählen Sie eine der folgenden Methoden:
    -   Manuell, mithilfe von Import Dateien. Weitere Informationen finden Sie in der Dokumentation [unter Verwendung des LDIF-Tools](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).
        > [!Note]  
        > Verwenden Sie LDIFDE nicht, um Windows Sch \* . LDF-Dateien zu importieren. Diese Dateien sind erforderlich, um das Active Directory Schema zu erweitern, um Domänen Controller zu installieren, auf denen eine neuere Version von Windows Server ausgeführt wird als die Version, die auf dem aktuellen Schema Master ausgeführt wird. Wenn Sie das Schema erweitern müssen, um einen neuen Domänen Controller zu installieren, verwenden Sie Adprep.exe.

         

    -   Programm gesteuert mithilfe eines Installationsprogramms. Weitere Informationen finden Sie Unterprogramm gesteuerte [Erweiterung](programmatic-extension.md) .
2.  Aktivieren von Schema Änderungen. Weitere Informationen finden Sie unter [Voraussetzungen für das Installieren einer Schema Erweiterung](prerequisites-for-installing-a-schema-extension.md) und [Aktivieren von Schema Änderungen am Schema Master](enabling-schema-changes-at-the-schema-master.md).
3.  Rufen Sie einen Objekt Bezeichner (OID) für Ihre neuen Attribute und/oder Klassen ab, wie unter Abrufen [eines Objekt Bezeichners](obtaining-an-object-identifier.md)beschrieben.
4.  Erstellen Sie neue Attribute und Klassen.
5.  Verwenden Sie die Anzeige spezifiken, um neue Attribute und Klassen bei Bedarf in die Benutzeroberfläche zu integrieren.
6.  Aktualisieren Sie den Schema Cache, wie in [Aktualisieren des Schema Caches](updating-the-schema-cache.md)beschrieben.
7.  Überprüfen Sie die Schema Erweiterung mithilfe LDP.exe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abrufen eines Objekt Bezeichners](obtaining-an-object-identifier.md)
</dt> <dt>

[Die neuen Befehlszeilen Tools für Active Directory in Windows Server 2003](https://support.microsoft.com/kb/298882)
</dt> <dt>

[Verwenden des LDIF-Tools](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))
</dt> <dt>

[Erweitern des Active Directory-Schemas](/previous-versions/ms806972(v=msdn.10))
</dt> <dt>

[Einschränkungen bei der Schema Erweiterung](restrictions-on-schema-extension.md)
</dt> </dl>

 

 