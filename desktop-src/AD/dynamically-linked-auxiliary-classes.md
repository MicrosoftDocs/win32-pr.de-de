---
title: Dynamisch verknüpfte Hilfsklassen
description: Eine dynamisch verknüpfte Hilfsklasse ist eine Klasse, die an ein einzelnes Objekt angefügt ist, und nicht an eine Objektklasse.
ms.assetid: 10530a3c-89fc-4ff0-a0b7-1c9a27659003
ms.tgt_platform: multiple
keywords:
- Dynamisch verknüpfte Hilfsklassen AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0cacb09d3aef05bcaf0ef729411c2e023469be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206275"
---
# <a name="dynamically-linked-auxiliary-classes"></a><span data-ttu-id="5f5c8-104">Dynamisch verknüpfte Hilfsklassen</span><span class="sxs-lookup"><span data-stu-id="5f5c8-104">Dynamically Linked Auxiliary Classes</span></span>

<span data-ttu-id="5f5c8-105">Eine dynamisch verknüpfte Hilfsklasse ist eine Klasse, die an ein einzelnes Objekt angefügt ist, und nicht an eine Objektklasse.</span><span class="sxs-lookup"><span data-stu-id="5f5c8-105">A dynamically linked auxiliary class is a class that is attached to an individual object, rather than to an object class.</span></span> <span data-ttu-id="5f5c8-106">Mithilfe dynamischer Verknüpfungen können Sie zusätzliche Attribute mit einem einzelnen Objekt speichern, ohne die Gesamtstruktur weite Auswirkung der Erweiterung der Schema Definition für eine ganze Klasse zu haben.</span><span class="sxs-lookup"><span data-stu-id="5f5c8-106">Dynamic linking enables you to store additional attributes with an individual object without the forest-wide impact of extending the schema definition for an entire class.</span></span> <span data-ttu-id="5f5c8-107">Beispielsweise könnte ein Unternehmen mithilfe dynamischer Verknüpfungen eine Verkaufs spezifische Hilfsklasse an die Benutzer Objekte seiner Vertriebsmitarbeiter und andere abteilungsspezifische Hilfssysteme an die Benutzer Objekte der Mitarbeiter in anderen Abteilungen anfügen.</span><span class="sxs-lookup"><span data-stu-id="5f5c8-107">For example, an enterprise could use dynamic linking to attach a sales-specific auxiliary class to the user objects of its sales people, and other department-specific auxiliary classes to the user objects of employees in other departments.</span></span>

<span data-ttu-id="5f5c8-108">Dynamisches Verknüpfen ist nicht komplex: Fügen Sie den Werten eines **objectClass** -Attributs für ein Objekt den Namen der Hilfsklasse hinzu.</span><span class="sxs-lookup"><span data-stu-id="5f5c8-108">Dynamic linking is not complex: add the name of the auxiliary class to the values of an object's **objectClass** attribute.</span></span> <span data-ttu-id="5f5c8-109">Wenn die Erweiterungs Klasse über obligatorische Attribute (**musthave** oder **systemmusthave**) verfügt, müssen Sie Sie gleichzeitig festlegen.</span><span class="sxs-lookup"><span data-stu-id="5f5c8-109">If the auxiliary class has any mandatory attributes (**mustHave** or **systemMustHave**), you must set them at the same time.</span></span> <span data-ttu-id="5f5c8-110">Weitere Informationen und ein Codebeispiel finden Sie unter [Hinzufügen einer zusätzlichen Klasse zu einer Objektinstanz](adding-an-auxiliary-class-to-an-object-instance.md).</span><span class="sxs-lookup"><span data-stu-id="5f5c8-110">For more information and a code example, see [Adding an Auxiliary Class to an Object Instance](adding-an-auxiliary-class-to-an-object-instance.md).</span></span>

<span data-ttu-id="5f5c8-111">Um eine dynamisch verknüpfte Hilfsklasse zu entfernen, löschen Sie die Werte aller Attribute aus der Erweiterungs Klasse, und entfernen Sie dann den Namen der Hilfsklasse aus dem **objectClass** -Attribut des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5f5c8-111">To remove a dynamically linked auxiliary class, clear the values of all attributes from the auxiliary class, and then remove the name of the auxiliary class from the **objectClass** attribute of the object.</span></span>

<span data-ttu-id="5f5c8-112">Wenn Sie eine zusätzliche Klasse dynamisch hinzufügen, die eine Unterklasse einer anderen Hilfsklasse ist, werden dem Zielobjekt beide Erweiterungs Klassen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5f5c8-112">If you dynamically add an auxiliary class that is a subclass of another auxiliary class, both auxiliary classes are added to the target object.</span></span> <span data-ttu-id="5f5c8-113">Das Entfernen der untergeordneten Erweiterungs Klasse entfernt jedoch nicht das übergeordnete Element. jede Klasse muss explizit entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="5f5c8-113">However, removing the child auxiliary class does not remove its parent; each class must be explicitly removed.</span></span>

 

 




