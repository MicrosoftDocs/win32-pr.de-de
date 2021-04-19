---
description: Weitere Informationen finden Sie in der Eigenschaft "instanceparameters. maxtemporarytables".
title: Instanceparameters. maxtemporarytables (Eigenschaft)
TOCTitle: 'MaxTemporaryTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxtemporarytables(v=EXCHG.10)
ms:contentKeyID: 55103560
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxTemporaryTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxTemporaryTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5802e512a4ea6a4916ae54c24357dbdad057540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368885"
---
# <a name="instanceparametersmaxtemporarytables-property"></a><span data-ttu-id="8018e-103">Instanceparameters. maxtemporarytables (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8018e-103">InstanceParameters.MaxTemporaryTables property</span></span>

<span data-ttu-id="8018e-104">Ruft die Anzahl der temporären Tabellen Ressourcen für die Verwendung durch eine-Instanz ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="8018e-104">Gets or sets the number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="8018e-105">Diese Einstellung wirkt sich darauf aus, wie viele temporäre Tabellen gleichzeitig verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8018e-105">This setting will affect how many temporary tables can be used at the same time.</span></span> <span data-ttu-id="8018e-106">Wenn dieser Systemparameter auf 0 (null) festgelegt ist, wird keine temporäre Datenbank erstellt, und jede Aktivität, die die temporäre Datenbank benötigt, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="8018e-106">If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="8018e-107">Diese Einstellung kann hilfreich sein, um die e/a-Vorgänge zu vermeiden, die zum Erstellen der temporären Datenbank erforderlich sind, wenn bekannt ist, dass Sie nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8018e-107">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span>

<span data-ttu-id="8018e-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8018e-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8018e-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8018e-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8018e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8018e-110">Syntax</span></span>

``` vb
'Declaration
Public Property MaxTemporaryTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxTemporaryTables

instance.MaxTemporaryTables = value
```

``` csharp
public int MaxTemporaryTables { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="8018e-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8018e-111">Property value</span></span>

<span data-ttu-id="8018e-112">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8018e-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="remarks"></a><span data-ttu-id="8018e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8018e-113">Remarks</span></span>

<span data-ttu-id="8018e-114">Die Verwendung einer temporären Tabelle erfordert auch eine Cursor Ressource.</span><span class="sxs-lookup"><span data-stu-id="8018e-114">The use of a temporary table also requires a cursor resource.</span></span>

## <a name="see-also"></a><span data-ttu-id="8018e-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8018e-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8018e-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="8018e-116">Reference</span></span>

[<span data-ttu-id="8018e-117">Instanceparameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="8018e-117">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="8018e-118">Instanceparameters-Elemente</span><span class="sxs-lookup"><span data-stu-id="8018e-118">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="8018e-119">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="8018e-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
