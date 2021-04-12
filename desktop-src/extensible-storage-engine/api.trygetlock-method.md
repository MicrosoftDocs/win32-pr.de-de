---
description: Weitere Informationen finden Sie in der API. trygetlock-Methode.
title: API. trygetlock-Methode
TOCTitle: 'TryGetLock method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryGetLock(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.GetLockGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trygetlock(v=EXCHG.10)
ms:contentKeyID: 55100934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryGetLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryGetLock
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ecd4e0e66226d438b4e5a78b2397f5637154096
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218273"
---
# <a name="apitrygetlock-method"></a><span data-ttu-id="67317-103">API. trygetlock-Methode</span><span class="sxs-lookup"><span data-stu-id="67317-103">Api.TryGetLock method</span></span>

<span data-ttu-id="67317-104">Reservieren Sie explizit die Möglichkeit, eine Zeile zu aktualisieren, eine Sperre zu schreiben oder explizit zu verhindern, dass eine Zeile von einer anderen Sitzung aktualisiert wird, und lesen Sie sperren.</span><span class="sxs-lookup"><span data-stu-id="67317-104">Explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="67317-105">Normalerweise werden Zeilen Schreib Sperren implizit durch das Aktualisieren von Zeilen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="67317-105">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="67317-106">Lese Sperren sind in der Regel aufgrund von Daten Satz Versionsverwaltung nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="67317-106">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="67317-107">In einigen Fällen möchte eine Transaktion jedoch möglicherweise eine Zeile explizit sperren, um die Serialisierung zu erzwingen, oder um sicherzustellen, dass ein nachfolgender Vorgang erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67317-107">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed.</span></span>

<span data-ttu-id="67317-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="67317-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="67317-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="67317-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="67317-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="67317-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryGetLock ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As GetLockGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As GetLockGrbit
Dim returnValue As Boolean

returnValue = Api.TryGetLock(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TryGetLock(
    JET_SESID sesid,
    JET_TABLEID tableid,
    GetLockGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="67317-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="67317-111">Parameters</span></span>

  - <span data-ttu-id="67317-112">-sid</span><span class="sxs-lookup"><span data-stu-id="67317-112">sesid</span></span>  
    <span data-ttu-id="67317-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="67317-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="67317-114">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="67317-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="67317-115">TableID</span><span class="sxs-lookup"><span data-stu-id="67317-115">tableid</span></span>  
    <span data-ttu-id="67317-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="67317-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="67317-117">Der zu verwendende Cursor.</span><span class="sxs-lookup"><span data-stu-id="67317-117">The cursor to use.</span></span> <span data-ttu-id="67317-118">Eine Sperre für den aktuellen Datensatz wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="67317-118">A lock will be acquired on the current record.</span></span>

<!-- end list -->

  - <span data-ttu-id="67317-119">grbit</span><span class="sxs-lookup"><span data-stu-id="67317-119">grbit</span></span>  
    <span data-ttu-id="67317-120">Typ: [Microsoft. ISAM. ESENT. Interop. getlockgrbit](./getlockgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="67317-120">Type: [Microsoft.Isam.Esent.Interop.GetLockGrbit](./getlockgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="67317-121">Sperr Optionen verwenden Sie diese Option, um den Typ der abzurufenden Sperre anzugeben.</span><span class="sxs-lookup"><span data-stu-id="67317-121">Lock options, use this to specify which type of lock to obtain.</span></span>

#### <a name="return-value"></a><span data-ttu-id="67317-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67317-122">Return value</span></span>

<span data-ttu-id="67317-123">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="67317-123">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="67317-124">True, wenn die Sperre abgerufen wurde, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="67317-124">True if the lock was obtained, false otherwise.</span></span> <span data-ttu-id="67317-125">Eine Ausnahme wird ausgelöst, wenn ein unerwarteter Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="67317-125">An exception is thrown if an unexpected error is encountered.</span></span>  

## <a name="see-also"></a><span data-ttu-id="67317-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67317-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="67317-127">Referenz</span><span class="sxs-lookup"><span data-stu-id="67317-127">Reference</span></span>

[<span data-ttu-id="67317-128">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="67317-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="67317-129">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="67317-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="67317-130">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="67317-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
