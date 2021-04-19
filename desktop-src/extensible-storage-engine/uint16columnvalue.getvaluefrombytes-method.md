---
description: 'Weitere Informationen finden Sie hier: UInt16ColumnValue. getvaluefrombytes-Methode'
title: UInt16ColumnValue. getvaluefrombytes-Methode
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.UInt16ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.uint16columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55104191
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.UInt16ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.UInt16ColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5df0a21587dfa30c01d04879db0c5370b8371287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363348"
---
# <a name="uint16columnvaluegetvaluefrombytes-method"></a><span data-ttu-id="a178c-103">UInt16ColumnValue. getvaluefrombytes-Methode</span><span class="sxs-lookup"><span data-stu-id="a178c-103">UInt16ColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="a178c-104">Wenn Sie Daten aus ESENT abrufen, decodieren Sie die Daten, und legen Sie den Wert im ColumnValue-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="a178c-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="a178c-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a178c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a178c-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a178c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a178c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a178c-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="a178c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a178c-108">Parameters</span></span>

  - <span data-ttu-id="a178c-109">value</span><span class="sxs-lookup"><span data-stu-id="a178c-109">value</span></span>  
    <span data-ttu-id="a178c-110">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="a178c-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="a178c-111">Ein Bytearray.</span><span class="sxs-lookup"><span data-stu-id="a178c-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="a178c-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="a178c-112">startIndex</span></span>  
    <span data-ttu-id="a178c-113">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a178c-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a178c-114">Die Anfangsposition innerhalb der Bytes.</span><span class="sxs-lookup"><span data-stu-id="a178c-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="a178c-115">count</span><span class="sxs-lookup"><span data-stu-id="a178c-115">count</span></span>  
    <span data-ttu-id="a178c-116">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a178c-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a178c-117">Die Anzahl der zu decodierenden Bytes.</span><span class="sxs-lookup"><span data-stu-id="a178c-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="a178c-118">irre</span><span class="sxs-lookup"><span data-stu-id="a178c-118">err</span></span>  
    <span data-ttu-id="a178c-119">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a178c-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a178c-120">Der von ESENT zurückgegebene Fehler.</span><span class="sxs-lookup"><span data-stu-id="a178c-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="a178c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a178c-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a178c-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="a178c-122">Reference</span></span>

[<span data-ttu-id="a178c-123">UInt16ColumnValue-Klasse</span><span class="sxs-lookup"><span data-stu-id="a178c-123">UInt16ColumnValue class</span></span>](./uint16columnvalue-class.md)

[<span data-ttu-id="a178c-124">UInt16ColumnValue-Member</span><span class="sxs-lookup"><span data-stu-id="a178c-124">UInt16ColumnValue members</span></span>](./uint16columnvalue-members.md)

[<span data-ttu-id="a178c-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="a178c-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
