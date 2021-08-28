---
title: IStorage-Compound-Dateiimplementierungen
description: Mit der Verbunddateiimplementierung von IStorage können Sie Unterspeicher und Datenströme in einem Speicherobjekt erstellen und verwalten, das sich in einem Verbunddateiobjekt befindet.
ms.assetid: 2a2253f6-d3d3-403e-a9ba-53a541c7a31e
keywords:
- IStorage Strctd Stg, Verbunddateiimplementierungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab243189d5a8cfb3e053c66bcd752d05bb65ab965657778a3bc3250c30ef8e75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992412"
---
# <a name="istorage-compound-file-implementation"></a>IStorage-Compound-Dateiimplementierungen

Mit der Verbunddateiimplementierung von [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) können Sie Unterspeicher und Datenströme in einem Speicherobjekt erstellen und verwalten, das sich in einem Verbunddateiobjekt befindet. Um ein Verbunddateiobjekt zu erstellen und einen **IStorage-Zeiger** abzurufen, rufen Sie die API-Funktion [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)auf. Um ein vorhandenes Verbunddateiobjekt zu öffnen und seinen **IStorage-Stammzeiger** abzurufen, rufen [**Sie StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)auf.

Anwendungen, die Verbundspeicher verwenden, sollten in HKEY \_ CLASSES \_ ROOT \\ SystemFileAssociations registriert werden und ihre eigenen Eigenschaftenhandler bereitstellen. Weitere Informationen finden Sie im Abschnitt "Registrieren von Verben und anderen Dateizuordnungsinformationen" der [Anwendungsregistrierung.](/windows/desktop/shell/app-registration)

## <a name="when-to-use"></a>Verwendungs wann

Die meisten Anwendungen verwenden diese Implementierung, um Speicher und Streams zu erstellen und zu verwalten.

## <a name="methods"></a>Methoden

<dl> <dt>

<span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)
</dt> <dd>

Erstellt und öffnet ein Streamobjekt mit dem angegebenen Namen, der in diesem Speicherobjekt enthalten ist. Der Name darf 31 Zeichen nicht überschreiten (ohne das Zeichenfolgenabschlusszeichen). Die Zeichen 000 bis 01f, welche als erste Zeichen des Namens des Datenstroms/Speichers dienen, sind durch die OLE für die Benutzung reserviert. Dies ist eine Verbunddateieinschränkung, keine strukturierte Speichereinschränkung. Die von COM bereitgestellte Verbunddateiimplementierungen der [**IStorage::CreateStream-Methode**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) unterstützen nicht die folgenden Verhaltensweisen:

-   Das STGM \_ DELETEONRELEASE-Flag wird nicht unterstützt.
-   Der Transaktionsmodus (STGM \_ TRANSACTED) wird für Streamobjekte nicht unterstützt.
-   Das mehrfache Öffnen desselben Streams aus dem gleichen Speicher wird nicht unterstützt. Das Freigabemodusflag STGM \_ SHARE EXCLUSIVE muss im \_ *grfMode-Parameter* angegeben werden.

</dd> <dt>

<span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)
</dt> <dd>

Öffnet ein vorhandenes Streamobjekt innerhalb dieses Speicherobjekts mithilfe der im *grfMode-Parameter* angegebenen Zugriffsmodi. Die Zeichen 000 bis 01f, welche als erste Zeichen des Namens des Datenstroms/Speichers dienen, sind durch die OLE für die Benutzung reserviert. Dies ist eine Verbunddateieinschränkung, keine strukturierte Speichereinschränkung. Die von COM bereitgestellte Verbunddateiimplementierungen der [**IStorage::OpenStream-Methode**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) unterstützen das folgende Verhalten nicht:

-   Das STGM \_ DELETEONRELEASE-Flag.
-   Transacted Mode (STGM \_ TRANSACTED) für Streamobjekte.
-   Öffnen Sie denselben Stream mehr als einmal aus dem gleichen Speicher. Das STGM \_ SHARE \_ EXCLUSIVE-Flag muss angegeben werden.

</dd> <dt>

<span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)
</dt> <dd>

