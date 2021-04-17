---
description: Weitere Informationen finden Sie in der API. JetBeginTransaction2-Methode.
title: API. JetBeginTransaction2-Methode
TOCTitle: 'JetBeginTransaction2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.BeginTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbegintransaction2(v=EXCHG.10)
ms:contentKeyID: 55107226
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8d41652c4688bd736ac5f5164ca9b487a24edf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524771"
---
# <a name="apijetbegintransaction2-method"></a><span data-ttu-id="9da14-103">API. JetBeginTransaction2-Methode</span><span class="sxs-lookup"><span data-stu-id="9da14-103">Api.JetBeginTransaction2 method</span></span>

<span data-ttu-id="9da14-104">Bewirkt, dass eine Sitzung eine Transaktion eingibt oder einen neuen Sicherungspunkt in einer vorhandenen Transaktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="9da14-104">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span>

<span data-ttu-id="9da14-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9da14-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9da14-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9da14-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9da14-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9da14-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginTransaction2 ( _
    sesid As JET_SESID, _
    grbit As BeginTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As BeginTransactionGrbitApi.JetBeginTransaction2(sesid, _
    grbit)
```

``` csharp
public static void JetBeginTransaction2(
    JET_SESID sesid,
    BeginTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="9da14-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9da14-108">Parameters</span></span>

  - <span data-ttu-id="9da14-109">-sid</span><span class="sxs-lookup"><span data-stu-id="9da14-109">sesid</span></span>  
    <span data-ttu-id="9da14-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9da14-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9da14-111">Die Sitzung, für die mit der Transaktion begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9da14-111">The session to begin the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="9da14-112">grbit</span><span class="sxs-lookup"><span data-stu-id="9da14-112">grbit</span></span>  
    <span data-ttu-id="9da14-113">Typ: [Microsoft. ISAM. ESENT. Interop. begintransaktiongrbit](./begintransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9da14-113">Type: [Microsoft.Isam.Esent.Interop.BeginTransactionGrbit](./begintransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="9da14-114">Transaktions Optionen.</span><span class="sxs-lookup"><span data-stu-id="9da14-114">Transaction options.</span></span>

## <a name="see-also"></a><span data-ttu-id="9da14-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9da14-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9da14-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="9da14-116">Reference</span></span>

[<span data-ttu-id="9da14-117">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="9da14-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9da14-118">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="9da14-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9da14-119">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="9da14-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
