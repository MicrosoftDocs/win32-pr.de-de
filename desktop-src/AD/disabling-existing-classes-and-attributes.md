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
# <a name="disabling-existing-classes-and-attributes"></a><span data-ttu-id="59978-103">Deaktivieren vorhandener Klassen und Attribute</span><span class="sxs-lookup"><span data-stu-id="59978-103">Disabling Existing Classes and Attributes</span></span>

<span data-ttu-id="59978-104">Schema Ergänzungen sind permanent.</span><span class="sxs-lookup"><span data-stu-id="59978-104">Schema additions are permanent.</span></span> <span data-ttu-id="59978-105">**AttributeSchema** -und **classSchema** -Objekte können nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="59978-105">You cannot delete **attributeSchema** and **classSchema** objects.</span></span> <span data-ttu-id="59978-106">In einem verteilten System ist es schwierig sicherzustellen, dass keine Instanzen einer bestimmten Klasse oder eines Attributs vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="59978-106">In a distributed system, it is difficult to guarantee that there are no instances of a given class or attribute.</span></span> <span data-ttu-id="59978-107">Wenn Sie die Definition einer Klasse oder eines Attributs entfernen, werden vorhandene Instanzen dieser Klasse oder dieses Attributs beschädigt.</span><span class="sxs-lookup"><span data-stu-id="59978-107">Removing the definition of a class or attribute damages existing instances of that class or attribute.</span></span>

<span data-ttu-id="59978-108">Sie können eine vorhandene Klasse oder ein vorhandenes Attribut deaktivieren, indem Sie es als "veraltet" markieren.</span><span class="sxs-lookup"><span data-stu-id="59978-108">You can disable an existing class or attribute by marking it as "defunct".</span></span> <span data-ttu-id="59978-109">Dies wirkt sich nicht auf vorhandene Instanzen der Klasse oder des Attributs aus, die so gekennzeichnet sind, verhindert jedoch die Erstellung neuer Instanzen.</span><span class="sxs-lookup"><span data-stu-id="59978-109">This does not affect existing instances of the class or attribute so marked, but it prevents the creation of new instances.</span></span>

<span data-ttu-id="59978-110">Beim Deaktivieren von Schema Klassen und Attributen gelten die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="59978-110">The following restrictions apply when disabling schema classes and attributes:</span></span>

-   <span data-ttu-id="59978-111">Eine Klasse oder ein Attribut der Kategorie 1 kann nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="59978-111">You cannot disable a Category 1 class or attribute.</span></span>
-   <span data-ttu-id="59978-112">Ein Attribut, das ein Member einer Klasse ist, die nicht gleichzeitig deaktiviert ist, kann nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="59978-112">You cannot disable an attribute that is a member of a class that is not also disabled.</span></span> <span data-ttu-id="59978-113">Dies liegt daran, dass ein Attribut möglicherweise für die (nicht deaktivierte) Klasse erforderlich ist, und durch das Deaktivieren des-Attributs wird verhindert, dass neue Instanzen der-Klasse erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="59978-113">This is because an attribute might be required for the (not disabled) class, and disabling the attribute prevents new instances of the class from being created.</span></span>

<span data-ttu-id="59978-114">Um ein Attribut zu deaktivieren, legen Sie das **isDefunct** -Attribut seines **attributeSchema** -Objekts auf " **true**" fest.</span><span class="sxs-lookup"><span data-stu-id="59978-114">To disable an attribute, set the **isDefunct** attribute of its **attributeSchema** object to **TRUE**.</span></span> <span data-ttu-id="59978-115">Wenn ein Attribut deaktiviert ist, können keine neuen Instanzen des Attributs erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="59978-115">When an attribute is disabled, new instances of the attribute cannot be created.</span></span> <span data-ttu-id="59978-116">Um das Attribut erneut zu aktivieren, legen Sie das **IsDebug** -Attribut auf " **false**" fest.</span><span class="sxs-lookup"><span data-stu-id="59978-116">To re-enable the attribute set the **isDefunct** attribute to **FALSE**.</span></span>

<span data-ttu-id="59978-117">Um eine Klasse zu deaktivieren, legen Sie das **isDefunct** -Attribut seines **classSchema** -Objekts auf " **true**" fest.</span><span class="sxs-lookup"><span data-stu-id="59978-117">To disable a class, set the **isDefunct** attribute of its **classSchema** object to **TRUE**.</span></span> <span data-ttu-id="59978-118">Wenn eine Klasse deaktiviert ist, können keine neuen Instanzen der Klasse erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="59978-118">When a class is disabled, new instances of the class cannot be created.</span></span> <span data-ttu-id="59978-119">Zum erneuten Aktivieren der-Klasse legen Sie das **isDefunct** -Attribut auf " **false**" fest.</span><span class="sxs-lookup"><span data-stu-id="59978-119">To re-enable the class set the **isDefunct** attribute to **FALSE**.</span></span>

