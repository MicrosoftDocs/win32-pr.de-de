---
description: Der hcryptkey-Datentyp wird verwendet, um Handles für kryptografische Schlüssel darzustellen.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: Hcryptkey (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56bda14169aa2f4d7c6e502d3444473ea0f00408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351427"
---
# <a name="hcryptkey"></a><span data-ttu-id="ee747-103">Hcryptkey</span><span class="sxs-lookup"><span data-stu-id="ee747-103">HCRYPTKEY</span></span>

<span data-ttu-id="ee747-104">Der **hcryptkey** -Datentyp wird verwendet, um Handles für [*kryptografische Schlüssel*](../secgloss/c-gly.md)darzustellen.</span><span class="sxs-lookup"><span data-stu-id="ee747-104">The **HCRYPTKEY** data type is used to represent handles to [*cryptographic keys*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="ee747-105">Diese Handles werden verwendet, um das CSP-Modul anzugeben, welcher Schlüssel in einem bestimmten Vorgang verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ee747-105">These handles are used to indicate to the CSP module which key is being used in a specific operation.</span></span> <span data-ttu-id="ee747-106">Das CSP-Modul ermöglicht keinen direkten Zugriff auf die Schlüsselwerte.</span><span class="sxs-lookup"><span data-stu-id="ee747-106">The CSP module does not enable direct access to the key values.</span></span> <span data-ttu-id="ee747-107">Stattdessen führt der Benutzer Funktionen mithilfe des Schlüssel Werts über das Schlüssel Handle aus.</span><span class="sxs-lookup"><span data-stu-id="ee747-107">Instead, the user performs functions by using the key value through the key handle.</span></span>


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a><span data-ttu-id="ee747-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee747-108">Requirements</span></span>



| <span data-ttu-id="ee747-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee747-109">Requirement</span></span> | <span data-ttu-id="ee747-110">Wert</span><span class="sxs-lookup"><span data-stu-id="ee747-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee747-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee747-111">Minimum supported client</span></span><br/> | <span data-ttu-id="ee747-112">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee747-112">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ee747-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee747-113">Minimum supported server</span></span><br/> | <span data-ttu-id="ee747-114">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee747-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ee747-115">Header</span><span class="sxs-lookup"><span data-stu-id="ee747-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee747-116"><dt>WinCrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee747-116"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
