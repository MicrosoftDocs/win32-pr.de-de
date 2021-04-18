---
description: Beendet den Collector. Wenn der Collector als Dienst ausgeführt wird, ist das Beenden des Dienstanbieter der bessere Ansatz.
ms.assetid: fab3e060-156f-46f5-98a2-d47a23d64552
ms.tgt_platform: multiple
title: Shutdown-Methode der Steuerelement Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Shutdown
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d401ac528498d7b8ab5ccacbf6a0b5bf781555f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344343"
---
# <a name="shutdown-method-of-the-control-class"></a><span data-ttu-id="4b787-104">Shutdown-Methode der Steuerelement Klasse</span><span class="sxs-lookup"><span data-stu-id="4b787-104">Shutdown method of the Control class</span></span>

<span data-ttu-id="4b787-105">Beendet den Collector.</span><span class="sxs-lookup"><span data-stu-id="4b787-105">Stops the collector.</span></span> <span data-ttu-id="4b787-106">Wenn der Collector als Dienst ausgeführt wird, ist das Beenden des Dienstanbieter der bessere Ansatz.</span><span class="sxs-lookup"><span data-stu-id="4b787-106">If the collector is running as a service, stopping the service is the better approach.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b787-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b787-107">Syntax</span></span>


```mof
void Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="4b787-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b787-108">Parameters</span></span>

<span data-ttu-id="4b787-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4b787-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b787-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b787-110">Return value</span></span>

<span data-ttu-id="4b787-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4b787-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b787-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b787-112">Requirements</span></span>



| <span data-ttu-id="4b787-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b787-113">Requirement</span></span> | <span data-ttu-id="4b787-114">Wert</span><span class="sxs-lookup"><span data-stu-id="4b787-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b787-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b787-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4b787-116">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b787-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4b787-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b787-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4b787-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4b787-118">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="4b787-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="4b787-119">Namespace</span></span><br/>                | <span data-ttu-id="4b787-120">Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector</span><span class="sxs-lookup"><span data-stu-id="4b787-120">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="4b787-121">MOF</span><span class="sxs-lookup"><span data-stu-id="4b787-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b787-122"><dt>Booteventcollector WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4b787-122"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b787-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4b787-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b787-124"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b787-124"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="4b787-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b787-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b787-126">**Control**</span><span class="sxs-lookup"><span data-stu-id="4b787-126">**Control**</span></span>](control.md)
</dt> </dl>

 

 




