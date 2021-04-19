---
description: Weitere Informationen finden Sie in der bytescolumnvalue. Value-Eigenschaft.
title: Bytescolumnvalue. Value-Eigenschaft
TOCTitle: 'Value property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue.value(v=EXCHG.10)
ms:contentKeyID: 55107249
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
- Microsoft.Isam.Esent.Interop.BytesColumnValue.set_Value
- Microsoft.Isam.Esent.Interop.BytesColumnValue.get_Value
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0804a7a05640336be77e5f446ad99227db592f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373205"
---
# <a name="bytescolumnvaluevalue-property"></a><span data-ttu-id="aa13a-103">Bytescolumnvalue. Value-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="aa13a-103">BytesColumnValue.Value property</span></span>

<span data-ttu-id="aa13a-104">Ruft den Wert der Spalte ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="aa13a-104">Gets or sets the value of the column.</span></span> <span data-ttu-id="aa13a-105">Verwenden Sie [SetColumns (JET_SESID, JET_TABLEID, \[ \] )](./api.setcolumns-method.md) , um einen Datensatz mit dem Spaltenwert zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="aa13a-105">Use [SetColumns(JET_SESID, JET_TABLEID, \[\])](./api.setcolumns-method.md) to update a record with the column value.</span></span>

<span data-ttu-id="aa13a-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aa13a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aa13a-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aa13a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aa13a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa13a-108">Syntax</span></span>

``` vb
'Declaration
Public Property Value As Byte()
    Get
    Set
'Usage
Dim instance As BytesColumnValue
Dim value As Byte()

value = instance.Value

instance.Value = value
```

``` csharp
public byte[] Value { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="aa13a-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="aa13a-109">Property value</span></span>

<span data-ttu-id="aa13a-110">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="aa13a-110">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="aa13a-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa13a-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aa13a-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="aa13a-112">Reference</span></span>

[<span data-ttu-id="aa13a-113">Bytescolumnvalue-Klasse</span><span class="sxs-lookup"><span data-stu-id="aa13a-113">BytesColumnValue class</span></span>](./bytescolumnvalue-class.md)

[<span data-ttu-id="aa13a-114">Bytescolumnvalue-Member</span><span class="sxs-lookup"><span data-stu-id="aa13a-114">BytesColumnValue members</span></span>](./bytescolumnvalue-members.md)

[<span data-ttu-id="aa13a-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="aa13a-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
