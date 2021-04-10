---
description: Weitere Informationen finden Sie in der API. jetclosetable-Methode.
title: API. jetclosetable-Methode
TOCTitle: 'JetCloseTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCloseTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetclosetable(v=EXCHG.10)
ms:contentKeyID: 55100664
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCloseTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCloseTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fee4ad7d7accf71bd4c3439f954ee36badd2ea20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958811"
---
# <a name="apijetclosetable-method"></a><span data-ttu-id="b8413-103">API. jetclosetable-Methode</span><span class="sxs-lookup"><span data-stu-id="b8413-103">Api.JetCloseTable method</span></span>

<span data-ttu-id="b8413-104">Schließen Sie eine geöffnete Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b8413-104">Close an open table.</span></span>

<span data-ttu-id="b8413-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b8413-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b8413-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b8413-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b8413-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8413-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCloseTable ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetCloseTable(sesid, tableid)
```

``` csharp
public static void JetCloseTable(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="b8413-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8413-108">Parameters</span></span>

  - <span data-ttu-id="b8413-109">-sid</span><span class="sxs-lookup"><span data-stu-id="b8413-109">sesid</span></span>  
    <span data-ttu-id="b8413-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b8413-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b8413-111">Die Sitzung, die die Tabelle geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="b8413-111">The session which opened the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8413-112">TableID</span><span class="sxs-lookup"><span data-stu-id="b8413-112">tableid</span></span>  
    <span data-ttu-id="b8413-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b8413-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b8413-114">Die Tabelle, die geschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8413-114">The table to close.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8413-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8413-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b8413-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="b8413-116">Reference</span></span>

[<span data-ttu-id="b8413-117">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="b8413-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b8413-118">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="b8413-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b8413-119">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="b8413-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
