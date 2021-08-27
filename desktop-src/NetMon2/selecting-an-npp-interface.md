---
description: Netzwerkpaketanbieter (Network Packet Providers, NPPs) machen die Schnittstellen IDelaydC, IESP, IRTC und IStats verfügbar.
ms.assetid: 269b26f5-b794-4920-98da-505eda83c990
title: Auswählen einer NPP-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4336c4ff2408aa89d723dd451174ef6dca81eba39c17c52aefdc829018e71483
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128850"
---
# <a name="selecting-an-npp-interface"></a>Auswählen einer NPP-Schnittstelle

Netzwerkpaketanbieter (Network Packet Providers, NPPs) machen die Schnittstellen [**IDelaydC,**](idelaydc.md) [**IESP,**](iesp.md) [**IRTC**](irtc.md)und [**IStats**](istats.md) verfügbar. Jede dieser Schnittstellen bietet ähnliche Methoden zum Verbinden des NPP mit dem Netzwerk, zum Erfassen des Netzwerkdatenverkehrs und zum Sammeln statistischer Informationen zu den erfassten Daten. Informationen zur Auswahl der zu verwendenden Schnittstelle finden Sie in der folgenden Tabelle.

> [!Note]  
> Wenn Sie mit einer dieser Schnittstellen eine NPP mit dem Netzwerk verbinden, können Sie nur die von dieser Schnittstelle bereitgestellten Methoden verwenden. Wenn Sie beispielsweise über die [**IRTC-Schnittstelle**](irtc.md) eine Verbindung mit dem Netzwerk herstellen und dann versuchen, eine Erfassung mit [**IDelaydC**](idelaydc.md)zu starten, schlägt der Aufruf zum Starten der Erfassung fehl, und ein Fehlercode wird zurückgegeben.

 



| Schnittstelle                    | Verwendung                                                                                                                                                                                                                                                                                                                                     |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDelaydC**](idelaydc.md) | Verwenden Sie , um Netzwerkdatenverkehr zu erfassen und in einer Erfassungsdatei zu speichern. Diese Schnittstelle wird von der Netzwerkmonitor-Benutzeroberfläche und anderen NPP-Anwendungen verwendet, die erfasste Netzwerkinformationen speichern müssen.<br/>                                                                                                                                      |
| [**IESP**](iesp.md)         | Wird verwendet, um erweiterte Statistiken in einem speziellen ESP-Dateiformat bereitzustellen. Diese Schnittstelle wird von NPP-Anwendungen verwendet, die die vom ESP-Format bereitgestellten erweiterten Statistiken erfordern.<br/>                                                                                                                                                        |
| [**IRTC**](irtc.md)         | Verwenden Sie , um Netzwerkdatenverkehr in Echtzeit zu erfassen und Ereignisse auszulösen, wenn diese auftreten. Diese Schnittstelle wird von NPP-Anwendungen verwendet, die Laufzeiterfassungen erfordern. Beachten Sie, dass diese Schnittstelle weder die Statistiken bereitstellt, die die anderen NPP-Schnittstellen bereitstellen, noch dass Sie Frames in den erfassten Netzwerkdatenverkehr einfügen können.<br/> |
| [**IStats**](istats.md)     | Verwenden Sie , um Erfassungsstatistiken abzurufen, aber nicht die erfassten Frames.                                                                                                                                                                                                                                                                                 |



 

 

 




