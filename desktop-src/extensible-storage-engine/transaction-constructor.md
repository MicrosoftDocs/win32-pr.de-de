---
description: 'Weitere Informationen finden Sie hier: transaktionskonstruktor'
title: Transaktionskonstruktor
TOCTitle: 'Transaction constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.transaction(v=EXCHG.10)
ms:contentKeyID: 55104069
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Transaction.Transaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Transaction..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a8c3214ebe3d88ce8b50aff000d64270ec50a6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217232"
---
# <a name="transaction-constructor"></a><span data-ttu-id="3179b-103">Transaktionskonstruktor</span><span class="sxs-lookup"><span data-stu-id="3179b-103">Transaction constructor</span></span>

<span data-ttu-id="3179b-104">Initialisiert eine neue Instanz der Transaction-Klasse.</span><span class="sxs-lookup"><span data-stu-id="3179b-104">Initializes a new instance of the Transaction class.</span></span> <span data-ttu-id="3179b-105">Dadurch wird automatisch eine Transaktion gestartet.</span><span class="sxs-lookup"><span data-stu-id="3179b-105">This automatically begins a transaction.</span></span> <span data-ttu-id="3179b-106">Wenn nicht explizit ein Commit für die Transaktion ausgeführt wird, wird ein Rollback ausgeführt</span><span class="sxs-lookup"><span data-stu-id="3179b-106">The transaction will be rolled back if not explicitly committed.</span></span>

<span data-ttu-id="3179b-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3179b-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3179b-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3179b-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3179b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3179b-109">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESID

Dim instance As New Transaction(sesid)
```

``` csharp
public Transaction(
    JET_SESID sesid
)
```

#### <a name="parameters"></a><span data-ttu-id="3179b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3179b-110">Parameters</span></span>

  - <span data-ttu-id="3179b-111">-sid</span><span class="sxs-lookup"><span data-stu-id="3179b-111">sesid</span></span>  
    <span data-ttu-id="3179b-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3179b-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3179b-113">Die Sitzung, für die die Transaktion gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3179b-113">The session to start the transaction for.</span></span>

## <a name="see-also"></a><span data-ttu-id="3179b-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3179b-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3179b-115">Referenz</span><span class="sxs-lookup"><span data-stu-id="3179b-115">Reference</span></span>

[<span data-ttu-id="3179b-116">Transaktionsklasse</span><span class="sxs-lookup"><span data-stu-id="3179b-116">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="3179b-117">Transaktions Mitglieder</span><span class="sxs-lookup"><span data-stu-id="3179b-117">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="3179b-118">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="3179b-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
