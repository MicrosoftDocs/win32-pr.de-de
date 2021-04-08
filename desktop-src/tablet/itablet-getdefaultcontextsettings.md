---
description: Ruft die Standardkontext Einstellungen für das Tablet ab.
ms.assetid: 59d1bab0-a8b8-4e23-9311-2921f9035dc4
title: 'ITablet:: getdefaultcontextsettings-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetDefaultContextSettings
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7e2f0977257553d8405b337dcc1f22d8b0fdff5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757350"
---
# <a name="itabletgetdefaultcontextsettings-method"></a><span data-ttu-id="007b8-103">ITablet:: getdefaultcontextsettings-Methode</span><span class="sxs-lookup"><span data-stu-id="007b8-103">ITablet::GetDefaultContextSettings method</span></span>

<span data-ttu-id="007b8-104">Ruft die Standardkontext Einstellungen für das Tablet ab.</span><span class="sxs-lookup"><span data-stu-id="007b8-104">Retrieves the default context settings for the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="007b8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="007b8-105">Syntax</span></span>


```C++
HRESULT GetDefaultContextSettings(
  [out] TABLET_CONTEXT_SETTINGS **ppTCS
);
```



## <a name="parameters"></a><span data-ttu-id="007b8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="007b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="007b8-107">*PPTCs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="007b8-107">*ppTCS* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="007b8-108">Die Standardkontext Einstellungen für das Tablet.</span><span class="sxs-lookup"><span data-stu-id="007b8-108">The default context settings for the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="007b8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="007b8-109">Return value</span></span>

<span data-ttu-id="007b8-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="007b8-110">This method can return one of these values.</span></span>



| <span data-ttu-id="007b8-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="007b8-111">Return code</span></span>                                                                            | <span data-ttu-id="007b8-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="007b8-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="007b8-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="007b8-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="007b8-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="007b8-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="007b8-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="007b8-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="007b8-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="007b8-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="007b8-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="007b8-117">Remarks</span></span>

<span data-ttu-id="007b8-118">Es ist Aufgabe des Aufrufers, den von dieser Methode zurückgegebenen Speicher mithilfe von " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)" freizugeben.</span><span class="sxs-lookup"><span data-stu-id="007b8-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="007b8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="007b8-119">Requirements</span></span>



| <span data-ttu-id="007b8-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="007b8-120">Requirement</span></span> | <span data-ttu-id="007b8-121">Wert</span><span class="sxs-lookup"><span data-stu-id="007b8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="007b8-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="007b8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="007b8-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="007b8-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="007b8-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="007b8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="007b8-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="007b8-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="007b8-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="007b8-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="007b8-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="007b8-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="007b8-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="007b8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="007b8-129">**ITablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="007b8-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

