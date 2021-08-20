---
title: Funktionsweise von asynchroner Bindung und Storage
description: Asynchroner Speicher erweitert die COM-Spezifikation für strukturierten Speicher, um das Herunterladen von Speicherobjekten in Netzwerken mit hoher Latenz und langsamen Verbindungen wie dem Internet zu unterstützen.
ms.assetid: 891152c3-5abd-45e4-a7bb-0aac23262b03
keywords:
- Funktionsweise von asynchroner Bindung und Storage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176ff85044210a94cecf2649fa7475eae2b291def43b0876d2ecbc9c98b0866e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961900"
---
# <a name="how-asynchronous-binding-and-storage-work"></a>Funktionsweise von asynchroner Bindung und Storage

Asynchroner Speicher erweitert die COM-Spezifikation für strukturierten Speicher, um das Herunterladen von Speicherobjekten in Netzwerken mit hoher Latenz und langsamen Verbindungen wie dem Internet zu unterstützen. Der asynchrone Speicher arbeitet mit asynchronen Monikern zusammen, um ein vollständiges asynchrones Bindungsverhalten bereitzustellen.

## <a name="document-object-embedded-in-a-web-page"></a>In eine Webseite eingebettetes Dokumentobjekt

Wenn ein Benutzer auf einen Link klickt, der ein in eine Webseite eingebettetes Dokument darstellt, treten die folgenden Ereignisse auf:

1.  Der Browser ruft die [**MkParseDisplayName-Funktion**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) auf und übergibt die Link-URL.
2.  [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) analysiert die URL, erstellt einen entsprechenden asynchronen Moniker und gibt einen Zeiger auf die [**IMoniker-Schnittstelle des Monikers**](/windows/win32/api/objidl/nn-objidl-imoniker) zurück.
3.  Der Browser ruft [**IsAsyncMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) auf, um zu bestimmen, ob der Moniker asynchron ist, erstellt einen Bindungskontext, registriert die [**IBindStatusCallback-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) mit dem Bindungskontext, nur wenn der Moniker asynchron ist, und ruft [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject)auf und übergibt den Bindungskontext.
4.  Der Moniker wird an das -Objekt gebunden und fragt es nach der [**IPersistMoniker-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) ab, die angibt, ob das Objekt asynchrone Bindung und Speicherung unterstützt. Wenn das -Objekt einen Zeiger auf **IPersistMoniker** zurückgibt:

    1.  Der URL-Moniker ruft [**IPersistMoniker::Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85))auf und übergibt seinen eigenen [**IMoniker-Zeiger**](/windows/win32/api/objidl/nn-objidl-imoniker) an das -Objekt.
    2.  Das -Objekt ändert den Bindungskontext, wählt aus, ob ein blockierender oder nicht blockierender Speicher verwendet werden soll, registriert seinen eigenen [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) und ruft [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) auf dem Zeiger auf, den es über [**IPersistMoniker::Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85))empfangen hat.
    3.  Der Moniker erstellt einen asynchronen Speicher, behält einen Verweis auf die [**IFillLockBytes-Schnittstelle**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) des Wrapperobjekts bei, registriert die [**IProgressNotify-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) im Stammspeicher und ruft [**IPersistStorage::Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load)auf und übergibt den [**IStorage-Zeiger**](/windows/desktop/api/Objidl/nn-objidl-istorage) des asynchronen Speichers. Wenn Daten eintreffen (in einem Hintergrundthread), ruft der Moniker **IFillLockBytes** auf, um die [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) in der temporären Datei zu füllen.
    4.  Das -Objekt liest Daten aus dem Speicher und gibt aus [**IPersistMoniker::Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)) zurück, wenn genügend Daten empfangen wurden, um sich selbst als initialisiert zu betrachten. Wenn das -Objekt versucht, Daten zu lesen, die noch nicht heruntergeladen wurden, erhält der Downloader eine Benachrichtigung über [**IProgressNotify.**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) Innerhalb der [**IProgressNotify::OnProgress-Methode**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) wird der Downloadthread entweder in einer modalen Nachrichtenschleife blockiert oder bewirkt, dass der asynchrone Speicher E \_ PENDING zurückgibt, je nachdem, ob das Objekt einen blockierenden oder nicht blockierenden Speicher angefordert hat.

5.  Wenn das -Objekt [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))nicht implementiert, fragt der Moniker [**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage)ab, was angibt, dass der persistente Zustand des Objekts in einem Speicherobjekt gespeichert ist. Wenn das -Objekt einen Zeiger auf **IPersistStorage** zurückgibt:

    1.  Der Moniker ruft [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) für sich selbst auf und fordert eine blockierende [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) an (da das Objekt nicht asynchron ist), erstellt einen asynchronen Speicher, behält einen Verweis auf die [**IFillLockBytes-Schnittstelle**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) des Wrapperobjekts bei, registriert die [**IProgressNotify-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) im Stammspeicher und ruft [**IPersistStorage::Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load)auf und übergibt den **IStorage-Zeiger** des asynchronen Speichers. Wenn Daten eintreffen (in einem Hintergrundthread), ruft der Moniker [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) auf, um die [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) in der temporären Datei auszufüllen.
    2.  Das -Objekt liest Daten aus dem Speicher und gibt aus [**IPersistStorage::Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) zurück, wenn genügend Daten empfangen wurden, um sich selbst als initialisiert zu betrachten. Wenn das Objekt versucht, Daten zu lesen, die noch nicht heruntergeladen wurden, erhält es eine Benachrichtigung über [**IProgressNotify.**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) Innerhalb der [**IProgressNotify::OnProgress-Methode**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) wird der herunterladende Thread immer in einer modalen Nachrichtenschleife blockiert.

6.  Unabhängig davon, ob der Download synchron oder asynchron ist, gibt der Moniker von [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject)zurück, und der Browser empfängt das angeforderte initialisierte Objekt.
7.  Der Browser fragt [**IOleObject**](/windows/win32/api/oleidl/nn-oleidl-ioleobject) ab und hostet das Objekt als Dokumentobjekt. (An diesem Punkt wird das Objekt möglicherweise nicht vollständig initialisiert, aber ausreichend, um etwas Nützliches anzuzeigen. In diesem Fall wird der Download im Hintergrund fortgesetzt.)

 

 