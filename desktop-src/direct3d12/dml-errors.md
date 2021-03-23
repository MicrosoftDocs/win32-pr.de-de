---
title: Behandeln von Fehlern und Entfernen von Geräten in der directml
description: In diesem Thema wird erläutert, wie Sie das Entfernen von Geräte-und anderen Fehlerzuständen in directml Debuggen.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b4567558b8b75685db16796e921f3daf35b849a1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548684"
---
# <a name="handling-errors-and-device-removal-in-directml"></a><span data-ttu-id="a865c-103">Behandeln von Fehlern und Entfernen von Geräten in der directml</span><span class="sxs-lookup"><span data-stu-id="a865c-103">Handling errors and device-removal in DirectML</span></span>

## <a name="device-removal"></a><span data-ttu-id="a865c-104">Gerät-entfernen</span><span class="sxs-lookup"><span data-stu-id="a865c-104">Device-removal</span></span>

<span data-ttu-id="a865c-105">Wenn ein nicht BEHEB barer Fehler auftritt, kann das directml-Gerät in den Zustand "Gerät entfernt" wechseln.</span><span class="sxs-lookup"><span data-stu-id="a865c-105">If an unrecoverable error occurs, the DirectML device may enter a "device-removed" state.</span></span> <span data-ttu-id="a865c-106">Nicht BEHEB Bare Fehler, die das Entfernen von Geräten bewirken, beinhalten eine ungültige API-Verwendung (bei Methoden, die kein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)zurückgeben), Treiber Fehler, Hardwarefehler oder OOM-Bedingungen (Out-of-Memory).</span><span class="sxs-lookup"><span data-stu-id="a865c-106">Unrecoverable errors that cause device-removal include invalid API usage (for methods that don't return an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)), driver error, hardware fault, or out-of-memory (OOM) conditions.</span></span>

<span data-ttu-id="a865c-107">Wenn ein directml-Gerät entfernt wird, werden alle Methodenaufrufe auf dem Gerät und alle von diesem Gerät erstellten Objekte.</span><span class="sxs-lookup"><span data-stu-id="a865c-107">When a DirectML device is removed, all method calls on the device, and every object created by that device, become no-ops.</span></span> <span data-ttu-id="a865c-108">Bei Methoden, die ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)zurückgeben, wird ein [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a865c-108">For methods that return an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes), a [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) error code is returned.</span></span> <span data-ttu-id="a865c-109">Sie können die [ **idmldevice:: getdeviceremovedreason** -Methode](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) verwenden, um zu überprüfen, ob das directml-Gerät entfernt wurde, und um einen ausführlicheren Fehlercode abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a865c-109">You can use the [**IDMLDevice::GetDeviceRemovedReason** method](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) to check whether the DirectML device has been removed, and to retrieve a more detailed error code.</span></span>

<span data-ttu-id="a865c-110">Sie können keine Wiederherstellung von der Geräte Entfernung durchführt, außer indem Sie das betroffene Gerät und alle ihm untergeordneten Elemente freigeben und dann das directml-Gerät von Grund auf neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a865c-110">You can't recover from device-removal except by releasing the affected device and all its children, then re-creating the DirectML device from scratch.</span></span>

<span data-ttu-id="a865c-111">Wenn das zugrunde liegende Direct3D 12-Gerät entfernt wird, wird auch das directml-Gerät entfernt.</span><span class="sxs-lookup"><span data-stu-id="a865c-111">Device-removal of the underlying Direct3D 12 device also causes the DirectML device to be removed.</span></span> <span data-ttu-id="a865c-112">Umgekehrt ist dies jedoch nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="a865c-112">However, the reverse is not true.</span></span> <span data-ttu-id="a865c-113">Das Entfernen von directml-Geräten bewirkt möglicherweise nicht notwendigerweise, dass das zugrunde liegende Direct3D 12-Gerät entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="a865c-113">DirectML device-removal may not necessarily cause the underlying Direct3D 12 device to become removed.</span></span>

## <a name="debugging-directml-device-removal-and-other-errors"></a><span data-ttu-id="a865c-114">Debuggen der directml-Geräte Löschung und anderer Fehler</span><span class="sxs-lookup"><span data-stu-id="a865c-114">Debugging DirectML device-removal, and other errors</span></span>

<span data-ttu-id="a865c-115">Die häufigste Ursache für directml-Fehler ist die ungültige API-Verwendung.</span><span class="sxs-lookup"><span data-stu-id="a865c-115">The most common cause of DirectML errors is invalid API usage.</span></span> <span data-ttu-id="a865c-116">Eine ungültige API-Verwendung kann zu einem **E_INVALIDARG** HRESULT-Fehlercode führen, oder es kann zu einem Geräte Entfernungs Vorgang führen.</span><span class="sxs-lookup"><span data-stu-id="a865c-116">Invalid API usage might result in an **E_INVALIDARG** HRESULT error code, or it might result in device-removal.</span></span>

<span data-ttu-id="a865c-117">Es wird dringend empfohlen, die [directml-debugschicht](dml-debug-layer.md) während der Entwicklung zu aktivieren, um solche Fehler zu erfassen und zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="a865c-117">We strongly recommend that you enable the [DirectML debug layer](dml-debug-layer.md) during your development, in order to catch and debug such errors.</span></span> <span data-ttu-id="a865c-118">Die directml-debugschicht führt eine umfassende Validierung von Methoden Parametern und API-Verwendung durch und gibt debugausgabenachrichten aus, die Sie beim Debuggen unterstützen</span><span class="sxs-lookup"><span data-stu-id="a865c-118">The DirectML debug layer performs extensive validation of method parameters and API usage, and it will emit debug output messages to help you debug.</span></span>

## <a name="see-also"></a><span data-ttu-id="a865c-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a865c-119">See also</span></span>

* [<span data-ttu-id="a865c-120">Verwenden der directml-debugschicht</span><span class="sxs-lookup"><span data-stu-id="a865c-120">Using the DirectML debug layer</span></span>](dml-debug-layer.md)
