---
description: 'Weitere Informationen finden Sie hier: JET_LGPOS. CompareTo-Methode'
title: JET_LGPOS. CompareTo-Methode
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo(Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.compareto(v=EXCHG.10)
ms:contentKeyID: 39514516
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 83012ed755ab876618147c013e99868927e16f1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349364"
---
# <a name="jet_lgposcompareto-method"></a><span data-ttu-id="11dce-103">JET_LGPOS. CompareTo-Methode</span><span class="sxs-lookup"><span data-stu-id="11dce-103">JET_LGPOS.CompareTo method</span></span>

<span data-ttu-id="11dce-104">Vergleicht diese Protokoll Position mit einer anderen Protokoll Position und bestimmt, ob diese Instanz vor oder nach der anderen Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="11dce-104">Compares this log position to another log position and determines whether this instance is before, the same as or after the other instance.</span></span>

<span data-ttu-id="11dce-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="11dce-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="11dce-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="11dce-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="11dce-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="11dce-107">Syntax</span></span>

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_LGPOS _
) As Integer
'Usage
Dim instance As JET_LGPOS
Dim other As JET_LGPOS
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_LGPOS other
)
```

#### <a name="parameters"></a><span data-ttu-id="11dce-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="11dce-108">Parameters</span></span>

  - <span data-ttu-id="11dce-109">andere</span><span class="sxs-lookup"><span data-stu-id="11dce-109">other</span></span>  
    <span data-ttu-id="11dce-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="11dce-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="11dce-111">Die Protokoll Position, die mit der aktuellen Instanz verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="11dce-111">The log position to compare to the current instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="11dce-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11dce-112">Return value</span></span>

<span data-ttu-id="11dce-113">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="11dce-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="11dce-114">Eine Zahl mit Vorzeichen, die die relativen Positionen dieser Instanz und des value-Parameters angibt.</span><span class="sxs-lookup"><span data-stu-id="11dce-114">A signed number indicating the relative positions of this instance and the value parameter.</span></span>  

#### <a name="implements"></a><span data-ttu-id="11dce-115">Implementiert</span><span class="sxs-lookup"><span data-stu-id="11dce-115">Implements</span></span>

[<span data-ttu-id="11dce-116">Nicht vergleichbar \<T\> . CompareTo (T)</span><span class="sxs-lookup"><span data-stu-id="11dce-116">IComparable\<T\>.CompareTo(T)</span></span>](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a><span data-ttu-id="11dce-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11dce-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="11dce-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="11dce-118">Reference</span></span>

[<span data-ttu-id="11dce-119">JET_LGPOS Struktur</span><span class="sxs-lookup"><span data-stu-id="11dce-119">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="11dce-120">Mitglieder JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="11dce-120">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="11dce-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="11dce-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
