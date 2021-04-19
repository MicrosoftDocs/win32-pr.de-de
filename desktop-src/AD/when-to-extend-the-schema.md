---
title: Wann soll das Schema erweitert werden?
description: Erweitern Sie das Schema nur dann, wenn keine vorhandene Objektklasse die Anforderungen Ihrer Anwendung erfüllt. Das Erweitern des Schemas ist ein komplexer Vorgang. Schema Änderungen werden auf allen Domänen Controllern in der Gesamtstruktur des Unternehmens repliziert. Berücksichtigen Sie dies sorgfältig.
ms.assetid: 92231f31-d2af-4c3b-981e-e55cc478899d
ms.tgt_platform: multiple
keywords:
- Wann soll das Schema AD erweitert werden?
- Schema-AD, wann es erweitert werden soll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c182b346fd1e31bc549325260d9b57d75bbb63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338157"
---
# <a name="when-to-extend-the-schema"></a><span data-ttu-id="53aa4-107">Wann soll das Schema erweitert werden?</span><span class="sxs-lookup"><span data-stu-id="53aa4-107">When to Extend the Schema</span></span>

<span data-ttu-id="53aa4-108">Erweitern Sie das Schema nur dann, wenn keine vorhandene Objektklasse die Anforderungen Ihrer Anwendung erfüllt.</span><span class="sxs-lookup"><span data-stu-id="53aa4-108">Extend the schema only if no existing object class fulfills the requirements of your application.</span></span> <span data-ttu-id="53aa4-109">Das Erweitern des Schemas ist ein komplexer Vorgang. Schema Änderungen werden auf allen Domänen Controllern in der Gesamtstruktur des Unternehmens repliziert.</span><span class="sxs-lookup"><span data-stu-id="53aa4-109">Extending the schema is a complex operation; schema changes are replicated to every domain controller in the enterprise forest.</span></span> <span data-ttu-id="53aa4-110">Berücksichtigen Sie dies sorgfältig.</span><span class="sxs-lookup"><span data-stu-id="53aa4-110">Consider this carefully.</span></span>

<span data-ttu-id="53aa4-111">Das Schema kann auf drei Arten erweitert werden:</span><span class="sxs-lookup"><span data-stu-id="53aa4-111">The schema can be extended in three ways:</span></span>

-   <span data-ttu-id="53aa4-112">Leiten Sie eine neue Unterklasse von einer vorhandenen Klasse ab: die Unterklasse verfügt über alle Attribute der übergeordneten Klasse und alle Attribute, die Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="53aa4-112">Derive a new subclass from an existing class - the subclass has all of the attributes of the superclass and any attributes you specify.</span></span> <span data-ttu-id="53aa4-113">Von einer vorhandenen Klasse ableiten:</span><span class="sxs-lookup"><span data-stu-id="53aa4-113">Derive from an existing class:</span></span>
    -   <span data-ttu-id="53aa4-114">Wenn die vorhandene Klasse zusätzliche Attribute erfordert, aber andernfalls akzeptabel ist.</span><span class="sxs-lookup"><span data-stu-id="53aa4-114">When the existing class requires additional attributes, but otherwise is acceptable.</span></span>
    -   <span data-ttu-id="53aa4-115">Wenn die Möglichkeit zum Transformieren vorhandener Objekte der Klasse in eine neue Klasse nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="53aa4-115">When the ability to transform existing objects of the class into a new class is not required.</span></span> <span data-ttu-id="53aa4-116">Es ist nicht möglich, einem vorhandenen Objekt eine Unterklasse hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="53aa4-116">It is not possible to add a subclass to an existing object.</span></span>
    -   <span data-ttu-id="53aa4-117">Verwenden Sie das vorhandene Verzeichnis-Manager-Snap-in, um die erweiterten Attribute der Objekte zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="53aa4-117">To use the existing Directory Manager snap-in to manage the extended attributes of the objects.</span></span>
