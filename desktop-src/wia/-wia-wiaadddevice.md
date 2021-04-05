---
description: Die Funktion wiaadddevice Ruft die Benutzeroberfläche des Assistenten zum Installieren von Scanner und Kameras auf. Dies entspricht der Ausführung von &\# 0034; rundll32.exe STI \_ci.dll AddDevice&\# 0034; von der Eingabeaufforderung aus.
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: Wiaadddevice-Funktion (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaAddDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 694265f0a59096a5a6a58ccbf4e43c92e21fe9b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751752"
---
# <a name="wiaadddevice-function"></a><span data-ttu-id="d760b-104">Wiaadddevice-Funktion</span><span class="sxs-lookup"><span data-stu-id="d760b-104">WiaAddDevice function</span></span>

<span data-ttu-id="d760b-105">Die Funktion **wiaadddevice** Ruft die Benutzeroberfläche des Assistenten zum Installieren von Scanner und Kameras auf.</span><span class="sxs-lookup"><span data-stu-id="d760b-105">The **WiaAddDevice** function invokes the Scanner and Camera Installation Wizard UI.</span></span> <span data-ttu-id="d760b-106">Dies entspricht der Ausführung von "rundll32.exe STI \_ci.dll AddDevice" an der Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="d760b-106">It is equivalent to running "rundll32.exe sti\_ci.dll AddDevice" from the command prompt.</span></span>

## <a name="syntax"></a><span data-ttu-id="d760b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d760b-107">Syntax</span></span>


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a><span data-ttu-id="d760b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d760b-108">Parameters</span></span>

<span data-ttu-id="d760b-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d760b-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d760b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d760b-110">Return value</span></span>

<span data-ttu-id="d760b-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d760b-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d760b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d760b-112">Remarks</span></span>

<span data-ttu-id="d760b-113">Diese Funktion sollte mit Administrator Anmelde Informationen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d760b-113">This function should be called with administrator credentials.</span></span> <span data-ttu-id="d760b-114">Bei der Ausführung unter der Benutzerkontensteuerung (LUA) sollte der Prozess erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="d760b-114">When running under User Account Control (LUA), the process should be elevated.</span></span>

## <a name="requirements"></a><span data-ttu-id="d760b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d760b-115">Requirements</span></span>



| <span data-ttu-id="d760b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d760b-116">Requirement</span></span> | <span data-ttu-id="d760b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d760b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d760b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d760b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d760b-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d760b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d760b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d760b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d760b-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d760b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d760b-122">Header</span><span class="sxs-lookup"><span data-stu-id="d760b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d760b-123"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="d760b-123"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="d760b-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d760b-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="d760b-125"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d760b-125"><dt>Wiaguid.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d760b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d760b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d760b-127">**Installwiadevice**</span><span class="sxs-lookup"><span data-stu-id="d760b-127">**InstallWiaDevice**</span></span>](-wia-installwiadevice.md)
</dt> </dl>

 

 




