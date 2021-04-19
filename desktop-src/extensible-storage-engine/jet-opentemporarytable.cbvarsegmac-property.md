---
description: 'Weitere Informationen finden Sie hier: JET_OPENTEMPORARYTABLE. cbvarsegmac-Eigenschaft'
title: JET_OPENTEMPORARYTABLE. cbvarsegmac-Eigenschaft (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cbVarSegMac property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbvarsegmac(v=EXCHG.10)
ms:contentKeyID: 55104115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbVarSegMac
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbVarSegMac
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37fe218a9741235410d2452f04f082dc6673eaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363517"
---
# <a name="jet_opentemporarytablecbvarsegmac-property"></a><span data-ttu-id="0b8c1-103">JET_OPENTEMPORARYTABLE. cbvarsegmac (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0b8c1-103">JET_OPENTEMPORARYTABLE.cbVarSegMac property</span></span>

<span data-ttu-id="0b8c1-104">Ruft die maximale Datenmenge ab oder legt Sie fest, die von einer beliebigen Variablen Längen Spalte verwendet wird, um einen Schlüssel für eine bestimmte Zeile zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b8c1-104">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="0b8c1-105">Dieser Parameter kann verwendet werden, um die Menge des von einer bestimmten Schlüssel Spalte genutzten schlüsselplatzes zu steuern.</span><span class="sxs-lookup"><span data-stu-id="0b8c1-105">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="0b8c1-106">Dieser Grenzwert ist in Bytes.</span><span class="sxs-lookup"><span data-stu-id="0b8c1-106">This limit is in bytes.</span></span> <span data-ttu-id="0b8c1-107">Wenn dieser Parameter 0 (null) ist oder mit der [cbkeymost](./jet-opentemporarytable.cbkeymost-property.md) -Eigenschaft identisch ist, ist kein Limit wirksam.</span><span class="sxs-lookup"><span data-stu-id="0b8c1-107">If this parameter is zero or is the same as the [cbKeyMost](./jet-opentemporarytable.cbkeymost-property.md) property then no limit is in effect.</span></span>

<span data-ttu-id="0b8c1-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0b8c1-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="0b8c1-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0b8c1-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0b8c1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b8c1-110">Syntax</span></span>

``` vb
'Declaration
Public Property cbVarSegMac As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbVarSegMac

instance.cbVarSegMac = value
```

``` csharp
public int cbVarSegMac { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="0b8c1-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0b8c1-111">Property value</span></span>

<span data-ttu-id="0b8c1-112">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0b8c1-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="0b8c1-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b8c1-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0b8c1-114">Referenz</span><span class="sxs-lookup"><span data-stu-id="0b8c1-114">Reference</span></span>

[<span data-ttu-id="0b8c1-115">JET_OPENTEMPORARYTABLE-Klasse</span><span class="sxs-lookup"><span data-stu-id="0b8c1-115">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="0b8c1-116">Mitglieder JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="0b8c1-116">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="0b8c1-117">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="0b8c1-117">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
