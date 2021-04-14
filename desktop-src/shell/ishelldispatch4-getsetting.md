---
description: Ruft eine globale shelleinstellung ab.
ms.assetid: b9b1542c-8e25-4966-b3df-13bfbd9b28aa
title: IShellDispatch4. GetSetting-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.GetSetting
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 755ee1d2bbd5026b1cc3ca165649e0fcb4ab20ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977985"
---
# <a name="ishelldispatch4getsetting-method"></a><span data-ttu-id="fd7ff-103">IShellDispatch4. GetSetting-Methode</span><span class="sxs-lookup"><span data-stu-id="fd7ff-103">IShellDispatch4.GetSetting method</span></span>

<span data-ttu-id="fd7ff-104">Ruft eine globale shelleinstellung ab.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-104">Retrieves a global Shell setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd7ff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd7ff-105">Syntax</span></span>


```JScript
retVal = IShellDispatch4.GetSetting(
  lSetting
)
```


```VB

IShellDispatch4.GetSetting( _
  ByVal lSetting As long _
) As VARIANT_BOOL
```





## <a name="parameters"></a><span data-ttu-id="fd7ff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd7ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd7ff-107">*lsetting* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd7ff-107">*lSetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd7ff-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="fd7ff-108">Type: **long**</span></span>

<span data-ttu-id="fd7ff-109">Ein-Wert, der die abzurufende aktuelle shelleinstellung angibt.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-109">A value that specifies the current Shell setting to retrieve.</span></span> <span data-ttu-id="fd7ff-110">In jedem-Befehl kann nur eine Einstellung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-110">Only one setting can be retrieved in each call.</span></span> <span data-ttu-id="fd7ff-111">Die folgenden Werte werden von dieser Methode erkannt.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-111">The following values are recognized by this method.</span></span>

<dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>

<span data-ttu-id="fd7ff-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ Autocheckselect** (0x00800000)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF\_AUTOCHECKSELECT** (0x00800000)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-113">**Windows Vista und** höher.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-113">**Windows Vista and later**.</span></span> <span data-ttu-id="fd7ff-114">Der Status der Option **Kontrollkästchen zum Auswählen von Elementen verwenden** .</span><span class="sxs-lookup"><span data-stu-id="fd7ff-114">The state of the **Use check boxes to select items** option.</span></span> <span data-ttu-id="fd7ff-115">Diese Option wird automatisch aktiviert, wenn für das System ein Stift Eingabegerät konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-115">This option is enabled automatically when the system has a pen input device configured.</span></span>

</dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>

<span data-ttu-id="fd7ff-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ Desktophtml** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF\_DESKTOPHTML** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-117">Not used.</span></span>

</dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>

<span data-ttu-id="fd7ff-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_ Dontprettypath** (0x00000800)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF\_DONTPRETTYPATH** (0x00000800)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-119">Der Status der Option **alle Großbuchstaben zulassen** .</span><span class="sxs-lookup"><span data-stu-id="fd7ff-119">The state of the **Allow all uppercase names** option.</span></span> <span data-ttu-id="fd7ff-120">Ab Windows Vista ist diese Ordner Option nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-120">As of Windows Vista, this folder option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>

<span data-ttu-id="fd7ff-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ Doubleclickinwebview** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF\_DOUBLECLICKINWEBVIEW** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-122">Der Zustand des **Doppelklick-Elements, um ein Element (mit einem Mausklick ausgewählt) zu öffnen** .</span><span class="sxs-lookup"><span data-stu-id="fd7ff-122">The state of the **Double-click to open an item (single-click to select)** option.</span></span>

</dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>

<span data-ttu-id="fd7ff-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF \_ Filter** (0x00010000 bis)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF\_FILTER** (0x00010000)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-124">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-124">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>

<span data-ttu-id="fd7ff-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_ Hiddenfileexts** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF\_HIDDENFILEEXTS** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-126">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-126">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>

