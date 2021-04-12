---
title: Difxapi.h
description: Dieser Abschnitt enthält Referenz Themen für den "difxapi. h"-Header.
ms.assetid: 84da7e54-0677-495e-9dc5-aca4ac12c0b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c549ed3fd781d9fde4e6ab48703e1df425986d0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209260"
---
# <a name="difxapih"></a>Difxapi.h

Dieser Abschnitt enthält Referenz Themen für den "difxapi. h"-Header.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*Diflogcallback*](/previous-versions/windows/hardware/difxapi/diflogcallback)<br/>                     | Eine **diflogcallback**-typisierte Funktion ist eine von der Anwendung bereitgestellte Rückruffunktion, die von einer Anwendung durch Aufrufen von [**setdifxlogcallback**](/previous-versions/windows/hardware/difxapi/setdifxlogcallback)registriert wird. Difxapi Ruft die Rückruffunktion auf, um Ereignisse zu protokollieren, die beim Vorgang "difxapi" auftreten.<br/>                        |
| [*Difxapilogcallback*](/previous-versions/windows/hardware/difxapi/difxapilogcallback)<br/>             | Eine **difxapilogcallback**-typisierte Funktion ist eine von der Anwendung bereitgestellte Rückruffunktion, die eine Anwendung durch Aufrufen von [**difxapisetlogcallback**](/previous-versions/windows/hardware/difxapi/difxapisetlogcallback)bei difxapi registriert. Difxapi Ruft die Rückruffunktion auf, um Ereignisse zu protokollieren, die beim Vorgang "difxapi" auftreten.<br/> |
| [**Difxapisetlogcallback**](/previous-versions/windows/hardware/difxapi/difxapisetlogcallback)<br/>     | Die **difxapisetlogcallback** -Funktion registriert eine vom Aufrufer bereitgestellte Rückruffunktion, die von difxapi aufgerufen wird, um Informationen über Ereignisse zu protokollieren, die während der Ausführung von difxapi <br/>                                                                                                            |
| [**DriverPackageGetPath**](/previous-versions/windows/hardware/difxapi/driverpackagegetpath)<br/>       | Die **DriverPackageGetPath** -Funktion Ruft den voll qualifizierten Pfad der [INF-Datei](/windows-hardware/drivers/install/overview-of-inf-files) für ein vorinstalliertes [Treiber Paket](/windows-hardware/drivers/install/driver-packages)ab.<br/>                                                                                                               |
| [**DriverPackageInstall**](/previous-versions/windows/hardware/difxapi/driverpackageinstall)<br/>       | Mit der **DriverPackageInstall** -Funktion wird ein [Treiber Paket](/windows-hardware/drivers/install/driver-packages) vorinstalliert, und anschließend wird der Treiber im System installiert.<br/>                                                                                                                                                 |
| [**DriverPackagePreinstall**](/previous-versions/windows/hardware/difxapi/driverpackagepreinstall)<br/> | Mit der **DriverPackagePreinstall** -Funktion wird ein [Treiber Paket](/windows-hardware/drivers/install/driver-packages) für einen Plug & Play (PNP)- [Funktions Treiber](/windows-hardware/drivers/kernel/function-drivers) vorinstalliert und die [INF-Datei](/windows-hardware/drivers/install/overview-of-inf-files) für das Treiber Paket im INF-Dateiverzeichnis des Systems installiert.<br/>             |
| [**DriverPackageUninstall**](/previous-versions/windows/hardware/difxapi/driverpackageuninstall)<br/>   | Die **DriverPackageUninstall** -Funktion deinstalliert das angegebene [Treiber Paket](/windows-hardware/drivers/install/driver-packages) aus dem System und entfernt das Treiber Paket. <br/>                                                                                                                               |
| [**Installerinfo**](/previous-versions/windows/hardware/difxapi/installerinfo)<br/>                     | Die installerinfo-Struktur enthält Informationen zu einer Anwendung, die von difxapi einem [Treiber Paket](/windows-hardware/drivers/install/driver-packages)zugeordnet wird. <br/>                                                                                                                                          |
| [**Setdifxlogcallback**](/previous-versions/windows/hardware/difxapi/setdifxlogcallback)<br/>           | Die **setdifxlogcallback** -Funktion registriert eine vom Aufrufer angegebene Rückruffunktion, die von difxapi aufgerufen wird, um Informationen über Ereignisse zu protokollieren, die während der Ausführung von difxapi auftreten <br/>                                                                                                               |



 

 

 

[Kommentare zu diesem Thema an Microsoft senden](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Difxapi.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Kommentare zu diesem Thema an Microsoft senden")