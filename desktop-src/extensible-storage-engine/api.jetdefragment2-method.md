---
description: Weitere Informationen finden Sie in der API. JetDefragment2-Methode.
title: API. JetDefragment2-Methode
TOCTitle: 'JetDefragment2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.JET_CALLBACK,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment2(v=EXCHG.10)
ms:contentKeyID: 55100696
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b22c89b304103954a2088bf05ba98797777489be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346501"
---
# <a name="apijetdefragment2-method"></a><span data-ttu-id="50690-103">API. JetDefragment2-Methode</span><span class="sxs-lookup"><span data-stu-id="50690-103">Api.JetDefragment2 method</span></span>

<span data-ttu-id="50690-104">Startet und beendet datenbankdefragmentierungsaufgaben, die die Datenorganisation innerhalb einer Datenbank verbessern.</span><span class="sxs-lookup"><span data-stu-id="50690-104">Starts and stops database defragmentation tasks that improves data organization within a database.</span></span>

<span data-ttu-id="50690-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="50690-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="50690-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="50690-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="50690-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="50690-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetDefragment2 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    callback As JET_CALLBACK, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim callback As JET_CALLBACK
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment2(sesid, _
    dbid, tableName, passes, seconds, _
    callback, grbit)
```

``` csharp
public static JET_wrn JetDefragment2(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    JET_CALLBACK callback,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="50690-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="50690-108">Parameters</span></span>

  - <span data-ttu-id="50690-109">-sid</span><span class="sxs-lookup"><span data-stu-id="50690-109">sesid</span></span>  
    <span data-ttu-id="50690-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="50690-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="50690-111">Die für den-Befehl zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="50690-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="50690-112">dbid</span><span class="sxs-lookup"><span data-stu-id="50690-112">dbid</span></span>  
    <span data-ttu-id="50690-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="50690-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="50690-114">Die Datenbank, die deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="50690-114">The database to be defragmented.</span></span>

<!-- end list -->

  - <span data-ttu-id="50690-115">tableName</span><span class="sxs-lookup"><span data-stu-id="50690-115">tableName</span></span>  
    <span data-ttu-id="50690-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="50690-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="50690-117">Nicht verwendeter Parameter.</span><span class="sxs-lookup"><span data-stu-id="50690-117">Unused parameter.</span></span> <span data-ttu-id="50690-118">Die Defragmentierung wird für die gesamte Datenbank ausgeführt, die durch die angegebene Datenbank-ID beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="50690-118">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<!-- end list -->

  - <span data-ttu-id="50690-119">ausweisen</span><span class="sxs-lookup"><span data-stu-id="50690-119">passes</span></span>  
    <span data-ttu-id="50690-120">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="50690-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="50690-121">Wenn eine Online Defragmentierung gestartet wird, wird mit diesem Parameter die maximale Anzahl von defragmentierungsläufen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="50690-121">When starting an online defragmentation task, this parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="50690-122">Wenn Sie eine Online Defragmentierung beenden, wird dieser Parameter auf die Anzahl der durchgeführten Durchläufen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="50690-122">When stopping an online defragmentation task, this parameter is set to the number of passes performed.</span></span>

<!-- end list -->

  - <span data-ttu-id="50690-123">Sekunden</span><span class="sxs-lookup"><span data-stu-id="50690-123">seconds</span></span>  
    <span data-ttu-id="50690-124">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="50690-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="50690-125">Wenn eine Online Defragmentierung gestartet wird, legt dieser Parameter die maximale Zeit für die Defragmentierung fest.</span><span class="sxs-lookup"><span data-stu-id="50690-125">When starting an online defragmentation task, this parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="50690-126">Wenn Sie eine Online Defragmentierung beenden, wird dieser Ausgabepuffer auf die für die Defragmentierung verwendete Zeitspanne festgelegt.</span><span class="sxs-lookup"><span data-stu-id="50690-126">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<!-- end list -->

  - <span data-ttu-id="50690-127">Rückruf</span><span class="sxs-lookup"><span data-stu-id="50690-127">callback</span></span>  
    <span data-ttu-id="50690-128">Typ: [Microsoft.ISAM.ESENT.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="50690-128">Type: [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span></span>  
    
    <span data-ttu-id="50690-129">Rückruffunktion, die defragmentiert, um den Fortschritt zu melden.</span><span class="sxs-lookup"><span data-stu-id="50690-129">Callback function that defrag uses to report progress.</span></span>

<!-- end list -->

  - <span data-ttu-id="50690-130">grbit</span><span class="sxs-lookup"><span data-stu-id="50690-130">grbit</span></span>  
    <span data-ttu-id="50690-131">Typ: [Microsoft. ISAM. ESENT. Interop. defraggrbit](./defraggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="50690-131">Type: [Microsoft.Isam.Esent.Interop.DefragGrbit](./defraggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="50690-132">Defragmentierungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="50690-132">Defragmentation options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50690-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50690-133">Return value</span></span>

<span data-ttu-id="50690-134">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="50690-134">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="50690-135">Ein Warnungs Code.</span><span class="sxs-lookup"><span data-stu-id="50690-135">A warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="50690-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50690-136">Remarks</span></span>

<span data-ttu-id="50690-137">Der an JetDefragment2 über gegebene Rückruf kann asynchron ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="50690-137">The callback passed to JetDefragment2 can be executed asynchronously.</span></span> <span data-ttu-id="50690-138">Der GC weiß nicht, dass der nicht verwaltete Code einen Verweis auf den Rückruf hat, daher ist es wichtig sicherzustellen, dass der Rückruf nicht erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="50690-138">The GC doesn't know that the unmanaged code has a reference to the callback so it is important to make sure the callback isn't collected.</span></span>

## <a name="see-also"></a><span data-ttu-id="50690-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50690-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="50690-140">Referenz</span><span class="sxs-lookup"><span data-stu-id="50690-140">Reference</span></span>

[<span data-ttu-id="50690-141">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="50690-141">Api class</span></span>](./api-class.md)

[<span data-ttu-id="50690-142">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="50690-142">Api members</span></span>](./api-members.md)

[<span data-ttu-id="50690-143">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="50690-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
