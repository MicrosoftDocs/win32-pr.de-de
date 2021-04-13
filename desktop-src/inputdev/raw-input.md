---
title: Rohdaten Eingabe
description: In diesem Abschnitt wird beschrieben, wie das System unformatierte Eingaben für Ihre Anwendung bereitstellt und wie eine Anwendung diese Eingabe empfängt und verarbeitet.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\rawinput.htm
keywords:
- Windows-Benutzeroberfläche, Benutzereingabe
- Windows-Benutzeroberfläche, Rohdaten Eingabe
- Benutzereingabe, Rohdaten Eingabe
- Erfassen von Benutzereingaben, Rohdaten Eingabe
- Rohdaten Eingabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88de70dd2b635cf7dda90f23686b9916c99be4f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390245"
---
# <a name="raw-input"></a><span data-ttu-id="10763-108">Rohdaten Eingabe</span><span class="sxs-lookup"><span data-stu-id="10763-108">Raw Input</span></span>

<span data-ttu-id="10763-109">In diesem Abschnitt wird beschrieben, wie das System unformatierte Eingaben für Ihre Anwendung bereitstellt und wie eine Anwendung diese Eingabe empfängt und verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="10763-109">This section describes how the system provides raw input to your application and how an application receives and processes that input.</span></span> <span data-ttu-id="10763-110">Unformatierte Eingaben werden manchmal auch als generische Eingaben bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="10763-110">Raw input is sometimes referred to as generic input.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="10763-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="10763-111">In This Section</span></span>



| <span data-ttu-id="10763-112">Name</span><span class="sxs-lookup"><span data-stu-id="10763-112">Name</span></span>                                           | <span data-ttu-id="10763-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10763-113">Description</span></span>                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10763-114">Informationen zu roheingaben</span><span class="sxs-lookup"><span data-stu-id="10763-114">About Raw Input</span></span>](about-raw-input.md)         | <span data-ttu-id="10763-115">Erläutert Benutzereingaben von Geräten wie z. b. Joysticks, Touchscreens und Mikrofonen.</span><span class="sxs-lookup"><span data-stu-id="10763-115">Discusses user-input from devices such as joysticks, touch screens, and microphones.</span></span><br/> |
| [<span data-ttu-id="10763-116">Verwenden von Rohdateneingaben</span><span class="sxs-lookup"><span data-stu-id="10763-116">Using Raw Input</span></span>](using-raw-input.md)         | <span data-ttu-id="10763-117">Stellt Beispielcode für Aufgaben im Zusammenhang mit unformatierten Eingaben bereit.</span><span class="sxs-lookup"><span data-stu-id="10763-117">Provides sample code for tasks relating to raw input.</span></span><br/>                                |
| [<span data-ttu-id="10763-118">Unformatierte Eingabe Referenz</span><span class="sxs-lookup"><span data-stu-id="10763-118">Raw Input Reference</span></span>](raw-input-reference.md) | <span data-ttu-id="10763-119">Enthält die API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="10763-119">Contains the API reference.</span></span><br/>                                                          |



 

### <a name="functions"></a><span data-ttu-id="10763-120">Functions</span><span class="sxs-lookup"><span data-stu-id="10763-120">Functions</span></span>



