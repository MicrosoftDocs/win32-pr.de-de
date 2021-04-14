---
description: Ausstellen von unformatierten AV/C-Befehlen
ms.assetid: 18081652-962f-4605-84b7-1fa60f61ad05
title: Ausstellen von unformatierten AV/C-Befehlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1cf1b25d45a0eb35ede7151941d0cd49d30db0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392513"
---
# <a name="issuing-raw-avc-commands"></a><span data-ttu-id="a848a-103">Ausstellen von unformatierten AV/C-Befehlen</span><span class="sxs-lookup"><span data-stu-id="a848a-103">Issuing Raw AV/C Commands</span></span>

<span data-ttu-id="a848a-104">Die [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)-, [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)-und [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) -Schnittstellen funktionieren, indem Sie die Methodenaufrufe in Befehle für den Treiber übersetzen und dann die Antwort des Treibers interpretieren und Sie durch ein **HRESULT** oder einen Output-Parameter zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a848a-104">The [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport), and [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) interfaces work by translating the method calls into commands for the driver, then interpreting the driver's response and returning it through an **HRESULT** or an output parameter.</span></span> <span data-ttu-id="a848a-105">Einige Gerätefunktionen sind jedoch möglicherweise über diese Methoden nicht zugänglich.</span><span class="sxs-lookup"><span data-stu-id="a848a-105">However, some device functions may not be accessible through these methods.</span></span> <span data-ttu-id="a848a-106">Daher unterstützt msdv das Senden von unformatierten AV/C-Befehlen an das Gerät.</span><span class="sxs-lookup"><span data-stu-id="a848a-106">Therefore, MSDV supports sending raw AV/C commands to the device.</span></span>

<span data-ttu-id="a848a-107">Beachten Sie bei der Verwendung dieses Features die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="a848a-107">You should keep the following points in mind when using this feature:</span></span>

-   <span data-ttu-id="a848a-108">Der Befehl wird ohne Fehlerüberprüfung oder Parameter Validierung direkt an das Gerät übergeben.</span><span class="sxs-lookup"><span data-stu-id="a848a-108">The command is passed directly to the device, with no error checking or parameter validation.</span></span> <span data-ttu-id="a848a-109">Aus diesem Grund sollten Sie unformatierte AV/C-Befehle nur dann ausgeben, wenn die DirectShow-Schnittstellen die benötigte Funktionalität nicht implementieren.</span><span class="sxs-lookup"><span data-stu-id="a848a-109">For this reason, you should issue raw AV/C commands only when the DirectShow interfaces do not implement the functionality you need.</span></span>
-   <span data-ttu-id="a848a-110">Alle unformatierten AV/C-Befehle sind synchron.</span><span class="sxs-lookup"><span data-stu-id="a848a-110">All raw AV/C commands are synchronous.</span></span> <span data-ttu-id="a848a-111">Der Thread, der den Befehl ausgibt, blockiert, bis der Befehl zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a848a-111">The thread issuing the command blocks until the command returns.</span></span>
-   <span data-ttu-id="a848a-112">Es kann jeweils nur ein Befehl angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a848a-112">Only one command can be given at a time.</span></span> <span data-ttu-id="a848a-113">Während der Befehl verarbeitet wird, lehnt das Gerät alle zusätzlichen Befehle ab.</span><span class="sxs-lookup"><span data-stu-id="a848a-113">While the command is being processed, the device will reject any additional commands.</span></span>
-   <span data-ttu-id="a848a-114">Der UVC-Treiber unterstützt keine unformatierten AV/C-Befehle.</span><span class="sxs-lookup"><span data-stu-id="a848a-114">The UVC driver does not support raw AV/C commands.</span></span>

