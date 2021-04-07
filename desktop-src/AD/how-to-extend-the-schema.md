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
# <a name="how-to-extend-the-schema"></a><span data-ttu-id="9984f-106">Erweitern des Schemas</span><span class="sxs-lookup"><span data-stu-id="9984f-106">How to Extend the Schema</span></span>

<span data-ttu-id="9984f-107">Wenn die vorhandenen Klassen und/oder Attribute nicht in den Datentyp passen, den Sie speichern möchten, können Sie das Schema erweitern.</span><span class="sxs-lookup"><span data-stu-id="9984f-107">When the existing classes and/or attributes do not fit with the type of data that you want to store, you might want to extend the schema.</span></span> <span data-ttu-id="9984f-108">Weitere Informationen zur Entscheidung, wann das Schema erweitert werden soll, finden Sie unter [Erweitern des Schemas](extending-the-schema.md).</span><span class="sxs-lookup"><span data-stu-id="9984f-108">For more information on deciding when to extend the schema, see [Extending the Schema](extending-the-schema.md).</span></span> <span data-ttu-id="9984f-109">Wenn Sie entschieden haben, dass eine Schema Erweiterung erforderlich ist, verwenden Sie das folgende Verfahren, um das Schema zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="9984f-109">When you have decided that schema extension is required, use the following procedure to extend the schema.</span></span>

## <a name="verify-active-directory-functionality-before-you-apply-any-schema-extensions"></a><span data-ttu-id="9984f-110">Überprüfen der Active Directory Funktionalität vor dem Anwenden von Schema Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="9984f-110">Verify Active Directory functionality before you apply any schema extensions</span></span>

<span data-ttu-id="9984f-111">Überprüfen Sie Active Directory Funktionalität, bevor Sie das Schema aktualisieren, um sicherzustellen, dass die Schema Erweiterung ohne Fehler fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="9984f-111">Verify Active Directory functionality before you update the schema to help ensure that the schema extension proceeds without error.</span></span> <span data-ttu-id="9984f-112">Stellen Sie mindestens sicher, dass alle Domänen Controller für die Gesamtstruktur online sind und die eingehende Replikation durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9984f-112">At a minimum, ensure that all domain controllers for the forest are online and performing inbound replication.</span></span>

<span data-ttu-id="9984f-113">**So überprüfen Sie Active Directory Funktionalität vor dem Anwenden der Schema Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="9984f-113">**To verify Active Directory functionality before you apply the schema extension**</span></span>

1.  <span data-ttu-id="9984f-114">Melden Sie sich bei einer administrativen Arbeitsstation an, auf der das Windows-Support Tool Repadmin.exe installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9984f-114">Log on to an administrative workstation that has the Windows Support Tool Repadmin.exe installed.</span></span>
    > [!Note]  
    > <span data-ttu-id="9984f-115">Die Support Tools befinden sich im Ordner "Support Tools" auf dem Installationsmedium des Betriebssystems \\ .</span><span class="sxs-lookup"><span data-stu-id="9984f-115">The Support Tools are located on the operating system installation media in the Support\\Tools folder.</span></span>

     

