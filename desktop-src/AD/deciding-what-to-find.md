---
title: Entscheiden, was gesucht werden soll
description: Bevor Sie ein Verzeichnis durchsuchen, berücksichtigen Sie, wie Ihre Suche basierend auf ihrer Herangehensweise durchgeführt wird. Die Daten und Eigenschaften, die zurückgegeben werden sollen, wirken sich darauf aus, wo Sie eine Suche binden, die Tiefe ihrer Suche, den Abfrage Filter und die Suchleistung.
ms.assetid: 788fa12c-9086-4d8b-bd2e-e96a494a26ad
ms.tgt_platform: multiple
keywords:
- Suchkriterien Active Directory
- entscheiden, was gesucht werden soll Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818b0f9be56830a836453c5e52ceadd52928a522
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036384"
---
# <a name="deciding-what-to-find"></a>Entscheiden, was gesucht werden soll

Bevor Sie ein Verzeichnis durchsuchen, berücksichtigen Sie, wie Ihre Suche basierend auf ihrer Herangehensweise durchgeführt wird. Die Daten und Eigenschaften, die zurückgegeben werden sollen, wirken sich darauf aus, wo Sie eine Suche binden, die Tiefe ihrer Suche, den Abfrage Filter und die Suchleistung.

Wenn Sie z. b. nach allen Benutzer Objekten mit Nachname Smith suchen möchten, geben Sie Folgendes an:



| Bereich                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Such Speicherort            | Ein bestimmter Container oder eine Organisationseinheit (OU) innerhalb einer Domäne, eine bestimmte Domäne, eine bestimmte Domänen Struktur oder die gesamte Gesamtstruktur. Wenn Sie in einem bestimmten Container oder einer Domäne nach Objekten suchen, wird die Suchabfrage besser durchgeführt, indem Sie direkt an diesen Container oder diese Domäne bindet, anstatt eine Unterstruktur Suche in einer Domänen Struktur durchzuführen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Suchtyp             | Wenn Sie das vorhanden sein oder das Abrufen der Eigenschaften eines bestimmten Objekts, das über einen Distinguished Name (DN) verfügt, überprüfen, sollten Sie eine Basis Suche durchführen, bei der nur das Objekt durchsucht wird, an das Sie gebunden sind.<br/> Wenn Sie wissen, dass ein Objekt ein direkter Nachfolger eines bestimmten Containers ist, binden Sie an diesen Container, und führen Sie eine Suche auf einer einzelnen Ebene durch (**attributeSchema** -und **classSchema** -Objekte im Schema Container und erweiterte Rechte Objekte im Container für erweiterte Rechte sind gute Beispiele).<br/> Wenn Sie nicht genau wissen, wo das Objekt ist, oder wenn Sie das Objekt, an das Sie gebunden sind, und alle untergeordneten Objekte in der Verzeichnishierarchie durchsuchen möchten, führen Sie eine Unterstruktur Suche aus.<br/>                                                       |
| Verwenden Sie nach Möglichkeit Indizes. | Wenn Sie nach einer bestimmten Objektklasse suchen, sollte der Abfrage Filter über Ausdrücke verfügen, die Eigenschaften auswerten, die für diese Klasse definiert sind.<br/> Um nach Gruppen Objekten zu suchen, schließen Sie den Ausdruck (objectCategory = Group) in den Filter ein. So suchen Sie nach Benutzer Objekten geben Sie (& (objectClass = User) (objectCategory = Person)) an, weil die Computerklasse von der Benutzerklasse abgeleitet ist. (objectClass = User) gibt also sowohl Benutzer als auch Computer zurück, da sowohl Contact-als auch User-Objekte eine **objectCategory** von Person aufweisen.<br/> Weitere Informationen finden Sie unter [Objektklasse und Objekt Kategorie](object-class-and-object-category.md) und [indizierte Attribute](indexed-attributes.md).<br/> |



 

 

 





