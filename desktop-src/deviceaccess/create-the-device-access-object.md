---
title: Implementieren des Geräte Zugriffs Objekts
description: In diesem Thema wird erläutert, wie das Geräte Zugriffs Objekt instanziiert und für den Zugriff auf ein Gerät verwendet wird.
ms.assetid: 26619A25-67FE-44DC-82DD-36076326748D
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 60bd634f72b29bb6520223a7933b22a396f99723
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104474596"
---
# <a name="implement-the-device-access-object"></a>Implementieren des Geräte Zugriffs Objekts

In diesem Thema wird erläutert, wie das Geräte Zugriffs Objekt instanziiert und für den Zugriff auf ein Gerät verwendet wird. Die instanziierte Klasse implementiert die Schnittstellen [**ideviceiocontrol**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) und [**ikreatedeviceaccessasync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) .

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1

Um das Geräte Zugriffs Objekt zu instanziieren, müssen Sie zuerst die Funktion " [**devatedeviceaccessinstance**](/windows/win32/api/deviceaccess/nf-deviceaccess-createdeviceaccessinstance) " aufrufen. Wenn " **deatedeviceaccessinstance** " erfolgreich ist, können Sie die [**Wait**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-wait) -Methode aufrufen, um zu warten, bis der asynchrone Vorgang abgeschlossen ist. Wenn der **warte** Vorgang erfolgreich ist, können Sie ein [**ideviceiocontrol**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) -Objekt (oder den entsprechenden Fehler) aus der [**GetResult**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-getresult) -Methode abrufen.

```C++
HRESULT
CMyServer::Initialize(
        PCWSTR   pszDeviceInterfacePath
    )

/*++
Routine Description:

    This routine is called to initialize the Device Access object.
    It's not part of the constructor as the initialization can fail.
    It opens the device and gets the IDeviceIoControl interface to the device instance
    via the broker.

Arguments:
    pszDeviceInterfacePath - the device interface string that needs to be opened

Return Value:

    HRESULT

--*/

{
    HRESULT hr;
    ICreateDeviceAccessAsync *pDeviceAccess;

     //
     // Here's the actual open call.  This will *fail* if your lowbox does
     // not have the capability mapped to the interface class specified.
     // If you are running this as normal user, it will just pass through to
     // create file.
     //

   hr = CreateDeviceAccessInstance(pszDeviceInterfacePath,
                                   GENERIC_READ|GENERIC_WRITE,
                                   &amp;pDeviceAccess);

    if (FAILED(hr)) {
        return hr;
    }

    if (SUCCEEDED(hr)) {
        hr = pDeviceAccess->Wait(INFINITE);
    }

    if (SUCCEEDED(hr)) {
        hr = pDeviceAccess->GetResult(IID_IDeviceIoControl,
                                            (void **)&amp;m_pDeviceIoControl);
    }

    pDeviceAccess->Release();

    return hr;
}
```



### <a name="step-2"></a>Schritt 2

Dies ist ein Beispiel für einen Aufrufs der **deviceiocontrolsync** -Methode.


```C++
IFACEMETHODIMP 
CMyServer::put_SevenSegmentDisplay(
    BYTE   value
    )
/*++

Routine Description:
    This routine puts the display value into the device.

Arguments:
    
    value - The value to be written to the device.
    
Return Value:

    HRESULT

--*/
{
    BYTE sevenSegment = 0;
    HRESULT hr;

    if (value >= ARRAYSIZE(g_NumberToMask)) {
        return E_INVALIDARG;
    }


    sevenSegment = g_NumberToMask[value];
    hr = m_pDeviceIoControl->DeviceIoControlSync(
                         IOCTL_OSRUSBFX2_SET_7_SEGMENT_DISPLAY,
                         &amp;sevenSegment,
                         sizeof(BYTE),
                         NULL,
                         0,
                         NULL
                         );

    return hr;
}
```



## <a name="remarks"></a>Bemerkungen

Sie können ioctl auch asynchron mithilfe der [**deviceiocontrolasync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync) -Methode senden. In diesem Fall müssen Sie die [**idevicerequestcompletioncallback**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback) -Schnittstelle implementieren.

## <a name="related-topics"></a>Zugehörige Themen

[Beispiel für benutzerdefinierten Treiber Zugriff](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware dev Center](/windows-hardware/drivers/)
