---
title: Registrieren der Geräteschnittstelle als auf privilegierte Apps beschränkt
description: In diesem Thema wird gezeigt, wie Sie die Restricted-Eigenschaft hinzufügen, die angibt, dass nur privilegierte Apps auf eine Geräteschnittstellenklasse zugreifen können.
ms.assetid: BCEB1FBF-3D3F-45B8-A92B-7C5FBF6745C0
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 62bca034a2edab9b31267f14672b4821ca6569dead0fd645d98c52c234c24cb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029050"
---
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a>Registrieren der Geräteschnittstelle als auf privilegierte Apps beschränkt

Anwendungen wird der Zugriff auf benutzerdefinierte Treiberfunktionen verweigert, es sei denn, ihnen werden Berechtigungen über signierte Gerätemetadaten erteilt. In diesem Thema wird gezeigt, wie Sie die **Restricted-Eigenschaft** hinzufügen, die angibt, dass nur privilegierte Apps auf eine Geräteschnittstellenklasse zugreifen können. Benutzerdefinierte Gerätetreiber müssen über diese Eigenschaft verfügen.

## <a name="instructions"></a>Anweisungen

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a>Festlegen der Restricted-Eigenschaft in einer Informationsdatei (INF)

Im Abschnitt `InterfaceInstall32` wird die GUID der Geräteschnittstellenklasse registriert.

Die Zeilen unter der **AddProperty-Direktive** legen die Eigenschaften der Geräteklasse fest. Die zweite Zeile legt eine benutzerdefinierte Eigenschaft in einer benutzerdefinierten Eigenschaftenkategorie fest. Die Eigenschaftenkategorie-GUID ist **14c83a99-0b3f-44b7-be4c-a178d3990564,** und der Eigenschaftenbezeichner **ist 2.** Der `Flags` optionale Eingabewert ist nicht vorhanden, und der Typ ist **17** (**DEVPROP_TYPE_BOOLEAN**). Der Wert der -Eigenschaft ist **1.**

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

## <a name="remarks"></a>Hinweise

Anstelle der **AddInterface-Direktive** kann der Treiber auch die [**IoRegisterDeviceInterface-Routine**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) aufrufen, um die Geräteschnittstellenklasse zu registrieren.

Sie können die Eingeschränkte Schnittstelleneigenschaft auch festlegen, indem Sie die [**IoSetDeviceInterfacePropertyData-Routine**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

[Beispiel für benutzerdefinierten Treiberzugriff,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) [UWP-Geräte-Apps für interne Geräte,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Hardware Dev Center](/windows-hardware/drivers/)
