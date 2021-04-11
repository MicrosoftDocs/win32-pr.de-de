---
description: Weitere Informationen finden Sie in der API. jetbackupinstance-Methode.
title: API. jetbackupinstance-Methode
TOCTitle: 'JetBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.BackupGrbit,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55107221
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73c5b44f1f0b69aaed6066635ad4e82690bc3c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128057"
---
# <a name="apijetbackupinstance-method"></a><span data-ttu-id="28e94-103">API. jetbackupinstance-Methode</span><span class="sxs-lookup"><span data-stu-id="28e94-103">Api.JetBackupInstance method</span></span>

<span data-ttu-id="28e94-104">Führt eine Streamingsicherung einer Instanz, einschließlich aller angefügten Datenbanken, in ein Verzeichnis aus.</span><span class="sxs-lookup"><span data-stu-id="28e94-104">Performs a streaming backup of an instance, including all the attached databases, to a directory.</span></span> <span data-ttu-id="28e94-105">Mit mehreren Sicherungsmethoden, die von der-Engine unterstützt werden, ist dies die einfachste und gekapselte Funktion.</span><span class="sxs-lookup"><span data-stu-id="28e94-105">With multiple backup methods supported by the engine, this is the simplest and most encapsulated function.</span></span>

<span data-ttu-id="28e94-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="28e94-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="28e94-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="28e94-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="28e94-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="28e94-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBackupInstance ( _
    instance As JET_INSTANCE, _
    destination As String, _
    grbit As BackupGrbit, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim destination As String
Dim grbit As BackupGrbit
Dim statusCallback As JET_PFNSTATUSApi.JetBackupInstance(instance, _
    destination, grbit, statusCallback)
```

``` csharp
public static void JetBackupInstance(
    JET_INSTANCE instance,
    string destination,
    BackupGrbit grbit,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="28e94-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="28e94-109">Parameters</span></span>

  - <span data-ttu-id="28e94-110">instance</span><span class="sxs-lookup"><span data-stu-id="28e94-110">instance</span></span>  
    <span data-ttu-id="28e94-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="28e94-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="28e94-112">Die Instanz, die gesichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="28e94-112">The instance to backup.</span></span>

<!-- end list -->

  - <span data-ttu-id="28e94-113">destination</span><span class="sxs-lookup"><span data-stu-id="28e94-113">destination</span></span>  
    <span data-ttu-id="28e94-114">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="28e94-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="28e94-115">Das Verzeichnis, in dem die Sicherung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="28e94-115">The directory where the backup is to be stored.</span></span> <span data-ttu-id="28e94-116">Wenn der Sicherungs Pfad für die Verwendung von NULL ist, schneidet die-Funktion die Protokolle ab, sofern dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="28e94-116">If the backup path is null to use the function will truncate the logs, if possible.</span></span>

<!-- end list -->

  - <span data-ttu-id="28e94-117">grbit</span><span class="sxs-lookup"><span data-stu-id="28e94-117">grbit</span></span>  
    <span data-ttu-id="28e94-118">Typ: [Microsoft. ISAM. ESENT. Interop. backupgrbit](./backupgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="28e94-118">Type: [Microsoft.Isam.Esent.Interop.BackupGrbit](./backupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="28e94-119">Sicherungs Optionen.</span><span class="sxs-lookup"><span data-stu-id="28e94-119">Backup options.</span></span>

<!-- end list -->

  - <span data-ttu-id="28e94-120">Status Rückruf</span><span class="sxs-lookup"><span data-stu-id="28e94-120">statusCallback</span></span>  
    <span data-ttu-id="28e94-121">Typ: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="28e94-121">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="28e94-122">Optionaler Status Benachrichtigungs Rückruf.</span><span class="sxs-lookup"><span data-stu-id="28e94-122">Optional status notification callback.</span></span>

## <a name="see-also"></a><span data-ttu-id="28e94-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28e94-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="28e94-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="28e94-124">Reference</span></span>

[<span data-ttu-id="28e94-125">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="28e94-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="28e94-126">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="28e94-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="28e94-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="28e94-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
