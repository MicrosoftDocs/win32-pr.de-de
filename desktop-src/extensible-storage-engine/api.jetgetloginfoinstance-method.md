---
description: Weitere Informationen finden Sie in der API. jetgetloginfoinstance-Methode.
title: API. jetgetloginfoinstance-Methode
TOCTitle: 'JetGetLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100726
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85e252b74c47d3274fc83af59e3fb571906219fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344418"
---
# <a name="apijetgetloginfoinstance-method"></a><span data-ttu-id="721e3-103">API. jetgetloginfoinstance-Methode</span><span class="sxs-lookup"><span data-stu-id="721e3-103">Api.JetGetLogInfoInstance method</span></span>

<span data-ttu-id="721e3-104">Wird bei einer von [jetbeginexternalbackupinstance initiierten Sicherung (JET_INSTANCE, beginexternalbackupgrbit)](./api.jetbeginexternalbackupinstance-method.md) verwendet, um eine Instanz für die Namen von datenbankpatchdateien und Protokolldateien abzufragen, die Teil der Sicherungsdatei Gruppe werden sollen.</span><span class="sxs-lookup"><span data-stu-id="721e3-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of database patch files and logfiles that should become part of the backup file set.</span></span> <span data-ttu-id="721e3-105">Diese Dateien können anschließend mit [jetopenfileinstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) geöffnet und mit [jetreadfileinstance (JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32)](./api.jetreadfileinstance-method.md)gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="721e3-105">These files may subsequently be opened using [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) and read using [JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[\], Int32, Int32)](./api.jetreadfileinstance-method.md).</span></span>

<span data-ttu-id="721e3-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="721e3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="721e3-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="721e3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="721e3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="721e3-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetLogInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="721e3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="721e3-109">Parameters</span></span>

  - <span data-ttu-id="721e3-110">instance</span><span class="sxs-lookup"><span data-stu-id="721e3-110">instance</span></span>  
    <span data-ttu-id="721e3-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="721e3-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="721e3-112">Die-Instanz, für die die Informationen zu erhalten sind.</span><span class="sxs-lookup"><span data-stu-id="721e3-112">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="721e3-113">files</span><span class="sxs-lookup"><span data-stu-id="721e3-113">files</span></span>  
    <span data-ttu-id="721e3-114">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="721e3-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="721e3-115">Gibt eine Liste von null-terminierten Zeichen folgen zurück, die den Satz von datenbankpatchdateien und Protokolldateien beschreiben, die Teil des Sicherungsdatei Satzes sein sollen.</span><span class="sxs-lookup"><span data-stu-id="721e3-115">Returns a list of null terminated strings describing the set of database patch files and log files that should be a part of the backup file set.</span></span> <span data-ttu-id="721e3-116">Die Liste der in diesem Puffer zurückgegebenen Zeichen folgen weist das gleiche Format auf wie eine von der Registrierung verwendete Multizeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="721e3-116">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="721e3-117">Jede NULL terminierte Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="721e3-117">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="721e3-118">maxChars</span><span class="sxs-lookup"><span data-stu-id="721e3-118">maxChars</span></span>  
    <span data-ttu-id="721e3-119">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="721e3-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="721e3-120">Maximale Anzahl der abzurufenden Zeichen.</span><span class="sxs-lookup"><span data-stu-id="721e3-120">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="721e3-121">actualchars</span><span class="sxs-lookup"><span data-stu-id="721e3-121">actualChars</span></span>  
    <span data-ttu-id="721e3-122">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="721e3-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="721e3-123">Die tatsächliche Größe der Datei Liste.</span><span class="sxs-lookup"><span data-stu-id="721e3-123">Actual size of the file list.</span></span> <span data-ttu-id="721e3-124">Wenn dieser Wert größer als maxChars ist, wurde die Liste abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="721e3-124">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="721e3-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="721e3-125">Remarks</span></span>

<span data-ttu-id="721e3-126">Beachten Sie, dass diese API keinen Fehler oder keine Warnung zurückgibt, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Bestandteil des Sicherungsdatei Satzes sein sollten.</span><span class="sxs-lookup"><span data-stu-id="721e3-126">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="721e3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="721e3-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="721e3-128">Referenz</span><span class="sxs-lookup"><span data-stu-id="721e3-128">Reference</span></span>

[<span data-ttu-id="721e3-129">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="721e3-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="721e3-130">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="721e3-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="721e3-131">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="721e3-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
