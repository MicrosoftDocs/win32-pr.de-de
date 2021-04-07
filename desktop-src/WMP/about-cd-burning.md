---
title: Informationen zum Brennen von CDs
description: Informationen zum Brennen von CDs
ms.assetid: 1ecc73ed-c49d-4190-baa9-93162f075a4c
keywords:
- Windows Media Player, CD-brennen
- Windows Media Player-Objektmodell, CD-brennen
- Objektmodell, CD-brennen
- Windows Media Player ActiveX-Steuerelement, CD-brennen
- ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile, CD-brennen
- CD-brennen, Informationen zu
- Brennen von CDs, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc921080d02bef6ffbf916fe4d7d1df09f1e8bbc
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724054"
---
# <a name="about-cd-burning"></a>Informationen zum Brennen von CDs

Mit dem Windows Media Player 11 SDK werden neue Funktionen zum Erstellen von CDs eingeführt. Dieser Vorgang wird als *Brennen* bezeichnet.

Um die CD-Laufwerke auf dem Computer des Benutzers aufzulisten, verwenden Sie die **iwmpcdromcollection** -Schnittstelle. Sie rufen einen Zeiger auf diese Schnittstelle ab, indem Sie [iwmpcore:: get \_ cdromcollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection)aufrufen. Mithilfe der Methoden " **count** " und " **Item** " können Sie die Auflistung durchlaufen, um einen **iwmpcdrom** -Schnittstellen Zeiger für jedes CD-Laufwerk auf dem Computer des Benutzers abzurufen. Die **iwmpcdrom** -Schnittstelle stellt ein einzelnes CD-Laufwerk dar.

Bevor Sie mit dem Brennen einer CD beginnen, müssen Sie zuerst **QueryInterface** über einen **iwmpcdrom** -Zeiger aufrufen, um einen Zeiger auf die **iwmpcdromburn** -Schnittstelle abzurufen. Mithilfe der **IsAvailable** -Methode können Sie feststellen, ob ein bestimmtes CD-Laufwerk CDs brennen kann, ob eine CD im Laufwerk vorhanden ist und wie die CD verwendet werden kann.

Um die Elemente anzugeben, die auf CD gebrannt werden sollen, müssen Sie eine Wiedergabeliste erstellen. Windows Media Player stellt Wiedergabelisten mithilfe der **iwmpwiedergabe** -Schnittstelle dar. Sie können diese Wiedergabeliste beliebig erstellen. Beispielsweise können Sie einfach eine Wiedergabeliste aus der Bibliothek abrufen, indem Sie [iwmpmediacollection:: getbyalbum](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum)aufrufen. Nachdem Sie die Wiedergabeliste erstellt haben, die Sie auf CD brennen möchten, müssen Sie die Methode [iwmpcdromburn::p UT \_ burnwiedergabe](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) und den Wiedergabelisten Zeiger als Argument übergeben. Dadurch wird die Wiedergabeliste als eine festgelegt, die von Windows Media Player auf die CD kopiert wird.

Wenn Sie eine Wiedergabeliste aus der Bibliothek abrufen, werden alle Änderungen, die Sie an der Wiedergabeliste vornehmen, in der Benutzer Bibliothek widergespiegelt. Um dies zu vermeiden, nennen Sie [iwmpwiedergabe:: Set Items MINFO](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo), und übergeben Sie dabei den Attributnamen "temporär" und den Wert "true". Dadurch wird die Wiedergabelisten Instanz in eine temporäre Wiedergabeliste konvertiert, die ohne Änderung der ursprünglichen Wiedergabeliste bearbeitet werden kann.

Jedes Mal, wenn Sie eine neue Wiedergabeliste zum Brennen festlegen oder Änderungen an einer vorhandenen Burn-Wiedergabeliste vornehmen, müssen Sie [iwmpcdromburn:: erfrischendes Status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-refreshstatus) zum Aktualisieren der Statusinformationen anrufen. Dadurch wird sichergestellt, dass Windows Media Player die erforderliche Verarbeitung durchführt, um Ihnen genaue Statusinformationen für den CD-Brennvorgang bereitzustellen.

Um den Typ der zu brennenden CD anzugeben, nennen Sie [iwmpcdromburn::p UT \_ burnformat](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnformat). Windows Media Player ermöglicht es Ihnen, zwei Arten von CDs zu brennen: AudioCDs und Daten-CDs. Die [wmpburnformat](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat) -Enumeration definiert die CD-Typen.

Sie können eine Volumebezeichnung für die CD angeben, indem Sie [iwmpcdromburn::p UT- \_ Bezeichnung](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_label)aufrufen.

Wenn Sie bereit sind, mit dem Brennen der CD zu beginnen, nennen Sie [iwmpcdromburn:: startburn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn). Sie können den Fortschritt des Brennvorgangs überwachen, indem Sie in regelmäßigen Abständen [iwmpcdromburn:: get \_ burnprogress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress)aufrufen. Diese Methode ruft einen Statuswert für den gesamten Brennvorgang ab. Der abgerufene Wert ist eine Zahl, die den Prozentsatz der abgeschlossenen Verbrennung darstellt. Sie können den Status des Brennvorgangs überwachen, indem Sie das [IWMPEvents3:: cdromburnstatechange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnstatechange) -Ereignis behandeln, bei dem die [wmpburnstate](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate) -Enumeration verwendet wird, um den aktuellen Zustand anzugeben. Sie sollten darauf achten, den **iwmpcdromburn** -Zeiger (bereitgestellt durch das-Ereignis) mit dem Zeiger zu vergleichen, der den Brennvorgang darstellt, um sicherzustellen, dass das Ereignis durch den Vorgang ausgelöst wurde. Sie können den Brennvorgang beenden, indem Sie [iwmpcdromburn:: stopburn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn)aufrufen.

Es gibt zwei Ereignisse, die Sie behandeln können, um Fehler Benachrichtigungen über den Brennvorgang zu erhalten. Das [IWMPEvents3:: cdromburnerror](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnerror) -Ereignis wird ausgelöst, wenn ein generischer Fehler auftritt. [IWMPEvents3:: cdromburnmediaerror](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnmediaerror) wird ausgelöst, wenn ein bestimmtes Medien Element beim Brennen einen Fehler verursacht. Wie das **cdromburnstatechange** -Ereignis stellt jedes dieser Ereignisse einen **iwmpcdromburn** -Zeiger bereit, der den Brennvorgang darstellt, der das Ereignis ausgelöst hat. Das **cdromburnmediaerror** -Ereignis stellt einen **IDispatch** -Zeiger bereit, der das Medien Element darstellt, das das Ereignis ausgelöst hat. Sie können **QueryInterface** mithilfe dieses Zeigers aufrufen, um einen **iwmpmedia** -Zeiger abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> <dt>

[**Iwmpcdrom-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**Iwmpcdromburn-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
</dt> <dt>

[**Iwmpcdromcollection-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**IWMPEvents3-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**Iwmpmedia-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Temporäres Attribut**](temporary-attribute.md)
</dt> </dl>

 

 




