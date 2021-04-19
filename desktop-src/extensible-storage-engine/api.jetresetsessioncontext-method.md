---
description: Weitere Informationen zur API. jetresessioncontext-Methode
title: API. jetresessioncontext-Methode
TOCTitle: 'JetResetSessionContext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetresetsessioncontext(v=EXCHG.10)
ms:contentKeyID: 55100785
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a34a6c2922c0041f0720b498855b15c4aed23f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353969"
---
# <a name="apijetresetsessioncontext-method"></a><span data-ttu-id="74899-103">API. jetresessioncontext-Methode</span><span class="sxs-lookup"><span data-stu-id="74899-103">Api.JetResetSessionContext method</span></span>

<span data-ttu-id="74899-104">Trennt eine Sitzung vom aktuellen Thread.</span><span class="sxs-lookup"><span data-stu-id="74899-104">Disassociates a session from the current thread.</span></span> <span data-ttu-id="74899-105">Dies sollte in Verbindung mit [jetsetup (JET_SESID, IntPtr)](./api.jetsetsessioncontext-method.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74899-105">This should be used in conjunction with [JetSetSessionContext(JET_SESID, IntPtr)](./api.jetsetsessioncontext-method.md).</span></span>

<span data-ttu-id="74899-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="74899-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="74899-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="74899-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="74899-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="74899-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetResetSessionContext ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESIDApi.JetResetSessionContext(sesid)
```

``` csharp
public static void JetResetSessionContext(
    JET_SESID sesid
)
```

#### <a name="parameters"></a><span data-ttu-id="74899-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="74899-109">Parameters</span></span>

  - <span data-ttu-id="74899-110">-sid</span><span class="sxs-lookup"><span data-stu-id="74899-110">sesid</span></span>  
    <span data-ttu-id="74899-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="74899-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="74899-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="74899-112">The session to use.</span></span>

## <a name="see-also"></a><span data-ttu-id="74899-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74899-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="74899-114">Referenz</span><span class="sxs-lookup"><span data-stu-id="74899-114">Reference</span></span>

[<span data-ttu-id="74899-115">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="74899-115">Api class</span></span>](./api-class.md)

[<span data-ttu-id="74899-116">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="74899-116">Api members</span></span>](./api-members.md)

[<span data-ttu-id="74899-117">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="74899-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
