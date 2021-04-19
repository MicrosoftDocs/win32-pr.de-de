---
description: Weitere Informationen finden Sie in der API. jetfrebuffer-Methode.
title: API. jetfrebuffer-Methode
TOCTitle: 'JetFreeBuffer method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer(System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetfreebuffer(v=EXCHG.10)
ms:contentKeyID: 55100694
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a584caf0f7c59c77e7d3c4a058a03780043e0f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339766"
---
# <a name="apijetfreebuffer-method"></a><span data-ttu-id="f5474-103">API. jetfrebuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="f5474-103">Api.JetFreeBuffer method</span></span>

<span data-ttu-id="f5474-104">Gibt Arbeitsspeicher frei, der durch einen Datenbankmodul-Befehl zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="f5474-104">Frees memory that was allocated by a database engine call.</span></span>

<span data-ttu-id="f5474-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f5474-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f5474-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f5474-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f5474-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5474-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetFreeBuffer ( _
    buffer As IntPtr _
)
'Usage
Dim buffer As IntPtrApi.JetFreeBuffer(buffer)
```

``` csharp
public static void JetFreeBuffer(
    IntPtr buffer
)
```

#### <a name="parameters"></a><span data-ttu-id="f5474-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5474-108">Parameters</span></span>

  - <span data-ttu-id="f5474-109">Puffer</span><span class="sxs-lookup"><span data-stu-id="f5474-109">buffer</span></span>  
    <span data-ttu-id="f5474-110">Typ: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="f5474-110">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="f5474-111">Der Puffer, der durch einen-Aufrufder Datenbank-Engine zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="f5474-111">The buffer allocated by a call to the database engine.</span></span> <span data-ttu-id="f5474-112">[Null](/dotnet/api/system.intptr.zero) ist akzeptabel und wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f5474-112">[Zero](/dotnet/api/system.intptr.zero) is acceptable, and will be ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5474-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5474-113">Remarks</span></span>

<span data-ttu-id="f5474-114">Diese Methode ist intern, weil wir den Aufrufern niemals den von ESENT zugewiesenen Arbeitsspeicher verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="f5474-114">This method is internal because we never expose the memory allocated by ESENT to our callers.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5474-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5474-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f5474-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="f5474-116">Reference</span></span>

[<span data-ttu-id="f5474-117">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="f5474-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f5474-118">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="f5474-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f5474-119">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f5474-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
