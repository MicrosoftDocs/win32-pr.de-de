---
title: Dynamische Hilfsklassen
description: Ähnlich wie bei strukturellen und abstrakten Objektklassen werden zusätzliche Klassen durch ein classSchema-Objekt im Active Directory Schema definiert.
ms.assetid: bd5f6aed-c79a-4c03-ad03-a4ae00f0b888
ms.tgt_platform: multiple
keywords:
- Dynamische Hilfsklassen AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c13fc8231b5232b82a61b9409f1736e5bd9249
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472580"
---
# <a name="dynamic-auxiliary-classes"></a>Dynamische Hilfsklassen

Ähnlich wie bei strukturellen und abstrakten Objektklassen werden zusätzliche Klassen durch ein [**classSchema**](/windows/desktop/ADSchema/c-classschema) -Objekt im Active Directory Schema definiert. Weitere Informationen finden Sie unter [Struktur-, abstrakte und Hilfsklassen](structural-abstract-and-auxiliary-classes.md). Diese Schema Definition gibt verschiedene Merkmale der-Klasse an, einschließlich der Attribute, die der-Klasse zugeordnet sind.

Anders als bei Struktur Klassen können Sie eine Instanz einer Hilfsklasse nicht wie bei einer strukturellen Klasse erstellen. Stattdessen verwenden Sie eine Hilfsklasse, um die Liste der Attribute zu erweitern, die einer anderen Struktur-, abstrakten oder zusätzlichen Objektklasse zugeordnet sind.

In der ersten Version von Windows 2000 hat Active Directory Domain Services Unterstützung für das statische Verknüpfen von Erweiterungs Klassen mit der [**classSchema**](/windows/desktop/ADSchema/c-classschema) -Definition einer anderen Objektklasse bereitgestellt. Wenn eine zusätzliche Klasse auf diese Weise verwendet wird, unterstützt jede Instanz der Objektklasse die Attribute der Erweiterungs Klasse.

**Windows 2000-Server und früher:** Active Directory Domain Services bietet keine Unterstützung für das dynamische Verknüpfen von Erweiterungs Klassen mit einzelnen Objekten, nicht nur für ganze Klassen von Objekten. Außerdem können zusätzliche Klassen, die an eine Objektinstanz angefügt wurden, anschließend nicht aus der Instanz entfernt werden.

**Windows Server 2003:** Dynamische Erweiterungs Klassen werden unterstützt, wenn auf allen Domänen Controllern in der Gesamtstruktur Windows Server 2003 und der Gesamtstruktur Funktionsmodus Windows Server 2003 ausgeführt wird.

Weitere Informationen zu Erweiterungs Klassen finden Sie unter:

-   [Dynamisch verknüpfte Hilfsklassen](dynamically-linked-auxiliary-classes.md)
-   [Statisch verknüpfte Hilfsklassen](statically-linked-auxiliary-classes.md)
-   [Bestimmen der Klassen, die einer Objektinstanz zugeordnet sind](determining-the-classes-associated-with-an-object-instance.md)
-   [Hinzufügen einer Hilfsklasse zu einer Objektinstanz](adding-an-auxiliary-class-to-an-object-instance.md)

Weitere Informationen zu Gesamtstruktur Funktionsebenen finden Sie unter "Vorgehensweise beim erhöhen Active Directory Domänen-und Gesamtstruktur Funktionsebenen" in der Hilfe-und Support Knowledge Base unter [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692) .

 

 