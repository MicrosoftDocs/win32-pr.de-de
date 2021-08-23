---
description: Aufzählen von Audiogeräten
ms.assetid: 20110ffc-5eff-4279-abea-53115803b6ee
title: Aufzählen von Audiogeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd5d21ec2de2b08ca3c6f26884bd210b2f149caaa9e3b6a4402b69dde9fb7540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018378"
---
# <a name="enumerating-audio-devices"></a>Aufzählen von Audiogeräten

Die erste Aufgabe einer Clientaudioanwendung besteht darin, ein geeignetes Audiogerät für die Verwendung zu finden. Mit [der MMDevice-API](mmdevice-api.md) können Clients die [Audioendpunktgeräte](audio-endpoint-devices.md) im System ermitteln und ermitteln, welche Geräte für die Anwendung geeignet sind. Mit dieser API können Clients Sammlungen der verfügbaren Endpunktgeräte abrufen und die Funktionen der einzelnen Geräte abrufen. Die Headerdatei Mmdeviceapi.h definiert die Schnittstellen in der MMDevice-API.

Ein Audioadapter kann mehrere Geräte enthalten, z. B. ein Wellenrenderinggerät und ein Wellenerfassungsgerät. Hierbei handelt es sich nicht um Endpunktgeräte, sondern um Adaptergeräte. Wie bereits erwähnt, werden Adaptergeräte vom Plug & Play-Manager registriert, im Gegensatz zu Endpunktgeräten, die vom Endpunkt-Manager registriert werden. Jedes Adaptergerät unterstützt in der Regel mindestens ein Endpunktgerät. Ein Renderingendpunktgerät (z. B. Funkgeräte) kann einen Audiodatenstrom von einer Clientanwendung empfangen, und ein Erfassungsendpunktgerät (z. B. ein Mikrofon) kann einen Audiostream an eine Clientanwendung senden.

Vor dem Aufzählen der Endpunktgeräte im System muss der Client zuerst die Windows [**CoCreateInstance-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen, um einen Geräteenumerator zu erstellen. Ein Geräteenumerator ist ein Objekt mit einer [**IMMDeviceEnumerator-Schnittstelle.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) Informationen zu **CoCreateInstance** finden Sie in der Windows SDK-Dokumentation.

Der Client ruft die [**IMMDeviceEnumerator::EnumAudioEndpoints-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) auf, um eine Auflistung von Endpunktobjekten zu erstellen. Jedes Endpunktobjekt stellt ein Audioendpunktgerät im System dar. In diesem Aufruf gibt der Client an, ob die Sammlung alle Renderinggeräte im System, alle Erfassungsgeräte oder beides enthalten soll.

Eine Gerätesammlung ist ein Objekt mit einer [**IMMDeviceCollection-Schnittstelle.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) Jedes Element in einer Gerätesammlung ist ein Endpunktobjekt mit mindestens den folgenden beiden Schnittstellen:

-   Eine [**IMMDevice-Schnittstelle.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) Ein Client ruft einen Verweis auf die **IMMDevice-Schnittstelle** eines Endpunktobjekts in einer Gerätesammlung ab, indem er die [**IMMDeviceCollection::Item-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item) aufruft.
-   Eine [**IMMEndpoint-Schnittstelle.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint) Ein Client ruft einen Verweis auf die **IMMEndpoint-Schnittstelle** eines Endpunktobjekts ab, indem er die [**IMMDevice::QueryInterface-Methode**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) aufruft.

Nach dem Abrufen einer Sammlung von Endpunktgeräten kann der Client die Eigenschaften der einzelnen Geräte in der Sammlung abfragen, um deren Eignung für die Verwendung zu ermitteln. Ein Codebeispiel, das zeigt, wie Sie Endpunktgeräte aufzählen und deren Eigenschaften abfragen, finden Sie unter [Geräteeigenschaften.](device-properties.md)

Nach der Auswahl eines geeigneten Geräts kann der Client die [**IMMDevice::Activate-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) aufrufen, um die gerätespezifischen Schnittstellen in [WASAPI,](wasapi.md)die [DeviceTopology-API](devicetopology-api.md)und die [EndpointVolume-API](endpointvolume-api.md)zu aktivieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioendpunktgeräte](audio-endpoint-devices.md)
</dt> </dl>

 

 
