---
description: 'Weitere Informationen finden Sie unter: JET_ENUMCOLUMNID. ctagsequence-Eigenschaft'
title: JET_ENUMCOLUMNID. ctagsequence (Eigenschaft)
TOCTitle: 'ctagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.ctagsequence(v=EXCHG.10)
ms:contentKeyID: 55107537
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_ctagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8e12c8c6a102cbb20862b3cc9859f7e632ade8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347758"
---
# <a name="jet_enumcolumnidctagsequence-property"></a><span data-ttu-id="e188c-103">JET_ENUMCOLUMNID. ctagsequence (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e188c-103">JET_ENUMCOLUMNID.ctagSequence property</span></span>

<span data-ttu-id="e188c-104">Ruft die Anzahl der Spaltenwerte (durch einen einbasierten Index) ab, die für die angegebene Spalten-ID aufgelistet werden sollen, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="e188c-104">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="e188c-105">Wenn ctagsequence gleich 0 (null) ist, wird rgtagsequence ignoriert, und alle Spaltenwerte für die angegebene Spalten-ID werden aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e188c-105">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span>

<span data-ttu-id="e188c-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e188c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e188c-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e188c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e188c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e188c-108">Syntax</span></span>

``` vb
'Declaration
Public Property ctagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer

value = instance.ctagSequence

instance.ctagSequence = value
```

``` csharp
public int ctagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="e188c-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e188c-109">Property value</span></span>

<span data-ttu-id="e188c-110">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e188c-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e188c-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e188c-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e188c-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="e188c-112">Reference</span></span>

[<span data-ttu-id="e188c-113">JET_ENUMCOLUMNID-Klasse</span><span class="sxs-lookup"><span data-stu-id="e188c-113">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="e188c-114">Mitglieder JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="e188c-114">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="e188c-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e188c-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
