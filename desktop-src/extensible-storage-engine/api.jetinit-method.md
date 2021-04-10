---
description: 'Weitere Informationen finden Sie hier: API. jetinit-Methode'
title: API. jetinit-Methode
TOCTitle: 'JetInit method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetInit(Microsoft.Isam.Esent.Interop.JET_INSTANCE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetinit(v=EXCHG.10)
ms:contentKeyID: 55100760
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetInit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetInit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27b0ad5fa640b853b46cd39ae595a1f486812adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868739"
---
# <a name="apijetinit-method"></a><span data-ttu-id="2934e-103">API. jetinit-Methode</span><span class="sxs-lookup"><span data-stu-id="2934e-103">Api.JetInit method</span></span>

<span data-ttu-id="2934e-104">Initialisieren Sie die ESENT-Datenbank-Engine.</span><span class="sxs-lookup"><span data-stu-id="2934e-104">Initialize the ESENT database engine.</span></span>

<span data-ttu-id="2934e-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2934e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2934e-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2934e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2934e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2934e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetInit ( _
    ByRef instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetInit(instance)
```

``` csharp
public static void JetInit(
    ref JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="2934e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2934e-108">Parameters</span></span>

  - <span data-ttu-id="2934e-109">instance</span><span class="sxs-lookup"><span data-stu-id="2934e-109">instance</span></span>  
    <span data-ttu-id="2934e-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2934e-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="2934e-111">Die-Instanz, die initialisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2934e-111">The instance to initialize.</span></span> <span data-ttu-id="2934e-112">Wenn eine Instanz nicht zugeordnet wurde, wird ein neuer erstellt, und die Engine wird im einzelinstanzmodus betrieben.</span><span class="sxs-lookup"><span data-stu-id="2934e-112">If an instance hasn't been allocated then a new one is created and the engine will operate in single-instance mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="2934e-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2934e-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2934e-114">Referenz</span><span class="sxs-lookup"><span data-stu-id="2934e-114">Reference</span></span>

[<span data-ttu-id="2934e-115">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="2934e-115">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2934e-116">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="2934e-116">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2934e-117">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="2934e-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
