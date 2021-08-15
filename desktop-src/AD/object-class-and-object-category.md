---
title: Objektklasse und Objektkategorie
description: Jede Instanz einer Objektklasse verfügt über eine mehrwertige objectClass-Eigenschaft, die die Klasse identifiziert, von der das Objekt eine Instanz ist, sowie alle strukturellen oder abstrakten Superklassen, von denen diese Klasse abgeleitet wird.
ms.assetid: b3c5f9ee-98e0-42dd-9b61-3731e14b9cd4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35e7f461caa27e8668cfc47cd94852bf53b291658b828ea017e3dc00a19d39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185697"
---
# <a name="object-class-and-object-category"></a>Objektklasse und Objektkategorie

Jede Instanz einer Objektklasse verfügt über eine mehrwertige [**objectClass-Eigenschaft,**](/windows/desktop/ADSchema/a-objectclass) die die Klasse identifiziert, von der das Objekt eine Instanz ist, sowie alle strukturellen oder abstrakten Superklassen, von denen diese Klasse abgeleitet wird. Daher würde die **objectClass-Eigenschaft** eines Benutzerobjekts die [**obersten**](/windows/desktop/ADSchema/c-top) [**Benutzerklassen**](/windows/desktop/ADSchema/c-user) , [**person**](/windows/desktop/ADSchema/c-person), [**organizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)und identifizieren. Die **objectClass-Eigenschaft** enthält keine zusätzlichen Klassen in der Liste. Das System legt den **objectClass-Wert** fest, wenn die Objektinstanz erstellt wird, und kann nicht geändert werden.

Jede Instanz einer Objektklasse verfügt auch über eine [**objectCategory-Eigenschaft,**](/windows/desktop/ADSchema/a-objectcategory) bei der es sich um eine einwertige Eigenschaft handelt, die den Distinguished Name der Klasse enthält, deren Objekt eine Instanz oder eine ihrer Übergeordneten Klassen ist. Wenn ein Objekt erstellt wird, legt das System seine **objectCategory-Eigenschaft** auf den Wert fest, der von der [**defaultObjectCategory-Eigenschaft**](/windows/desktop/ADSchema/a-defaultobjectcategory) seiner Objektklasse angegeben wird. Die **objectCategory-Eigenschaft** eines Objekts kann nicht geändert werden.

Weitere Informationen und ein Codebeispiel zum Abrufen der [**objectClass-Eigenschaft**](/windows/desktop/ADSchema/a-objectclass) eines Objekts finden Sie unter [Abrufen des objectClass-Attributs.](retrieving-the-objectclass-property.md)

> [!IMPORTANT]
> Vor Windows Server 2008 wurde das [**objectClass-Attribut**](/windows/desktop/ADSchema/a-objectclass) nicht indiziert. Dies liegt daran, dass sie über mehrere Werte verfügt und in hohem Maße nicht eindeutig ist. Das heißt, jede Instanz des **objectClass-Attributs** enthält die [**oberste**](/windows/desktop/ADSchema/c-top) Klasse. Dies bedeutet, dass ein Index sehr groß und ineffektiv wäre. Um Objekte einer bestimmten Klasse zu suchen, verwenden Sie das [**objectCategory-Attribut,**](/windows/desktop/ADSchema/a-objectcategory) das einwertig und indiziert ist. Weitere Informationen zur Verwendung dieser Eigenschaften in Suchfiltern finden Sie unter [Entscheidung, was gesucht werden soll.](deciding-what-to-find.md)

 

Für die meisten Klassen ist [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) der Distinguished Name des [**classSchema-Objekts**](/windows/desktop/ADSchema/c-classschema) der Klasse. Die **defaultObjectCategory-Klasse** für die [**organizationalUnit-Klasse**](/windows/desktop/ADSchema/c-organizationalunit) ist beispielsweise "CN=Organizational-Unit,CN=Schema,CN=Configuration,<DC=forestroot>". Einige Klassen verweisen jedoch auf eine andere Klasse als **defaultObjectCategory**. Dadurch kann eine Abfrage Gruppen verwandter Objekte leicht finden, auch wenn sie von unterschiedlichen Klassen sind. Beispielsweise identifizieren die [**Benutzer-,**](/windows/desktop/ADSchema/c-user) [**Personen-, Organisationsperson-**](/windows/desktop/ADSchema/c-organizationalperson)und [**Kontaktklassen**](/windows/desktop/ADSchema/c-contact) alle die **Person-Klasse** in ihren [](/windows/desktop/ADSchema/c-person) **defaultObjectCategory-Eigenschaften.** Dadurch können Suchfilter wie (objectCategory=person) Instanzen aller dieser Klassen mit einer einzelnen Abfrage suchen. Abfragen für Personen sind sehr häufig, sodass dies eine einfache Optimierung ist.

Wenn Sie eine Unterklasse aus einer strukturellen Klasse erstellen, besteht die bewährte Methode darin, den [**defaultObjectCategory-Wert**](/windows/desktop/ADSchema/a-defaultobjectcategory) der neuen Klasse auf den gleichen Distinguished Name der Übergeordneten Klasse festzulegen. Dadurch kann die Standard-Benutzeroberfläche die Unterklasse "suchen".

 

 