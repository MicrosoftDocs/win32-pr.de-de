---
title: Open-Befehl (corecrt \_ IO. h)
description: Der Open-Befehl initialisiert ein Gerät. Dieser Befehl wird von allen MCI-Geräten erkannt.
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- Open-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- open
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8d31f1806a9c12f764c679548564aa053c3041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741432"
---
# <a name="open-command"></a><span data-ttu-id="f2b4c-105">Befehl Öffnen</span><span class="sxs-lookup"><span data-stu-id="f2b4c-105">open command</span></span>

<span data-ttu-id="f2b4c-106">Der Open-Befehl initialisiert ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-106">The open command initializes a device.</span></span> <span data-ttu-id="f2b4c-107">Dieser Befehl wird von allen MCI-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="f2b4c-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("open %s %s %s"), 
  lpszDevice, 
  lpszOpenFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="f2b4c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2b4c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2b4c-110"><span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszdevice*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-110"><span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*</span></span>
</dt> <dd>

<span data-ttu-id="f2b4c-111">Der Bezeichner eines MCI-Geräts oder Gerätetreibers.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-111">Identifier of an MCI device or device driver.</span></span> <span data-ttu-id="f2b4c-112">Dabei kann es sich entweder um einen Gerätenamen (wie in der Registrierung oder in der SYSTEM.INI-Datei angegeben) oder um den Dateinamen des Gerätetreibers handeln.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-112">This can be either a device name (as given in the registry or the SYSTEM.INI file) or the filename of the device driver.</span></span> <span data-ttu-id="f2b4c-113">Wenn Sie den Dateinamen des Gerätetreibers angeben, können Sie optional den einschließen. DRV-Erweiterung, Sie sollten jedoch nicht den Pfad zur Datei einschließen.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-113">If you specify the filename of the device driver, you can optionally include the .DRV extension, but you should not include the path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="f2b4c-114"><span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszopenflags*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-114"><span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f2b4c-115">Flag, das angibt, was initialisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-115">Flag that identifies what to initialize.</span></span> <span data-ttu-id="f2b4c-116">In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **geöffneten** Befehl und die von den einzelnen Typen verwendeten Flags erkennen.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-116">The following table lists device types that recognize the **open** command and the flags used by each type.</span></span>



| <span data-ttu-id="f2b4c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f2b4c-117">Value</span></span>        | <span data-ttu-id="f2b4c-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f2b4c-118">Meaning</span></span>                                                        | <span data-ttu-id="f2b4c-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f2b4c-119">Meaning</span></span>                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="f2b4c-120">CDAudio</span><span class="sxs-lookup"><span data-stu-id="f2b4c-120">cdaudio</span></span>      | <span data-ttu-id="f2b4c-121">Alias *- \_ geräteralias* freigegeben</span><span class="sxs-lookup"><span data-stu-id="f2b4c-121">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="f2b4c-122">Typ des *Geräte \_ Typs*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-122">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="f2b4c-123">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="f2b4c-123">digitalvideo</span></span> | <span data-ttu-id="f2b4c-124">Alias *Gerät \_ aliaselementname* nostatic übergeordnetes *HWND* freigegeben</span><span class="sxs-lookup"><span data-stu-id="f2b4c-124">alias *device\_aliaselementname* nostatic parent *hwnd* sharable</span></span> | <span data-ttu-id="f2b4c-125">Stil für Stil des untergeordneten Stils im Stil *von \_ Popup Stil Typen Typ* *\_ Gerätetyp*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-125">style child style overlapped style popup style *style\_type* type *device\_type*</span></span> |
| <span data-ttu-id="f2b4c-126">overlay</span><span class="sxs-lookup"><span data-stu-id="f2b4c-126">overlay</span></span>      | <span data-ttu-id="f2b4c-127">Alias *- \_ Gerätealias* übergeordnetes *HWND*-Element mit shardstil</span><span class="sxs-lookup"><span data-stu-id="f2b4c-127">alias *device\_alias* parent *hwnd* sharable style child</span></span>         | <span data-ttu-id="f2b4c-128">Stil des Stil Überlapp enden Stils *Stil \_ Typs* Typ *\_ Gerätetyp*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-128">style overlapped style popup style *style\_type* type *device\_type*</span></span>             |
| <span data-ttu-id="f2b4c-129">sequencer</span><span class="sxs-lookup"><span data-stu-id="f2b4c-129">sequencer</span></span>    | <span data-ttu-id="f2b4c-130">Alias *- \_ geräteralias* freigegeben</span><span class="sxs-lookup"><span data-stu-id="f2b4c-130">alias *device\_alias* sharable</span></span>                                 | <span data-ttu-id="f2b4c-131">Typ des *Geräte \_ Typs*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-131">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="f2b4c-132">VCR</span><span class="sxs-lookup"><span data-stu-id="f2b4c-132">vcr</span></span>          | <span data-ttu-id="f2b4c-133">Alias *- \_ geräteralias* freigegeben</span><span class="sxs-lookup"><span data-stu-id="f2b4c-133">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="f2b4c-134">Typ des *Geräte \_ Typs*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-134">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="f2b4c-135">Videodisk</span><span class="sxs-lookup"><span data-stu-id="f2b4c-135">videodisk</span></span>    | <span data-ttu-id="f2b4c-136">Alias *- \_ geräteralias* freigegeben</span><span class="sxs-lookup"><span data-stu-id="f2b4c-136">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="f2b4c-137">Typ des *Geräte \_ Typs*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-137">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="f2b4c-138">waveaudiodatei</span><span class="sxs-lookup"><span data-stu-id="f2b4c-138">waveaudio</span></span>    | <span data-ttu-id="f2b4c-139">Alias Puffer *\_ Größe* des Alias *Geräts \_*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-139">alias *device\_alias* buffer *buffer\_size*</span></span>                     | <span data-ttu-id="f2b4c-140">*\_ Gerätetyp* "freigegeben Type"</span><span class="sxs-lookup"><span data-stu-id="f2b4c-140">sharable type *device\_type*</span></span>                                                    |



 

