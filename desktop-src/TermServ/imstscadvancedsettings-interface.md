---
title: Imstscadvancedsettings-Schnittstelle
description: Enthält Methoden zum Abrufen und Festlegen von Eigenschaften, die das Zwischenspeichern von Bitmaps, die Komprimierung und die Umleitung von Druckern und Zwischenablage aktivieren
ms.assetid: 3385e843-be05-4801-8d59-6395d95686b1
ms.tgt_platform: multiple
keywords:
- Imstscadvancedsettings-Schnittstelle Remotedesktopdienste
- Imstscadvancedsettings-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4d55df30c940ecc5a5515f13c05a285507499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341608"
---
# <a name="imstscadvancedsettings-interface"></a><span data-ttu-id="47a95-105">Imstscadvancedsettings-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="47a95-105">IMsTscAdvancedSettings interface</span></span>

<span data-ttu-id="47a95-106">Enthält Methoden zum Abrufen und Festlegen von Eigenschaften, die das Zwischenspeichern von Bitmaps, die Komprimierung und die Umleitung von Druckern und Zwischenablage aktivieren</span><span class="sxs-lookup"><span data-stu-id="47a95-106">Includes methods to retrieve and set properties that enable bitmap caching, compression, and printer and clipboard redirection.</span></span> <span data-ttu-id="47a95-107">Sie können auch Namen von Client-DLLs für virtuelle Kanäle angeben.</span><span class="sxs-lookup"><span data-stu-id="47a95-107">You can also specify names of virtual channel client DLLs.</span></span>

<span data-ttu-id="47a95-108">Sie erhalten eine Instanz dieser Schnittstelle, indem Sie die [**imstscax:: advancedsettings**](imstscax-advancedsettings.md) -Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="47a95-108">You obtain an instance of this interface by using the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="47a95-109">Member</span><span class="sxs-lookup"><span data-stu-id="47a95-109">Members</span></span>

<span data-ttu-id="47a95-110">Die **imstscadvancedsettings** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="47a95-110">The **IMsTscAdvancedSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="47a95-111">**Imstscadvancedsettings** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="47a95-111">**IMsTscAdvancedSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="47a95-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47a95-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47a95-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47a95-113">Properties</span></span>

