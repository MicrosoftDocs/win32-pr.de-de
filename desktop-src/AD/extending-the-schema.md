---
title: Erweitern des Schemas
description: Das Schema für den Active Directory Directory-Dienst definiert die Attribute und Klassen, die in Active Directory Domain Services verwendet werden.
ms.assetid: 1c7c1fa7-56d9-4b2d-9c48-aa10464064bc
ms.tgt_platform: multiple
keywords:
- Active Directory mit, Schema, Erweitern des Schemas
- Schema AD, Erweitern des Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c03d57468fb5275c55ce0d725a2decd7cfbf0f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106337419"
---
# <a name="extending-the-schema"></a><span data-ttu-id="d7b12-105">Erweitern des Schemas</span><span class="sxs-lookup"><span data-stu-id="d7b12-105">Extending the Schema</span></span>

<span data-ttu-id="d7b12-106">Das Schema für den Active Directory Directory-Dienst definiert die Attribute und Klassen, die in Active Directory Domain Services verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7b12-106">The Active Directory directory service schema defines the attributes and classes used in Active Directory Domain Services.</span></span> <span data-ttu-id="d7b12-107">Das Basis Schema, das im System enthalten ist, enthält einen umfangreichen Satz von Klassendefinitionen, wie z. b. **User**, **Computer** und **OrganizationalUnit**, und Attribut Definitionen, wie z. b. **userPrincipalName**, **telefonienumber** und **objectSID**.</span><span class="sxs-lookup"><span data-stu-id="d7b12-107">The base schema that is included the system contains a rich set of class definitions, such as **user**, **computer**, and **organizationalUnit**, and attribute definitions, such as **userPrincipalName**, **telephoneNumber**, and **objectSid**.</span></span> <span data-ttu-id="d7b12-108">Die vorhandenen Klassen und Attribute sind für die meisten Anwendungen ausreichend.</span><span class="sxs-lookup"><span data-stu-id="d7b12-108">The existing set of classes and attributes will be sufficient for most applications.</span></span> <span data-ttu-id="d7b12-109">Das Schema ist jedoch erweiterbar, was bedeutet, dass Sie neue Klassen und Attribute definieren können.</span><span class="sxs-lookup"><span data-stu-id="d7b12-109">However, the schema is extensible, which means that you can define new classes and attributes.</span></span> <span data-ttu-id="d7b12-110">In diesem Abschnitt wird erläutert, wie das Active Directory Schema erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="d7b12-110">This section discusses how to extend the Active Directory schema.</span></span>

## <a name="when-to-extend-the-schema"></a><span data-ttu-id="d7b12-111">Wann soll das Schema erweitert werden?</span><span class="sxs-lookup"><span data-stu-id="d7b12-111">When to Extend the Schema</span></span>

<span data-ttu-id="d7b12-112">Wenn die vorhandenen Klassen und Attribute nicht in den Datentyp passen, den Sie speichern möchten, sollten Sie das Schema erweitern.</span><span class="sxs-lookup"><span data-stu-id="d7b12-112">If the existing classes and attributes do not fit with the type of data you want to store, you should extend the schema.</span></span> <span data-ttu-id="d7b12-113">Es ist wichtig zu beachten, dass Schema Ergänzungen permanent sind. Sie können Klassen und Attribute deaktivieren, Sie können Sie jedoch nie aus dem Schema entfernen.</span><span class="sxs-lookup"><span data-stu-id="d7b12-113">It is important to note that schema additions are permanent; you can disable classes and attributes, but you can never remove them from the schema.</span></span> <span data-ttu-id="d7b12-114">Beachten Sie dies, wenn Sie Code testen.</span><span class="sxs-lookup"><span data-stu-id="d7b12-114">Keep this in mind when you are testing code.</span></span>

<span data-ttu-id="d7b12-115">Beachten Sie auch die Größe der Daten, die Sie speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="d7b12-115">Also consider the size of the data that you want to store.</span></span> <span data-ttu-id="d7b12-116">Microsoft empfiehlt, dass kein Attribut Wert 500 Kilobyte, einschließlich der Summe der mehrwertigen Attribute, überschreitet.</span><span class="sxs-lookup"><span data-stu-id="d7b12-116">Microsoft recommends that no attribute value exceed 500 kilobytes, including the sum of multivalued attributes.</span></span> <span data-ttu-id="d7b12-117">Außerdem sollte die Größe von Objekten 1 Megabyte nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="d7b12-117">Also, objects should not exceed 1 megabyte in size.</span></span> <span data-ttu-id="d7b12-118">Beachten Sie auch die Anzahl der Instanzen der Daten. Wenn Sie der [**User**](/windows/desktop/ADSchema/c-user) -Klasse auf einem System mit 100.000 Benutzern ein neues Attribut hinzufügen, kann dies einen beträchtlichen Speicherplatz beanspruchen.</span><span class="sxs-lookup"><span data-stu-id="d7b12-118">Consider also the number of instances of the data; if you add a new attribute to the [**User**](/windows/desktop/ADSchema/c-user) class on a system that has 100,000 users, this can use up considerable space.</span></span>

<span data-ttu-id="d7b12-119">Die Themen in diesem Abschnitt umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d7b12-119">Topics in this section include:</span></span>

-   <span data-ttu-id="d7b12-120">Binden an den Schema Container und Lesen der Eigenschaften vorhandener Klassen und Attribute.</span><span class="sxs-lookup"><span data-stu-id="d7b12-120">How to bind to the schema container and read the properties of existing classes and attributes.</span></span>
-   <span data-ttu-id="d7b12-121">Gibt an, wie und wann das Schema durch Definieren neuer Attribute und Klassen erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7b12-121">How and when to extend the schema by defining new attributes and classes.</span></span>
-   <span data-ttu-id="d7b12-122">Installieren von Schema Erweiterungen mithilfe von LDIFDE, CSVDE oder Programm gesteuert mit ADSI.</span><span class="sxs-lookup"><span data-stu-id="d7b12-122">How to install schema extensions using LDIFDE, CSVDE, or programmatically with ADSI.</span></span>

<span data-ttu-id="d7b12-123">Weitere Informationen und eine Übersicht über das Active Directory Schema, einschließlich Informationen über die Schema Implementierung, Klassendefinitionen und Attribut Definitionen, finden Sie unter [Active Directory Schema](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="d7b12-123">For more information and an overview of the Active Directory schema, including information about the schema implementation, class definitions, and attribute definitions, see [Active Directory Schema](active-directory-schema.md).</span></span>

<span data-ttu-id="d7b12-124">Weitere Informationen, einschließlich Referenzseiten für die vordefinierten Schema Klassen, Attribute und Attributsyntaxen, finden Sie in der Active Directory-Schema Referenz in der [Active Directory Domain Services Referenz](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d7b12-124">For more information, including reference pages for the predefined schema classes, attributes, and attribute syntaxes, see the Active Directory Schema Reference in the [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

 

 