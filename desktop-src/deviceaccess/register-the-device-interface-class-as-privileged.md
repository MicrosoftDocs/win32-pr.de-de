---
title: Registrieren der Geräteschnittstelle, wie auf privilegierte apps beschränkt
description: In diesem Thema wird gezeigt, wie Sie die eingeschränkte Eigenschaft hinzufügen, die angibt, dass nur privilegierte apps auf eine Geräteschnittstellen Klasse zugreifen können.
ms.assetid: BCEB1FBF-3D3F-45B8-A92B-7C5FBF6745C0
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: e23f8b7f2cc1884e2f878739f56507e79eb1bb69
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039804"
---
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a><span data-ttu-id="a551f-103">Registrieren der Geräteschnittstelle, wie auf privilegierte apps beschränkt</span><span class="sxs-lookup"><span data-stu-id="a551f-103">Register the device interface as restricted to privileged apps</span></span>

<span data-ttu-id="a551f-104">Anwendungen wird der Zugriff auf benutzerdefinierte Treiberfunktionen verweigert, es sei denn, Ihnen werden Berechtigungen über signierte Geräte Metadaten erteilt.</span><span class="sxs-lookup"><span data-stu-id="a551f-104">Applications are denied access to custom driver functionality, unless they're granted permissions through signed device metadata.</span></span> <span data-ttu-id="a551f-105">In diesem Thema wird gezeigt, wie Sie die **Eingeschränkte** Eigenschaft hinzufügen, die angibt, dass nur privilegierte apps auf eine Geräteschnittstellen Klasse zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="a551f-105">This topic shows how to add the **Restricted** property that indicates that only privileged apps can access a device interface class.</span></span> <span data-ttu-id="a551f-106">Benutzerdefinierte Gerätetreiber müssen über diese Eigenschaft verfügen.</span><span class="sxs-lookup"><span data-stu-id="a551f-106">Custom device drivers must have this property.</span></span>

## <a name="instructions"></a><span data-ttu-id="a551f-107">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="a551f-107">Instructions</span></span>

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a><span data-ttu-id="a551f-108">Festlegen der eingeschränkten Eigenschaft in einer Informationsdatei (INF)</span><span class="sxs-lookup"><span data-stu-id="a551f-108">Setting the Restricted property in an information (INF) file</span></span>

<span data-ttu-id="a551f-109">Im `InterfaceInstall32` Abschnitt wird die GUID der Geräteschnittstellen Klasse registriert.</span><span class="sxs-lookup"><span data-stu-id="a551f-109">In the `InterfaceInstall32` section, the GUID of the device interface class is registered.</span></span>

<span data-ttu-id="a551f-110">Die Zeilen unter der **AddProperty** -Direktive legen die Eigenschaften der Geräteklasse fest.</span><span class="sxs-lookup"><span data-stu-id="a551f-110">The lines under the **AddProperty** directive set the device class properties.</span></span> <span data-ttu-id="a551f-111">In der zweiten Zeile wird eine benutzerdefinierte Eigenschaft in einer benutzerdefinierten Eigenschaften Kategorie festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a551f-111">The second line sets a custom property in a custom property category.</span></span> <span data-ttu-id="a551f-112">Die GUID der Eigenschaften Kategorie ist **14c83a99-0b3s-44b7-be4c-a178d3990564**, und der Eigenschafts Bezeichner ist **2**.</span><span class="sxs-lookup"><span data-stu-id="a551f-112">The property-category GUID is **14c83a99-0b3f-44b7-be4c-a178d3990564**, and the property identifier is **2**.</span></span> <span data-ttu-id="a551f-113">Der optionale `Flags` Einstiegs Wert ist nicht vorhanden, und der Typ ist **17** (**DEVPROP_TYPE_BOOLEAN**).</span><span class="sxs-lookup"><span data-stu-id="a551f-113">The optional `Flags` entry value is not present, and the type is **17** (**DEVPROP_TYPE_BOOLEAN**).</span></span> <span data-ttu-id="a551f-114">Der Wert der-Eigenschaft ist **1**.</span><span class="sxs-lookup"><span data-stu-id="a551f-114">The value of the property is **1**.</span></span>

```Text
; Below, {11111111-0000-1111-0000-111111111111} is the GUID of the
; new device interface class in an AddInterface directive



; -- Interface installation
[InterfaceInstall32]
{11111111-0000-1111-0000-111111111111}=NewInterfaceInstall

[NewInterfaceInstall]
AddProperty=PrivilegedProperties

[PrivilegedProperties]
; DEVPKey_DeviceInterfaceClass_Restricted
{14c83a99-0b3f-44b7-be4c-a178d3990564}, 2, 17,,1 ; -- non-zero indicates privileged
```

## <a name="remarks"></a><span data-ttu-id="a551f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a551f-115">Remarks</span></span>

<span data-ttu-id="a551f-116">Anstelle der **AddInterface** -Direktive kann der Treiber auch die [**ioregisterdeviceinterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) -Routine aufrufen, um die Geräteschnittstellen Klasse zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="a551f-116">Instead of the **AddInterface** directive, the driver can also call the [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) routine to register the device interface class.</span></span>

<span data-ttu-id="a551f-117">Sie können auch die eingeschränkte Schnittstellen Eigenschaft festlegen, indem Sie die [**iosetdeviceinterfacepropertydata**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) -Routine aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a551f-117">You can also set the restricted interface property by calling the [**IoSetDeviceInterfacePropertyData**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) routine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a551f-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a551f-118">Related topics</span></span>

<span data-ttu-id="a551f-119">[Beispiel für benutzerdefinierten Treiber Zugriff](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware dev Center](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="a551f-119">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
