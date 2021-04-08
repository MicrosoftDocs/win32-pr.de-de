---
title: Informationen zum Active Directory Schema
description: Jedes Objekt in Active Directory Domain Services ist eine Instanz einer Objektklasse, die im Active Directory Schema definiert ist.
ms.assetid: 8fc9cd2d-8fed-4fda-918c-79b01f9a19bb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f55513b359a7ef293b005d93a20ac43f470d515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855207"
---
# <a name="about-the-active-directory-schema"></a><span data-ttu-id="f0818-103">Informationen zum Active Directory Schema</span><span class="sxs-lookup"><span data-stu-id="f0818-103">About the Active Directory Schema</span></span>

<span data-ttu-id="f0818-104">Jedes Objekt in Active Directory Domain Services ist eine Instanz einer Objektklasse, die im Active Directory Schema definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f0818-104">Every object in Active Directory Domain Services is an instance of an object class defined in the Active Directory schema.</span></span> <span data-ttu-id="f0818-105">Eine Objektklasse stellt eine Kategorie von Objekten dar, wie z. B. Benutzer, Drucker oder Anwendungsprogramme, die gemeinsame Merkmale aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f0818-105">An object class represents a category of objects, such as users, printers, or application programs, that share a set of common characteristics.</span></span> <span data-ttu-id="f0818-106">Die Definition für jede Objektklasse enthält eine Liste der Attribute, mit denen Instanzen der Klasse beschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="f0818-106">The definition for each object class contains a list of the attributes that can be used to describe instances of the class.</span></span> <span data-ttu-id="f0818-107">Beispielsweise weist die Klasse Benutzer Attribute wie **givenName**, **surname** und **streetAddress** auf.</span><span class="sxs-lookup"><span data-stu-id="f0818-107">For example, the User class has attributes such as **givenName**, **surname**, and **streetAddress**.</span></span> <span data-ttu-id="f0818-108">Die Liste der Attribute für eine Klasse wird in diejenigen unterteilt, die ein Objekt dieser Klasse enthalten muss, sowie zusätzliche Attribute, die ein Objekt enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="f0818-108">The list of attributes for a class is divided into those that an object of that class must contain, and additional attributes that an object may contain.</span></span> <span data-ttu-id="f0818-109">Das Verzeichnis ist in einer Hierarchie angeordnet. die Definition jeder Klasse listet auch die Klassen auf, deren Objekte übergeordnete Elemente von Objekten einer bestimmten Klasse sein können – dies steuert die Form der Verzeichnishierarchie.</span><span class="sxs-lookup"><span data-stu-id="f0818-109">The directory is arranged in a hierarchy; the definition of each class also lists the classes whose objects can be parents of objects of a given class—this controls the shape of the directory hierarchy.</span></span>

<span data-ttu-id="f0818-110">Das Schema definiert auch formal jedes Attribut.</span><span class="sxs-lookup"><span data-stu-id="f0818-110">The schema also formally defines each attribute.</span></span> <span data-ttu-id="f0818-111">Die Definition für jedes Attribut umfasst eindeutige Bezeichner für das Attribut, die Syntax für das Attribut (d. h. den Datentyp für die Werte des Attributs), optionale Bereichs Begrenzungen für die Attributwerte, ob das Attribut nur einen Wert oder mehrere Werte aufweisen kann und ob das Attribut indiziert ist.</span><span class="sxs-lookup"><span data-stu-id="f0818-111">The definition for each attribute includes unique identifiers for the attribute, the syntax for the attribute (that is, the data type for the attribute's values), optional range limits for the attribute values, whether the attribute can have only one value or multiple values, and whether the attribute is indexed.</span></span> <span data-ttu-id="f0818-112">Das Verzeichnisschema definiert jedes Attribut genau einmal, – Objektklassen Definitionen enthalten Verweise auf die Attribute, die im Schema definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f0818-112">The directory schema defines each attribute exactly once—object class definitions contain references to the attributes defined in the schema.</span></span> <span data-ttu-id="f0818-113">Das Attribut "Description" wird beispielsweise nur einmal definiert, und es wird von vielen Objektklassen darauf verwiesen.</span><span class="sxs-lookup"><span data-stu-id="f0818-113">For example, the "description" attribute is defined only once and is referenced by many object classes.</span></span> <span data-ttu-id="f0818-114">Dies unterscheidet sich von einem relationalen Datenbankschema, bei dem die "Attribute" (Spalten) für jede Tabelle separat definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f0818-114">This is different than a relational database schema, where the "attributes" (columns) are separately defined for each table.</span></span>

 

 




