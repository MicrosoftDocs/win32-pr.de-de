---
description: Weitere Informationen finden Sie in der API. jetresettablesequential-Methode.
title: API. jetresettablesequential-Methode
TOCTitle: 'JetResetTableSequential method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ResetTableSequentialGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetresettablesequential(v=EXCHG.10)
ms:contentKeyID: 55100789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b45ca118894015df7cda56201733cdaad9b88d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218274"
---
# <a name="apijetresettablesequential-method"></a><span data-ttu-id="86f39-103">API. jetresettablesequential-Methode</span><span class="sxs-lookup"><span data-stu-id="86f39-103">Api.JetResetTableSequential method</span></span>

<span data-ttu-id="86f39-104">Benachrichtigt die Datenbank-Engine, dass die Anwendung nicht mehr den gesamten Index scannt, auf dem sich der Cursor befindet.</span><span class="sxs-lookup"><span data-stu-id="86f39-104">Notifies the database engine that the application is no longer scanning the entire index the cursor is positioned on.</span></span> <span data-ttu-id="86f39-105">Dieser Rückruf kehrt eine Benachrichtigung um, die von [jetsettablesequential (JET_SESID, JET_TABLEID, settablesequentialgrbit)](./api.jetsettablesequential-method.md)gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="86f39-105">This call reverses a notification sent by [JetSetTableSequential(JET_SESID, JET_TABLEID, SetTableSequentialGrbit)](./api.jetsettablesequential-method.md).</span></span>

<span data-ttu-id="86f39-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="86f39-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="86f39-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="86f39-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="86f39-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="86f39-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetResetTableSequential ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As ResetTableSequentialGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As ResetTableSequentialGrbitApi.JetResetTableSequential(sesid, _
    tableid, grbit)
```

``` csharp
public static void JetResetTableSequential(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ResetTableSequentialGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="86f39-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="86f39-109">Parameters</span></span>

  - <span data-ttu-id="86f39-110">-sid</span><span class="sxs-lookup"><span data-stu-id="86f39-110">sesid</span></span>  
    <span data-ttu-id="86f39-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="86f39-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="86f39-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="86f39-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="86f39-113">TableID</span><span class="sxs-lookup"><span data-stu-id="86f39-113">tableid</span></span>  
    <span data-ttu-id="86f39-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="86f39-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="86f39-115">Der Cursor, der auf die Daten zugegriffen hat.</span><span class="sxs-lookup"><span data-stu-id="86f39-115">The cursor that was accessing the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="86f39-116">grbit</span><span class="sxs-lookup"><span data-stu-id="86f39-116">grbit</span></span>  
    <span data-ttu-id="86f39-117">Typ: [Microsoft. ISAM. ESENT. Interop. resettablesequentialgrbit](./resettablesequentialgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="86f39-117">Type: [Microsoft.Isam.Esent.Interop.ResetTableSequentialGrbit](./resettablesequentialgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="86f39-118">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="86f39-118">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="86f39-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86f39-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="86f39-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="86f39-120">Reference</span></span>

[<span data-ttu-id="86f39-121">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="86f39-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="86f39-122">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="86f39-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="86f39-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="86f39-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
