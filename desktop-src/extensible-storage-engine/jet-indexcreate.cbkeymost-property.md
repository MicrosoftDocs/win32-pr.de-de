---
description: 'Weitere Informationen finden Sie hier: JET_INDEXCREATE. cbkeymost-Eigenschaft'
title: JET_INDEXCREATE. cbkeymost-Eigenschaft
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55103646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_cbKeyMost
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 321704f88da59af33f4dab99d7d681fbcbd96e1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866847"
---
# <a name="jet_indexcreatecbkeymost-property"></a><span data-ttu-id="86406-103">JET_INDEXCREATE. cbkeymost-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="86406-103">JET_INDEXCREATE.cbKeyMost property</span></span>

<span data-ttu-id="86406-104">Ruft die maximal zulässige Größe (in Bytes) für Schlüssel im Index ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="86406-104">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="86406-105">Die unterstützte Mindestschlüsselgröße ist JET_cbKeyMostMin (255). Dies ist die maximale maximale Schlüsselgröße.</span><span class="sxs-lookup"><span data-stu-id="86406-105">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="86406-106">Die maximale Schlüsselgröße hängt von der Datenbankseiten Größe [databasepagesize](./jet-param-enumeration.md)ab.</span><span class="sxs-lookup"><span data-stu-id="86406-106">The maximum key size is dependent on the database page size [DatabasePageSize](./jet-param-enumeration.md).</span></span> <span data-ttu-id="86406-107">Die maximale Schlüsselgröße kann mit [keymost](./systemparameters.keymost-property.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="86406-107">The maximum key size can be retrieved with [KeyMost](./systemparameters.keymost-property.md).</span></span> <span data-ttu-id="86406-108">Dieser Parameter wird unter Windows XP und Windows Server 2003 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="86406-108">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="86406-109">Anders als bei der nicht verwalteten API ist **indexkeymost ()** (JET_bitIndexKeyMost) nicht erforderlich, sondern wird automatisch hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86406-109">Unlike the unmanaged API, **IndexKeyMost()** (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span>

<span data-ttu-id="86406-110">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="86406-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="86406-111">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="86406-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="86406-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="86406-112">Syntax</span></span>

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="86406-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="86406-113">Property value</span></span>

<span data-ttu-id="86406-114">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="86406-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="86406-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86406-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="86406-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="86406-116">Reference</span></span>

[<span data-ttu-id="86406-117">JET_INDEXCREATE-Klasse</span><span class="sxs-lookup"><span data-stu-id="86406-117">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="86406-118">Mitglieder JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="86406-118">JET_INDEXCREATE members</span></span>](./jet-indexcreate-members.md)

[<span data-ttu-id="86406-119">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="86406-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
