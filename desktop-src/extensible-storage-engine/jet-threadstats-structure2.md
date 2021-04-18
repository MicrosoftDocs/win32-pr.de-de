---
description: 'Weitere Informationen finden Sie hier: JET_THREADSTATS Struktur'
title: JET_THREADSTATS Struktur (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_THREADSTATS structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats(v=EXCHG.10)
ms:contentKeyID: 39512342
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 764a9276543fbb7a5b1aa2762cc8ed1877c45ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338960"
---
# <a name="jet_threadstats-structure"></a><span data-ttu-id="71bb5-103">JET_THREADSTATS Struktur</span><span class="sxs-lookup"><span data-stu-id="71bb5-103">JET_THREADSTATS structure</span></span>

<span data-ttu-id="71bb5-104">Enthält kumulative Statistiken für die Arbeit, die von der Datenbank-Engine auf dem aktuellen Thread ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71bb5-104">Contains cumulative statistics on the work performed by the database engine on the current thread.</span></span> <span data-ttu-id="71bb5-105">Diese Informationen werden über jetgetthreadstats zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="71bb5-105">This information is returned via JetGetThreadStats.</span></span>

<span data-ttu-id="71bb5-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="71bb5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="71bb5-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="71bb5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="71bb5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="71bb5-108">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_THREADSTATS _
    Implements IEquatable(Of JET_THREADSTATS)
'Usage
Dim instance As JET_THREADSTATS
```

``` csharp
[SerializableAttribute]
public struct JET_THREADSTATS : IEquatable<JET_THREADSTATS>
```

## <a name="thread-safety"></a><span data-ttu-id="71bb5-109">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="71bb5-109">Thread safety</span></span>

<span data-ttu-id="71bb5-110">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="71bb5-110">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="71bb5-111">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="71bb5-111">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="71bb5-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71bb5-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="71bb5-113">Referenz</span><span class="sxs-lookup"><span data-stu-id="71bb5-113">Reference</span></span>

[<span data-ttu-id="71bb5-114">Mitglieder JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="71bb5-114">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="71bb5-115">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="71bb5-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
