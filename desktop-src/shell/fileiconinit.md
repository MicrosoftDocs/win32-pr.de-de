---
description: Initialisiert oder initialisiert die System Abbild Liste neu.
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: "\"Fleieninit\"-Funktion"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIconInit
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 090f35cc576caf6f99a8d5822a0304f15383e8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345418"
---
# <a name="fileiconinit-function"></a><span data-ttu-id="a3a31-103">"Fleieninit"-Funktion</span><span class="sxs-lookup"><span data-stu-id="a3a31-103">FileIconInit function</span></span>

<span data-ttu-id="a3a31-104">Initialisiert oder initialisiert die System Abbild Liste neu.</span><span class="sxs-lookup"><span data-stu-id="a3a31-104">Initializes or reinitializes the system image list.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3a31-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3a31-105">Syntax</span></span>


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a><span data-ttu-id="a3a31-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3a31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3a31-107">*frestorecache* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3a31-107">*fRestoreCache* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3a31-108">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="a3a31-108">Type: **BOOL**</span></span>

<span data-ttu-id="a3a31-109">**True** , um den System Abbild Cache von der Festplatte wiederherzustellen. Andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="a3a31-109">**TRUE** to restore the system image cache from disk; **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3a31-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3a31-110">Return value</span></span>

<span data-ttu-id="a3a31-111">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="a3a31-111">Type: **BOOL**</span></span>

<span data-ttu-id="a3a31-112">**True** , wenn der Cache erfolgreich aktualisiert wurde, **false** , wenn die Initialisierung fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="a3a31-112">**TRUE** if the cache was successfully refreshed, **FALSE** if the initialization failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3a31-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3a31-113">Remarks</span></span>

<span data-ttu-id="a3a31-114">Wenn Sie System Abbild Listen in Ihrem eigenen Prozess verwenden, müssen Sie in den folgenden Zeitpunkten " **fleieninit** " anrufen:</span><span class="sxs-lookup"><span data-stu-id="a3a31-114">If you are using system image lists in your own process, you must call **FileIconInit** at the following times:</span></span>

-   <span data-ttu-id="a3a31-115">Beim Start.</span><span class="sxs-lookup"><span data-stu-id="a3a31-115">On launch.</span></span>
-   <span data-ttu-id="a3a31-116">Als Antwort auf eine [**WM- \_ settingchange**](../winmsg/wm-settingchange.md) -Nachricht, wenn das [**SPI- \_ setnonclientmetrics**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a3a31-116">In response to a [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message when the [**SPI\_SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) flag is set.</span></span>

<span data-ttu-id="a3a31-117">" **Fleideinit** " ist nicht in einer Header Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="a3a31-117">**FileIconInit** is not included in a header file.</span></span> <span data-ttu-id="a3a31-118">Sie müssen es direkt aus Shell32.dll mit der Ordnungszahl 660 abrufen.</span><span class="sxs-lookup"><span data-stu-id="a3a31-118">You must call it directly from Shell32.dll, using ordinal 660.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3a31-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a3a31-119">Requirements</span></span>



| <span data-ttu-id="a3a31-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3a31-120">Requirement</span></span> | <span data-ttu-id="a3a31-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a3a31-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3a31-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3a31-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a3a31-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3a31-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a3a31-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3a31-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a3a31-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3a31-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a3a31-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a3a31-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3a31-127"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3a31-127"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