<span data-ttu-id="59978-120">Das Festlegen von Schema Objekten als veraltet kann in Produktionsumgebungen nützlich sein.</span><span class="sxs-lookup"><span data-stu-id="59978-120">Setting schema objects as defunct can be useful in production environments.</span></span> <span data-ttu-id="59978-121">Wenn eine Testversion einer Schema Erweiterung nicht mehr benötigt wird, markieren Sie Sie als veraltet.</span><span class="sxs-lookup"><span data-stu-id="59978-121">When a test version of a schema extension is no longer required, mark it as defunct.</span></span> <span data-ttu-id="59978-122">Sie können es wiederherstellen, indem Sie das Attribut **IsOut** entfernen oder den Attribut Wert auf **false** festlegen.</span><span class="sxs-lookup"><span data-stu-id="59978-122">You can restore it by removing the **isDefunct** attribute or setting the attribute value to **FALSE**.</span></span> <span data-ttu-id="59978-123">Dies schützt auch vor einem unbeabsichtigten Entfernen eines Schema Objekts, indem es auf "veraltet" festgelegt wird, da der Vorgang problemlos rückgängig gemacht werden kann.</span><span class="sxs-lookup"><span data-stu-id="59978-123">This also protects against an unintended removal of a schema object by setting it to defunct because the operation can be easily reversed.</span></span>

<span data-ttu-id="59978-124">Beachten Sie, dass der Active Directory Server vorhandene Instanzen eines Attributs oder einer Klasse nicht bereinigt, wenn Sie ein Schema Objekt defunct machen.</span><span class="sxs-lookup"><span data-stu-id="59978-124">Be aware that the Active Directory server does not clean up existing instances of an attribute or class when you make a schema object defunct.</span></span> <span data-ttu-id="59978-125">Wenn Sie die **IsDebug** -Eigenschaft entfernen, werden alle Instanzen zu gültigen, normalen Objekten.</span><span class="sxs-lookup"><span data-stu-id="59978-125">If you remove the **isDefunct** property, any instances become valid, normal objects again.</span></span>

<span data-ttu-id="59978-126">Die folgende Liste enthält weitere Konsequenzen, die das Markieren eines **attributeSchema** -oder **classSchema** -Objekts außer Kraft setzen:</span><span class="sxs-lookup"><span data-stu-id="59978-126">The following list includes other consequences of marking an **attributeSchema** or **classSchema** object defunct:</span></span>

-   <span data-ttu-id="59978-127">Das Hinzufügen oder Ändern einer Instanz schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="59978-127">Addition or modification of an instance fails.</span></span>
-   <span data-ttu-id="59978-128">Fehlercodes Verhalten sich so, als ob eine veraltete Klasse nie vorhanden wäre.</span><span class="sxs-lookup"><span data-stu-id="59978-128">Error codes behave as if a defunct class never existed.</span></span>
-   <span data-ttu-id="59978-129">Suchen und löschen Verhalten sich so, als ob keine Schema Objekte außer Kraft gesetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="59978-129">Search and delete behave as if no schema objects have been made defunct.</span></span>
-   <span data-ttu-id="59978-130">Nur das Löschen des gesamten Attributs aus dem Objekt zulassen.</span><span class="sxs-lookup"><span data-stu-id="59978-130">Only allow deleting entire attribute from object.</span></span>

<span data-ttu-id="59978-131">In der folgenden Liste sind zusätzliche Optionen in einer Produktionsumgebung enthalten, um die Auswirkungen von veralteten Schema Erweiterungen zu verringern:</span><span class="sxs-lookup"><span data-stu-id="59978-131">The following list includes additional options in a production environment for reducing the impact of defunct schema extensions:</span></span>

-   <span data-ttu-id="59978-132">Entfernen Sie alle " **mayhave** "-Attributwerte aus einer veralteten Klasse.</span><span class="sxs-lookup"><span data-stu-id="59978-132">Remove all **mayHave** attribute values from a defunct class.</span></span>
-   <span data-ttu-id="59978-133">Reduzieren Sie die Größe aller **musthave** -Attributwerte von einer veralteten Klasse.</span><span class="sxs-lookup"><span data-stu-id="59978-133">Reduce the size of all **mustHave** attribute values from a defunct class.</span></span>
-   <span data-ttu-id="59978-134">Entfernen eines veralteten Attributs aus dem globalen Katalog.</span><span class="sxs-lookup"><span data-stu-id="59978-134">Remove a defunct attribute from the global catalog.</span></span>
-   <span data-ttu-id="59978-135">Entfernen eines veralteten Attributs aus einem beliebigen Index.</span><span class="sxs-lookup"><span data-stu-id="59978-135">Remove a defunct attribute from any index.</span></span>

