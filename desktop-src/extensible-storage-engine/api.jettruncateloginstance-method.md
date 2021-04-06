---
description: 'Weitere Informationen finden Sie hier: API. jettruneureloginstance-Methode'
title: API. jettruneureloginstance-Methode
TOCTitle: 'JetTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jettruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55100815
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc1693b3f84cd594bfeca81a8e854e49e28d955f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960788"
---
# <a name="apijettruncateloginstance-method"></a><span data-ttu-id="a17ca-103">API. jettruneureloginstance-Methode</span><span class="sxs-lookup"><span data-stu-id="a17ca-103">Api.JetTruncateLogInstance method</span></span>

<span data-ttu-id="a17ca-104">Wird bei einer von jetbeginexternalbackup initiierten Sicherung verwendet, um Transaktionsprotokoll Dateien zu löschen, die nicht mehr benötigt werden, nachdem die aktuelle Sicherung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a17ca-104">Used during a backup initiated by JetBeginExternalBackup to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

<span data-ttu-id="a17ca-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a17ca-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a17ca-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a17ca-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a17ca-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a17ca-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetTruncateLogInstance ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetTruncateLogInstance(instance)
```

``` csharp
public static void JetTruncateLogInstance(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="a17ca-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a17ca-108">Parameters</span></span>

  - <span data-ttu-id="a17ca-109">instance</span><span class="sxs-lookup"><span data-stu-id="a17ca-109">instance</span></span>  
    <span data-ttu-id="a17ca-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a17ca-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="a17ca-111">Die-Instanz, die abgeschnitten werden soll.</span><span class="sxs-lookup"><span data-stu-id="a17ca-111">The instance to truncate.</span></span>

## <a name="see-also"></a><span data-ttu-id="a17ca-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a17ca-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a17ca-113">Referenz</span><span class="sxs-lookup"><span data-stu-id="a17ca-113">Reference</span></span>

[<span data-ttu-id="a17ca-114">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="a17ca-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a17ca-115">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="a17ca-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a17ca-116">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="a17ca-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
