---
description: Weitere Informationen finden Sie in der Eigenschaft instanceparameters. preferredverpages.
title: Instanceparameters. preferredverpages (Eigenschaft)
TOCTitle: 'PreferredVerPages property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.preferredverpages(v=EXCHG.10)
ms:contentKeyID: 55103322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PreferredVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PreferredVerPages
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 067d41cd3fb945b2f18d3cd6154b1eef6793b1e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347426"
---
# <a name="instanceparameterspreferredverpages-property"></a><span data-ttu-id="2c412-103">Instanceparameters. preferredverpages (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2c412-103">InstanceParameters.PreferredVerPages property</span></span>

<span data-ttu-id="2c412-104">Ruft die bevorzugte Anzahl von Versionsspeicher Seiten ab, die für diese Instanz reserviert sind, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="2c412-104">Gets or sets the preferred number of version store pages reserved for this instance.</span></span> <span data-ttu-id="2c412-105">Wenn die Größe des Versionsspeicher diesen Schwellenwert überschreitet, werden alle Informationen, die nur für optionale Hintergrundaufgaben verwendet werden, z. b. das Freigeben von gelöschtem Speicherplatz in der Datenbank, stattdessen geopfert, um Platz für Transaktionsinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2c412-105">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span>

<span data-ttu-id="2c412-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2c412-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2c412-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2c412-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2c412-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c412-108">Syntax</span></span>

``` vb
'Declaration
Public Property PreferredVerPages As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PreferredVerPages

instance.PreferredVerPages = value
```

``` csharp
public int PreferredVerPages { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="2c412-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2c412-109">Property value</span></span>

<span data-ttu-id="2c412-110">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2c412-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="2c412-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c412-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2c412-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="2c412-112">Reference</span></span>

[<span data-ttu-id="2c412-113">Instanceparameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="2c412-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="2c412-114">Instanceparameters-Elemente</span><span class="sxs-lookup"><span data-stu-id="2c412-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="2c412-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="2c412-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
