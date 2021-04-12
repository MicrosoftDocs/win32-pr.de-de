---
description: Lädt die AppHelp-Ressourcen Datei.
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: Sdbopenapphelpresourcefile-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpResourceFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2f1dfb1695e25bfb82e01ffa4f9eac4e245a6ffa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393077"
---
# <a name="sdbopenapphelpresourcefile-function"></a><span data-ttu-id="d44eb-103">Sdbopenapphelpresourcefile-Funktion</span><span class="sxs-lookup"><span data-stu-id="d44eb-103">SdbOpenApphelpResourceFile function</span></span>

<span data-ttu-id="d44eb-104">Lädt die AppHelp-Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="d44eb-104">Loads the Apphelp resource file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d44eb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d44eb-105">Syntax</span></span>


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a><span data-ttu-id="d44eb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d44eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d44eb-107">*pwszacresourcefile* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d44eb-107">*pwszACResourceFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d44eb-108">Der Pfad zur Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="d44eb-108">The path to the resource file.</span></span> <span data-ttu-id="d44eb-109">Wenn dieser Parameter **null** ist, wird die lokale Ressourcen-DLL geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d44eb-109">If this parameter is **NULL**, the local resource DLL is opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d44eb-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d44eb-110">Return value</span></span>

<span data-ttu-id="d44eb-111">Die-Funktion gibt ein Handle für die geöffnete Ressourcen Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="d44eb-111">The function returns a handle to the opened resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="d44eb-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d44eb-112">Requirements</span></span>



| <span data-ttu-id="d44eb-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d44eb-113">Requirement</span></span> | <span data-ttu-id="d44eb-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d44eb-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d44eb-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d44eb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d44eb-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d44eb-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d44eb-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d44eb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d44eb-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d44eb-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d44eb-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d44eb-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d44eb-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d44eb-120"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




