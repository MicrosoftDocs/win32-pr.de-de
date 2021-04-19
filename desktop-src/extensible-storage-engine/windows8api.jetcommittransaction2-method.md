---
description: 'Weitere Informationen über: Windows8Api. JetCommitTransaction2-Methode'
title: Windows8Api. JetCommitTransaction2-Methode (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetCommitTransaction2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.CommitTransactionGrbit,System.TimeSpan,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcommittransaction2(v=EXCHG.10)
ms:contentKeyID: 55104454
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80ddc0670b60a3f2a280ff2aca3f051242c453ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360114"
---
# <a name="windows8apijetcommittransaction2-method"></a><span data-ttu-id="c88ff-103">Windows8Api. JetCommitTransaction2-Methode</span><span class="sxs-lookup"><span data-stu-id="c88ff-103">Windows8Api.JetCommitTransaction2 method</span></span>

<span data-ttu-id="c88ff-104">Führt einen Commit für die Änderungen aus, die an den Zustand der Datenbank während des aktuellen Speicher Punkts vorgenommen werden, und migriert Sie zum vorherigen Sicherungspunkt.</span><span class="sxs-lookup"><span data-stu-id="c88ff-104">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="c88ff-105">Wenn für den äußersten Speicherpunkt ein Commit ausgeführt wird, werden die während dieses Speicher Punkts vorgenommenen Änderungen in den Zustand der Datenbank übertragen, und die Sitzung wird beendet.</span><span class="sxs-lookup"><span data-stu-id="c88ff-105">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="c88ff-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c88ff-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="c88ff-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c88ff-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c88ff-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c88ff-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCommitTransaction2 ( _
    sesid As JET_SESID, _
    grbit As CommitTransactionGrbit, _
    durableCommit As TimeSpan, _
    <OutAttribute> ByRef commitId As JET_COMMIT_ID _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As CommitTransactionGrbit
Dim durableCommit As TimeSpan
Dim commitId As JET_COMMIT_IDWindows8Api.JetCommitTransaction2(sesid, _
    grbit, durableCommit, commitId)
```

``` csharp
public static void JetCommitTransaction2(
    JET_SESID sesid,
    CommitTransactionGrbit grbit,
    TimeSpan durableCommit,
    out JET_COMMIT_ID commitId
)
```

#### <a name="parameters"></a><span data-ttu-id="c88ff-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c88ff-109">Parameters</span></span>

  - <span data-ttu-id="c88ff-110">-sid</span><span class="sxs-lookup"><span data-stu-id="c88ff-110">sesid</span></span>  
    <span data-ttu-id="c88ff-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c88ff-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c88ff-112">Die Sitzung, für die die Transaktion übernommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c88ff-112">The session to commit the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="c88ff-113">grbit</span><span class="sxs-lookup"><span data-stu-id="c88ff-113">grbit</span></span>  
    <span data-ttu-id="c88ff-114">Typ: [Microsoft. ISAM. ESENT. Interop. committransaktiongrbit](./committransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c88ff-114">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c88ff-115">Commit-Optionen.</span><span class="sxs-lookup"><span data-stu-id="c88ff-115">Commit options.</span></span>

<!-- end list -->

  - <span data-ttu-id="c88ff-116">durablecommit</span><span class="sxs-lookup"><span data-stu-id="c88ff-116">durableCommit</span></span>  
    <span data-ttu-id="c88ff-117">Typ: [System. TimeSpan](/dotnet/api/system.timespan)</span><span class="sxs-lookup"><span data-stu-id="c88ff-117">Type: [System.TimeSpan](/dotnet/api/system.timespan)</span></span>  
    
    <span data-ttu-id="c88ff-118">Dauer für den Commit einer verzögerten Transaktion.</span><span class="sxs-lookup"><span data-stu-id="c88ff-118">Duration to commit lazy transaction.</span></span>

<!-- end list -->

  - <span data-ttu-id="c88ff-119">commitId</span><span class="sxs-lookup"><span data-stu-id="c88ff-119">commitId</span></span>  
    <span data-ttu-id="c88ff-120">Typ: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="c88ff-120">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="c88ff-121">Commit-ID, die diesem Commitdatensatz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c88ff-121">Commit-id associated with this commit record.</span></span>

## <a name="see-also"></a><span data-ttu-id="c88ff-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c88ff-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c88ff-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="c88ff-123">Reference</span></span>

[<span data-ttu-id="c88ff-124">Windows8Api-Klasse</span><span class="sxs-lookup"><span data-stu-id="c88ff-124">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="c88ff-125">Windows8Api-Member</span><span class="sxs-lookup"><span data-stu-id="c88ff-125">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="c88ff-126">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="c88ff-126">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
