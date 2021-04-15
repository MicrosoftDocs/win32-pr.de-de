---
description: 'Weitere Informationen finden Sie hier: System Parameters. outstandingiomax (Eigenschaft)'
title: System Parameters. outstandingiomax (Eigenschaft)
TOCTitle: 'OutstandingIOMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.outstandingiomax(v=EXCHG.10)
ms:contentKeyID: 55104045
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_OutstandingIOMax
- Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
- Microsoft.Isam.Esent.Interop.SystemParameters.set_OutstandingIOMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7faf7af3aec16bc81fada5c8742b4c60595bedad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529285"
---
# <a name="systemparametersoutstandingiomax-property"></a><span data-ttu-id="6850c-103">System Parameters. outstandingiomax (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6850c-103">SystemParameters.OutstandingIOMax property</span></span>

<span data-ttu-id="6850c-104">Mit diesem Parameter wird gesteuert, wie viele Datenbankdatei-e/a-Vorgänge pro Datenträger im Host Betriebssystem gleichzeitig in eine Warteschlange eingereiht werden können.</span><span class="sxs-lookup"><span data-stu-id="6850c-104">This parameter controls how many database file I/Os can be queued per-disk in the host operating system at one time.</span></span> <span data-ttu-id="6850c-105">Ein größerer Wert für diesen Parameter kann die Leistung einer großen Datenbankanwendung erheblich unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6850c-105">A larger value for this parameter can significantly help the performance of a large database application.</span></span>

<span data-ttu-id="6850c-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6850c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6850c-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6850c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6850c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6850c-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Property OutstandingIOMax As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.OutstandingIOMax

SystemParameters.OutstandingIOMax = value
```

``` csharp
public static int OutstandingIOMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="6850c-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6850c-109">Property value</span></span>

<span data-ttu-id="6850c-110">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6850c-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="6850c-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6850c-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6850c-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="6850c-112">Reference</span></span>

[<span data-ttu-id="6850c-113">SystemParameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="6850c-113">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="6850c-114">SystemParameters-Member</span><span class="sxs-lookup"><span data-stu-id="6850c-114">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="6850c-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="6850c-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
