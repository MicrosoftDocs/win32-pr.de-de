---
title: Öffnen eines Geräts
description: Öffnen eines Geräts
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- MCI_OPEN-Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd975b0dd5004fb4b1209003568b7fd5901cfc4e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038839"
---
# <a name="opening-a-device"></a><span data-ttu-id="0cb03-104">Öffnen eines Geräts</span><span class="sxs-lookup"><span data-stu-id="0cb03-104">Opening a Device</span></span>

<span data-ttu-id="0cb03-105">Bevor Sie ein Gerät verwenden, müssen Sie es mit dem [**geöffneten**](open.md) Befehl ([**MCI \_ Open**](mci-open.md)) initialisieren.</span><span class="sxs-lookup"><span data-stu-id="0cb03-105">Before using a device, you must initialize it by using the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span> <span data-ttu-id="0cb03-106">Mit diesem Befehl wird der Treiber in den Arbeitsspeicher geladen (sofern er nicht bereits geladen wurde), und der Geräte Bezeichner wird abgerufen, den Sie zum Identifizieren des Geräts in nachfolgenden MCI-Befehlen verwenden.</span><span class="sxs-lookup"><span data-stu-id="0cb03-106">This command loads the driver into memory (if it isn't already loaded) and retrieves the device identifier you will use to identify the device in subsequent MCI commands.</span></span> <span data-ttu-id="0cb03-107">Sie sollten den Rückgabewert der Funktion " [**mciSendString**](/previous-versions//dd757161(v=vs.85)) " oder " [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) " überprüfen, bevor Sie einen neuen Geräte Bezeichner verwenden, um sicherzustellen, dass der Bezeichner gültig ist.</span><span class="sxs-lookup"><span data-stu-id="0cb03-107">You should check the return value of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) or [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function before using a new device identifier to ensure that the identifier is valid.</span></span> <span data-ttu-id="0cb03-108">(Sie können auch einen Geräte Bezeichner mithilfe der Funktion " [**mcigetdebug Eid**](/previous-versions//dd757156(v=vs.85)) " abrufen.)</span><span class="sxs-lookup"><span data-stu-id="0cb03-108">(You can also retrieve a device identifier by using the [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) function.)</span></span>

<span data-ttu-id="0cb03-109">Wie bei allen MCI-befehlsnachrichten verfügt **MCI \_ Open** über eine zugeordnete Struktur.</span><span class="sxs-lookup"><span data-stu-id="0cb03-109">Like all MCI command messages, **MCI\_OPEN** has an associated structure.</span></span> <span data-ttu-id="0cb03-110">Diese Strukturen werden manchmal als *Parameter Blöcke* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0cb03-110">These structures are sometimes called *parameter blocks*.</span></span> <span data-ttu-id="0cb03-111">Die Standardstruktur für **MCI \_ Open** ist [**MCI \_ Open- \_ Parser**](mci-open-parms.md).</span><span class="sxs-lookup"><span data-stu-id="0cb03-111">The default structure for **MCI\_OPEN** is [**MCI\_OPEN\_PARMS**](mci-open-parms.md).</span></span> <span data-ttu-id="0cb03-112">Bestimmte Geräte (z. b. *Wellenform* und *Overlay*) haben erweiterte Strukturen (z. b. [**MCI \_ Wave \_ Open \_**](mci-wave-open-parms.md) -Parameter und [**MCI- \_ Oly- \_ Open \_**](mci-ovly-open-parms.md)-Parameter), um zusätzliche optionale Parameter zu bieten.</span><span class="sxs-lookup"><span data-stu-id="0cb03-112">Certain devices (such as *waveform* and *overlay*) have extended structures (such as [**MCI\_WAVE\_OPEN\_PARMS**](mci-wave-open-parms.md) and [**MCI\_OVLY\_OPEN\_PARMS**](mci-ovly-open-parms.md)) to accommodate additional optional parameters.</span></span> <span data-ttu-id="0cb03-113">Wenn Sie diese zusätzlichen Parameter nicht benötigen, können Sie die MCI-Struktur mit **\_ offenen \_ para** Metern mit einem beliebigen MCI-Gerät verwenden.</span><span class="sxs-lookup"><span data-stu-id="0cb03-113">Unless you need to use these additional parameters, you can use the **MCI\_OPEN\_PARMS** structure with any MCI device.</span></span>

<span data-ttu-id="0cb03-114">Die Anzahl der Geräte, die Sie öffnen können, ist nur durch die Menge des verfügbaren Arbeitsspeichers beschränkt.</span><span class="sxs-lookup"><span data-stu-id="0cb03-114">The number of devices you can have open is limited only by the amount of available memory.</span></span>

## <a name="using-an-alias"></a><span data-ttu-id="0cb03-115">Verwenden eines Alias</span><span class="sxs-lookup"><span data-stu-id="0cb03-115">Using an Alias</span></span>

<span data-ttu-id="0cb03-116">Wenn Sie ein Gerät öffnen, können Sie das Flag "Alias" verwenden, um einen Geräte Bezeichner für das Gerät anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0cb03-116">When you open a device, you can use the "alias" flag to specify a device identifier for the device.</span></span> <span data-ttu-id="0cb03-117">Mit diesem Flag können Sie eine kurze Geräte-ID für Verbund Geräte mit langen Dateinamen zuweisen, und Sie können mehrere Instanzen derselben Datei oder eines Geräts öffnen.</span><span class="sxs-lookup"><span data-stu-id="0cb03-117">This flag lets you assign a short device identifier for compound devices with lengthy filenames, and it lets you open multiple instances of the same file or device.</span></span>

<span data-ttu-id="0cb03-118">Der folgende Befehl weist z. b. den Geräte Bezeichner "birdcall" dem langen Dateinamen "C: \\ nabunds \\ Sounds \\ mockmtng" zu. Wave</span><span class="sxs-lookup"><span data-stu-id="0cb03-118">For example, the following command assigns the device identifier "birdcall" to the lengthy filename C:\\NABIRDS\\SOUNDS\\MOCKMTNG.WAV:</span></span>


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="0cb03-119">In der befehlsnachrichten Schnittstelle geben Sie einen Alias an, indem Sie den **lpstraualias** -Member der [**geöffneten MCI-Struktur \_ Öffnen \_**](mci-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="0cb03-119">In the command-message interface, you specify an alias by using the **lpstrAlias** member of the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span>

## <a name="specifying-a-device-type"></a><span data-ttu-id="0cb03-120">Angeben eines Gerätetyps</span><span class="sxs-lookup"><span data-stu-id="0cb03-120">Specifying a Device Type</span></span>

<span data-ttu-id="0cb03-121">Wenn Sie ein Gerät öffnen, können Sie das Flag "Type" verwenden, um auf einen Gerätetyp und nicht auf einen bestimmten Gerätetreiber zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="0cb03-121">When you open a device, you can use the "type" flag to refer to a device type, rather than to a specific device driver.</span></span> <span data-ttu-id="0cb03-122">Im folgenden Beispiel wird die Waveform-Audiodatei C: \\ Windows- \\ Chimes geöffnet. WAV (mit dem Flag "Type", um den **waveaudiogerätetyp** anzugeben) und weist den Alias "Chimes" zu:</span><span class="sxs-lookup"><span data-stu-id="0cb03-122">The following example opens the waveform-audio file C:\\WINDOWS\\CHIMES.WAV (using the "type" flag to specify the **waveaudio** device type) and assigns the alias "chimes":</span></span>


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="0cb03-123">In der befehlsnachrichten Schnittstelle wird die Funktionalität des "Type"-Flags durch das **lpstraudevicetype** -Element der [**MCI \_ Open \_**](mci-open-parms.md) -Parameterstruktur bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="0cb03-123">In the command-message interface, the functionality of the "type" flag is supplied by the **lpstrDeviceType** member of the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span>

## <a name="simple-and-compound-devices"></a><span data-ttu-id="0cb03-124">Einfache und Verbund Geräte</span><span class="sxs-lookup"><span data-stu-id="0cb03-124">Simple and Compound Devices</span></span>

<span data-ttu-id="0cb03-125">MCI klassifiziert Gerätetreiber als *Verbund* oder *einfach*.</span><span class="sxs-lookup"><span data-stu-id="0cb03-125">MCI classifies device drivers as *compound* or *simple*.</span></span> <span data-ttu-id="0cb03-126">Treiber für Verbund Geräte erfordern den Namen einer Datendatei für die Wiedergabe. Treiber für einfache Geräte nicht.</span><span class="sxs-lookup"><span data-stu-id="0cb03-126">Drivers for compound devices require the name of a data file for playback; drivers for simple devices do not.</span></span>

<span data-ttu-id="0cb03-127">Einfache Geräte sind **CDAudio** -und **Videodisk** -Geräte.</span><span class="sxs-lookup"><span data-stu-id="0cb03-127">Simple devices include **cdaudio** and **videodisc** devices.</span></span> <span data-ttu-id="0cb03-128">Es gibt zwei Möglichkeiten, um einfache Geräte zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="0cb03-128">There are two ways to open simple devices:</span></span>

-   <span data-ttu-id="0cb03-129">Geben Sie einen Zeiger auf eine NULL-terminierte Zeichenfolge an, die den Gerätenamen aus der Registrierung oder der SYSTEM.INI Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="0cb03-129">Specify a pointer to a null-terminated string containing the device name from the registry or the SYSTEM.INI file.</span></span>

    <span data-ttu-id="0cb03-130">Beispielsweise können Sie ein **Videodisk** -Gerät mit dem folgenden Befehl öffnen:</span><span class="sxs-lookup"><span data-stu-id="0cb03-130">For example, you can open a **videodisc** device by using the following command:</span></span>


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="0cb03-131">In diesem Fall ist "Videodisk" der Gerätename aus der Registrierung oder der \[ MCI- \] Abschnitt der SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="0cb03-131">In this case, "videodisc" is the device name from the registry or the \[mci\] section of SYSTEM.INI.</span></span>

-   <span data-ttu-id="0cb03-132">Geben Sie den tatsächlichen Namen des Gerätetreibers an.</span><span class="sxs-lookup"><span data-stu-id="0cb03-132">Specify the actual name of the device driver.</span></span> <span data-ttu-id="0cb03-133">Wenn Sie ein Gerät mit dem Gerätetreiber-Dateinamen öffnen, wird die Anwendung jedoch gerätespezifisch, und die Ausführung der Anwendung kann verhindert werden, wenn sich die Systemkonfiguration ändert.</span><span class="sxs-lookup"><span data-stu-id="0cb03-133">Opening a device using the device-driver filename, however, makes the application device-specific and can prevent the application from running if the system configuration changes.</span></span> <span data-ttu-id="0cb03-134">Wenn Sie einen Dateinamen verwenden, müssen Sie nicht den kompletten Pfad oder die Dateinamenerweiterung angeben. MCI geht davon aus, dass sich Treiber in einem System Verzeichnis befinden und über verfügen. DRV-Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="0cb03-134">If you use a filename, you do not need to specify the complete path or the filename extension; MCI assumes drivers are located in a system directory and have the .DRV filename extension.</span></span>

<span data-ttu-id="0cb03-135">Verbund Geräte umfassen **waveaudiogeräte** und **Sequencer** -Geräte.</span><span class="sxs-lookup"><span data-stu-id="0cb03-135">Compound devices include **waveaudio** and **sequencer** devices.</span></span> <span data-ttu-id="0cb03-136">Die Daten für ein Verbund Gerät werden manchmal als *Geräte Element* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0cb03-136">The data for a compound device is sometimes called a *device element*.</span></span> <span data-ttu-id="0cb03-137">Dieses Dokument bezieht sich jedoch im Allgemeinen auf diese Daten als Datei, auch wenn die Daten in einigen Fällen nicht als Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0cb03-137">This document, however, generally refers to this data as a file, even though in some cases the data might not be stored as a file.</span></span>

<span data-ttu-id="0cb03-138">Es gibt drei Möglichkeiten, ein Verbund Gerät zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="0cb03-138">There are three ways to open a compound device:</span></span>

-   <span data-ttu-id="0cb03-139">Geben Sie nur den Gerätenamen an.</span><span class="sxs-lookup"><span data-stu-id="0cb03-139">Specify only the device name.</span></span> <span data-ttu-id="0cb03-140">Auf diese Weise können Sie ein Verbund Gerät öffnen, ohne einen Dateinamen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="0cb03-140">This lets you open a compound device without associating a filename.</span></span> <span data-ttu-id="0cb03-141">Bei den meisten Verbund Geräten werden nur die [**Funktionen**](capability.md) ([**MCI \_ getdevcaps**](mci-getdevcaps.md)) und [**Close**](close.md) ([**MCI \_ Close**](mci-close.md)) verarbeitet, wenn Sie auf diese Weise geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="0cb03-141">Most compound devices process only the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)) and [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)) commands when they are opened this way.</span></span>
-   <span data-ttu-id="0cb03-142">Geben Sie nur den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="0cb03-142">Specify only the filename.</span></span> <span data-ttu-id="0cb03-143">Der Gerätename wird aus den Zuordnungen in der Registrierung ermittelt.</span><span class="sxs-lookup"><span data-stu-id="0cb03-143">The device name is determined from the associations in the registry.</span></span>
-   <span data-ttu-id="0cb03-144">Geben Sie den Dateinamen und den Gerätenamen an.</span><span class="sxs-lookup"><span data-stu-id="0cb03-144">Specify the filename and the device name.</span></span> <span data-ttu-id="0cb03-145">MCI ignoriert die Einträge in der Registrierung und öffnet den angegebenen Gerätenamen.</span><span class="sxs-lookup"><span data-stu-id="0cb03-145">MCI ignores the entries in the registry and opens the specified device name.</span></span>

