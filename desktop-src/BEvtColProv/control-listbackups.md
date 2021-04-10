---
description: Gibt die Liste der gespeicherten Sicherungs Konfigurationsdateien zurück, die wieder hergestellt werden können.
ms.assetid: 9487c50e-ef3b-425f-92ef-0614290e9af4
ms.tgt_platform: multiple
title: Listbackups-Methode der Steuerelement Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ListBackups
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 858fb7ee38b7875426ae31172618ad8ac60510ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125839"
---
# <a name="listbackups-method-of-the-control-class"></a><span data-ttu-id="ad8d5-103">Listbackups-Methode der Steuerelement Klasse</span><span class="sxs-lookup"><span data-stu-id="ad8d5-103">ListBackups method of the Control class</span></span>

<span data-ttu-id="ad8d5-104">Gibt die Liste der gespeicherten Sicherungs Konfigurationsdateien zurück, die wieder hergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="ad8d5-104">Returns the list of the saved backup configuration files that can be restored.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad8d5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad8d5-105">Syntax</span></span>


```mof
void ListBackups(
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string Files[],
  [out] Uint32 FilesTimestampLow[],
  [out] Uint32 FilesTimestampHigh[]
);
```



## <a name="parameters"></a><span data-ttu-id="ad8d5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad8d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad8d5-107">*Originaltimestamplow* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ad8d5-107">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad8d5-108">Der Zeitstempel, zu dem die aktuelle Konfiguration festgelegt wurde (wenn Sie von einer Sicherung wieder hergestellt wird, enthält den ursprünglichen Zeitstempel).</span><span class="sxs-lookup"><span data-stu-id="ad8d5-108">The timestamp of when the current configuration was set (if restored from backup, will contain the original timestamp).</span></span> <span data-ttu-id="ad8d5-109">Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="ad8d5-109">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="ad8d5-110">*Originaltimestamphigh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ad8d5-110">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad8d5-111">Der Zeitstempel, zu dem die aktuelle Konfiguration festgelegt wurde (wenn Sie von einer Sicherung wieder hergestellt wird, enthält den ursprünglichen Zeitstempel).</span><span class="sxs-lookup"><span data-stu-id="ad8d5-111">The timestamp of when the current configuration was set (if restored from backup, will contain the original timestamp).</span></span> <span data-ttu-id="ad8d5-112">Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="ad8d5-112">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="ad8d5-113">*Dateien* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ad8d5-113">*Files* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad8d5-114">Die Liste der verfügbaren Sicherungsdateien, von der neuesten zum ältesten.</span><span class="sxs-lookup"><span data-stu-id="ad8d5-114">The list of available backup files, in order from the newest to the oldest.</span></span>

</dd> <dt>

<span data-ttu-id="ad8d5-115">*Filestimestamplow* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ad8d5-115">*FilesTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad8d5-116">Für jede Sicherungsdatei der Zeitstempel, zu dem die Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ad8d5-116">For each backup file, the timestamp of when its configuration was set.</span></span> <span data-ttu-id="ad8d5-117">Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="ad8d5-117">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="ad8d5-118">*Filestimestamphigh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ad8d5-118">*FilesTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad8d5-119">Für jede Sicherungsdatei der Zeitstempel, zu dem die Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ad8d5-119">For each backup file, the timestamp of when its configuration was set.</span></span> <span data-ttu-id="ad8d5-120">Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="ad8d5-120">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad8d5-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad8d5-121">Return value</span></span>

<span data-ttu-id="ad8d5-122">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ad8d5-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad8d5-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad8d5-123">Requirements</span></span>



| <span data-ttu-id="ad8d5-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad8d5-124">Requirement</span></span> | <span data-ttu-id="ad8d5-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ad8d5-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad8d5-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad8d5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ad8d5-127">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad8d5-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ad8d5-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad8d5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ad8d5-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ad8d5-129">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="ad8d5-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad8d5-130">Namespace</span></span><br/>                | <span data-ttu-id="ad8d5-131">Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector</span><span class="sxs-lookup"><span data-stu-id="ad8d5-131">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="ad8d5-132">MOF</span><span class="sxs-lookup"><span data-stu-id="ad8d5-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad8d5-133"><dt>Booteventcollector WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ad8d5-133"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad8d5-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ad8d5-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad8d5-135"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ad8d5-135"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="ad8d5-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad8d5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad8d5-137">**Control**</span><span class="sxs-lookup"><span data-stu-id="ad8d5-137">**Control**</span></span>](control.md)
</dt> </dl>

 

