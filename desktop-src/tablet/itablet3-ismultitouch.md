---
description: Bestimmt, ob ein Eingabegerät Multitouchscreen unterstützt.
ms.assetid: 4fef7060-2235-4bee-a37b-40d827732b30
title: 'ITablet3:: ismultitouchscreen-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.IsMultiTouch
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: ed05e110c13af8fe73eebf004183de42eb9fffd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217670"
---
# <a name="itablet3ismultitouch-method"></a><span data-ttu-id="411b6-103">ITablet3:: ismultitouchscreen-Methode</span><span class="sxs-lookup"><span data-stu-id="411b6-103">ITablet3::IsMultiTouch method</span></span>

<span data-ttu-id="411b6-104">Bestimmt, ob ein Eingabegerät Multitouchscreen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="411b6-104">Determines whether an input device supports multitouch.</span></span>

## <a name="syntax"></a><span data-ttu-id="411b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="411b6-105">Syntax</span></span>


```C++
HRESULT IsMultiTouch(
  [out] BOOL *bIsMultiTouch
);
```



## <a name="parameters"></a><span data-ttu-id="411b6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="411b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="411b6-107">*bismultiberühren* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="411b6-107">*bIsMultiTouch* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="411b6-108">Gibt an, ob das Gerät multiberühren ist.</span><span class="sxs-lookup"><span data-stu-id="411b6-108">Indicates whether the device is multitouch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="411b6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="411b6-109">Return value</span></span>

<span data-ttu-id="411b6-110">Gibt bei Erfolg **S \_ OK** zurück, andernfalls wird ein Fehlercode wie **z \_ . b**. "Fehler" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="411b6-110">Returns **S\_OK** on success, otherwise returns an error code such as **E\_FAIL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="411b6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="411b6-111">Remarks</span></span>

<span data-ttu-id="411b6-112">Nachdem Sie über [**IRealTimeStylus3:: multitouchenabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) oder **ITablet3:: ismultiberühren** festgelegt haben, dass multiinput verfügbar ist, wählt eine Anwendung möglicherweise multifingereingabenachrichten aus.</span><span class="sxs-lookup"><span data-stu-id="411b6-112">After determining through [**IRealTimeStylus3::MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) or **ITablet3::IsMultiTouch** that multitouch is available, an application may choose to opt in for multitouch input messages.</span></span> <span data-ttu-id="411b6-113">Weitere Informationen zum Filtern von multifingermethoden finden Sie im Abschnitt **IRealTimeStylus3:: multitouchenabled** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="411b6-113">Additional information on filtering multitouch methods is available in the **IRealTimeStylus3::MultiTouchEnabled** property section.</span></span>

## <a name="examples"></a><span data-ttu-id="411b6-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="411b6-114">Examples</span></span>


```C++
CComQIPtr<ITablet3> spITablet3 = g_spITablet3;
VARIANT_BOOL b;
spITablet3->get_IsMultiTouch(&b);
```



## <a name="requirements"></a><span data-ttu-id="411b6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="411b6-115">Requirements</span></span>



| <span data-ttu-id="411b6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="411b6-116">Requirement</span></span> | <span data-ttu-id="411b6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="411b6-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="411b6-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="411b6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="411b6-119">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="411b6-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="411b6-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="411b6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="411b6-121">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="411b6-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="411b6-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="411b6-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="411b6-123"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="411b6-123"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="411b6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="411b6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="411b6-125">**ITablet3**</span><span class="sxs-lookup"><span data-stu-id="411b6-125">**ITablet3**</span></span>](itablet3.md)
</dt> <dt>

[<span data-ttu-id="411b6-126">**MultiTouchEnabled**</span><span class="sxs-lookup"><span data-stu-id="411b6-126">**MultiTouchEnabled**</span></span>](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




