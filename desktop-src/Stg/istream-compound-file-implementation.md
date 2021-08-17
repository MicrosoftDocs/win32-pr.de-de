---
title: IStream – Verbunddateiimplementierungen
description: Die IStream-Schnittstelle unterstützt das Lesen und Schreiben von Daten in Streamobjekte. In einem strukturierten Speicherobjekt enthalten Streamobjekte die Daten, und Speicher stellen die Struktur bereit.
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- IStream Strctd Stg , Verbunddateiimplementierungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57a974e44e66d8709a002f9635c41f751e80ab1d3f3875f8eb129cef2b14847
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961208"
---
# <a name="istream---compound-file-implementation"></a>IStream – Verbunddateiimplementierungen

Die [**IStream-Schnittstelle**](/windows/desktop/api/Objidl/nn-objidl-istream) unterstützt das Lesen und Schreiben von Daten in Streamobjekte. In einem strukturierten Speicherobjekt enthalten Streamobjekte die Daten, und Speicher stellen die Struktur bereit. Einfache Daten können direkt in einen Stream geschrieben werden, aber häufiger sind Streams Elemente, die in einem Speicherobjekt geschachtelt sind. Sie ähneln Standarddateien.

Die Spezifikation von [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) definiert mehr Funktionalität, als von der COM-Implementierung unterstützt wird. Beispielsweise definiert die **IStream-Schnittstelle** Streams mit einer Länge von bis zu 2⁶⁴ Bytes, die einen 64-Bit-Suchzeiger erfordern. Die COM-Implementierung unterstützt jedoch nur Streams mit einer Länge von bis zu 2 gb (4 GB), und Lese- und Schreibvorgänge sind immer auf jeweils 2 gb beschränkt. Die COM-Implementierung unterstützt auch keine Streamtransaktionen oder Regionssperren.

Um einen einfachen Stream basierend auf dem globalen Arbeitsspeicher zu erstellen, rufen Sie einen [**IStream-Zeiger**](/windows/desktop/api/Objidl/nn-objidl-istream) ab, indem Sie die API-Funktion [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)aufrufen. Um einen **IStream-Zeiger** in einem Verbunddateiobjekt abzurufen, rufen Sie entweder [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) oder [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)auf. Diese Funktionen rufen einen [**IStorage-Zeiger**](/windows/desktop/api/Objidl/nn-objidl-istorage) ab, mit dem Sie dann [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) oder [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) für einen **IStream-Zeiger** aufrufen können. In beiden Fällen  wird der gleiche IStream-Implementierungscode verwendet.

> [!Note]  
> Die Verbunddateiimplementierung des strukturierten Speichers ist für eine [**QueryInterface-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream)nicht erfolgreich, enthält jedoch die [**Read-**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) und [**Write-Methoden**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) über den IStream-Schnittstellenzeiger. [](/windows/desktop/api/Objidl/nn-objidl-istream)

 

## <a name="when-to-use"></a>Verwendungs wann

Rufen Sie die Methoden von [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) auf, um Daten zu lesen und in einen Stream zu schreiben.

Da Streamobjekte an andere Prozesse gemarshallt werden können, können Anwendungen die Daten in Speicherobjekten freigeben, ohne globalen Arbeitsspeicher verwenden zu müssen. In der COM-Verbunddateiimplementierung von Streamobjekten erstellen die benutzerdefinierten Marshalling-Einrichtungen in COM eine Remoteversion des ursprünglichen Objekts im neuen Prozess, wenn die beiden Prozesse über Shared Memory-Zugriff verfügen. Daher muss die Remoteversion nicht mit dem ursprünglichen Prozess kommunizieren, um ihre Funktionen auszuführen.

Die Remoteversion des Streamobjekts verwendet den gleichen Suchzeiger wie der ursprüngliche Stream. Wenn Sie den Suchzeiger nicht freigeben möchten, verwenden Sie die [**IStream::Clone-Methode,**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) um eine Kopie des Streamobjekts für den Remoteprozess bereitzustellen.

