---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNID. CompareTo-Methode'
title: JET_COLUMNID. CompareTo-Methode
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo(Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.compareto(v=EXCHG.10)
ms:contentKeyID: 39509744
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7eea24875b0639f7f5b7968084a3fff2aa7cccec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130176"
---
# <a name="jet_columnidcompareto-method"></a><span data-ttu-id="a25db-103">JET_COLUMNID. CompareTo-Methode</span><span class="sxs-lookup"><span data-stu-id="a25db-103">JET_COLUMNID.CompareTo method</span></span>

<span data-ttu-id="a25db-104">Vergleicht dieses ColumnID mit einem anderen ColumnID und bestimmt, ob diese Instanz vor oder nach der anderen Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="a25db-104">Compares this columnid to another columnid and determines whether this instance is before, the same as or after the other instance.</span></span>

<span data-ttu-id="a25db-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a25db-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a25db-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a25db-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a25db-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a25db-107">Syntax</span></span>

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_COLUMNID _
) As Integer
'Usage
Dim instance As JET_COLUMNID
Dim other As JET_COLUMNID
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_COLUMNID other
)
```

#### <a name="parameters"></a><span data-ttu-id="a25db-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a25db-108">Parameters</span></span>

  - <span data-ttu-id="a25db-109">andere</span><span class="sxs-lookup"><span data-stu-id="a25db-109">other</span></span>  
    <span data-ttu-id="a25db-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a25db-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="a25db-111">Das ColumnID, das mit der aktuellen Instanz verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a25db-111">The columnid to compare to the current instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a25db-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a25db-112">Return value</span></span>

<span data-ttu-id="a25db-113">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a25db-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="a25db-114">Eine Zahl mit Vorzeichen, die die relativen Positionen dieser Instanz und des value-Parameters angibt.</span><span class="sxs-lookup"><span data-stu-id="a25db-114">A signed number indicating the relative positions of this instance and the value parameter.</span></span>  

#### <a name="implements"></a><span data-ttu-id="a25db-115">Implementiert</span><span class="sxs-lookup"><span data-stu-id="a25db-115">Implements</span></span>

[<span data-ttu-id="a25db-116">Nicht vergleichbar \<T\> . CompareTo (T)</span><span class="sxs-lookup"><span data-stu-id="a25db-116">IComparable\<T\>.CompareTo(T)</span></span>](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a><span data-ttu-id="a25db-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a25db-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a25db-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="a25db-118">Reference</span></span>

[<span data-ttu-id="a25db-119">JET_COLUMNID Struktur</span><span class="sxs-lookup"><span data-stu-id="a25db-119">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="a25db-120">Mitglieder JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="a25db-120">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="a25db-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="a25db-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
