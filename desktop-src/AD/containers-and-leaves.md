---
title: Container und Blätter
description: Active Directory Domain Services eine Hierarchie von Objekten enthalten, in der jede Objektinstanz, mit Ausnahme des Stamm Verzeichnisses der Verzeichnishierarchie, in einem anderen Objekt enthalten ist.
ms.assetid: ef17e84c-6c7f-4ebe-a904-fead6c27518d
ms.tgt_platform: multiple
keywords:
- Container und Blätter Active Directory
- Blatt Active Directory
- Container Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9039e4619ea0bd50d20c3bd425b6a8536a1034
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472645"
---
# <a name="containers-and-leaves"></a>Container und Blätter

Active Directory Domain Services eine Hierarchie von Objekten enthalten, in der jede Objektinstanz, mit Ausnahme des Stamm Verzeichnisses der Verzeichnishierarchie, in einem anderen Objekt enthalten ist. Die Struktur dieser Hierarchie ist flexibler als ein Dateisystem von Verzeichnissen und Dateien. Stattdessen bestimmen Regeln im [Active Directory Schema](active-directory-schema.md), welche Objektklassen Instanzen enthalten können, die andere Objektklassen enthalten. Die Standardschema Definition der [**Benutzer**](/windows/desktop/ADSchema/c-user) Objektklasse enthält z. b. die [**Organisationseinheiten-**](/windows/desktop/ADSchema/c-organizationalunit) und [**Container**](/windows/desktop/ADSchema/c-container) Objektklassen als mögliche Endknoten. Das heißt, mögliche übergeordnete Objekte oder Container einer **Benutzer** Objektinstanz. Dies bedeutet, dass ein Objekt der **Organisationseinheit** ein **Benutzer** Objekt enthalten kann, aber ein **Benutzer** Objekt kann kein anderes **Benutzer** Objekt enthalten, es sei denn, die Schema Definition der **Benutzer** Klasse wird geändert.

Mit Ausnahme von Schema Objekten, d. h. den [**classSchema**](/windows/desktop/ADSchema/c-classschema) -oder [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Objekten, die die Klassen und Attribute definieren, die in einer Server Gesamtstruktur vorhanden sein können, kann jedes Objekt in Active Directory Domain Services ein Container sein. Jede Objektklasse, die im Attribut " [**possvorgesetzten**](/windows/desktop/ADSchema/a-posssuperiors) " oder " [**systempossvorgesetzten**](/windows/desktop/ADSchema/a-systemposssuperiors) " einer Objektklassen Definition angezeigt wird, ist möglicherweise ein Container. Weitere Informationen zu Containern einer vordefinierten Objektklasse finden Sie unter [Active Directory Domain Services Referenz](active-directory-domain-services-reference.md). Sie können Programm gesteuert an das abstrakte Schema binden und die [**iadsclass:: get- \_ Containment**](/windows/desktop/api/iads/nn-iads-iadsclass) -Methode oder die [**iadsclass \_ :: Get**](/windows/desktop/api/iads/nn-iads-iadsclass) -Methode verwenden, um die Klassen zu erhalten, die eine bestimmte Klasse enthalten oder enthalten kann. Weitere Informationen finden Sie unter [Lesen des abstrakten Schemas](reading-the-abstract-schema.md). Sie können auch das Attribut " [**PossibleInferiors**](/windows/desktop/ADSchema/a-possibleinferiors) " jeder Objektinstanz lesen, um die Objektklassen zu bestimmen, die das Objekt enthalten kann. Beachten Sie, dass **PossibleInferiors** ein konstruiertes Attribut ist, d. h., es wird aus den **Besitz** enden / **systempossvorgänger** -Werten der anderen Klassendefinitionen berechnet und nicht tatsächlich im Verzeichnis gespeichert.

Beachten Sie, dass das Active Directory Schema eine [**Container**](/windows/desktop/ADSchema/c-container) Klasse definiert. Wie bereits erläutert, ist es nicht erforderlich, dass ein Objekt eine Instanz der **Container** Klasse als Container ist. Es gibt auch eine [**Blatt**](/windows/desktop/ADSchema/c-leaf) Klasse, und obwohl es sich bei Unterklassen dieser Klasse in der Regel nicht um Container handelt, gibt es keinen Grund, warum dies nicht der Fall sein kann.

Schließlich können Sie für den mit einer Objektklasse verknüpften Anzeige Spezifizierer ein Flag festlegen, um anzugeben, dass Benutzeroberflächen immer Instanzen der Klasse als Blätter anstatt als Container anzeigen sollen. Dadurch wird verhindert, dass die Benutzeroberfläche durch zu viele Container überlastet wird. Weitere Informationen finden Sie unter [Anzeigen von Containern als Blattknoten](viewing-containers-as-leaf-nodes.md).

 

 