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
# <a name="direct3d-device-manager"></a><span data-ttu-id="31933-103">Direct3D Device Manager</span><span class="sxs-lookup"><span data-stu-id="31933-103">Direct3D Device Manager</span></span>

<span data-ttu-id="31933-104">Mit dem Microsoft Direct3D-Geräte-Manager können zwei oder mehr Objekte dasselbe Microsoft Direct3D 9-Gerät gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="31933-104">The Microsoft Direct3D device manager enables two or more objects to share the same Microsoft Direct3D 9 device.</span></span> <span data-ttu-id="31933-105">Ein Objekt fungiert als Besitzer des Direct3D 9-Geräts.</span><span class="sxs-lookup"><span data-stu-id="31933-105">One object acts as the owner of the Direct3D 9 device.</span></span> <span data-ttu-id="31933-106">Zum Freigeben des Geräts erstellt der Besitzer des Geräts den Direct3D-Geräte-Manager.</span><span class="sxs-lookup"><span data-stu-id="31933-106">To share the device, the owner of the device creates the Direct3D device manager.</span></span> <span data-ttu-id="31933-107">Andere Objekte können vom Gerätebesitzer einen Zeiger auf den Geräte-Manager abrufen und dann den Geräte-Manager verwenden, um einen Zeiger auf das Direct3D-Gerät zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="31933-107">Other objects can obtain a pointer to the device manager from the device owner, then use the device manager to get a pointer to the Direct3D device.</span></span> <span data-ttu-id="31933-108">Jedes Objekt, das das Gerät verwendet, verfügt über eine exklusive Sperre, wodurch verhindert wird, dass andere Objekte das Gerät gleichzeitig verwenden.</span><span class="sxs-lookup"><span data-stu-id="31933-108">Any object that uses the device holds an exclusive lock, which prevents other objects from using the device at the same time.</span></span>

> [!Note]  
> <span data-ttu-id="31933-109">Der Direct3D-Device Manager unterstützt nur Direct3D 9-Geräte.</span><span class="sxs-lookup"><span data-stu-id="31933-109">The Direct3D Device Manager supports Direct3D 9 devices only.</span></span> <span data-ttu-id="31933-110">DXGI-Geräte werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="31933-110">It does not support DXGI devices.</span></span>

 