<span data-ttu-id="fd7ff-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF \_ Hideicons** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF\_HIDEICONS** (0x00004000)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-128">Der Status der Symbol Anzeige in der Listenansicht von Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-128">The state of icon display in the Windows Explorer list view.</span></span> <span data-ttu-id="fd7ff-129">Wenn diese Option aktiviert ist, werden keine Symbole in der Listenansicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-129">If this option is active, no icons are displayed in the list view.</span></span>

</dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>

<span data-ttu-id="fd7ff-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF \_ Iconsonly** (0x01000000)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF\_ICONSONLY** (0x01000000)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-131">**Windows Vista und** höher.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-131">**Windows Vista and later**.</span></span> <span data-ttu-id="fd7ff-132">Der Status des anzeigen Amens wird in der Listenansicht von Windows-Explorer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-132">The state of display name display in the Windows Explorer list view.</span></span> <span data-ttu-id="fd7ff-133">Wenn diese Option aktiviert ist, werden Symbole in der Listenansicht angezeigt, aber keine anzeigen Amen.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-133">If this option is active, icons are displayed in the list view, but display names are not.</span></span>

</dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>

<span data-ttu-id="fd7ff-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_ Mapnetdrvbutton** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF\_MAPNETDRVBUTTON** (0x00001000)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-135">Der Status der **Schaltfläche Zuordnungs Netzwerklaufwerk anzeigen in der Symbol** leisten Option.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-135">The state of the **Show map network drive button in toolbar** option.</span></span> <span data-ttu-id="fd7ff-136">Ab Windows Vista steht diese Option nicht mehr zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-136">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>

<span data-ttu-id="fd7ff-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_ Noconfirmrecycle** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF\_NOCONFIRMRECYCLE** (0x00008000)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-138">Der Status der Option zum Anzeigen von **Lösch Dialogfeld** für den Papierkorb.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-138">The state of the Recycle Bin's **Display delete confirmation dialog** option.</span></span>

</dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>

<span data-ttu-id="fd7ff-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_ Nonetcrawlen** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF\_NONETCRAWLING** (0x00100000)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-140">Der Status der Option **Netzwerkordner und Drucker automatisch suchen** .</span><span class="sxs-lookup"><span data-stu-id="fd7ff-140">The state of the **Automatically search for network folders and printers** option.</span></span> <span data-ttu-id="fd7ff-141">Ab Windows Vista steht diese Option nicht mehr zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-141">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>

<span data-ttu-id="fd7ff-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_ Sepprocess** (0x00080000)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF\_SEPPROCESS** (0x00080000)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-143">Der Zustand der **Fenster "Ordner starten" in einer separaten Prozess** Option.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-143">The state of the **Launch folder windows in a separate process** option.</span></span>

</dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>

<span data-ttu-id="fd7ff-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ Serveradminui** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF\_SERVERADMINUI** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-145">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-145">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>

<span data-ttu-id="fd7ff-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_ Showallobjects** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF\_SHOWALLOBJECTS** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-147">Der Status der ausgeblendeten **Dateien und Ordner** .</span><span class="sxs-lookup"><span data-stu-id="fd7ff-147">The state of the **Hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>

<span data-ttu-id="fd7ff-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ ShowAttribCol** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF\_SHOWATTRIBCOL** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-149">Der Status der Option **Dateiattribute in Detail Ansicht anzeigen** .</span><span class="sxs-lookup"><span data-stu-id="fd7ff-149">The state of the **Show File Attributes in Detail View** option.</span></span> <span data-ttu-id="fd7ff-150">Ab Windows Vista steht diese Option nicht mehr zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-150">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>

<span data-ttu-id="fd7ff-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_ Showcompcolor** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF\_SHOWCOMPCOLOR** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-152">Der Status der Option **verschlüsselte oder komprimierte NTFS-Dateien in Farbe anzeigen** .</span><span class="sxs-lookup"><span data-stu-id="fd7ff-152">The state of the **Show encrypted or compressed NTFS files in color** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>

