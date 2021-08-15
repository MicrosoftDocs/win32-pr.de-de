---
title: Statisch verknüpfte Hilfsklassen
description: Eine statisch verknüpfte Hilfsklasse ist eine Klasse, die im auxiliaryClass- oder systemAuxiliaryClass-Attribut der classSchema-Definition einer Objektklasse im Schema enthalten ist.
ms.assetid: 24765001-7a60-4654-a23a-bf0326b59096
ms.tgt_platform: multiple
keywords:
- Statisch verknüpfte Ad-Hilfsklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce00592052b1b52f82e2758fdfd7241c6bd24233ce6db6c11389165eeaa5e843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024718"
---
# <a name="statically-linked-auxiliary-classes"></a>Statisch verknüpfte Hilfsklassen

Eine statisch verknüpfte Hilfsklasse ist eine Klasse, die im **auxiliaryClass-** oder **systemAuxiliaryClass-Attribut** der **classSchema-Definition** einer Objektklasse im Schema enthalten ist. Dies bedeutet, dass die Hilfsklasse Teil jeder Instanz der Klasse ist, der sie zugeordnet ist.

Eine Hilfsklasse kann statisch mit einer Objektklasse verknüpft werden, wenn die Klasse definiert wird, d. h. wenn ihr **classSchema-Objekt** dem Schemacontainer hinzugefügt wird. Dies ist der einzige Zeitpunkt, zu dem **systemAuxiliaryClass** verwendet werden kann. Nachdem ein **classSchema-Objekt** erstellt wurde, kann das **systemAuxiliaryClass-Attribut** nicht mehr geändert werden. Eine Hilfsklasse, die zu diesem Zeitpunkt statisch verknüpft ist, kann über obligatorische Attribute (**mustHave**) und/oder optional (**mayHave**) verfügen.

Ein privilegierter Benutzer mit den berechtigungen, die zum Erweitern des Schemas erforderlich sind, kann dem **systemAuxiliaryClass-Attribut** eines vorhandenen **classSchema-Objekts** Hilfsklassen hinzufügen oder daraus entfernen. Dadurch wird die Hilfsklasse aus jeder vorhandenen Instanz der Objektklasse hinzugefügt oder entfernt. Eine Hilfsklasse, die zu diesem Zeitpunkt statisch verknüpft ist, kann optionale Attribute aufweisen, jedoch keine obligatorischen Attribute. Dies liegt daran, dass möglicherweise Instanzen der Objektklasse vorhanden sind. In diesem Fall würde das Hinzufügen eines neuen obligatorischen Attributs zu Problemen führen. Ein privilegierter Benutzer kann anschließend eine Hilfsklasse aus dem **auxiliaryClass-Attribut** eines **classSchema-Objekts** entfernen.

 

 




