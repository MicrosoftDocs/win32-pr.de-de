---
description: Weitere Informationen finden Sie im Feld VistaGrbits.IndexCrossProduct.
title: VistaGrbits.IndexCrossProduct-Feld (Microsoft.Isam.Esent.Interop.Vista)
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
ms.openlocfilehash: ad3828411177d1c500c1b21b62797f093143ba1ac5b9770d9d6444d5c1a7aa9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471130"
---
# <a name="vistagrbitsindexcrossproduct-field"></a>VistaGrbits.IndexCrossProduct-Feld

Wenn Sie dieses Flag für einen Index angeben, der mehr als eine Schlüsselspalte enthält, bei der es sich um eine mehrwertige Spalte handelt, wird für jedes Ergebnis eines Kreuzprodukts aller Werte in diesen Schlüsselspalten ein Indexeintrag erstellt. Andernfalls hätte der Index nur einen Eintrag für jeden Mehrwert in der wichtigsten Schlüsselspalte, bei der es sich um eine mehrwertige Spalte handelt, und jeder dieser Indexeinträge würde den ersten Mehrwert aus allen anderen Schlüsselspalten verwenden, bei denen es sich um mehrwertige Spalten handelt. Wenn Sie dieses Flag beispielsweise für einen Index über Spalte A mit den Werten "red" und "blue" und für Spalte B mit den Werten "1" und "2" angegeben haben, werden die folgenden Indexeinträge erstellt: "red", "1"; "red", "2"; "blue", "1"; "blue", "2". Andernfalls werden die folgenden Indexeinträge erstellt: "red", "1"; "blue", "1".

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[VistaGrbits-Klasse](./vistagrbits-class.md)

[VistaGrbits-Member](./vistagrbits-members.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
