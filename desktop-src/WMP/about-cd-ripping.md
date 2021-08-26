---
title: Informationen zu CD-Ending
description: Informationen zu CD-Ending
ms.assetid: 1a179284-2909-4fc0-82be-996794ee4f31
keywords:
- Windows Media Player,CD-Lässing
- Windows Media Player-Objektmodell,CD-Bebauung
- Objektmodell,CD-Bebauung
- Windows Media Player ActiveX,CD-Kontrolle
- ActiveX,CD-Steuerung
- Windows Media Player Mobile ActiveX,CD-Steuerung
- Windows Media Player Mobil, CD-10
- CD-Ing, Informationen
- Verwenden von CDs, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efab14a97f9cc24c4137e5d939bc9562b1fc073cd551bd83388de4ba1de0b65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903600"
---
# <a name="about-cd-ripping"></a>Informationen zu CD-Ending

Das Windows Media Player 11 SDK führt neue Funktionen zum Kopieren von Audiospuren von CDs auf den Computer des Benutzers ein. Dieser Prozess wird als *"beläsingend" bezeichnet.*

Wenn Sie Audiospuren mithilfe der Windows Media Player SDK-Schnittstellen aufreifen, werden die resultierenden Musiktitel mithilfe der Einstellungen erstellt, die der Benutzer im Dialogfeld Windows Media Player **Optionen** definiert hat.

Um die CD-Laufwerke auf dem Computer des Benutzers aufzählen zu können, verwenden Sie **die IWMPCcollection-Schnittstelle.** Sie rufen einen Zeiger auf diese Schnittstelle ab, indem Sie [IWMPCore::get \_ ccollection aufrufen.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection) Mithilfe der **Count-** und **Item-Methoden** können Sie die Sammlung iterieren, um einen **IWMPCführung-Schnittstellenzeiger** für jedes CD-Laufwerk auf dem Computer des Benutzers abzurufen. Die **IWMPC cri-Schnittstelle** stellt ein einzelnes CD-Laufwerk dar. Bevor Sie mit dem Erstellen einer CD beginnen, müssen Sie **zunächst QueryInterface** über einen **IWMPCaufrufen,** um einen Zeiger auf die **IWMPCiusRip-Schnittstelle abzurufen.**

Rufen Sie einfach [IWMPCiererRip::startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip)auf, um den Startvorgang zu starten. Sie können den Fortschritt des Wischvorgang überwachen, indem Sie [regelmäßig IWMPCiererRip::get \_ ripProgress aufrufen.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress) Diese Methode ruft einen Statuswert für den gesamten Belässungsvorgang ab. Der abgerufene Wert ist eine Zahl, die den Prozentsatz der abgeschlossenen Besendeung darstellt. Sie können den Zustand des Wischvorgang überwachen, indem Sie [regelmäßig IWMPCiererRip::get \_ ripState aufrufen.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate) Diese Methode ruft einen [WMPRipState-Enumerationswert](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) ab, der angibt, ob der Vorgang durchgeführt oder beendet wird. Sie können auch den Status des Vorgangs überwachen, indem Sie das [IWMPEvents3::CiererRipStateChange-Ereignis](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) behandeln. Sie sollten darauf achten, den **IWMPCiererRip-Zeiger** (bereitgestellt durch das -Ereignis) mit dem Zeiger zu vergleichen, der Ihren Beschningsvorgang darstellt, um sicherzustellen, dass das Ereignis von Ihrem Vorgang ausgelöst wurde. Sie können den Beschningsvorgang beenden, indem Sie [IWMPCiererRip::stopRip aufrufen.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip)

Sie können das [IWMPEvents3::CmgRipMediaError-Ereignis](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror) behandeln, um Fehlerbenachrichtigungen zu einem Benachrichtigungsvorgang zu erhalten. Wie **CiererRipStateChange** stellt dieses Ereignis einen **IWMPCiererRip-Schnittstellenzeiger** bereit, der den verfeinerten Vorgang darstellt, der das Ereignis ausgelöst hat. Das -Ereignis stellt auch einen **IDispatch-Zeiger** für das Medienelement dar, das das Ereignis ausgelöst hat. Sie können **QueryInterface über diesen** Zeiger aufrufen, um einen **IWMPMedia-Zeiger** abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> </dl>

 

 




