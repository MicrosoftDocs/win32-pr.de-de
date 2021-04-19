---
description: Weitere Informationen finden Sie in der Eigenschaft instanceparameters. circularlog.
title: Instanceparameters. circularlog (Eigenschaft)
TOCTitle: 'CircularLog property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.circularlog(v=EXCHG.10)
ms:contentKeyID: 55103320
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CircularLog
- Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CircularLog
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f9a77aa0d0f60b49269dc939787b165a3f2f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354858"
---
# <a name="instanceparameterscircularlog-property"></a><span data-ttu-id="74a91-103">Instanceparameters. circularlog (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="74a91-103">InstanceParameters.CircularLog property</span></span>

<span data-ttu-id="74a91-104">Ruft einen Wert ab, der angibt, ob die zirkuläre Protokollierung on ist</span><span class="sxs-lookup"><span data-stu-id="74a91-104">Gets or sets a value indicating whether circular logging is on.</span></span> <span data-ttu-id="74a91-105">Wenn die zirkuläre Protokollierung deaktiviert ist, werden alle generierten Transaktionsprotokoll Dateien auf dem Datenträger gespeichert, bis Sie nicht mehr benötigt werden, da eine vollständige Sicherung der Datenbank ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="74a91-105">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="74a91-106">Wenn die zirkuläre Protokollierung auf on festgehalten wird, werden nur Transaktionsprotokoll Dateien auf dem Datenträger beibehalten</span><span class="sxs-lookup"><span data-stu-id="74a91-106">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="74a91-107">Der Vorteil dieses Modus besteht darin, dass keine Sicherungen erforderlich sind, um alte Transaktionsprotokoll Dateien abzukoppeln.</span><span class="sxs-lookup"><span data-stu-id="74a91-107">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span>

<span data-ttu-id="74a91-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="74a91-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="74a91-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="74a91-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="74a91-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="74a91-110">Syntax</span></span>

``` vb
'Declaration
Public Property CircularLog As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CircularLog

instance.CircularLog = value
```

``` csharp
public bool CircularLog { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="74a91-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="74a91-111">Property value</span></span>

<span data-ttu-id="74a91-112">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="74a91-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="74a91-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74a91-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="74a91-114">Referenz</span><span class="sxs-lookup"><span data-stu-id="74a91-114">Reference</span></span>

[<span data-ttu-id="74a91-115">Instanceparameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="74a91-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="74a91-116">Instanceparameters-Elemente</span><span class="sxs-lookup"><span data-stu-id="74a91-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="74a91-117">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="74a91-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
