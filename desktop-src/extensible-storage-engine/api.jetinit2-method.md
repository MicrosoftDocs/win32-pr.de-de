---
description: Weitere Informationen finden Sie in der API. JetInit2-Methode.
title: API. JetInit2-Methode
TOCTitle: 'JetInit2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetInit2(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetinit2(v=EXCHG.10)
ms:contentKeyID: 55100762
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetInit2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetInit2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 138a9830d5a74b887e7e68f3a3833f5f7e7fb8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363333"
---
# <a name="apijetinit2-method"></a><span data-ttu-id="3bbe0-103">API. JetInit2-Methode</span><span class="sxs-lookup"><span data-stu-id="3bbe0-103">Api.JetInit2 method</span></span>

<span data-ttu-id="3bbe0-104">Initialisieren Sie die ESENT-Datenbank-Engine.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-104">Initialize the ESENT database engine.</span></span>

<span data-ttu-id="3bbe0-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3bbe0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3bbe0-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3bbe0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3bbe0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bbe0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetInit2 ( _
    ByRef instance As JET_INSTANCE, _
    grbit As InitGrbit _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim grbit As InitGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetInit2(instance, _
    grbit)
```

``` csharp
public static JET_wrn JetInit2(
    ref JET_INSTANCE instance,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="3bbe0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bbe0-108">Parameters</span></span>

  - <span data-ttu-id="3bbe0-109">instance</span><span class="sxs-lookup"><span data-stu-id="3bbe0-109">instance</span></span>  
    <span data-ttu-id="3bbe0-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3bbe0-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="3bbe0-111">Die-Instanz, die initialisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-111">The instance to initialize.</span></span> <span data-ttu-id="3bbe0-112">Wenn eine Instanz nicht zugeordnet wurde, wird ein neuer erstellt, und die Engine wird im einzelinstanzmodus betrieben.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-112">If an instance hasn't been allocated then a new one is created and the engine will operate in single-instance mode.</span></span>

<!-- end list -->

  - <span data-ttu-id="3bbe0-113">grbit</span><span class="sxs-lookup"><span data-stu-id="3bbe0-113">grbit</span></span>  
    <span data-ttu-id="3bbe0-114">Type: [Microsoft.Isam.Esent.Interop.Initgrbit](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3bbe0-114">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3bbe0-115">Initialisierungs Optionen.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-115">Initialization options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3bbe0-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3bbe0-116">Return value</span></span>

<span data-ttu-id="3bbe0-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3bbe0-117">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="3bbe0-118">Ein Warnungs Code.</span><span class="sxs-lookup"><span data-stu-id="3bbe0-118">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3bbe0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bbe0-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3bbe0-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="3bbe0-120">Reference</span></span>

[<span data-ttu-id="3bbe0-121">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="3bbe0-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3bbe0-122">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="3bbe0-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3bbe0-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="3bbe0-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
