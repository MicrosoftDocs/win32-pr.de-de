---
title: IPropertySetStorage-NTFS-Datei System Implementierung
description: Die NTFS-Version 5,0 bietet eine Implementierung von IPropertySetStorage für Dateien auf einem NTFS-Volume, wenn die Dateien selbst keine Verbund Dateien sind.
ms.assetid: cd7290bb-bb4e-4dea-9bf6-2e1fdd0ebae8
keywords:
- IPropertySetStorage-Schnittstellen-STG, Implementierungen, NTFS-Dateisystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0d647b9cb804376a9efeb687b1524585ee938d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339491"
---
# <a name="ipropertysetstorage-ntfs-file-system-implementation"></a>IPropertySetStorage-NTFS-Datei System Implementierung

Die NTFS-Version 5,0 bietet eine Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) für Dateien auf einem NTFS-Volume, wenn die Dateien selbst keine Verbund Dateien sind. Die NTFS-Implementierung entspricht der [Implementierung der Verbund Datei](ipropertysetstorage-compound-file-implementation.md). Weitere Informationen zu Ausnahmen finden Sie unter "Hinweise".

**So erhalten Sie einen Zeiger auf die NTFS-Implementierung von IPropertySetStorage**

1.  Rufen Sie [**stgforatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) auf, und geben Sie die **stgfmt- \_ Datei** im *grfFlags* -Parameter an, um eine neue Datei zu erstellen.
2.  Aufrufen [**von stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) und angeben der stgfmt-oder **stgfmt \_** -Enumerationswerte im *grfFlags* -Parameter, um eine vorhandene Datei zu öffnen. **\_**

Allerdings können Sie die NTFS-Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) nicht für eine Verbund Datei abrufen. Beim Öffnen einer Verbund Datei mit [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)führt die Angabe des **stgfmt- \_ datumenumerationswerts** zu einem Fehler.

Außerdem können einfache Eigenschaften Sätze nicht transaktiv sein. Das heißt, Sie können **STGM- \_ Transaktionen** nicht im *grfMode* -Parameter der [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) -Methode und [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) -Methode angeben, es sei denn, Sie geben auch **propsetflag \_ nonsimple** im *grfFlags* -Parameter an. Das Eigenschaften Satz-Speicher Objekt selbst unterstützt keine Transaktionsverarbeitung.

## <a name="when-to-use"></a>Verwendungs Zeitpunkt

Rufen Sie die [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Methoden auf, um Eigenschaften Sätze im aktuellen NTFS-Eigenschaften Satz Speicher zu erstellen, zu öffnen oder zu löschen. Es gibt auch eine Methode, [**IPropertySetStorage:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), die einen Zeiger auf einen Enumerator bereitstellt, der zum Auflisten der Eigenschaften Sätze im Speicher verwendet werden kann.

## <a name="compatibility"></a>Kompatibilität

Die NTFS-Implementierungen von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) und [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) sind ab Windows 2000 verfügbar. Frühere Versionen können nicht auf diese Eigenschaften Sätze zugreifen.

Die NTFS-Implementierung speichert Eigenschaften Sätze in alternativen Streams einer NTFS-Datei. Die alternativen Streams müssen kopiert werden, wenn die Hauptdatei kopiert wird.

> [!Caution]  
> Nicht alle Dateisysteme unterstützen solche Streams. Wenn eine NTFS-Datei mit Eigenschafts Sätzen in ein FAT-Volume kopiert wird, werden nur die Daten in der Datei kopiert. der Eigenschaften Satz geht verloren. In diesem Fall gibt die [**CopyFile**](/windows/desktop/api/winbase/nf-winbase-copyfile) -Funktion keinen Fehler zurück.

 

> [!Caution]  
> Wenn es sich bei dem Computer, der die Dateikopie ausführt, nicht um einen Computer handelt, der unter Windows 2000 oder höher ausgeführt wird, können die Eigenschaften Sätze verloren gehen Wenn beispielsweise ein Computer, auf dem das Betriebssystem Windows 95 ausgeführt wird, eine NTFS-Datei kopiert, geht der Eigenschaften Satz verloren, auch wenn sich die Zieldatei ebenfalls auf einem NTFS-Volume befindet.

 

## <a name="methods"></a>Methoden

Die NTFS-Dateisystem Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) unterstützt die folgenden Methoden.

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

Erstellt eine neue Eigenschaft, die im aktuellen NTFS-Dateispeicher festgelegt ist, und stellt bei der Rückgabe einen Schnittstellen Zeiger auf die Implementierung der NTFS-Datei [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) bereit. Der im *GRF Mode* -Parameter angegebene Freigabe Modus muss " **STGM- \_ Freigabe \_ exklusiv**" lauten.

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

Öffnet eine vorhandene Eigenschaft, die im aktuellen Eigenschaften Speicher festgelegt ist. Bei der Rückgabe stellt Sie einen Schnittstellen Zeiger auf die NTFS-Datei Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)bereit. Der im *GRF Mode* -Parameter angegebene Freigabe Modus muss " **STGM- \_ Freigabe \_ exklusiv**" lauten.

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D Elete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

