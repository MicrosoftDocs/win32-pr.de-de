---
description: 'Weitere Informationen finden Sie hier: JET_CALLBACK-Delegaten'
title: JET_CALLBACK Delegat
TOCTitle: JET_CALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_CALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_callback(v=EXCHG.10)
ms:contentKeyID: 39515752
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK..ctor
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.Invoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 617cbefba047f822b338627a782be7e016c2a16f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373287"
---
# <a name="jet_callback-delegate"></a><span data-ttu-id="e2a7c-103">JET_CALLBACK Delegat</span><span class="sxs-lookup"><span data-stu-id="e2a7c-103">JET_CALLBACK delegate</span></span>

<span data-ttu-id="e2a7c-104">Eine multizweck-Rückruffunktion, die von der Datenbank-Engine verwendet wird, um die Anwendung über ein Ereignis mit Online Defragmentierung und Cursor Zustands Benachrichtigungen zu informieren.</span><span class="sxs-lookup"><span data-stu-id="e2a7c-104">A multi-purpose callback function used by the database engine to inform the application of an event involving online defragmentation and cursor state notifications.</span></span>

<span data-ttu-id="e2a7c-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e2a7c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e2a7c-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e2a7c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e2a7c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2a7c-107">Syntax</span></span>

``` vb
'Declaration
Public Delegate Function JET_CALLBACK ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    arg1 As Object, _
    arg2 As Object, _
    context As IntPtr, _
    unused As IntPtr _
) As JET_err
'Usage
Dim instance As New JET_CALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_CALLBACK(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    Object arg1,
    Object arg2,
    IntPtr context,
    IntPtr unused
)
```

#### <a name="parameters"></a><span data-ttu-id="e2a7c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2a7c-108">Parameters</span></span>

  - <span data-ttu-id="e2a7c-109">-sid</span><span class="sxs-lookup"><span data-stu-id="e2a7c-109">sesid</span></span>  
    <span data-ttu-id="e2a7c-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e2a7c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e2a7c-111">Die Sitzung, für die der Rückruf erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e2a7c-111">The session for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2a7c-112">dbid</span><span class="sxs-lookup"><span data-stu-id="e2a7c-112">dbid</span></span>  
    <span data-ttu-id="e2a7c-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e2a7c-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="e2a7c-114">Die Datenbank, für die der Rückruf erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e2a7c-114">The database for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2a7c-115">TableID</span><span class="sxs-lookup"><span data-stu-id="e2a7c-115">tableid</span></span>  
    <span data-ttu-id="e2a7c-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e2a7c-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e2a7c-117">Der Cursor, für den der Rückruf erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e2a7c-117">The cursor for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2a7c-118">cbyp</span><span class="sxs-lookup"><span data-stu-id="e2a7c-118">cbtyp</span></span>  
    <span data-ttu-id="e2a7c-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e2a7c-119">Type: [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="e2a7c-120">Der Vorgang, für den der Rückruf durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2a7c-120">The operation for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2a7c-121">arg1</span><span class="sxs-lookup"><span data-stu-id="e2a7c-121">arg1</span></span>  
    <span data-ttu-id="e2a7c-122">Type: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="e2a7c-122">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="e2a7c-123">Das erste Rückruf spezifische Argument.</span><span class="sxs-lookup"><span data-stu-id="e2a7c-123">First callback-specific argument.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2a7c-124">arg2</span><span class="sxs-lookup"><span data-stu-id="e2a7c-124">arg2</span></span>  
    <span data-ttu-id="e2a7c-125">Type: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="e2a7c-125">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="e2a7c-126">Zweites Rückruf spezifisches Argument.</span><span class="sxs-lookup"><span data-stu-id="e2a7c-126">Second callback-specific argument.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2a7c-127">context</span><span class="sxs-lookup"><span data-stu-id="e2a7c-127">context</span></span>  
    <span data-ttu-id="e2a7c-128">Typ: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="e2a7c-128">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="e2a7c-129">Rückruf Kontext.</span><span class="sxs-lookup"><span data-stu-id="e2a7c-129">Callback context.</span></span>

<!-- end list -->

  - <span data-ttu-id="e2a7c-130">unused</span><span class="sxs-lookup"><span data-stu-id="e2a7c-130">unused</span></span>  
    <span data-ttu-id="e2a7c-131">Typ: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="e2a7c-131">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="e2a7c-132">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2a7c-132">This parameter is not used.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e2a7c-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2a7c-133">Return value</span></span>

<span data-ttu-id="e2a7c-134">Typ: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e2a7c-134">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e2a7c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2a7c-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e2a7c-136">Referenz</span><span class="sxs-lookup"><span data-stu-id="e2a7c-136">Reference</span></span>

[<span data-ttu-id="e2a7c-137">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2a7c-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
