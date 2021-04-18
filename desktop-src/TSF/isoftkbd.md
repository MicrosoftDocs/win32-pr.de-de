---
title: ISOFT kbd-Schnittstelle (Software-BDC. h)
description: Die isoftkbd-Schnittstelle wird von Anwendungen und Text Diensten verwendet, um eine weiche Tastatur zu implementieren.
ms.assetid: 804634bd-646e-459f-9fbb-cd6929b11fab
keywords:
- Iweichkbd Interface Text Services-Framework
- ISOFT kbd Interface Text Services-Framework, beschrieben
topic_type:
- apiref
api_name:
- ISoftKbd
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e046964616fc564aa2e0c3d0098ee2186cdaf8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339309"
---
# <a name="isoftkbd-interface"></a><span data-ttu-id="36721-105">ISOFT kbd-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="36721-105">ISoftKbd interface</span></span>

<span data-ttu-id="36721-106">Die **isoftkbd** -Schnittstelle wird von Anwendungen und Text Diensten verwendet, um eine weiche Tastatur zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="36721-106">The **ISoftKbd** interface is used by applications and text services to implement a soft keyboard.</span></span>

## <a name="members"></a><span data-ttu-id="36721-107">Member</span><span class="sxs-lookup"><span data-stu-id="36721-107">Members</span></span>

<span data-ttu-id="36721-108">Die **iSOFT kbd** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="36721-108">The **ISoftKbd** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="36721-109">**ISOFT kbd** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="36721-109">**ISoftKbd** also has these types of members:</span></span>

