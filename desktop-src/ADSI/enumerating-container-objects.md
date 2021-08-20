---
title: Aufzählen von Containerobjekten
description: Standardmäßig müssen alle Elemente in einer Enumeration in ADSI vom gleichen Automation-Datentyp sein. Beispielsweise sollte eine Enumeration einige Elemente nicht als VARIANT des Typs VT I4 und andere als VARIANT des Typs \_ VT \_ BSTR zurückgeben.
ms.assetid: 155caa67-05db-432b-b813-0d891a502301
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff6bb6d05a34ce6434531338a877d2dd4aaee2cd4df0b38c81b50b7f56db4bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428559"
---
# <a name="enumerating-container-objects"></a>Aufzählen von Containerobjekten

Standardmäßig müssen alle Elemente in einer Enumeration in ADSI vom gleichen Automation-Datentyp sein. Beispielsweise sollte eine Enumeration einige Elemente nicht als **VARIANT** des Typs **VT \_ I4** und andere als **VARIANT** des Typs **VT \_ BSTR zurückgeben.**

Um eine Liste von Elementen aufzählen zu können, die ein Objekt verwaltet, fordert ein Client die Erstellung eines Enumerationsobjekts für den spezifischen Informationstyp an, der aufgelistet wird. In ADSI kann der Client die Objekte in Namespaceobjekten, generischen Containerobjekten, Sammlungsobjekten, Memberobjekten oder Schemaobjekten auflisten. ADSI bietet einen Filter, der mit der [**IADsContainer.Filter-Eigenschaft**](iadscontainer-property-methods.md) festgelegt und geändert werden kann, um die Übereinstimmungen in jeder Enumeration zu beschränken. Beispiele für Implementierungen von Enumeratorobjekten finden Sie im Beispielanbieterkomponentencode für die folgenden ADs-Containerobjekte.



| Objekttyp         | code         |
|---------------------|--------------|
| Generischer Container   | cenumobj.cpp |
| Namespacecontainer | cenumns.cpp  |
| Schemacontainer    | cenumsch.cpp |



 

Clientseitige Informationen finden Sie unter [Sammlungen und Gruppen.](collections-and-groups.md)

 

 




