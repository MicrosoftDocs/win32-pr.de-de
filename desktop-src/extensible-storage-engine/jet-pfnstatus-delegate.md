---
description: 'Weitere Informationen finden Sie hier: JET_PFNSTATUS-Delegaten'
title: JET_PFNSTATUS Delegat
TOCTitle: JET_PFNSTATUS delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnstatus(v=EXCHG.10)
ms:contentKeyID: 39515654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.BeginInvoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16cc5807d858f964f995b449a0a0eee78659aefd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347729"
---
# <a name="jet_pfnstatus-delegate"></a><span data-ttu-id="e79f7-103">JET_PFNSTATUS Delegat</span><span class="sxs-lookup"><span data-stu-id="e79f7-103">JET_PFNSTATUS delegate</span></span>

<span data-ttu-id="e79f7-104">Empfängt Informationen zum Fortschritt von Vorgängen mit langer Ausführungszeit, z. b. Defragmentierungs-, Sicherungs-oder Wiederherstellungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="e79f7-104">Receives information about the progress of long-running operations, such as defragmentation, backup, or restore operations.</span></span> <span data-ttu-id="e79f7-105">Bei solchen Vorgängen Ruft die Datenbank-Engine diese Rückruffunktion auf, um ein Update für den Fortschritt des Vorgangs zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e79f7-105">During such operations, the database engine calls this callback function to give an update on the progress of the operation.</span></span>

<span data-ttu-id="e79f7-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e79f7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e79f7-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e79f7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e79f7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e79f7-108">Syntax</span></span>

``` vb
'Declaration
Public Delegate Function JET_PFNSTATUS ( _
    sesid As JET_SESID, _
    snp As JET_SNP, _
    snt As JET_SNT, _
    data As Object _
) As JET_err
'Usage
Dim instance As New JET_PFNSTATUS(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNSTATUS(
    JET_SESID sesid,
    JET_SNP snp,
    JET_SNT snt,
    Object data
)
```

#### <a name="parameters"></a><span data-ttu-id="e79f7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e79f7-109">Parameters</span></span>

  - <span data-ttu-id="e79f7-110">-sid</span><span class="sxs-lookup"><span data-stu-id="e79f7-110">sesid</span></span>  
    <span data-ttu-id="e79f7-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e79f7-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e79f7-112">Die Sitzung, mit der der Vorgang mit langer Laufzeit aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e79f7-112">The session with which the long running operation was called.</span></span>

<!-- end list -->

  - <span data-ttu-id="e79f7-113">SNP</span><span class="sxs-lookup"><span data-stu-id="e79f7-113">snp</span></span>  
    <span data-ttu-id="e79f7-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SNP](./jet-snp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e79f7-114">Type: [Microsoft.Isam.Esent.Interop.JET_SNP](./jet-snp-enumeration.md)</span></span>  
    
    <span data-ttu-id="e79f7-115">Der Typ des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e79f7-115">The type of operation.</span></span>

<!-- end list -->

  - <span data-ttu-id="e79f7-116">SNT</span><span class="sxs-lookup"><span data-stu-id="e79f7-116">snt</span></span>  
    <span data-ttu-id="e79f7-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SNT](./jet-snt-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e79f7-117">Type: [Microsoft.Isam.Esent.Interop.JET_SNT](./jet-snt-enumeration.md)</span></span>  
    
    <span data-ttu-id="e79f7-118">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e79f7-118">The status of the operation.</span></span>

<!-- end list -->

  - <span data-ttu-id="e79f7-119">Daten</span><span class="sxs-lookup"><span data-stu-id="e79f7-119">data</span></span>  
    <span data-ttu-id="e79f7-120">Type: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="e79f7-120">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="e79f7-121">Optionale Daten.</span><span class="sxs-lookup"><span data-stu-id="e79f7-121">Optional data.</span></span> <span data-ttu-id="e79f7-122">Kann ein [JET_SNPROG](./jet-snprog-class.md)sein.</span><span class="sxs-lookup"><span data-stu-id="e79f7-122">May be a [JET_SNPROG](./jet-snprog-class.md).</span></span>

#### <a name="return-value"></a><span data-ttu-id="e79f7-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e79f7-123">Return value</span></span>

<span data-ttu-id="e79f7-124">Typ: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e79f7-124">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e79f7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e79f7-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e79f7-126">Referenz</span><span class="sxs-lookup"><span data-stu-id="e79f7-126">Reference</span></span>

[<span data-ttu-id="e79f7-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e79f7-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
