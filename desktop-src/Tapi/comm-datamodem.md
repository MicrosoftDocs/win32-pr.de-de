---
description: Die Geräteklasse "comm/datamoder" besteht aus DataModem-Geräten.
ms.assetid: 6bc314c6-30ec-4318-856a-3ab2fa6aadfb
title: comm/datamoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89210bcf14931e3905f71cdbb8678f5519cc4c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343731"
---
# <a name="commdatamodem"></a><span data-ttu-id="d225f-103">comm/datamoder</span><span class="sxs-lookup"><span data-stu-id="d225f-103">comm/datamodem</span></span>

<span data-ttu-id="d225f-104">Die Geräteklasse "comm/datamoder" besteht aus DataModem-Geräten.</span><span class="sxs-lookup"><span data-stu-id="d225f-104">The comm/datamodem device class consists of datamodem devices.</span></span> <span data-ttu-id="d225f-105">Sie greifen auf diese Geräte mithilfe der [Datei](/windows/desktop/FileIO/file-management-functions) -und [Kommunikationsfunktionen](/windows/desktop/DevIO/communications-functions)zu.</span><span class="sxs-lookup"><span data-stu-id="d225f-105">You access these devices by using the [file](/windows/desktop/FileIO/file-management-functions) and [communications functions](/windows/desktop/DevIO/communications-functions).</span></span> <span data-ttu-id="d225f-106">Geräte in dieser Klasse sind Zeilen Geräten zugeordnet, die den Typ linemediamode \_ datamoder-Medientyp unterstützen, der im **dwmediamodes** -Member der [**linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) -Struktur für das liniengerät angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d225f-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_DATAMODEM media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="d225f-107">Die [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) -Funktion füllt eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, legt **dwstringformat** auf den "StringFormat" \_ -Binärwert fest und fügt diese zusätzlichen Member an:</span><span class="sxs-lookup"><span data-stu-id="d225f-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to the STRINGFORMAT\_BINARY value and appending these additional members:</span></span>

``` syntax
HANDLE hComm;            // file handle to data modem
CHAR   szDeviceName[1];  // name of data modem
```

<span data-ttu-id="d225f-108">Der **hcomm** -Member ist das Handle des Open Communications-Ports.</span><span class="sxs-lookup"><span data-stu-id="d225f-108">The **hComm** member is the handle of the open communications port.</span></span> <span data-ttu-id="d225f-109">Dieser Member ist **null** , wenn der Anschluss noch nicht geöffnet ist, oder wenn der *dwselect* -Parameter von [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) nicht der linecallselect- \_ Aufrufwert ist.</span><span class="sxs-lookup"><span data-stu-id="d225f-109">This member is **NULL** if the port is not yet open or if the *dwSelect* parameter of [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) is not the LINECALLSELECT\_CALL value.</span></span> <span data-ttu-id="d225f-110">Wenn ein-Rückruf aktiv ist, öffnet der Dienstanbieter in der Regel den Port selbst, um die direkte Steuerung der Kommunikationshardware zu erhalten, ist jedoch nur erforderlich, um ein gültiges Handle zurückzugeben, wenn die Zeile verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="d225f-110">If a call is active, the service provider typically opens the port itself to get direct control of the communications hardware, but is only required to return a valid handle if the line is connected.</span></span> <span data-ttu-id="d225f-111">Der Dienstanbieter öffnet den Port mit dem überlappenden \_ Dateiflag \_ und konfiguriert dann den Port mit den Einstellungen, die von der [**linesetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) -Funktion angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d225f-111">The service provider opens the port using the FILE\_FLAG\_OVERLAPPED value and then configures the port using the settings specified by the [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) function.</span></span> <span data-ttu-id="d225f-112">Sie können zusätzliche Konfigurationsoptionen für das Gerät festlegen, indem Sie Kommunikationsfunktionen mit dem zurückgegebenen Handle verwenden.</span><span class="sxs-lookup"><span data-stu-id="d225f-112">You can set additional configuration options for the device by using communications functions with the returned handle.</span></span>

<span data-ttu-id="d225f-113">Der **szdevicename** -Member ist eine **null**-terminierte Zeichenfolge, die den Namen des Kommunikationsports angibt, der der Zeile, Adresse oder dem-Befehl zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d225f-113">The **szDeviceName** member is a **null**-terminated string that specifies the name of the communications port associated with the line, address, or call.</span></span>

<span data-ttu-id="d225f-114">Wenn **hcomm** ein gültiges Handle ist, können Sie es in nachfolgenden Aufrufen von Dateifunktionen wie "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " und " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile)" verwenden, um Daten für den Aufruf zu senden und zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d225f-114">If **hComm** is a valid handle, you can use it in subsequent calls to file functions, such as [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) and [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), to send and receive data on the call.</span></span> <span data-ttu-id="d225f-115">Wenn Sie den Kommunikationsport nicht mehr verwenden und vorzugsweise die [**linedeallo-eCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) -Funktion verwenden, um die Zuordnung des Aufrufes aufzurufen, müssen Sie den Port mit der [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion schließen.</span><span class="sxs-lookup"><span data-stu-id="d225f-115">When you are finished using the communications port and preferably before you use the [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) function to deallocate the call, you must close the port by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="d225f-116">Bei Verwendung der Funktionen [**linegetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) und [**linesetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) ist es für einige Dienstanbieter erforderlich, dass die Konfigurationsdaten für diese Geräteklasse das folgende Format aufweisen:</span><span class="sxs-lookup"><span data-stu-id="d225f-116">When using the [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) and [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) functions, some service providers require that the configuration data for this device class have the following format:</span></span>

