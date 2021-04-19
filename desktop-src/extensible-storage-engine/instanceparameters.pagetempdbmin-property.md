---
description: Weitere Informationen finden Sie in der Eigenschaft instanceparameters. pagetempdbmin.
title: Instanceparameters. pagetempdbmin (Eigenschaft)
TOCTitle: 'PageTempDBMin property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.pagetempdbmin(v=EXCHG.10)
ms:contentKeyID: 55103558
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PageTempDBMin
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PageTempDBMin
- Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 06825762485ad52743d585ce0fed86bd1739cd21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356222"
---
# <a name="instanceparameterspagetempdbmin-property"></a><span data-ttu-id="3baf4-103">Instanceparameters. pagetempdbmin (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3baf4-103">InstanceParameters.PageTempDBMin property</span></span>

<span data-ttu-id="3baf4-104">Ruft die Anfangs Größe der temporären Datenbank ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="3baf4-104">Gets or sets the initial size of the temporary database.</span></span> <span data-ttu-id="3baf4-105">Die Größe befindet sich auf Datenbankseiten.</span><span class="sxs-lookup"><span data-stu-id="3baf4-105">The size is in database pages.</span></span> <span data-ttu-id="3baf4-106">Eine Größe von NULL gibt an, dass die Standardgröße einer normalen Datenbank verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3baf4-106">A size of zero indicates that the default size of an ordinary database should be used.</span></span> <span data-ttu-id="3baf4-107">Häufig ist es wünschenswert, dass kleine Anwendungen die temporäre Datenbank so klein wie möglich konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="3baf4-107">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="3baf4-108">Wenn Sie diesen Parameter auf [pagetempdbkleinsten](./systemparameters.pagetempdbsmallest-field.md) festlegen, wird die kleinste temporäre Datenbank erreicht.</span><span class="sxs-lookup"><span data-stu-id="3baf4-108">Setting this parameter to [PageTempDBSmallest](./systemparameters.pagetempdbsmallest-field.md) will achieve the smallest temporary database possible.</span></span>

<span data-ttu-id="3baf4-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3baf4-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3baf4-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3baf4-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3baf4-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="3baf4-111">Syntax</span></span>

``` vb
'Declaration
Public Property PageTempDBMin As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PageTempDBMin

instance.PageTempDBMin = value
```

``` csharp
public int PageTempDBMin { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="3baf4-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3baf4-112">Property value</span></span>

<span data-ttu-id="3baf4-113">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3baf4-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="3baf4-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3baf4-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3baf4-115">Referenz</span><span class="sxs-lookup"><span data-stu-id="3baf4-115">Reference</span></span>

[<span data-ttu-id="3baf4-116">Instanceparameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="3baf4-116">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="3baf4-117">Instanceparameters-Elemente</span><span class="sxs-lookup"><span data-stu-id="3baf4-117">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="3baf4-118">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="3baf4-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
