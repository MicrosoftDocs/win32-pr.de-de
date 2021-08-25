---
title: Informationen zum Brennen von CDs
description: Informationen zum Brennen von CDs
ms.assetid: 1ecc73ed-c49d-4190-baa9-93162f075a4c
keywords:
- Windows Media Player,CD-1
- Windows Media Player-Objektmodell,CD-Endung
- Objektmodell, CD-1
- Windows Media Player ActiveX,CD-Sicherung
- ActiveX-Steuerelement,CD-Endung
- Windows Media Player Mobile ActiveX-Steuerelement, CD-Steuerung
- Windows Media Player Mobil, CD-1
- CD-2016,About
- -CDs,About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c784765a09b601da2f0ec75434a37f55a75ff7e6ab6d737f7912daab8f197c07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957140"
---
# <a name="about-cd-burning"></a>Informationen zum Brennen von CDs

Das Windows Media Player 11 SDK führt neue Funktionen zum Erstellen von CDs ein. Dieser Prozess wird als *"1" bezeichnet.*

Um die CD-Laufwerke auf dem Computer des Benutzers aufzählen zu können, verwenden Sie **die IWMPCcollection-Schnittstelle.** Sie rufen einen Zeiger auf diese Schnittstelle ab, indem Sie [IWMPCore::get \_ ccollection aufrufen.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection) Mithilfe der **Count-** und **Item-Methoden** können Sie die Sammlung iterieren, um einen **IWMPCführung-Schnittstellenzeiger** für jedes CD-Laufwerk auf dem Computer des Benutzers abzurufen. Die **IWMPC cri-Schnittstelle** stellt ein einzelnes CD-Laufwerk dar.

Bevor Sie mit dem Erstellen einer CD beginnen, müssen Sie **zunächst QueryInterface** über einen **IWMPCführungszeiger** aufrufen, um einen Zeiger auf die **IWMPCleitschnittstelle** abzurufen. Mithilfe der **isAvailable-Methode** können Sie bestimmen, ob ein bestimmtes CD-Laufwerk CDs verwenden kann, ob auf dem Laufwerk eine CD vorhanden ist und wie die CD verwendet werden kann.

Um die Elemente anzugeben, die auf CD zusammengestellt werden sollen, müssen Sie eine Wiedergabeliste erstellen. Windows Media Player Wiedergabelisten mithilfe der **IWMPPlaylist-Schnittstelle** darstellt. Sie können diese Wiedergabeliste auf beliebige Weise erstellen. Sie können z. B. einfach eine Wiedergabeliste aus der Bibliothek abrufen, indem Sie [IWMPMediaCollection::getByZeichnet aufrufen.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum) Nachdem Sie die Wiedergabeliste erstellt haben, die Sie auf CD einbetten möchten, müssen Sie die [IWMPC wie die Methode IWMPCwist::p ut \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) aufrufen und den Wiedergabelistenzeiger als Argument übergeben. Dadurch wird Ihre Wiedergabeliste als die Wiedergabeliste Windows Media Player die auf die CD kopiert wird.

Wenn Sie eine Wiedergabeliste aus der Bibliothek abrufen, werden alle Änderungen, die Sie an der Wiedergabeliste vornehmen, in der Bibliothek des Benutzers widergespiegelt. Um dies zu vermeiden, rufen Sie [IWMPPlaylist::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo)auf, und übergeben Sie den Attributnamen "Temporary" und den Wert "true". Dadurch wird Ihre Wiedergabelisteninstanz in eine temporäre Wiedergabeliste konvertiert, die bearbeitet werden kann, ohne die ursprüngliche Wiedergabeliste zu ändern.

Each time you set a new playlist for burning, or make changes to an existing burn playlist, you must call [IWMPCdromBurn::refreshStatus](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-refreshstatus) to update the status information. Dadurch wird sichergestellt, Windows Media Player die Verarbeitung übernimmt, die erforderlich ist, um Ihnen genaue Statusinformationen für den CD-Vorgang zur Verfügung zu stellen.

Um den Typ der zu verwendenden CD anzugeben, rufen [Sie IWMPC dateityp::p ut \_ burnFormat auf.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnformat) Windows Media Player können Sie zwei Arten von CDs verwenden: Audio-CDs und Daten-CDs. Die [WMPFormat-Enumeration](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat) definiert die CD-Typen.

Sie können eine Volumebezeichnung für die CD angeben, indem Sie IWMPC wie die Bezeichnung [ \_ :p ut aufrufen.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_label)

Wenn Sie bereit sind, mit dem Erstellen der CD zu beginnen, rufen [Sie IWMPCwiedrIg::start Auf.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn) Sie können den Fortschritt des Vorgangs überwachen, indem Sie in regelmäßigen Abständen [IWMPCwiedErv::get \_ burnProgress aufrufen.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) Diese Methode ruft einen Statuswert für den gesamten Vorgang ab. Der abgerufene Wert ist eine Zahl, die den Prozentsatz des abgeschlossenen Abschlusses darstellt. Sie können den Zustand des Vorgangs überwachen, indem Sie das [IWMPEvents3::C enumerationStateChange-Ereignis](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnstatechange) behandeln, das die [WMP -Enumeration Verwendet,](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate) um den aktuellen Zustand anzugeben. Sie sollten darauf achten, den (vom -Ereignis **bereitgestellten) IWMPCwieder-Zeiger** mit dem Zeiger zu vergleichen, der Ihren Vorgang darstellt, um sicherzustellen, dass das Ereignis von Ihrem Vorgang ausgelöst wurde. Sie können den Vorgang beenden, indem Sie [IWMPC wies::stop Aus.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn)

Es gibt zwei Ereignisse, die Sie behandeln können, um Fehlerbenachrichtigungen zu Ihrem Benachrichtigungsvorgang zu erhalten. Das [IWMPEvents3::Cerror-Ereignis](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnerror) wird ausgelöst, wenn ein generischer Fehler auftritt. [IWMPEvents3::CmediaMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnmediaerror) wird ausgelöst, wenn ein bestimmtes Medienelement während der Störung einen Fehler verursacht. Jedes dieser Ereignisse stellt genau wie das **CfenEntStateChange-Ereignis** einen **IWMPCprotokoll-Zeiger** zur Verfügung, der den Vorgang darstellt, der das Ereignis ausgelöst hat. Das **CpatchMediaError-Ereignis** stellt einen **IDispatch-Zeiger** zur Unterstützung des Medienelements dar, das das Ereignis ausgelöst hat. Sie können **QueryInterface über diesen** Zeiger aufrufen, um einen **IWMPMedia-Zeiger** abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> <dt>

[**IWMPCführungsschnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**IWMPC wies die Schnittstelle auf.**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
</dt> <dt>

[**IWMPCcollection-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**IWMPEvents3-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**IWMPMedia-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Temporäres Attribut**](temporary-attribute.md)
</dt> </dl>

 

 