Erstellt und öffnet ein neues Speicherobjekt mit dem angegebenen Namen im angegebenen Zugriffsmodus. Der Name darf 31 Zeichen nicht überschreiten (ohne das Zeichenfolgenabschlusszeichen). Die Zeichen 000 bis 01f, welche als erste Zeichen des Namens des Datenstroms/Speichers dienen, sind durch die OLE für die Benutzung reserviert. Dies ist eine Verbunddateieinschränkung, keine strukturierte Speichereinschränkung. Die von COM bereitgestellte Verbunddateiimplementierungen der [**IStorage::CreateStorage-Methode**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) unterstützen das folgende Verhalten nicht:

-   Das STGM \_ PRIORITY-Flag für Nicht-Root-Speicher.
-   Dasselbe Speicherobjekt wird aus demselben übergeordneten Speicher mehr als einmal geöffnet. Das STGM \_ SHARE \_ EXCLUSIVE-Flag muss angegeben werden.
-   Das STGM \_ DELETEONRELEASE-Flag. Wenn dieses Flag angegeben ist, gibt die Funktion STG \_ E \_ INVALIDFLAG zurück.

</dd> <dt>

<span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)
</dt> <dd>

Öffnet ein vorhandenes Speicherobjekt mit dem angegebenen Namen im angegebenen Zugriffsmodus. Die Zeichen 000 bis 01f, welche als erste Zeichen des Namens des Datenstroms/Speichers dienen, sind durch die OLE für die Benutzung reserviert. Dies ist eine Verbunddateieinschränkung, keine strukturierte Speichereinschränkung. Die von COM bereitgestellte Verbunddateiimplementierungen der [**IStorage::OpenStorage-Methode**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) unterstützen das folgende Verhalten nicht:

-   Das STGM \_ PRIORITY-Flag für Nicht-Root-Speicher.
-   Dasselbe Speicherobjekt wird aus demselben übergeordneten Speicher mehr als einmal geöffnet. Das STGM \_ SHARE \_ EXCLUSIVE-Flag muss angegeben werden.
-   Das STGM \_ DELETEONRELEASE-Flag. Wenn dieses Flag angegeben ist, gibt die Funktion STG \_ E \_ INVALIDFUNCTION zurück.

</dd> <dt>

<span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)
</dt> <dd>

Kopiert nur die Unterspeicher und Streams dieses offenen Speicherobjekts in ein anderes Speicherobjekt. Der *rgiidExclude-Parameter* kann auf IID IStream festgelegt \_ werden, um nur Untertoragen zu kopieren, oder auf IID \_ IStorage, um nur Streams zu kopieren.

</dd> <dt>

<span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage::MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)
</dt> <dd>

Kopiert oder verschiebt einen Unterspeicher oder Stream aus diesem Speicherobjekt in ein anderes Speicherobjekt.

</dd> <dt>

<span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)
</dt> <dd>

Stellt sicher, dass alle Änderungen, die an einem im Transaktionsmodus geöffneten Speicherobjekt vorgenommen werden, im übergeordneten Speicher widergespiegelt werden. gibt für einen Stammspeicher die Änderungen am tatsächlichen Gerät wieder. z. B. eine Datei auf dem Datenträger. Für ein im direkten Modus geöffnetes Stammspeicherobjekt hat diese Methode keine Auswirkungen, außer alle Speicherpuffer auf den Datenträger zu leeren. Für Nicht-Root-Speicherobjekte im direkten Modus hat diese Methode keine Auswirkungen.

Die von COM bereitgestellte Verbunddateienimplementierung verwendet einen zweistufigen Commitprozess, es sei denn, STGC \_ OVERWRITE wird im *grfCommitFlags-Parameter* angegeben. Dieser zweistufige Prozess stellt die Stabilität der Daten sicher, falls der Commitvorgang fehlschlägt. Zunächst werden alle neuen Daten in den nicht verwendeten Speicherplatz in der zugrunde liegenden Datei geschrieben. Bei Bedarf wird der Datei neuer Speicherplatz zugeordnet. Nach Abschluss dieses Schritts wird eine Tabelle in der Datei mithilfe eines Schreibvorgangs für einen einzelnen Sektor aktualisiert, um anzugeben, dass die neuen Daten anstelle der alten datenverwendet werden sollen. Die alten Daten werden zum freien Speicherplatz, der beim nächsten Commitvorgang verwendet werden soll. Daher sind die alten Daten verfügbar und können wiederhergestellt werden, wenn beim Committen von Änderungen ein Fehler auftritt. Wenn STGC \_ OVERWRITE angegeben wird, wird ein Einphasencommitvorgang verwendet. Weitere Informationen zu Flags im Transaktionsmodus finden Sie unter [**STGC-Enumeration.**](/windows/win32/api/wtypes/ne-wtypes-stgc)

