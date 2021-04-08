---
description: Endpointvolume-API
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: Endpointvolume-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b827045250336aa499e386a8dafedb6ae068b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748552"
---
# <a name="endpointvolume-api"></a>Endpointvolume-API

Die endpointvolume-API ermöglicht spezialisierten Clients das Steuern und Überwachen der volumeebenen von [audioendpunktgeräten](audio-endpoint-devices.md). Ein Client erhält Verweise auf die Schnittstellen in der endpointvolume-API, indem er die [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle eines audioendpunktgeräts erhält und die [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) -Methode aufruft.

Die Header Datei "endpointvolume. h" definiert die Schnittstellen in der endpointvolume-API.

Audioanwendungen, die die [mmdevice-API](mmdevice-api.md) und die [WASAPI](wasapi.md) verwenden, verwenden in der Regel die [**isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) -Schnittstelle, um die volumeebenen pro Sitzung zu steuern. Nur zwei Arten von Audioanwendungen müssen die endpointvolume-API verwenden. Diese Anwendungs Typen lauten wie folgt:

-   Anwendungen, die die Master Volume-Ebenen von audioendpunktgeräten verwalten, ähnlich dem Windows-Volumen Steuerungsprogramm, Sndvol.exe.
-   Professionelle Audioanwendungen ("pro-Audioanwendungen"), die exklusiven Modus-Zugriff auf audioendpunktgeräte benötigen.

Die ungeeignete Verwendung der endpointvolume-API kann die Windows-audiorichtlinie beeinträchtigen und die systemvolumeeinstellungen des Benutzers stören.

Wenn ein audioendpunktgerät Hardware Volume und stumm Steuerelemente implementiert, verwendet die endpointvolume-API diese Steuerelemente, um das Geräte Volume zu verwalten. Andernfalls implementiert die endpointvolume-API die Steuerelemente in Software, transparent für den Client.

Wenn ein Gerät über Hardware Volume und stumm Steuerelemente verfügt, wirken sich Änderungen am Geräte Volume und stumm Einstellungen über die endpointvolume-API auf die Volumeebene im Modus "Shared" und im exklusiven Modus aus. Wenn ein Gerät nicht über Hardware Volume und stumm Steuerelemente verfügt, wirken sich Änderungen am Software Volume und stumm Steuerelemente über die endpointvolume-API auf die Volumeebene im freigegebenen Modus, jedoch nicht im exklusiven Modus aus. Im exklusiven Modus tauschen der Client und das Gerät Audiodaten direkt aus, wobei die Software Steuerelemente umgangen werden.

Für Anwendungen, die das Hardware Volume und das stumm schalten von Steuerelementen verwalten müssen, bietet die endpointvolume-API zwei mögliche Vorteile gegenüber der Debug- [API](devicetopology-api.md).

Erstens fehlen für eine Reihe von audioadaptergeräten Hardware Volume-Steuerelemente. Wenn ein Gerät nicht über ein Hardware Volume-Steuerelement verfügt, implementiert die [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) -Schnittstelle in der endpointvolume-API automatisch ein Software Volume-Steuerelement auf dem Stream zu oder von diesem Gerät. Für einen Client der endpointvolume-API ist das Ergebnis identisch, unabhängig davon, ob die volumesteuerung vom Gerät oder in der Software von der endpointvolume-API-Schnittstelle in der Hardware implementiert wird.

Zweitens: auch wenn das Adapter Gerät Hardware Volume-Steuerelemente implementiert, kann eine Anwendung, die die devicetopology-API zum Implementieren eines topologietraktalgorithmus verwendet, das gesuchte Steuerelement nicht finden. In der Regel ist eine solche Anwendung so konzipiert, dass Sie die Hardware Topologie eines bestimmten Geräts oder einer Gruppe verwandter Geräte durchläuft. Die Anwendungs Risiken können nicht durchlaufen werden, wenn versucht wird, die Topologie eines Geräts zu durchlaufen, mit dem Sie nicht speziell entworfen oder getestet wurde.

Nur spezialisierte Anwendungen, die auf andere Hardwarefunktionen als Volume-und stumm Steuerelemente zugreifen müssen, müssen die devicetopology-API verwenden. Bei Anwendungen, für die nur die Volumeebene eines Datenstroms im exklusiven Modus gesteuert werden muss, ist die endpointvolume-API einfacher zu verwenden und funktioniert zuverlässig mit einer breiteren Palette von audiohardwaregeräten.

Codebeispiele, die die Schnittstellen in der endpointvolume-API verwenden, finden Sie in den folgenden Themen:

-   [Steuerelemente für Endpunkt-](endpoint-volume-controls.md)
-   [Spitzen Zähler](peak-meters.md)

Ein Beispiel, das die endpointvolume-API verwendet, finden Sie unter [endpointvolume](endpointvolume.md) in der Windows SDK.

Die endpointvolume-API implementiert die folgenden Schnittstellen.



| Schnittstelle                                                | BESCHREIBUNG                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | Stellt die volumesteuerelemente im Audiostream zu oder von einem audioendpunktgerät dar. |
| [**Iaudiometerinformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | Stellt einen Spitzen Zähler für den Audiostream zu oder von einem audioendpunktgerät dar.        |



 

Außerdem sollten Clients der endpointvolume-API, die eine Benachrichtigung über das Volume und Änderungen an audioendpunktgeräten erfordern, die folgende Schnittstelle implementieren.



| Schnittstelle                                                            | BESCHREIBUNG                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**Iaudioendpointvolumecallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Stellt Benachrichtigungen bereit, wenn die Volumeebene oder der stumm Schaltung-Status eines audioendpunktgeräts geändert wird. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lautstärkeregler](volume-controls.md)
</dt> <dt>

[**Immdevice-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**Immdevice:: Aktivieren**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[**Isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 



