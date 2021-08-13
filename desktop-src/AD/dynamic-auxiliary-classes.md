---
title: Dynamische Hilfsklassen
description: Ähnlich wie strukturelle und abstrakte Objektklassen werden Hilfsklassen durch ein classSchema-Objekt im Active Directory-Schema definiert.
ms.assetid: bd5f6aed-c79a-4c03-ad03-a4ae00f0b888
ms.tgt_platform: multiple
keywords:
- Dynamische Hilfsklassen AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce88f525b5d72a271aab1746a0ce0d0b308cb7022c4702433b82038c101435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429900"
---
# <a name="dynamic-auxiliary-classes"></a>Dynamische Hilfsklassen

Ähnlich wie strukturelle und abstrakte Objektklassen werden Hilfsklassen durch ein [**classSchema-Objekt**](/windows/desktop/ADSchema/c-classschema) im Active Directory-Schema definiert. Weitere Informationen finden Sie unter [Strukturelle, Abstrakte und Hilfsklassen.](structural-abstract-and-auxiliary-classes.md) Diese Schemadefinition gibt verschiedene Merkmale der -Klasse an, einschließlich der Attribute, die der -Klasse zugeordnet sind.

Im Gegensatz zu strukturellen Klassen können Sie eine Instanz einer Hilfsklasse nicht wie mit einer strukturellen Klasse erstellen. Stattdessen verwenden Sie eine Hilfsklasse, um die Liste der Attribute zu erweitern, die einer anderen Struktur-, Abstrakten- oder Hilfsobjektklasse zugeordnet sind.

In der ersten Version von Windows 2000 Active Directory Domain Services Unterstützung für das statische Verknüpfen von Hilfsklassen mit der [**classSchema-Definition**](/windows/desktop/ADSchema/c-classschema) einer anderen Objektklasse bereitgestellt. Wenn auf diese Weise eine Hilfsklasse verwendet wird, unterstützt jede Instanz der Objektklasse die Attribute der Hilfsklasse.

**Windows 2000 Server und früher:** Active Directory Domain Services bietet keine Unterstützung für das dynamische Verknüpfen von Hilfsklassen mit einzelnen Objekten und nicht nur mit ganzen Klassen von Objekten. Darüber hinaus können zusätzliche Klassen, die an eine Objektinstanz angefügt wurden, nicht später aus der -Instanz entfernt werden.

**Windows Server 2003:** Dynamische Hilfsklassen werden unterstützt, wenn alle Domänencontroller in der Gesamtstruktur Windows Server 2003 ausgeführt werden und der Gesamtstrukturfunktionsmodus Windows Server 2003 lautet.

Weitere Informationen zu Hilfsklassen finden Sie unter:

-   [Dynamisch verknüpfte Hilfsklassen](dynamically-linked-auxiliary-classes.md)
-   [Statisch verknüpfte Hilfsklassen](statically-linked-auxiliary-classes.md)
-   [Bestimmen der klassen, die einer Objektinstanz zugeordnet sind](determining-the-classes-associated-with-an-object-instance.md)
-   [Hinzufügen einer Hilfsklasse zu einer Objektinstanz](adding-an-auxiliary-class-to-an-object-instance.md)

Weitere Informationen zu Gesamtstrukturfunktionsebenen finden Sie unter "Heraufstufen von Active Directory-Domänen- und -Gesamtstrukturfunktionsebenen" im Hilfe- und Support-Knowledge Base unter [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692) .

 

 