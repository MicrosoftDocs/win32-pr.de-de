---
description: 'Weitere Informationen finden Sie unter: JET_RECPOS-Klasse'
title: JET_RECPOS-Klasse
TOCTitle: JET_RECPOS class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_RECPOS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_recpos(v=EXCHG.10)
ms:contentKeyID: 55103839
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RECPOS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RECPOS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 09fce4bf1d73ad1b9767e39ae5c90b25eccdea73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366252"
---
# <a name="jet_recpos-class"></a><span data-ttu-id="34c05-103">JET_RECPOS-Klasse</span><span class="sxs-lookup"><span data-stu-id="34c05-103">JET_RECPOS class</span></span>

<span data-ttu-id="34c05-104">Stellt eine Bruch Position innerhalb eines Indexes dar.</span><span class="sxs-lookup"><span data-stu-id="34c05-104">Represents a fractional position within an index.</span></span> <span data-ttu-id="34c05-105">Diese wird von jetgotoposition und jetgetrecordposition verwendet.</span><span class="sxs-lookup"><span data-stu-id="34c05-105">This is used by JetGotoPosition and JetGetRecordPosition.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="34c05-106">Vererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="34c05-106">Inheritance hierarchy</span></span>

[<span data-ttu-id="34c05-107">System.Object</span><span class="sxs-lookup"><span data-stu-id="34c05-107">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="34c05-108">Microsoft.Isam.Esent.Interop.JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="34c05-108">Microsoft.Isam.Esent.Interop.JET_RECPOS</span></span>  

<span data-ttu-id="34c05-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="34c05-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="34c05-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="34c05-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="34c05-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="34c05-111">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class JET_RECPOS _
    Implements IContentEquatable(Of JET_RECPOS), IDeepCloneable(Of JET_RECPOS)
'Usage
Dim instance As JET_RECPOS
```

``` csharp
[SerializableAttribute]
public sealed class JET_RECPOS : IContentEquatable<JET_RECPOS>, 
    IDeepCloneable<JET_RECPOS>
```

## <a name="thread-safety"></a><span data-ttu-id="34c05-112">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="34c05-112">Thread safety</span></span>

<span data-ttu-id="34c05-113">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="34c05-113">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="34c05-114">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="34c05-114">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="34c05-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34c05-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="34c05-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="34c05-116">Reference</span></span>

[<span data-ttu-id="34c05-117">Mitglieder JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="34c05-117">JET_RECPOS members</span></span>](./jet-recpos-members.md)

[<span data-ttu-id="34c05-118">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="34c05-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
