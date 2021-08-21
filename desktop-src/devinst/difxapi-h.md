---
title: Difxapi.h
description: Dieser Abschnitt enthält Referenzthemen für den Header Difxapi.h.
ms.assetid: 84da7e54-0677-495e-9dc5-aca4ac12c0b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5dcace8f7f8c8ed528849da02016f04e0ca32b2132c7b0587a96872d7cc561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736020"
---
# <a name="difxapih"></a>Difxapi.h

Dieser Abschnitt enthält Referenzthemen für den Header Difxapi.h.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                 | Beschreibung                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*DIFLOGCALLBACK*](/previous-versions/windows/hardware/difxapi/diflogcallback)<br/>                     | Eine **DIFLOGCALLBACK-Typfunktion** ist eine von der Anwendung bereitgestellte Rückruffunktion, die von einer Anwendung durch Aufrufen von [**SetDifxLogCallback**](/previous-versions/windows/hardware/difxapi/setdifxlogcallback)registriert wird. DIFxAPI ruft die Rückruffunktion auf, um Ereignisse zu protokollieren, die während des DIFxAPI-Vorgangs auftreten.<br/>                        |
| [*DIFXAPILOGCALLBACK*](/previous-versions/windows/hardware/difxapi/difxapilogcallback)<br/>             | Eine **vom Typ DIFXAPILOGCALLBACK** typisierte Funktion ist eine von der Anwendung bereitgestellte Rückruffunktion, die eine Anwendung bei DIFxAPI durch Aufrufen von [**DIFXAPISetLogCallback**](/previous-versions/windows/hardware/difxapi/difxapisetlogcallback)registriert. DIFxAPI ruft die Rückruffunktion auf, um Ereignisse zu protokollieren, die während des DIFxAPI-Vorgangs auftreten.<br/> |
| [**DIFXAPISetLogCallback**](/previous-versions/windows/hardware/difxapi/difxapisetlogcallback)<br/>     | Die **DIFXAPISetLogCallback-Funktion** registriert eine vom Aufrufer bereitgestellte Rückruffunktion, die DIFxAPI aufruft, um Informationen zu Ereignissen zu protokollieren, die während DIFxAPI-Vorgängen auftreten. <br/>                                                                                                            |
| [**DriverPackageGetPath**](/previous-versions/windows/hardware/difxapi/driverpackagegetpath)<br/>       | Die **DriverPackageGetPath-Funktion** ruft den vollqualifizierten Pfad der [INF-Datei](/windows-hardware/drivers/install/overview-of-inf-files) für ein vorinstalliertes [Treiberpaket](/windows-hardware/drivers/install/driver-packages)ab.<br/>                                                                                                               |
| [**DriverPackageInstall**](/previous-versions/windows/hardware/difxapi/driverpackageinstall)<br/>       | Die **DriverPackageInstall-Funktion** installiert ein [Treiberpaket](/windows-hardware/drivers/install/driver-packages) vorinstalliert und dann den Treiber im System.<br/>                                                                                                                                                 |
| [**DriverPackagePreinstall**](/previous-versions/windows/hardware/difxapi/driverpackagepreinstall)<br/> | The **DriverPackagePreinstall** function preinstalls a [driver package](/windows-hardware/drivers/install/driver-packages) for a Plug and Play (PnP) [function driver](/windows-hardware/drivers/kernel/function-drivers) and installs the [INF file](/windows-hardware/drivers/install/overview-of-inf-files) for the driver package in the system INF file directory.<br/>             |
| [**DriverPackageUninstall**](/previous-versions/windows/hardware/difxapi/driverpackageuninstall)<br/>   | Die **DriverPackageUninstall-Funktion** deinstalliert das angegebene [Treiberpaket](/windows-hardware/drivers/install/driver-packages) aus dem System und entfernt das Treiberpaket. <br/>                                                                                                                               |
| [**INSTALLERINFO**](/previous-versions/windows/hardware/difxapi/installerinfo)<br/>                     | Die INSTALLERINFO-Struktur enthält Informationen zu einer Anwendung, die DIFxAPI einem [Treiberpaket](/windows-hardware/drivers/install/driver-packages)zuweist. <br/>                                                                                                                                          |
| [**SetDifxLogCallback**](/previous-versions/windows/hardware/difxapi/setdifxlogcallback)<br/>           | Die **SetDifxLogCallback-Funktion** registriert eine vom Aufrufer bereitgestellte Rückruffunktion, die DIFxAPI aufruft, um Informationen zu Ereignissen zu protokollieren, die während DIFxAPI-Vorgängen auftreten. <br/>                                                                                                               |



 

 

 

[Senden von Kommentaren zu diesem Thema an Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Difxapi.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Senden von Kommentaren zu diesem Thema an Microsoft")