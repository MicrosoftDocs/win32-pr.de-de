---
title: Iconfigasfwriter-Methode "Konfigurations Methode"
description: Mit der Methode "konfigurierte Methode" wird der Filter konfiguriert, um eine auf dem angegebenen vordefinierten Profil basierende ASF-Datei zu schreiben. (Veraltet.).
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- Konfigurierten Windows Media-Format für die Methode "Konfigurations Methode"
- Methode "config refilterusingprofileguid" Windows Media-Format, iconfigasfwriter-Schnittstelle
- Iconfigasfwriter-Schnittstelle Windows Media-Format, Methode "config refilterusingprofileguid"
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1521738af4411baa2c11f3d20722e09e2d22a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517024"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a><span data-ttu-id="ded46-107">Iconfigasfwriter:: konfigurifirefilterusingprofileguid-Methode</span><span class="sxs-lookup"><span data-stu-id="ded46-107">IConfigAsfWriter::ConfigureFilterUsingProfileGuid method</span></span>

<span data-ttu-id="ded46-108">Mit der Methode " **konfigurierte** Methode" wird der Filter konfiguriert, um eine auf dem angegebenen vordefinierten Profil basierende ASF-Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="ded46-108">The **ConfigureFilterUsingProfileGuid** method configures the filter to write an ASF file based on the specified predefined profile.</span></span> <span data-ttu-id="ded46-109">(Veraltet.)</span><span class="sxs-lookup"><span data-stu-id="ded46-109">(Deprecated.)</span></span>

## <a name="syntax"></a><span data-ttu-id="ded46-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ded46-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a><span data-ttu-id="ded46-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ded46-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ded46-112">*guidprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ded46-112">*guidProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ded46-113">**GUID** , die ein Profil identifiziert, das in der Windows Media-Format-SDK-Header Datei "wmsysprf. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ded46-113">**GUID** identifying a profile as defined in the Windows Media Format SDK header file Wmsysprf.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ded46-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ded46-114">Return value</span></span>

<span data-ttu-id="ded46-115">Gibt einen der folgenden **HRESULT** -Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="ded46-115">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="ded46-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ded46-116">Return code</span></span>                                                                                         | <span data-ttu-id="ded46-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ded46-117">Description</span></span>                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="ded46-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ded46-118"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="ded46-119">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ded46-119">The method succeeded.</span></span><br/>        |
| <dl> <span data-ttu-id="ded46-120"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="ded46-120"><dt>**E\_FAIL**</dt></span></span> </dl>              | <span data-ttu-id="ded46-121">Das Profil ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ded46-121">The profile is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="ded46-122"><dt>**VFW \_ E \_ falscher \_ Zustand**</dt></span><span class="sxs-lookup"><span data-stu-id="ded46-122"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="ded46-123">Das Filter Diagramm wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="ded46-123">The filter graph is stopped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ded46-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ded46-124">Remarks</span></span>

<span data-ttu-id="ded46-125">Ab dem Windows Media Format 9-Reihe-SDK wurden keine neuen Systemprofile definiert.</span><span class="sxs-lookup"><span data-stu-id="ded46-125">Beginning with the Windows Media Format 9 Series SDK, no new system profiles have been defined.</span></span> <span data-ttu-id="ded46-126">Mit dieser Methode können nur Systemprofil-GUIDs der Version 8 (oder früher) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ded46-126">Only version 8 (or earlier) system profile GUIDs can be used with this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="ded46-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ded46-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="ded46-128">[**Iconfigasfwriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ded46-128">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

