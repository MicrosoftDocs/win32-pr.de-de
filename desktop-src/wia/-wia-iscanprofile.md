---
description: Die iscanprofile-Schnittstelle stellt ein einzelnes Überprüfungs Profil dar und ermöglicht Anwendungen das Festlegen und Abrufen der Eigenschaften des Profils.
ms.assetid: 5cd76256-d64e-4934-8cc2-0a467c7e34a9
title: Iscanprofile-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile
api_type:
- COM
api_location:
- Scanprofiles.idl
ms.openlocfilehash: 2e02352eef16a9b899e4c635f11c5d10b3ab5113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359061"
---
# <a name="iscanprofile-interface"></a><span data-ttu-id="cae41-103">Iscanprofile-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cae41-103">IScanProfile interface</span></span>

<span data-ttu-id="cae41-104">Die **iscanprofile** -Schnittstelle stellt ein einzelnes Überprüfungs Profil dar und ermöglicht Anwendungen das Festlegen und Abrufen der Eigenschaften des Profils.</span><span class="sxs-lookup"><span data-stu-id="cae41-104">The **IScanProfile** interface represents a single scan profile and enables applications to set and get the properties of the profile.</span></span>

## <a name="members"></a><span data-ttu-id="cae41-105">Member</span><span class="sxs-lookup"><span data-stu-id="cae41-105">Members</span></span>

<span data-ttu-id="cae41-106">Die **iscanprofile** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cae41-106">The **IScanProfile** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="cae41-107">**Iscanprofile** verfügt auch über die folgenden Typen von Mitgliedern:</span><span class="sxs-lookup"><span data-stu-id="cae41-107">**IScanProfile** also has these types of members:</span></span>

-   [<span data-ttu-id="cae41-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="cae41-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cae41-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="cae41-109">Methods</span></span>

<span data-ttu-id="cae41-110">Die **iscanprofile** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="cae41-110">The **IScanProfile** interface has these methods.</span></span>



| <span data-ttu-id="cae41-111">Methode</span><span class="sxs-lookup"><span data-stu-id="cae41-111">Method</span></span>                                                     | <span data-ttu-id="cae41-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cae41-112">Description</span></span>                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cae41-113">**Getallpropids**</span><span class="sxs-lookup"><span data-stu-id="cae41-113">**GetAllPropIDs**</span></span>](-wia-iscanprofile-getallpropids.md)   | <span data-ttu-id="cae41-114">Ruft alle verfügbaren Eigenschaften-IDs in einem Profil ab.</span><span class="sxs-lookup"><span data-stu-id="cae41-114">Gets all available property IDs in a profile.</span></span><br/>                                                                                            |
| [<span data-ttu-id="cae41-115">**GetDeviceID**</span><span class="sxs-lookup"><span data-stu-id="cae41-115">**GetDeviceID**</span></span>](-wia-iscanprofile-getdeviceid.md)       | <span data-ttu-id="cae41-116">Gibt die ID des Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="cae41-116">Returns the ID of the device.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="cae41-117">**GetGUID**</span><span class="sxs-lookup"><span data-stu-id="cae41-117">**GetGUID**</span></span>](-wia-iscanprofile-getguid.md)               | <span data-ttu-id="cae41-118">Gibt die GUID des Profils zurück.</span><span class="sxs-lookup"><span data-stu-id="cae41-118">Returns the GUID of the profile.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="cae41-119">**GetItem**</span><span class="sxs-lookup"><span data-stu-id="cae41-119">**GetItem**</span></span>](-wia-iscanprofile-getitem.md)               | <span data-ttu-id="cae41-120">Ruft die GUID der Kategorie des WIA 2,0-Elements ab, dem das Profil zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cae41-120">Gets the GUID of the category of the WIA 2.0 item that the profile is associated with.</span></span><br/>                                                   |
| [<span data-ttu-id="cae41-121">**GetName**</span><span class="sxs-lookup"><span data-stu-id="cae41-121">**GetName**</span></span>](-wia-iscanprofile-getname.md)               | <span data-ttu-id="cae41-122">Ruft den anzeigen amen des Profils ab.</span><span class="sxs-lookup"><span data-stu-id="cae41-122">Gets the friendly name of the profile.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="cae41-123">**Getnumpropids**</span><span class="sxs-lookup"><span data-stu-id="cae41-123">**GetNumPropIDS**</span></span>](-wia-iscanprofile-getnumpropids.md)   | <span data-ttu-id="cae41-124">Ruft die Anzahl der Eigenschaften-IDs in einem Profil ab.</span><span class="sxs-lookup"><span data-stu-id="cae41-124">Gets the number of property IDs in a profile.</span></span><br/>                                                                                            |
| [<span data-ttu-id="cae41-125">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="cae41-125">**GetProperty**</span></span>](-wia-iscanprofile-getproperty.md)       | <span data-ttu-id="cae41-126">Ruft den Wert der angegebenen untergeordneten Eigenschaften im- `<Properties>` Element eines Scan Profils ab.</span><span class="sxs-lookup"><span data-stu-id="cae41-126">Gets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |
| [<span data-ttu-id="cae41-127">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="cae41-127">**IsDefault**</span></span>](-wia-iscanprofile-isdefault.md)           | <span data-ttu-id="cae41-128">Ruft einen Wert ab, der angibt, ob das Profil das Standard Überprüfungs Profil eines zugeordneten [**IWiaItem2**](-wia-iwiaitem2.md) -Geräts ist.</span><span class="sxs-lookup"><span data-stu-id="cae41-128">Gets a value that indicates whether the profile is the default scan profile of an associated [**IWiaItem2**](-wia-iwiaitem2.md) device.</span></span><br/> |
| [<span data-ttu-id="cae41-129">**RemoveProperty**</span><span class="sxs-lookup"><span data-stu-id="cae41-129">**RemoveProperty**</span></span>](-wia-iscanprofile-removeproperty.md) | <span data-ttu-id="cae41-130">Entfernt eine angegebene Liste von untergeordneten Eigenschaften im- `<Properties>` Element eines Scan Profils.</span><span class="sxs-lookup"><span data-stu-id="cae41-130">Removes a specified list of child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |
| [<span data-ttu-id="cae41-131">**Speichern**</span><span class="sxs-lookup"><span data-stu-id="cae41-131">**Save**</span></span>](-wia-iscanprofile-save.md)                     | <span data-ttu-id="cae41-132">Speichert Änderungen an einem Profil auf der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="cae41-132">Saves changes to a profile to disk.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="cae41-133">**-Element**</span><span class="sxs-lookup"><span data-stu-id="cae41-133">**SetItem**</span></span>](-wia-iscanprofile-setitem.md)               | <span data-ttu-id="cae41-134">Legt die GUID der Kategorie eines WIA-2,0-Elements fest, dem das Profil zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cae41-134">Sets the GUID of the category of WIA 2.0 item that the profile is associated with.</span></span><br/>                                                       |
| [<span data-ttu-id="cae41-135">**SetName**</span><span class="sxs-lookup"><span data-stu-id="cae41-135">**SetName**</span></span>](-wia-iscanprofile-setname.md)               | <span data-ttu-id="cae41-136">Legt den anzeigen amen des Profils fest.</span><span class="sxs-lookup"><span data-stu-id="cae41-136">Sets the friendly name of the profile.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="cae41-137">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="cae41-137">**SetProperty**</span></span>](-wia-iscanprofile-setproperty.md)       | <span data-ttu-id="cae41-138">Legt den Wert der angegebenen untergeordneten Eigenschaften im- `<Properties>` Element eines Scan Profils fest.</span><span class="sxs-lookup"><span data-stu-id="cae41-138">Sets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="cae41-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cae41-139">Remarks</span></span>

