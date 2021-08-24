---
description: QueryAccept (Downstream)
ms.assetid: 3ca30f62-c320-40ea-9bf5-022abad912c4
title: QueryAccept (Downstream)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ec5c26209839f0dcd8351cc9a7ca84227faa2289d44d46c2c321fce0429e3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747734"
---
# <a name="queryaccept-downstream"></a>QueryAccept (Downstream)

Dieser Mechanismus ermöglicht es einem Ausgabepin, seinem Downstreamspeer ein neues Format vorzuschlagen. Das neue Format darf keine größere Puffergröße erfordern. Der Ausgabepin führt folgende Schritte aus:

1.  Ruft [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) oder [**IPinConnection::D ynamicQueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) für den Downstreampin auf, um zu überprüfen, ob der andere Pin den neuen Medientyp akzeptieren kann (siehe Abbildung, Schritt A).
2.  Wenn der Rückgabewert aus Schritt 1 S \_ OK ist, fügt die Stecknadel den Medientyp an das nächste Beispiel an. Dazu ruft es zuerst [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) auf, um das Beispiel (B) abzurufen. Anschließend wird [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) zum Anfügen des Medientyps an dieses Beispiel (C) aufrufen. Durch Anfügen des Medientyps an das Beispiel gibt der Filter an, dass sich das Format geändert hat, beginnend mit diesem Beispiel.
3.  Die Stecknadel liefert das Beispiel (D).
4.  Wenn der Downstreamfilter das Beispiel empfängt, ruft er [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) auf, um den neuen Medientyp abzurufen.

    ![queryaccept (downstream)](images/dynformat3.png)

Alle Pins unterstützen die `QueryAccept` -Methode. Diese Methode ist jedoch etwas mehrdeutig, da der Rückgabewert S \_ OK nicht immer garantiert, dass Sie das Format ändern können, während das Diagramm aktiv ist. Einige Filter geben möglicherweise S \_ OK zurück, weisen die Änderung jedoch zurück, wenn das Diagramm aktiv ist. Die **DynamicQueryAccept-Methode,** die von einigen Eingabepins unterstützt wird, definiert explizit S \_ OK, um zu bedeuten, dass der Pin formate ändern kann, während er aktiv ist. Wenn ein Eingabepin die **IPinConnection-Schnittstelle** unterstützt, sollten Sie **DynamicQueryAccept** anstelle von `QueryAccept` aufrufen.

In den meisten Fällen lässt dieser Mechanismus keine drastischen Änderungen am Format zu, z. B. das Ändern der Bittiefe. Eine Situation, in der es verwendet werden kann, ist, wenn ein Videodecoder Paletten wechselt. Die grundlegenden Details des Formats bleiben unverändert, z. B. die Bilddimensionen und die Bittiefe, aber der neue Medientyp verfügt über einen anderen Satz von Paletteneinträgen.

**Implementierungshinweis**

In den DirectShow-Basisklassen ruft [**CBasePin::QueryAccept**](cbasepin-queryaccept.md) die **CheckMediaType-Methode** auf, die auch während der ersten Pinverbindung aufgerufen wird. Bei einem Transformationsfilter sollte die **CheckMediaType-Methode** des Eingabepins immer überprüfen, ob der Ausgabepin verbunden ist, und in diesem Fall, ob der Eingabemedientyp mit dem Ausgabemedientyp kompatibel ist. Daher ist diese Implementierung wahrscheinlich für `QueryAccept` gültig. Wenn dies nicht der Fall ist, sollten Sie außer Kraft `QueryAccept` setzen, um alle erforderlichen zusätzlichen Überprüfungen durchzuführen. Beachten Sie außerdem, dass die [**CTransformFilter-Klasse**](ctransformfilter.md) diese Logik in den **Methoden CheckInputType** und **CheckTransform** kapselt. Die [**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md) ruft dagegen immer `QueryAccept` für den nächsten Upstream- oder Downstreamfilter auf.

Die [**CBaseInputPin::Receive-Methode**](cbaseinputpin-receive.md) überprüft im eingehenden Beispiel auf einen Medientyp, und wenn vorhanden, ruft **CheckMediaType** auf. Der **m \_ mt-Member** des Pins, der den aktuellen Medientyp enthält, wird jedoch nicht aktualisiert. Wenn Ihr Filter das Beispiel verarbeitet, sollten Sie das Beispiel auf einen Medientyp überprüfen. Wenn ein neuer Typ vorhanden ist, müssen Sie ihn wahrscheinlich speichern, indem Sie **Entweder SetMediaType** an Ihrem Pin aufrufen oder den Wert von **m \_ mt** direkt festlegen. Andererseits speichert die [**CVideoTransformFilter-Klasse,**](cvideotransformfilter.md) die für Videotransformationsfilter konzipiert ist, den Medientyp, wenn er sich ändert. Weitere Informationen finden Sie im Quellcode für [**CVideoTransformFilter::Receive**](cvideotransformfilter-receive.md) in der DirectShow-Basisklassenbibliothek.

In einigen Fällen können Sie einfach den `QueryAccept` Aufruf downstream übergeben, dann den Medientyp an das Ausgabebeispiel anfügen und den Downstreamfilter die Formatänderung verarbeiten lassen.

 

 



