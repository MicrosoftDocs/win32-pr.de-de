---
description: Weitere Informationen finden Sie in der API. jetrestorerstance-Methode.
title: API. jetrestoreingestance-Methode
TOCTitle: 'JetRestoreInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrestoreinstance(v=EXCHG.10)
ms:contentKeyID: 55100787
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e2c2976eb8bf661dc53bdc86723bb21309ab973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346706"
---
# <a name="apijetrestoreinstance-method"></a><span data-ttu-id="08e89-103">API. jetrestoreingestance-Methode</span><span class="sxs-lookup"><span data-stu-id="08e89-103">Api.JetRestoreInstance method</span></span>

<span data-ttu-id="08e89-104">Stellt eine Streamingsicherung einer Instanz, einschließlich aller angefügten Datenbanken, wieder her.</span><span class="sxs-lookup"><span data-stu-id="08e89-104">Restores and recovers a streaming backup of an instance including all the attached databases.</span></span> <span data-ttu-id="08e89-105">Es ist für die Arbeit mit einer Sicherung konzipiert, die mit der [jetbackupinstance (JET_INSTANCE, String, backupgrbit JET_PFNSTATUS)](./api.jetbackupinstance-method.md) -Funktion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="08e89-105">It is designed to work with a backup created with the [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md) function.</span></span> <span data-ttu-id="08e89-106">Dies ist die einfachste und gekapselte Restore-Funktion.</span><span class="sxs-lookup"><span data-stu-id="08e89-106">This is the simplest and most encapsulated restore function.</span></span>

<span data-ttu-id="08e89-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="08e89-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="08e89-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="08e89-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="08e89-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="08e89-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRestoreInstance ( _
    instance As JET_INSTANCE, _
    source As String, _
    destination As String, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim source As String
Dim destination As String
Dim statusCallback As JET_PFNSTATUSApi.JetRestoreInstance(instance, _
    source, destination, statusCallback)
```

``` csharp
public static void JetRestoreInstance(
    JET_INSTANCE instance,
    string source,
    string destination,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="08e89-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="08e89-110">Parameters</span></span>

  - <span data-ttu-id="08e89-111">instance</span><span class="sxs-lookup"><span data-stu-id="08e89-111">instance</span></span>  
    <span data-ttu-id="08e89-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="08e89-112">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="08e89-113">Die zu verwendende-Instanz.</span><span class="sxs-lookup"><span data-stu-id="08e89-113">The instance to use.</span></span> <span data-ttu-id="08e89-114">Die Instanz sollte nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="08e89-114">The instance should not be initialized.</span></span> <span data-ttu-id="08e89-115">Durch das Wiederherstellen der Dateien wird die Instanz initialisiert.</span><span class="sxs-lookup"><span data-stu-id="08e89-115">Restoring the files will initialize the instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="08e89-116">source</span><span class="sxs-lookup"><span data-stu-id="08e89-116">source</span></span>  
    <span data-ttu-id="08e89-117">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="08e89-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="08e89-118">Speicherort der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="08e89-118">Location of the backup.</span></span> <span data-ttu-id="08e89-119">Die Sicherung sollte mit [jetbackupinstance (JET_INSTANCE, String, backupgrbit JET_PFNSTATUS)](./api.jetbackupinstance-method.md)erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="08e89-119">The backup should have been created with [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span></span>

<!-- end list -->

  - <span data-ttu-id="08e89-120">destination</span><span class="sxs-lookup"><span data-stu-id="08e89-120">destination</span></span>  
    <span data-ttu-id="08e89-121">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="08e89-121">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="08e89-122">Der Name des Ordners, in den die Datenbankdateien aus dem Sicherungs Satz kopiert und wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="08e89-122">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="08e89-123">Wenn dieser Wert auf NULL festgelegt ist, werden die Datenbankdateien kopiert und an Ihrem ursprünglichen Speicherort wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="08e89-123">If this is set to null, the database files will be copied and recovered to their original location.</span></span>

<!-- end list -->

  - <span data-ttu-id="08e89-124">Status Rückruf</span><span class="sxs-lookup"><span data-stu-id="08e89-124">statusCallback</span></span>  
    <span data-ttu-id="08e89-125">Typ: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="08e89-125">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="08e89-126">Optionaler Status Benachrichtigungs Rückruf.</span><span class="sxs-lookup"><span data-stu-id="08e89-126">Optional status notification callback.</span></span>

## <a name="see-also"></a><span data-ttu-id="08e89-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08e89-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="08e89-128">Referenz</span><span class="sxs-lookup"><span data-stu-id="08e89-128">Reference</span></span>

[<span data-ttu-id="08e89-129">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="08e89-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="08e89-130">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="08e89-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="08e89-131">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="08e89-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
