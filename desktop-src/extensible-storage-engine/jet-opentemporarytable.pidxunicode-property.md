---
description: Weitere Informationen finden Sie in der JET_OPENTEMPORARYTABLE. pidxunicode-Eigenschaft.
title: JET_OPENTEMPORARYTABLE. pidxunicode-Eigenschaft (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'pidxunicode property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.pidxunicode(v=EXCHG.10)
ms:contentKeyID: 55104227
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 98e5beb4f4523f5e6a6da37a999b6c0a2ab7b4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352722"
---
# <a name="jet_opentemporarytablepidxunicode-property"></a><span data-ttu-id="5cb0a-103">JET_OPENTEMPORARYTABLE. pidxunicode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5cb0a-103">JET_OPENTEMPORARYTABLE.pidxunicode property</span></span>

<span data-ttu-id="5cb0a-104">Ruft die Gebiets Schema-ID und normalisierungs Flags ab, die zum Vergleichen von Unicode-Schlüssel Spaltendaten in der temporären Tabelle verwendet werden, oder legt diese fest</span><span class="sxs-lookup"><span data-stu-id="5cb0a-104">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="5cb0a-105">Wenn dieser Parameter NULL ist, wird die Standard-LCID verwendet, um alle Unicode-Schlüssel Spalten in der temporären Tabelle zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-105">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="5cb0a-106">Die Standard-LCID ist das US-englische Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-106">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="5cb0a-107">Wenn dieser Parameter NULL ist, werden die standardnormalisierungs-Flags verwendet, um alle Unicode-Schlüssel Spaltendaten in der temporären Tabelle zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-107">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="5cb0a-108">Die standardnormalisierungs-Flags lauten: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="5cb0a-108">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="5cb0a-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5cb0a-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="5cb0a-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5cb0a-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5cb0a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cb0a-111">Syntax</span></span>

``` vb
'Declaration
Public Property pidxunicode As JET_UNICODEINDEX
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_UNICODEINDEX

value = instance.pidxunicode

instance.pidxunicode = value
```

``` csharp
public JET_UNICODEINDEX pidxunicode { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="5cb0a-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5cb0a-112">Property value</span></span>

<span data-ttu-id="5cb0a-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span><span class="sxs-lookup"><span data-stu-id="5cb0a-113">Type: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="5cb0a-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5cb0a-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5cb0a-115">Referenz</span><span class="sxs-lookup"><span data-stu-id="5cb0a-115">Reference</span></span>

[<span data-ttu-id="5cb0a-116">JET_OPENTEMPORARYTABLE-Klasse</span><span class="sxs-lookup"><span data-stu-id="5cb0a-116">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="5cb0a-117">Mitglieder JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="5cb0a-117">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="5cb0a-118">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="5cb0a-118">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