-   <span data-ttu-id="53aa4-118">Hinzufügen von Attributen zu einer vorhandenen Klasse und/oder Hinzufügen von übergeordneten Objekten für die Klasse.</span><span class="sxs-lookup"><span data-stu-id="53aa4-118">Add attributes to an existing class and/or add parent objects for the class.</span></span> <span data-ttu-id="53aa4-119">Wenn Sie mehrere Attribute hinzufügen, führen Sie diesen Vorgang strukturiert aus, indem Sie eine zusätzliche Klasse definieren und diese Hilfsklasse der vorhandenen Klasse hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="53aa4-119">When adding multiple attributes, perform this operation in a structured manner by defining an auxiliary class and adding that auxiliary class to the existing class.</span></span>
-   <span data-ttu-id="53aa4-120">Änderungen an einer vorhandenen Klasse sind erforderlich, wenn eine Anwendung die Möglichkeit benötigt, vorhandene Objekte der Klasse zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="53aa4-120">Modification of an existing class is required when an application requires the ability to extend existing objects of the class.</span></span> <span data-ttu-id="53aa4-121">Wenn Sie z. b. dem Benutzerobjekt anwendungsspezifische Daten hinzufügen möchten, erweitern Sie die Klasse Benutzer normal, da Sie vorhandene Benutzer und nicht nur die von der Anwendung erstellten speziellen Benutzer verarbeiten müssen.</span><span class="sxs-lookup"><span data-stu-id="53aa4-121">For example, to add application-specific data to the User object, extend the class User normally, because you must handle existing Users and not just special Users created by your application.</span></span>
-   <span data-ttu-id="53aa4-122">Erstellen Sie eine neue Klasse mit den erforderlichen Attributen.</span><span class="sxs-lookup"><span data-stu-id="53aa4-122">Create a new class with the required attributes.</span></span> <span data-ttu-id="53aa4-123">Erstellen Sie eine neue Klasse. Das heißt, eine Klasse, die von "Top" abgeleitet wird, wenn keine vorhandene Klasse die betrieblichen Anforderungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="53aa4-123">Create a new class; that is, a class derived from "Top" when no existing class fulfills the operational requirements.</span></span>

<span data-ttu-id="53aa4-124">Wenn Sie eine Unterklasse einer vorhandenen Klasse unterteilen, werden alle der ursprünglichen Klasse zugeordneten Benutzeroberflächen Elemente nicht von der Unterklasse geerbt.</span><span class="sxs-lookup"><span data-stu-id="53aa4-124">When you subclass an existing class, any user interface items associated to the original class will not be inherited by the subclass.</span></span> <span data-ttu-id="53aa4-125">Wenn Sie z. b. ein Benutzerobjekt Unterklassen, werden die dem Benutzer zugeordneten Eigenschaften Seiten und Menü Elemente nicht geerbt.</span><span class="sxs-lookup"><span data-stu-id="53aa4-125">For example, if you subclass a user object, the property pages and menu items associated to user are not inherited.</span></span> <span data-ttu-id="53aa4-126">Aus diesem Grund ist es vorzuziehen, ein vorhandenes Objekt zu erweitern oder eine Hilfsklasse zu erstellen, anstatt eine Unterklasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="53aa4-126">For this reason, it is preferable to extend an existing object or create an auxiliary class rather than create a subclass.</span></span>

<span data-ttu-id="53aa4-127">Unabhängig davon, ob Sie eine Unterklasse einer vorhandenen Klasse oder eine vorhandene Klasse ändern, sollten Sie Tools wie das Snap-in "Active Directory-Benutzer und-Computer" erweitern, um die erweiterten Attribute der Objekte zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="53aa4-127">Whether you subclass an existing class or modify an existing class, you will want to extend tools such as the Active Directory Users and Computers snap-in to manage the extended attributes of the objects.</span></span> <span data-ttu-id="53aa4-128">Weitere Informationen finden Sie unter [Erweitern der Benutzeroberfläche für Verzeichnisobjekte](extending-the-user-interface-for-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="53aa4-128">For more information, see [Extending the User Interface for Directory Objects](extending-the-user-interface-for-directory-objects.md).</span></span>

 

 




