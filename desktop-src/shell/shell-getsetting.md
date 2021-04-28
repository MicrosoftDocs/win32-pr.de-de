---
description: 'Shell.GetSetting-Methode: Ruft eine globale Shelleinstellung ab.'
ms.assetid: 3E8C7C6A-5696-4756-B4BF-902FA2420AE9
title: Shell.GetSetting-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSetting
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: dc8fe6277208808ad5f5b182f3eee416daf4a5d0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083738"
---
# <a name="shellgetsetting-method"></a><span data-ttu-id="963b5-103">Shell.GetSetting-Methode</span><span class="sxs-lookup"><span data-stu-id="963b5-103">Shell.GetSetting method</span></span>

<span data-ttu-id="963b5-104">Ruft eine globale Shelleinstellung ab.</span><span class="sxs-lookup"><span data-stu-id="963b5-104">Retrieves a global Shell setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="963b5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="963b5-105">Syntax</span></span>


```JScript
retVal = Shell.GetSetting(
  lSetting
)
```


```VB

Shell.GetSetting( _
  ByVal lSetting As long _
) As VARIANT_BOOL
```





## <a name="parameters"></a><span data-ttu-id="963b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="963b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="963b5-107">*lSetting* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="963b5-107">*lSetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="963b5-108">Typ: **long**</span><span class="sxs-lookup"><span data-stu-id="963b5-108">Type: **long**</span></span>

<span data-ttu-id="963b5-109">Ein -Wert, der die aktuelle abzurufende Shelleinstellung angibt.</span><span class="sxs-lookup"><span data-stu-id="963b5-109">A value that specifies the current Shell setting to retrieve.</span></span> <span data-ttu-id="963b5-110">In jedem Aufruf kann nur eine Einstellung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="963b5-110">Only one setting can be retrieved in each call.</span></span> <span data-ttu-id="963b5-111">Die folgenden Werte werden von dieser Methode erkannt.</span><span class="sxs-lookup"><span data-stu-id="963b5-111">The following values are recognized by this method.</span></span>

<dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>

<span data-ttu-id="963b5-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ AUTOCHECKSELECT** (0x00800000)</span><span class="sxs-lookup"><span data-stu-id="963b5-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF\_AUTOCHECKSELECT** (0x00800000)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-113">**Windows Vista und höher.**</span><span class="sxs-lookup"><span data-stu-id="963b5-113">**Windows Vista and later**.</span></span> <span data-ttu-id="963b5-114">Der Status der Option **Elemente mithilfe der Kontrollkästchen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="963b5-114">The state of the **Use check boxes to select items** option.</span></span> <span data-ttu-id="963b5-115">Diese Option wird automatisch aktiviert, wenn für das System ein Stifteingabegerät konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="963b5-115">This option is enabled automatically when the system has a pen input device configured.</span></span>

</dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>

<span data-ttu-id="963b5-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ DESKTOPHTML** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="963b5-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF\_DESKTOPHTML** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="963b5-117">Not used.</span></span>

</dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>

<span data-ttu-id="963b5-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_ DONTPRETTYPATH** (0x00000800)</span><span class="sxs-lookup"><span data-stu-id="963b5-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF\_DONTPRETTYPATH** (0x00000800)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-119">Der Status der Option **Alle Großbuchstaben zulassen.**</span><span class="sxs-lookup"><span data-stu-id="963b5-119">The state of the **Allow all uppercase names** option.</span></span> <span data-ttu-id="963b5-120">Ab Windows Vista ist diese Ordneroption nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="963b5-120">As of Windows Vista, this folder option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>

<span data-ttu-id="963b5-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ DOUBLECLICKINWEBVIEW** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="963b5-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF\_DOUBLECLICKINWEBVIEW** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-122">Der Status der Option **Doppelklicken, um ein Element zu öffnen (einfaches Klicken zum Auswählen).**</span><span class="sxs-lookup"><span data-stu-id="963b5-122">The state of the **Double-click to open an item (single-click to select)** option.</span></span>

</dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>

<span data-ttu-id="963b5-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF \_ FILTER** (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="963b5-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF\_FILTER** (0x00010000)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-124">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="963b5-124">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>

