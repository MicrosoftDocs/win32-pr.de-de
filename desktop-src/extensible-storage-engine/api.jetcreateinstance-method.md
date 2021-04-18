---
description: Weitere Informationen finden Sie in der API. jetkreateinzustance-Methode.
title: API. jetkreateinzustance-Methode
TOCTitle: 'JetCreateInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateinstance(v=EXCHG.10)
ms:contentKeyID: 55100672
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e865c443d4f19b14a955204840355ee73be8773
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347129"
---
# <a name="apijetcreateinstance-method"></a><span data-ttu-id="413e5-103">API. jetkreateinzustance-Methode</span><span class="sxs-lookup"><span data-stu-id="413e5-103">Api.JetCreateInstance method</span></span>

<span data-ttu-id="413e5-104">Ordnet eine neue Instanz der Datenbank-Engine zu.</span><span class="sxs-lookup"><span data-stu-id="413e5-104">Allocates a new instance of the database engine.</span></span>

<span data-ttu-id="413e5-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="413e5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="413e5-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="413e5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="413e5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="413e5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateInstance ( _
    <OutAttribute> ByRef instance As JET_INSTANCE, _
    name As String _
)
'Usage
Dim instance As JET_INSTANCE
Dim name As StringApi.JetCreateInstance(instance, _
    name)
```

``` csharp
public static void JetCreateInstance(
    out JET_INSTANCE instance,
    string name
)
```

#### <a name="parameters"></a><span data-ttu-id="413e5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="413e5-108">Parameters</span></span>

  - <span data-ttu-id="413e5-109">instance</span><span class="sxs-lookup"><span data-stu-id="413e5-109">instance</span></span>  
    <span data-ttu-id="413e5-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="413e5-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="413e5-111">Gibt die neue-Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="413e5-111">Returns the new instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="413e5-112">name</span><span class="sxs-lookup"><span data-stu-id="413e5-112">name</span></span>  
    <span data-ttu-id="413e5-113">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="413e5-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="413e5-114">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="413e5-114">The name of the instance.</span></span> <span data-ttu-id="413e5-115">Die Namen müssen eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="413e5-115">Names must be unique.</span></span>

## <a name="see-also"></a><span data-ttu-id="413e5-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="413e5-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="413e5-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="413e5-117">Reference</span></span>

[<span data-ttu-id="413e5-118">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="413e5-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="413e5-119">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="413e5-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="413e5-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="413e5-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