</dd> <dt>

<span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage::Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)
</dt> <dd>

Verwirft alle Änderungen, die seit dem letzten Commitvorgang am Speicherobjekt vorgenommen wurden.

</dd> <dt>

<span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage::EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dd>

Erstellt einen Zeiger auf ein Enumeratorobjekt und ruft diesen ab, mit dem die in diesem Speicherobjekt enthaltenen Speicher- und Streamobjekte aufzählt werden können. Die von COM bereitgestellte Verbunddateiimplementation erstellt eine Momentaufnahme dieser Informationen. Daher werden Änderungen an streams und storages erst dann im Enumerator widergespiegelt, wenn ein neuer Enumerator abgerufen wird.

</dd> <dt>

<span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage::D estmillElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)
</dt> <dd>

Entfernt das angegebene Element (substorage oder stream) aus diesem Speicherobjekt.

</dd> <dt>

<span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage::RenameElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)
</dt> <dd>

Benennt den angegebenen Unterspeicher oder Stream in diesem Speicherobjekt um. Die Zeichen 000 bis 01f, welche als erste Zeichen des Namens des Datenstroms/Speichers dienen, sind durch die OLE für die Benutzung reserviert. Dies ist eine Verbunddateieinschränkung, keine strukturierte Speichereinschränkung.

</dd> <dt>

<span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dd>

Legt die Änderungs-, Zugriffs- und Erstellungszeiten des angegebenen Speicherelements fest. Die von COM bereitgestellte Verbunddateiimplementierungen verwaltet Änderungs- und Änderungszeiten für interne Speicherobjekte. Stammspeicherobjekte unterstützen alles, was vom zugrunde liegenden Dateisystem (oder von [**ILockBytes)**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)unterstützt wird. Die Verbunddateiimplementierungen behalten keine Zeitstempel für interne Streams bei. Nicht unterstützte Zeitstempel werden als 0 (null) gemeldet, wodurch der Aufrufer auf Unterstützung testen kann.

</dd> <dt>

<span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage::SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)
</dt> <dd>

Weist diesem Speicherobjekt die angegebene CLSID zu.

</dd> <dt>

<span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage::SetStateBits**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)
</dt> <dd>

Speichert bis zu 32 Bit an Zustandsinformationen in diesem Speicherobjekt. Der von dieser Methode festgelegte Zustand ist nur für die externe Verwendung vorgesehen. Die von COM bereitgestellte Verbunddateiimplementierungen führen keine Aktionen basierend auf dem Zustand aus.

</dd> <dt>

<span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)
</dt> <dd>

Ruft die [**STATSTG-Struktur**](/windows/win32/api/objidl/ns-objidl-statstg) für dieses offene Speicherobjekt ab.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn das Speicherobjekt im einfachen Modus geöffnet wird, ist die Verwendung der oben genannten Methoden eingeschränkt. Ein Speicher befindet sich im einfachen Modus, wenn er mit dem STGM SIMPLE-Element geöffnet wird, \_ das im *grfMode-Parameter* der [**StgCreateStorageEx-**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) oder [**StgOpenStorageEx-Funktion**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) angegeben ist. Weitere Informationen zu Speicher im einfachen Modus finden Sie unter [**STGM-Konstanten.**](stgm-constants.md) Wenn das Speicherobjekt im einfachen Modus von der **StgCreateStorageEx-Funktion** erhalten wurde, kann die [**CreateStream-Methode**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) aufgerufen werden, die [**OpenStream-Methode jedoch**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) nicht. Wenn das Speicherobjekt im einfachen Modus von der **StgOpenStorageEx-Funktion** erhalten wurde, kann die **OpenStream-Methode** aufgerufen werden, die **CreateStream-Methode jedoch** nicht.

Wenn ein Speicherobjekt im einfachen Modus zum Erstellen eines Streams verwendet wird, beträgt die Mindestgröße dieses Streams in der Regel 4.096 Bytes. Wenn weniger Daten in den Stream geschrieben werden, wird die Größe auf 4096 Bytes aufgerundet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grenzwerte für die Implementierung von Verbunddatei](structured-storage-interfaces.md)
</dt> <dt>

[**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)
</dt> <dt>

[**Ilockbytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**Istorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**Istream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> </dl>

 

 