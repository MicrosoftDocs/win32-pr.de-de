---
description: Netzwerk Paketanbieter (NPPs) machen die Schnittstellen idelta aydc, iESP, iritc und iStats verfügbar.
ms.assetid: 269b26f5-b794-4920-98da-505eda83c990
title: Auswählen einer NPP-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8dba919302190e1fd89c859f61fca14aaf7d6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864059"
---
# <a name="selecting-an-npp-interface"></a>Auswählen einer NPP-Schnittstelle

Netzwerk Paketanbieter (NPPs) machen die Schnittstellen [**idelta aydc**](idelaydc.md), [**iESP**](iesp.md), [**iritc**](irtc.md)und [**iStats**](istats.md) verfügbar. Jede dieser Schnittstellen bietet ähnliche Methoden zum Verbinden des NPP mit dem Netzwerk, zum Erfassen von Netzwerk Datenverkehr und zum Sammeln statistischer Informationen zu den erfassten Daten. Informationen zu den zu verwendenden Schnittstellen finden Sie in der folgenden Tabelle.

> [!Note]  
> Wenn Sie eine NPP mit dem Netzwerk verbinden, können Sie nur die Methoden verwenden, die von dieser Schnittstelle bereitgestellt werden. Wenn Sie z. b. eine Verbindung mit dem Netzwerk über die [**untc**](irtc.md) -Schnittstelle herstellen und dann versuchen, eine Erfassung mit [**idelta aydc**](idelaydc.md)zu starten, schlägt der Start der Erfassung fehl, und es wird ein Fehlercode zurückgegeben.

 



| Schnittstelle                    | Verwendung                                                                                                                                                                                                                                                                                                                                     |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Idelta-DC**](idelaydc.md) | Verwenden Sie, um Netzwerk Datenverkehr zu erfassen und in einer Erfassungs Datei zu speichern. Diese Schnittstelle wird von der Netzwerkmonitor-Benutzeroberfläche und anderen NPP-Anwendungen verwendet, bei denen erfasste Netzwerkinformationen gespeichert werden müssen.<br/>                                                                                                                                      |
| [**IESP**](iesp.md)         | Wird verwendet, um Erweiterte Statistiken in einem speziellen ESP-Dateiformat bereitzustellen. Diese Schnittstelle wird von NPP-Anwendungen verwendet, die die im ESP-Format bereitgestellte erweiterte Statistik erfordern.<br/>                                                                                                                                                        |
| [**"Iran"**](irtc.md)         | Verwenden Sie, um den Netzwerk Datenverkehr in Echtzeit aufzuzeichnen und Ereignisse bei Auftreten zu Triggern aufzurufenden. Diese Schnittstelle wird von NPP-Anwendungen verwendet, die Lauf Zeitaufzeichnungen erfordern. Beachten Sie, dass diese Schnittstelle nicht die Statistiken bereitstellt, die von den anderen NPP-Schnittstellen bereitgestellt werden, und Sie können keine Frames in den erfassten Netzwerk Datenverkehr einfügen.<br/> |
| [**IStats**](istats.md)     | Verwenden Sie, um Aufzeichnungs Statistiken, aber nicht die erfassten Frames abzurufen.                                                                                                                                                                                                                                                                                 |



 

 

 




