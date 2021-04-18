---
description: Weitere Informationen finden Sie in der ColumnValue. length-Eigenschaft.
title: ColumnValue. length (Eigenschaft)
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55101208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Length
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c64e2b8e7b25be5b33d64591e16b982604e2fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354865"
---
# <a name="columnvaluelength-property"></a><span data-ttu-id="2cc4e-103">ColumnValue. length (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2cc4e-103">ColumnValue.Length property</span></span>

<span data-ttu-id="2cc4e-104">Ruft die Byte Länge eines Spaltenwerts ab, der 0 (null) ist, wenn die Spalte NULL ist, andernfalls die Größe für Spalten mit fester Größe und die tatsächliche Bytelänge für Spalten mit variabler Größe (z. b. Binär und Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="2cc4e-104">Gets the byte length of a column value, which is zero if column is null, otherwise it matches the Size for fixed-size columns and represent the actual value byte length for variable sized columns (i.e. binary and string).</span></span> <span data-ttu-id="2cc4e-105">Für Zeichen folgen wird die Länge in der Annahme von zwei Bytes pro Zeichen bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2cc4e-105">For strings the length is determined in assumption two bytes per character.</span></span>

<span data-ttu-id="2cc4e-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2cc4e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2cc4e-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2cc4e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2cc4e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cc4e-108">Syntax</span></span>

``` vb
'Declaration
Public MustOverride ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As ColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public abstract int Length { get; }
```

#### <a name="property-value"></a><span data-ttu-id="2cc4e-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2cc4e-109">Property value</span></span>

<span data-ttu-id="2cc4e-110">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2cc4e-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="2cc4e-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cc4e-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2cc4e-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="2cc4e-112">Reference</span></span>

[<span data-ttu-id="2cc4e-113">ColumnValue-Klasse</span><span class="sxs-lookup"><span data-stu-id="2cc4e-113">ColumnValue class</span></span>](./columnvalue-class.md)

[<span data-ttu-id="2cc4e-114">ColumnValue-Member</span><span class="sxs-lookup"><span data-stu-id="2cc4e-114">ColumnValue members</span></span>](./columnvalue-members.md)

[<span data-ttu-id="2cc4e-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="2cc4e-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
