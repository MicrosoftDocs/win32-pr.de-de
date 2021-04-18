---
title: Iconfigasfwriter getcurrentprofileid-Methode
description: Die getcurrentprofileid-Methode ruft die aktuelle Profil-ID ab. (Nur für Windows Media-Format 4,0-Profile.).
ms.assetid: a5162bb1-5fcb-449e-b8d3-624b863e656d
keywords:
- Getcurrentprofileid-Methode Windows Media-Format
- Getcurrentprofileid-Methode Windows Media-Format, iconfigasfwriter-Schnittstelle
- Iconfigasfwriter-Schnittstelle Windows Media-Format, getcurrentprofileid-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416ac2c48f6ec8836a7390f18f38eca3dca35274
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337230"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a><span data-ttu-id="f8473-107">Iconfigasfwriter:: getcurrentprofileid-Methode</span><span class="sxs-lookup"><span data-stu-id="f8473-107">IConfigAsfWriter::GetCurrentProfileId method</span></span>

<span data-ttu-id="f8473-108">Die **getcurrentprofileid** -Methode ruft die aktuelle Profil-ID ab.</span><span class="sxs-lookup"><span data-stu-id="f8473-108">The **GetCurrentProfileId** method retrieves the current profile ID.</span></span> <span data-ttu-id="f8473-109">(Nur für Windows Media-Format 4,0-Profile.)</span><span class="sxs-lookup"><span data-stu-id="f8473-109">(For Windows Media Format 4.0 profiles only.)</span></span>

## <a name="syntax"></a><span data-ttu-id="f8473-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8473-110">Syntax</span></span>


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
);
```



## <a name="parameters"></a><span data-ttu-id="f8473-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8473-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8473-112">*pdwprofileid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f8473-112">*pdwProfileId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8473-113">Ein Zeiger auf eine Variable vom Typ **DWORD** , die die aktuelle Profil-ID empfängt.</span><span class="sxs-lookup"><span data-stu-id="f8473-113">Pointer to a variable of type **DWORD** that receives the current profile ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8473-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8473-114">Return value</span></span>

<span data-ttu-id="f8473-115">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="f8473-115">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="f8473-116">Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8473-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8473-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8473-117">Remarks</span></span>

<span data-ttu-id="f8473-118">Diese Methode ist mittlerweile veraltet, da Sie Windows Media-Format-SDK-Profile von Version 4,0 annimmt.</span><span class="sxs-lookup"><span data-stu-id="f8473-118">This method is now obsolete because it assumes version 4.0 Windows Media Format SDK profiles.</span></span> <span data-ttu-id="f8473-119">Verwenden Sie stattdessen [**iconfigasfwriter:: getcurrentprofile**](iconfigasfwriter-getcurrentprofile.md) oder [**iconfigasfwriter:: getcurrentprofileguid**](iconfigasfwriter-getcurrentprofileguid.md) , um ein Profil für Version 7,0 und höher ordnungsgemäß zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f8473-119">Use [**IConfigAsfWriter::GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) or [**IConfigAsfWriter::GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) instead to correctly identify a profile for version 7.0 and later.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8473-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8473-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="f8473-121">[**Iconfigasfwriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f8473-121">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 