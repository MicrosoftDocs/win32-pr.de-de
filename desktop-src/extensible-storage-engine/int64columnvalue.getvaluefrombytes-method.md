---
description: 'Weitere Informationen finden Sie hier: Int64ColumnValue. getvaluefrombytes-Methode'
title: Int64ColumnValue. getvaluefrombytes-Methode
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Int64ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.int64columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55103365
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Int64ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Int64ColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a33d85fb929f61d67d814ad47eb64406b77e7c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349439"
---
# <a name="int64columnvaluegetvaluefrombytes-method"></a><span data-ttu-id="409fe-103">Int64ColumnValue. getvaluefrombytes-Methode</span><span class="sxs-lookup"><span data-stu-id="409fe-103">Int64ColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="409fe-104">Wenn Sie Daten aus ESENT abrufen, decodieren Sie die Daten, und legen Sie den Wert im ColumnValue-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="409fe-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="409fe-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="409fe-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="409fe-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="409fe-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="409fe-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="409fe-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="409fe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="409fe-108">Parameters</span></span>

  - <span data-ttu-id="409fe-109">value</span><span class="sxs-lookup"><span data-stu-id="409fe-109">value</span></span>  
    <span data-ttu-id="409fe-110">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="409fe-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="409fe-111">Ein Bytearray.</span><span class="sxs-lookup"><span data-stu-id="409fe-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="409fe-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="409fe-112">startIndex</span></span>  
    <span data-ttu-id="409fe-113">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="409fe-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="409fe-114">Die Anfangsposition innerhalb der Bytes.</span><span class="sxs-lookup"><span data-stu-id="409fe-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="409fe-115">count</span><span class="sxs-lookup"><span data-stu-id="409fe-115">count</span></span>  
    <span data-ttu-id="409fe-116">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="409fe-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="409fe-117">Die Anzahl der zu decodierenden Bytes.</span><span class="sxs-lookup"><span data-stu-id="409fe-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="409fe-118">irre</span><span class="sxs-lookup"><span data-stu-id="409fe-118">err</span></span>  
    <span data-ttu-id="409fe-119">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="409fe-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="409fe-120">Der von ESENT zurückgegebene Fehler.</span><span class="sxs-lookup"><span data-stu-id="409fe-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="409fe-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="409fe-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="409fe-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="409fe-122">Reference</span></span>

[<span data-ttu-id="409fe-123">Int64ColumnValue-Klasse</span><span class="sxs-lookup"><span data-stu-id="409fe-123">Int64ColumnValue class</span></span>](./int64columnvalue-class.md)

[<span data-ttu-id="409fe-124">Int64ColumnValue-Member</span><span class="sxs-lookup"><span data-stu-id="409fe-124">Int64ColumnValue members</span></span>](./int64columnvalue-members.md)

[<span data-ttu-id="409fe-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="409fe-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