2.  <span data-ttu-id="9984f-116">Öffnen Sie eine Eingabeaufforderung, und ändern Sie dann die Verzeichnisse in den Ordner, in dem die Windows-Support Tools installiert sind.</span><span class="sxs-lookup"><span data-stu-id="9984f-116">Open a command prompt, and then change directories to the folder in which the Windows Support Tools are installed.</span></span>
3.  <span data-ttu-id="9984f-117">Geben Sie Folgendes an der Eingabeaufforderung ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="9984f-117">At a command prompt, type the following, and then press ENTER:</span></span>

    ``` syntax
    repadmin /replsum /bysrc /bydest /sort:delta
    ```

    <span data-ttu-id="9984f-118">Auf allen Domänen Controllern sollte in der Spalte Fehler der Wert 0 angezeigt werden, und die größten Delta-Daten (die angeben, wie viele Änderungen seit der letzten erfolgreichen Replikation an der Active Directory Datenbank vorgenommen wurden) sollten kleiner oder ungefähr gleich der Replikations Häufigkeit der Standort Verknüpfung sein, die vom Domänen Controller für die Replikation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9984f-118">All domain controllers should show 0 in the Fails column, and the largest deltas (which indicate the number of changes that have been made to the Active Directory database since the last successful replication) should be less than or roughly equal to the replication frequency of the site link that is used by the domain controller for replication.</span></span> <span data-ttu-id="9984f-119">Die Standardreplikationsrate beträgt 180 Minuten.</span><span class="sxs-lookup"><span data-stu-id="9984f-119">The default replication frequency is 180 minutes.</span></span>

    <span data-ttu-id="9984f-120">Weitere Informationen zu zusätzlichen Schritten, die Sie ausführen können, um Active Directory Funktionalität zu überprüfen, bevor Sie die Schema Erweiterung anwenden, finden Sie [im Artikel 325379 in der Microsoft Knowledge Base](https://support.microsoft.com/kb/325379/en-us).</span><span class="sxs-lookup"><span data-stu-id="9984f-120">For more information about additional steps that you can take to verify Active Directory functionality before you apply the schema extension, see [article 325379 in the Microsoft Knowledge Base](https://support.microsoft.com/kb/325379/en-us).</span></span>

<span data-ttu-id="9984f-121">**So erweitern Sie das Schema**</span><span class="sxs-lookup"><span data-stu-id="9984f-121">**To Extend the Schema**</span></span>

1.  <span data-ttu-id="9984f-122">Bestimmen Sie die Erweiterungsmethode.</span><span class="sxs-lookup"><span data-stu-id="9984f-122">Determine the method of extension.</span></span> <span data-ttu-id="9984f-123">Nachdem Sie die Schema Änderungen sorgfältig entworfen haben, besteht der nächste Schritt in der Entscheidung, welche Methode zum Erweitern des Schemas verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9984f-123">Once you have carefully designed your schema changes, the next step is to decide which method to use to extend the schema.</span></span> <span data-ttu-id="9984f-124">Wählen Sie eine der folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="9984f-124">You can use one of the following methods:</span></span>
    -   <span data-ttu-id="9984f-125">Manuell, mithilfe von Import Dateien.</span><span class="sxs-lookup"><span data-stu-id="9984f-125">Manually, using import files.</span></span> <span data-ttu-id="9984f-126">Weitere Informationen finden Sie in der Dokumentation [unter Verwendung des LDIF-Tools](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).</span><span class="sxs-lookup"><span data-stu-id="9984f-126">See the documentation [Using the LDIFDE Tool](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).</span></span>
        > [!Note]  
        > <span data-ttu-id="9984f-127">Verwenden Sie LDIFDE nicht, um Windows Sch \* . LDF-Dateien zu importieren.</span><span class="sxs-lookup"><span data-stu-id="9984f-127">Do not use LDIFDE to import Windows Sch\*.ldf files.</span></span> <span data-ttu-id="9984f-128">Diese Dateien sind erforderlich, um das Active Directory Schema zu erweitern, um Domänen Controller zu installieren, auf denen eine neuere Version von Windows Server ausgeführt wird als die Version, die auf dem aktuellen Schema Master ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9984f-128">Those files are required to extend the Active Directory schema in order to install domain controllers that run a newer version of Windows Server than the version that is running on the current schema master.</span></span> <span data-ttu-id="9984f-129">Wenn Sie das Schema erweitern müssen, um einen neuen Domänen Controller zu installieren, verwenden Sie Adprep.exe.</span><span class="sxs-lookup"><span data-stu-id="9984f-129">When you need to extend the schema in order to install a new domain controller, use Adprep.exe.</span></span>

         

    -   <span data-ttu-id="9984f-130">Programm gesteuert mithilfe eines Installationsprogramms.</span><span class="sxs-lookup"><span data-stu-id="9984f-130">Programmatically, using an installation program.</span></span> <span data-ttu-id="9984f-131">Weitere Informationen finden Sie Unterprogramm gesteuerte [Erweiterung](programmatic-extension.md) .</span><span class="sxs-lookup"><span data-stu-id="9984f-131">For more information, see [Programmatic Extension](programmatic-extension.md)</span></span>
2.  <span data-ttu-id="9984f-132">Aktivieren von Schema Änderungen.</span><span class="sxs-lookup"><span data-stu-id="9984f-132">Enable Schema Changes.</span></span> <span data-ttu-id="9984f-133">Weitere Informationen finden Sie unter [Voraussetzungen für das Installieren einer Schema Erweiterung](prerequisites-for-installing-a-schema-extension.md) und [Aktivieren von Schema Änderungen am Schema Master](enabling-schema-changes-at-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="9984f-133">For more information, see [Prerequisites for Installing a Schema Extension](prerequisites-for-installing-a-schema-extension.md) and [Enabling Schema Changes at the Schema Master](enabling-schema-changes-at-the-schema-master.md).</span></span>
3.  <span data-ttu-id="9984f-134">Rufen Sie einen Objekt Bezeichner (OID) für Ihre neuen Attribute und/oder Klassen ab, wie unter Abrufen [eines Objekt Bezeichners](obtaining-an-object-identifier.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9984f-134">Obtain an Object Identifier (OID) for your new attributes and/or classes, as described in [Obtaining an Object Identifier](obtaining-an-object-identifier.md).</span></span>
4.  <span data-ttu-id="9984f-135">Erstellen Sie neue Attribute und Klassen.</span><span class="sxs-lookup"><span data-stu-id="9984f-135">Create new attributes and classes.</span></span>
5.  <span data-ttu-id="9984f-136">Verwenden Sie die Anzeige spezifiken, um neue Attribute und Klassen bei Bedarf in die Benutzeroberfläche zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="9984f-136">Use display specifiers to integrate new attributes and classes with the user interface, if necessary.</span></span>
6.  <span data-ttu-id="9984f-137">Aktualisieren Sie den Schema Cache, wie in [Aktualisieren des Schema Caches](updating-the-schema-cache.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9984f-137">Update the schema cache as described in [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>
7.  <span data-ttu-id="9984f-138">Überprüfen Sie die Schema Erweiterung mithilfe LDP.exe.</span><span class="sxs-lookup"><span data-stu-id="9984f-138">Verify the schema extension using LDP.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9984f-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9984f-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9984f-140">Abrufen eines Objekt Bezeichners</span><span class="sxs-lookup"><span data-stu-id="9984f-140">Obtaining an Object Identifier</span></span>](obtaining-an-object-identifier.md)
</dt> <dt>

[<span data-ttu-id="9984f-141">Die neuen Befehlszeilen Tools für Active Directory in Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9984f-141">The new command-line tools for Active Directory in Windows Server 2003</span></span>](https://support.microsoft.com/kb/298882)
</dt> <dt>

<span data-ttu-id="9984f-142">[Verwenden des LDIF-Tools](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))</span><span class="sxs-lookup"><span data-stu-id="9984f-142">[Using the LDIFDE Tool](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))</span></span>
</dt> <dt>

<span data-ttu-id="9984f-143">[Erweitern des Active Directory-Schemas](/previous-versions/ms806972(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="9984f-143">[Extending the Active Directory Schema](/previous-versions/ms806972(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="9984f-144">Einschränkungen bei der Schema Erweiterung</span><span class="sxs-lookup"><span data-stu-id="9984f-144">Restrictions on Schema Extension</span></span>](restrictions-on-schema-extension.md)
</dt> </dl>

 

 