> [!Note]
> Wenn Sie ein Streamobjekt erstellen, das größer als der Heap im Arbeitsspeicher Ihres Computers ist, und Sie ein **HGLOBAL-Handle** für ein globales Speicherobjekt verwenden, ruft das Streamobjekt intern die [**GlobalRealloc-Methode**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) auf, um mehr Arbeitsspeicher zu benötigen. Da **GlobalRealloc** daten immer aus der Quelle in das Ziel kopiert, erfordert beispielsweise das Erhöhen eines Streamobjekts von 20 MB auf 25 MB viel Zeit. Dies ist auf die Größe der kopierten Inkremente zurückzuführen und wird verringert, wenn aufgrund des Datenträgeraustauschs weniger als 45 MB Arbeitsspeicher auf dem Computer vorhanden sind.
>
> Die bevorzugte Lösung besteht darin, eine [**IStream-Methode**](/windows/desktop/api/Objidl/nn-objidl-istream) zu implementieren, die von [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) belegten Arbeitsspeicher anstelle von [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc)verwendet. Dadurch kann ein großer Teil des virtuellen Adressraums reserviert und anschließend nach Bedarf ein Commit des Arbeitsspeichers innerhalb dieses Adressraums erfolgen. Es erfolgt kein Datenkopiervorgang, und für den Arbeitsspeicher wird nur ein Commit ausgeführt, wenn er erforderlich ist.
>
> Eine Alternative zu [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) besteht darin, die [**IStream::SetSize-Methode**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) für das Streamobjekt aufzurufen, um die Speicherbelegung im Voraus zu erhöhen. Dies ist jedoch nicht so effizient wie die Verwendung von [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), wie oben beschrieben.

 

## <a name="methods"></a>Methoden

<dl> <dt>

<span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dd>

Liest eine angegebene Anzahl von Bytes beginnend beim aktuellen Suchzeiger aus dem Datenstromobjekt in den Arbeitsspeicher. Diese Implementierung gibt S \_ OK zurück, wenn das Ende des Streams während des Lesens erreicht wurde. (Dies entspricht dem Verhalten des Dateiendes im MS-DOS FAT-Dateisystem.)

</dd> <dt>

<span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)
</dt> <dd>

Schreibt eine angegebene Zahl aus Bytes ab dem aktuellen Suchzeiger in das Streamobjekt. In dieser Implementierung sind Streamobjekte nicht sparse. Alle Füllbytes werden schließlich auf dem Datenträger zugeordnet und dem Stream zugewiesen.

</dd> <dt>

<span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream::Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)
</dt> <dd>

Verschiebt den Suchzeiger auf eine neue Position im Verhältnis zum Anfang oder Ende des Datenstroms bzw. zum aktuellen Suchzeiger.

</dd> <dt>

<span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)
</dt> <dd>

Ändert die Größe des Streamobjekts. In dieser Implementierung gibt es keine Garantie dafür, dass der zugeordnete Speicherplatz zusammenhängend ist.

</dd> <dt>

<span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)
</dt> <dd>

Kopiert eine angegebene Anzahl von Bytes vom aktuellen Suchzeiger im Datenstrom an den aktuellen Suchzeiger in einem anderen Datenstrom.

</dd> <dt>

<span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream::Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)
</dt> <dd>

Die Verbunddateiimplementierungen von [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) unterstützen das Öffnen von Datenströmen nur im direkten Modus, nicht im Transaktionsmodus. Daher hat die -Methode keine Auswirkung, wenn sie aufgerufen wird, außer alle Speicherpuffer auf die nächste Speicherebene zu leeren.

In dieser Implementierung spielt es keine Rolle, ob Sie Änderungen an Streams committen, sondern nur Änderungen für Speicherobjekte committen müssen.

</dd> <dt>

<span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream::Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)
</dt> <dd>

Diese Implementierung unterstützt keine transaktiven Datenströme, sodass ein Aufruf dieser Methode keine Auswirkungen hat.

</dd> <dt>

<span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)
</dt> <dd>

Bereichssperren werden von dieser Implementierung nicht unterstützt, sodass ein Aufruf dieser Methode keine Auswirkungen hat.

</dd> <dt>

<span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream::UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)
</dt> <dd>

Entfernt die Zugriffseinschränkung für einen Bereich von Bytes, der zuvor mit [**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)eingeschränkt wurde.

</dd> <dt>

<span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)
</dt> <dd>

Ruft die [**STATSTG-Struktur**](/windows/win32/api/objidl/ns-objidl-statstg) für diesen Stream ab.

</dd> <dt>

<span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)
</dt> <dd>

Erstellt ein neues Datenstromobjekt mit einem eigenen Suchzeiger, der auf die gleichen Bytes wie der Originaldatenstrom verweist.

</dd> </dl>

Ein [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) im einfachen Modus unterliegt den folgenden Einschränkungen.

-   Ein Stream ist ein einfacher Modus, wenn er in einem Speicher im einfachen Modus erstellt oder geöffnet wurde. Ein Speicher ist ein einfacher Modus, wenn er mit dem STGM SIMPLE-Flag erstellt oder geöffnet wird, \_ das im *grfMode-Parameter* festgelegt ist.
-   Die [**Methoden Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) und [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) werden nicht unterstützt.
-   Die [**Stat-Methode**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) wird unterstützt, aber der STATFLAG \_ NONAME-Wert muss angegeben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Istream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**Istorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 