<span data-ttu-id="47a95-114">Die **imstscadvancedsettings** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="47a95-114">The **IMsTscAdvancedSettings** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="47a95-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="47a95-115">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="47a95-116">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="47a95-116">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="47a95-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47a95-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47a95-118"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowbackgroundinput</strong></a></span><span class="sxs-lookup"><span data-stu-id="47a95-118"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-119">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47a95-119">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-120">Gibt an, ob der Hintergrund Eingabemodus aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="47a95-120">Specifies whether background input mode is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47a95-121"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>Bitmapperistenz</strong></a></span><span class="sxs-lookup"><span data-stu-id="47a95-121"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47a95-122">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-123">Gibt an, ob bitmapcaching aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="47a95-123">Specifies whether bitmap caching is enabled.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="47a95-124">Der Rechtschreibfehler im Namen der Eigenschaft ist in der veröffentlichten Version des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="47a95-124">The spelling error in the name of the property is in the released version of the control.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47a95-125"><a href="imstscadvancedsettings-compress.md"><strong>Komprimieren</strong></a></span><span class="sxs-lookup"><span data-stu-id="47a95-125"><a href="imstscadvancedsettings-compress.md"><strong>Compress</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-126">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47a95-126">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-127">Gibt an, ob die Komprimierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="47a95-127">Specifies whether compression is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47a95-128"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>Containerhandledfullscreen</strong></a></span><span class="sxs-lookup"><span data-stu-id="47a95-128"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-129">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47a95-129">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-130">Gibt an, ob der vom Container behandelte Vollbildmodus aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="47a95-130">Specifies whether the container-handled full-screen mode is enabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47a95-131"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>Disablerdpdr</strong></a></span><span class="sxs-lookup"><span data-stu-id="47a95-131"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-132">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="47a95-132">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-133">Gibt an, ob die Umleitung von Drucker und Zwischenablage aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="47a95-133">Specifies whether printer and clipboard redirection is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47a95-134"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="47a95-134"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-135">Lesegeschützt</span><span class="sxs-lookup"><span data-stu-id="47a95-135">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-136">Gibt den Namen der Datei mit den Symbol Daten an, auf die zugegriffen wird, wenn der Client im Vollbildmodus angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="47a95-136">Specifies the name of the file containing icon data that will be accessed when displaying the client in full-screen mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47a95-137"><a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a></span><span class="sxs-lookup"><span data-stu-id="47a95-137"><a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-138">Lesegeschützt</span><span class="sxs-lookup"><span data-stu-id="47a95-138">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-139">Gibt den Index des Symbols in der aktuellen Symbol Datei an.</span><span class="sxs-lookup"><span data-stu-id="47a95-139">Specifies the index of the icon within the current icon file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="47a95-140"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>Keyboardlayoutstr</strong></a></span><span class="sxs-lookup"><span data-stu-id="47a95-140"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-141">Lesegeschützt</span><span class="sxs-lookup"><span data-stu-id="47a95-141">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-142">Gibt den Namen des aktiven Eingabe Gebiets Schema Bezeichners (früher als Tastaturlayout bezeichnet) für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="47a95-142">Specifies the name of the active input locale identifier (formerly called the keyboard layout) to use for the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="47a95-143"><a href="imstscadvancedsettings-plugindlls.md"><strong>Plugindlls</strong></a></span><span class="sxs-lookup"><span data-stu-id="47a95-143"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-144">Lesegeschützt</span><span class="sxs-lookup"><span data-stu-id="47a95-144">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="47a95-145">Gibt die Namen der zu ladenden Virtual Channel-Client-DLLs an.</span><span class="sxs-lookup"><span data-stu-id="47a95-145">Specifies the names of virtual channel client DLLs to be loaded.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="47a95-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47a95-146">Remarks</span></span>

<span data-ttu-id="47a95-147">Diese Schnittstelle wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:</span><span class="sxs-lookup"><span data-stu-id="47a95-147">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="47a95-148">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="47a95-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
-   [<span data-ttu-id="47a95-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="47a95-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
-   [<span data-ttu-id="47a95-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="47a95-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
-   [<span data-ttu-id="47a95-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="47a95-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="47a95-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="47a95-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="47a95-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="47a95-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="47a95-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="47a95-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="47a95-155">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="47a95-155">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="47a95-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47a95-156">Requirements</span></span>



| <span data-ttu-id="47a95-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47a95-157">Requirement</span></span> | <span data-ttu-id="47a95-158">Wert</span><span class="sxs-lookup"><span data-stu-id="47a95-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="47a95-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47a95-159">Minimum supported client</span></span><br/> | <span data-ttu-id="47a95-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47a95-160">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="47a95-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47a95-161">Minimum supported server</span></span><br/> | <span data-ttu-id="47a95-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47a95-162">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="47a95-163">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="47a95-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="47a95-164"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47a95-164"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="47a95-165">DLL</span><span class="sxs-lookup"><span data-stu-id="47a95-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47a95-166"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47a95-166"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="47a95-167">IID</span><span class="sxs-lookup"><span data-stu-id="47a95-167">IID</span></span><br/>                      | <span data-ttu-id="47a95-168">IID \_ imstscadvancedsettings ist als 809945cc-4b3b-4a92-a6b0-DBF 9b5s2ef2d definiert.</span><span class="sxs-lookup"><span data-stu-id="47a95-168">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47a95-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47a95-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47a95-170">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="47a95-170">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="47a95-171">Remotedesktop-Webverbindung Referenz</span><span class="sxs-lookup"><span data-stu-id="47a95-171">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