<span data-ttu-id="963b5-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_ HIDDENFILEEXTS** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="963b5-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF\_HIDDENFILEEXTS** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-126">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="963b5-126">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>

<span data-ttu-id="963b5-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF \_ HIDEICONS** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="963b5-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF\_HIDEICONS** (0x00004000)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-128">Der Status des Symbols, der in der listenansicht Windows-Explorer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="963b5-128">The state of icon display in the Windows Explorer list view.</span></span> <span data-ttu-id="963b5-129">Wenn diese Option aktiv ist, werden in der Listenansicht keine Symbole angezeigt.</span><span class="sxs-lookup"><span data-stu-id="963b5-129">If this option is active, no icons are displayed in the list view.</span></span>

</dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>

<span data-ttu-id="963b5-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF \_ ICONSONLY** (0x01000000)</span><span class="sxs-lookup"><span data-stu-id="963b5-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF\_ICONSONLY** (0x01000000)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-131">**Windows Vista und höher.**</span><span class="sxs-lookup"><span data-stu-id="963b5-131">**Windows Vista and later**.</span></span> <span data-ttu-id="963b5-132">Der Status des Anzeigenamens, der in der Windows-Explorer Listenansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="963b5-132">The state of display name display in the Windows Explorer list view.</span></span> <span data-ttu-id="963b5-133">Wenn diese Option aktiv ist, werden Symbole in der Listenansicht angezeigt, Anzeigenamen jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="963b5-133">If this option is active, icons are displayed in the list view, but display names are not.</span></span>

</dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>

<span data-ttu-id="963b5-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_ MAPNETDRVBUTTON** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="963b5-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF\_MAPNETDRVBUTTON** (0x00001000)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-135">Der Status der **Schaltfläche Kartennetzwerklaufwerk anzeigen in der Symbolleistenoption.**</span><span class="sxs-lookup"><span data-stu-id="963b5-135">The state of the **Show map network drive button in toolbar** option.</span></span> <span data-ttu-id="963b5-136">Ab Windows Vista ist diese Option nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="963b5-136">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>

<span data-ttu-id="963b5-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_ NOCONFIRMRECYCLE** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="963b5-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF\_NOCONFIRMRECYCLE** (0x00008000)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-138">Der Status der **Bestätigungsdialogoption Löschbestätigung anzeigen** des Papierkorb.</span><span class="sxs-lookup"><span data-stu-id="963b5-138">The state of the Recycle Bin's **Display delete confirmation dialog** option.</span></span>

</dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>

<span data-ttu-id="963b5-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_ NONETCRAWLING** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="963b5-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF\_NONETCRAWLING** (0x00100000)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-140">Der Status der Option **Automatisch nach Netzwerkordnern und Druckern suchen.**</span><span class="sxs-lookup"><span data-stu-id="963b5-140">The state of the **Automatically search for network folders and printers** option.</span></span> <span data-ttu-id="963b5-141">Ab Windows Vista ist diese Option nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="963b5-141">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>

<span data-ttu-id="963b5-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_ SEPPROCESS** (0x00080000)</span><span class="sxs-lookup"><span data-stu-id="963b5-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF\_SEPPROCESS** (0x00080000)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-143">Der Status der **Ordnerfenster in einem separaten Prozess starten.**</span><span class="sxs-lookup"><span data-stu-id="963b5-143">The state of the **Launch folder windows in a separate process** option.</span></span>

</dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>

<span data-ttu-id="963b5-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ SERVERADMINUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="963b5-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF\_SERVERADMINUI** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-145">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="963b5-145">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>

<span data-ttu-id="963b5-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_ SHOWALLOBJECTS** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="963b5-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF\_SHOWALLOBJECTS** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-147">Der Status der Option **Ausgeblendete Dateien und** Ordner.</span><span class="sxs-lookup"><span data-stu-id="963b5-147">The state of the **Hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>

<span data-ttu-id="963b5-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ SHOWATTRIBCOL** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="963b5-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF\_SHOWATTRIBCOL** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-149">Der Status der Option **Dateiattribute in Detailansicht** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="963b5-149">The state of the **Show File Attributes in Detail View** option.</span></span> <span data-ttu-id="963b5-150">Ab Windows Vista ist diese Option nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="963b5-150">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>

