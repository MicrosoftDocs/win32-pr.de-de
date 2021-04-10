---
description: Bestimmt, ob die angegebene Datenbank eine der Standard Datenbanken (sysmain, AppHelp, drvmain oder msimain) ist.
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: Sdbisstandarddatabase-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbIsStandardDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9e9e445162c2bfc171ccf975981876f81a8bb804
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041325"
---
# <a name="sdbisstandarddatabase-function"></a><span data-ttu-id="a2140-103">Sdbisstandarddatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="a2140-103">SdbIsStandardDatabase function</span></span>

<span data-ttu-id="a2140-104">Bestimmt, ob die angegebene Datenbank eine der Standard Datenbanken (sysmain, AppHelp, drvmain oder msimain) ist.</span><span class="sxs-lookup"><span data-stu-id="a2140-104">Determines whether the specified database is one of the standard databases (Sysmain, Apphelp, Drvmain, or Msimain).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2140-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2140-105">Syntax</span></span>


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a><span data-ttu-id="a2140-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2140-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2140-107">*Guiddb* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2140-107">*GuidDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2140-108">Die GUID für die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a2140-108">The GUID for the database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2140-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2140-109">Return value</span></span>

<span data-ttu-id="a2140-110">Die Funktion gibt **true** zurück, wenn die GUID eine Standarddatenbank darstellt, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="a2140-110">The function returns **TRUE** if the GUID represents a standard database or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2140-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2140-111">Requirements</span></span>



| <span data-ttu-id="a2140-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2140-112">Requirement</span></span> | <span data-ttu-id="a2140-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a2140-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2140-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2140-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a2140-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2140-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a2140-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2140-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a2140-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2140-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a2140-118">DLL</span><span class="sxs-lookup"><span data-stu-id="a2140-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2140-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2140-119"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




