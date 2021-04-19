---
description: Weitere Informationen finden Sie in der API. jetcommittransaction-Methode.
title: API. jetcommittransaction-Methode
TOCTitle: 'JetCommitTransaction method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.CommitTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcommittransaction(v=EXCHG.10)
ms:contentKeyID: 55100665
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edf0799af53c3da422f92f981f7a28ee7a283d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341165"
---
# <a name="apijetcommittransaction-method"></a><span data-ttu-id="80c82-103">API. jetcommittransaction-Methode</span><span class="sxs-lookup"><span data-stu-id="80c82-103">Api.JetCommitTransaction method</span></span>

<span data-ttu-id="80c82-104">Führt einen Commit für die Änderungen aus, die an den Zustand der Datenbank während des aktuellen Speicher Punkts vorgenommen werden, und migriert Sie zum vorherigen Sicherungspunkt.</span><span class="sxs-lookup"><span data-stu-id="80c82-104">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="80c82-105">Wenn für den äußersten Speicherpunkt ein Commit ausgeführt wird, werden die während dieses Speicher Punkts vorgenommenen Änderungen in den Zustand der Datenbank übertragen, und die Sitzung wird beendet.</span><span class="sxs-lookup"><span data-stu-id="80c82-105">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="80c82-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="80c82-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="80c82-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="80c82-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="80c82-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="80c82-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCommitTransaction ( _
    sesid As JET_SESID, _
    grbit As CommitTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As CommitTransactionGrbitApi.JetCommitTransaction(sesid, _
    grbit)
```

``` csharp
public static void JetCommitTransaction(
    JET_SESID sesid,
    CommitTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="80c82-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="80c82-109">Parameters</span></span>

  - <span data-ttu-id="80c82-110">-sid</span><span class="sxs-lookup"><span data-stu-id="80c82-110">sesid</span></span>  
    <span data-ttu-id="80c82-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="80c82-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="80c82-112">Die Sitzung, für die die Transaktion übernommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="80c82-112">The session to commit the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="80c82-113">grbit</span><span class="sxs-lookup"><span data-stu-id="80c82-113">grbit</span></span>  
    <span data-ttu-id="80c82-114">Typ: [Microsoft. ISAM. ESENT. Interop. committransaktiongrbit](./committransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="80c82-114">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="80c82-115">Commit-Optionen.</span><span class="sxs-lookup"><span data-stu-id="80c82-115">Commit options.</span></span>

## <a name="see-also"></a><span data-ttu-id="80c82-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80c82-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="80c82-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="80c82-117">Reference</span></span>

[<span data-ttu-id="80c82-118">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="80c82-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="80c82-119">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="80c82-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="80c82-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="80c82-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
