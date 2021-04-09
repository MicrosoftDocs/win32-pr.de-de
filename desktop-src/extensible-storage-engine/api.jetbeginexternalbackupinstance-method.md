---
description: Weitere Informationen finden Sie in der API. jetbeginexternalbackupinstance-Methode.
title: API. jetbeginexternalbackupinstance-Methode
TOCTitle: 'JetBeginExternalBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbeginexternalbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55100659
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c42f5d1f62de0af7582247fb47d407f82981a42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958813"
---
# <a name="apijetbeginexternalbackupinstance-method"></a><span data-ttu-id="7182c-103">API. jetbeginexternalbackupinstance-Methode</span><span class="sxs-lookup"><span data-stu-id="7182c-103">Api.JetBeginExternalBackupInstance method</span></span>

<span data-ttu-id="7182c-104">Initiiert eine externe Sicherung, während die-Engine und die-Datenbank online und aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="7182c-104">Initiates an external backup while the engine and database are online and active.</span></span>

<span data-ttu-id="7182c-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7182c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7182c-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7182c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7182c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7182c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginExternalBackupInstance ( _
    instance As JET_INSTANCE, _
    grbit As BeginExternalBackupGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As BeginExternalBackupGrbitApi.JetBeginExternalBackupInstance(instance, _
    grbit)
```

``` csharp
public static void JetBeginExternalBackupInstance(
    JET_INSTANCE instance,
    BeginExternalBackupGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="7182c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7182c-108">Parameters</span></span>

  - <span data-ttu-id="7182c-109">instance</span><span class="sxs-lookup"><span data-stu-id="7182c-109">instance</span></span>  
    <span data-ttu-id="7182c-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7182c-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="7182c-111">Die-Instanz bereitet eine Sicherung vor.</span><span class="sxs-lookup"><span data-stu-id="7182c-111">The instance prepare for backup.</span></span>

<!-- end list -->

  - <span data-ttu-id="7182c-112">grbit</span><span class="sxs-lookup"><span data-stu-id="7182c-112">grbit</span></span>  
    <span data-ttu-id="7182c-113">Typ: [Microsoft. ISAM. ESENT. Interop. beginexternalbackupgrbit](./beginexternalbackupgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7182c-113">Type: [Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit](./beginexternalbackupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7182c-114">Sicherungs Optionen.</span><span class="sxs-lookup"><span data-stu-id="7182c-114">Backup options.</span></span>

## <a name="see-also"></a><span data-ttu-id="7182c-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7182c-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7182c-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="7182c-116">Reference</span></span>

[<span data-ttu-id="7182c-117">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="7182c-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7182c-118">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="7182c-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7182c-119">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="7182c-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
