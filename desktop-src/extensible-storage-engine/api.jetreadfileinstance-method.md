---
description: 'Weitere Informationen finden Sie unter: API. jetreadfilanstance-Methode'
title: API. jetreadfilinput Stance-Methode
TOCTitle: 'JetReadFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_HANDLE,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetreadfileinstance(v=EXCHG.10)
ms:contentKeyID: 55100781
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80eaf61fd9cd07fce80d32fddf7056f6bff683c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352335"
---
# <a name="apijetreadfileinstance-method"></a><span data-ttu-id="8c8e2-103">API. jetreadfilinput Stance-Methode</span><span class="sxs-lookup"><span data-stu-id="8c8e2-103">Api.JetReadFileInstance method</span></span>

<span data-ttu-id="8c8e2-104">Ruft den Inhalt einer Datei ab, die mit [jetopenfileinstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md)geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="8c8e2-104">Retrieves the contents of a file opened with [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md).</span></span>

<span data-ttu-id="8c8e2-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8c8e2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8c8e2-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8c8e2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8c8e2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c8e2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetReadFileInstance ( _
    instance As JET_INSTANCE, _
    file As JET_HANDLE, _
    buffer As Byte(), _
    bufferSize As Integer, _
    <OutAttribute> ByRef bytesRead As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim file As JET_HANDLE
Dim buffer As Byte()
Dim bufferSize As Integer
Dim bytesRead As IntegerApi.JetReadFileInstance(instance, _
    file, buffer, bufferSize, bytesRead)
```

``` csharp
public static void JetReadFileInstance(
    JET_INSTANCE instance,
    JET_HANDLE file,
    byte[] buffer,
    int bufferSize,
    out int bytesRead
)
```

#### <a name="parameters"></a><span data-ttu-id="8c8e2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c8e2-108">Parameters</span></span>

  - <span data-ttu-id="8c8e2-109">instance</span><span class="sxs-lookup"><span data-stu-id="8c8e2-109">instance</span></span>  
    <span data-ttu-id="8c8e2-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8c8e2-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="8c8e2-111">Die zu verwendende-Instanz.</span><span class="sxs-lookup"><span data-stu-id="8c8e2-111">The instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8c8e2-112">file</span><span class="sxs-lookup"><span data-stu-id="8c8e2-112">file</span></span>  
    <span data-ttu-id="8c8e2-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8c8e2-113">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="8c8e2-114">Die Datei, aus der gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c8e2-114">The file to read from.</span></span>

<!-- end list -->

  - <span data-ttu-id="8c8e2-115">Puffer</span><span class="sxs-lookup"><span data-stu-id="8c8e2-115">buffer</span></span>  
    <span data-ttu-id="8c8e2-116">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="8c8e2-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="8c8e2-117">Der Puffer, in den gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c8e2-117">The buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="8c8e2-118">bufferSize</span><span class="sxs-lookup"><span data-stu-id="8c8e2-118">bufferSize</span></span>  
    <span data-ttu-id="8c8e2-119">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8c8e2-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8c8e2-120">Die Größe des Puffers.</span><span class="sxs-lookup"><span data-stu-id="8c8e2-120">The size of the buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="8c8e2-121">bytesRead</span><span class="sxs-lookup"><span data-stu-id="8c8e2-121">bytesRead</span></span>  
    <span data-ttu-id="8c8e2-122">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8c8e2-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8c8e2-123">Gibt die Menge der Daten zurück, die in den Puffer gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="8c8e2-123">Returns the amount of data read into the buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c8e2-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c8e2-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8c8e2-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="8c8e2-125">Reference</span></span>

[<span data-ttu-id="8c8e2-126">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="8c8e2-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8c8e2-127">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="8c8e2-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8c8e2-128">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="8c8e2-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
