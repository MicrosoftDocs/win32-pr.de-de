---
title: Implementierung der IStorage-Compound Datei
description: Die Implementierung der Verbund Datei von IStorage ermöglicht Ihnen das Erstellen und Verwalten von substorages und Streams innerhalb eines Speicher Objekts, das sich in einem Verbund Datei Objekt befindet.
ms.assetid: 2a2253f6-d3d3-403e-a9ba-53a541c7a31e
keywords:
- IStorage-STG, Implementierung von Verbund Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bf37b24a7c68bbe357d99f94e666bfcb613c472
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338071"
---
# <a name="istorage-compound-file-implementation"></a>Implementierung der IStorage-Compound Datei

Die Implementierung der Verbund Datei von [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ermöglicht Ihnen das Erstellen und Verwalten von substorages und Streams innerhalb eines Speicher Objekts, das sich in einem Verbund Datei Objekt befindet. Um ein Verbund Datei Objekt zu erstellen und einen **IStorage** -Zeiger abzurufen, rufen Sie die API-Funktion [**stgkreatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)auf. Um ein vorhandenes Verbund Datei Objekt zu öffnen und dessen Stamm- **IStorage** -Zeiger abzurufen, nennen Sie [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).

Anwendungen, die Verbund Speicher verwenden, müssen in den HKEY \_ -Klassen " \_ root \\ systemfileassociations" registriert sein und ihre eigenen Eigenschaften Handler bereitstellen. Weitere Informationen finden Sie im Abschnitt "Registrieren von Verben und anderen Datei Zuordnungs Informationen" unter [Anwendungs Registrierung](/windows/desktop/shell/app-registration).

## <a name="when-to-use"></a>Verwendungs Zeitpunkt

Die meisten Anwendungen verwenden diese Implementierung, um Speicher und Streams zu erstellen und zu verwalten.

## <a name="methods"></a>Methoden

<dl> <dt>

<span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage:: kreatestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)
</dt> <dd>

Erstellt und öffnet ein Stream-Objekt mit dem angegebenen Namen, das in diesem Speicher Objekt enthalten ist. Der Name darf nicht länger als 31 Zeichen sein (ohne das Zeichen folgen Abschluss Zeichen). Die Zeichen 000 bis 01f, welche als erste Zeichen des Namens des Datenstroms/Speichers dienen, sind durch die OLE für die Benutzung reserviert. Dies ist eine Verbunddateieinschränkung, keine strukturierte Speichereinschränkung. Die von com bereitgestellte Verbund Datei Implementierung der [**IStorage:: foratestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) -Methode unterstützt nicht die folgenden Verhaltensweisen:

-   Das STGM \_ deleteonrelease-Flag wird nicht unterstützt.
-   Der transaktive Modus (STGM \_ transaktive) wird für Streamobjekte nicht unterstützt.
-   Das gleichzeitige Öffnen desselben Streams aus demselben Speicher wird nicht unterstützt. Das STGM \_ \_ -Freigabe exklusive Freigabe Modus-Flag muss im *GRF Mode* -Parameter angegeben werden.

</dd> <dt>

<span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)
</dt> <dd>

Öffnet ein vorhandenes Stream-Objekt in diesem Speicher Objekt unter Verwendung der Zugriffs Modi, die im *GRF Mode* -Parameter angegeben sind. Die Zeichen 000 bis 01f, welche als erste Zeichen des Namens des Datenstroms/Speichers dienen, sind durch die OLE für die Benutzung reserviert. Dies ist eine Verbunddateieinschränkung, keine strukturierte Speichereinschränkung. Die von com bereitgestellte Verbund Datei Implementierung der [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) -Methode unterstützt das folgende Verhalten nicht:

-   Das STGM \_ deleteonrelease-Flag.
-   Transaktiver Modus (STGM \_ transaktiv) für Streamobjekte.
-   Der gleiche Stream wird mehr als einmal aus demselben Speicher geöffnet. Das Flag "STGM- \_ Freigabe \_ exklusiv" muss angegeben werden.

</dd> <dt>

<span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage:: foratestorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)
</dt> <dd>

