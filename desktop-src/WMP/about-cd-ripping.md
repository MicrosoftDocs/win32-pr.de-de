---
title: Informationen zum CD-Ripping
description: Informationen zum CD-Ripping
ms.assetid: 1a179284-2909-4fc0-82be-996794ee4f31
keywords:
- Windows Media Player, CD-einreißen
- Windows Media Player-Objektmodell, CD-einreißen
- Objektmodell, CD-einreißen
- Windows Media Player ActiveX-Steuerelement, CD-einreißen
- ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile, CD-einreißen
- CD-Ripping, Info
- einreißen CDs, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28769c6af666e510fb97ebc98e44fadc7c3e472
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106338439"
---
# <a name="about-cd-ripping"></a>Informationen zum CD-Ripping

Mit dem Windows Media Player 11 SDK werden neue Funktionen zum Kopieren von Audiospuren aus CDs auf den Computer des Benutzers eingeführt. Dieser Vorgang wird als *einreißen* bezeichnet.

Wenn Sie Audiospuren mithilfe der Windows-Media Player-SDK-Schnittstellen durchlaufen, werden die sich ergebenden Musiktitel mit den Einstellungen erstellt, die der Benutzer im Dialogfeld Windows Media Player **Optionen** definiert hat.

Um die CD-Laufwerke auf dem Computer des Benutzers aufzulisten, verwenden Sie die **iwmpcdromcollection** -Schnittstelle. Sie rufen einen Zeiger auf diese Schnittstelle ab, indem Sie [iwmpcore:: get \_ cdromcollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection)aufrufen. Mithilfe der Methoden " **count** " und " **Item** " können Sie die Auflistung durchlaufen, um einen **iwmpcdrom** -Schnittstellen Zeiger für jedes CD-Laufwerk auf dem Computer des Benutzers abzurufen. Die **iwmpcdrom** -Schnittstelle stellt ein einzelnes CD-Laufwerk dar. Bevor Sie mit dem Einreißen einer CD beginnen, müssen Sie zuerst **QueryInterface** über einen **iwmpcdrom** -Zeiger aufrufen, um einen Zeiger auf die **iwmpcdromrip** -Schnittstelle abzurufen.

Um den einreißen-Vorgang zu starten, nennen Sie einfach [iwmpcdromrip:: startrip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip). Sie können den Fortschritt des einreißen-Vorgangs überwachen, indem Sie in regelmäßigen Abständen [iwmpcdromrip:: get \_ ripprogress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress)aufrufen. Diese Methode ruft einen Statuswert für den gesamten einreißen-Vorgang ab. Der abgerufene Wert ist eine Zahl, die den Prozentsatz der abgeschlossenen einreißen darstellt. Sie können den Status des einreißen-Vorgangs überwachen, indem Sie in regelmäßigen Abständen [iwmpcdromrip:: get \_ ripstate](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate)aufrufen. Diese Methode ruft einen [wmpripstate](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) -Enumerationswert ab, der angibt, ob der Vorgang gerade ausgeführt wird oder beendet wurde. Sie können auch den Status des rippingvorgangs überwachen, indem Sie das [IWMPEvents3:: cdromripstatechange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) -Ereignis behandeln. Sie sollten darauf achten, den **iwmpcdromrip** -Zeiger (bereitgestellt durch das-Ereignis) mit dem Zeiger zu vergleichen, der den einreißen-Vorgang darstellt, um sicherzustellen, dass das Ereignis durch den Vorgang ausgelöst wurde. Sie können den einreißen-Vorgang beenden, indem Sie [iwmpcdromrip:: stoprip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip)aufrufen.

Zum Empfangen von Fehler Benachrichtigungen zu einem einreißen-Vorgang können Sie das [IWMPEvents3:: cdromripmediaerror](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror) -Ereignis behandeln. Wie **cdromripstatechange** stellt dieses Ereignis einen **iwmpcdromrip** -Schnittstellen Zeiger bereit, der den einreißen-Vorgang darstellt, der das Ereignis ausgelöst hat. Das Ereignis stellt auch einen **IDispatch** -Zeiger bereit, der das Medien Element darstellt, das das Ereignis ausgelöst hat. Sie können **QueryInterface** mithilfe dieses Zeigers aufrufen, um einen **iwmpmedia** -Zeiger abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> </dl>

 

 




