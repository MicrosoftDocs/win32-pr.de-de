---
description: 'Weitere Informationen finden Sie hier: JET_INDEXID Struktur'
title: JET_INDEXID Struktur
TOCTitle: JET_INDEXID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_INDEXID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid(v=EXCHG.10)
ms:contentKeyID: 39510071
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13ff0984926fe821d666d18c1907c9bd1bf93b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362947"
---
# <a name="jet_indexid-structure"></a><span data-ttu-id="8972a-103">JET_INDEXID Struktur</span><span class="sxs-lookup"><span data-stu-id="8972a-103">JET_INDEXID structure</span></span>

<span data-ttu-id="8972a-104">Enthält eine Index-ID.</span><span class="sxs-lookup"><span data-stu-id="8972a-104">Holds an index ID.</span></span> <span data-ttu-id="8972a-105">Eine Index-ID ist ein Hinweis, der verwendet wird, um die Auswahl des aktuellen Indexes mithilfe von jetsetcurrentindex zu beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="8972a-105">An index ID is a hint that is used to accelerate the selection of the current index using JetSetCurrentIndex.</span></span> <span data-ttu-id="8972a-106">Dies ist besonders nützlich, wenn eine Tabelle eine große Anzahl von Indizes enthält.</span><span class="sxs-lookup"><span data-stu-id="8972a-106">It is most useful when there is a very large number of indexes over a table.</span></span> <span data-ttu-id="8972a-107">Die Index-ID kann mit jetgetindexinfo oder jetgettableindexinfo abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8972a-107">The index ID can be retrieved using JetGetIndexInfo or JetGetTableIndexInfo.</span></span>

<span data-ttu-id="8972a-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8972a-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8972a-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8972a-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8972a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8972a-110">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_INDEXID _
    Implements IEquatable(Of JET_INDEXID)
'Usage
Dim instance As JET_INDEXID
```

``` csharp
public struct JET_INDEXID : IEquatable<JET_INDEXID>
```

## <a name="remarks"></a><span data-ttu-id="8972a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8972a-111">Remarks</span></span>

<span data-ttu-id="8972a-112">Das Pack-Attribut ist erforderlich, da die C++-Version als Bytearray definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8972a-112">The Pack attribute is necessary because the C++ version is defined as a byte array.</span></span> <span data-ttu-id="8972a-113">Wenn der C \# -Compiler die übliche Auffüll Zeichen zwischen uint cbStruct und IntPtr einfügt, wird die Struktur zu groß.</span><span class="sxs-lookup"><span data-stu-id="8972a-113">If the C\# compiler inserts the usual padding between the uint cbStruct and the IntPtr, then the structure ends up too large.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="8972a-114">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="8972a-114">Thread safety</span></span>

<span data-ttu-id="8972a-115">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="8972a-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8972a-116">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="8972a-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8972a-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8972a-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8972a-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="8972a-118">Reference</span></span>

[<span data-ttu-id="8972a-119">Mitglieder JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="8972a-119">JET_INDEXID members</span></span>](./jet-indexid-members.md)

[<span data-ttu-id="8972a-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="8972a-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
