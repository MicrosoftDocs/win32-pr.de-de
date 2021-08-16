---
description: MTP-/Bluetooth-Verbindungsschnittstellen
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: MTP-/Bluetooth-Verbindungsschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c0f32717afe14be05cae6e43d097e67fc9790729e5be4ce9c2dfa6f901a126a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843367"
---
# <a name="mtpbluetooth-connection-interfaces"></a>MTP-/Bluetooth-Verbindungsschnittstellen

Mit den folgenden Schnittstellen können Anwendungen nur Geräte aufzählen und verbindungen, die das Media Transfer Protocol (MTP) über Bluetooth (MTP/Bluetooth) unterstützen. Die WPD-Treiber-, Sammlungs- und Clientschnittstellen sind nicht auf das MTP/Bluetooth-Protokoll beschränkt.



| Schnittstelle                                                              | Beschreibung                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**IConnectionRequestCallback**](iconnectionrequestcallback.md)       | Definiert eine einzelne Rückrufmethode, mit der Anwendungen Benachrichtigungen über abgeschlossene und abgebrochene Anforderungen erhalten. |
| [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) | Listet **IPortableDeviceConnector-Schnittstellen** auf.                                                                 |
| [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | Unterstützt Methoden, die Anwendungen aufrufen, um Verbindungen mit MTP-Bluetooth-Geräten herzustellen.                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 



