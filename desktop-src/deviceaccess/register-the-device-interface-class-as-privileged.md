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
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a>Registrieren der Geräteschnittstelle, wie auf privilegierte apps beschränkt

Anwendungen wird der Zugriff auf benutzerdefinierte Treiberfunktionen verweigert, es sei denn, Ihnen werden Berechtigungen über signierte Geräte Metadaten erteilt. In diesem Thema wird gezeigt, wie Sie die **Eingeschränkte** Eigenschaft hinzufügen, die angibt, dass nur privilegierte apps auf eine Geräteschnittstellen Klasse zugreifen können. Benutzerdefinierte Gerätetreiber müssen über diese Eigenschaft verfügen.

## <a name="instructions"></a>Anweisungen

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a>Festlegen der eingeschränkten Eigenschaft in einer Informationsdatei (INF)

Im `InterfaceInstall32` Abschnitt wird die GUID der Geräteschnittstellen Klasse registriert.

Die Zeilen unter der **AddProperty** -Direktive legen die Eigenschaften der Geräteklasse fest. In der zweiten Zeile wird eine benutzerdefinierte Eigenschaft in einer benutzerdefinierten Eigenschaften Kategorie festgelegt. Die GUID der Eigenschaften Kategorie ist **14c83a99-0b3s-44b7-be4c-a178d3990564**, und der Eigenschafts Bezeichner ist **2**. Der optionale `Flags` Einstiegs Wert ist nicht vorhanden, und der Typ ist **17** (**DEVPROP_TYPE_BOOLEAN**). Der Wert der-Eigenschaft ist **1**.

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

## <a name="remarks"></a>Bemerkungen

Anstelle der **AddInterface** -Direktive kann der Treiber auch die [**ioregisterdeviceinterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) -Routine aufrufen, um die Geräteschnittstellen Klasse zu registrieren.

Sie können auch die eingeschränkte Schnittstellen Eigenschaft festlegen, indem Sie die [**iosetdeviceinterfacepropertydata**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) -Routine aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

[Beispiel für benutzerdefinierten Treiber Zugriff](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware dev Center](/windows-hardware/drivers/)
