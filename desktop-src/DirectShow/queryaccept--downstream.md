---
description: Queryaccept (Downstream)
ms.assetid: 3ca30f62-c320-40ea-9bf5-022abad912c4
title: Queryaccept (Downstream)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9015e0a246abb9fb996c0771e4bc935cccda054d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104554229"
---
# <a name="queryaccept-downstream"></a>Queryaccept (Downstream)

Dieser Mechanismus ermöglicht es einer Ausgabepin, dem downstreampeer ein neues Format vorzuschlagen. Das neue Format darf keine größere Puffergröße erfordern. Die Ausgabe-PIN führt folgende Aktionen aus:

1.  Ruft [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) oder [**ipinconnection::D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) auf der Downstream-PIN auf, um zu überprüfen, ob die andere Pin den neuen Medientyp akzeptieren kann (siehe Abbildung, Schritt A).
2.  Wenn der Rückgabewert aus Schritt 1 S \_ OK ist, fügt die PIN den Medientyp an das nächste Beispiel an. Zu diesem Zweck wird zuerst [**imemzucator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) aufgerufen, um das Beispiel (B) zu erhalten. Anschließend wird [**imediasample:: setmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) aufgerufen, um den Medientyp an dieses Beispiel (C) anzufügen. Durch Anfügen des Medientyps an das Beispiel gibt der Filter an, dass sich das Format geändert hat, beginnend mit diesem Beispiel.
3.  Die PIN liefert das Beispiel (D).
4.  Wenn der Downstream-Filter das Beispiel empfängt, ruft er [**imediasample:: getmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) auf, um den neuen Medientyp abzurufen.

    ![queryaccept (Downstream)](images/dynformat3.png)

Alle Pins unterstützen die- `QueryAccept` Methode. Diese Methode ist jedoch etwas mehrdeutig, da der Rückgabewert S \_ OK nicht immer garantiert, dass Sie das Format ändern können, während das Diagramm aktiv ist. Einige Filter geben möglicherweise S OK zurück, \_ lehnen die Änderung jedoch ab, wenn das Diagramm aktiv ist. Die **dynamicqueryaccept** -Methode, die von einigen Eingabe Pins unterstützt wird, definiert e OK explizit, \_ um zu bedeuten, dass die PIN Formate ändern kann, während Sie aktiv ist. Wenn eine Eingabe-PIN die **ipinconnection** -Schnittstelle unterstützt, sollte **dynamicqueryaccept** anstelle von aufgerufen werden `QueryAccept` .

In den meisten Fällen lässt dieser Mechanismus keine drastischen Änderungen am Format zu, wie z. b. das Ändern der Bittiefe. Eine Situation, in der Sie verwendet werden kann, ist, wenn ein Video Decoder Paletten wechselt. Die grundlegenden Details des Formats bleiben unverändert, wie z. b. die Bild Dimensionen und die Bittiefe, aber der neue Medientyp verfügt über einen anderen Satz von paletteneinträgen.

**Implementierungs Hinweis**

In den DirectShow-Basisklassen ruft [**cbasepin:: queryaccept**](cbasepin-queryaccept.md) die **checkmediatype** -Methode auf, die auch während der anfänglichen Pin-Verbindung aufgerufen wird. Bei einem Transformations Filter sollte die **checkmediatype** -Methode der Eingabe-PIN immer überprüfen, ob die Ausgabe-PIN verbunden ist, und wenn dies der Fall ist, ob der Eingabe Medientyp mit dem Ausgabe Medientyp kompatibel ist. Daher wird diese Implementierung wahrscheinlich für gültig sein `QueryAccept` . Andernfalls sollten Sie außer Kraft setzen, um `QueryAccept` zusätzliche Überprüfungen durchzuführen, die benötigt werden. Beachten Sie außerdem, dass die [**ctransformfilter**](ctransformfilter.md) -Klasse diese Logik innerhalb der Methoden **checkinputtype** und **checktransform** kapselt. Die [**ctransinplacefilter**](ctransinplacefilter.md) -Klasse hingegen ruft immer `QueryAccept` für den nächsten Upstream-oder downstreamfilter auf.

Die [**cbaseinputpin:: Receive**](cbaseinputpin-receive.md) -Methode überprüft, ob ein Medientyp für das eingehende Beispiel vorhanden ist. ist dies der Fall, wird **checkmediatype** aufgerufen. Der **m \_ MT** -Member der PIN, der den aktuellen Medientyp enthält, wird jedoch nicht aktualisiert. Wenn Ihr Filter das Beispiel verarbeitet, sollten Sie das Beispiel auf einen Medientyp überprüfen. Wenn ein neuer Typ vorhanden ist, müssen Sie ihn wahrscheinlich speichern, indem Sie entweder **setmediatype** auf der PIN aufrufen oder den Wert von **m \_ MT** direkt festlegen. Andererseits speichert die [**cvideotransformfilter**](cvideotransformfilter.md) -Klasse, die für Video Transformations Filter entwickelt wurde, den Medientyp, wenn Sie sich ändert. Weitere Informationen finden Sie im Quellcode für [**cvideotransformfilter:: Receive**](cvideotransformfilter-receive.md) in der DirectShow-Basisklassen Bibliothek.

In einigen Fällen können Sie einfach den-Befehl `QueryAccept` Downstream übergeben und dann den Medientyp an das Ausgabe Beispiel anfügen und den downstreamfilter das Format ändern.

 

 



