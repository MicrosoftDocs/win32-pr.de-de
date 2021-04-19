---
title: Implementierung von IStream-Verbund Dateien
description: Die IStream-Schnittstelle unterstützt das Lesen und Schreiben von Daten in Streamobjekte. In einem strukturierten Speicher Objekt enthalten Streamobjekte die Daten, und die Speicher stellen die Struktur bereit.
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- IStream-Schnittstellen-STG, Implementierung von Verbund Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d15e671521f4a1e81b78579bc1225eccb48898
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "106364271"
---
# <a name="istream---compound-file-implementation"></a>Implementierung von IStream-Verbund Dateien

Die [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Schnittstelle unterstützt das Lesen und Schreiben von Daten in Streamobjekte. In einem strukturierten Speicher Objekt enthalten Streamobjekte die Daten, und die Speicher stellen die Struktur bereit. Einfache Daten können direkt in einen Stream geschrieben werden, aber häufig sind Streams Elemente, die in einem Speicher Objekt geschachtelt sind. Sie ähneln Standard Dateien.

Die Spezifikation von [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) definiert mehr Funktionen, als von der com-Implementierung unterstützt werden. Die **IStream** -Schnittstelle definiert z. b. Datenströme bis zu 2 ⁶ ⁴ Bytes, die einen 64-Bit-Such Zeiger erfordern. Die com-Implementierung unterstützt jedoch nur Datenströme mit einer Länge von bis zu 2 ³ ² (4 GB), Lese-und Schreibvorgänge sind immer auf jeweils 2 ³ ² Byte beschränkt. Die com-Implementierung unterstützt auch keine Stream-Transaktions-oder Regions sperren.

Um einen einfachen Datenstrom auf der Grundlage des globalen Speichers zu erstellen, rufen Sie einen [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Zeiger ab, indem Sie die API-Funktion [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)aufrufen. Wenn Sie einen **IStream** -Zeiger innerhalb eines Verbund Datei Objekts abrufen möchten, müssen Sie entweder [**stgkreatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) oder [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)aufrufen. Diese Funktionen rufen einen [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Zeiger ab, mit dem Sie dann für einen **IStream** -Zeiger " [**foratestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) " oder " [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) " aufrufen können. In beiden Fällen wird derselbe **IStream** -Implementierungs Code verwendet.

> [!Note]  
> Die Implementierung der Verbund Datei von strukturiertem Speicher ist in einer [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode für [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream)nicht erfolgreich, enthält jedoch die [**Lese**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) -und [**Schreib**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) Methoden über den [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Schnittstellen Zeiger.

 

## <a name="when-to-use"></a>Verwendungs Zeitpunkt

Ruft die Methoden von [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) auf, um Daten zu lesen und in einen Stream zu schreiben.

Da Stream-Objekte an andere Prozesse gemarshallt werden können, können Anwendungen die Daten in Speicher Objekten freigeben, ohne globalen Speicher verwenden zu müssen. In der Implementierung der com-Verbund Datei von Streamobjekten wird durch die benutzerdefinierten Marshallingfunktionen in com eine Remote Version des ursprünglichen Objekts im neuen Prozess erstellt, wenn die beiden Prozesse über Shared-Memory-Zugriff verfügen. Folglich muss die Remote Version nicht mit dem ursprünglichen Prozess kommunizieren, um die zugehörigen Funktionen auszuführen.

Die Remote Version des Stream-Objekts nutzt denselben Such Zeiger wie der ursprüngliche Datenstrom. Wenn Sie den Seek-Zeiger nicht freigeben möchten, verwenden Sie die [**IStream:: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) -Methode, um eine Kopie des Datenstrom Objekts für den Remote Prozess bereitzustellen.

> [!Note]
> Wenn Sie ein Streamobjekt erstellen, das größer als der Heap im Arbeitsspeicher Ihres Computers ist, und Sie ein **HGLOBAL** -Handle für ein globales Speicher Objekt verwenden, ruft das Stream-Objekt die [**globalrebelegc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) -Methode intern auf, wenn Sie mehr Arbeitsspeicher benötigt. Da **globalrezuweisungen** immer Daten aus der Quelle in das Ziel kopiert, erfordert die Erhöhung eines Streamobjekts von 20 MB auf 25 MB beispielsweise eine große Zeit Menge. Dies liegt an der Größe der kopierten Inkremente und wird verschlechtert, wenn auf dem Computer weniger als 45 MB Arbeitsspeicher vorhanden sind, da Datenträger ausgetauscht werden.
>
> Die bevorzugte Lösung besteht darin, eine [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Methode zu implementieren, die von [**virtualbelegc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) zugeordnete Arbeitsspeicher anstelle von [**globalbelegc**](/windows/desktop/api/winbase/nf-winbase-globalalloc)verwendet. Dadurch kann ein großer Teil des virtuellen Adressraums reserviert werden, und anschließend wird der Arbeitsspeicher in diesem Adressraum nach Bedarf übernommen. Es findet kein Daten Kopiervorgang statt, und der Arbeitsspeicher wird nur nach Bedarf committet.
>
> Eine Alternative zu [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) besteht darin, die [**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) -Methode für das Stream-Objekt aufzurufen, um die Speicher Belegung im Voraus zu erhöhen. Dies ist jedoch nicht so effizient wie die Verwendung von [**virtualzugewiesenen**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), wie oben beschrieben.

 

## <a name="methods"></a>Methoden

<dl> <dt>

<span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dd>

Liest eine angegebene Anzahl von Bytes beginnend beim aktuellen Suchzeiger aus dem Datenstromobjekt in den Arbeitsspeicher. Diese Implementierung gibt "S OK" zurück, \_ Wenn das Ende des Streams während des Lesevorgang erreicht wurde. (Dies ist das gleiche wie das "Dateiende"-Verhalten im DOS-FAT-Dateisystem.)

</dd> <dt>

<span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)
</dt> <dd>

Schreibt eine angegebene Anzahl von Bytes in das Streamobjekt, beginnend beim aktuellen Such Zeiger. In dieser Implementierung sind Streamobjekte nicht sparsam. Alle Füll Bytes werden schließlich auf dem Datenträger zugeordnet und dem Stream zugewiesen.

</dd> <dt>

<span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream:: Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)
</dt> <dd>

Verschiebt den Suchzeiger auf eine neue Position im Verhältnis zum Anfang oder Ende des Datenstroms bzw. zum aktuellen Suchzeiger.

</dd> <dt>

<span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)
</dt> <dd>

Ändert die Größe des Streamobjekts. In dieser Implementierung gibt es keine Garantie dafür, dass der zugeordnete Speicherplatz zusammenhängend ist.

</dd> <dt>

<span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)
</dt> <dd>

Kopiert eine angegebene Anzahl von Bytes vom aktuellen Suchzeiger im Datenstrom an den aktuellen Suchzeiger in einem anderen Datenstrom.

</dd> <dt>

<span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)
</dt> <dd>

Die Implementierung der Verbund Datei von [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) unterstützt das Öffnen von Streams nur im direkten Modus, nicht im Transaktionsmodus. Daher hat die-Methode keine Auswirkung, wenn Sie nicht aufgerufen wird, um alle Speicherpuffer auf die nächste Speicher Ebene zu leeren.

In dieser Implementierung spielt es keine Rolle, ob Sie Änderungen an Streams übertragen. Sie benötigen nur Änderungen für Speicher Objekte.

</dd> <dt>

<span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)
</dt> <dd>

