---
title: Funktionsweise der asynchronen Bindung und Speicherung
description: Der asynchrone Speicher erweitert die strukturierte com-Speicher Spezifikation, um das Herunterladen von Speicher Objekten bei Netzwerken mit hoher Latenz und langsamen Verbindungen wie dem Internet zu unterstützen.
ms.assetid: 891152c3-5abd-45e4-a7bb-0aac23262b03
keywords:
- Funktionsweise der asynchronen Bindung und Speicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626e8c7a55b667e158de42b3c88a17315b5e41ad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390487"
---
# <a name="how-asynchronous-binding-and-storage-work"></a>Funktionsweise der asynchronen Bindung und Speicherung

Der asynchrone Speicher erweitert die strukturierte com-Speicher Spezifikation, um das Herunterladen von Speicher Objekten bei Netzwerken mit hoher Latenz und langsamen Verbindungen wie dem Internet zu unterstützen. Der asynchrone Speicher kann zusammen mit asynchronen Monikern verwendet werden, um ein umfassendes asynchrones Bindungsverhalten bereitzustellen.

## <a name="document-object-embedded-in-a-web-page"></a>Dokument Objekt, eingebettet in eine Webseite

Wenn ein Benutzer auf einen Link klickt, der ein Dokument darstellt, das auf einer Webseite eingebettet ist, treten die folgenden Ereignisse auf:

1.  Der Browser Ruft die [**mkparser-DisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) -Funktion auf und übergibt die Link-URL.
2.  [**Mkparser-DisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) analysiert die URL, erstellt einen entsprechenden asynchronen Moniker und gibt einen Zeiger auf die [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) -Schnittstelle des Monikers zurück.
3.  Der Browser ruft [**isasyncmoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) auf, um zu bestimmen, ob der Moniker asynchron ist, erstellt einen Bindungs Kontext, registriert die [**ibindstatus-Callback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) -Schnittstelle beim Bindungs Kontext nur, wenn der Moniker asynchron ist, und ruft [**IMoniker:: bindjeobject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject)auf und übergibt den Bindungs Kontext.
4.  Der Moniker bindet an das-Objekt und fragt ihn nach der [**ipersistmoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) -Schnittstelle ab, die angibt, ob das Objekt asynchrone Bindungen und Speicher unterstützt. Wenn das Objekt einen Zeiger auf **ipersistmoniker** zurückgibt:

    1.  Der URL-Moniker ruft [**ipersistmoniker:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85))auf und übergibt seinen eigenen [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) -Zeiger an das-Objekt.
    2.  Das-Objekt ändert den Bindungs Kontext, wählt, ob er einen blockierenden oder nicht blockierenden Speicher benötigt, registriert seinen eigenen [**ibindstatus-Rückruf**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) und ruft [**IMoniker:: bindesstorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) für den Zeiger auf, der über [**ipersistmoniker:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85))empfangen wurde.
    3.  Der Moniker erstellt einen asynchronen Speicher, behält einen Verweis auf die [**ifilllockbytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) -Schnittstelle des Wrapper Objekts bei, registriert die [**iprogressnotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) -Schnittstelle im Stamm Speicher und ruft [**IPersistStorage:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load)auf und übergibt dabei den [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Zeiger des asynchronen Speichers. Beim Eintreffen von Daten (in einem Hintergrund Thread) ruft der Moniker **ifilllockbytes** auf, um die [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) in der temporären Datei auszufüllen.
    4.  Das-Objekt liest Daten aus dem Speicher und gibt von [**ipersistmoniker:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)) zurück, wenn ausreichend Daten empfangen wurden, um sich selbst zu initialisieren. Wenn das Objekt versucht, Daten zu lesen, die noch nicht heruntergeladen wurden, empfängt das Download Programm eine Benachrichtigung über [**iprogressnotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify). Innerhalb der [**iprogressnotify:: OnProgress**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) -Methode blockiert der Download Thread entweder in einer modalen Nachrichten Schleife oder bewirkt, dass der asynchrone Speicher "E Pending" zurückgibt \_ , je nachdem, ob das Objekt einen blockierenden oder nicht blockierenden Speicher angefordert hat.

5.  Wenn das Objekt [**ipersistmoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))nicht implementiert, fragt der Moniker [**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage)ab, was darauf hinweist, dass der persistente Zustand des Objekts in einem Speicher Objekt gespeichert wird. Wenn das Objekt einen Zeiger auf **IPersistStorage** zurückgibt:

    1.  Der Moniker ruft [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) auf sich selbst, das eine blockierende [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Anforderung anfordert (da das Objekt nicht asynchron unterstützt wird), erstellt einen asynchronen Speicher, behält einen Verweis auf die [**ifilllockbytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) -Schnittstelle des Wrapper Objekts, registriert die [**iprogressnotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) **-Schnitt** Stelle im Stamm Speicher und ruft [**IPersistStorage:**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) Beim Eintreffen von Daten (in einem Hintergrund Thread) ruft der Moniker [**ifilllockbytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) auf, um die [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) in der temporären Datei auszufüllen.
    2.  Das-Objekt liest Daten aus dem Speicher und gibt von [**IPersistStorage:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) zurück, wenn genügend Daten für die Initialisierung gefunden wurden. Wenn das Objekt versucht, Daten zu lesen, die noch nicht heruntergeladen wurden, erhält es eine Benachrichtigung über [**iprogressnotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify). Innerhalb der [**iprogressnotify:: OnProgress**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) -Methode blockiert der Download Thread immer in einer modalen Nachrichten Schleife.

6.  Unabhängig davon, ob der Download synchron oder asynchron ist, gibt der Moniker von [**IMoniker:: bindtoken Object**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject)zurück, und der Browser empfängt das initialisierte Objekt, das er angefordert hat.
7.  Der Browser fragt [**IOleObject**](/windows/win32/api/oleidl/nn-oleidl-ioleobject) ab und hostet das Objekt als Dokument Objekt. (An diesem Punkt wird das Objekt möglicherweise nicht vollständig initialisiert, aber genug, um etwas Nützliches anzuzeigen. in diesem Fall wird das Herunterladen im Hintergrund fortgesetzt.)

 

 