| <span data-ttu-id="10763-121">Name</span><span class="sxs-lookup"><span data-stu-id="10763-121">Name</span></span>                                                                 | <span data-ttu-id="10763-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10763-122">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10763-123">**"Entfrawinputproc"**</span><span class="sxs-lookup"><span data-stu-id="10763-123">**DefRawInputProc**</span></span>](/windows/win32/api/winuser/nf-winuser-defrawinputproc)                           | <span data-ttu-id="10763-124">Ruft die standardmäßige unformatierte Eingabe Prozedur auf, um die Standard Verarbeitung für alle unformatierten Eingabe Nachrichten bereitzustellen, die eine Anwendung nicht verarbeitet</span><span class="sxs-lookup"><span data-stu-id="10763-124">Calls the default raw input procedure to provide default processing for any raw input messages that an application does not process.</span></span> <span data-ttu-id="10763-125">Diese Funktion stellt sicher, dass jede Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="10763-125">This function ensures that every message is processed.</span></span> <span data-ttu-id="10763-126">[**Defrawinputproc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) wird mit denselben Parametern aufgerufen, die von der Fenster Prozedur empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="10763-126">[**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) is called with the same parameters received by the window procedure.</span></span> <br/> |
| [<span data-ttu-id="10763-127">**Getrawinputbuffer**</span><span class="sxs-lookup"><span data-stu-id="10763-127">**GetRawInputBuffer**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer)                       | <span data-ttu-id="10763-128">Führt einen gepufferten Lesevorgang für die Rohdaten der Eingabe aus.</span><span class="sxs-lookup"><span data-stu-id="10763-128">Performs a buffered read of the raw input data.</span></span><br/>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="10763-129">**Getrawinputdata**</span><span class="sxs-lookup"><span data-stu-id="10763-129">**GetRawInputData**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdata)                           | <span data-ttu-id="10763-130">Ruft die unformatierte Eingabe vom angegebenen Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="10763-130">Gets the raw input from the specified device.</span></span><br/>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="10763-131">**Getrawinputdeaktiviert**</span><span class="sxs-lookup"><span data-stu-id="10763-131">**GetRawInputDeviceInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa)               | <span data-ttu-id="10763-132">Ruft Informationen über das roheingabe Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="10763-132">Gets information about the raw input device.</span></span><br/>                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="10763-133">**Getrawinputdevicelist**</span><span class="sxs-lookup"><span data-stu-id="10763-133">**GetRawInputDeviceList**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)               | <span data-ttu-id="10763-134">Listet die unformatierten Eingabegeräte auf, die mit dem System verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="10763-134">Enumerates the raw input devices attached to the system.</span></span> <br/>                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="10763-135">**Getregisteredrawinputdevices**</span><span class="sxs-lookup"><span data-stu-id="10763-135">**GetRegisteredRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) | <span data-ttu-id="10763-136">Ruft die Informationen zu den unformatierten Eingabegeräten für die aktuelle Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="10763-136">Gets the information about the raw input devices for the current application.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="10763-137">**Registerrawinputdevices**</span><span class="sxs-lookup"><span data-stu-id="10763-137">**RegisterRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)           | <span data-ttu-id="10763-138">Registriert die Geräte, die die Rohdaten für die Eingabe bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="10763-138">Registers the devices that supply the raw input data.</span></span><br/>                                                                                                                                                                                                                                                        |



 

### <a name="macros"></a><span data-ttu-id="10763-139">Makros</span><span class="sxs-lookup"><span data-stu-id="10763-139">Macros</span></span>



| <span data-ttu-id="10763-140">Name</span><span class="sxs-lookup"><span data-stu-id="10763-140">Name</span></span>                                                            | <span data-ttu-id="10763-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10763-141">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10763-142">**GET \_ rawinput \_ Code \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="10763-142">**GET\_RAWINPUT\_CODE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) | <span data-ttu-id="10763-143">Ruft den Eingabecode von *wParam* in der [**WM- \_ Eingabe**](wm-input.md)ab.</span><span class="sxs-lookup"><span data-stu-id="10763-143">Gets the input code from *wParam* in [**WM\_INPUT**](wm-input.md).</span></span><br/>                              |
| [<span data-ttu-id="10763-144">**Nextrawinputblock**</span><span class="sxs-lookup"><span data-stu-id="10763-144">**NEXTRAWINPUTBLOCK**</span></span>](/windows/win32/api/winuser/nf-winuser-nextrawinputblock)                  | <span data-ttu-id="10763-145">Ruft den Speicherort der nächsten-Struktur in einem Array von [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) -Strukturen ab.</span><span class="sxs-lookup"><span data-stu-id="10763-145">Gets the location of the next structure in an array of [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) structures.</span></span> <br/> |



 

### <a name="notifications"></a><span data-ttu-id="10763-146">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="10763-146">Notifications</span></span>



| <span data-ttu-id="10763-147">Name</span><span class="sxs-lookup"><span data-stu-id="10763-147">Name</span></span>                                                        | <span data-ttu-id="10763-148">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10763-148">Description</span></span>                                                          |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="10763-149">**WM- \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="10763-149">**WM\_INPUT**</span></span>](wm-input.md)                               | <span data-ttu-id="10763-150">Wird an das Fenster gesendet, das roheingaben erhält.</span><span class="sxs-lookup"><span data-stu-id="10763-150">Sent to the window that is getting raw input.</span></span> <br/>            |
| [<span data-ttu-id="10763-151">**WM- \_ Eingabe \_ Geräte \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="10763-151">**WM\_INPUT\_DEVICE\_CHANGE**</span></span>](wm-input-device-change.md) | <span data-ttu-id="10763-152">Wird an das Fenster gesendet, das für den Empfang von roheingaben registriert ist.</span><span class="sxs-lookup"><span data-stu-id="10763-152">Sent to the window that registered to receive raw input.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="10763-153">Strukturen</span><span class="sxs-lookup"><span data-stu-id="10763-153">Structures</span></span>



