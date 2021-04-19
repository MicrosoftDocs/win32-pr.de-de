---
description: 'Weitere Informationen finden Sie hier: API. trymuvefirst-Methode'
title: API. trymuvefirst-Methode
TOCTitle: 'TryMoveFirst method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMoveFirst(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymovefirst(v=EXCHG.10)
ms:contentKeyID: 55100946
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMoveFirst
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMoveFirst
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 624fba29ab6fe653b7af674e32b907ea3934d643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342801"
---
# <a name="apitrymovefirst-method"></a><span data-ttu-id="34ca5-103">API. trymuvefirst-Methode</span><span class="sxs-lookup"><span data-stu-id="34ca5-103">Api.TryMoveFirst method</span></span>

<span data-ttu-id="34ca5-104">Versuchen Sie, zum ersten Datensatz in der Tabelle zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="34ca5-104">Try to move to the first record in the table.</span></span> <span data-ttu-id="34ca5-105">Wenn die Tabelle leer ist, wird false zurückgegeben. Wenn ein anderer Fehler auftritt, wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="34ca5-105">If the table is empty this returns false, if a different error is encountered an exception is thrown.</span></span>

<span data-ttu-id="34ca5-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="34ca5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="34ca5-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="34ca5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="34ca5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="34ca5-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMoveFirst ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryMoveFirst(sesid, _
    tableid)
```

``` csharp
public static bool TryMoveFirst(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="34ca5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="34ca5-109">Parameters</span></span>

  - <span data-ttu-id="34ca5-110">-sid</span><span class="sxs-lookup"><span data-stu-id="34ca5-110">sesid</span></span>  
    <span data-ttu-id="34ca5-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="34ca5-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="34ca5-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="34ca5-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="34ca5-113">TableID</span><span class="sxs-lookup"><span data-stu-id="34ca5-113">tableid</span></span>  
    <span data-ttu-id="34ca5-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="34ca5-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="34ca5-115">Der Cursor, der positioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="34ca5-115">The cursor to position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="34ca5-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34ca5-116">Return value</span></span>

<span data-ttu-id="34ca5-117">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="34ca5-117">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="34ca5-118">True, wenn die Verschiebung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="34ca5-118">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="34ca5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34ca5-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="34ca5-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="34ca5-120">Reference</span></span>

[<span data-ttu-id="34ca5-121">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="34ca5-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="34ca5-122">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="34ca5-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="34ca5-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="34ca5-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
