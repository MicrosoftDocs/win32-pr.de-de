---
description: Weitere Informationen finden Sie in der API. jetgetattachinfoinstance-Methode.
title: API. jetgetattachinfoinstance-Methode
TOCTitle: 'JetGetAttachInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetattachinfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100704
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94865042edf8b049b7140673a8aee1b4e2d91573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348967"
---
# <a name="apijetgetattachinfoinstance-method"></a><span data-ttu-id="cceca-103">API. jetgetattachinfoinstance-Methode</span><span class="sxs-lookup"><span data-stu-id="cceca-103">Api.JetGetAttachInfoInstance method</span></span>

<span data-ttu-id="cceca-104">Wird bei einer von [jetbeginexternalbackupinstance initiierten Sicherung (JET_INSTANCE beginexternalbackupgrbit)](./api.jetbeginexternalbackupinstance-method.md) verwendet, um eine Instanz nach den Namen von Datenbankdateien abzufragen, die Teil des Sicherungsdatei Satzes werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cceca-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="cceca-105">Nur Datenbanken, die zurzeit an die Instanz mit [jetattachdatabase (JET_SESID, String, attachdatabasegrbit)](./api.jetattachdatabase-method.md) angefügt sind, werden berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="cceca-105">Only databases that are currently attached to the instance using [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) will be considered.</span></span> <span data-ttu-id="cceca-106">Diese Dateien können anschließend mit [jetopenfileinstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) geöffnet und mit [jetreadfileinstance (JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32)](./api.jetreadfileinstance-method.md)gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="cceca-106">These files may subsequently be opened using [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) and read using [JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[\], Int32, Int32)](./api.jetreadfileinstance-method.md).</span></span>

<span data-ttu-id="cceca-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cceca-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cceca-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cceca-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cceca-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cceca-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetAttachInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetAttachInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetAttachInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="cceca-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cceca-110">Parameters</span></span>

  - <span data-ttu-id="cceca-111">instance</span><span class="sxs-lookup"><span data-stu-id="cceca-111">instance</span></span>  
    <span data-ttu-id="cceca-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cceca-112">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="cceca-113">Die-Instanz, für die die Informationen zu erhalten sind.</span><span class="sxs-lookup"><span data-stu-id="cceca-113">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="cceca-114">files</span><span class="sxs-lookup"><span data-stu-id="cceca-114">files</span></span>  
    <span data-ttu-id="cceca-115">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="cceca-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="cceca-116">Gibt eine Liste von null-terminierten Zeichen folgen zurück, die den Satz von Datenbankdateien beschreiben, die Teil des Sicherungsdatei Satzes sein sollen.</span><span class="sxs-lookup"><span data-stu-id="cceca-116">Returns a list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="cceca-117">Die Liste der in diesem Puffer zurückgegebenen Zeichen folgen weist das gleiche Format auf wie eine von der Registrierung verwendete Multizeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cceca-117">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="cceca-118">Jede NULL terminierte Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="cceca-118">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="cceca-119">maxChars</span><span class="sxs-lookup"><span data-stu-id="cceca-119">maxChars</span></span>  
    <span data-ttu-id="cceca-120">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="cceca-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="cceca-121">Maximale Anzahl der abzurufenden Zeichen.</span><span class="sxs-lookup"><span data-stu-id="cceca-121">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="cceca-122">actualchars</span><span class="sxs-lookup"><span data-stu-id="cceca-122">actualChars</span></span>  
    <span data-ttu-id="cceca-123">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="cceca-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="cceca-124">Die tatsächliche Größe der Datei Liste.</span><span class="sxs-lookup"><span data-stu-id="cceca-124">Actual size of the file list.</span></span> <span data-ttu-id="cceca-125">Wenn dieser Wert größer als maxChars ist, wurde die Liste abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="cceca-125">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="cceca-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cceca-126">Remarks</span></span>

<span data-ttu-id="cceca-127">Beachten Sie, dass diese API keinen Fehler oder keine Warnung zurückgibt, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Bestandteil des Sicherungsdatei Satzes sein sollten.</span><span class="sxs-lookup"><span data-stu-id="cceca-127">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="cceca-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cceca-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cceca-129">Referenz</span><span class="sxs-lookup"><span data-stu-id="cceca-129">Reference</span></span>

[<span data-ttu-id="cceca-130">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="cceca-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="cceca-131">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="cceca-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="cceca-132">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="cceca-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
