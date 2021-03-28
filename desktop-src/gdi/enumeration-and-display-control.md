---
description: Um alle Geräte auf dem Computer aufzulisten, müssen Sie die Funktion "EnumDisplayDevices" aufzählen. Die zurückgegebenen Informationen zeigen auch an, welcher Monitor Teil des Desktops ist.
ms.assetid: 834dee04-66fa-42eb-adff-c08a74c6cea8
title: Enumeration und Anzeige Steuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8cdfd5e3b1c6ebb5ff0d4ebdfa1ab44b45c2c25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041971"
---
# <a name="enumeration-and-display-control"></a><span data-ttu-id="53d4c-104">Enumeration und Anzeige Steuerung</span><span class="sxs-lookup"><span data-stu-id="53d4c-104">Enumeration and Display Control</span></span>

<span data-ttu-id="53d4c-105">Um alle Geräte auf dem Computer aufzulisten, müssen Sie die Funktion " [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) " aufzählen.</span><span class="sxs-lookup"><span data-stu-id="53d4c-105">To enumerate all the devices on the computer, call the [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) function.</span></span> <span data-ttu-id="53d4c-106">Die zurückgegebenen Informationen zeigen auch an, welcher Monitor Teil des Desktops ist.</span><span class="sxs-lookup"><span data-stu-id="53d4c-106">The information that is returned also indicates which monitor is part of the desktop.</span></span>

<span data-ttu-id="53d4c-107">Um die Geräte auf dem Desktop aufzulisten, die einen Clippingbereich überschneiden, können Sie [**enumdisplaymonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors)aufzählen.</span><span class="sxs-lookup"><span data-stu-id="53d4c-107">To enumerate the devices on the desktop that intersect a clipping region, call [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors).</span></span> <span data-ttu-id="53d4c-108">Dadurch wird das Hmonitor-Handle für jeden Monitor zurückgegeben, der mit " [**getmonitorinfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="53d4c-108">This returns the HMONITOR handle to each monitor, which is used with [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span></span> <span data-ttu-id="53d4c-109">Verwenden Sie zum Auflisten aller Geräte auf dem virtuellen Bildschirm " **enumdisplaymonitors**".</span><span class="sxs-lookup"><span data-stu-id="53d4c-109">To enumerate all the devices in the virtual screen, use **EnumDisplayMonitors**.</span></span> <span data-ttu-id="53d4c-110">wie im folgenden Code gezeigt:</span><span class="sxs-lookup"><span data-stu-id="53d4c-110">as shown in the following code:</span></span>


```C++
EnumDisplayMonitors(NULL, NULL, MyInfoEnumProc, 0);  
```



<span data-ttu-id="53d4c-111">Um Informationen zu einem Anzeigegerät zu erhalten, verwenden Sie " [**enumdisplaysettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) " oder " [**enumdisplaysettingsex**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa)".</span><span class="sxs-lookup"><span data-stu-id="53d4c-111">To get information about a display device, use [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) or [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa).</span></span>

<span data-ttu-id="53d4c-112">Die [**changedisplaysettingsex**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) -Funktion wird verwendet, um die Anzeigegeräte auf dem Computer zu steuern.</span><span class="sxs-lookup"><span data-stu-id="53d4c-112">The [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) function is used to control the display devices on the computer.</span></span> <span data-ttu-id="53d4c-113">Sie kann die Konfiguration der Geräte ändern, z. b. die Position eines Monitors auf dem virtuellen Desktop angeben und die Bittiefe der Anzeige ändern.</span><span class="sxs-lookup"><span data-stu-id="53d4c-113">It can modify the configuration of the devices, such as specifying the position of a monitor on the virtual desktop and changing the bit depth of any display.</span></span> <span data-ttu-id="53d4c-114">In der Regel verwendet eine Anwendung diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="53d4c-114">Typically, an application does not use this function.</span></span> <span data-ttu-id="53d4c-115">Zum programmgesteuerten Hinzufügen eines Anzeige Monitors zu einem System mit mehreren Monitoren legen Sie **DEVMODE. dmFields** auf DM \_ -Position fest, und geben Sie eine Position (mithilfe von **DEVMODE. dmposition** ) für den Monitor an, den Sie hinzufügen, der zu mindestens einem Pixel des Anzeige Bereichs eines vorhandenen Monitors gehört.</span><span class="sxs-lookup"><span data-stu-id="53d4c-115">To add a display monitor to a multiple-monitor system programmatically, set **DEVMODE.dmFields** to DM\_POSITION and specify a position (using **DEVMODE.dmPosition** ) for the monitor you are adding that is adjacent to at least one pixel of the display area of an existing monitor.</span></span> <span data-ttu-id="53d4c-116">Legen Sie zum Trennen des Monitors **DEVMODE. dmFields** auf DM \_ -Position fest, und legen Sie **DEVMODE. dmPelsWidth** und **DEVMODE. dmPelsHeight** auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="53d4c-116">To detach the monitor, set **DEVMODE.dmFields** to DM\_POSITION and set **DEVMODE.dmPelsWidth** and **DEVMODE.dmPelsHeight** to zero.</span></span>

