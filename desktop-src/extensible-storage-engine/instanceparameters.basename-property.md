---
description: Weitere Informationen finden Sie in der instanceparameters. baseName-Eigenschaft.
title: Instanceparameters. baseName-Eigenschaft
TOCTitle: 'BaseName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.BaseName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.basename(v=EXCHG.10)
ms:contentKeyID: 55103315
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.BaseName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.BaseName
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_BaseName
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_BaseName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d7e36363a73dc19c324e1852f58346e0ad95b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353537"
---
# <a name="instanceparametersbasename-property"></a><span data-ttu-id="b46d2-103">Instanceparameters. baseName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b46d2-103">InstanceParameters.BaseName property</span></span>

<span data-ttu-id="b46d2-104">Ruft das drei Buchstabe-Präfix für viele der Dateien ab, die von der Datenbank-Engine verwendet werden, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="b46d2-104">Gets or sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="b46d2-105">Beispielsweise wird die Prüf Punkt Datei als EDB bezeichnet. Standardmäßig chk, da EDB der Standardbasis Name ist.</span><span class="sxs-lookup"><span data-stu-id="b46d2-105">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span>

<span data-ttu-id="b46d2-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b46d2-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b46d2-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b46d2-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b46d2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b46d2-108">Syntax</span></span>

``` vb
'Declaration
Public Property BaseName As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.BaseName

instance.BaseName = value
```

``` csharp
public string BaseName { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="b46d2-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b46d2-109">Property value</span></span>

<span data-ttu-id="b46d2-110">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b46d2-110">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="b46d2-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b46d2-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b46d2-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="b46d2-112">Reference</span></span>

[<span data-ttu-id="b46d2-113">Instanceparameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="b46d2-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="b46d2-114">Instanceparameters-Elemente</span><span class="sxs-lookup"><span data-stu-id="b46d2-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="b46d2-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="b46d2-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
