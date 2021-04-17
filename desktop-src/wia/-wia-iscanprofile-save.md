---
description: Speichert Änderungen an einem Profil auf der Festplatte.
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: 'Iscanprofile:: Save-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.Save
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 6d4787380344a7bf8adb70f4cb5a3eaacdea403a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527086"
---
# <a name="iscanprofilesave-method"></a><span data-ttu-id="bc4e0-103">Iscanprofile:: Save-Methode</span><span class="sxs-lookup"><span data-stu-id="bc4e0-103">IScanProfile::Save method</span></span>

<span data-ttu-id="bc4e0-104">Speichert Änderungen an einem Profil auf der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="bc4e0-104">Saves changes to a profile to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc4e0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc4e0-105">Syntax</span></span>


```C++
HRESULT Save();
```



## <a name="parameters"></a><span data-ttu-id="bc4e0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc4e0-106">Parameters</span></span>

<span data-ttu-id="bc4e0-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bc4e0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc4e0-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc4e0-108">Return value</span></span>

<span data-ttu-id="bc4e0-109">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bc4e0-109">Type: **HRESULT**</span></span>

<span data-ttu-id="bc4e0-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="bc4e0-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bc4e0-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bc4e0-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc4e0-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc4e0-112">Remarks</span></span>

<span data-ttu-id="bc4e0-113">Bei einem gespeicherten Überprüfungs Profil handelt es sich um eine XML-Datei, die unter% User Profile% \\ Application Data \\ Microsoft \\ Document Center \\ userscanprofiles gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="bc4e0-113">A saved scan profile is an XML file stored at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

<span data-ttu-id="bc4e0-114">Wenn mehr als ein Prozess in das [**iscanprofile**](-wia-iscanprofile.md) -Objekt schreibt, ist das Objekt, das **iscanprofile:: Save** Last aufruft, der einzige Prozess, dessen Änderungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="bc4e0-114">If more than one process writes to the [**IScanProfile**](-wia-iscanprofile.md) object, the one that calls **IScanProfile::Save** last is the only process whose changes are saved.</span></span>

<span data-ttu-id="bc4e0-115">Die **iscanprofile:: Save** -Methode überprüft das Profil vor dem Speichern.</span><span class="sxs-lookup"><span data-stu-id="bc4e0-115">The **IScanProfile::Save** method validates the profile before saving.</span></span> <span data-ttu-id="bc4e0-116">Das Profil wird immer als gültig angesehen, es sei denn, die Kategorie des Windows-Abbild Erwerbs (WIA) 2,0-Elements, das mit dem Profil verknüpft ist, ist entweder eine Kategorie mit einem \_ \_ Flatbed oder eine \_ Kategorie- \_ Feed</span><span class="sxs-lookup"><span data-stu-id="bc4e0-116">The profile is always considered valid unless the category of the Windows Image Acquisition (WIA) 2.0 item associated with the profile is either WIA\_CATEGORY\_FLATBED or WIA\_CATEGORY\_FEEDER.</span></span> <span data-ttu-id="bc4e0-117">Wenn es sich bei der Kategorie um eine Kategorie vom Typ " \_ Kategorie für \_ flatgrades" oder um einen \_ kategorieanleger handelt \_ , müssen die folgenden Eigenschaften für das Element gültig sein, wenn die Eigenschaften im Profil enthalten sind:</span><span class="sxs-lookup"><span data-stu-id="bc4e0-117">If the category is WIA\_CATEGORY\_FLATBED or WIA\_CATEGORY\_FEEDER, the following properties must be valid for the item, if the properties are contained in the profile:</span></span>

<span data-ttu-id="bc4e0-118">Helligkeit der WIA- \_ IPS \_</span><span class="sxs-lookup"><span data-stu-id="bc4e0-118">WIA\_IPS\_BRIGHTNESS</span></span>

<span data-ttu-id="bc4e0-119">Kontrast zwischen WIA- \_ IPS \_</span><span class="sxs-lookup"><span data-stu-id="bc4e0-119">WIA\_IPS\_CONTRAST</span></span>

<span data-ttu-id="bc4e0-120">WIA \_ IPA- \_ DataType</span><span class="sxs-lookup"><span data-stu-id="bc4e0-120">WIA\_IPA\_DATATYPE</span></span>

<span data-ttu-id="bc4e0-121">WIA- \_ IPS- \_ xres</span><span class="sxs-lookup"><span data-stu-id="bc4e0-121">WIA\_IPS\_XRES</span></span>

<span data-ttu-id="bc4e0-122">WIA \_ IPA- \_ Format</span><span class="sxs-lookup"><span data-stu-id="bc4e0-122">WIA\_IPA\_FORMAT</span></span>

<span data-ttu-id="bc4e0-123">Wenn es sich bei der Kategorie um einen "a category"-Wert handelt \_ \_ , muss die Eigenschaft "WIA \_ IPS page size" ggf \_ \_ . gültig sein, wenn Sie im Profil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bc4e0-123">In addition, if the category is WIA\_CATEGORY\_FEEDER, the WIA\_IPS\_PAGE\_SIZE property must be valid, if it is present in the profile.</span></span> <span data-ttu-id="bc4e0-124">Weitere Informationen zu diesen Eigenschaften finden Sie unter [**Scanner WIA Item Property Konstanten**](-wia-wiaitempropscanneritem.md).</span><span class="sxs-lookup"><span data-stu-id="bc4e0-124">For more information about these properties, see [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc4e0-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc4e0-125">Requirements</span></span>



| <span data-ttu-id="bc4e0-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc4e0-126">Requirement</span></span> | <span data-ttu-id="bc4e0-127">Wert</span><span class="sxs-lookup"><span data-stu-id="bc4e0-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc4e0-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc4e0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bc4e0-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc4e0-129">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="bc4e0-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc4e0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bc4e0-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc4e0-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bc4e0-132">Header</span><span class="sxs-lookup"><span data-stu-id="bc4e0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc4e0-133"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc4e0-133"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="bc4e0-134">IDL</span><span class="sxs-lookup"><span data-stu-id="bc4e0-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bc4e0-135"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bc4e0-135"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc4e0-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc4e0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc4e0-137">**Iscanprofile**</span><span class="sxs-lookup"><span data-stu-id="bc4e0-137">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="bc4e0-138">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="bc4e0-138">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




