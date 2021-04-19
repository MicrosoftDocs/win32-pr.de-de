---
description: Die iscanprofilemgr-Schnittstelle stellt Methoden zum Erstellen, öffnen, löschen und Verwalten von Scan Profilen bereit.
ms.assetid: f57a71b7-750c-42a8-be73-229f0145d9d5
title: Iscanprofilemgr-Schnittstelle (scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 9f0762befdda272b91451dcca67c3f9560ad354e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348226"
---
# <a name="iscanprofilemgr-interface"></a><span data-ttu-id="55a55-103">Iscanprofilemgr-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="55a55-103">IScanProfileMgr interface</span></span>

<span data-ttu-id="55a55-104">Die **iscanprofilemgr** -Schnittstelle stellt Methoden zum Erstellen, öffnen, löschen und Verwalten von Scan Profilen bereit.</span><span class="sxs-lookup"><span data-stu-id="55a55-104">The **IScanProfileMgr** interface provides methods for creating, opening, deleting, and managing scan profiles.</span></span>

## <a name="members"></a><span data-ttu-id="55a55-105">Member</span><span class="sxs-lookup"><span data-stu-id="55a55-105">Members</span></span>

<span data-ttu-id="55a55-106">Die **iscanprofilemgr** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="55a55-106">The **IScanProfileMgr** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="55a55-107">**Iscanprofilemgr** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="55a55-107">**IScanProfileMgr** also has these types of members:</span></span>

-   [<span data-ttu-id="55a55-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="55a55-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="55a55-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="55a55-109">Methods</span></span>

<span data-ttu-id="55a55-110">Die **iscanprofilemgr** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="55a55-110">The **IScanProfileMgr** interface has these methods.</span></span>



| <span data-ttu-id="55a55-111">Methode</span><span class="sxs-lookup"><span data-stu-id="55a55-111">Method</span></span>                                                                              | <span data-ttu-id="55a55-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55a55-112">Description</span></span>                                                                                                            |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55a55-113">**"Kreateprofile"**</span><span class="sxs-lookup"><span data-stu-id="55a55-113">**CreateProfile**</span></span>](-wia-iscanprofilemgr-createprofile.md)                         | <span data-ttu-id="55a55-114">Erstellt ein leeres Überprüfungs Profil und ordnet es einem Scanner oder einem anderen WIA-2,0-Element zu.</span><span class="sxs-lookup"><span data-stu-id="55a55-114">Creates an empty scan profile and associates it with a scanner or other WIA 2.0 item.</span></span><br/>                       |
| [<span data-ttu-id="55a55-115">**Deleteallprofiles**</span><span class="sxs-lookup"><span data-stu-id="55a55-115">**DeleteAllProfiles**</span></span>](-wia-iscanprofilemgr-deleteallprofiles.md)                 | <span data-ttu-id="55a55-116">Löscht alle Überprüfungs Profile, die dem angegebenen Gerät zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="55a55-116">Deletes all the scan profiles associated with the specified device.</span></span><br/>                                         |
| [<span data-ttu-id="55a55-117">**Deleteallprofilesforuser**</span><span class="sxs-lookup"><span data-stu-id="55a55-117">**DeleteAllProfilesForUser**</span></span>](-wia-iscanprofilemgr-deleteallprofilesforuser.md)   | <span data-ttu-id="55a55-118">Löscht alle Überprüfungs Profile, die für den Benutzer in dem System verfügbar sind, unter dem Ihre Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55a55-118">Deletes all the scan profiles available for the user in the system that your application is running under.</span></span> <br/> |
| [<span data-ttu-id="55a55-119">**DeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="55a55-119">**DeleteProfile**</span></span>](-wia-iscanprofilemgr-deleteprofile.md)                         | <span data-ttu-id="55a55-120">Löscht das angegebene Überprüfungs Profil.</span><span class="sxs-lookup"><span data-stu-id="55a55-120">Deletes the specified scan profile.</span></span><br/>                                                                         |
| [<span data-ttu-id="55a55-121">**Getdefaultprofile**</span><span class="sxs-lookup"><span data-stu-id="55a55-121">**GetDefaultProfile**</span></span>](-wia-iscanprofilemgr-getdefaultprofile.md)                 | <span data-ttu-id="55a55-122">Ruft das Standard Überprüfungs Profil ab.</span><span class="sxs-lookup"><span data-stu-id="55a55-122">Gets the default scan profile.</span></span><br/>                                                                              |
| [<span data-ttu-id="55a55-123">**Getnumprofiles**</span><span class="sxs-lookup"><span data-stu-id="55a55-123">**GetNumProfiles**</span></span>](-wia-iscanprofilemgr-getnumprofiles.md)                       | <span data-ttu-id="55a55-124">Ruft die Anzahl der Überprüfungs Profile ab, die für den Benutzer im System erstellt wurden, unter dem Ihre Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55a55-124">Gets the number of scan profiles created for the user in the system that your application is running under.</span></span><br/> |
| [<span data-ttu-id="55a55-125">**Getnumprofilesforde viceid**</span><span class="sxs-lookup"><span data-stu-id="55a55-125">**GetNumProfilesforDeviceID**</span></span>](-wia-iscanprofilemgr-getnumprofilesfordeviceid.md) | <span data-ttu-id="55a55-126">Ruft die Anzahl der Scan Profile für das Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="55a55-126">Gets the number of scan profiles for the device.</span></span><br/>                                                            |
| [<span data-ttu-id="55a55-127">**Getprofiles**</span><span class="sxs-lookup"><span data-stu-id="55a55-127">**GetProfiles**</span></span>](-wia-iscanprofilemgr-getprofiles.md)                             | <span data-ttu-id="55a55-128">Ruft alle Überprüfungs Profile ab, die für den Benutzer im System verfügbar sind, unter dem Ihre Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55a55-128">Gets all the scan profiles available for the user in the system that your application is running under.</span></span><br/>     |
| [<span data-ttu-id="55a55-129">**Getprofilesforde viceid**</span><span class="sxs-lookup"><span data-stu-id="55a55-129">**GetProfilesforDeviceID**</span></span>](-wia-iscanprofilemgr-getprofilesfordeviceid.md)       | <span data-ttu-id="55a55-130">Ruft alle einem Gerät zugeordneten Scan Profile ab.</span><span class="sxs-lookup"><span data-stu-id="55a55-130">Gets all the scan profiles associated with a device.</span></span><br/>                                                        |
| [<span data-ttu-id="55a55-131">**Openprofile**</span><span class="sxs-lookup"><span data-stu-id="55a55-131">**OpenProfile**</span></span>](-wia-iscanprofilemgr-openprofile.md)                             | <span data-ttu-id="55a55-132">Öffnet ein Überprüfungs Profil, das als XML-Datei auf einem Datenträger gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="55a55-132">Opens a scan profile that has been saved to disk as an XML file.</span></span><br/>                                            |
| [<span data-ttu-id="55a55-133">**Aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="55a55-133">**Refresh**</span></span>](-wia-iscanprofilemgr-refresh.md)                                     | <span data-ttu-id="55a55-134">Listet alle Scan Profile im System erneut auf.</span><span class="sxs-lookup"><span data-stu-id="55a55-134">Re-enumerates all the scan profiles in the system.</span></span><br/>                                                          |
| [<span data-ttu-id="55a55-135">**SetDefault**</span><span class="sxs-lookup"><span data-stu-id="55a55-135">**SetDefault**</span></span>](-wia-iscanprofilemgr-setdefault.md)                               | <span data-ttu-id="55a55-136">Legt das angegebene Überprüfungs Profil als Standardprofil fest.</span><span class="sxs-lookup"><span data-stu-id="55a55-136">Sets the specified scan profile as the default profile.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="55a55-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55a55-137">Remarks</span></span>

<span data-ttu-id="55a55-138">Verwenden Sie zum Erstellen eines **iscanprofilemgr** -Objekts die [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode mit den folgenden Parametern:</span><span class="sxs-lookup"><span data-stu-id="55a55-138">To create an **IScanProfileMgr** object, use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method with the following parameters:</span></span>

``` syntax
CoCreateInstance(CLSID_ScanProfileMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IScanProfileMgr, ppv)
```

<span data-ttu-id="55a55-139">Wenn ein Überprüfungs Profil mithilfe der [**iscanprofile:: Save**](-wia-iscanprofile-save.md) -Methode gespeichert wird, wird es als XML-Datei unter% User Profile% \\ Application Data \\ Microsoft \\ Document Center \\ userscanprofiles gespeichert.</span><span class="sxs-lookup"><span data-stu-id="55a55-139">If a scan profile is saved using the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="55a55-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55a55-140">Requirements</span></span>



| <span data-ttu-id="55a55-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55a55-141">Requirement</span></span> | <span data-ttu-id="55a55-142">Wert</span><span class="sxs-lookup"><span data-stu-id="55a55-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="55a55-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55a55-143">Minimum supported client</span></span><br/> | <span data-ttu-id="55a55-144">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55a55-144">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="55a55-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55a55-145">Minimum supported server</span></span><br/> | <span data-ttu-id="55a55-146">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55a55-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55a55-147">Header</span><span class="sxs-lookup"><span data-stu-id="55a55-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="55a55-148"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="55a55-148"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="55a55-149">IDL</span><span class="sxs-lookup"><span data-stu-id="55a55-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55a55-150"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="55a55-150"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55a55-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55a55-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a55-152">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="55a55-152">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="55a55-153">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="55a55-153">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
