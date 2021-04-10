---
description: Auflisten von Audiogeräten
ms.assetid: 20110ffc-5eff-4279-abea-53115803b6ee
title: Auflisten von Audiogeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707b9a88181c83344757c711af1c0199c19ebc16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041455"
---
# <a name="enumerating-audio-devices"></a>Auflisten von Audiogeräten

Die erste Aufgabe einer Client-Audioanwendung besteht darin, ein geeignetes Audiogerät zu finden, das verwendet werden soll. Mit der [mmdevice-API](mmdevice-api.md) können Clients die [audioendpunktgeräte](audio-endpoint-devices.md) im System ermitteln und ermitteln, welche Geräte für die Anwendung geeignet sind. Mit dieser API können Clients Sammlungen der verfügbaren Endpunkt Geräte abrufen und die Funktionen jedes Geräts abrufen. Die Header Datei "mmdeviceapi. h" definiert die Schnittstellen in der mmdevice-API.

Ein Audioadapter kann mehrere Geräte enthalten, z. –. ein waverenderinggerät und ein Wellen Erfassungsgerät. Dabei handelt es sich um Adapter Geräte anstelle von Endpunkt Geräten. Wie bereits erwähnt, werden Adapter Geräte vom Plug & Play-Manager registriert, im Gegensatz zu Endpunkt Geräten, die vom Endpunkt-Manager registriert werden. Jedes Adapter Gerät unterstützt normalerweise ein oder mehrere Endpunkt Geräte. Ein renderingendpunktgerät (z. b. Kopfhörer) kann einen Stream von Audiodaten von einer Client Anwendung empfangen, und ein Erfassungs Endpunkt-Gerät (z. b. ein Mikrofon) kann einen Audiostream an eine Client Anwendung senden.

Vor dem Auflisten der Endpunkt Geräte im System muss der Client zuerst die Windows [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufrufen, um einen Geräte Enumerator zu erstellen. Ein Geräte Enumerator ist ein Objekt mit einer [**immdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle. Weitere Informationen zu **cokreateinstance** finden Sie in der Windows SDK-Dokumentation.

Der Client ruft die [**immdeviceenumerator:: enumaudioendpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) -Methode auf, um eine Auflistung von Endpunkt Objekten zu erstellen. Jedes Endpunkt Objekt stellt ein audioendpunktgerät im System dar. In diesem Befehl gibt der Client an, ob die Sammlung alle renderinggeräte im System, alle Erfassungsgeräte oder beides enthalten soll.

Eine Geräte Sammlung ist ein Objekt mit der [**immdebug**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) -Schnittstelle. Jedes Element in einer Geräte Sammlung ist ein Endpunkt Objekt mit mindestens den folgenden beiden Schnittstellen:

-   Eine [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle. Ein Client ruft einen Verweis auf die **immdevice** -Schnittstelle eines Endpunkt Objekts in einer Geräte Sammlung ab, indem er die [**immdevicecollection:: Item**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item) -Methode aufruft.
-   Eine [**immendpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint) -Schnittstelle. Ein Client ruft einen Verweis auf die **immendpoint** -Schnittstelle eines Endpunkt Objekts durch Aufrufen der [**immdevice:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode ab.

Nachdem eine Sammlung von Endpunkt Geräten abgerufen wurde, kann der Client die Eigenschaften der einzelnen Geräte in der Sammlung Abfragen, um deren Eignung für die Verwendung zu ermitteln. Ein Codebeispiel, das zeigt, wie Endpunkt Geräte aufgezählt und deren Eigenschaften abgefragt werden, finden Sie unter [Geräteeigenschaften](device-properties.md).

Nachdem Sie ein geeignetes Gerät ausgewählt haben, kann der Client die [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) -Methode zum Aktivieren der gerätespezifischen Schnittstellen in [WASAPI](wasapi.md), der [devicetopology-API](devicetopology-api.md)und der [endpointvolume-API](endpointvolume-api.md)aufruft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioendpunktgeräte](audio-endpoint-devices.md)
</dt> </dl>

 

 
