---
title: Funktionen der Softwaregeräte-API
description: In diesem Abschnitt werden funktionen der Softwaregeräte-API beschrieben, die eine Client-App aufruft, und eine Rückruffunktion, die von einer Client-App implementiert wird.
ms.assetid: 68F142A9-08AD-4F74-A0C3-3DCC8F7449B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f5d525eb9a4d4bc9af4807a2b3ad069b109b17874040e84cb3a9059d31bb85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937090"
---
# <a name="software-device-api-functions"></a>Funktionen der Softwaregeräte-API

In diesem Abschnitt werden funktionen der Softwaregeräte-API beschrieben, die eine Client-App aufruft, und eine Rückruffunktion, die von einer Client-App implementiert wird.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                           | Beschreibung                                                                                                                                                      |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SwDeviceClose**](/windows/win32/api/swdevice/nf-swdevice-swdeviceclose)<br/>                               | Schließt das Softwaregerätehandle. Wenn das Handle geschlossen wird, initiiert PnP den Vorgang zum Entfernen des Geräts.<br/>                                   |
| [**SW \_ DEVICE \_ CREATE \_ CALLBACK**](/windows/win32/api/swdevice/nc-swdevice-sw_device_create_callback)<br/>    | Stellt ein Gerät mit Unterstützung in der Registrierung bereit und ermöglicht es dem Aufrufer, dann Aufrufe an Funktionen der Softwaregeräte-API mit dem *hSwDevice-Handle* vorzunehmen.<br/> |
| [**SwDeviceCreate**](/windows/win32/api/swdevice/nf-swdevice-swdevicecreate)<br/>                             | Initiiert die Enumeration eines Softwaregeräts.<br/>                                                                                                       |
| [**SwDeviceGetLifetime**](/windows/win32/api/swdevice/nf-swdevice-swdevicegetlifetime)<br/>                   | Ruft die Lebensdauer eines Softwaregeräts ab. <br/>                                                                                                              |
| [**SwDeviceInterfacePropertySet**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacepropertyset)<br/> | Legt Eigenschaften für eine Softwaregeräteschnittstelle fest. <br/>                                                                                                      |
| [**SwDeviceInterfaceRegister**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfaceregister)<br/>       | Registriert eine Geräteschnittstelle für ein Softwaregerät und legt optional Eigenschaften für diese Schnittstelle fest. <br/>                                                 |
| [**SwDeviceInterfaceSetState**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacesetstate)<br/>       | Aktiviert oder deaktiviert eine Geräteschnittstelle für ein Softwaregerät. <br/>                                                                                        |
| [**SwDevicePropertySet**](/windows/win32/api/swdevice/nf-swdevice-swdevicepropertyset)<br/>                   | Legt Eigenschaften auf einem Softwaregerät fest. <br/>                                                                                                                |
| [**SwDeviceSetLifetime**](/windows/win32/api/swdevice/nf-swdevice-swdevicesetlifetime)<br/>                   | Verwaltet die Lebensdauer eines Softwaregeräts. <br/>                                                                                                           |
| [**SwMemFree**](/windows/win32/api/swdevice/nf-swdevice-swmemfree)<br/>                                       | Gibt Arbeitsspeicher frei, den andere Funktionen der Softwaregeräte-API zugeordnet haben.<br/>                                                                                      |



 

 

 

[Senden von Kommentaren zu diesem Thema an Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bswdevice\swdevice%5D:%20Software%20Device%20API%20Functions%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Senden von Kommentaren zu diesem Thema an Microsoft")