-   [<span data-ttu-id="36721-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="36721-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="36721-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="36721-111">Methods</span></span>

<span data-ttu-id="36721-112">Die **iSOFT kbd** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="36721-112">The **ISoftKbd** interface has these methods.</span></span>



| <span data-ttu-id="36721-113">Methode</span><span class="sxs-lookup"><span data-stu-id="36721-113">Method</span></span>                                                                                        | <span data-ttu-id="36721-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36721-114">Description</span></span>                                                                                                   |
|:----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36721-115">**Advisesoftkeyboarabventsink**</span><span class="sxs-lookup"><span data-stu-id="36721-115">**AdviseSoftKeyboardEventSink**</span></span>](isoftkbd-advisesoftkeyboardeventsink.md)                   | <span data-ttu-id="36721-116">Installiert eine weiche Tastaturereignis Senke, um onkeyselection-Benachrichtigungen von der Soft Tastatur zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="36721-116">Installs a soft keyboard event sink to handle OnKeySelection notifications from the soft keyboard.</span></span><br/> |
| [<span data-ttu-id="36721-117">**"Kreatesoftkeyboardlayoutfromresource"**</span><span class="sxs-lookup"><span data-stu-id="36721-117">**CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md) | <span data-ttu-id="36721-118">Erstellt ein weiches Tastaturlayout aus der angegebenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="36721-118">Creates a soft keyboard layout from the specified resource.</span></span><br/>                                        |
| [<span data-ttu-id="36721-119">**"Kreatesoftkeyboardlayoutfromxmlfile"**</span><span class="sxs-lookup"><span data-stu-id="36721-119">**CreateSoftKeyboardLayoutFromXMLFile**</span></span>](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)   | <span data-ttu-id="36721-120">Erstellt ein weiches Tastaturlayout aus der angegebenen XML-Datei.</span><span class="sxs-lookup"><span data-stu-id="36721-120">Creates a soft keyboard layout from the specified XML file.</span></span><br/>                                        |
| [<span data-ttu-id="36721-121">**"Kreatesoftkeyboardwindow"**</span><span class="sxs-lookup"><span data-stu-id="36721-121">**CreateSoftKeyboardWindow**</span></span>](isoftkbd-createsoftkeyboardwindow.md)                         | <span data-ttu-id="36721-122">Erstellt ein weiches Tastatur Fenster.</span><span class="sxs-lookup"><span data-stu-id="36721-122">Creates a soft keyboard window.</span></span><br/>                                                                    |
| [<span data-ttu-id="36721-123">**Destroysoftware keyboardwindow**</span><span class="sxs-lookup"><span data-stu-id="36721-123">**DestroySoftKeyboardWindow**</span></span>](isoftkbd-destroysoftkeyboardwindow.md)                       | <span data-ttu-id="36721-124">Zerstört ein weiches Tastatur Fenster.</span><span class="sxs-lookup"><span data-stu-id="36721-124">Destroys a soft keyboard window.</span></span><br/>                                                                   |
| [<span data-ttu-id="36721-125">**Enumsoft Keyboard**</span><span class="sxs-lookup"><span data-stu-id="36721-125">**EnumSoftKeyboard**</span></span>](isoftkbd-enumsoftkeyboard.md)                                         | <span data-ttu-id="36721-126">Listet die möglichen weichen Tastaturen auf, die die angegebene Sprache unterstützen.</span><span class="sxs-lookup"><span data-stu-id="36721-126">Enumerates the possible soft keyboards that support the specified language.</span></span><br/>                        |
| [<span data-ttu-id="36721-127">**Getsoft keyboardcolors**</span><span class="sxs-lookup"><span data-stu-id="36721-127">**GetSoftKeyboardColors**</span></span>](isoftkbd-getsoftkeyboardcolors.md)                               | <span data-ttu-id="36721-128">Ruft die weiche Tastatur Farbe ab, die dem angegebenen Farbtyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="36721-128">Retrieves the soft keyboard color corresponding to the supplied color type.</span></span><br/>                        |
| [<span data-ttu-id="36721-129">**Getsoft keyboardpossize**</span><span class="sxs-lookup"><span data-stu-id="36721-129">**GetSoftKeyboardPosSize**</span></span>](isoftkbd-getsoftkeyboardpossize.md)                             | <span data-ttu-id="36721-130">Ruft die Anfangsposition und die Größe einer Soft Tastatur ab.</span><span class="sxs-lookup"><span data-stu-id="36721-130">Retrieves the starting position and size of a soft keyboard.</span></span><br/>                                       |
| [<span data-ttu-id="36721-131">**Getsoftware keyboardtextfont**</span><span class="sxs-lookup"><span data-stu-id="36721-131">**GetSoftKeyboardTextFont**</span></span>](isoftkbd-getsoftkeyboardtextfont.md)                           | <span data-ttu-id="36721-132">Ruft die von einer Soft Tastatur verwendete Text Schriftart ab.</span><span class="sxs-lookup"><span data-stu-id="36721-132">Retrieves the text font used by a soft keyboard.</span></span><br/>                                                   |
| [<span data-ttu-id="36721-133">**Getsoft keyboardtypemode**</span><span class="sxs-lookup"><span data-stu-id="36721-133">**GetSoftKeyboardTypeMode**</span></span>](isoftkbd-getsoftkeyboardtypemode.md)                           | <span data-ttu-id="36721-134">Ruft den typmodus für eine weiche Tastatur ab.</span><span class="sxs-lookup"><span data-stu-id="36721-134">Retrieves the type mode for a soft keyboard.</span></span><br/>                                                       |
| [<span data-ttu-id="36721-135">**Initialisieren**</span><span class="sxs-lookup"><span data-stu-id="36721-135">**Initialize**</span></span>](isoftkbd-initialize.md)                                                     | <span data-ttu-id="36721-136">Initialisiert alle erforderlichen Felder für eine weiche Tastatur und generiert standardmäßige weiche Tastaturlayouts.</span><span class="sxs-lookup"><span data-stu-id="36721-136">Initializes all necessary fields for a soft keyboard and generates standard soft keyboard layouts.</span></span><br/> |
| [<span data-ttu-id="36721-137">**Selectsoft Keyboard**</span><span class="sxs-lookup"><span data-stu-id="36721-137">**SelectSoftKeyboard**</span></span>](isoftkbd-selectsoftkeyboard.md)                                     | <span data-ttu-id="36721-138">Wählt die angegebene weiche Tastatur aus.</span><span class="sxs-lookup"><span data-stu-id="36721-138">Selects the specified soft keyboard.</span></span><br/>                                                               |
| [<span data-ttu-id="36721-139">**Setkeyboardlabeltext**</span><span class="sxs-lookup"><span data-stu-id="36721-139">**SetKeyboardLabelText**</span></span>](isoftkbd-setkeyboardlabeltext.md)                                 | <span data-ttu-id="36721-140">Legt den Beschriftungs Text aus dem Layout für eine weiche Tastatur fest.</span><span class="sxs-lookup"><span data-stu-id="36721-140">Sets the label text from the layout for a soft keyboard.</span></span><br/>                                           |
| [<span data-ttu-id="36721-141">**Setkeyboardlabeltextkombination**</span><span class="sxs-lookup"><span data-stu-id="36721-141">**SetKeyboardLabelTextCombination**</span></span>](isoftkbd-setkeyboardlabeltextcombination.md)           | <span data-ttu-id="36721-142">Legt eine Kombination aus Bezeichnung und Text fest, mit der eine weiche Tastatur beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="36721-142">Sets a combination of label and text used to describe a soft keyboard.</span></span><br/>                             |
| [<span data-ttu-id="36721-143">**Setsoft keyboardcolors**</span><span class="sxs-lookup"><span data-stu-id="36721-143">**SetSoftKeyboardColors**</span></span>](isoftkbd-setsoftkeyboardcolors.md)                               | <span data-ttu-id="36721-144">Legt die weiche Tastatur Farbe fest, die dem angegebenen Farbtyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="36721-144">Sets the soft keyboard color corresponding to the supplied color type.</span></span><br/>                             |
| [<span data-ttu-id="36721-145">**Setsoft keyboardpossize**</span><span class="sxs-lookup"><span data-stu-id="36721-145">**SetSoftKeyboardPosSize**</span></span>](isoftkbd-setsoftkeyboardpossize.md)                             | <span data-ttu-id="36721-146">Legt die Anfangsposition und die Größe einer Soft Tastatur fest.</span><span class="sxs-lookup"><span data-stu-id="36721-146">Sets the starting position and size of a soft keyboard.</span></span><br/>                                            |
| [<span data-ttu-id="36721-147">**Setsoft keyboardtextfont**</span><span class="sxs-lookup"><span data-stu-id="36721-147">**SetSoftKeyboardTextFont**</span></span>](isoftkbd-setsoftkeyboardtextfont.md)                           | <span data-ttu-id="36721-148">Legt die von einer Soft Tastatur verwendete Text Schriftart fest.</span><span class="sxs-lookup"><span data-stu-id="36721-148">Sets the text font used by a soft keyboard.</span></span><br/>                                                        |
| [<span data-ttu-id="36721-149">**Setsoft keyboardtypemode**</span><span class="sxs-lookup"><span data-stu-id="36721-149">**SetSoftKeyboardTypeMode**</span></span>](isoftkbd-setsoftkeyboardtypemode.md)                           | <span data-ttu-id="36721-150">Legt den typmodus für eine weiche Tastatur fest.</span><span class="sxs-lookup"><span data-stu-id="36721-150">Sets the type mode for a soft keyboard.</span></span><br/>                                                            |
| [<span data-ttu-id="36721-151">**Showkeysforkeyscanmode**</span><span class="sxs-lookup"><span data-stu-id="36721-151">**ShowKeysForKeyScanMode**</span></span>](isoftkbd-showkeysforkeyscanmode.md)                             | <span data-ttu-id="36721-152">Zeigt die Schlüssel an, die für den Schlüssel Scan Modus für eine weiche Tastatur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36721-152">Displays the keys used for the key scan mode for a soft keyboard.</span></span><br/>                                  |
| [<span data-ttu-id="36721-153">**ShowSoft Keyboard**</span><span class="sxs-lookup"><span data-stu-id="36721-153">**ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)                                         | <span data-ttu-id="36721-154">Zeigt eine weiche Tastatur an.</span><span class="sxs-lookup"><span data-stu-id="36721-154">Displays a soft keyboard.</span></span><br/>                                                                          |
| [<span data-ttu-id="36721-155">**Unadvisesoftkeyboarabventsink**</span><span class="sxs-lookup"><span data-stu-id="36721-155">**UnadviseSoftKeyboardEventSink**</span></span>](isoftkbd-unadvisesoftkeyboardeventsink.md)               | <span data-ttu-id="36721-156">Entfernt eine weiche Tastaturereignis Senke.</span><span class="sxs-lookup"><span data-stu-id="36721-156">Removes a soft keyboard event sink.</span></span><br/>                                                                |



 

## <a name="requirements"></a><span data-ttu-id="36721-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36721-157">Requirements</span></span>



| <span data-ttu-id="36721-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36721-158">Requirement</span></span> | <span data-ttu-id="36721-159">Wert</span><span class="sxs-lookup"><span data-stu-id="36721-159">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36721-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36721-160">Minimum supported client</span></span><br/> | <span data-ttu-id="36721-161">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36721-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="36721-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36721-162">Minimum supported server</span></span><br/> | <span data-ttu-id="36721-163">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36721-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="36721-164">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="36721-164">Redistributable</span></span><br/>          | <span data-ttu-id="36721-165">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="36721-165">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="36721-166">Header</span><span class="sxs-lookup"><span data-stu-id="36721-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="36721-167"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="36721-167"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="36721-168">IDL</span><span class="sxs-lookup"><span data-stu-id="36721-168">IDL</span></span><br/>                      | <dl> <span data-ttu-id="36721-169"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="36721-169"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="36721-170">DLL</span><span class="sxs-lookup"><span data-stu-id="36721-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36721-171"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36721-171"><dt>Softkbd.dll</dt></span></span> </dl> |



 

