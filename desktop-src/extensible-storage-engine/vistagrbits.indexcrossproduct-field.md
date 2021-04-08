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
# <a name="vistagrbitsindexcrossproduct-field"></a><span data-ttu-id="ca581-103">Vistagrbits. indexcrossproduct-Feld</span><span class="sxs-lookup"><span data-stu-id="ca581-103">VistaGrbits.IndexCrossProduct field</span></span>

<span data-ttu-id="ca581-104">Wenn dieses Flag für einen Index angegeben wird, der mehr als eine Schlüssel Spalte aufweist, die eine mehrwertige Spalte ist, führt dies dazu, dass für jedes Ergebnis eines Kreuz Produkts aller Werte in diesen Schlüssel Spalten ein Index Eintrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ca581-104">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="ca581-105">Andernfalls würde der Index nur einen Eintrag für jeden multiwert in der signifikantesten Schlüssel Spalte enthalten, bei der es sich um eine mehrwertige Spalte handelt, und jede dieser Indexeinträge würde den ersten mehrwertigen Wert aus anderen Schlüssel Spalten verwenden, die mehrwertige Spalten sind.</span><span class="sxs-lookup"><span data-stu-id="ca581-105">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="ca581-106">Wenn Sie z. B. dieses Flag für einen Index über Spalte A mit den Werten "Red" und "Blue" und over column B mit den Werten "1" und "2" angegeben haben, werden die folgenden Indexeinträge erstellt: "Red", "1"; "Red", "2"; "Blue", "1"; "Blue", "2".</span><span class="sxs-lookup"><span data-stu-id="ca581-106">For example, if you specified this flag for an index over column A that has the values "red" and "blue" and over column B that has the values "1" and "2" then the following index entries would be created: "red", "1"; "red", "2"; "blue", "1"; "blue", "2".</span></span> <span data-ttu-id="ca581-107">Andernfalls werden die folgenden Indexeinträge erstellt: "Red", "1"; "Blue", "1".</span><span class="sxs-lookup"><span data-stu-id="ca581-107">Otherwise, the following index entries would be created: "red", "1"; "blue", "1".</span></span>

<span data-ttu-id="ca581-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ca581-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="ca581-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ca581-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ca581-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca581-110">Syntax</span></span>

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

## <a name="see-also"></a><span data-ttu-id="ca581-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca581-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ca581-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="ca581-112">Reference</span></span>

[<span data-ttu-id="ca581-113">Vistagrbits-Klasse</span><span class="sxs-lookup"><span data-stu-id="ca581-113">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="ca581-114">Vistagrbits-Member</span><span class="sxs-lookup"><span data-stu-id="ca581-114">VistaGrbits members</span></span>](./vistagrbits-members.md)

[<span data-ttu-id="ca581-115">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="ca581-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
