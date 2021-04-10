---
description: Weitere Informationen finden Sie in der API. JetEndExternalBackupInstance2-Methode.
title: API. JetEndExternalBackupInstance2-Methode
TOCTitle: 'JetEndExternalBackupInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendexternalbackupinstance2(v=EXCHG.10)
ms:contentKeyID: 55100692
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 71a405c5e0ba3a398071cc317e0d42dd98c4953d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214505"
---
# <a name="apijetendexternalbackupinstance2-method"></a><span data-ttu-id="86cc0-103">API. JetEndExternalBackupInstance2-Methode</span><span class="sxs-lookup"><span data-stu-id="86cc0-103">Api.JetEndExternalBackupInstance2 method</span></span>

<span data-ttu-id="86cc0-104">Beendet eine externe Sicherungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="86cc0-104">Ends an external backup session.</span></span> <span data-ttu-id="86cc0-105">Diese API ist die letzte API in einer Reihe von APIs, die aufgerufen werden muss, um eine erfolgreiche (nicht auf VSS basierende) Online Sicherung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="86cc0-105">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="86cc0-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="86cc0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="86cc0-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="86cc0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="86cc0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="86cc0-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndExternalBackupInstance2 ( _
    instance As JET_INSTANCE, _
    grbit As EndExternalBackupGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As EndExternalBackupGrbitApi.JetEndExternalBackupInstance2(instance, _
    grbit)
```

``` csharp
public static void JetEndExternalBackupInstance2(
    JET_INSTANCE instance,
    EndExternalBackupGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="86cc0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="86cc0-109">Parameters</span></span>

  - <span data-ttu-id="86cc0-110">instance</span><span class="sxs-lookup"><span data-stu-id="86cc0-110">instance</span></span>  
    <span data-ttu-id="86cc0-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="86cc0-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="86cc0-112">Die-Instanz, für die die Sicherung beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="86cc0-112">The instance to end the backup for.</span></span>

<!-- end list -->

  - <span data-ttu-id="86cc0-113">grbit</span><span class="sxs-lookup"><span data-stu-id="86cc0-113">grbit</span></span>  
    <span data-ttu-id="86cc0-114">Typ: [Microsoft. ISAM. ESENT. Interop. endexternalbackupgrbit](./endexternalbackupgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="86cc0-114">Type: [Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit](./endexternalbackupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="86cc0-115">Optionen, die angeben, wie die Sicherung beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="86cc0-115">Options that specify how the backup ended.</span></span>

## <a name="see-also"></a><span data-ttu-id="86cc0-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86cc0-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="86cc0-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="86cc0-117">Reference</span></span>

[<span data-ttu-id="86cc0-118">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="86cc0-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="86cc0-119">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="86cc0-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="86cc0-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="86cc0-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
