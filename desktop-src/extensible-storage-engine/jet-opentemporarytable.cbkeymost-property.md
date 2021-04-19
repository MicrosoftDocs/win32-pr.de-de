---
description: 'Weitere Informationen finden Sie hier: JET_OPENTEMPORARYTABLE. cbkeymost-Eigenschaft'
title: JET_OPENTEMPORARYTABLE. cbkeymost-Eigenschaft (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55104228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbKeyMost
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8e608d1419cd381c507874bf1f1c334d192ae2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363380"
---
# <a name="jet_opentemporarytablecbkeymost-property"></a><span data-ttu-id="d6d3b-103">JET_OPENTEMPORARYTABLE. cbkeymost-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d6d3b-103">JET_OPENTEMPORARYTABLE.cbKeyMost property</span></span>

<span data-ttu-id="d6d3b-104">Ruft die maximale Größe für einen Schlüssel ab, der eine angegebene Zeile darstellt, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="d6d3b-104">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="d6d3b-105">Die maximale Schlüsselgröße kann festgelegt werden, um zu steuern, wie Schlüssel abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="d6d3b-105">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="d6d3b-106">Das Abschneiden von Schlüsseln ist wichtig, da sich dies auf den Fall auswirkt, dass Zeilen als verschieden betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="d6d3b-106">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="d6d3b-107">Wenn dieser Parameter auf 0 oder 255 festgelegt ist, bleiben die maximale Schlüsselgröße und ihre Semantik identisch mit der maximalen Schlüsselgröße, die von Windows Server 2003 unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d6d3b-107">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="d6d3b-108">Dieser Parameter kann auch auf einen größeren Wert als Funktion der Datenbankseiten Größe für die Instanz [databasepagesize](./jet-param-enumeration.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d6d3b-108">This parameter may also be set to a larger value as a function of the database page size for the instance [DatabasePageSize](./jet-param-enumeration.md).</span></span> <span data-ttu-id="d6d3b-109">Weitere Informationen finden Sie unter [keymost](./vistaparam.keymost-field.md) .</span><span class="sxs-lookup"><span data-stu-id="d6d3b-109">See [KeyMost](./vistaparam.keymost-field.md) for more information.</span></span>

<span data-ttu-id="d6d3b-110">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d6d3b-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="d6d3b-111">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d6d3b-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d3b-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6d3b-112">Syntax</span></span>

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="d6d3b-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d6d3b-113">Property value</span></span>

<span data-ttu-id="d6d3b-114">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d6d3b-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="d6d3b-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6d3b-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d6d3b-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="d6d3b-116">Reference</span></span>

[<span data-ttu-id="d6d3b-117">JET_OPENTEMPORARYTABLE-Klasse</span><span class="sxs-lookup"><span data-stu-id="d6d3b-117">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="d6d3b-118">Mitglieder JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="d6d3b-118">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="d6d3b-119">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="d6d3b-119">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