``` syntax
typedef struct  tagDEVCFG  {
  DEVCFGHDR   dfgHdr;
  COMMCONFIG  commconfig;
} DEVCFG, *PDEVCFG, FAR* LPDEVCFG;

// Device setting information
typedef struct  tagDEVCFGDR  {
  DWORD       dwSize;
  DWORD       dwVersion;
  WORD        fwOptions;
  WORD        wWaitBong;
} DEVCFGHDR;
```

<span data-ttu-id="d225f-117">Im folgenden finden Sie Informationen zur Gerätekonfiguration für die Verwendung mit den Funktionen [**linegetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) und [**linesetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .</span><span class="sxs-lookup"><span data-stu-id="d225f-117">The following is device configuration information for use with the [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) and [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) functions.</span></span>

<dl> <dt>

<span data-ttu-id="d225f-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="d225f-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="d225f-119">Summe der Größe der **devcfghdr** -Struktur und der tatsächlichen Größe der [**CommConfig**](/windows/desktop/api/winbase/ns-winbase-commconfig) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d225f-119">Sum of the size of the **DEVCFGHDR** structure and the actual size of the [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d225f-120"><span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="d225f-120"><span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d225f-121">Die Versionsnummer der Unimodem- **Devconfig** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d225f-121">Version number of the Unimodem **DevConfig** structure.</span></span> <span data-ttu-id="d225f-122">Dieser Member kann mdmcfg- \_ Version (0x00010003) sein.</span><span class="sxs-lookup"><span data-stu-id="d225f-122">This member can be MDMCFG\_VERSION (0x00010003).</span></span>

</dd> <dt>

<span data-ttu-id="d225f-123"><span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**"f"-Optionen**</span><span class="sxs-lookup"><span data-stu-id="d225f-123"><span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**</span></span>
</dt> <dd>

<span data-ttu-id="d225f-124">Optionsflags, die auf der Optionsseite Unimodem angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d225f-124">Option flags that appear on the Unimodem Option page.</span></span> <span data-ttu-id="d225f-125">Dieser Member kann eine Kombination folgender Werte sein:</span><span class="sxs-lookup"><span data-stu-id="d225f-125">This member can be a combination of these values:</span></span>

<dl> <dt>

<span data-ttu-id="d225f-126"><span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>Terminal \_ vor (1)</span><span class="sxs-lookup"><span data-stu-id="d225f-126"><span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>TERMINAL\_PRE (1)</span></span>
</dt> <dd>

<span data-ttu-id="d225f-127">Zeigt den Bildschirm vor dem Terminal an.</span><span class="sxs-lookup"><span data-stu-id="d225f-127">Displays the pre-terminal screen.</span></span>

</dd> <dt>

<span data-ttu-id="d225f-128"><span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>Terminal \_ Post (2)</span><span class="sxs-lookup"><span data-stu-id="d225f-128"><span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>TERMINAL\_POST (2)</span></span>
</dt> <dd>

<span data-ttu-id="d225f-129">Zeigt den Bildschirm nach dem Terminal an.</span><span class="sxs-lookup"><span data-stu-id="d225f-129">Displays the post-terminal screen.</span></span>

</dd> <dt>

<span data-ttu-id="d225f-130"><span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>Manuelles \_ wählen (4)</span><span class="sxs-lookup"><span data-stu-id="d225f-130"><span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>MANUAL\_DIAL (4)</span></span>
</dt> <dd>

<span data-ttu-id="d225f-131">Gibt das Telefon manuell aus, wenn dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="d225f-131">Dials the phone manually, if capable of doing so.</span></span>

</dd> <dt>

<span data-ttu-id="d225f-132"><span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>Start \_ Beleuchtung (8)</span><span class="sxs-lookup"><span data-stu-id="d225f-132"><span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>LAUNCH\_LIGHTS (8)</span></span>
</dt> <dd>

<span data-ttu-id="d225f-133">Zeigt das Modem Symbol im Statusbereich der Taskleiste an.</span><span class="sxs-lookup"><span data-stu-id="d225f-133">Displays the modem icon in the status area of the taskbar.</span></span>

<span data-ttu-id="d225f-134">Nur der Wert für die Start \_ Beleuchtung ist standardmäßig festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d225f-134">Only the LAUNCH\_LIGHTS value is set by default</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d225f-135"><span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wwaitbong**</span><span class="sxs-lookup"><span data-stu-id="d225f-135"><span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**</span></span>
</dt> <dd>

<span data-ttu-id="d225f-136">Anzahl von Sekunden (in zwei Sekunden, Granularität), um den warte Vorgang auf den Bonitäts Ton ($) zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="d225f-136">Number of seconds (in two seconds granularity) to replace the wait for credit tone ($).</span></span>

</dd> <dt>

<span data-ttu-id="d225f-137"><span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**CommConfig**</span><span class="sxs-lookup"><span data-stu-id="d225f-137"><span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**</span></span>
</dt> <dd>

<span data-ttu-id="d225f-138">Die [**CommConfig**](/windows/desktop/api/winbase/ns-winbase-commconfig) -Struktur, die mit den Konfigurationsfunktionen für die Kommunikation und Modem verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d225f-138">[**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) structure that can be used with the communications and modem configuration functions.</span></span>

</dd> </dl>

 

 
