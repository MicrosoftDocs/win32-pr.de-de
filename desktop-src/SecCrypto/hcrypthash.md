---
description: Der hcrypthash-Datentyp wird verwendet, um Handles für Hash Objekte darzustellen.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: Hcrypthash (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a009350ed910627c1e6ec9ae33997ed20c7fec2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867412"
---
# <a name="hcrypthash"></a><span data-ttu-id="56ecf-103">Hcrypthash</span><span class="sxs-lookup"><span data-stu-id="56ecf-103">HCRYPTHASH</span></span>

<span data-ttu-id="56ecf-104">Der **hcrypthash** -Datentyp wird verwendet, um Handles für [*Hash Objekte*](../secgloss/h-gly.md)darzustellen.</span><span class="sxs-lookup"><span data-stu-id="56ecf-104">The **HCRYPTHASH** data type is used to represent handles to [*hash objects*](../secgloss/h-gly.md).</span></span> <span data-ttu-id="56ecf-105">Diese Handles geben dem CSP-Modul an, welcher Hash in einem bestimmten Vorgang verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56ecf-105">These handles indicate to the CSP module which hash is being used in a particular operation.</span></span> <span data-ttu-id="56ecf-106">Das CSP-Modul ermöglicht keine direkte Bearbeitung der Hashwerte.</span><span class="sxs-lookup"><span data-stu-id="56ecf-106">The CSP module does not enable direct manipulation of the hash values.</span></span> <span data-ttu-id="56ecf-107">Stattdessen manipuliert der Benutzer die Hashwerte durch das Hashhandle.</span><span class="sxs-lookup"><span data-stu-id="56ecf-107">Instead, the user manipulates the hash values through the hash handle.</span></span>


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a><span data-ttu-id="56ecf-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56ecf-108">Requirements</span></span>



| <span data-ttu-id="56ecf-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56ecf-109">Requirement</span></span> | <span data-ttu-id="56ecf-110">Wert</span><span class="sxs-lookup"><span data-stu-id="56ecf-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56ecf-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56ecf-111">Minimum supported client</span></span><br/> | <span data-ttu-id="56ecf-112">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56ecf-112">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="56ecf-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56ecf-113">Minimum supported server</span></span><br/> | <span data-ttu-id="56ecf-114">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56ecf-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56ecf-115">Header</span><span class="sxs-lookup"><span data-stu-id="56ecf-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="56ecf-116"><dt>WinCrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="56ecf-116"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