<span data-ttu-id="f2b4c-141">In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszopenflags** -Parameter und deren Bedeutung angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-141">The following table lists the flags that can be specified in the **lpszOpenFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="f2b4c-142">Wert</span><span class="sxs-lookup"><span data-stu-id="f2b4c-142">Value</span></span>                 | <span data-ttu-id="f2b4c-143">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f2b4c-143">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b4c-144">Alias *- \_ Gerätealias*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-144">alias *device\_alias*</span></span> | <span data-ttu-id="f2b4c-145">Gibt einen alternativen Namen für das angegebene Gerät an.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-145">Specifies an alternate name for the given device.</span></span> <span data-ttu-id="f2b4c-146">Wenn dieser Wert angegeben ist, muss er in nachfolgenden Befehlen als *Geräte- \_ ID* verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-146">If specified, it must be used as the *device\_id* in subsequent commands.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="f2b4c-147">*Elementname*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-147">*elementname*</span></span>         | <span data-ttu-id="f2b4c-148">Gibt den Namen des Geräte Elements (Datei) an, das beim Öffnen des Geräts geladen wird.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-148">Specifies the name of the device element (file) loaded when the device opens.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="f2b4c-149">Puffer *Puffer \_ Größe*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-149">buffer *buffer\_size*</span></span> | <span data-ttu-id="f2b4c-150">Legt die Größe des Puffers, der vom Waveform-Audiogerät verwendet wird, in Sekunden fest.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-150">Sets the size, in seconds, of the buffer used by the waveform-audio device.</span></span> <span data-ttu-id="f2b4c-151">Die Standardgröße des Puffers wird festgelegt, wenn das Waveform-Audiogerät installiert oder konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-151">The default size of the buffer is set when the waveform-audio device is installed or configured.</span></span> <span data-ttu-id="f2b4c-152">In der Regel ist die Puffergröße auf 4 Sekunden festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-152">Typically the buffer size is set to 4 seconds.</span></span> <span data-ttu-id="f2b4c-153">Mit dem MCIWave-Gerät beträgt die Mindestgröße 2 Sekunden, und die maximale Größe beträgt 9 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-153">With the MCIWAVE device, the minimum size is 2 seconds and the maximum size is 9 seconds.</span></span>                                                |
| <span data-ttu-id="f2b4c-154">übergeordnetes *HWND*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-154">parent *hwnd*</span></span>         | <span data-ttu-id="f2b4c-155">Gibt das Fenster Handle des übergeordneten Fensters an.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-155">Specifies the window handle of the parent window.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="f2b4c-156">freigegeben</span><span class="sxs-lookup"><span data-stu-id="f2b4c-156">sharable</span></span>              | <span data-ttu-id="f2b4c-157">Initialisiert das Gerät oder die Datei als Sharable.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-157">Initializes the device or file as sharable.</span></span> <span data-ttu-id="f2b4c-158">Bei nachfolgenden versuchen, das Gerät oder die Datei zu öffnen, tritt ein Fehler auf, es sei denn, Sie geben "sharable" in den ursprünglichen **und nachfolgenden**</span><span class="sxs-lookup"><span data-stu-id="f2b4c-158">Subsequent attempts to open the device or file fail unless you specify "sharable" in both the original and subsequent **open** commands.</span></span> <span data-ttu-id="f2b4c-159">MCI gibt einen ungültigen Gerätefehler zurück, wenn das Gerät bereits geöffnet ist und nicht freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-159">MCI returns an invalid device error if the device is already open and not sharable.</span></span><br/> <span data-ttu-id="f2b4c-160">Die mciseq Sequencer-und MCIWave-Geräte unterstützen keine freigegebenen Dateien.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-160">The MCISEQ sequencer and MCIWAVE devices do not support shared files.</span></span><br/> |
| <span data-ttu-id="f2b4c-161">untergeordnetes Stil</span><span class="sxs-lookup"><span data-stu-id="f2b4c-161">style child</span></span>           | <span data-ttu-id="f2b4c-162">Öffnet ein Fenster mit einem untergeordneten Fenster Stil.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-162">Opens a window with a child window style.</span></span>                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f2b4c-163">überschlender Stil</span><span class="sxs-lookup"><span data-stu-id="f2b4c-163">style overlapped</span></span>      | <span data-ttu-id="f2b4c-164">Öffnet ein Fenster mit einem überlappenden Fenster Stil.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-164">Opens a window with an overlapped window style.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="f2b4c-165">Stil-Popup</span><span class="sxs-lookup"><span data-stu-id="f2b4c-165">style popup</span></span>           | <span data-ttu-id="f2b4c-166">Öffnet ein Fenster mit einem Popup Fenster Stil.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-166">Opens a window with a pop-up window style.</span></span>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f2b4c-167">Stil *\_ Stiltyp*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-167">style *style\_type*</span></span>   | <span data-ttu-id="f2b4c-168">Gibt einen Fenster Stil an.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-168">Indicates a window style.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f2b4c-169">Typ des *Geräte \_ Typs*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-169">type *device\_type*</span></span>   | <span data-ttu-id="f2b4c-170">Gibt den Gerätetyp einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-170">Specifies the device type of a file.</span></span>                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="f2b4c-171"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-171"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f2b4c-172">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-172">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="f2b4c-173">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f2b4c-173">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2b4c-174">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2b4c-174">Return Value</span></span>

