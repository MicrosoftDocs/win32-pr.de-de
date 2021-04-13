---
title: API-Funktionen der Software Geräte
description: In diesem Abschnitt werden die Funktionen der Software Geräte-API beschrieben, die von einer Client-App aufgerufen werden
ms.assetid: 68F142A9-08AD-4F74-A0C3-3DCC8F7449B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a3cc9f0cd8b018f40210c434ee22b3512b2e81
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390904"
---
# <a name="software-device-api-functions"></a>API-Funktionen der Software Geräte

In diesem Abschnitt werden die Funktionen der Software Geräte-API beschrieben, die von einer Client-App aufgerufen werden

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                           | BESCHREIBUNG                                                                                                                                                      |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Austausch von "austauschen"**](/windows/win32/api/swdevice/nf-swdevice-swdeviceclose)<br/>                               | Schließt das Handle des Software Geräts. Wenn das Handle geschlossen wird, initiiert PNP den Prozess des Entfernens des Geräts.<br/>                                   |
| [**Rückruf für SW- \_ Geräte \_ Erstellung \_**](/windows/win32/api/swdevice/nc-swdevice-sw_device_create_callback)<br/>    | Bietet ein Gerät, das in der Registrierung unterstützt wird, und ermöglicht dem Aufrufer, dann mit dem *hwaydevice* -handle Aufrufe an die API-Funktionen der Software Geräte zu senden<br/> |
| [**Austauschen von "austauschen"**](/windows/win32/api/swdevice/nf-swdevice-swdevicecreate)<br/>                             | Initiiert die Enumeration eines Software Geräts.<br/>                                                                                                       |
| [**Swap-Lebensdauer**](/windows/win32/api/swdevice/nf-swdevice-swdevicegetlifetime)<br/>                   | Ruft die Lebensdauer eines Software Geräts ab. <br/>                                                                                                              |
| [**' Swap PropertySet '**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacepropertyset)<br/> | Legt die Eigenschaften einer Software Geräteschnittstelle fest. <br/>                                                                                                      |
| [**Austauschen von Austausch Elementen**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfaceregister)<br/>       | Registriert eine Geräteschnittstelle für ein Software Gerät und legt optional Eigenschaften für diese Schnittstelle fest. <br/>                                                 |
| [**Austausch von "austauschen"**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacesetstate)<br/>       | Aktiviert oder deaktiviert eine Geräteschnittstelle für ein Software Gerät. <br/>                                                                                        |
| [**"Devidevicepropertyset"**](/windows/win32/api/swdevice/nf-swdevice-swdevicepropertyset)<br/>                   | Legt Eigenschaften auf einem Software Gerät fest. <br/>                                                                                                                |
| [**Austauschbare Lebensdauer**](/windows/win32/api/swdevice/nf-swdevice-swdevicesetlifetime)<br/>                   | Verwaltet die Lebensdauer eines Software Geräts. <br/>                                                                                                           |
| [**Austausch frei**](/windows/win32/api/swdevice/nf-swdevice-swmemfree)<br/>                                       | Gibt Arbeitsspeicher frei, der von anderen API-Gerätefunktionen zugewiesen wurde<br/>                                                                                      |



 

 

 

[Kommentare zu diesem Thema an Microsoft senden](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bswdevice\swdevice%5D:%20Software%20Device%20API%20Functions%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Kommentare zu diesem Thema an Microsoft senden")