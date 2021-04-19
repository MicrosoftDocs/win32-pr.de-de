---
description: Weitere Informationen finden Sie in der API. trymuveprevious-Methode.
title: API. trymuveprevious-Methode
TOCTitle: 'TryMovePrevious method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMovePrevious(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymoveprevious(v=EXCHG.10)
ms:contentKeyID: 55100940
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMovePrevious
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMovePrevious
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe512ac4443f670ac73964a422bd9606d903055a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356110"
---
# <a name="apitrymoveprevious-method"></a><span data-ttu-id="db1d3-103">API. trymuveprevious-Methode</span><span class="sxs-lookup"><span data-stu-id="db1d3-103">Api.TryMovePrevious method</span></span>

<span data-ttu-id="db1d3-104">Versuchen Sie, zum vorherigen Datensatz in der Tabelle zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="db1d3-104">Try to move to the previous record in the table.</span></span> <span data-ttu-id="db1d3-105">Wenn kein vorheriger Datensatz vorhanden ist, wird false zurückgegeben. Wenn ein anderer Fehler auftritt, wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="db1d3-105">If there is not a previous record this returns false, if a different error is encountered an exception is thrown.</span></span>

<span data-ttu-id="db1d3-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="db1d3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="db1d3-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="db1d3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="db1d3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="db1d3-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMovePrevious ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryMovePrevious(sesid, _
    tableid)
```

``` csharp
public static bool TryMovePrevious(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="db1d3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="db1d3-109">Parameters</span></span>

  - <span data-ttu-id="db1d3-110">-sid</span><span class="sxs-lookup"><span data-stu-id="db1d3-110">sesid</span></span>  
    <span data-ttu-id="db1d3-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="db1d3-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="db1d3-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="db1d3-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="db1d3-113">TableID</span><span class="sxs-lookup"><span data-stu-id="db1d3-113">tableid</span></span>  
    <span data-ttu-id="db1d3-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="db1d3-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="db1d3-115">Der Cursor, der positioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="db1d3-115">The cursor to position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="db1d3-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db1d3-116">Return value</span></span>

<span data-ttu-id="db1d3-117">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="db1d3-117">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="db1d3-118">True, wenn die Verschiebung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="db1d3-118">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="db1d3-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db1d3-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="db1d3-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="db1d3-120">Reference</span></span>

[<span data-ttu-id="db1d3-121">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="db1d3-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="db1d3-122">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="db1d3-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="db1d3-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="db1d3-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
