---
description: 'Weitere Informationen finden Sie hier: updaterkonstruktor'
title: Updaterkonstruktor
TOCTitle: 'Update constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_prep)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.update(v=EXCHG.10)
ms:contentKeyID: 55104189
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.Update
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 841403523e0cae7c71fb8fa0861c1d400a26a726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351471"
---
# <a name="update-constructor"></a><span data-ttu-id="dedf5-103">Updaterkonstruktor</span><span class="sxs-lookup"><span data-stu-id="dedf5-103">Update constructor</span></span>

<span data-ttu-id="dedf5-104">Initialisiert eine neue Instanz der Update-Klasse.</span><span class="sxs-lookup"><span data-stu-id="dedf5-104">Initializes a new instance of the Update class.</span></span> <span data-ttu-id="dedf5-105">Dadurch wird automatisch ein Update gestartet.</span><span class="sxs-lookup"><span data-stu-id="dedf5-105">This automatically begins an update.</span></span> <span data-ttu-id="dedf5-106">Das Update wird abgebrochen, wenn es nicht explizit gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="dedf5-106">The update will be cancelled if not explicitly saved.</span></span>

<span data-ttu-id="dedf5-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dedf5-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dedf5-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dedf5-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dedf5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="dedf5-109">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    prep As JET_prep _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim prep As JET_prep

Dim instance As New Update(sesid, tableid, _
    prep)
```

``` csharp
public Update(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_prep prep
)
```

#### <a name="parameters"></a><span data-ttu-id="dedf5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dedf5-110">Parameters</span></span>

  - <span data-ttu-id="dedf5-111">-sid</span><span class="sxs-lookup"><span data-stu-id="dedf5-111">sesid</span></span>  
    <span data-ttu-id="dedf5-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dedf5-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="dedf5-113">Die Sitzung, für die die Transaktion gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dedf5-113">The session to start the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="dedf5-114">TableID</span><span class="sxs-lookup"><span data-stu-id="dedf5-114">tableid</span></span>  
    <span data-ttu-id="dedf5-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dedf5-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="dedf5-116">Die TableID, für die das Update vorbereitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dedf5-116">The tableid to prepare the update for.</span></span>

<!-- end list -->

  - <span data-ttu-id="dedf5-117">vorzubereiten</span><span class="sxs-lookup"><span data-stu-id="dedf5-117">prep</span></span>  
    <span data-ttu-id="dedf5-118">Typ: [Microsoft.ISAM.ESENT.Interop.JET_prep](./jet-prep-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="dedf5-118">Type: [Microsoft.Isam.Esent.Interop.JET_prep](./jet-prep-enumeration.md)</span></span>  
    
    <span data-ttu-id="dedf5-119">Der Typ des Updates.</span><span class="sxs-lookup"><span data-stu-id="dedf5-119">The type of update.</span></span>

## <a name="see-also"></a><span data-ttu-id="dedf5-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dedf5-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dedf5-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="dedf5-121">Reference</span></span>

[<span data-ttu-id="dedf5-122">Update-Klasse</span><span class="sxs-lookup"><span data-stu-id="dedf5-122">Update class</span></span>](./update-class.md)

[<span data-ttu-id="dedf5-123">Mitglieder aktualisieren</span><span class="sxs-lookup"><span data-stu-id="dedf5-123">Update members</span></span>](./update-members.md)

[<span data-ttu-id="dedf5-124">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="dedf5-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
