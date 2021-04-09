---
description: 'Weitere Informationen finden Sie hier: JET_sesparam-Enumeration'
title: JET_sesparam-Enumeration (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: JET_sesparam enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_sesparam(v=EXCHG.10)
ms:contentKeyID: 55104452
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.Base
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitDefault
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitGenericContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.Base
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitGenericContext
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitDefault
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5ddfd613eecf5e9a6d9b6cec9eebcbab04e9b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128649"
---
# <a name="jet_sesparam-enumeration"></a><span data-ttu-id="51bd5-103">JET_sesparam-Enumeration</span><span class="sxs-lookup"><span data-stu-id="51bd5-103">JET_sesparam enumeration</span></span>

<span data-ttu-id="51bd5-104">ESENT-Sitzungs Parameter.</span><span class="sxs-lookup"><span data-stu-id="51bd5-104">ESENT session parameters.</span></span>

<span data-ttu-id="51bd5-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="51bd5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="51bd5-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="51bd5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="51bd5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="51bd5-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_sesparam
'Usage
Dim instance As JET_sesparam
```

``` csharp
public enum JET_sesparam
```

## <a name="members"></a><span data-ttu-id="51bd5-108">Member</span><span class="sxs-lookup"><span data-stu-id="51bd5-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="51bd5-109">Membername</span><span class="sxs-lookup"><span data-stu-id="51bd5-109">Member name</span></span></th>
<th><span data-ttu-id="51bd5-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51bd5-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="51bd5-111">Basis</span><span class="sxs-lookup"><span data-stu-id="51bd5-111">Base</span></span></td>
<td><span data-ttu-id="51bd5-112">Dieser Parameter ist nicht für die Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="51bd5-112">This parameter is not meant to be used.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="51bd5-113">Commitdefault</span><span class="sxs-lookup"><span data-stu-id="51bd5-113">CommitDefault</span></span></td>
<td><span data-ttu-id="51bd5-114">Dieser Parameter legt die grbits für Commit fest.</span><span class="sxs-lookup"><span data-stu-id="51bd5-114">This parameter sets the grbits for commit.</span></span> <span data-ttu-id="51bd5-115">Es ist funktional identisch mit dem Systemparameter JET_param. commitdefault bei Verwendung mit einer-Instanz und einer-SID.</span><span class="sxs-lookup"><span data-stu-id="51bd5-115">It is functionally the same as the system parameter JET_param.CommitDefault when used with an instance and a sesid.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="51bd5-116">Commitgenericcontext</span><span class="sxs-lookup"><span data-stu-id="51bd5-116">CommitGenericContext</span></span></td>
<td><span data-ttu-id="51bd5-117">Mit diesem Parameter wird ein Benutzer spezifischer commitkontext festgelegt, der im Transaktionsprotokoll bei Commit auf Ebene 0 platziert wird.</span><span class="sxs-lookup"><span data-stu-id="51bd5-117">This parameter sets a user specific commit context that will be placed in the transaction log on commit to level 0.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="51bd5-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51bd5-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="51bd5-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="51bd5-119">Reference</span></span>

[<span data-ttu-id="51bd5-120">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="51bd5-120">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
