---
description: Weitere Informationen finden Sie in der API. jetprepareupdate-Methode.
title: API. jetprepareupdate-Methode
TOCTitle: 'JetPrepareUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_prep)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetprepareupdate(v=EXCHG.10)
ms:contentKeyID: 55100782
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e8094fef5fcf008dd5f6eb6f2bfd05a0be1bf077
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218277"
---
# <a name="apijetprepareupdate-method"></a><span data-ttu-id="97a4f-103">API. jetprepareupdate-Methode</span><span class="sxs-lookup"><span data-stu-id="97a4f-103">Api.JetPrepareUpdate method</span></span>

<span data-ttu-id="97a4f-104">Vorbereiten eines Cursors für die Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="97a4f-104">Prepare a cursor for update.</span></span>

<span data-ttu-id="97a4f-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="97a4f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="97a4f-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="97a4f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="97a4f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="97a4f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetPrepareUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    prep As JET_prep _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim prep As JET_prepApi.JetPrepareUpdate(sesid, tableid, _
    prep)
```

``` csharp
public static void JetPrepareUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_prep prep
)
```

#### <a name="parameters"></a><span data-ttu-id="97a4f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="97a4f-108">Parameters</span></span>

  - <span data-ttu-id="97a4f-109">-sid</span><span class="sxs-lookup"><span data-stu-id="97a4f-109">sesid</span></span>  
    <span data-ttu-id="97a4f-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="97a4f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="97a4f-111">Die Sitzung, von der das Update gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="97a4f-111">The session which is starting the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="97a4f-112">TableID</span><span class="sxs-lookup"><span data-stu-id="97a4f-112">tableid</span></span>  
    <span data-ttu-id="97a4f-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="97a4f-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="97a4f-114">Der Cursor, für den das Update gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="97a4f-114">The cursor to start the update for.</span></span>

<!-- end list -->

  - <span data-ttu-id="97a4f-115">vorzubereiten</span><span class="sxs-lookup"><span data-stu-id="97a4f-115">prep</span></span>  
    <span data-ttu-id="97a4f-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_prep](./jet-prep-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="97a4f-116">Type: [Microsoft.Isam.Esent.Interop.JET_prep](./jet-prep-enumeration.md)</span></span>  
    
    <span data-ttu-id="97a4f-117">Der Typ des Vorbereitungs Updates.</span><span class="sxs-lookup"><span data-stu-id="97a4f-117">The type of update to prepare.</span></span>

## <a name="see-also"></a><span data-ttu-id="97a4f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97a4f-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="97a4f-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="97a4f-119">Reference</span></span>

[<span data-ttu-id="97a4f-120">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="97a4f-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="97a4f-121">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="97a4f-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="97a4f-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="97a4f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
