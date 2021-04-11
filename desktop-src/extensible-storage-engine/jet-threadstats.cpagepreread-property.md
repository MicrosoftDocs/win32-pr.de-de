---
description: 'Weitere Informationen finden Sie unter: JET_THREADSTATS. cpagepreread-Eigenschaft'
title: JET_THREADSTATS. cpagepreread-Eigenschaft (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cPagePreread property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPagePreread
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cpagepreread(v=EXCHG.10)
ms:contentKeyID: 39510638
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPagePreread
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cPagePreread
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPagePreread
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cPagePreread
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd004407fcc7474435b8b2e12dc7eff9555b0e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217547"
---
# <a name="jet_threadstatscpagepreread-property"></a><span data-ttu-id="78b51-103">JET_THREADSTATS. cpagepreread (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="78b51-103">JET_THREADSTATS.cPagePreread property</span></span>

<span data-ttu-id="78b51-104">Ruft die Gesamtanzahl der Datenbankseiten ab, die von der Datenbank-Engine auf dem aktuellen Thread vorab von der Festplatte abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="78b51-104">Gets the total number of database pages prefetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="78b51-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="78b51-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="78b51-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="78b51-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="78b51-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="78b51-107">Syntax</span></span>

``` vb
'Declaration
Public Property cPagePreread As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cPagePreread
```

``` csharp
public int cPagePreread { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="78b51-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="78b51-108">Property value</span></span>

<span data-ttu-id="78b51-109">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="78b51-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="78b51-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78b51-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="78b51-111">Referenz</span><span class="sxs-lookup"><span data-stu-id="78b51-111">Reference</span></span>

[<span data-ttu-id="78b51-112">JET_THREADSTATS Struktur</span><span class="sxs-lookup"><span data-stu-id="78b51-112">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="78b51-113">Mitglieder JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="78b51-113">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="78b51-114">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="78b51-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
