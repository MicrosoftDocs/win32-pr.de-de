---
description: Weitere Informationen finden Sie in der datetimecolumnvalue. Size-Eigenschaft.
title: Datetimecolumnvalue. Size-Eigenschaft
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.DateTimeColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.datetimecolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55101209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DateTimeColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DateTimeColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.DateTimeColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a006cafa81f46ca36d5bb76aa678122c2c6eab66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106361723"
---
# <a name="datetimecolumnvaluesize-property"></a><span data-ttu-id="0d011-103">Datetimecolumnvalue. Size-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0d011-103">DateTimeColumnValue.Size property</span></span>

<span data-ttu-id="0d011-104">Ruft die Größe des Werts in der Spalte ab.</span><span class="sxs-lookup"><span data-stu-id="0d011-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="0d011-105">Dadurch wird 0 für Spalten variabler Größen (z. b. Binär und Zeichenfolge) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0d011-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="0d011-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0d011-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0d011-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0d011-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0d011-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d011-108">Syntax</span></span>

``` vb
'Declaration
Protected Overrides ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected override int Size { get; }
```

#### <a name="property-value"></a><span data-ttu-id="0d011-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0d011-109">Property value</span></span>

<span data-ttu-id="0d011-110">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0d011-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="0d011-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d011-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0d011-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="0d011-112">Reference</span></span>

[<span data-ttu-id="0d011-113">Datetimecolumnvalue-Klasse</span><span class="sxs-lookup"><span data-stu-id="0d011-113">DateTimeColumnValue class</span></span>](./datetimecolumnvalue-class.md)

[<span data-ttu-id="0d011-114">Datetimecolumnvalue-Member</span><span class="sxs-lookup"><span data-stu-id="0d011-114">DateTimeColumnValue members</span></span>](./datetimecolumnvalue-members.md)

[<span data-ttu-id="0d011-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="0d011-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
