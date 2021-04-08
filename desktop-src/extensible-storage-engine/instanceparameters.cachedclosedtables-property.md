---
description: Weitere Informationen finden Sie in der Eigenschaft "instanceparameters. cachedclosedtables".
title: Instanceparameters. cachedclosedtables (Eigenschaft)
TOCTitle: 'CachedClosedTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55103293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CachedClosedTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CachedClosedTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f2465de2df3d25293f5298d40700512b6a086d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753976"
---
# <a name="instanceparameterscachedclosedtables-property"></a><span data-ttu-id="50ed6-103">Instanceparameters. cachedclosedtables (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="50ed6-103">InstanceParameters.CachedClosedTables property</span></span>

<span data-ttu-id="50ed6-104">Ruft einen Wert ab, der die Anzahl der B +-strukturressourcen angibt, die von der-Instanz zwischengespeichert wurden, nachdem die von Ihnen dargestellten Tabellen von der Anwendung geschlossen wurden</span><span class="sxs-lookup"><span data-stu-id="50ed6-104">Gets or sets a value giving the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="50ed6-105">Große Werte für diesen Parameter bewirken, dass die Datenbank-Engine mehr Arbeitsspeicher verwendet, aber die Geschwindigkeit erhöht, mit der eine große Anzahl von Tabellen nach dem Zufallsprinzip von der Anwendung geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="50ed6-105">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="50ed6-106">Dies ist nützlich für Anwendungen, die über ein Schema mit einer sehr großen Anzahl von Tabellen verfügen.</span><span class="sxs-lookup"><span data-stu-id="50ed6-106">This is useful for applications that have a schema with a very large number of tables.</span></span> <span data-ttu-id="50ed6-107">Unterstützt unter Windows Vista und up.</span><span class="sxs-lookup"><span data-stu-id="50ed6-107">Supported on Windows Vista and up.</span></span> <span data-ttu-id="50ed6-108">Wird unter Windows XP und Windows Server 2003 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="50ed6-108">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="50ed6-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="50ed6-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="50ed6-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="50ed6-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="50ed6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="50ed6-111">Syntax</span></span>

``` vb
'Declaration
Public Property CachedClosedTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.CachedClosedTables

instance.CachedClosedTables = value
```

``` csharp
public int CachedClosedTables { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="50ed6-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="50ed6-112">Property value</span></span>

<span data-ttu-id="50ed6-113">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="50ed6-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="50ed6-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50ed6-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="50ed6-115">Referenz</span><span class="sxs-lookup"><span data-stu-id="50ed6-115">Reference</span></span>

[<span data-ttu-id="50ed6-116">Instanceparameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="50ed6-116">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="50ed6-117">Instanceparameters-Elemente</span><span class="sxs-lookup"><span data-stu-id="50ed6-117">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="50ed6-118">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="50ed6-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
