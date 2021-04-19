---
description: Weitere Informationen finden Sie in der floatcolumnvalue. getvaluefromb tes-Methode.
title: Floatcolumnvalue. getvaluefrombytes-Methode
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.FloatColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.floatcolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55103242
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.FloatColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.FloatColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 21fade2ca6c2febc5c28bdad217f450f81c2673f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372921"
---
# <a name="floatcolumnvaluegetvaluefrombytes-method"></a><span data-ttu-id="8fa4f-103">Floatcolumnvalue. getvaluefrombytes-Methode</span><span class="sxs-lookup"><span data-stu-id="8fa4f-103">FloatColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="8fa4f-104">Wenn Sie Daten aus ESENT abrufen, decodieren Sie die Daten, und legen Sie den Wert im ColumnValue-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="8fa4f-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="8fa4f-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8fa4f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8fa4f-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8fa4f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8fa4f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fa4f-107">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub GetValueFromBytes ( _
    value As Byte(), _
    startIndex As Integer, _
    count As Integer, _
    err As Integer _
)
'Usage
Dim value As Byte()
Dim startIndex As Integer
Dim count As Integer
Dim err As Integer

Me.GetValueFromBytes(value, startIndex, _
    count, err)
```

``` csharp
protected override void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a><span data-ttu-id="8fa4f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fa4f-108">Parameters</span></span>

  - <span data-ttu-id="8fa4f-109">value</span><span class="sxs-lookup"><span data-stu-id="8fa4f-109">value</span></span>  
    <span data-ttu-id="8fa4f-110">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="8fa4f-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="8fa4f-111">Ein Bytearray.</span><span class="sxs-lookup"><span data-stu-id="8fa4f-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="8fa4f-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="8fa4f-112">startIndex</span></span>  
    <span data-ttu-id="8fa4f-113">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8fa4f-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8fa4f-114">Die Anfangsposition innerhalb der Bytes.</span><span class="sxs-lookup"><span data-stu-id="8fa4f-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="8fa4f-115">count</span><span class="sxs-lookup"><span data-stu-id="8fa4f-115">count</span></span>  
    <span data-ttu-id="8fa4f-116">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8fa4f-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8fa4f-117">Die Anzahl der zu decodierenden Bytes.</span><span class="sxs-lookup"><span data-stu-id="8fa4f-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="8fa4f-118">irre</span><span class="sxs-lookup"><span data-stu-id="8fa4f-118">err</span></span>  
    <span data-ttu-id="8fa4f-119">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8fa4f-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8fa4f-120">Der von ESENT zurückgegebene Fehler.</span><span class="sxs-lookup"><span data-stu-id="8fa4f-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="8fa4f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fa4f-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8fa4f-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="8fa4f-122">Reference</span></span>

[<span data-ttu-id="8fa4f-123">Floatcolumnvalue-Klasse</span><span class="sxs-lookup"><span data-stu-id="8fa4f-123">FloatColumnValue class</span></span>](./floatcolumnvalue-class.md)

[<span data-ttu-id="8fa4f-124">Floatcolumnvalue-Member</span><span class="sxs-lookup"><span data-stu-id="8fa4f-124">FloatColumnValue members</span></span>](./floatcolumnvalue-members.md)

[<span data-ttu-id="8fa4f-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="8fa4f-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
