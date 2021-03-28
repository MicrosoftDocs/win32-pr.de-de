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
# <a name="enumeration-and-display-control"></a>Enumeration und Anzeige Steuerung

Um alle Geräte auf dem Computer aufzulisten, müssen Sie die Funktion " [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) " aufzählen. Die zurückgegebenen Informationen zeigen auch an, welcher Monitor Teil des Desktops ist.

Um die Geräte auf dem Desktop aufzulisten, die einen Clippingbereich überschneiden, können Sie [**enumdisplaymonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors)aufzählen. Dadurch wird das Hmonitor-Handle für jeden Monitor zurückgegeben, der mit " [**getmonitorinfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)" verwendet wird. Verwenden Sie zum Auflisten aller Geräte auf dem virtuellen Bildschirm " **enumdisplaymonitors**". wie im folgenden Code gezeigt:


```C++
EnumDisplayMonitors(NULL, NULL, MyInfoEnumProc, 0);  
```



Um Informationen zu einem Anzeigegerät zu erhalten, verwenden Sie " [**enumdisplaysettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) " oder " [**enumdisplaysettingsex**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa)".

Die [**changedisplaysettingsex**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) -Funktion wird verwendet, um die Anzeigegeräte auf dem Computer zu steuern. Sie kann die Konfiguration der Geräte ändern, z. b. die Position eines Monitors auf dem virtuellen Desktop angeben und die Bittiefe der Anzeige ändern. In der Regel verwendet eine Anwendung diese Funktion nicht. Zum programmgesteuerten Hinzufügen eines Anzeige Monitors zu einem System mit mehreren Monitoren legen Sie **DEVMODE. dmFields** auf DM \_ -Position fest, und geben Sie eine Position (mithilfe von **DEVMODE. dmposition** ) für den Monitor an, den Sie hinzufügen, der zu mindestens einem Pixel des Anzeige Bereichs eines vorhandenen Monitors gehört. Legen Sie zum Trennen des Monitors **DEVMODE. dmFields** auf DM \_ -Position fest, und legen Sie **DEVMODE. dmPelsWidth** und **DEVMODE. dmPelsHeight** auf 0 (null) fest.

Der folgende Code veranschaulicht, wie alle sekundären Anzeigegeräte vom Desktop getrennt werden:


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



Die Anwendung kann für jedes Anzeigegerät Informationen in der Registrierung speichern, die die Konfigurationsparameter für das Gerät sowie Location-Parameter beschreiben. Die Anwendung kann auch bestimmen, welche Anzeigen Teil des Desktops sind und welche nicht, über das \_ Flag Anzeigegerät an \_ \_ \_ Desktop in der [**Anzeige \_ Geräte**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) Struktur. Nachdem alle Konfigurationsinformationen in der Registrierung gespeichert wurden, kann die Anwendung [**changedisplaysettingsex**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) erneut aufzurufen, um die Einstellungen dynamisch zu ändern, ohne dass ein Neustart erforderlich ist.

 

 



