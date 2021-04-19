---
description: Weitere Informationen finden Sie in der API. jetdefragment-Methode.
title: API. jetdefragment-Methode
TOCTitle: 'JetDefragment method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment(v=EXCHG.10)
ms:contentKeyID: 55100679
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 69428d785bf9d607199cb62bfe02d2e373e7dbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344419"
---
# <a name="apijetdefragment-method"></a><span data-ttu-id="82356-103">API. jetdefragment-Methode</span><span class="sxs-lookup"><span data-stu-id="82356-103">Api.JetDefragment method</span></span>

<span data-ttu-id="82356-104">Startet und beendet datenbankdefragmentierungsaufgaben, die die Datenorganisation innerhalb einer Datenbank verbessern.</span><span class="sxs-lookup"><span data-stu-id="82356-104">Starts and stops database defragmentation tasks that improves data organization within a database.</span></span>

<span data-ttu-id="82356-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="82356-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="82356-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="82356-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="82356-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="82356-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetDefragment ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment(sesid, _
    dbid, tableName, passes, seconds, _
    grbit)
```

``` csharp
public static JET_wrn JetDefragment(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="82356-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="82356-108">Parameters</span></span>

  - <span data-ttu-id="82356-109">-sid</span><span class="sxs-lookup"><span data-stu-id="82356-109">sesid</span></span>  
    <span data-ttu-id="82356-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="82356-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="82356-111">Die für den-Befehl zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="82356-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="82356-112">dbid</span><span class="sxs-lookup"><span data-stu-id="82356-112">dbid</span></span>  
    <span data-ttu-id="82356-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="82356-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="82356-114">Die Datenbank, die deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="82356-114">The database to be defragmented.</span></span>

<!-- end list -->

  - <span data-ttu-id="82356-115">tableName</span><span class="sxs-lookup"><span data-stu-id="82356-115">tableName</span></span>  
    <span data-ttu-id="82356-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="82356-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="82356-117">Nicht verwendeter Parameter.</span><span class="sxs-lookup"><span data-stu-id="82356-117">Unused parameter.</span></span> <span data-ttu-id="82356-118">Die Defragmentierung wird für die gesamte Datenbank ausgeführt, die durch die angegebene Datenbank-ID beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="82356-118">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<!-- end list -->

  - <span data-ttu-id="82356-119">ausweisen</span><span class="sxs-lookup"><span data-stu-id="82356-119">passes</span></span>  
    <span data-ttu-id="82356-120">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="82356-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="82356-121">Wenn eine Online Defragmentierung gestartet wird, wird mit diesem Parameter die maximale Anzahl von defragmentierungsläufen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82356-121">When starting an online defragmentation task, this parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="82356-122">Wenn Sie eine Online Defragmentierung beenden, wird dieser Parameter auf die Anzahl der durchgeführten Durchläufen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82356-122">When stopping an online defragmentation task, this parameter is set to the number of passes performed.</span></span>

<!-- end list -->

  - <span data-ttu-id="82356-123">Sekunden</span><span class="sxs-lookup"><span data-stu-id="82356-123">seconds</span></span>  
    <span data-ttu-id="82356-124">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="82356-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="82356-125">Wenn eine Online Defragmentierung gestartet wird, legt dieser Parameter die maximale Zeit für die Defragmentierung fest.</span><span class="sxs-lookup"><span data-stu-id="82356-125">When starting an online defragmentation task, this parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="82356-126">Wenn Sie eine Online Defragmentierung beenden, wird dieser Ausgabepuffer auf die für die Defragmentierung verwendete Zeitspanne festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82356-126">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<!-- end list -->

  - <span data-ttu-id="82356-127">grbit</span><span class="sxs-lookup"><span data-stu-id="82356-127">grbit</span></span>  
    <span data-ttu-id="82356-128">Typ: [Microsoft. ISAM. ESENT. Interop. defraggrbit](./defraggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="82356-128">Type: [Microsoft.Isam.Esent.Interop.DefragGrbit](./defraggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="82356-129">Defragmentierungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="82356-129">Defragmentation options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="82356-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82356-130">Return value</span></span>

<span data-ttu-id="82356-131">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="82356-131">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="82356-132">Ein Warnungs Code.</span><span class="sxs-lookup"><span data-stu-id="82356-132">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="82356-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82356-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="82356-134">Referenz</span><span class="sxs-lookup"><span data-stu-id="82356-134">Reference</span></span>

[<span data-ttu-id="82356-135">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="82356-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="82356-136">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="82356-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="82356-137">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="82356-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