Erstellt und öffnet ein neues Speicher Objekt mit dem angegebenen Namen im angegebenen Zugriffsmodus. Der Name darf nicht länger als 31 Zeichen sein (ohne das Zeichen folgen Abschluss Zeichen). Die Zeichen 000 bis 01f, welche als erste Zeichen des Namens des Datenstroms/Speichers dienen, sind durch die OLE für die Benutzung reserviert. Dies ist eine Verbunddateieinschränkung, keine strukturierte Speichereinschränkung. Die von com bereitgestellte Verbund Datei Implementierung der [**IStorage:: foratestorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) -Methode unterstützt das folgende Verhalten nicht:

-   Das STGM- \_ Prioritäts Kennzeichen für nicht Stamm-Storages.
-   Das gleiche Speicher Objekt wird mehr als einmal aus demselben übergeordneten Speicher geöffnet. Das Flag "STGM- \_ Freigabe \_ exklusiv" muss angegeben werden.
-   Das STGM \_ deleteonrelease-Flag. Wenn dieses Flag angegeben wird, gibt die Funktion STG \_ E \_ invalidflag zurück.

</dd> <dt>

<span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)
</dt> <dd>

Öffnet ein vorhandenes Speicher Objekt mit dem angegebenen Namen im angegebenen Zugriffsmodus. Die Zeichen 000 bis 01f, welche als erste Zeichen des Namens des Datenstroms/Speichers dienen, sind durch die OLE für die Benutzung reserviert. Dies ist eine Verbunddateieinschränkung, keine strukturierte Speichereinschränkung. Die von com bereitgestellte Verbund Datei Implementierung der [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) -Methode unterstützt das folgende Verhalten nicht:

-   Das STGM- \_ Prioritäts Kennzeichen für nicht Stamm-Storages.
-   Das gleiche Speicher Objekt wird mehr als einmal aus demselben übergeordneten Speicher geöffnet. Das Flag "STGM- \_ Freigabe \_ exklusiv" muss angegeben werden.
-   Das STGM \_ deleteonrelease-Flag. Wenn dieses Flag angegeben wird, gibt die Funktion "STG \_ E \_ invalidfunction" zurück.

</dd> <dt>

<span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)
</dt> <dd>

Kopiert nur die substorages und Streams dieses geöffneten Speicher Objekts in ein anderes Speicher Objekt. Der *rgiidexclude* -Parameter kann auf IID IStream festgelegt werden, \_ um nur substorages zu kopieren, oder auf IID \_ IStorage, um nur Streams zu kopieren.

</dd> <dt>

<span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage:: muveelementto**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)
</dt> <dd>

Kopiert oder verschiebt einen unter Speicher oder Stream von diesem Speicher Objekt in ein anderes Speicher Objekt.

</dd> <dt>

<span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)
</dt> <dd>

Stellt sicher, dass alle Änderungen, die an einem im Transaktionsmodus geöffneten Speicher Objekt vorgenommen werden, im übergeordneten Speicher widergespiegelt werden. bei einem Stamm Speicher werden die Änderungen im eigentlichen Gerät widergespiegelt. beispielsweise eine Datei auf dem Datenträger. Für ein im direkten Modus geöffnetes Stamm Speicher Objekt hat diese Methode keine Auswirkung, außer wenn alle Speicherpuffer auf den Datenträger geleert werden. Bei nicht stammenden Speicher Objekten im direkten Modus hat diese Methode keine Auswirkungen.

Die von com bereitgestellte Verbund Datei Implementierung verwendet einen Zweiphasencommit-Prozess, es sei denn, das Überschreiben von "stgc" \_ ist im *GRF commitflags* -Parameter angegeben Dieser zweistufige Prozess stellt die Stabilität von Daten sicher, falls der Commitvorgang fehlschlägt. Zuerst werden alle neuen Daten in den nicht verwendeten Speicherplatz in der zugrunde liegenden Datei geschrieben. Bei Bedarf wird der Datei neuer Speicherplatz zugeordnet. Nachdem dieser Schritt abgeschlossen wurde, wird eine Tabelle in der Datei mithilfe eines Schreibvorgangs mit einem einzelnen Sektor aktualisiert, um anzugeben, dass die neuen Daten anstelle der alten verwendet werden sollen. Die alten Daten werden zu freiem Speicherplatz, der beim nächsten Commitvorgang verwendet werden soll. Folglich sind die alten Daten verfügbar und können wieder hergestellt werden, wenn ein Fehler beim Ausführen eines Commits für Änderungen auftritt. Wenn stgc-über \_ Schreiben angegeben ist, wird ein einzelner Phasen-Commit-Vorgang verwendet. Weitere Informationen über transaktive modusflags finden Sie unter [**stgc**](/windows/win32/api/wtypes/ne-wtypes-stgc) -Enumeration.

