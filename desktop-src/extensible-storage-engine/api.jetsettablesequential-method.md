---
description: 'Weitere Informationen über: API. jetsettablesequential-Methode'
title: API. jetsettablesequential-Methode
TOCTitle: 'JetSetTableSequential method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetTableSequentialGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsettablesequential(v=EXCHG.10)
ms:contentKeyID: 55100810
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 879eca53c4867bb41ee0a231bff9adce39aa58a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360867"
---
# <a name="apijetsettablesequential-method"></a><span data-ttu-id="69bf5-103">API. jetsettablesequential-Methode</span><span class="sxs-lookup"><span data-stu-id="69bf5-103">Api.JetSetTableSequential method</span></span>

<span data-ttu-id="69bf5-104">Benachrichtigt die Datenbank-Engine, dass die Anwendung den gesamten Index scannt, auf dem sich der Cursor befindet.</span><span class="sxs-lookup"><span data-stu-id="69bf5-104">Notifies the database engine that the application is scanning the entire index that the cursor is positioned on.</span></span> <span data-ttu-id="69bf5-105">Folglich werden die Methoden, die für den Zugriff auf die Indexdaten verwendet werden, optimiert, um dieses Szenario so schnell wie möglich zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="69bf5-105">Consequently, the methods that are used to access the index data will be tuned to make this scenario as fast as possible.</span></span> <span data-ttu-id="69bf5-106">Siehe auch [jetresettablesequential (JET_SESID, JET_TABLEID, resettablesequentialgrbit)](./api.jetresettablesequential-method.md).</span><span class="sxs-lookup"><span data-stu-id="69bf5-106">Also see [JetResetTableSequential(JET_SESID, JET_TABLEID, ResetTableSequentialGrbit)](./api.jetresettablesequential-method.md).</span></span>

<span data-ttu-id="69bf5-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="69bf5-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="69bf5-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="69bf5-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="69bf5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="69bf5-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetTableSequential ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetTableSequentialGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetTableSequentialGrbitApi.JetSetTableSequential(sesid, _
    tableid, grbit)
```

``` csharp
public static void JetSetTableSequential(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetTableSequentialGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="69bf5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="69bf5-110">Parameters</span></span>

  - <span data-ttu-id="69bf5-111">-sid</span><span class="sxs-lookup"><span data-stu-id="69bf5-111">sesid</span></span>  
    <span data-ttu-id="69bf5-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="69bf5-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="69bf5-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="69bf5-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="69bf5-114">TableID</span><span class="sxs-lookup"><span data-stu-id="69bf5-114">tableid</span></span>  
    <span data-ttu-id="69bf5-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="69bf5-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="69bf5-116">Der Cursor, der auf die Daten zugreift.</span><span class="sxs-lookup"><span data-stu-id="69bf5-116">The cursor that will be accessing the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="69bf5-117">grbit</span><span class="sxs-lookup"><span data-stu-id="69bf5-117">grbit</span></span>  
    <span data-ttu-id="69bf5-118">Typ: [Microsoft. ISAM. ESENT. Interop. settablesequentialgrbit](./settablesequentialgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="69bf5-118">Type: [Microsoft.Isam.Esent.Interop.SetTableSequentialGrbit](./settablesequentialgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="69bf5-119">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="69bf5-119">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="69bf5-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69bf5-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="69bf5-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="69bf5-121">Reference</span></span>

[<span data-ttu-id="69bf5-122">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="69bf5-122">Api class</span></span>](./api-class.md)

[<span data-ttu-id="69bf5-123">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="69bf5-123">Api members</span></span>](./api-members.md)

[<span data-ttu-id="69bf5-124">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="69bf5-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
