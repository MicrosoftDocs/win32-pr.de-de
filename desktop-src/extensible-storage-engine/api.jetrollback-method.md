---
description: 'Weitere Informationen finden Sie unter: API. jetrollback-Methode'
title: API. jetrollback-Methode
TOCTitle: 'JetRollback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRollback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrollback(v=EXCHG.10)
ms:contentKeyID: 55100794
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRollback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRollback
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9144bade272ddaea7501be5622c7263268c0f1fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343058"
---
# <a name="apijetrollback-method"></a><span data-ttu-id="35cbd-103">API. jetrollback-Methode</span><span class="sxs-lookup"><span data-stu-id="35cbd-103">Api.JetRollback method</span></span>

<span data-ttu-id="35cbd-104">Macht die am Status der Datenbank vorgenommenen Änderungen rückgängig und kehrt zum letzten Sicherungspunkt zurück.</span><span class="sxs-lookup"><span data-stu-id="35cbd-104">Undoes the changes made to the state of the database and returns to the last save point.</span></span> <span data-ttu-id="35cbd-105">Jetrollback schließt auch alle Cursor, die während des Speicher Punkts geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="35cbd-105">JetRollback will also close any cursors opened during the save point.</span></span> <span data-ttu-id="35cbd-106">Wenn der äußerste Speicherpunkt rückgängig gemacht wird, beendet die Sitzung die Transaktion.</span><span class="sxs-lookup"><span data-stu-id="35cbd-106">If the outermost save point is undone, the session will exit the transaction.</span></span>

<span data-ttu-id="35cbd-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="35cbd-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="35cbd-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="35cbd-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="35cbd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="35cbd-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRollback ( _
    sesid As JET_SESID, _
    grbit As RollbackTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As RollbackTransactionGrbitApi.JetRollback(sesid, grbit)
```

``` csharp
public static void JetRollback(
    JET_SESID sesid,
    RollbackTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="35cbd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="35cbd-110">Parameters</span></span>

  - <span data-ttu-id="35cbd-111">-sid</span><span class="sxs-lookup"><span data-stu-id="35cbd-111">sesid</span></span>  
    <span data-ttu-id="35cbd-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="35cbd-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="35cbd-113">Die Sitzung, für die die Transaktion zurückgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="35cbd-113">The session to rollback the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="35cbd-114">grbit</span><span class="sxs-lookup"><span data-stu-id="35cbd-114">grbit</span></span>  
    <span data-ttu-id="35cbd-115">Typ: [Microsoft. ISAM. ESENT. Interop. rollbacktransaktiongrbit](./rollbacktransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="35cbd-115">Type: [Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit](./rollbacktransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="35cbd-116">Rollback-Optionen.</span><span class="sxs-lookup"><span data-stu-id="35cbd-116">Rollback options.</span></span>

## <a name="see-also"></a><span data-ttu-id="35cbd-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35cbd-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="35cbd-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="35cbd-118">Reference</span></span>

[<span data-ttu-id="35cbd-119">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="35cbd-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="35cbd-120">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="35cbd-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="35cbd-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="35cbd-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
