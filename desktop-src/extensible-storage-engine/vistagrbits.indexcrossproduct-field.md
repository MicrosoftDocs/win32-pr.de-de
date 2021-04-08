---
description: 'Weitere Informationen finden Sie hier: vistagrbits. indexcrossproduct-Feld'
title: Vistagrbits. indexcrossproduct-Feld (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: IndexCrossProduct field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits.indexcrossproduct(v=EXCHG.10)
ms:contentKeyID: 55104426
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1b16f741c63d455d18a887331505080aef62990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960953"
---
# <a name="vistagrbitsindexcrossproduct-field"></a>Vistagrbits. indexcrossproduct-Feld

Wenn dieses Flag für einen Index angegeben wird, der mehr als eine Schlüssel Spalte aufweist, die eine mehrwertige Spalte ist, führt dies dazu, dass für jedes Ergebnis eines Kreuz Produkts aller Werte in diesen Schlüssel Spalten ein Index Eintrag erstellt wird. Andernfalls würde der Index nur einen Eintrag für jeden multiwert in der signifikantesten Schlüssel Spalte enthalten, bei der es sich um eine mehrwertige Spalte handelt, und jede dieser Indexeinträge würde den ersten mehrwertigen Wert aus anderen Schlüssel Spalten verwenden, die mehrwertige Spalten sind. Wenn Sie z. B. dieses Flag für einen Index über Spalte A mit den Werten "Red" und "Blue" und over column B mit den Werten "1" und "2" angegeben haben, werden die folgenden Indexeinträge erstellt: "Red", "1"; "Red", "2"; "Blue", "1"; "Blue", "2". Andernfalls werden die folgenden Indexeinträge erstellt: "Red", "1"; "Blue", "1".

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Const IndexCrossProduct As CreateIndexGrbit
'Usage
Dim value As CreateIndexGrbit

value = VistaGrbits.IndexCrossProduct
```

``` csharp
public const CreateIndexGrbit IndexCrossProduct
```

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Vistagrbits-Klasse](./vistagrbits-class.md)

[Vistagrbits-Member](./vistagrbits-members.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