| <span data-ttu-id="10763-154">Name</span><span class="sxs-lookup"><span data-stu-id="10763-154">Name</span></span>                                                            | <span data-ttu-id="10763-155">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10763-155">Description</span></span>                                                                            |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="10763-156">**Rawhid**</span><span class="sxs-lookup"><span data-stu-id="10763-156">**RAWHID**</span></span>](/windows/win32/api/winuser/ns-winuser-rawhid)                                        | <span data-ttu-id="10763-157">Beschreibt das Format der unformatierten Eingabe von einem Eingabegeräte (HID).</span><span class="sxs-lookup"><span data-stu-id="10763-157">Describes the format of the raw input from a Human Interface Device (HID).</span></span> <br/> |
| [<span data-ttu-id="10763-158">**Rawinput**</span><span class="sxs-lookup"><span data-stu-id="10763-158">**RAWINPUT**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinput)                                    | <span data-ttu-id="10763-159">Enthält die unformatierte Eingabe von einem Gerät.</span><span class="sxs-lookup"><span data-stu-id="10763-159">Contains the raw input from a device.</span></span> <br/>                                      |
| [<span data-ttu-id="10763-160">**RAWINPUTDEVICE**</span><span class="sxs-lookup"><span data-stu-id="10763-160">**RAWINPUTDEVICE**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevice)                        | <span data-ttu-id="10763-161">Definiert Informationen für die unformatierten Eingabegeräte.</span><span class="sxs-lookup"><span data-stu-id="10763-161">Defines information for the raw input devices.</span></span> <br/>                             |
| [<span data-ttu-id="10763-162">**Rawinputdevicelist**</span><span class="sxs-lookup"><span data-stu-id="10763-162">**RAWINPUTDEVICELIST**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevicelist)                | <span data-ttu-id="10763-163">Enthält Informationen zu einem unformatierten Eingabegerät.</span><span class="sxs-lookup"><span data-stu-id="10763-163">Contains information about a raw input device.</span></span><br/>                              |
| [<span data-ttu-id="10763-164">**Rawinpuderader**</span><span class="sxs-lookup"><span data-stu-id="10763-164">**RAWINPUTHEADER**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputheader)                        | <span data-ttu-id="10763-165">Enthält die Header Informationen, die Teil der Rohdaten für die Eingabe sind.</span><span class="sxs-lookup"><span data-stu-id="10763-165">Contains the header information that is part of the raw input data.</span></span> <br/>        |
| [<span data-ttu-id="10763-166">**Rawkeyboard**</span><span class="sxs-lookup"><span data-stu-id="10763-166">**RAWKEYBOARD**</span></span>](/windows/win32/api/winuser/ns-winuser-rawkeyboard)                              | <span data-ttu-id="10763-167">Enthält Informationen zum Zustand der Tastatur.</span><span class="sxs-lookup"><span data-stu-id="10763-167">Contains information about the state of the keyboard.</span></span> <br/>                      |
| [<span data-ttu-id="10763-168">**Rawmouse**</span><span class="sxs-lookup"><span data-stu-id="10763-168">**RAWMOUSE**</span></span>](/windows/win32/api/winuser/ns-winuser-rawmouse)                                    | <span data-ttu-id="10763-169">Enthält Informationen über den Zustand der Maus.</span><span class="sxs-lookup"><span data-stu-id="10763-169">Contains information about the state of the mouse.</span></span> <br/>                         |
| [<span data-ttu-id="10763-170">**Info zum RID- \_ Gerät \_**</span><span class="sxs-lookup"><span data-stu-id="10763-170">**RID\_DEVICE\_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info)                    | <span data-ttu-id="10763-171">Definiert die unformatierten Eingabedaten, die von einem beliebigen Gerät stammen.</span><span class="sxs-lookup"><span data-stu-id="10763-171">Defines the raw input data coming from any device.</span></span> <br/>                         |
| [<span data-ttu-id="10763-172">**Rid- \_ Geräte \_ Informationen \_ verborgen**</span><span class="sxs-lookup"><span data-stu-id="10763-172">**RID\_DEVICE\_INFO\_HID**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_hid)           | <span data-ttu-id="10763-173">Definiert die unformatierten Eingabedaten, die aus dem angegebenen HID stammen.</span><span class="sxs-lookup"><span data-stu-id="10763-173">Defines the raw input data coming from the specified HID.</span></span> <br/>                  |
| [<span data-ttu-id="10763-174">**\_ \_ Info \_ Tastatur für Rid-Gerät**</span><span class="sxs-lookup"><span data-stu-id="10763-174">**RID\_DEVICE\_INFO\_KEYBOARD**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_keyboard) | <span data-ttu-id="10763-175">Definiert die unformatierten Eingabedaten, die von der angegebenen Tastatur stammen.</span><span class="sxs-lookup"><span data-stu-id="10763-175">Defines the raw input data coming from the specified keyboard.</span></span> <br/>             |
| [<span data-ttu-id="10763-176">**Info-Maus des RID- \_ Geräts \_ \_**</span><span class="sxs-lookup"><span data-stu-id="10763-176">**RID\_DEVICE\_INFO\_MOUSE**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_mouse)       | <span data-ttu-id="10763-177">Definiert die unformatierten Eingabedaten, die von der angegebenen Maus stammen.</span><span class="sxs-lookup"><span data-stu-id="10763-177">Defines the raw input data coming from the specified mouse.</span></span><br/>                 |



 

 

