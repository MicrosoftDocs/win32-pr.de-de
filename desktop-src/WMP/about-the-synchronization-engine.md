---
title: Informationen zur Synchronisierungs-Engine
description: Informationen zur Synchronisierungs-Engine
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Windows Media Player, Synchronisierungs Modul
- Windows Media Player-Objektmodell, Synchronisierungs Modul
- Objektmodell, Synchronisierungs Modul
- Windows Media Player ActiveX-Steuerelement, Synchronisierungs Modul
- ActiveX-Steuerelement, Synchronisierungs Modul
- Windows Media Player Mobile ActiveX-Steuerelement, Synchronisierungs Modul
- Windows Media Player Mobile, Synchronisierungs Modul
- Synchronisieren von Geräten, Synchronisierungs Modul
- Geräte Synchronisierung, Synchronisierungs Modul
- Synchronisierungs Modul
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe0768c4805b074fdaf628a25daf47b9ced97ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389898"
---
# <a name="about-the-synchronization-engine"></a>Informationen zur Synchronisierungs-Engine

Das Synchronisierungs Modul ist die Komponente von Windows Media Player, die das Kopieren von Inhalten digitaler Medien auf tragbare Geräte verwaltet. Windows Media Player unterstützt eine einzelne Instanz der Synchronisierungs-Engine für jedes Gerät. Sie müssen eine Remote Instanz des Windows Media Player-Steuer Elements verwenden, um Synchronisierungs Tasks Programm gesteuert auszuführen. Tatsächlich werden die Synchronisierungs-Engine-Instanzen von Ihrem Programm mit Windows Media Player und allen anderen Programmen gemeinsam genutzt, die die Player-Schnittstellen für die Geräte Synchronisierung verwenden.

Sie können [iwmpsyncdevice:: Start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) und [iwmpsyncdevice::](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) End verwenden, um zu steuern, wann das Synchronisierungs Modul funktioniert. In den meisten Fällen sollten Sie diese Methoden nicht verwenden. Stattdessen sollten Sie zulassen, dass das Synchronisierungs Modul seine Arbeit automatisch plant. Die Methoden zum **starten** und **Abbrechen** sind vorhanden, damit Sie Sie verwenden können, wenn das Programm die Windows Media Player-Benutzeroberfläche ersetzen soll. In diesem Fall empfiehlt es sich, eine Schaltfläche zum Starten und Abbrechen ähnlich der eines Windows-Media Player bereitzustellen, die auf der Registerkarte **Geräte** bereitgestellt wird.

Sie können den Synchronisierungs Fortschritt für ein Gerät überwachen, indem Sie [iwmpsyncdevice:: get \_ Progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress)abrufen. Diese Methode ruft einen Fortschritts Wert für den gesamten Synchronisierungs Prozess mit einem bestimmten Gerät ab. Der abgerufene Wert ist eine Zahl, die den Prozentsatz der abgeschlossenen Synchronisierung darstellt. Es gibt zwei Ereignisse, die Sie im Zusammenhang mit der Synchronisierung erhalten können. Wenn ein Problem auftritt, werden Sie durch das Ereignis " **entvicesyncerror** " benachrichtigt. Das **devicesyncstatechange** -Ereignis warnt Sie, wenn das Synchronisierungs Modul den Status für das aktuelle Gerät geändert hat.

Sie können die Menge an Gerätespeicher einschränken, die Windows Media Player für die Synchronisierung verwendet, indem Sie [IWMPSyncDevice2:: abtiteminfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) mit dem Attribut " **prozentuspacereserved** " aufrufen. Die Verwendung dieser Schnittstelle erfordert Windows Media Player 11.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zur Geräte Synchronisierung**](about-device-synchronization.md)
</dt> <dt>

[**IWMPEvents2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Anzeigen des Synchronisierungs Status**](showing-synchronization-progress.md)
</dt> </dl>

 

 