<span data-ttu-id="f2b4c-175">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-175">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2b4c-176">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2b4c-176">Remarks</span></span>

<span data-ttu-id="f2b4c-177">MCI reserviert "CDAudio" für den CD-audiogerätetyp "Videodisk" für den Videodisk-Gerätetyp "Sequencer" für den Typ des MIDI Sequencer-Geräts, "AVIVideo" für den Gerätetyp Digital-Video und "waveaudiodatei" für den Typ "Waveform-Audiogerät".</span><span class="sxs-lookup"><span data-stu-id="f2b4c-177">MCI reserves "cdaudio" for the CD audio device type, "videodisc" for the videodisc device type, "sequencer" for the MIDI sequencer device type, "AVIVideo" for the digital-video device type, and "waveaudio" for the waveform-audio device type.</span></span>

<span data-ttu-id="f2b4c-178">Als Alternative zum Flag "Type" kann MCI das Gerät basierend auf der von der Datei verwendeten Erweiterung auswählen, wie in der Registrierung oder im \[ MCI-Erweiterungs \] Abschnitt der SYSTEM.INI Datei aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-178">As an alternative to the "type" flag, MCI can select the device based on the extension used by the file, as recorded in the registry or the \[mci extension\] section of the SYSTEM.INI file.</span></span>

