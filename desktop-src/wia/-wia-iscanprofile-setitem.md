---
description: Legt die GUID der Kategorie des Windows-Abbild Erwerbs (WIA) 2,0-Elements fest, dem das Profil zugeordnet ist.
ms.assetid: e359abcb-b5d5-45a4-b650-2b278ba1ff6a
title: 'Iscanprofile:: SetItem-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: d4b20aae0740656b46dd26824947fc27513afcac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354533"
---
# <a name="iscanprofilesetitem-method"></a><span data-ttu-id="61d24-103">Iscanprofile:: SetItem-Methode</span><span class="sxs-lookup"><span data-stu-id="61d24-103">IScanProfile::SetItem method</span></span>

<span data-ttu-id="61d24-104">Legt die GUID der Kategorie des Windows-Abbild Erwerbs (WIA) 2,0-Elements fest, dem das Profil zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="61d24-104">Sets the GUID of the category of Windows Image Acquisition (WIA) 2.0 item that the profile is associated with.</span></span>

## <a name="syntax"></a><span data-ttu-id="61d24-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="61d24-105">Syntax</span></span>


```C++
HRESULT SetItem(
  [in] GUID guidCategory
);
```



## <a name="parameters"></a><span data-ttu-id="61d24-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="61d24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61d24-107">*guidcategory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61d24-107">*guidCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61d24-108">Typ: **GUID**</span><span class="sxs-lookup"><span data-stu-id="61d24-108">Type: **GUID**</span></span>

<span data-ttu-id="61d24-109">Die GUID der Kategorie des WIA 2,0-Elements.</span><span class="sxs-lookup"><span data-stu-id="61d24-109">The GUID of the category of the WIA 2.0 item.</span></span> <span data-ttu-id="61d24-110">Dabei muss es sich um eine der WIA- \_ IPA- \_ Element Kategorie- \_ Konstanten handeln.</span><span class="sxs-lookup"><span data-stu-id="61d24-110">This must be one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61d24-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61d24-111">Return value</span></span>

<span data-ttu-id="61d24-112">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="61d24-112">Type: **HRESULT**</span></span>

<span data-ttu-id="61d24-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="61d24-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="61d24-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="61d24-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="61d24-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61d24-115">Remarks</span></span>

<span data-ttu-id="61d24-116">Benutzer können die Kategorie mit der [**scanprofiledialog**](-wia-iscanprofileui-scanprofiledialog.md) -Methode ändern.</span><span class="sxs-lookup"><span data-stu-id="61d24-116">Users can change the category with the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="61d24-117">Änderungen an einem Profil werden erst auf dem Datenträger gespeichert, wenn die Anwendung die [**iscanprofile:: Save**](-wia-iscanprofile-save.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="61d24-117">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="61d24-118">Wenn zwei Anwendungen Überprüfungs Profil Objekte aus derselben XML-Datei erstellen und jede Anwendung Änderungen in das zugehörige Objekt schreibt, werden nur die Änderungen, die von der Anwendung vorgenommen werden, die [**iscanprofile:: Save**](-wia-iscanprofile-save.md) Last aufruft, auf dem Datenträger gespeichert.</span><span class="sxs-lookup"><span data-stu-id="61d24-118">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="61d24-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61d24-119">Requirements</span></span>



| <span data-ttu-id="61d24-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61d24-120">Requirement</span></span> | <span data-ttu-id="61d24-121">Wert</span><span class="sxs-lookup"><span data-stu-id="61d24-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="61d24-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61d24-122">Minimum supported client</span></span><br/> | <span data-ttu-id="61d24-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61d24-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="61d24-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61d24-124">Minimum supported server</span></span><br/> | <span data-ttu-id="61d24-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61d24-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61d24-126">Header</span><span class="sxs-lookup"><span data-stu-id="61d24-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="61d24-127"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="61d24-127"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="61d24-128">IDL</span><span class="sxs-lookup"><span data-stu-id="61d24-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="61d24-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="61d24-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61d24-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61d24-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61d24-131">**Iscanprofile**</span><span class="sxs-lookup"><span data-stu-id="61d24-131">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="61d24-132">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="61d24-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