<span data-ttu-id="59978-136">Weitere Optionen zum Entfernen unerwünschter Schema Änderungen in einer Produktionsumgebung sind für Entwickler die Verwendung eines privaten Domänen Controllers zum Testen.</span><span class="sxs-lookup"><span data-stu-id="59978-136">Other options for removing unwanted schema changes in a production environment are for developers to use a private domain controller for testing.</span></span> <span data-ttu-id="59978-137">In diesem Fall können Sie folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="59978-137">In this case, you can:</span></span>

-   <span data-ttu-id="59978-138">Setzen Sie den Active Directory Server mit Dcpromo.exe, um den DC herabzusetzen.</span><span class="sxs-lookup"><span data-stu-id="59978-138">"Reset" the Active Directory server by using Dcpromo.exe to demote the DC.</span></span> <span data-ttu-id="59978-139">Nachdem die Herabstufung abgeschlossen ist, verwenden Sie Dcpromo.exe erneut, um den Server wieder zu einem Domänen Controller heraufzustufen.</span><span class="sxs-lookup"><span data-stu-id="59978-139">After the demote completes, use Dcpromo.exe again to promote the server back to a DC.</span></span> <span data-ttu-id="59978-140">Der Entwickler kann dann LDIF-Skripts verwenden, um alle erforderlichen Klassen, Attribute und Objektinstanzen neu zu laden.</span><span class="sxs-lookup"><span data-stu-id="59978-140">The developer can then use LDIF scripts to reload any required classes, attributes, and object instances.</span></span>
-   <span data-ttu-id="59978-141">Verwenden Sie Ntbackup.exe, um eine Systemstatus Sicherung auf eine verfügbare Datenträger Partition auszuführen.</span><span class="sxs-lookup"><span data-stu-id="59978-141">Use Ntbackup.exe to perform a system-state backup to an available disk partition.</span></span> <span data-ttu-id="59978-142">Starten Sie den Wiederherstellungs Modus für den sicheren/Verzeichnisdienst wieder her.</span><span class="sxs-lookup"><span data-stu-id="59978-142">Reboot to Safe/Directory Service Restore mode to restore.</span></span>

<span data-ttu-id="59978-143">Wenn Sie für Windows Server 2003-Betriebssysteme eine Klasse oder ein Attribut auf "veraltet" festlegen, können Sie die Werte für " **ldapDisplayName**", " **schemaIdGUID**", " **OID** " und " **mapiId** " des veralteten Schema Elements sofort wieder verwenden, wenn Sie eine neue Klasse oder ein neues Attribut erstellen, um es zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="59978-143">For Windows Server 2003 operating systems, when you set a class or attribute to defunct, you can immediately reuse the **ldapDisplayName**, **schemaIdGuid**, **OID** and **mapiID** values of the defunct schema element when you create a new class or attribute to replace it.</span></span> <span data-ttu-id="59978-144">Die veraltete Version der Klasse oder des Attributs wird im Schema Container verwaltet, aber im MMC-Snap-in ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="59978-144">The defunct version of the class or attribute is maintained in the Schema container, but it is hidden in the MMC snap-in.</span></span> <span data-ttu-id="59978-145">Wenn Sie das alte Schema Element reaktivieren möchten, legen Sie **IsDebug** auf **false** fest.</span><span class="sxs-lookup"><span data-stu-id="59978-145">To reactivate the old schema element, set **isDefunct** to **FALSE**.</span></span>

<span data-ttu-id="59978-146">Im folgenden LDIF-Codebeispiel wird veranschaulicht, wie das **isDefunct** -Attribut geändert und der RDN so geändert wird, dass es nicht mit der neuen Klasse verwechselt wird, die Sie zum Ersetzen von erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="59978-146">The following LDIF code example shows how to modify the **isDefunct** attribute and change the RDN so that it is not confused with the new class that you create to replace it.</span></span>

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

<span data-ttu-id="59978-147">Verwenden Sie den folgenden Befehl, um das LDIF-Codebeispiel für eine Gesamtstruktur eines Computers auszuführen, auf dem Windows Server 2003-Betriebssysteme ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="59978-147">Use the following command to run the LDIF code example against a forest for a computer running on Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="59978-148">**LDIF/i/f RDN. ldf/c "DC = X" "DC = MyDomain, DC = com"**</span><span class="sxs-lookup"><span data-stu-id="59978-148">**ldifde /i /f rdn.ldf /c "DC=X" "dc=mydomain,dc=com"**</span></span>

<span data-ttu-id="59978-149">(Wobei "DC = X" eine Konstante ist)</span><span class="sxs-lookup"><span data-stu-id="59978-149">(Where "DC=X" is a constant)</span></span>

 

 




