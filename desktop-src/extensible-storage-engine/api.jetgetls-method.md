---
description: Weitere Informationen finden Sie in der API. jetgetls-Methode.
title: API. jetgetls-Methode
TOCTitle: 'JetGetLS method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLS(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_LS@,Microsoft.Isam.Esent.Interop.LsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetls(v=EXCHG.10)
ms:contentKeyID: 55100734
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 611f92e21dad83121b4e4a6226838ac9ebce2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214497"
---
# <a name="apijetgetls-method"></a><span data-ttu-id="a32b0-103">API. jetgetls-Methode</span><span class="sxs-lookup"><span data-stu-id="a32b0-103">Api.JetGetLS method</span></span>

<span data-ttu-id="a32b0-104">Ermöglicht der Anwendung das Abrufen des Kontext Handles, das als lokaler Speicher bezeichnet wird, der einem Cursor oder der diesem Cursor zugeordneten Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a32b0-104">Enables the application to retrieve the context handle known as Local Storage that is associated with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="a32b0-105">Dieses Kontext Handle muss zuvor mithilfe von [jetsetls (JET_SESID, JET_TABLEID, JET_LS, lsgrbit)](./api.jetsetls-method.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a32b0-105">This context handle must have been previously set using [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).</span></span> <span data-ttu-id="a32b0-106">Jetgetls kann auch zum gleichzeitigen Abrufen des aktuellen Kontext Handles für einen Cursor oder eine Tabelle und zum Zurücksetzen dieses Kontext Handles verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a32b0-106">JetGetLS can also be used to simultaneously fetch the current context handle for a cursor or table and reset that context handle.</span></span>

<span data-ttu-id="a32b0-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a32b0-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a32b0-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a32b0-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a32b0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a32b0-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLS ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef ls As JET_LS, _
    grbit As LsGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim ls As JET_LS
Dim grbit As LsGrbitApi.JetGetLS(sesid, tableid, ls, _
    grbit)
```

``` csharp
public static void JetGetLS(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_LS ls,
    LsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="a32b0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a32b0-110">Parameters</span></span>

  - <span data-ttu-id="a32b0-111">-sid</span><span class="sxs-lookup"><span data-stu-id="a32b0-111">sesid</span></span>  
    <span data-ttu-id="a32b0-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a32b0-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a32b0-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="a32b0-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a32b0-114">TableID</span><span class="sxs-lookup"><span data-stu-id="a32b0-114">tableid</span></span>  
    <span data-ttu-id="a32b0-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a32b0-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a32b0-116">Der zu verwendende Cursor.</span><span class="sxs-lookup"><span data-stu-id="a32b0-116">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a32b0-117">ls</span><span class="sxs-lookup"><span data-stu-id="a32b0-117">ls</span></span>  
    <span data-ttu-id="a32b0-118">Typ: [Microsoft.ISAM.ESENT.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a32b0-118">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="a32b0-119">Gibt das abgerufene Kontext Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="a32b0-119">Returns the retrieved context handle.</span></span>

<!-- end list -->

  - <span data-ttu-id="a32b0-120">grbit</span><span class="sxs-lookup"><span data-stu-id="a32b0-120">grbit</span></span>  
    <span data-ttu-id="a32b0-121">Typ: [Microsoft. ISAM. ESENT. Interop. lsgrbit](./lsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a32b0-121">Type: [Microsoft.Isam.Esent.Interop.LsGrbit](./lsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="a32b0-122">Abrufen von Optionen.</span><span class="sxs-lookup"><span data-stu-id="a32b0-122">Retrieve options.</span></span>

## <a name="see-also"></a><span data-ttu-id="a32b0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a32b0-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a32b0-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="a32b0-124">Reference</span></span>

[<span data-ttu-id="a32b0-125">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="a32b0-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a32b0-126">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="a32b0-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a32b0-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="a32b0-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
