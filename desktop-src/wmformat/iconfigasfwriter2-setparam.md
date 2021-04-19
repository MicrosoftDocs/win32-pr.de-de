---
title: IConfigAsfWriter2 SetParam-Methode
description: Die SetParam-Methode legt den Wert des angegebenen Filter Konfigurations Parameters fest.
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- SetParam-Methode Windows Media-Format
- SetParam-Methode, Windows Media-Format, IConfigAsfWriter2-Schnittstelle
- IConfigAsfWriter2-Schnittstelle Windows Media-Format, SetParam-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f123bf11c8297f3a7ce0d4b0047874d8d7b31b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341316"
---
# <a name="iconfigasfwriter2setparam-method"></a><span data-ttu-id="4c054-106">IConfigAsfWriter2:: SetParam-Methode</span><span class="sxs-lookup"><span data-stu-id="4c054-106">IConfigAsfWriter2::SetParam method</span></span>

<span data-ttu-id="4c054-107">Die **SetParam** -Methode legt den Wert des angegebenen Filter Konfigurations Parameters fest.</span><span class="sxs-lookup"><span data-stu-id="4c054-107">The **SetParam** method sets the value of the specified filter configuration parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c054-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c054-108">Syntax</span></span>


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a><span data-ttu-id="4c054-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c054-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c054-110">*dwparam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c054-110">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c054-111">Gibt den festzulegenden Parameter an.</span><span class="sxs-lookup"><span data-stu-id="4c054-111">Specifies the parameter to set.</span></span> <span data-ttu-id="4c054-112">Dabei muss es sich um einen Wert handeln, der in der Enumeration [ \_ am \_ asfschreiterconfig-Parameter \_ ](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4c054-112">It must be a value defined in the [\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="4c054-113">*dwParam1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c054-113">*dwParam1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c054-114">Gibt den Wert an, der dem *dwparam* -Parameter zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c054-114">Specifies the value to assign to the *dwParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4c054-115">*dwParam2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c054-115">*dwParam2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c054-116">Nicht verwendet; muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="4c054-116">Not used; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c054-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c054-117">Return value</span></span>

<span data-ttu-id="4c054-118">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="4c054-118">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="4c054-119">Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4c054-119">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c054-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c054-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="4c054-121">[**IConfigAsfWriter2-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4c054-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4c054-122">**IConfigAsfWriter2:: GetParam**</span><span class="sxs-lookup"><span data-stu-id="4c054-122">**IConfigAsfWriter2::GetParam**</span></span>](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 