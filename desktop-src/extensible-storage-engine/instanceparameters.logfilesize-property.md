---
description: Weitere Informationen finden Sie in der instanceparameters. LogFileSize-Eigenschaft.
title: Instanceparameters. LogFileSize (Eigenschaft)
TOCTitle: 'LogFileSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logfilesize(v=EXCHG.10)
ms:contentKeyID: 55103312
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogFileSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogFileSize
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c141c76a92f49b4b5000cad65e302a7cf15d780f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368886"
---
# <a name="instanceparameterslogfilesize-property"></a><span data-ttu-id="514d4-103">Instanceparameters. LogFileSize (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="514d4-103">InstanceParameters.LogFileSize property</span></span>

<span data-ttu-id="514d4-104">Ruft die Größe der Transaktionsprotokoll Dateien ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="514d4-104">Gets or sets the size of the transaction log files.</span></span> <span data-ttu-id="514d4-105">Dieser Parameter sollte in Einheiten von 1024 Bytes festgelegt werden (z. b. eine Einstellung von 2048 gibt 2 MB Protokolldateien aus).</span><span class="sxs-lookup"><span data-stu-id="514d4-105">This parameter should be set in units of 1024 bytes (e.g. a setting of 2048 will give 2MB logfiles).</span></span>

<span data-ttu-id="514d4-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="514d4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="514d4-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="514d4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="514d4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="514d4-108">Syntax</span></span>

``` vb
'Declaration
Public Property LogFileSize As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogFileSize

instance.LogFileSize = value
```

``` csharp
public int LogFileSize { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="514d4-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="514d4-109">Property value</span></span>

<span data-ttu-id="514d4-110">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="514d4-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="514d4-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="514d4-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="514d4-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="514d4-112">Reference</span></span>

[<span data-ttu-id="514d4-113">Instanceparameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="514d4-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="514d4-114">Instanceparameters-Elemente</span><span class="sxs-lookup"><span data-stu-id="514d4-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="514d4-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="514d4-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
