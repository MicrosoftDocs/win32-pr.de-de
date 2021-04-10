---
title: 'COM-Schnittstellen: Gerätezugriff'
description: Component Object Model (com)-Schnittstellen in der Geräte Zugriffs-API.
ms.assetid: 96F532B7-5CF9-4341-932B-7F8BEDA9551F
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 07abbfd15f8383bbbd9cd9d1f5fc4c9fb1f42b9e
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039803"
---
# <a name="com-interfaces---device-access"></a><span data-ttu-id="9e469-103">COM-Schnittstellen: Gerätezugriff</span><span class="sxs-lookup"><span data-stu-id="9e469-103">COM Interfaces - Device Access</span></span>

<span data-ttu-id="9e469-104">Component Object Model (com)-Schnittstellen in der Geräte Zugriffs-API.</span><span class="sxs-lookup"><span data-stu-id="9e469-104">Component Object Model (COM)interfaces in the Device Access API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9e469-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9e469-105">In this section</span></span>

| <span data-ttu-id="9e469-106">Thema</span><span class="sxs-lookup"><span data-stu-id="9e469-106">Topic</span></span> | <span data-ttu-id="9e469-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e469-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="9e469-108">**Ikreatedeviceaccessasync**</span><span class="sxs-lookup"><span data-stu-id="9e469-108">**ICreateDeviceAccessAsync**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)<br/> | <span data-ttu-id="9e469-109">Die [**ikreatedeviceaccessasync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) -Schnittstelle wird von einem aufzurufenden aufrufswert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9e469-109">The [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) interface is returned from a call to CreateDeviceAccessInstance.</span></span> <span data-ttu-id="9e469-110">Sie ermöglicht es dem Aufrufer, den Vorgang der Bindung an eine Instanz eines Geräts zu steuern, um eine andere Schnittstelle abzurufen, die für die Interaktion mit dem Gerät verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9e469-110">It enables the caller to control the operation of binding to an instance of a device in order to retrieve another interface that can be used to interact with that device.</span></span><br/> |
| [<span data-ttu-id="9e469-111">**Ideviceiocontrol**</span><span class="sxs-lookup"><span data-stu-id="9e469-111">**IDeviceIoControl**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)<br/> | <span data-ttu-id="9e469-112">Sendet einen Steuerungs Code an einen Gerätetreiber. Diese Aktion bewirkt, dass das Gerät den entsprechenden Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="9e469-112">Sends a control code to a device driver.This action causes the device to perform the corresponding operation.</span></span> <br/> |
| [<span data-ttu-id="9e469-113">**Idevicerequestcompletioncallback**</span><span class="sxs-lookup"><span data-stu-id="9e469-113">**IDeviceRequestCompletionCallback**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)<br/> | <span data-ttu-id="9e469-114">Stellt eine Methode bereit, mit der der Abschluss von Aufrufen der [**deviceiocontrolasync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)-Methode behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e469-114">Provides a method to handle the completion of calls to the [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)method.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="9e469-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9e469-115">Related topics</span></span>

<span data-ttu-id="9e469-116">[Beispiel für benutzerdefinierten Treiber Zugriff](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware dev Center](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="9e469-116">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