<span data-ttu-id="f2b4c-179">MCI kann AVI-Dateien mithilfe eines Datei Schnittstellen Zeigers oder eines Stream-Schnittstellen Zeigers öffnen.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-179">MCI can open AVI files by using a file-interface pointer or a stream-interface pointer.</span></span> <span data-ttu-id="f2b4c-180">Wenn Sie eine Datei mit einer der beiden Schnittstellen Zeiger Typen öffnen möchten, geben Sie ein @-Zeichen gefolgt vom Schnittstellen Zeiger anstelle des Datei-oder Geräte namens für den *lpszdevice* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-180">To open a file by using either type of interface pointer, specify an at sign (@) followed by the interface pointer in place of the file or device name for the *lpszDevice* parameter.</span></span> <span data-ttu-id="f2b4c-181">Weitere Informationen über die Datei-und streamschnittstellen finden Sie unter " [avifile-Funktionen und-Makros](avifile-functions-and-macros.md)".</span><span class="sxs-lookup"><span data-stu-id="f2b4c-181">For more information about the file and stream interfaces, see " [AVIFile Functions and Macros](avifile-functions-and-macros.md)."</span></span>

<span data-ttu-id="f2b4c-182">Mit dem folgenden Befehl wird das Gerät "mysound" geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-182">The following command opens the "mysound" device.</span></span>

``` syntax
open new type waveaudio alias mysound buffer 6
```

<span data-ttu-id="f2b4c-183">Mit dem Gerätenamen "New" bereitet der Wellenform-Treiber eine neue Wellenform-Ressource vor.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-183">With device name "new", the waveform driver prepares a new waveform resource.</span></span> <span data-ttu-id="f2b4c-184">Der Befehl weist den Gerätealias "mysound" zu und gibt einen 6-Sekunden-Puffer an.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-184">The command assigns the device alias "mysound" and specifies a 6-second buffer.</span></span>

<span data-ttu-id="f2b4c-185">Sie können das Flag "Type" entfernen, wenn Sie den Gerätenamen mit dem Dateinamen kombinieren.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-185">You can eliminate the "type" flag if you combine the device name with the filename.</span></span> <span data-ttu-id="f2b4c-186">MCI erkennt diese Kombination, wenn Sie die folgende Syntax verwenden:</span><span class="sxs-lookup"><span data-stu-id="f2b4c-186">MCI recognizes this combination when you use the following syntax:</span></span>

<span data-ttu-id="f2b4c-187">*Geräte \_ Name* !</span><span class="sxs-lookup"><span data-stu-id="f2b4c-187">*device\_name* !</span></span> <span data-ttu-id="f2b4c-188">*Element \_ Name*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-188">*element\_name*</span></span>

<span data-ttu-id="f2b4c-189">Das Ausrufezeichen trennt den Gerätenamen vom Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-189">The exclamation point separates the device name from the filename.</span></span> <span data-ttu-id="f2b4c-190">Das Ausrufezeichen sollte nicht durch Leerzeichen getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-190">The exclamation point should not be delimited by white spaces.</span></span>

<span data-ttu-id="f2b4c-191">Im folgenden Beispiel wird das Recht geöffnet. WAV-Datei, die das Gerät "WaveAudio" verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-191">The following example opens the RIGHT.WAV file using the "waveaudio" device.</span></span>

``` syntax
open waveaudio!right.wav
```

<span data-ttu-id="f2b4c-192">Der MCIWave-Treiber erfordert ein asynchrones Waveform-Audiogerät.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-192">The MCIWAVE driver requires an asynchronous waveform-audio device.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2b4c-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2b4c-193">Requirements</span></span>



| <span data-ttu-id="f2b4c-194">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2b4c-194">Requirement</span></span> | <span data-ttu-id="f2b4c-195">Wert</span><span class="sxs-lookup"><span data-stu-id="f2b4c-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b4c-196">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2b4c-196">Minimum supported client</span></span><br/> | <span data-ttu-id="f2b4c-197">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2b4c-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f2b4c-198">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2b4c-198">Minimum supported server</span></span><br/> | <span data-ttu-id="f2b4c-199">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2b4c-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f2b4c-200">Header</span><span class="sxs-lookup"><span data-stu-id="f2b4c-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2b4c-201"><dt>Corecrt \_ IO. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2b4c-201"><dt>Corecrt\_io.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2b4c-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2b4c-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2b4c-203">MCI</span><span class="sxs-lookup"><span data-stu-id="f2b4c-203">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f2b4c-204">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="f2b4c-204">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