<span data-ttu-id="fd7ff-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_ Showextensions** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF\_SHOWEXTENSIONS** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-154">Der Status der Option **Erweiterungen für bekannte Dateitypen ausblenden** .</span><span class="sxs-lookup"><span data-stu-id="fd7ff-154">The state of the **Hide extensions for known file types** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>

<span data-ttu-id="fd7ff-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_ ShowInfoTip** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF\_SHOWINFOTIP** (0x00002000)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-156">Der Status der Option **Popup Beschreibung für Ordner und Desktop Elemente anzeigen** .</span><span class="sxs-lookup"><span data-stu-id="fd7ff-156">The state of the **Show pop-up description for folder and desktop items** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>

<span data-ttu-id="fd7ff-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_ Showstartpage** (0x00400000)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF\_SHOWSTARTPAGE** (0x00400000)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-158">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-158">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>

<span data-ttu-id="fd7ff-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ ShowSuperHidden** (0x00040000)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF\_SHOWSUPERHIDDEN** (0x00040000)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-160">Der Status der Option **geschützte Betriebssystemdateien ausblenden** .</span><span class="sxs-lookup"><span data-stu-id="fd7ff-160">The state of the **Hide protected operating system files** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>

<span data-ttu-id="fd7ff-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_ Showsysfiles** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF\_SHOWSYSFILES** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-162">Der Status der ausgeblendeten **Dateien und Ordner** .</span><span class="sxs-lookup"><span data-stu-id="fd7ff-162">The state of the **Hidden files and folders** option.</span></span> <span data-ttu-id="fd7ff-163">In Windows Vista und höher entspricht dies SSF \_ showallobjects.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-163">In Windows Vista and later, this is equivalent to SSF\_SHOWALLOBJECTS.</span></span> <span data-ttu-id="fd7ff-164">In Windows-Versionen vor Windows Vista bezog sich dieser Wert auf den Zustand der Option nicht ausgeblendete **Dateien und Ordner anzeigen** .</span><span class="sxs-lookup"><span data-stu-id="fd7ff-164">In versions of Windows before Windows Vista, this value referred to the state of the **Do not show hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>

<span data-ttu-id="fd7ff-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_ Showtypeoverlay** (0x02000000)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF\_SHOWTYPEOVERLAY** (0x02000000)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-166">**Windows Vista und** höher.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-166">**Windows Vista and later**.</span></span> <span data-ttu-id="fd7ff-167">Der Status des **Symbols für die Anzeige Datei in der Miniatur** Ansicht.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-167">The state of the **Display file icon on thumbnails** option.</span></span> <span data-ttu-id="fd7ff-168">Wenn diese Option aktiviert ist, wird eine Dateityp Überlagerung angewendet, wenn eine Datei eine Miniaturansicht bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-168">If this option is active, a file type overlay is applied when a file supplies a thumbnail representation.</span></span>

</dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>

<span data-ttu-id="fd7ff-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_ SortColumns** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF\_SORTCOLUMNS** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-170">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-170">Not used.</span></span>

</dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>

<span data-ttu-id="fd7ff-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ Startpanelon** (0x00200000)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF\_STARTPANELON** (0x00200000)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-172">Der Status der Anzeigeoption von Windows XP, die zwischen dem Windows XP-Stil und dem klassischen Stil auswählt.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-172">The state of the Windows XP display option, which selects between the Windows XP style and the classic style.</span></span> <span data-ttu-id="fd7ff-173">Ab Windows Vista steht diese Option nicht mehr zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-173">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>

<span data-ttu-id="fd7ff-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF \_ WebView** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF\_WEBVIEW** (0x00020000)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-175">Der Zustand der **Anzeige als webansichts Option**.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-175">The state of the **Display as a web view option**.</span></span> <span data-ttu-id="fd7ff-176">Ab Windows Vista steht diese Option nicht mehr zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-176">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>

<span data-ttu-id="fd7ff-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC** (0x00000400)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF\_WIN95CLASSIC** (0x00000400)</span></span>


</dt> <dd>

