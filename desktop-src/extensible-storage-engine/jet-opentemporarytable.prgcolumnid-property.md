---
description: 'Weitere Informationen finden Sie hier: JET_OPENTEMPORARYTABLE. prgcolumnid-Eigenschaft'
title: JET_OPENTEMPORARYTABLE. prgcolumnid-Eigenschaft (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'prgcolumnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.prgcolumnid(v=EXCHG.10)
ms:contentKeyID: 55104133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_prgcolumnid
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_prgcolumnid
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd6516e01d08de32f7962a48d2caca69ddbf0427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960684"
---
# <a name="jet_opentemporarytableprgcolumnid-property"></a><span data-ttu-id="51882-103">JET_OPENTEMPORARYTABLE. prgcolumnid-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="51882-103">JET_OPENTEMPORARYTABLE.prgcolumnid property</span></span>

<span data-ttu-id="51882-104">Ruft den Ausgabepuffer ab, der das Array der Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="51882-104">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="51882-105">Die Spalten-IDs in diesem Array entsprechen exakt dem Eingabe Array von Spaltendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="51882-105">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="51882-106">Folglich muss die Größe dieses Puffers der Größe von [prgcolumndef](./jet-opentemporarytable.prgcolumndef-property.md)entsprechen.</span><span class="sxs-lookup"><span data-stu-id="51882-106">As a result, the size of this buffer must correspond to the size of [prgcolumndef](./jet-opentemporarytable.prgcolumndef-property.md).</span></span>

<span data-ttu-id="51882-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="51882-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="51882-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="51882-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="51882-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="51882-109">Syntax</span></span>

``` vb
'Declaration
Public Property prgcolumnid As JET_COLUMNID()
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_COLUMNID()

value = instance.prgcolumnid

instance.prgcolumnid = value
```

``` csharp
public JET_COLUMNID[] prgcolumnid { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="51882-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="51882-110">Property value</span></span>

<span data-ttu-id="51882-111">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="51882-111">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="51882-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51882-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="51882-113">Referenz</span><span class="sxs-lookup"><span data-stu-id="51882-113">Reference</span></span>

[<span data-ttu-id="51882-114">JET_OPENTEMPORARYTABLE-Klasse</span><span class="sxs-lookup"><span data-stu-id="51882-114">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="51882-115">Mitglieder JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="51882-115">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="51882-116">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="51882-116">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