<span data-ttu-id="0cb03-146">Wenn Sie einer Datendatei ein bestimmtes Gerät zuordnen möchten, können Sie den Dateinamen und den Gerätenamen angeben.</span><span class="sxs-lookup"><span data-stu-id="0cb03-146">To associate a data file with a particular device, you can specify the filename and device name.</span></span> <span data-ttu-id="0cb03-147">Der folgende Befehl öffnet z. b. das **Waveaudiogerät** mit dem Dateinamen myvoice. SND</span><span class="sxs-lookup"><span data-stu-id="0cb03-147">For example, the following command opens the **waveaudio** device with the filename MYVOICE.SND:</span></span>


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="0cb03-148">In der Befehls Zeichenfolgen-Schnittstelle können Sie auch die Geräte namens Spezifikation mit dem alternativen Ausrufezeichen Format abkürzen, wie mit dem [**Open**](open.md) -Befehl dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="0cb03-148">In the command-string interface, you can also abbreviate the device name specification by using the alternative exclamation-point format, as documented with the [**open**](open.md) command.</span></span>

## <a name="opening-a-device-using-the-filename-extension"></a><span data-ttu-id="0cb03-149">Öffnen eines Geräts mithilfe der Dateinamenerweiterung</span><span class="sxs-lookup"><span data-stu-id="0cb03-149">Opening a Device Using the Filename Extension</span></span>

