---
title: Medienstreamingschnittstellen
description: Die Media Streaming-API stellt die folgenden Schnittstellen bereit.
ms.assetid: 1E25B452-D23C-4A1D-BC39-A5B719DF2C5D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb21c5c17502c887f78fa223ec2a2f8f814d3998bb75b81812eb4de9919f7342
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972189"
---
# <a name="media-streaming-interfaces"></a>Medienstreamingschnittstellen

Die [Media Streaming-API](media-streaming-api-portal.md) stellt die folgenden Schnittstellen bereit.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActiveBasicDevice**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice)<br/>                           | Stellt eine aktive [**IBasicDevice dar,**](ibasicdevice.md) die einem UPnP-Gerät zugeordnet ist. <br/>                                                                                                                                          |
| [**IActiveBasicDeviceStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevicestatics)<br/>             | Stellt statische Methoden zum Erstellen von [**IActiveBasicDevice-Objekten**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice) dar. <br/>                                                                                                                                            |
| [**IBasicDevice**](ibasicdevice.md)<br/>                                       | Kapselt die Methoden und Ereignisse, die zum Modellieren eines DLNA-Geräts erforderlich sind.<br/>                                                                                                                                                                         |
| [**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)<br/>                             | Kapselt die Methoden und Ereignisse, die zum Abrufen einer Liste zwischengespeicherter Digital Media Renderer (DMRs) und/oder Digital Media Servers (DMSs) oder zum asynchronen Suchen der DMRs und/oder DMSs erforderlich sind, die sich derzeit im Netzwerk befinden.<br/>              |
| [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)<br/>                                         | Kapselt die Methoden, die zum Bereitstellen von Informationen über das Symbol eines DLNA-Geräts erforderlich sind.<br/>                                                                                                                                                    |
| [**IDevicePair**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicepair)<br/>                                         | Stellt ein Paar von [**ActiveBasicDevice-Objekten**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) dar, das aus einem Renderer und einem Server besteht.<br/>                                                                                                                 |
| [**IMediaRenderer**](imediarenderer.md)<br/>                                   | Kapselt die Methoden und Ereignisse, die zur Darstellung eines DMR-Geräts (DLNA Digital Media Renderer) erforderlich sind.<br/>                                                                                                                                        |
| [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)<br/> | Kapselt die Methoden, die zum Bereitstellen von Informationen darüber erforderlich sind, welche Methoden derzeit für die DMR aufgerufen werden können.<br/>                                                                                                                             |
| [**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)<br/>                     | Kapselt die Methoden, die zum asynchronen Erstellen einer neuen Instanz eines Objekts erforderlich sind, das die [**IMediaRenderer-Schnittstelle**](imediarenderer.md) implementiert.<br/>                                                                               |
| [**IStreamSelectorStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-istreamselectorstatics)<br/>                   | Kapselt die Methoden, die zum asynchronen Auswählen eines Streams erforderlich sind.<br/>                                                                                                                                                                         |
| [**ITransportParameters**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)<br/>                       | Kapselt die Methoden, die zum Bereitstellen von Informationen über die aktuellen transportbezogenen Einstellungen der DMR erforderlich sind. Diese Einstellungen umfassen den aktuellen Transportstatus und Informationen darüber, welche Methoden derzeit für die DMR aufgerufen werden können.<br/> |



 

 