<span data-ttu-id="a848a-115">Um einen AV/C-Befehl zu senden, formatieren Sie den Befehl als Bytearray.</span><span class="sxs-lookup"><span data-stu-id="a848a-115">To send an AV/C command, format the command as an array of bytes.</span></span> <span data-ttu-id="a848a-116">Nennen Sie dann [**IAMExtTransport:: gettransportbasicparameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters).</span><span class="sxs-lookup"><span data-stu-id="a848a-116">Then call [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters).</span></span> <span data-ttu-id="a848a-117">Übergeben Sie das ED \_ RAW \_ Ext \_ dev \_ cmd-Flag, die Array Größe und das Array.</span><span class="sxs-lookup"><span data-stu-id="a848a-117">Pass in the ED\_RAW\_EXT\_DEV\_CMD flag, the array size, and the array.</span></span> <span data-ttu-id="a848a-118">Sie müssen die Array Adresse in einen \**lpolestr \** _-Typ umwandeln, da der ursprüngliche Zweck dieses Parameters darin besteht, einen Zeichen folgen Wert zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="a848a-118">You must cast the array address to an \**LPOLESTR\** _ type, because the original purpose of this parameter was to return a string value.</span></span>


```C++
BYTE AvcCmd[] = { ... }; // Contains the AV/C command (not shown)
long cbCmd = sizeof(AvcCmd);
hr = pTransport->GetTransportBasicParameters(
    ED_RAW_EXT_DEV_CMD, 
    &cbCmd,
    (LPOLESTR_) AvcCmd);
```