<span data-ttu-id="963b5-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_ SHOWCOMPCOLOR** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="963b5-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF\_SHOWCOMPCOLOR** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-152">Der Status der Option **Verschlüsselte oder komprimierte NTFS-Dateien in Farbe** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="963b5-152">The state of the **Show encrypted or compressed NTFS files in color** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>

<span data-ttu-id="963b5-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_ SHOWEXTENSIONS** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="963b5-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF\_SHOWEXTENSIONS** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-154">Der Status der Option **Erweiterungen für bekannte Dateitypen ausblenden.**</span><span class="sxs-lookup"><span data-stu-id="963b5-154">The state of the **Hide extensions for known file types** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>

<span data-ttu-id="963b5-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_ SHOWINFOTIP** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="963b5-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF\_SHOWINFOTIP** (0x00002000)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-156">Der Status der Option **Popupbeschreibung für Ordner** und Desktopelemente anzeigen.</span><span class="sxs-lookup"><span data-stu-id="963b5-156">The state of the **Show pop-up description for folder and desktop items** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>

<span data-ttu-id="963b5-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_ SHOWSTARTPAGE** (0x00400000)</span><span class="sxs-lookup"><span data-stu-id="963b5-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF\_SHOWSTARTPAGE** (0x00400000)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-158">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="963b5-158">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>

<span data-ttu-id="963b5-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ SHOWSUPERHIDDEN** (0x00040000)</span><span class="sxs-lookup"><span data-stu-id="963b5-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF\_SHOWSUPERHIDDEN** (0x00040000)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-160">Der Status der Option **Geschützte Betriebssystemdateien ausblenden.**</span><span class="sxs-lookup"><span data-stu-id="963b5-160">The state of the **Hide protected operating system files** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>

<span data-ttu-id="963b5-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_ SHOWSYSFILES** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="963b5-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF\_SHOWSYSFILES** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-162">Der Status der Option **Ausgeblendete Dateien und** Ordner.</span><span class="sxs-lookup"><span data-stu-id="963b5-162">The state of the **Hidden files and folders** option.</span></span> <span data-ttu-id="963b5-163">In Windows Vista und höher entspricht dies SSF \_ SHOWALLOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="963b5-163">In Windows Vista and later, this is equivalent to SSF\_SHOWALLOBJECTS.</span></span> <span data-ttu-id="963b5-164">In Windows-Versionen vor Windows Vista wurde dieser Wert auf den Status der Option **Ausgeblendete** Dateien und Ordner nicht anzeigen verwiesen.</span><span class="sxs-lookup"><span data-stu-id="963b5-164">In versions of Windows before Windows Vista, this value referred to the state of the **Do not show hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>

<span data-ttu-id="963b5-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_ SHOWTYPEOVERLAY** (0x02000000)</span><span class="sxs-lookup"><span data-stu-id="963b5-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF\_SHOWTYPEOVERLAY** (0x02000000)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-166">**Windows Vista und höher.**</span><span class="sxs-lookup"><span data-stu-id="963b5-166">**Windows Vista and later**.</span></span> <span data-ttu-id="963b5-167">Der Status der Option **Dateisymbol für Miniaturansichten** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="963b5-167">The state of the **Display file icon on thumbnails** option.</span></span> <span data-ttu-id="963b5-168">Wenn diese Option aktiv ist, wird eine Dateitypüberlagerung angewendet, wenn eine Datei eine Miniaturansichtsdarstellung liefert.</span><span class="sxs-lookup"><span data-stu-id="963b5-168">If this option is active, a file type overlay is applied when a file supplies a thumbnail representation.</span></span>

</dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>

<span data-ttu-id="963b5-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_ SORTCOLUMNS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="963b5-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF\_SORTCOLUMNS** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-170">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="963b5-170">Not used.</span></span>

</dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>