<span data-ttu-id="31933-111">Rufen Sie [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9)auf, um den Direct3D-Geräte-Manager zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="31933-111">To create the Direct3D device manager, call [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span></span> <span data-ttu-id="31933-112">Diese Funktion gibt einen Zeiger auf die [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle des Geräte-Managers zurück, zusammen mit einem Token zum Zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="31933-112">This function returns a pointer to the device manager's [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface, along with a reset token.</span></span> <span data-ttu-id="31933-113">Das Token zum Zurücksetzen ermöglicht dem Besitzer des Direct3D-Geräts das festlegen (und zurücksetzen) des Geräts im Geräte-Manager.</span><span class="sxs-lookup"><span data-stu-id="31933-113">The reset token enables the owner of the Direct3D device to set (and reset) the device on the device manager.</span></span> <span data-ttu-id="31933-114">Um den Geräte-Manager zu initialisieren, nennen Sie [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span><span class="sxs-lookup"><span data-stu-id="31933-114">To initialize the device manager, call [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span></span> <span data-ttu-id="31933-115">Übergeben Sie einen Zeiger auf das Direct3D-Gerät zusammen mit dem Token zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="31933-115">Pass in a pointer to the Direct3D device, along with the reset token.</span></span>

<span data-ttu-id="31933-116">Der folgende Code zeigt, wie der Geräte-Manager erstellt und initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="31933-116">The following code shows how to create and initialize the device manager.</span></span>


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



<span data-ttu-id="31933-117">Der Gerätebesitzer muss eine Möglichkeit bereitstellen, um anderen Objekten einen Zeiger auf die [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="31933-117">The device owner must provide a way for other objects to get a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span> <span data-ttu-id="31933-118">Der Standardmechanismus besteht darin, die [**imfgetservice**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="31933-118">The standard mechanism is to implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span> <span data-ttu-id="31933-119">Die Dienst-GUID ist der Mr- \_ Video \_ Acceleration \_ Service.</span><span class="sxs-lookup"><span data-stu-id="31933-119">The service GUID is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>

<span data-ttu-id="31933-120">Um das Gerät für mehrere Objekte freizugeben, muss jedes Objekt (einschließlich des Besitzers des Geräts) wie folgt über den Geräte-Manager auf das Gerät zugreifen:</span><span class="sxs-lookup"><span data-stu-id="31933-120">To share the device among several objects, each object (including the owner of the device) must access the device through the device manager, as follows:</span></span>

1.  <span data-ttu-id="31933-121">Wenden Sie [**IDirect3DDeviceManager9:: opentovicehandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) an, um ein Handle für das Gerät zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="31933-121">Call [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) to get a handle to the device.</span></span>
2.  <span data-ttu-id="31933-122">Um das Gerät zu verwenden, wenden Sie [**IDirect3DDeviceManager9:: lockdevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) an, und übergeben Sie das Geräte handle.</span><span class="sxs-lookup"><span data-stu-id="31933-122">To use the device, call [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) and pass in the device handle.</span></span> <span data-ttu-id="31933-123">Die-Methode gibt einen Zeiger auf die **IDirect3DDevice9** -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="31933-123">The method returns a pointer to the **IDirect3DDevice9** interface.</span></span> <span data-ttu-id="31933-124">Die-Methode kann je nach dem Wert des *fblock* -Parameters in einem blockierenden Modus oder in einem nicht blockierenden Modus aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="31933-124">The method can be called in a blocking mode or a non-blocking mode, depending on the value of the *fBlock* parameter.</span></span>
3.  <span data-ttu-id="31933-125">Wenn Sie die Verwendung des Geräts abgeschlossen haben, wenden Sie sich an [**IDirect3DDeviceManager9:: UnLockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice).</span><span class="sxs-lookup"><span data-stu-id="31933-125">When you are done using the device, call [**IDirect3DDeviceManager9::UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice).</span></span> <span data-ttu-id="31933-126">Mit dieser Methode wird das Gerät anderen Objekten zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="31933-126">This method makes the device available to other objects.</span></span>
4.  <span data-ttu-id="31933-127">Bevor Sie den Eintrag beenden, wenden Sie [**IDirect3DDeviceManager9:: closedebug-andle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) an, um das Geräte Handle zu schließen.</span><span class="sxs-lookup"><span data-stu-id="31933-127">Before exiting, call [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) to close the device handle.</span></span>

<span data-ttu-id="31933-128">Sie sollten die Geräte Sperre nur bei Verwendung des Geräts aufbewahren, da das halten der Geräte Sperre verhindert, dass andere Objekte das Gerät verwenden.</span><span class="sxs-lookup"><span data-stu-id="31933-128">You should hold the device lock only while using the device, because holding the device lock prevents other objects from using the device.</span></span>

<span data-ttu-id="31933-129">Der Besitzer des Geräts kann jederzeit durch Aufrufen von [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice)zu einem anderen Gerät wechseln, in der Regel, weil das ursprüngliche Gerät verloren gegangen ist.</span><span class="sxs-lookup"><span data-stu-id="31933-129">The owner of the device can switch to another device at any time by calling [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), typically because the original device was lost.</span></span> <span data-ttu-id="31933-130">Geräte Verluste können aus verschiedenen Gründen auftreten, darunter Änderungen in der Monitor Auflösung, Energie Verwaltungs Aktionen, Sperren und Entsperren des Computers usw.</span><span class="sxs-lookup"><span data-stu-id="31933-130">Device loss can occur for various reasons, including changes in the monitor resolution, power management actions, locking and unlocking the computer, and so forth.</span></span> <span data-ttu-id="31933-131">Weitere Informationen finden Sie in der Direct3D-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="31933-131">For more information, see the Direct3D documentation.</span></span>

<span data-ttu-id="31933-132">Die [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) -Methode macht alle zuvor geöffneten Geräte Handles ungültig.</span><span class="sxs-lookup"><span data-stu-id="31933-132">The [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) method invalidates any device handles that were opened previously.</span></span> <span data-ttu-id="31933-133">Wenn ein Geräte Handle ungültig ist, gibt die [**lockdevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) -Methode **DXVA2 \_ E \_ New \_ Video \_ Device** zurück.</span><span class="sxs-lookup"><span data-stu-id="31933-133">When a device handle is invalid, the [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) method returns **DXVA2\_E\_NEW\_VIDEO\_DEVICE**.</span></span> <span data-ttu-id="31933-134">Schließen Sie in diesem Fall das Handle, und rufen Sie [**opendevicehandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) erneut auf, um ein neues Geräte Handle zu erhalten, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="31933-134">If this occurs, close the handle and call [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) again to obtain a new device handle, as shown in the following code.</span></span>

<span data-ttu-id="31933-135">Im folgenden Beispiel wird gezeigt, wie ein Geräte Handle geöffnet und das Gerät gesperrt wird.</span><span class="sxs-lookup"><span data-stu-id="31933-135">The following example shows how to open a device handle and lock the device.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="31933-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="31933-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31933-137">DirectX-Video Beschleunigung 2,0</span><span class="sxs-lookup"><span data-stu-id="31933-137">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 