<span data-ttu-id="a848a-119">Der Inhalt des Arrays wird direkt an das Gerät übermittelt, sodass Sie darauf achten müssen, ihn ordnungsgemäß zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="a848a-119">The contents of the array are passed directly to the device, so you must be careful to format it correctly.</span></span> <span data-ttu-id="a848a-120">Ein Befehl kann auf die Einheit (Camcorder) oder eine Untereinheit (Band oder Kamera) abzielen.</span><span class="sxs-lookup"><span data-stu-id="a848a-120">A command can target the unit (camcorder) or a subunit (tape or camera).</span></span> <span data-ttu-id="a848a-121">Die relevanten Standards sind auf der [1394-Handels Assoziations Website](https://1394ta.org)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a848a-121">The relevant standards are available from the [1394 Trade Association Web site](https://1394ta.org).</span></span>

-   <span data-ttu-id="a848a-122">Allgemeine Spezifikation für den Befehl "AV/C Digital Interface"</span><span class="sxs-lookup"><span data-stu-id="a848a-122">AV/C Digital Interface Command Set General Specification</span></span>
-   <span data-ttu-id="a848a-123">Spezifikation für AV/C-Band Aufzeichnung/-Player-Untereinheit</span><span class="sxs-lookup"><span data-stu-id="a848a-123">AV/C Tape Recorder/Player Subunit Specification</span></span>

<span data-ttu-id="a848a-124">Im ersten Thema wird beschrieben, wie Sie die AV/C-Befehle formatieren und die Unit-Befehle auflisten.</span><span class="sxs-lookup"><span data-stu-id="a848a-124">The former describes how to format AV/C commands and lists the unit commands.</span></span> <span data-ttu-id="a848a-125">In der zweiten Spezifikation werden die Untereinheiten Befehle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a848a-125">The latter specification lists the subunit commands.</span></span>

<span data-ttu-id="a848a-126">Die **gettransportbasicparameters** -Methode gibt möglicherweise einen der folgenden Fehlercodes zurück:</span><span class="sxs-lookup"><span data-stu-id="a848a-126">The **GetTransportBasicParameters** method may return one of the following error codes:</span></span>



| <span data-ttu-id="a848a-127">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="a848a-127">Error Code</span></span>              | <span data-ttu-id="a848a-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a848a-128">Description</span></span>                                                                      |
|-------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a848a-129">Fehler \_ Timeout</span><span class="sxs-lookup"><span data-stu-id="a848a-129">ERROR\_TIMEOUT</span></span>          | <span data-ttu-id="a848a-130">Timeout für den Befehl.</span><span class="sxs-lookup"><span data-stu-id="a848a-130">The command timed out.</span></span>                                                           |
| <span data-ttu-id="a848a-131">Fehler beim Zurücksetzen des Fehlers. \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a848a-131">ERROR\_REQ\_NOT\_ACCEP</span></span>  | <span data-ttu-id="a848a-132">Das Gerät hat den Befehl nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="a848a-132">The device did not accept the command.</span></span>                                           |
| <span data-ttu-id="a848a-133">Fehler \_ nicht \_ unterstützt</span><span class="sxs-lookup"><span data-stu-id="a848a-133">ERROR\_NOT\_SUPPORTED</span></span>   | <span data-ttu-id="a848a-134">Der Befehl wird vom Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a848a-134">The device does not support the command.</span></span>                                         |
| <span data-ttu-id="a848a-135">Fehler \_ Anforderung \_ abgebrochen</span><span class="sxs-lookup"><span data-stu-id="a848a-135">ERROR\_REQUEST\_ABORTED</span></span> | <span data-ttu-id="a848a-136">Der Befehl wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a848a-136">The command was aborted.</span></span> <span data-ttu-id="a848a-137">Der Besitz des Geräts wurde entfernt, oder es ist ein Zurücksetzen des Busses aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a848a-137">Possbly the device was removed or a bus reset occurred.</span></span> |



 

> [!Note]  
> <span data-ttu-id="a848a-138">Diese Fehler werden als Win32-Fehlercodes zurückgegeben, nicht als HRESULTs. Daher sollten Sie diese Werte direkt testen, anstatt die Makros " **erfolgreich** " und " **failed** " zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a848a-138">These errors are returned as Win32 error codes, not HRESULTs, so you should test for these values directly, rather than using the **SUCCEEDED** and **FAILED** macros.</span></span>

 

<span data-ttu-id="a848a-139">Wenn die Methode "S OK" zurückgibt \_ , wird die Antwort vom Gerät in das Array kopiert.</span><span class="sxs-lookup"><span data-stu-id="a848a-139">If the method returns S\_OK, the response from the device is copied into the array.</span></span> <span data-ttu-id="a848a-140">Die Antwort Nutzlast ist möglicherweise größer als der Befehl, daher müssen Sie einen Puffer zuordnen, der groß genug ist, um Sie zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a848a-140">The response payload might be larger than the command, so you must allocate a buffer large enough to hold it.</span></span> <span data-ttu-id="a848a-141">Die maximale Nutzlastgröße beträgt 512 Bytes.</span><span class="sxs-lookup"><span data-stu-id="a848a-141">The maximum payload size is 512 bytes.</span></span> <span data-ttu-id="a848a-142">Beachten Sie, dass der Rückgabewert S \_ OK nicht immer bedeutet, dass das Gerät den Befehl erfolgreich ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="a848a-142">Note that a return value of S\_OK does not always mean the device successfully carried out the command.</span></span> <span data-ttu-id="a848a-143">Die Anwendung muss die Antwort Nutzlast überprüfen, um den Status zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a848a-143">The application must examine the response payload to determine the status.</span></span>

<span data-ttu-id="a848a-144">Das folgende Beispiel zeigt den Befehl für die Suche nach einer absoluten Nachverfolgung der Nachverfolgung:</span><span class="sxs-lookup"><span data-stu-id="a848a-144">The following example shows the command to search for an absolute track number search:</span></span>


```C++
// Set up the ATN search command.
BYTE AvcCmd[] = 
{ 
    0x00,   // ctype = "control"
    0x20,   // subunit_type, subunit_id
    0x52,   // opcode (ATN)
    0x20,   // operand 0 = "search"
    0x00,   // operand 1 = ATN
    0x00,   // operand 2 = ATN
    0x00,   // operand 3 = ATN
    0xFF   //  operand 4 = D-VCR medium type.
};
// Specify a track number.
ULONG ulTrackNumber = track_number; // Specify the track number here.
// Shift over by 1 (LSB of operand 1 is a 1-bit blank flag)
ulTrackNumber = ulTrackNumber << 1; 
// Plug this number into operands 1 - 3.
AvcCmd[4] = (BYTE) (ulTrackNumber & 0x000000FF);
AvcCmd[5] = (BYTE)((ulTrackNumber & 0x0000FF00) >> 8);
AvcCmd[6] = (BYTE)((ulTrackNumber & 0x00FF0000) >> 16);
```



## <a name="related-topics"></a><span data-ttu-id="a848a-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a848a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a848a-146">Steuern eines DV-Camcorder</span><span class="sxs-lookup"><span data-stu-id="a848a-146">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



