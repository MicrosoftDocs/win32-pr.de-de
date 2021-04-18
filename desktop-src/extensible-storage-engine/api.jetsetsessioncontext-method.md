---
description: Weitere Informationen finden Sie in der API. jetabzessioncontext-Methode.
title: API. jetabzessioncontext-Methode
TOCTitle: 'JetSetSessionContext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext(Microsoft.Isam.Esent.Interop.JET_SESID,System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsessioncontext(v=EXCHG.10)
ms:contentKeyID: 55100820
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d73a382a2b8e176e2d1ce6fa13585a6b5fa103e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352500"
---
# <a name="apijetsetsessioncontext-method"></a><span data-ttu-id="76f83-103">API. jetabzessioncontext-Methode</span><span class="sxs-lookup"><span data-stu-id="76f83-103">Api.JetSetSessionContext method</span></span>

<span data-ttu-id="76f83-104">Verknüpft eine Sitzung mit dem aktuellen Thread unter Verwendung des angegebenen Kontext Handles.</span><span class="sxs-lookup"><span data-stu-id="76f83-104">Associates a session with the current thread using the given context handle.</span></span> <span data-ttu-id="76f83-105">Diese Zuordnung überschreibt die Standard-Engine-Anforderung, dass eine Transaktion für eine bestimmte Sitzung vollständig im gleichen Thread ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="76f83-105">This association overrides the default engine requirement that a transaction for a given session must occur entirely on the same thread.</span></span> <span data-ttu-id="76f83-106">Verwenden Sie [jetresessioncontext (JET_SESID)](./api.jetresetsessioncontext-method.md) , um die Zuordnung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="76f83-106">Use [JetResetSessionContext(JET_SESID)](./api.jetresetsessioncontext-method.md) to remove the association.</span></span>

<span data-ttu-id="76f83-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="76f83-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="76f83-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="76f83-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="76f83-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="76f83-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetSessionContext ( _
    sesid As JET_SESID, _
    context As IntPtr _
)
'Usage
Dim sesid As JET_SESID
Dim context As IntPtrApi.JetSetSessionContext(sesid, _
    context)
```

``` csharp
public static void JetSetSessionContext(
    JET_SESID sesid,
    IntPtr context
)
```

#### <a name="parameters"></a><span data-ttu-id="76f83-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="76f83-110">Parameters</span></span>

  - <span data-ttu-id="76f83-111">-sid</span><span class="sxs-lookup"><span data-stu-id="76f83-111">sesid</span></span>  
    <span data-ttu-id="76f83-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="76f83-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="76f83-113">Die Sitzung, für die der Kontext festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76f83-113">The session to set the context on.</span></span>

<!-- end list -->

  - <span data-ttu-id="76f83-114">context</span><span class="sxs-lookup"><span data-stu-id="76f83-114">context</span></span>  
    <span data-ttu-id="76f83-115">Typ: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="76f83-115">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="76f83-116">Der festzulegende Kontext.</span><span class="sxs-lookup"><span data-stu-id="76f83-116">The context to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="76f83-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76f83-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="76f83-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="76f83-118">Reference</span></span>

[<span data-ttu-id="76f83-119">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="76f83-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="76f83-120">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="76f83-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="76f83-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="76f83-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