</dd> <dt>

<span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)
</dt> <dd>

Verwirft alle Änderungen, die seit dem letzten Commitvorgang an dem Speicher Objekt vorgenommen wurden.

</dd> <dt>

<span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage:: enumelements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dd>

Erstellt und Ruft einen Zeiger auf ein Enumeratorobjekt ab, das verwendet werden kann, um die Speicher-und Streamobjekte aufzulisten, die in diesem Speicher Objekt enthalten sind. Die von com bereitgestellte Verbund Datei Implementierung erstellt eine Momentaufnahme dieser Informationen. Folglich werden Änderungen an Streams und Speicher nicht im Enumerator widergespiegelt, bis ein neuer Enumerator abgerufen wird.

</dd> <dt>

<span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage::D estroyelement**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)
</dt> <dd>

Entfernt das angegebene Element (unter Speicher oder Stream) aus diesem Speicher Objekt.

</dd> <dt>

<span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage:: renameelement**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)
</dt> <dd>

Benennt den angegebenen unter Speicher oder Stream in diesem Speicher Objekt um. Die Zeichen 000 bis 01f, welche als erste Zeichen des Namens des Datenstroms/Speichers dienen, sind durch die OLE für die Benutzung reserviert. Dies ist eine Verbunddateieinschränkung, keine strukturierte Speichereinschränkung.

</dd> <dt>

<span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage::/telementtimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dd>

Legt die Änderungs-, Zugriffs-und Erstellungs Zeiten für das angegebene Speicher Element fest. Die von com bereitgestellte Verbund Datei Implementierung behält Änderungs-und Änderungs Zeiten für interne Speicher Objekte bei. Stamm Speicher Objekte unterstützen alle Vorgänge, die vom zugrunde liegenden Dateisystem (oder von [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)) unterstützt werden. Die Implementierung der Verbund Datei behält keine Zeitstempel für interne Streams bei. Nicht unterstützte Zeitstempel werden als 0 (null) gemeldet, sodass der Aufrufer die Unterstützung testen kann.

</dd> <dt>

<span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage:: setClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)
</dt> <dd>

Weist diesem Speicher Objekt die angegebene CLSID zu.

</dd> <dt>

<span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage:: SetStateBits**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)
</dt> <dd>

Speichert bis zu 32 Bits Zustandsinformationen in diesem Speicher Objekt. Der von dieser Methode festgelegte Status ist nur für die externe Verwendung vorgesehen. Die von com bereitgestellte Verbund Datei Implementierung führt keine Aktionen aus, die auf dem Status basieren.

</dd> <dt>

<span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)
</dt> <dd>

Ruft die [**Statuslisten**](/windows/win32/api/objidl/ns-objidl-statstg) Struktur für dieses geöffnete Speicher Objekt ab.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn das Speicher Objekt im einfachen Modus geöffnet wird, ist die Verwendung der oben genannten Methoden eingeschränkt. Ein Speicher befindet sich im einfachen Modus, wenn er mit dem einfachen STGM-Element geöffnet wird, das \_ im *GRF Mode* -Parameter der [**stgforatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) -oder [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) -Funktion angegeben ist. Weitere Informationen zu Storages im einfachen Modus finden Sie unter [**STGM-Konstanten**](stgm-constants.md). Wenn das Speicher Objekt im einfachen Modus von der **stganatestorageex** -Funktion abgerufen wurde, kann die Methode [**"Methode"**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) aufgerufen werden, aber die [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) -Methode kann nicht ausgeführt werden. Wenn das Speicher Objekt im einfachen Modus von der **stgopenstorageex** -Funktion abgerufen wurde, kann die **OpenStream** -Methode aufgerufen werden **, die Methode "Methode"** kann jedoch nicht ausgeführt werden.

Wenn ein Speicher Objekt im einfachen Modus zum Erstellen eines Streams verwendet wird, beträgt die Mindestgröße dieses Streams in der Regel 4096 Bytes. Wenn weniger Daten in den Stream geschrieben werden, wird die Größe auf 4096 Bytes aufgerundet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Implementierungs Limits für Verbund Dateien](structured-storage-interfaces.md)
</dt> <dt>

[**Ifilllockbytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)
</dt> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**Irootstorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**Stgkreatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**Stgkreatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**Stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> </dl>

 

 