---
description: Weitere Informationen finden Sie in der API. jetterm-Methode.
title: API. jetterm-Methode
TOCTitle: 'JetTerm method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTerm(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetterm(v=EXCHG.10)
ms:contentKeyID: 55100813
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTerm
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTerm
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c8e028ecdc6456521b7aaa671cb4f5199e8751e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218464"
---
# <a name="apijetterm-method"></a><span data-ttu-id="8cfbc-103">API. jetterm-Methode</span><span class="sxs-lookup"><span data-stu-id="8cfbc-103">Api.JetTerm method</span></span>

<span data-ttu-id="8cfbc-104">Beenden Sie eine Instanz, die mit [jetinit (JET_INSTANCE)](./api.jetinit-method.md) oder [jetkreateinstance (JET_INSTANCE, String)](./api.jetcreateinstance-method.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8cfbc-104">Terminate an instance that was created with [JetInit(JET_INSTANCE)](./api.jetinit-method.md) or [JetCreateInstance(JET_INSTANCE, String)](./api.jetcreateinstance-method.md).</span></span>

<span data-ttu-id="8cfbc-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8cfbc-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8cfbc-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8cfbc-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8cfbc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cfbc-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetTerm ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetTerm(instance)
```

``` csharp
public static void JetTerm(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="8cfbc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cfbc-108">Parameters</span></span>

  - <span data-ttu-id="8cfbc-109">instance</span><span class="sxs-lookup"><span data-stu-id="8cfbc-109">instance</span></span>  
    <span data-ttu-id="8cfbc-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8cfbc-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="8cfbc-111">Die Instanz, die beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8cfbc-111">The instance to terminate.</span></span>

## <a name="see-also"></a><span data-ttu-id="8cfbc-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cfbc-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8cfbc-113">Referenz</span><span class="sxs-lookup"><span data-stu-id="8cfbc-113">Reference</span></span>

[<span data-ttu-id="8cfbc-114">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="8cfbc-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8cfbc-115">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="8cfbc-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8cfbc-116">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="8cfbc-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
