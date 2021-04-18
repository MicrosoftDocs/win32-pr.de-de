---
title: Iconfigasfwriter-Methode "konfigurifisingprofileid"
description: Die Methode "konfigurierte Methode" konfiguriert den Filter zum Schreiben einer ASF-Datei mit einem Profil Bezeichner (ID)-Index aus der Liste "Systemprofile". (Nur für Windows Media-Format 4,0-Profile.).
ms.assetid: b0375785-83db-4540-aca9-7ba0bb81c1ef
keywords:
- Konfigurierungs Methode für das Windows Media-Format
- Konfigurations-/filterusingprofileid-Methode Windows Media-Format, iconfigasfwriter-Schnittstelle
- Iconfigasfwriter-Schnittstelle Windows Media-Format, Configuration Report User User-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0226195d7657667e3947b55546b321edafa7befc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340276"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a><span data-ttu-id="c4f1c-107">Iconfigasfwriter:: konfiguriert refilterusingprofileid-Methode</span><span class="sxs-lookup"><span data-stu-id="c4f1c-107">IConfigAsfWriter::ConfigureFilterUsingProfileId method</span></span>

<span data-ttu-id="c4f1c-108">Die Methode " **konfigurierte** Methode" konfiguriert den Filter zum Schreiben einer ASF-Datei mit einem Profil Bezeichner (ID)-Index aus der Liste "Systemprofile".</span><span class="sxs-lookup"><span data-stu-id="c4f1c-108">The **ConfigureFilterUsingProfileId** method configures the filter to write an ASF file with a profile identifier (ID) index from the system profile list.</span></span> <span data-ttu-id="c4f1c-109">(Nur für Windows Media-Format 4,0-Profile.)</span><span class="sxs-lookup"><span data-stu-id="c4f1c-109">(For Windows Media Format 4.0 profiles only.)</span></span>

## <a name="syntax"></a><span data-ttu-id="c4f1c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4f1c-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfileId(
  [in] DWORD dwProfileId
);
```



## <a name="parameters"></a><span data-ttu-id="c4f1c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4f1c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4f1c-112">*dwprofileid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4f1c-112">*dwProfileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4f1c-113">Profil-ID gemäß der Definition in Version 4,0 des Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="c4f1c-113">Profile ID as defined in version 4.0 of the Windows Media Format SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4f1c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4f1c-114">Return value</span></span>

<span data-ttu-id="c4f1c-115">Gibt einen der folgenden **HRESULT** -Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="c4f1c-115">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="c4f1c-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c4f1c-116">Return code</span></span>                                                                                         | <span data-ttu-id="c4f1c-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4f1c-117">Description</span></span>                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="c4f1c-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c4f1c-118"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="c4f1c-119">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4f1c-119">The method succeeded.</span></span><br/>        |
| <dl> <span data-ttu-id="c4f1c-120"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="c4f1c-120"><dt>**E\_FAIL**</dt></span></span> </dl>              | <span data-ttu-id="c4f1c-121">Das Profil ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c4f1c-121">The profile is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="c4f1c-122"><dt>**VFW \_ E \_ falscher \_ Zustand**</dt></span><span class="sxs-lookup"><span data-stu-id="c4f1c-122"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="c4f1c-123">Das Filter Diagramm wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="c4f1c-123">The filter graph is stopped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c4f1c-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4f1c-124">Remarks</span></span>

<span data-ttu-id="c4f1c-125">Diese Methode ist mittlerweile veraltet, da Sie Windows Media-Format-SDK-Profile von Version 4,0 annimmt.</span><span class="sxs-lookup"><span data-stu-id="c4f1c-125">This method is now obsolete because it assumes version 4.0 Windows Media Format SDK profiles.</span></span> <span data-ttu-id="c4f1c-126">Verwenden Sie [**iconfigasfwriter:: Configure refilterusingprofile**](iconfigasfwriter-configurefilterusingprofile.md) oder [**iconfigasfwriter:: Configure refilterusingprofileguid**](iconfigasfwriter-configurefilterusingprofileguid.md), um den Filter für Profile der Version 7,0 und höher zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c4f1c-126">To configure the filter for version 7.0 and later profiles, use [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) or [**IConfigAsfWriter::ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c4f1c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4f1c-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="c4f1c-128">[**Iconfigasfwriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4f1c-128">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

