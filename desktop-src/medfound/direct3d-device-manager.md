---
description: Direct3D Device Manager
ms.assetid: d82fd82d-510e-4004-b18b-8f2372e29701
title: Direct3D Device Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aeff41b790df9537854ab715724d95cee646168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342508"
---
# <a name="direct3d-device-manager"></a>Direct3D Device Manager

Mit dem Microsoft Direct3D-Geräte-Manager können zwei oder mehr Objekte dasselbe Microsoft Direct3D 9-Gerät gemeinsam verwenden. Ein Objekt fungiert als Besitzer des Direct3D 9-Geräts. Zum Freigeben des Geräts erstellt der Besitzer des Geräts den Direct3D-Geräte-Manager. Andere Objekte können vom Gerätebesitzer einen Zeiger auf den Geräte-Manager abrufen und dann den Geräte-Manager verwenden, um einen Zeiger auf das Direct3D-Gerät zu erhalten. Jedes Objekt, das das Gerät verwendet, verfügt über eine exklusive Sperre, wodurch verhindert wird, dass andere Objekte das Gerät gleichzeitig verwenden.

> [!Note]  
> Der Direct3D-Device Manager unterstützt nur Direct3D 9-Geräte. DXGI-Geräte werden nicht unterstützt.

 

Rufen Sie [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9)auf, um den Direct3D-Geräte-Manager zu erstellen. Diese Funktion gibt einen Zeiger auf die [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle des Geräte-Managers zurück, zusammen mit einem Token zum Zurücksetzen. Das Token zum Zurücksetzen ermöglicht dem Besitzer des Direct3D-Geräts das festlegen (und zurücksetzen) des Geräts im Geräte-Manager. Um den Geräte-Manager zu initialisieren, nennen Sie [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice). Übergeben Sie einen Zeiger auf das Direct3D-Gerät zusammen mit dem Token zurücksetzen.

Der folgende Code zeigt, wie der Geräte-Manager erstellt und initialisiert wird.


```C++
HRESULT CreateD3DDeviceManager(
    IDirect3DDevice9 *pDevice, 
    UINT *pReset, 
    IDirect3DDeviceManager9 **ppManager
    )
{
    UINT resetToken = 0;

    IDirect3DDeviceManager9 *pD3DManager = NULL;

    HRESULT hr = DXVA2CreateDirect3DDeviceManager9(&resetToken, &pD3DManager);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pD3DManager->ResetDevice(pDevice, resetToken);

    if (FAILED(hr))
    {
        goto done;
    }

    *ppManager = pD3DManager;
    (*ppManager)->AddRef();

    *pReset = resetToken;


done:
    SafeRelease(&pD3DManager);
    return hr;
}
```



Der Gerätebesitzer muss eine Möglichkeit bereitstellen, um anderen Objekten einen Zeiger auf die [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle zu erhalten. Der Standardmechanismus besteht darin, die [**imfgetservice**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle zu implementieren. Die Dienst-GUID ist der Mr- \_ Video \_ Acceleration \_ Service.

Um das Gerät für mehrere Objekte freizugeben, muss jedes Objekt (einschließlich des Besitzers des Geräts) wie folgt über den Geräte-Manager auf das Gerät zugreifen:

1.  Wenden Sie [**IDirect3DDeviceManager9:: opentovicehandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) an, um ein Handle für das Gerät zu erhalten.
2.  Um das Gerät zu verwenden, wenden Sie [**IDirect3DDeviceManager9:: lockdevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) an, und übergeben Sie das Geräte handle. Die-Methode gibt einen Zeiger auf die **IDirect3DDevice9** -Schnittstelle zurück. Die-Methode kann je nach dem Wert des *fblock* -Parameters in einem blockierenden Modus oder in einem nicht blockierenden Modus aufgerufen werden.
3.  Wenn Sie die Verwendung des Geräts abgeschlossen haben, wenden Sie sich an [**IDirect3DDeviceManager9:: UnLockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice). Mit dieser Methode wird das Gerät anderen Objekten zur Verfügung gestellt.
4.  Bevor Sie den Eintrag beenden, wenden Sie [**IDirect3DDeviceManager9:: closedebug-andle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) an, um das Geräte Handle zu schließen.

Sie sollten die Geräte Sperre nur bei Verwendung des Geräts aufbewahren, da das halten der Geräte Sperre verhindert, dass andere Objekte das Gerät verwenden.

Der Besitzer des Geräts kann jederzeit durch Aufrufen von [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice)zu einem anderen Gerät wechseln, in der Regel, weil das ursprüngliche Gerät verloren gegangen ist. Geräte Verluste können aus verschiedenen Gründen auftreten, darunter Änderungen in der Monitor Auflösung, Energie Verwaltungs Aktionen, Sperren und Entsperren des Computers usw. Weitere Informationen finden Sie in der Direct3D-Dokumentation.

Die [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) -Methode macht alle zuvor geöffneten Geräte Handles ungültig. Wenn ein Geräte Handle ungültig ist, gibt die [**lockdevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) -Methode **DXVA2 \_ E \_ New \_ Video \_ Device** zurück. Schließen Sie in diesem Fall das Handle, und rufen Sie [**opendevicehandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) erneut auf, um ein neues Geräte Handle zu erhalten, wie im folgenden Code gezeigt.

Im folgenden Beispiel wird gezeigt, wie ein Geräte Handle geöffnet und das Gerät gesperrt wird.


```C++
HRESULT LockDevice(
    IDirect3DDeviceManager9 *pDeviceManager,
    BOOL fBlock,
    IDirect3DDevice9 **ppDevice, // Receives a pointer to the device.
    HANDLE *pHandle              // Receives a device handle.   
    )
{
    *pHandle = NULL;
    *ppDevice = NULL;

    HANDLE hDevice = 0;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);

    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->LockDevice(hDevice, ppDevice, fBlock);
    }

    if (hr == DXVA2_E_NEW_VIDEO_DEVICE)
    {
        // Invalid device handle. Try to open a new device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (SUCCEEDED(hr))
        {
            hr = pDeviceManager->OpenDeviceHandle(&hDevice);
        }

        // Try to lock the device again.
        if (SUCCEEDED(hr))
        {
            hr = pDeviceManager->LockDevice(hDevice, ppDevice, TRUE); 
        }
    }

    if (SUCCEEDED(hr))
    {
        *pHandle = hDevice;
    }
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Video Beschleunigung 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 



