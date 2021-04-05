---
title: Statisch verknüpfte Hilfsklassen
description: Eine statisch verknüpfte Hilfsklasse ist eine, die im-Schema im auxiliaryClass-oder systemAuxiliaryClass-Attribut der classSchema-Definition einer Objektklasse enthalten ist.
ms.assetid: 24765001-7a60-4654-a23a-bf0326b59096
ms.tgt_platform: multiple
keywords:
- Statisch verknüpfte Hilfsklassen AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1ef6191834687fc2b7741f097f6bfe75b5ef31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707536"
---
# <a name="statically-linked-auxiliary-classes"></a><span data-ttu-id="3824e-104">Statisch verknüpfte Hilfsklassen</span><span class="sxs-lookup"><span data-stu-id="3824e-104">Statically Linked Auxiliary Classes</span></span>

<span data-ttu-id="3824e-105">Eine statisch verknüpfte Hilfsklasse ist eine, die im-Schema im **auxiliaryClass** -oder **systemAuxiliaryClass** -Attribut der **classSchema** -Definition einer Objektklasse enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="3824e-105">A statically linked auxiliary class is one that is included in the **auxiliaryClass** or **systemAuxiliaryClass** attribute of an object class's **classSchema** definition in the schema.</span></span> <span data-ttu-id="3824e-106">Dies bedeutet, dass die Hilfsklasse Teil jeder Instanz der Klasse ist, der Sie zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3824e-106">This means that the auxiliary class is part of every instance of the class with which it is associated.</span></span>

<span data-ttu-id="3824e-107">Eine Hilfsklasse kann statisch mit einer Objektklasse verknüpft werden, wenn die Klasse definiert ist, d. h., wenn Ihr **classSchema** -Objekt dem Schema Container hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="3824e-107">An auxiliary class can be statically linked to an object class when the class is defined, that is, when its **classSchema** object is added to the schema container.</span></span> <span data-ttu-id="3824e-108">Dies ist der einzige Zeitpunkt, an dem die **systemAuxiliaryClass** verwendet werden kann. Nachdem ein **classSchema** -Objekt erstellt wurde, kann das zugehörige **systemAuxiliaryClass** -Attribut nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3824e-108">This is the only time that the **systemAuxiliaryClass** can be used; after a **classSchema** object is created, its **systemAuxiliaryClass** attribute cannot be modified.</span></span> <span data-ttu-id="3824e-109">Eine Hilfsklasse, die zu diesem Zeitpunkt statisch verknüpft ist, kann über verbindliche (**musthave**) und/oder optionale (**mayhat**) Attribute verfügen.</span><span class="sxs-lookup"><span data-stu-id="3824e-109">An auxiliary class that is statically linked at this time can have mandatory (**mustHave**) and/or optional (**mayHave**) attributes.</span></span>

<span data-ttu-id="3824e-110">Ein privilegierter Benutzer mit den Berechtigungen, die zum Erweitern des Schemas erforderlich sind, kann Hilfsklassen aus dem Attribut " **systemAuxiliaryClass** " eines vorhandenen **classSchema** -Objekts hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="3824e-110">A privileged user with the permissions required to extend the schema can add or remove auxiliary classes from the **systemAuxiliaryClass** attribute of an existing **classSchema** object.</span></span> <span data-ttu-id="3824e-111">Dadurch wird die Hilfsklasse aus jeder vorhandenen Instanz der Objektklasse hinzugefügt oder daraus entfernt.</span><span class="sxs-lookup"><span data-stu-id="3824e-111">Doing so adds or removes the auxiliary class from every existing instance of the object class.</span></span> <span data-ttu-id="3824e-112">Eine Hilfsklasse, die zu diesem Zeitpunkt statisch verknüpft ist, kann über optionale Attribute verfügen, aber keine obligatorischen Attribute besitzen.</span><span class="sxs-lookup"><span data-stu-id="3824e-112">An auxiliary class that is statically linked at this time can have optional attributes, but cannot have mandatory attributes.</span></span> <span data-ttu-id="3824e-113">Dies liegt daran, dass es möglicherweise vorhandene Instanzen der Objektklasse gibt. in diesem Fall würden durch das Hinzufügen eines neuen obligatorischen Attributs Probleme entstehen.</span><span class="sxs-lookup"><span data-stu-id="3824e-113">This is because there may be existing instances of the object class, in which case, adding a new mandatory attribute would create problems.</span></span> <span data-ttu-id="3824e-114">Ein privilegierter Benutzer kann anschließend eine Hilfsklasse aus dem **auxiliaryClass** -Attribut eines **classSchema** -Objekts entfernen.</span><span class="sxs-lookup"><span data-stu-id="3824e-114">A privileged user can subsequently remove an auxiliary class from the **auxiliaryClass** attribute of a **classSchema** object.</span></span>

 

 




