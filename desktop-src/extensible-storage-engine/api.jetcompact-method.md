---
description: Weitere Informationen finden Sie in der API. jetcompact-Methode.
title: API. jetcompact-Methode
TOCTitle: 'JetCompact method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCompact(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS,Microsoft.Isam.Esent.Interop.JET_CONVERT,Microsoft.Isam.Esent.Interop.CompactGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcompact(v=EXCHG.10)
ms:contentKeyID: 55100666
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74d714a1b0fa8d53743945afb3a35cc2015df293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958810"
---
# <a name="apijetcompact-method"></a><span data-ttu-id="1ea64-103">API. jetcompact-Methode</span><span class="sxs-lookup"><span data-stu-id="1ea64-103">Api.JetCompact method</span></span>

<span data-ttu-id="1ea64-104">Erstellt eine Kopie einer vorhandenen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1ea64-104">Makes a copy of an existing database.</span></span> <span data-ttu-id="1ea64-105">Die Kopie wird zu einem für die Verwendung optimalen Zustand komprimiert.</span><span class="sxs-lookup"><span data-stu-id="1ea64-105">The copy is compacted to a state optimal for usage.</span></span> <span data-ttu-id="1ea64-106">Die Daten in den kopierten Daten werden entsprechend den Measures verpackt, die bei der Indexerstellung für die Indizes ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="1ea64-106">Data in the copied data will be packed according to the measures chosen for the indexes at index create.</span></span> <span data-ttu-id="1ea64-107">Auf diese Weise können komprimierte Daten so dicht wie möglich gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1ea64-107">In this way, compacted data may be stored as densely as possible.</span></span> <span data-ttu-id="1ea64-108">Alternativ können durch komprimierte Datenspeicher Platz für nachfolgende Daten Satz Vergrößerung oder Index Einfügungen reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="1ea64-108">Alternatively, compacted data may reserve space for subsequent record growth or index insertions.</span></span>

<span data-ttu-id="1ea64-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1ea64-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1ea64-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1ea64-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1ea64-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ea64-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCompact ( _
    sesid As JET_SESID, _
    sourceDatabase As String, _
    destinationDatabase As String, _
    statusCallback As JET_PFNSTATUS, _
    ignored As JET_CONVERT, _
    grbit As CompactGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim sourceDatabase As String
Dim destinationDatabase As String
Dim statusCallback As JET_PFNSTATUS
Dim ignored As JET_CONVERT
Dim grbit As CompactGrbitApi.JetCompact(sesid, sourceDatabase, _
    destinationDatabase, statusCallback, _
    ignored, grbit)
```

``` csharp
public static void JetCompact(
    JET_SESID sesid,
    string sourceDatabase,
    string destinationDatabase,
    JET_PFNSTATUS statusCallback,
    JET_CONVERT ignored,
    CompactGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1ea64-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ea64-112">Parameters</span></span>

  - <span data-ttu-id="1ea64-113">-sid</span><span class="sxs-lookup"><span data-stu-id="1ea64-113">sesid</span></span>  
    <span data-ttu-id="1ea64-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1ea64-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1ea64-115">Die für den-Befehl zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1ea64-115">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ea64-116">sourceDatabase</span><span class="sxs-lookup"><span data-stu-id="1ea64-116">sourceDatabase</span></span>  
    <span data-ttu-id="1ea64-117">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1ea64-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1ea64-118">Die Quelldatenbank, die komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="1ea64-118">The source database that will be compacted.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ea64-119">destinationDatabase</span><span class="sxs-lookup"><span data-stu-id="1ea64-119">destinationDatabase</span></span>  
    <span data-ttu-id="1ea64-120">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1ea64-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1ea64-121">Der Name, der für die komprimierte Datenbank verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ea64-121">The name to use for the compacted database.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ea64-122">Status Rückruf</span><span class="sxs-lookup"><span data-stu-id="1ea64-122">statusCallback</span></span>  
    <span data-ttu-id="1ea64-123">Typ: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="1ea64-123">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="1ea64-124">Eine Rückruffunktion, die regelmäßig über den Daten Bank Compact-Vorgang aufgerufen werden kann, um den Status zu melden.</span><span class="sxs-lookup"><span data-stu-id="1ea64-124">A callback function that can be called periodically through the database compact operation to report progress.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ea64-125">wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1ea64-125">ignored</span></span>  
    <span data-ttu-id="1ea64-126">Typ: [Microsoft.ISAM.ESENT.Interop.JET_CONVERT](./jet-convert-class.md)</span><span class="sxs-lookup"><span data-stu-id="1ea64-126">Type: [Microsoft.Isam.Esent.Interop.JET_CONVERT](./jet-convert-class.md)</span></span>  
    
    <span data-ttu-id="1ea64-127">Dieser Parameter wird ignoriert und sollte NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1ea64-127">This parameter is ignored and should be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ea64-128">grbit</span><span class="sxs-lookup"><span data-stu-id="1ea64-128">grbit</span></span>  
    <span data-ttu-id="1ea64-129">Typ: [Microsoft. ISAM. ESENT. Interop. compactgrbit](./compactgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1ea64-129">Type: [Microsoft.Isam.Esent.Interop.CompactGrbit](./compactgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1ea64-130">Compact-Optionen.</span><span class="sxs-lookup"><span data-stu-id="1ea64-130">Compact options.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ea64-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ea64-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1ea64-132">Referenz</span><span class="sxs-lookup"><span data-stu-id="1ea64-132">Reference</span></span>

[<span data-ttu-id="1ea64-133">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="1ea64-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1ea64-134">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="1ea64-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1ea64-135">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="1ea64-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