<span data-ttu-id="963b5-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ STARTPANELON** (0x00200000)</span><span class="sxs-lookup"><span data-stu-id="963b5-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF\_STARTPANELON** (0x00200000)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-172">Der Status der Windows XP-Anzeigeoption, die zwischen dem Windows XP-Stil und dem klassischen Stil auswählt.</span><span class="sxs-lookup"><span data-stu-id="963b5-172">The state of the Windows XP display option, which selects between the Windows XP style and the classic style.</span></span> <span data-ttu-id="963b5-173">Ab Windows Vista ist diese Option nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="963b5-173">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>

<span data-ttu-id="963b5-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF \_ WEBVIEW** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="963b5-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF\_WEBVIEW** (0x00020000)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-175">Der Status der **Option Als Webansicht anzeigen.**</span><span class="sxs-lookup"><span data-stu-id="963b5-175">The state of the **Display as a web view option**.</span></span> <span data-ttu-id="963b5-176">Ab Windows Vista ist diese Option nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="963b5-176">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>

<span data-ttu-id="963b5-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC** (0x00000400)</span><span class="sxs-lookup"><span data-stu-id="963b5-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF\_WIN95CLASSIC** (0x00000400)</span></span>


</dt> <dd>

<span data-ttu-id="963b5-178">Der Status der Option **"Klassischer Stil".**</span><span class="sxs-lookup"><span data-stu-id="963b5-178">The state of the **Classic Style** option.</span></span> <span data-ttu-id="963b5-179">Ab Windows Vista ist diese Option nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="963b5-179">As of Windows Vista, this option is no longer available.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="963b5-180">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="963b5-180">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="963b5-181">JScript</span><span class="sxs-lookup"><span data-stu-id="963b5-181">JScript</span></span>

<span data-ttu-id="963b5-182">Typ: **VARIANT \_ BOOL \***</span><span class="sxs-lookup"><span data-stu-id="963b5-182">Type: **VARIANT\_BOOL\***</span></span>

<span data-ttu-id="963b5-183">Legen Sie auf **TRUE** fest, wenn die Einstellung vorhanden ist. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="963b5-183">Set to **true** if the setting exists; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="963b5-184">VB</span><span class="sxs-lookup"><span data-stu-id="963b5-184">VB</span></span>

<span data-ttu-id="963b5-185">Typ: **VARIANT \_ BOOL \***</span><span class="sxs-lookup"><span data-stu-id="963b5-185">Type: **VARIANT\_BOOL\***</span></span>

<span data-ttu-id="963b5-186">Legen Sie auf **TRUE** fest, wenn die Einstellung vorhanden ist. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="963b5-186">Set to **true** if the setting exists; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="963b5-187">Beispiele</span><span class="sxs-lookup"><span data-stu-id="963b5-187">Examples</span></span>

<span data-ttu-id="963b5-188">Die folgenden Beispiele zeigen die Verwendung von **GetSetting** für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="963b5-188">The following examples show the use of **GetSetting** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="963b5-189">Jscript:</span><span class="sxs-lookup"><span data-stu-id="963b5-189">JScript:</span></span>


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



<span data-ttu-id="963b5-190">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="963b5-190">VBScript:</span></span>


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
```



<span data-ttu-id="963b5-191">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="963b5-191">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="963b5-192">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="963b5-192">Requirements</span></span>



| <span data-ttu-id="963b5-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="963b5-193">Requirement</span></span> | <span data-ttu-id="963b5-194">Wert</span><span class="sxs-lookup"><span data-stu-id="963b5-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="963b5-195">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="963b5-195">Minimum supported client</span></span><br/> | <span data-ttu-id="963b5-196">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="963b5-196">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="963b5-197">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="963b5-197">Minimum supported server</span></span><br/> | <span data-ttu-id="963b5-198">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="963b5-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="963b5-199">Header</span><span class="sxs-lookup"><span data-stu-id="963b5-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="963b5-200"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="963b5-200"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="963b5-201">Idl</span><span class="sxs-lookup"><span data-stu-id="963b5-201">IDL</span></span><br/>                      | <dl> <span data-ttu-id="963b5-202"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="963b5-202"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="963b5-203">DLL</span><span class="sxs-lookup"><span data-stu-id="963b5-203">DLL</span></span><br/>                      | <dl> <span data-ttu-id="963b5-204"><dt>Shell32.dll (Version 6.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="963b5-204"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




