---
description: 'ICE05 überprüft, ob bestimmte Tabellen erforderliche Einträge enthalten. Dies umfasst, ist aber nicht darauf beschränkt, die Tabelle Property auf die erforderlichen Eigenschaften zu überprüfen: ProductName, ProductLanguage, ProductVersion, ProductCode und Manufacturer.'
ms.assetid: 90b35758-c9d9-4104-a352-f0b17b04b571
title: ICE05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94766ed0a311243b47c2214ea21de89576d533f0d1fa76f776dedfa3afdc7da0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142558"
---
# <a name="ice05"></a>ICE05

ICE05 überprüft, ob bestimmte Tabellen erforderliche Einträge enthalten. Dies umfasst, ist aber nicht darauf beschränkt, die [Property](property-table.md) -Tabelle auf die erforderlichen Eigenschaften zu überprüfen: [**ProductName**](productname.md), [**ProductLanguage**](productlanguage.md), [**ProductVersion**](productversion.md), [**ProductCode**](productcode.md)und [**Manufacturer**](manufacturer.md).

## <a name="result"></a>Ergebnis

ICE05 gibt einen Fehler aus, wenn ein erforderlicher Eintrag fehlt.

## <a name="example"></a>Beispiel

Für das gezeigte Beispiel würde ICE05 melden, dass der Eintrag "ProductVersion" in der Tabelle "Property" erforderlich ist.

[Eigenschaftentabelle](property-table.md) (partiell)



| Eigenschaft                           | Wert     |
|------------------------------------|-----------|
| [**Productname**](productname.md) | MyProduct |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



