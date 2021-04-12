---
description: 'Weitere Informationen finden Sie hier: Server2003Grbits. ForwardOnly-Feld'
title: Server2003Grbits. ForwardOnly-Feld (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: ForwardOnly field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.forwardonly(v=EXCHG.10)
ms:contentKeyID: 55104214
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec4427628e8d6bfee427fa91c15ed6aee3887314
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130157"
---
# <a name="server2003grbitsforwardonly-field"></a><span data-ttu-id="7acaa-103">Server2003Grbits. ForwardOnly-Feld</span><span class="sxs-lookup"><span data-stu-id="7acaa-103">Server2003Grbits.ForwardOnly field</span></span>

<span data-ttu-id="7acaa-104">Mit dieser Option wird angefordert, dass die temporäre Tabelle nur erstellt wird, wenn der temporäre Tabellen-Manager die für zwischen Abfrageergebnisse optimierte-Implementierung verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="7acaa-104">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="7acaa-105">Wenn ein beliebiges Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, schlägt der Vorgang mit JET_errCannotMaterializeForwardOnlySort fehl.</span><span class="sxs-lookup"><span data-stu-id="7acaa-105">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="7acaa-106">Ein Nebeneffekt dieser Option besteht darin, zuzulassen, dass die temporäre Tabelle Datensätze mit doppelten Index Schlüsseln enthält.</span><span class="sxs-lookup"><span data-stu-id="7acaa-106">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="7acaa-107">Weitere Informationen finden Sie unter [Unique](./temptablegrbit-enumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="7acaa-107">See [Unique](./temptablegrbit-enumeration.md) for more information.</span></span>

<span data-ttu-id="7acaa-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7acaa-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="7acaa-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7acaa-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7acaa-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7acaa-110">Syntax</span></span>

``` vb
'Declaration
Public Const ForwardOnly As TempTableGrbit
'Usage
Dim value As TempTableGrbit

value = Server2003Grbits.ForwardOnly
```

``` csharp
public const TempTableGrbit ForwardOnly
```

## <a name="see-also"></a><span data-ttu-id="7acaa-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7acaa-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7acaa-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="7acaa-112">Reference</span></span>

[<span data-ttu-id="7acaa-113">Server2003Grbits-Klasse</span><span class="sxs-lookup"><span data-stu-id="7acaa-113">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="7acaa-114">Server2003Grbits-Member</span><span class="sxs-lookup"><span data-stu-id="7acaa-114">Server2003Grbits members</span></span>](./server2003grbits-members.md)

[<span data-ttu-id="7acaa-115">Microsoft. ISAM. ESENT. Interop. Server2003-Namespace</span><span class="sxs-lookup"><span data-stu-id="7acaa-115">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
