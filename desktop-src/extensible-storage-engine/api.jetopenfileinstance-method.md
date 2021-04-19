---
description: 'Weitere Informationen finden Sie hier: API. jetoperfileinstance-Methode'
title: API. jetopdenfileinstance-Methode
TOCTitle: 'JetOpenFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.JET_HANDLE@,System.Int64@,System.Int64@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopenfileinstance(v=EXCHG.10)
ms:contentKeyID: 55100767
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b58b3a426fd2eb7e33cce1f5f539418bcc993ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369850"
---
# <a name="apijetopenfileinstance-method"></a><span data-ttu-id="5599e-103">API. jetopdenfileinstance-Methode</span><span class="sxs-lookup"><span data-stu-id="5599e-103">Api.JetOpenFileInstance method</span></span>

<span data-ttu-id="5599e-104">Öffnet eine angefügte Datenbank, datenbankpatchdatei oder Transaktionsprotokoll Datei einer aktiven Instanz zum Ausführen einer Streaming-Fuzzy-Sicherung.</span><span class="sxs-lookup"><span data-stu-id="5599e-104">Opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="5599e-105">Die Daten aus diesen Dateien können anschließend mithilfe von jetreadfileinstance durch das zurückgegebene Handle gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="5599e-105">The data from these files can subsequently be read through the returned handle using JetReadFileInstance.</span></span> <span data-ttu-id="5599e-106">Das zurückgegebene Handle muss mithilfe von jetclosefilinput Stance geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="5599e-106">The returned handle must be closed using JetCloseFileInstance.</span></span> <span data-ttu-id="5599e-107">Eine externe Sicherung der Instanz muss mithilfe von jetbeginexternalbackupinstance initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="5599e-107">An external backup of the instance must have been previously initiated using JetBeginExternalBackupInstance.</span></span>

<span data-ttu-id="5599e-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5599e-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5599e-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5599e-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5599e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5599e-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenFileInstance ( _
    instance As JET_INSTANCE, _
    file As String, _
    <OutAttribute> ByRef handle As JET_HANDLE, _
    <OutAttribute> ByRef fileSizeLow As Long, _
    <OutAttribute> ByRef fileSizeHigh As Long _
)
'Usage
Dim instance As JET_INSTANCE
Dim file As String
Dim handle As JET_HANDLE
Dim fileSizeLow As Long
Dim fileSizeHigh As LongApi.JetOpenFileInstance(instance, _
    file, handle, fileSizeLow, fileSizeHigh)
```

``` csharp
public static void JetOpenFileInstance(
    JET_INSTANCE instance,
    string file,
    out JET_HANDLE handle,
    out long fileSizeLow,
    out long fileSizeHigh
)
```

#### <a name="parameters"></a><span data-ttu-id="5599e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5599e-111">Parameters</span></span>

  - <span data-ttu-id="5599e-112">instance</span><span class="sxs-lookup"><span data-stu-id="5599e-112">instance</span></span>  
    <span data-ttu-id="5599e-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5599e-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="5599e-114">Die zu verwendende-Instanz.</span><span class="sxs-lookup"><span data-stu-id="5599e-114">The instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5599e-115">file</span><span class="sxs-lookup"><span data-stu-id="5599e-115">file</span></span>  
    <span data-ttu-id="5599e-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5599e-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5599e-117">Die zu öffnende Datei.</span><span class="sxs-lookup"><span data-stu-id="5599e-117">The file to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="5599e-118">Handlebezeichner</span><span class="sxs-lookup"><span data-stu-id="5599e-118">handle</span></span>  
    <span data-ttu-id="5599e-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5599e-119">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="5599e-120">Gibt ein Handle für die Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="5599e-120">Returns a handle to the file.</span></span>

<!-- end list -->

  - <span data-ttu-id="5599e-121">filesizelow</span><span class="sxs-lookup"><span data-stu-id="5599e-121">fileSizeLow</span></span>  
    <span data-ttu-id="5599e-122">Typ: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="5599e-122">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="5599e-123">Gibt die am wenigsten signifikanten 32 Bits der Dateigröße zurück.</span><span class="sxs-lookup"><span data-stu-id="5599e-123">Returns the least significant 32 bits of the file size.</span></span>

<!-- end list -->

  - <span data-ttu-id="5599e-124">filesizehigh</span><span class="sxs-lookup"><span data-stu-id="5599e-124">fileSizeHigh</span></span>  
    <span data-ttu-id="5599e-125">Typ: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="5599e-125">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="5599e-126">Gibt die signifikantesten 32 Bits der Dateigröße zurück.</span><span class="sxs-lookup"><span data-stu-id="5599e-126">Returns the most significant 32 bits of the file size.</span></span>

## <a name="see-also"></a><span data-ttu-id="5599e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5599e-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5599e-128">Referenz</span><span class="sxs-lookup"><span data-stu-id="5599e-128">Reference</span></span>

[<span data-ttu-id="5599e-129">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="5599e-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5599e-130">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="5599e-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5599e-131">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="5599e-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
