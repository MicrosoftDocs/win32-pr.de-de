---
description: Weitere Informationen finden Sie in der Eigenschaft instanceparameters. maxcursors.
title: Instanceparameters. maxcursors (Eigenschaft)
TOCTitle: 'MaxCursors property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxcursors(v=EXCHG.10)
ms:contentKeyID: 55103565
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxCursors
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxCursors
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 029ff7c41916e668f532be60f018870f30e487ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364248"
---
# <a name="instanceparametersmaxcursors-property"></a><span data-ttu-id="1747d-103">Instanceparameters. maxcursors (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1747d-103">InstanceParameters.MaxCursors property</span></span>

<span data-ttu-id="1747d-104">Ruft die Anzahl der für diese Instanz reservierten Cursor Ressourcen ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="1747d-104">Gets or sets the number of cursor resources reserved for this instance.</span></span> <span data-ttu-id="1747d-105">Eine Cursor Ressource entspricht direkt einer JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="1747d-105">A cursor resource directly corresponds to a JET_TABLEID.</span></span>

<span data-ttu-id="1747d-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1747d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1747d-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1747d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1747d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1747d-108">Syntax</span></span>

``` vb
'Declaration
Public Property MaxCursors As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxCursors

instance.MaxCursors = value
```

``` csharp
public int MaxCursors { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="1747d-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1747d-109">Property value</span></span>

<span data-ttu-id="1747d-110">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1747d-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="1747d-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1747d-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1747d-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="1747d-112">Reference</span></span>

[<span data-ttu-id="1747d-113">Instanceparameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="1747d-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="1747d-114">Instanceparameters-Elemente</span><span class="sxs-lookup"><span data-stu-id="1747d-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="1747d-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="1747d-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