Diese Implementierung bietet keine Unterstützung für transaktive Streams, sodass ein Aufrufder Methode keine Auswirkung hat.

</dd> <dt>

<span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)
</dt> <dd>

Bereichs Sperren werden von dieser Implementierung nicht unterstützt, sodass ein aufrufender aufrufungsmethode keine Auswirkung hat.

</dd> <dt>

<span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream:: UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)
</dt> <dd>

Entfernt die Zugriffsbeschränkung für einen Bereich von Bytes, der zuvor durch [**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)eingeschränkt wurde.

</dd> <dt>

<span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)
</dt> <dd>

Ruft die [**Statuslisten**](/windows/win32/api/objidl/ns-objidl-statstg) Struktur für diesen Datenstrom ab.

</dd> <dt>

<span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream:: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)
</dt> <dd>

Erstellt ein neues Datenstromobjekt mit einem eigenen Suchzeiger, der auf die gleichen Bytes wie der Originaldatenstrom verweist.

</dd> </dl>

Ein [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) im einfachen Modus unterliegt den folgenden Einschränkungen.

-   Ein Datenstrom ist der einfache Modus, wenn er von einem Speicher im einfachen Modus erstellt oder geöffnet wurde. Bei einem Speicher handelt es sich um einen einfachen Modus, wenn er erstellt oder geöffnet wird, wobei das \_ in der *GRF Mode* -Parameter festgelegte STGM Simple-Flag
-   Die Methoden [**Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) und [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) werden nicht unterstützt.
-   Die [**stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) -Methode wird unterstützt, aber der STATFLAG- \_ Wert Noname muss angegeben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**"Kreatestreamonhglobal"**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[**Stgkreatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 