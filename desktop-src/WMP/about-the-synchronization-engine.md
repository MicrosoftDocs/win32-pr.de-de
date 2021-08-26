---
title: Informationen zur Synchronisierungs-Engine
description: Informationen zur Synchronisierungs-Engine
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Windows Media Player,Synchronisierungs-Engine
- Windows Media Player-Objektmodell, Synchronisierungs-Engine
- Objektmodell, Synchronisierungs-Engine
- Windows Media Player ActiveX,Synchronisierungs-Engine
- ActiveX,Synchronisierungs-Engine
- Windows Media Player Mobile ActiveX,Synchronisierungs-Engine
- Windows Media Player Mobil, Synchronisierungsmodul
- Synchronisieren von Geräten, Synchronisierungsmodul
- Gerätesynchronisierung, Synchronisierungsmodul
- Synchronisierungs-Engine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ccac14f6416b080ae22407930d720df84bd5b4dc399892b9a2d8678d03eee6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903070"
---
# <a name="about-the-synchronization-engine"></a>Informationen zur Synchronisierungs-Engine

Die Synchronisierungs-Engine ist die Komponente Windows Media Player, die das Kopieren digitaler Medieninhalte auf portable Geräte verwaltet. Windows Media Player unterstützt eine einzelne Instanz der Synchronisierungs-Engine für jedes Gerät. Sie müssen eine Remoteinstanz des -Steuerelements Windows Media Player, um Synchronisierungsaufgaben programmgesteuert auszuführen. Das Programm teilt die Instanzen der Synchronisierungs-Engine mit Windows Media Player und allen anderen Programmen, die die Player-Schnittstellen für die Gerätesynchronisierung verwenden.

Sie können [IWMPSyncDevice::start und](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) [IWMPSyncDevice::stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) verwenden, um zu steuern, wann die Synchronisierungs-Engine ihre Arbeit übernimmt. In den meisten Fällen sollten Sie diese Methoden nicht verwenden. Stattdessen sollten Sie die Synchronisierungs-Engine ihre Arbeit automatisch planen lassen. Die **Start-** **und Stop-Methoden** sind vorhanden, sodass Sie sie verwenden können, wenn Ihr Programm die Benutzeroberfläche Windows Media Player ersetzen soll. In diesem Fall sollten Sie eine Schaltfläche zum Starten/Beenden bereitstellen, die der Schaltfläche ähnelt, die Windows Media Player registerkarte **Geräte angezeigt** wird.

Sie können den Synchronisierungsfortschritt für ein Gerät überwachen, indem Sie [IWMPSyncDevice::get \_ progressabgleichen.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress) Diese Methode ruft einen Statuswert für den gesamten Synchronisierungsprozess mit einem bestimmten Gerät ab. Der abgerufene Wert ist eine Zahl, die den Prozentsatz der abgeschlossenen Synchronisierung darstellt. Sie können zwei Ereignisse empfangen, die sich auf die Synchronisierung bezieht. Das **DeviceSyncError-Ereignis** benachrichtigt Sie, wenn ein Problem auftritt. Das **Ereignis DeviceSyncStateChange** warnt Sie, wenn sich der Status der Synchronisierungs-Engine für das aktuelle Gerät geändert hat.

Sie können die Menge an Gerätespeicher begrenzen, die Windows Media Player für die Synchronisierung verwendet, indem [Sie IWMPSyncDevice2::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) mit dem **PercentSpaceReserved-Attribut** aufrufen. Die Verwendung dieser Schnittstelle erfordert Windows Media Player 11.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zur Gerätesynchronisierung**](about-device-synchronization.md)
</dt> <dt>

[**IWMPEvents2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Anzeigen des Synchronisierungsfortschritts**](showing-synchronization-progress.md)
</dt> </dl>

 

 