<span data-ttu-id="53d4c-117">Der folgende Code veranschaulicht, wie alle sekundären Anzeigegeräte vom Desktop getrennt werden:</span><span class="sxs-lookup"><span data-stu-id="53d4c-117">The following code demonstrates how to detach all secondary display devices from the desktop:</span></span>


```
void DetachDisplay()
{
    BOOL            FoundSecondaryDisp = FALSE;
    DWORD           DispNum = 0;
    DISPLAY_DEVICE  DisplayDevice;
    LONG            Result;
    TCHAR           szTemp[200];
    int             i = 0;
    DEVMODE   defaultMode;

    // initialize DisplayDevice
    ZeroMemory(&DisplayDevice, sizeof(DisplayDevice));
    DisplayDevice.cb = sizeof(DisplayDevice);

    // get all display devices
    while (EnumDisplayDevices(NULL, DispNum, &DisplayDevice, 0))
        {
        ZeroMemory(&defaultMode, sizeof(DEVMODE));
        defaultMode.dmSize = sizeof(DEVMODE);
        if ( !EnumDisplaySettings((LPSTR)DisplayDevice.DeviceName, ENUM_REGISTRY_SETTINGS, &defaultMode) )
                  OutputDebugString("Store default failed\n");

        if ((DisplayDevice.StateFlags & DISPLAY_DEVICE_ATTACHED_TO_DESKTOP) &&
            !(DisplayDevice.StateFlags & DISPLAY_DEVICE_PRIMARY_DEVICE))
            {
            DEVMODE    DevMode;
            ZeroMemory(&DevMode, sizeof(DevMode));
            DevMode.dmSize = sizeof(DevMode);
            DevMode.dmFields = DM_PELSWIDTH | DM_PELSHEIGHT | DM_BITSPERPEL | DM_POSITION
                        | DM_DISPLAYFREQUENCY | DM_DISPLAYFLAGS ;
            Result = ChangeDisplaySettingsEx((LPSTR)DisplayDevice.DeviceName, 
                                            &DevMode,
                                            NULL,
                                            CDS_UPDATEREGISTRY,
                                            NULL);

            //The code below shows how to re-attach the secondary displays to the desktop

            //ChangeDisplaySettingsEx((LPSTR)DisplayDevice.DeviceName,
            //                       &defaultMode,
            //                       NULL,
            //                       CDS_UPDATEREGISTRY,
            //                       NULL);

            }

        // Reinit DisplayDevice just to be extra clean

        ZeroMemory(&DisplayDevice, sizeof(DisplayDevice));
        DisplayDevice.cb = sizeof(DisplayDevice);
        DispNum++;
        } // end while for all display devices
}
```



<span data-ttu-id="53d4c-118">Die Anwendung kann für jedes Anzeigegerät Informationen in der Registrierung speichern, die die Konfigurationsparameter für das Gerät sowie Location-Parameter beschreiben.</span><span class="sxs-lookup"><span data-stu-id="53d4c-118">For each display device, the application can save information in the registry that describes the configuration parameters for the device, as well as location parameters.</span></span> <span data-ttu-id="53d4c-119">Die Anwendung kann auch bestimmen, welche Anzeigen Teil des Desktops sind und welche nicht, über das \_ Flag Anzeigegerät an \_ \_ \_ Desktop in der [**Anzeige \_ Geräte**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) Struktur.</span><span class="sxs-lookup"><span data-stu-id="53d4c-119">The application can also determine which displays are part of the desktop, and which are not, through the DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP flag in the [**DISPLAY\_DEVICE**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) structure.</span></span> <span data-ttu-id="53d4c-120">Nachdem alle Konfigurationsinformationen in der Registrierung gespeichert wurden, kann die Anwendung [**changedisplaysettingsex**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) erneut aufzurufen, um die Einstellungen dynamisch zu ändern, ohne dass ein Neustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="53d4c-120">Once all the configuration information is stored in the registry, the application can call [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) again to dynamically change the settings, with no restart required.</span></span>

 

 



