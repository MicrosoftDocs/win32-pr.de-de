---
description: Weitere Informationen finden Sie in der Eigenschaft instanceparameters. logbuffers.
title: Instanceparameters. logbuffers (Eigenschaft)
TOCTitle: 'LogBuffers property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logbuffers(v=EXCHG.10)
ms:contentKeyID: 55107472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogBuffers
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f58e43ea38792549d384328dc0fd6c5d31616e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363665"
---
# <a name="instanceparameterslogbuffers-property"></a><span data-ttu-id="f88ef-103">Instanceparameters. logbuffers (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f88ef-103">InstanceParameters.LogBuffers property</span></span>

<span data-ttu-id="f88ef-104">Dient zum Abrufen oder Festlegen des Speichers, der zum Zwischenspeichern von Protokolldaten Sätzen verwendet wird, bevor Sie in die Transaktionsprotokoll Datei geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f88ef-104">Gets or sets the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="f88ef-105">Die Einheit für diesen Parameter ist die Sektorgröße des Volumes, das die Transaktionsprotokoll Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="f88ef-105">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="f88ef-106">Die Sektorgröße beträgt fast immer 512 Bytes, sodass es sicher ist, dass diese Größe für die Einheit angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="f88ef-106">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span> <span data-ttu-id="f88ef-107">Dieser Parameter wirkt sich auf die Leistung aus.</span><span class="sxs-lookup"><span data-stu-id="f88ef-107">This parameter has an impact on performance.</span></span> <span data-ttu-id="f88ef-108">Wenn die Auslastung der Datenbank-Engine stark ausgelastet ist, kann dieser Puffer sehr schnell vollständig werden.</span><span class="sxs-lookup"><span data-stu-id="f88ef-108">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="f88ef-109">Eine größere Cache Größe für die Transaktionsprotokoll Datei ist wichtig für eine gute Aktualisierungs Leistung bei einer solchen hohen Lade Bedingung.</span><span class="sxs-lookup"><span data-stu-id="f88ef-109">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="f88ef-110">Der Standardwert ist für diesen Fall zu klein.</span><span class="sxs-lookup"><span data-stu-id="f88ef-110">The default is known to be too small for this case.</span></span> <span data-ttu-id="f88ef-111">Legen Sie diesen Parameter nicht auf eine größere Anzahl von Puffern (in Bytes) als die Hälfte der Größe einer Transaktionsprotokoll Datei fest.</span><span class="sxs-lookup"><span data-stu-id="f88ef-111">Do not set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span>

<span data-ttu-id="f88ef-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f88ef-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f88ef-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f88ef-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f88ef-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="f88ef-114">Syntax</span></span>

``` vb
'Declaration
Public Property LogBuffers As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogBuffers

instance.LogBuffers = value
```

``` csharp
public int LogBuffers { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="f88ef-115">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f88ef-115">Property value</span></span>

<span data-ttu-id="f88ef-116">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f88ef-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="f88ef-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f88ef-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f88ef-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="f88ef-118">Reference</span></span>

[<span data-ttu-id="f88ef-119">Instanceparameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="f88ef-119">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="f88ef-120">Instanceparameters-Elemente</span><span class="sxs-lookup"><span data-stu-id="f88ef-120">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="f88ef-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f88ef-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