<span data-ttu-id="0cb03-150">Wenn der Befehl [**Öffnen**](open.md) ([**MCI \_ geöffnet**](mci-open.md)) nur den Dateinamen angibt, verwendet MCI die Dateinamenerweiterung, um das entsprechende Gerät aus der Liste in der Registrierung oder im \[ Abschnitt MCI-Erweiterungen \] der SYSTEM.INI Datei auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="0cb03-150">If the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command specifies only the filename, MCI uses the filename extension to select the appropriate device from the list in the registry or the \[mci extensions\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="0cb03-151">Die Einträge im \[ Abschnitt MCI- \] Erweiterungen verwenden die folgende Form:</span><span class="sxs-lookup"><span data-stu-id="0cb03-151">The entries in the \[mci extensions\] section use the following form:</span></span>

<span data-ttu-id="0cb03-152">*Dateiname \_ Erweiterung*  =  *Geräte \_ Name*</span><span class="sxs-lookup"><span data-stu-id="0cb03-152">*filename\_extension* = *device\_name*</span></span>

<span data-ttu-id="0cb03-153">MCI verwendet implizit den *Geräte \_ Namen* , wenn die Erweiterung gefunden wird und ein Gerätename nicht im Befehl " **Öffnen** " angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="0cb03-153">MCI implicitly uses *device\_name* if the extension is found and if a device name has not been specified in the **open** command.</span></span>

<span data-ttu-id="0cb03-154">Das folgende Beispiel zeigt einen typischen \[ MCI-Erweiterungs \] Abschnitt:</span><span class="sxs-lookup"><span data-stu-id="0cb03-154">The following example shows a typical \[mci extensions\] section:</span></span>


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



<span data-ttu-id="0cb03-155">Mithilfe dieser Definitionen öffnet MCI das **Waveaudiogerät** , wenn der folgende Befehl ausgegeben wird:</span><span class="sxs-lookup"><span data-stu-id="0cb03-155">Using these definitions, MCI opens the **waveaudio** device if the following command is issued:</span></span>


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a><span data-ttu-id="0cb03-156">Neue Datendateien</span><span class="sxs-lookup"><span data-stu-id="0cb03-156">New Data Files</span></span>

<span data-ttu-id="0cb03-157">Geben Sie einfach einen leeren Dateinamen an, um eine neue Datendatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0cb03-157">To create a new data file, simply specify a blank filename.</span></span> <span data-ttu-id="0cb03-158">MCI speichert eine neue Datei erst, wenn Sie Sie mit dem Befehl [**Speichern**](save.md) ([**MCI- \_ Speicher**](mci-save.md)) speichern.</span><span class="sxs-lookup"><span data-stu-id="0cb03-158">MCI does not save a new file until you save it by using the [**save**](save.md) ([**MCI\_SAVE**](mci-save.md)) command.</span></span> <span data-ttu-id="0cb03-159">Beim Erstellen einer neuen Datei müssen Sie einen Gerätealias mit dem [**geöffneten**](open.md) Befehl ([**MCI \_ Open**](mci-open.md)) einschließen.</span><span class="sxs-lookup"><span data-stu-id="0cb03-159">When creating a new file, you must include a device alias with the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span>

<span data-ttu-id="0cb03-160">Im folgenden Beispiel wird eine neue **waveaudiodatei** geöffnet, die Aufzeichnung gestartet und beendet und anschließend die Datei gespeichert und geschlossen:</span><span class="sxs-lookup"><span data-stu-id="0cb03-160">The following example opens a new **waveaudio** file, starts and stops recording, then saves and closes the file:</span></span>


```C++
mciSendString("open new type waveaudio alias capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("record capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("stop capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("save capture orca.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="sharable-devices"></a><span data-ttu-id="0cb03-161">Sharable-Geräte</span><span class="sxs-lookup"><span data-stu-id="0cb03-161">Sharable Devices</span></span>

<span data-ttu-id="0cb03-162">Mit dem Flag "sharable" (MCI \_ Open \_ share able) des [**geöffneten**](open.md) Befehls ([**MCI \_ Open**](mci-open.md)) können mehrere Anwendungen gleichzeitig auf das gleiche Gerät (oder die gleiche Datei) und die Geräte Instanz zugreifen.</span><span class="sxs-lookup"><span data-stu-id="0cb03-162">The "sharable" (MCI\_OPEN\_SHAREABLE) flag of the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command lets multiple applications access the same device (or file) and device instance simultaneously.</span></span> <span data-ttu-id="0cb03-163">Wenn Ihre Anwendung ein Gerät oder eine Datei als frei stellbar öffnet, können auch andere Anwendungen darauf zugreifen, indem Sie Sie als Sharable öffnen.</span><span class="sxs-lookup"><span data-stu-id="0cb03-163">If your application opens a device or file as sharable, other applications can also access it by opening it as sharable.</span></span> <span data-ttu-id="0cb03-164">Das freigegebene Gerät oder die freigegebene Datei gibt jeder Anwendung die Möglichkeit, die Parameter zu ändern, die den Betriebszustand steuern.</span><span class="sxs-lookup"><span data-stu-id="0cb03-164">The shared device or file gives each application the ability to change the parameters governing its operating state.</span></span> <span data-ttu-id="0cb03-165">Jedes Mal, wenn ein Gerät oder eine Datei als Sharable geöffnet wird, gibt MCI einen eindeutigen Geräte Bezeichner zurück, auch wenn die Bezeichner auf dieselbe Instanz verweisen.</span><span class="sxs-lookup"><span data-stu-id="0cb03-165">Each time a device or file is opened as sharable, MCI returns a unique device identifier, even though the identifiers refer to the same instance.</span></span>

<span data-ttu-id="0cb03-166">Wenn Ihre Anwendung ein Gerät oder eine Datei öffnet, ohne anzugeben, dass Sie freigegeben werden kann, kann keine andere Anwendung darauf zugreifen, bis Sie von der Anwendung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="0cb03-166">If your application opens a device or file without specifying that it is sharable, no other application can access it until your application closes it.</span></span> <span data-ttu-id="0cb03-167">Wenn ein Gerät nur eine geöffnete Instanz unterstützt, schlägt der Befehl " **Öffnen** " fehl, wenn Sie das freigegeben-Flag angeben.</span><span class="sxs-lookup"><span data-stu-id="0cb03-167">Also, if a device supports only one open instance, the **open** command will fail if you specify the sharable flag.</span></span>

<span data-ttu-id="0cb03-168">Wenn Ihre Anwendung ein Gerät öffnet und angibt, dass Sie freigegeben werden kann, sollte Ihre Anwendung keine Annahmen über den Status dieses Geräts treffen.</span><span class="sxs-lookup"><span data-stu-id="0cb03-168">If your application opens a device and specifies that it is sharable, your application should not make any assumptions about the state of this device.</span></span> <span data-ttu-id="0cb03-169">Die Anwendung muss möglicherweise Änderungen vornehmen, die von anderen Anwendungen, die auf das Gerät zugreifen, vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="0cb03-169">Your application might need to compensate for changes made by other applications accessing the device.</span></span>

<span data-ttu-id="0cb03-170">Die meisten Verbund Dateien können nicht freigegeben werden. Sie können jedoch mehrere Dateien öffnen oder eine einzelne Datei mehrmals öffnen.</span><span class="sxs-lookup"><span data-stu-id="0cb03-170">Most compound files are not sharable; however, you can open multiple files, or you can open a single file multiple times.</span></span> <span data-ttu-id="0cb03-171">Wenn Sie eine einzelne Datei mehrmals öffnen, erstellt MCI jeweils eine unabhängige Instanz, wobei jede Instanz einen eindeutigen Betriebsstatus aufweist.</span><span class="sxs-lookup"><span data-stu-id="0cb03-171">If you open a single file multiple times, MCI creates an independent instance for each, with each instance having a unique operating status.</span></span>

<span data-ttu-id="0cb03-172">Wenn Sie mehrere Instanzen einer Datei öffnen, müssen Sie jedem eine eindeutige Gerätekennung zuweisen.</span><span class="sxs-lookup"><span data-stu-id="0cb03-172">If you open multiple instances of a file, you must assign a unique device identifier to each.</span></span> <span data-ttu-id="0cb03-173">Sie können einen Alias verwenden, wie im folgenden Abschnitt beschrieben, um für jede Datei einen eindeutigen Namen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="0cb03-173">You can use an alias, as described in the following section, to assign a unique name for each file.</span></span>

 

 