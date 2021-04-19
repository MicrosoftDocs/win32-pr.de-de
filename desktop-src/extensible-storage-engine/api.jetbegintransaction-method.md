---
description: Weitere Informationen finden Sie in der API. jetbegintransaction-Methode.
title: API. jetbegintransaction-Methode
TOCTitle: 'JetBeginTransaction method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbegintransaction(v=EXCHG.10)
ms:contentKeyID: 55107225
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b8812df332734ee109ea52820346e433e747751
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348366"
---
# <a name="apijetbegintransaction-method"></a><span data-ttu-id="4b39f-103">API. jetbegintransaction-Methode</span><span class="sxs-lookup"><span data-stu-id="4b39f-103">Api.JetBeginTransaction method</span></span>

<span data-ttu-id="4b39f-104">Bewirkt, dass eine Sitzung eine Transaktion eingibt oder einen neuen Sicherungspunkt in einer vorhandenen Transaktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="4b39f-104">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span>

<span data-ttu-id="4b39f-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4b39f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4b39f-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4b39f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4b39f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b39f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginTransaction ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESIDApi.JetBeginTransaction(sesid)
```

``` csharp
public static void JetBeginTransaction(
    JET_SESID sesid
)
```

#### <a name="parameters"></a><span data-ttu-id="4b39f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b39f-108">Parameters</span></span>

  - <span data-ttu-id="4b39f-109">-sid</span><span class="sxs-lookup"><span data-stu-id="4b39f-109">sesid</span></span>  
    <span data-ttu-id="4b39f-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4b39f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4b39f-111">Die Sitzung, für die mit der Transaktion begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b39f-111">The session to begin the transaction for.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b39f-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b39f-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4b39f-113">Referenz</span><span class="sxs-lookup"><span data-stu-id="4b39f-113">Reference</span></span>

[<span data-ttu-id="4b39f-114">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="4b39f-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4b39f-115">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="4b39f-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4b39f-116">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="4b39f-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
