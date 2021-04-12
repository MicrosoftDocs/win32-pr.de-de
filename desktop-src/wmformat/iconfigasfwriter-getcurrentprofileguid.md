---
title: Iconfigasfwriter getcurrentprofileguid-Methode
description: Die getcurrentprofileguid-Methode ruft die aktuelle Windows Media Systemprofile-GUID ab.
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- Getcurrentprofileguid-Methode Windows Media-Format
- Getcurrentprofileguid-Methode Windows Media-Format, iconfigasfwriter-Schnittstelle
- Iconfigasfwriter-Schnittstelle Windows Media-Format, getcurrentprofileguid-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49282ed6ea33db8052e167568e5b5fa70cda9e01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316125"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a><span data-ttu-id="8abfa-106">Iconfigasfwriter:: getcurrentprofileguid-Methode</span><span class="sxs-lookup"><span data-stu-id="8abfa-106">IConfigAsfWriter::GetCurrentProfileGuid method</span></span>

<span data-ttu-id="8abfa-107">Die **getcurrentprofileguid** -Methode ruft die aktuelle Windows Media Systemprofile-GUID ab.</span><span class="sxs-lookup"><span data-stu-id="8abfa-107">The **GetCurrentProfileGuid** method retrieves the current Windows Media system profile GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="8abfa-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8abfa-108">Syntax</span></span>


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a><span data-ttu-id="8abfa-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8abfa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8abfa-110">*pprofileguid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8abfa-110">*pProfileGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8abfa-111">Ein Zeiger auf eine Variable vom Typ **GUID** , die das aktuelle Systemprofil identifiziert, das vom Filter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8abfa-111">Pointer to a variable of type **GUID** that identifies the current system profile being used by the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8abfa-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8abfa-112">Return value</span></span>

<span data-ttu-id="8abfa-113">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="8abfa-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="8abfa-114">Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8abfa-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8abfa-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8abfa-115">Remarks</span></span>

<span data-ttu-id="8abfa-116">Diese Methode wird nicht mit benutzerdefinierten Profilen verwendet (einschließlich aller Profile, die Streams enthalten, die die Windows Media Audio und Video Codecs verwenden), da alle diese Profile von Anwendungen erstellt werden und keinen GUID-Bezeichner aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8abfa-116">This method is not used with custom profiles (including all profiles that include streams that use the Windows Media Audio and Video codecs) because all such profiles are created by applications and have no GUID identifier.</span></span> <span data-ttu-id="8abfa-117">Wenn kein Systemprofil geladen wird, wird *pprofileguid* auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8abfa-117">If no system profile is loaded, *pProfileGuid* will be set to **NULL**.</span></span>

## <a name="see-also"></a><span data-ttu-id="8abfa-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8abfa-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="8abfa-119">[**Iconfigasfwriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8abfa-119">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 