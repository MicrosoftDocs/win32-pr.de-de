---
title: Auflisten von Container Objekten
description: Gemäß der Konvention müssen alle Elemente in einer Enumeration in ADSI denselben Automatisierungs Datentyp aufweisen. Beispielsweise sollte eine Enumeration einige Elemente nicht als Variante vom Typ VT \_ I4 und andere als Variante des Typs VT BSTR zurückgeben \_ .
ms.assetid: 155caa67-05db-432b-b813-0d891a502301
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5514596b02521fa869ffd7c712dcac2cacb40192
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341215"
---
# <a name="enumerating-container-objects"></a>Auflisten von Container Objekten

Gemäß der Konvention müssen alle Elemente in einer Enumeration in ADSI denselben Automatisierungs Datentyp aufweisen. Beispielsweise sollte eine Enumeration einige Elemente nicht als **Variante** vom Typ **VT \_ I4** und andere als **Variante** des Typs **VT \_ BSTR** zurückgeben.

Zum Auflisten einer Liste von Elementen, die von einem Objekt verwaltet werden, fordert ein Client die Erstellung eines Enumerationsobjekt für den bestimmten Typ der aufgelisteten Informationen an. In ADSI kann der Client die Objekte in Namespace Objekten, generischen Container Objekten, Auflistungs Objekten, Element Objekten oder Schema Objekten auflisten. ADSI stellt einen Filter bereit, der festgelegt und geändert werden kann, um die Übereinstimmungen in einer Enumeration mit der [**IADsContainer. Filter**](iadscontainer-property-methods.md) -Eigenschaft einzuschränken. Beispiele für Implementierungen von enumeratorobjekten finden Sie im Beispiel Anbieter-Komponenten Code für die folgenden ADS-Containerobjekte.



| Objekttyp         | code         |
|---------------------|--------------|
| Generischer Container   | cenumubj. cpp |
| Namespace Container | cenum NS. cpp  |
| Schema Container    | cenum Sch. cpp |



 

Informationen zu Client seitigen Informationen finden Sie unter [Sammlungen und Gruppen](collections-and-groups.md).

 

 