<span data-ttu-id="fd7ff-178">Der Status der **klassischen Stil** Option.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-178">The state of the **Classic Style** option.</span></span> <span data-ttu-id="fd7ff-179">Ab Windows Vista steht diese Option nicht mehr zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-179">As of Windows Vista, this option is no longer available.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd7ff-180">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd7ff-180">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="fd7ff-181">JScript</span><span class="sxs-lookup"><span data-stu-id="fd7ff-181">JScript</span></span>

<span data-ttu-id="fd7ff-182">Typ: \**Variant \_ bool \** _</span><span class="sxs-lookup"><span data-stu-id="fd7ff-182">Type: \**VARIANT\_BOOL\** _</span></span>

<span data-ttu-id="fd7ff-183">Legen Sie auf _ *true*\* fest, wenn die Einstellung vorhanden ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-183">Set to _ *true*\* if the setting exists; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="fd7ff-184">VB</span><span class="sxs-lookup"><span data-stu-id="fd7ff-184">VB</span></span>

<span data-ttu-id="fd7ff-185">Typ: \**Variant \_ bool \** _</span><span class="sxs-lookup"><span data-stu-id="fd7ff-185">Type: \**VARIANT\_BOOL\** _</span></span>

<span data-ttu-id="fd7ff-186">Legen Sie auf _ *true*\* fest, wenn die Einstellung vorhanden ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-186">Set to _ *true*\* if the setting exists; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="fd7ff-187">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd7ff-187">Examples</span></span>

<span data-ttu-id="fd7ff-188">In den folgenden Beispielen wird die Verwendung von **GetSetting** für JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fd7ff-188">The following examples show the use of **GetSetting** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="fd7ff-189">JScript</span><span class="sxs-lookup"><span data-stu-id="fd7ff-189">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnIShellDispatch4GetSettingJ()
    {
        var objIShellDispatch4 = new ActiveXObject("Shell.Application");
        var vReturn;
        var ssfSHOWALLOBJECTS = 1;

        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS);
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="fd7ff-190">VBScript</span><span class="sxs-lookup"><span data-stu-id="fd7ff-190">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellDispatch4GetSettingVB()
        dim objIShellDispatch4
        
        set objIShellDispatch4 = CreateObject("Shell.Application")
        if (not objIShellDispatch4 is nothing) then
            dim vReturn
            dim ssfSHOWALLOBJECTS
            
            ssfSHOWALLOBJECTS = 1
            vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
            alert(vReturn)
        end if
        set objIShellDispatch4 = nothing
    end function
</script>
```



<span data-ttu-id="fd7ff-191">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="fd7ff-191">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4GetSetting()
    Dim objIShellDispatch4 As Shell
    
    Set objIShellDispatch4 = New Shell
    If (Not objIShellDispatch4 Is Nothing) Then
        Dim vReturn As Variant
        Dim ssfSHOWALLOBJECTS As Long
        
        ssfSHOWALLOBJECTS = 1
        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
        Debug.Print vReturn
    End If
    Set objIShellDispatch4 = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="fd7ff-192">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-192">Requirements</span></span>



| <span data-ttu-id="fd7ff-193">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd7ff-193">Requirement</span></span> | <span data-ttu-id="fd7ff-194">Wert</span><span class="sxs-lookup"><span data-stu-id="fd7ff-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd7ff-195">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-195">Minimum supported client</span></span><br/> | <span data-ttu-id="fd7ff-196">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd7ff-196">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="fd7ff-197">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd7ff-197">Minimum supported server</span></span><br/> | <span data-ttu-id="fd7ff-198">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd7ff-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fd7ff-199">Header</span><span class="sxs-lookup"><span data-stu-id="fd7ff-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd7ff-200"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd7ff-200"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fd7ff-201">IDL</span><span class="sxs-lookup"><span data-stu-id="fd7ff-201">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fd7ff-202"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fd7ff-202"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fd7ff-203">DLL</span><span class="sxs-lookup"><span data-stu-id="fd7ff-203">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd7ff-204"><dt>Shell32.dll (Version 6,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="fd7ff-204"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




