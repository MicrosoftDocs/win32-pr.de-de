---
description: 'Weitere Informationen finden Sie hier: JET_SNT-Enumeration'
title: JET_SNT-Enumeration
TOCTitle: JET_SNT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snt(v=EXCHG.10)
ms:contentKeyID: 39511261
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f6cad661d8265c32d605bbef94d75714ccb1783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346678"
---
# <a name="jet_snt-enumeration"></a><span data-ttu-id="50402-103">JET_SNT-Enumeration</span><span class="sxs-lookup"><span data-stu-id="50402-103">JET_SNT enumeration</span></span>

<span data-ttu-id="50402-104">Der Typ des Status, der gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="50402-104">Type of progress being reported.</span></span>

<span data-ttu-id="50402-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="50402-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="50402-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="50402-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="50402-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="50402-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_SNT
'Usage
Dim instance As JET_SNT
```

``` csharp
public enum JET_SNT
```

## <a name="members"></a><span data-ttu-id="50402-108">Member</span><span class="sxs-lookup"><span data-stu-id="50402-108">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="50402-109">Membername</span><span class="sxs-lookup"><span data-stu-id="50402-109">Member name</span></span></th>
<th><span data-ttu-id="50402-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50402-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="50402-111">Starten</span><span class="sxs-lookup"><span data-stu-id="50402-111">Begin</span></span></td>
<td><span data-ttu-id="50402-112">Rückruf für den Anfang eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="50402-112">Callback for the beginning of an operation.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="50402-113">Fortschritt</span><span class="sxs-lookup"><span data-stu-id="50402-113">Progress</span></span></td>
<td><span data-ttu-id="50402-114">Rückruf für den Fortschritt des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="50402-114">Callback for operation progress.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="50402-115">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="50402-115">Complete</span></span></td>
<td><span data-ttu-id="50402-116">Rückruf für den Abschluss eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="50402-116">Callback for the completion of an operation.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="50402-117">Fehler</span><span class="sxs-lookup"><span data-stu-id="50402-117">Fail</span></span></td>
<td><span data-ttu-id="50402-118">Rückruf für Fehler während des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="50402-118">Callback for failure during the operation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="50402-119">Wiederherstellbarkeits Schritt</span><span class="sxs-lookup"><span data-stu-id="50402-119">RecoveryStep</span></span></td>
<td><span data-ttu-id="50402-120">Rückruf für die Wiederherstellungs Steuerung.</span><span class="sxs-lookup"><span data-stu-id="50402-120">Callback for recovery control.</span></span>
<p><span data-ttu-id="50402-121">Wird für die interne Verarbeitung in Versionen des Windows-Betriebssystems vor Windows 8 verwendet.</span><span class="sxs-lookup"><span data-stu-id="50402-121">Used for internal processing in versions of the Windows operating system earlier than Windows 8.</span></span> <span data-ttu-id="50402-122">Dieser Wert gilt nicht für Windows-Versionen ab Windows 8.</span><span class="sxs-lookup"><span data-stu-id="50402-122">This value is not applicable to versions of Windows starting with Windows 8.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="50402-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50402-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="50402-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="50402-124">Reference</span></span>

[<span data-ttu-id="50402-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="50402-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
