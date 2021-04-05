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
# <a name="statically-linked-auxiliary-classes"></a>Statisch verknüpfte Hilfsklassen

Eine statisch verknüpfte Hilfsklasse ist eine, die im-Schema im **auxiliaryClass** -oder **systemAuxiliaryClass** -Attribut der **classSchema** -Definition einer Objektklasse enthalten ist. Dies bedeutet, dass die Hilfsklasse Teil jeder Instanz der Klasse ist, der Sie zugeordnet ist.

Eine Hilfsklasse kann statisch mit einer Objektklasse verknüpft werden, wenn die Klasse definiert ist, d. h., wenn Ihr **classSchema** -Objekt dem Schema Container hinzugefügt wird. Dies ist der einzige Zeitpunkt, an dem die **systemAuxiliaryClass** verwendet werden kann. Nachdem ein **classSchema** -Objekt erstellt wurde, kann das zugehörige **systemAuxiliaryClass** -Attribut nicht geändert werden. Eine Hilfsklasse, die zu diesem Zeitpunkt statisch verknüpft ist, kann über verbindliche (**musthave**) und/oder optionale (**mayhat**) Attribute verfügen.

Ein privilegierter Benutzer mit den Berechtigungen, die zum Erweitern des Schemas erforderlich sind, kann Hilfsklassen aus dem Attribut " **systemAuxiliaryClass** " eines vorhandenen **classSchema** -Objekts hinzufügen oder entfernen. Dadurch wird die Hilfsklasse aus jeder vorhandenen Instanz der Objektklasse hinzugefügt oder daraus entfernt. Eine Hilfsklasse, die zu diesem Zeitpunkt statisch verknüpft ist, kann über optionale Attribute verfügen, aber keine obligatorischen Attribute besitzen. Dies liegt daran, dass es möglicherweise vorhandene Instanzen der Objektklasse gibt. in diesem Fall würden durch das Hinzufügen eines neuen obligatorischen Attributs Probleme entstehen. Ein privilegierter Benutzer kann anschließend eine Hilfsklasse aus dem **auxiliaryClass** -Attribut eines **classSchema** -Objekts entfernen.

 

 




