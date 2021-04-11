---
description: Lesen Sie die aktive Konfiguration des Sammlers.
ms.assetid: ea26142d-5dcd-466d-b9df-5349f58a190f
ms.tgt_platform: multiple
title: GetConfiguration-Methode der Control-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.GetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5adfedb833043ffc56da09c7bdab95c1c4698587
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958160"
---
# <a name="getconfiguration-method-of-the-control-class"></a><span data-ttu-id="c4b1b-103">GetConfiguration-Methode der Control-Klasse</span><span class="sxs-lookup"><span data-stu-id="c4b1b-103">GetConfiguration method of the Control class</span></span>

<span data-ttu-id="c4b1b-104">Lesen Sie die aktive Konfiguration des Sammlers.</span><span class="sxs-lookup"><span data-stu-id="c4b1b-104">Read the active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4b1b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4b1b-105">Syntax</span></span>


```mof
Uint32 GetConfiguration(
  [out] Uint32 TimestampLow,
  [out] Uint32 TimestampHigh
);
```



## <a name="parameters"></a><span data-ttu-id="c4b1b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4b1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4b1b-107">*TimeStampLow* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c4b1b-107">*TimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4b1b-108">Wenn diese Methode zurückgegeben wird, enthält dieser Parameter die nieder wertigen Bits eines Zeitstempels, der angibt, wann die Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="c4b1b-108">When this method returns, this parameter contains the low-order bits of a timestamp that indicates when the configuration was set.</span></span>

</dd> <dt>

<span data-ttu-id="c4b1b-109">*TimeStampHigh* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c4b1b-109">*TimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4b1b-110">Wenn diese Methode zurückgegeben wird, enthält dieser Parameter die höherwertigen Bits eines Zeitstempels, der angibt, wann die Konfiguration festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="c4b1b-110">When this method returns, this parameter contains the high-order bits of a timestamp that indicates when the configuration was set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4b1b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4b1b-111">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="c4b1b-112">0</span><span class="sxs-lookup"><span data-stu-id="c4b1b-112">0</span></span>

<span data-ttu-id="c4b1b-113">Fehler</span><span class="sxs-lookup"><span data-stu-id="c4b1b-113">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c4b1b-114">1</span><span class="sxs-lookup"><span data-stu-id="c4b1b-114">1</span></span>

<span data-ttu-id="c4b1b-115">Erfolg</span><span class="sxs-lookup"><span data-stu-id="c4b1b-115">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4b1b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4b1b-116">Requirements</span></span>



| <span data-ttu-id="c4b1b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4b1b-117">Requirement</span></span> | <span data-ttu-id="c4b1b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c4b1b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4b1b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4b1b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c4b1b-120">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4b1b-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c4b1b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4b1b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c4b1b-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c4b1b-122">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="c4b1b-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4b1b-123">Namespace</span></span><br/>                | <span data-ttu-id="c4b1b-124">Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector</span><span class="sxs-lookup"><span data-stu-id="c4b1b-124">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="c4b1b-125">MOF</span><span class="sxs-lookup"><span data-stu-id="c4b1b-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4b1b-126"><dt>Booteventcollector WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c4b1b-126"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4b1b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c4b1b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4b1b-128"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4b1b-128"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="c4b1b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4b1b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4b1b-130">**Control**</span><span class="sxs-lookup"><span data-stu-id="c4b1b-130">**Control**</span></span>](control.md)
</dt> </dl>

 

 




