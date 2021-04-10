---
title: Objektklasse und Objekt Kategorie
description: Jede Instanz einer Objektklasse verfügt über eine mehrwertige objectClass-Eigenschaft, die die Klasse identifiziert, für die das Objekt eine Instanz ist, sowie alle strukturellen oder abstrakten Element, von denen diese Klasse abgeleitet ist.
ms.assetid: b3c5f9ee-98e0-42dd-9b61-3731e14b9cd4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74941b4f32cc197d3dbbf3aa0dc3179b4098ee8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948553"
---
# <a name="object-class-and-object-category"></a>Objektklasse und Objekt Kategorie

Jede Instanz einer Objektklasse verfügt über eine mehrwertige [**objectClass**](/windows/desktop/ADSchema/a-objectclass) -Eigenschaft, die die Klasse identifiziert, für die das Objekt eine Instanz ist, sowie alle strukturellen oder abstrakten Element, von denen diese Klasse abgeleitet ist. Folglich identifiziert die **objectClass** -Eigenschaft eines User-Objekts die Klassen " [**Top**](/windows/desktop/ADSchema/c-top)", " [**Person**](/windows/desktop/ADSchema/c-person)", " [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)" und " [**User**](/windows/desktop/ADSchema/c-user) ". Die **objectClass** -Eigenschaft enthält keine Erweiterungs Klassen in der Liste. Das System legt den **objectClass** -Wert fest, wenn die Objektinstanz erstellt wird, und kann nicht geändert werden.

Jede Instanz einer Objektklasse verfügt auch über eine [**objectCategory**](/windows/desktop/ADSchema/a-objectcategory) -Eigenschaft, bei der es sich um eine Eigenschaft mit einem Wert handelt, die den Distinguished Name der Klasse enthält, für die das Objekt eine Instanz oder eine der übergeordneten Klassen ist. Wenn ein Objekt erstellt wird, legt das System seine **objectCategory** -Eigenschaft auf den Wert fest, der von der [**defaultobjectcategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) -Eigenschaft der zugehörigen Objektklasse angegeben wird. Die **objectCategory** -Eigenschaft eines Objekts kann nicht geändert werden.

Weitere Informationen und ein Codebeispiel, in dem die [**objectClass**](/windows/desktop/ADSchema/a-objectclass) -Eigenschaft eines Objekts abgerufen wird, finden Sie unter [Abrufen des Attributs "objectClass](retrieving-the-objectclass-property.md)".

> [!IMPORTANT]
> Vor Windows Server 2008 ist das [**objectClass**](/windows/desktop/ADSchema/a-objectclass) -Attribut nicht indiziert. Dies liegt daran, dass Sie über mehrere Werte verfügt und stark nicht eindeutig ist. Das heißt, jede Instanz des **objectClass** -Attributs enthält die [**Top**](/windows/desktop/ADSchema/c-top) -Klasse. Dies bedeutet, dass ein Index sehr groß und wirkungslos wäre. Um Objekte einer bestimmten Klasse zu suchen, verwenden Sie das [**objectCategory**](/windows/desktop/ADSchema/a-objectcategory) -Attribut, das einwertig und indiziert ist. Weitere Informationen zum Verwenden dieser Eigenschaften in Suchfiltern finden Sie unter [entscheiden, was](deciding-what-to-find.md)gesucht werden soll.

 

Bei den meisten Klassen ist die [**defaultobjectcategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) der Distinguished Name des [**classSchema**](/windows/desktop/ADSchema/c-classschema) -Objekts der Klasse. Die **defaultobjectcategory** für die [**OrganizationalUnit**](/windows/desktop/ADSchema/c-organizationalunit) -Klasse lautet z. b. "CN = Organisationseinheit, CN = Schema, CN = Configuration, <DC = forestroot>". Einige Klassen verweisen jedoch auf eine andere Klasse als **defaultobjectcategory**. Dadurch kann eine Abfrage Gruppen verwandter Objekte problemlos finden, auch wenn Sie unterschiedliche Klassen haben. Beispielsweise identifizieren die Klassen [**User**](/windows/desktop/ADSchema/c-user), [**Person**](/windows/desktop/ADSchema/c-person), [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)und [**Contact**](/windows/desktop/ADSchema/c-contact) alle die **Person** -Klasse in Ihren **defaultobjectcategory** -Eigenschaften. Dies ermöglicht Suchfiltern wie (objectCategory = Person) das Auffinden von Instanzen dieser Klassen mit einer einzelnen Abfrage. Abfragen für Personen sind sehr häufig, sodass es sich hierbei um eine einfache Optimierung handelt.

Wenn Sie eine Unterklasse aus einer strukturellen Klasse erstellen, empfiehlt es sich, den [**defaultobjectcategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) -Wert der neuen Klasse auf denselben Distinguished Name der übergeordneten Klasse festzulegen. Dadurch kann die Standardbenutzer Oberfläche die Unterklasse "finden".

 

 