<span data-ttu-id="cae41-140">Jedes [**IWiaItem2**](-wia-iwiaitem2.md) -Gerät kann über ein Überprüfungs Profil verfügen.</span><span class="sxs-lookup"><span data-stu-id="cae41-140">Any [**IWiaItem2**](-wia-iwiaitem2.md) device can have a scan profile.</span></span> <span data-ttu-id="cae41-141">Allerdings können **IWiaItem2** Items von Typen, \_ die mit einer Kategorie \_ fertiggestellt \_ wurden, die Datei fertiggestellt \_ \_ haben</span><span class="sxs-lookup"><span data-stu-id="cae41-141">However, **IWiaItem2** items of types WIA\_CATEGORY\_FINISHED\_FILE and WIA\_CATEGORY\_ROOT cannot have profiles.</span></span>

<span data-ttu-id="cae41-142">Wenn ein Überprüfungs Profil mithilfe der [**iscanprofile:: Save**](-wia-iscanprofile-save.md) -Methode gespeichert wird, wird es als XML-Datei unter% User Profile% \\ Application Data \\ Microsoft \\ Document Center \\ userscanprofiles gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cae41-142">If a scan profile is saved using the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

<span data-ttu-id="cae41-143">Um eine Instanz eines **iscanprofile** -Objekts zu erstellen, verwenden Sie die [**iscanprofilemgr:: kreateprofile**](-wia-iscanprofilemgr-createprofile.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="cae41-143">To create an instance of an **IScanProfile** object, use the [**IScanProfileMgr::CreateProfile**](-wia-iscanprofilemgr-createprofile.md) method.</span></span> <span data-ttu-id="cae41-144">Um einen Verweis auf ein Überprüfungs Profil zu erhalten, das bereits auf dem Datenträger gespeichert wurde, verwenden Sie die [**iscanprofilemgr:: openprofile**](-wia-iscanprofilemgr-openprofile.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="cae41-144">To get a reference to a scan profile that has already been saved to disk, use the [**IScanProfileMgr::OpenProfile**](-wia-iscanprofilemgr-openprofile.md) method.</span></span>

<span data-ttu-id="cae41-145">Alle Scan Profile verfügen über die folgenden Elemente: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , und `<Properties>` .</span><span class="sxs-lookup"><span data-stu-id="cae41-145">All scan profiles have the following elements: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>`, and `<Properties>`.</span></span> <span data-ttu-id="cae41-146">Das Standardprofil eines Geräts weist auch ein- `<Default>` Element auf.</span><span class="sxs-lookup"><span data-stu-id="cae41-146">The default profile of a device also has a `<Default>` element.</span></span>

<span data-ttu-id="cae41-147">Das `<ProfileGUID>` -Element und das- `<DeviceID>` Element können nicht geändert werden, nachdem das Profil erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="cae41-147">The `<ProfileGUID>` and `<DeviceID>` elements cannot be changed after the profile is created.</span></span> <span data-ttu-id="cae41-148">Die Werte des `<ProfileName>` -Elements und des- `<WiaItem>` Elements können nach dem Erstellen des Profils geändert werden.</span><span class="sxs-lookup"><span data-stu-id="cae41-148">The values of the `<ProfileName>` element and the `<WiaItem>` element can be changed after the profile is created.</span></span> <span data-ttu-id="cae41-149">Das- `<Default>` Element kann hinzugefügt oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="cae41-149">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="cae41-150">Dies kann Programm gesteuert mit den Methoden [**iscanprofile:: SetName**](-wia-iscanprofile-setname.md), [**iscanprofile:: SetItem**](-wia-iscanprofile-setitem.md)und [**iscanprofilemgr:: SetDefault**](-wia-iscanprofilemgr-setdefault.md) erfolgen.</span><span class="sxs-lookup"><span data-stu-id="cae41-150">This can be done programatically with the [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md), and [**IScanProfileMgr::SetDefault**](-wia-iscanprofilemgr-setdefault.md) methods.</span></span> <span data-ttu-id="cae41-151">Diese Eigenschaften können auch von Benutzern über die [**iscanprofileui:: scanprofiledialog**](-wia-iscanprofileui-scanprofiledialog.md) -Methode geändert werden.</span><span class="sxs-lookup"><span data-stu-id="cae41-151">These properties can also be changed by users through the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="cae41-152">Das- `<Properties>` Element enthält untergeordnete Elemente `<Property>` .</span><span class="sxs-lookup"><span data-stu-id="cae41-152">The `<Properties>` element contains `<Property>` children.</span></span> <span data-ttu-id="cae41-153">Verwenden Sie diese, um dem Profil eine beliebige WIA 2,0-Element-oder-Geräte Eigenschaft hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cae41-153">Use these to add any WIA 2.0 item or device property to the profile.</span></span> <span data-ttu-id="cae41-154">Sie können auch Ihre eigenen Image-Erstell-untergeordneten Elemente entwickeln `<Property>` .</span><span class="sxs-lookup"><span data-stu-id="cae41-154">You can also develop your own image acquistion `<Property>` children.</span></span> <span data-ttu-id="cae41-155">Dadurch ist das Scan Profil Schema erweiterbar.</span><span class="sxs-lookup"><span data-stu-id="cae41-155">This makes the Scan Profile Schema extensible.</span></span> <span data-ttu-id="cae41-156">(Weitere Informationen zum Erweitern des Schemas finden Sie unter [Definieren von benutzerdefinierten Eigenschaften](-wia-defining-custom-properties.md), [**iscanprofile:: GetProperty**](-wia-iscanprofile-getproperty.md)und [**iscanprofile:: SetProperty**](-wia-iscanprofile-setproperty.md).)</span><span class="sxs-lookup"><span data-stu-id="cae41-156">(For more information about extending the schema, see [Defining Custom Properties](-wia-defining-custom-properties.md), [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md), and [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="cae41-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cae41-157">Requirements</span></span>



| <span data-ttu-id="cae41-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cae41-158">Requirement</span></span> | <span data-ttu-id="cae41-159">Wert</span><span class="sxs-lookup"><span data-stu-id="cae41-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cae41-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cae41-160">Minimum supported client</span></span><br/> | <span data-ttu-id="cae41-161">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cae41-161">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="cae41-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cae41-162">Minimum supported server</span></span><br/> | <span data-ttu-id="cae41-163">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cae41-163">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cae41-164">IDL</span><span class="sxs-lookup"><span data-stu-id="cae41-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cae41-165"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cae41-165"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cae41-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cae41-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae41-167">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="cae41-167">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="cae41-168">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="cae41-168">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