Löscht eine Eigenschaft, die im aktuellen Eigenschaften Speicher festgelegt ist.

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage:: Aufzählung**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

Erstellt ein-Objekt, das zum Aufzählen von [**Status-setstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) -Strukturen verwendet wird. Jede **Status-setstg** -Struktur stellt Daten zu einem einzelnen Eigenschaften Satz bereit.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die NTFS-Implementierungen von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) und [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) speichern Eigenschaften Sätze in einer Datei, ohne den Inhalt dieser Datei zu beeinträchtigen. Wenn Sie z. b. in einer HTML-Datei mit dem Namen Default.htm einen Eigenschaften Satz erstellen, wird diese Datei weiterhin ordnungsgemäß in einem Webbrowser angezeigt. Das heißt, dass Änderungen an einer Datei, die diese beiden Schnittstellen verwendet, nicht erkennbar sind, wenn Sie [**mit der Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf eine Datei zugreifen.

Die NTFS-Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) bietet eine sichere Implementierung, wenn Sie zum Schreiben von Eigenschaften Sätzen in eine Datei auf einem Volume der NTFS-Version 5,0 verwendet wird. Solche Eigenschaften Sätze können von der Implementierung auch im Falle eines Systemfehlers nicht beschädigt werden. Wenn beispielsweise die Leistung eines Systems während eines Aufrufens von [**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) fehlschlägt, während der Eigenschaften Satz auf den Datenträger geleert wird, bleibt der Eigenschaften Satz nie in einem Zwischenzustand. Die vorherige Version des Eigenschaften Satzes bleibt bestehen, oder alle Updates werden gespeichert.

Die NTFS-Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) unterscheidet sich wie folgt von der Implementierung der Verbund Datei:

-   Eine von der [**ienumstatus propsetstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) -Schnittstelle erhaltene " [**Status-setstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) "-Struktur enthält einen **CLSID** -Member, dessen Wert immer NULL (**CLSID \_ null**) ist. Bei der Implementierung der Verbund Datei wird der richtige **CLSID** -Member für nicht-einfach zurückgegeben (siehe [Speicher-und Streamobjekte für Eigenschaften](storage-vs--stream-for-a-property-set.md)Sätze).
-   Wenn Sie eine NTFS-Implementierung des [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstellen Zeigers mithilfe der [**stgforatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) -oder [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) -Funktion abrufen, muss der *GRF Mode* -Parameter denselben Regeln wie für die Implementierung der Verbund Datei entsprechen.

    Außerdem dürfen die folgenden Flags nicht verwendet werden:

    **STGM \_ Einfach**, **STGM \_ transaktiv**, **STGM \_ Convert**, **STGM \_ Priority** und **STGM \_ deleteonrelease**.

-   Wenn eine NTFS- [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle von den Funktionen " [**stganatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) " oder " [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) " abgerufen wird, gelten die Freigabe Modi hauptsächlich für andere Instanzen dieser Schnittstelle und nicht für Instanzen des Öffnens der Datei. Wenn z. b. eine NTFS- **IPropertySetStorage** -Schnittstelle durch Aufrufen der Funktion " **stgopenstorageex** " geöffnet wird und der *grfMode* -Parameter auf " **STGM \_ infowrite \| STGM- \_ Freigabe \_ exklusiv**" festgelegt ist, kann die Datei mit der [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) -Funktion geöffnet werden.

    Solche gleichzeitigen Instanzen, die diese Schnittstelle öffnen, unterliegen den folgenden Einschränkungen: der Parameter " *dwsharemode* " in [**der Funktion "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Funktion" muss das **\_ \_ leseflag für die Dateifreigabe** angeben, und der *dwaccess* -Parameter darf das Flag " **Delete** " nicht angeben. Außerdem dürfen die Funktionen " [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) " und " [**muvefile**](/windows/desktop/api/winbase/nf-winbase-movefile) " nicht für eine Datei aufgerufen werden, für die diese Eigenschaften Satz Schnittstellen geöffnet sind, da diese Funktionen den **Lösch** Zugriff auf die Datei erfordern.

-   Wenn eine NTFS- [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Methode als schreibgeschützt geöffnet wird und die Datei zurzeit keine Eigenschaften Sätze hat, wird die Datei vom zurückgegebenen Objekt nicht tatsächlich geöffnet. Folglich sind andere Öffnungen dieser Datei erfolgreich, auch wenn der Freigabe Modus des ursprünglichen Öffnungs Vorgangs diese andernfalls ablehnen würde.

    Beispiel Wenn eine NTFS- [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Klasse im Modus **STGM-Lese-und-Freigabe- \_ \| \_ Freigabe \_ exklusiv** geöffnet ist, und die Datei keine Eigenschaften Sätze hat, ist es möglich, die Datei " **STGM-Lese \_ schreiben \| STGM- \_ Freigabe \_ exklusiv**" gleichzeitig zu öffnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPropertyStorage-NTFS-Datei System Implementierung](ipropertystorage-ntfs-file-system-implementation.md)
</dt> <dt>

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage:: enumelements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[**Propsetflag-Konstanten**](propsetflag-constants.md)
</dt> <dt>

[**Status-setstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> </dl>

 

 