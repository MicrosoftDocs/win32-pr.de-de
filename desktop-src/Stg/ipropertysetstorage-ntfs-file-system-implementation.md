---
title: IPropertySetStorage-NTFS-Dateisystemimplementierung
description: NTFS Version 5.0 bietet eine Implementierung von IPropertySetStorage für Dateien auf einem NTFS-Volume, wenn die Dateien selbst keine Verbunddateien sind.
ms.assetid: cd7290bb-bb4e-4dea-9bf6-2e1fdd0ebae8
keywords:
- IPropertySetStorage Strctd Stg , Implementierungen, NTFS-Dateisystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0794e2905cd9e8bd06804decb756b3f1f639c75e837b2d5f3181bb73939717f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683040"
---
# <a name="ipropertysetstorage-ntfs-file-system-implementation"></a>IPropertySetStorage-NTFS-Dateisystemimplementierung

NTFS Version 5.0 bietet eine Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) für Dateien auf einem NTFS-Volume, wenn die Dateien selbst keine Verbunddateien sind. Die NTFS-Implementierung entspricht der [Verbunddateiimplementierungen](ipropertysetstorage-compound-file-implementation.md). Weitere Informationen zu Ausnahmen finden Sie unter Hinweise.

**So erhalten Sie einen Zeiger auf die NTFS-Implementierung von IPropertySetStorage**

1.  Rufen Sie [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) auf, und geben Sie **STGFMT \_ FILE** im *grfFlags-Parameter* an, um eine neue Datei zu erstellen.
2.  Rufen Sie [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) auf, und geben Sie entweder den **STGFMT \_ FILE-** oder **STGFMT \_ ANY-Enumerationswert** im *grfFlags-Parameter* an, um eine vorhandene Datei zu öffnen.

Sie können jedoch nicht die NTFS-Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) für eine Verbunddatei abrufen. Beim Öffnen einer Verbunddatei mit [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)führt die Angabe des **STGFMT \_ FILE-Enumerationswerts** zu einem Fehler.

Darüber hinaus können einfache Eigenschaftensätze nicht transaktiviert werden. Das heißt, Sie können **STGM \_ TRANSACTED** nicht im *grfmode-Parameter* der [**Create-**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) und [**Open-Methoden**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) angeben, es sei denn, Sie geben auch **PROPSETFLAG \_ NONSIMPLE** im *grfFlags-Parameter* an. Das Eigenschaftensatzspeicherobjekt selbst unterstützt keine Transaktionsverarbeitung.

## <a name="when-to-use"></a>Verwendungs wann

Rufen Sie die [**IPropertySetStorage-Methoden**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) auf, um Eigenschaftensätze im aktuellen NTFS-Eigenschaftensatzspeicher zu erstellen, zu öffnen oder zu löschen. Es gibt auch die Methode [**IPropertySetStorage::Enum,**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)die einen Zeiger auf einen Enumerator angibt, der zum Aufzählen der Eigenschaftensätze im Speicher verwendet werden kann.

## <a name="compatibility"></a>Kompatibilität

Die NTFS-Implementierungen von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) und [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) sind ab Windows 2000 verfügbar. Frühere Versionen können nicht auf diese Eigenschaftensätze zugreifen.

Die NTFS-Implementierung speichert Eigenschaftensätze in alternativen Datenströmen einer NTFS-Datei. Die alternativen Streams müssen kopiert werden, wenn die Hauptdatei kopiert wird.

> [!Caution]  
> Nicht alle Dateisysteme unterstützen solche Streams. Wenn eine NTFS-Datei mit Eigenschaftensätzen auf ein FAT-Volume kopiert wird, werden nur die Daten in der Datei kopiert. Der Eigenschaftensatz geht verloren. Die [**CopyFile-Funktion**](/windows/desktop/api/winbase/nf-winbase-copyfile) gibt in diesem Fall keinen Fehler zurück.

 

> [!Caution]  
> Wenn der Computer, auf dem die Datei kopiert wird, kein Computer ist, auf dem Windows 2000 oder höher ausgeführt wird, gehen die Eigenschaftensätze möglicherweise verloren. Wenn beispielsweise ein Computer, auf dem Windows 95-Betriebssystem ausgeführt wird, eine NTFS-Datei kopiert, geht der Eigenschaftensatz verloren, auch wenn sich die Zieldatei auch auf einem NTFS-Volume befindet.

 

## <a name="methods"></a>Methoden

Die NTFS-Dateisystemimplementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) unterstützt die folgenden Methoden.

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

Erstellt einen neuen Eigenschaftensatz im aktuellen NTFS-Dateispeicher und stellt bei der Rückgabe einen Schnittstellenzeiger auf die IMPLEMENTIERUNG der NTFS-Datei [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) bereit. Der im *grfmode-Parameter* angegebene Freigabemodus muss **STGM \_ SHARE \_ EXCLUSIVE** sein.

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

Öffnet einen vorhandenen Eigenschaftensatz im aktuellen Eigenschaftenspeicher. Bei der Rückgabe wird ein Schnittstellenzeiger auf die NTFS-Dateiimplementierungen von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)bereitgestellt. Der im *grfmode-Parameter* angegebene Freigabemodus muss **STGM \_ SHARE \_ EXCLUSIVE** sein.

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D elete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

Löscht einen Im aktuellen Eigenschaftenspeicher festgelegten Eigenschaftensatz.

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

Erstellt ein Objekt, das zum Aufzählen von [**STATPROPSETSTG-Strukturen**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) verwendet wird. Jede **STATPROPSETSTG-Struktur** stellt Daten zu einem einzelnen Eigenschaftensatz bereit.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die NTFS-Implementierungen von [**IPropertySetStorage-**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) und [**IPropertyStorage-Speichereigenschaftssätzen**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) in einer Datei ohne Auswirkungen auf den Inhalt dieser Datei. Wenn Sie beispielsweise einen Eigenschaftensatz in einer HTML-Datei mit dem Namen Default.htm erstellen, wird diese Datei weiterhin ordnungsgemäß in einem Webbrowser angezeigt. Das heißt, Änderungen an einer Datei, die diese beiden Schnittstellen verwenden, sind beim Zugriff auf eine Datei mit der [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) nicht erkennbar.

Die NTFS-Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) bietet eine sichere Implementierung, wenn eigenschaftensätze in eine Datei auf einem NTFS-Volume der Version 5.0 geschrieben werden. Solche Eigenschaftensätze können von der Implementierung auch bei einem Systemfehler nicht beschädigt werden. Wenn z. B. die Stromversorgung eines Systems während eines Aufrufs von [**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) fehlschlägt, während der Eigenschaftensatz auf den Datenträger geleert wird, bleibt der Eigenschaftensatz nie in einem Zwischenzustand. Entweder bleibt die vorherige Version des Eigenschaftensatzes erhalten, oder alle Updates werden gespeichert.

Die NTFS-Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) unterscheidet sich wie folgt von der Implementierung der Verbunddatei:

-   Eine von der [**IEnumSTATPROPSETSTG-Schnittstelle**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) abgerufene [**STATPROPSETSTG-Struktur**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) enthält einen **clsid-Member,** dessen Wert immer 0 **(CLSID \_ NULL)** ist. Bei der Implementierung der Verbunddatei wird der richtige **clsid-Member** für nicht einfache Eigenschaftensätze zurückgegeben (siehe [Storage und Stream Objects für einen Eigenschaftensatz).](storage-vs--stream-for-a-property-set.md)
-   Beim Abrufen einer NTFS-Implementierung des [**IPropertySetStorage-Schnittstellenzeigers**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) mithilfe der [**Funktion StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) oder [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) muss der *grfmode-Parameter* die gleichen Regeln wie für die Verbunddateiimplementierung befolgen.

    Darüber hinaus dürfen die folgenden Flags nicht verwendet werden:

    **STGM \_ SIMPLE,** **STGM \_ TRANSACTED,** **STGM \_ CONVERT,** **STGM \_ PRIORITY** und **STGM \_ DELETEONRELEASE**.

-   Wenn eine [**NTFS-IPropertySetStorage-Schnittstelle**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) von den Funktionen [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) oder [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) abgerufen wird, gelten die Freigabemodi in erster Linie für andere Instanzen dieser Schnittstelle und nicht für Instanzen des Öffnens der Datei selbst. Wenn beispielsweise eine **NTFS-IPropertySetStorage-Schnittstelle** durch Aufrufen der **StgOpenStorageEx-Funktion** geöffnet wird und der *grfmode-Parameter* auf **STGM \_ READWRITE \| STGM \_ SHARE \_ EXCLUSIVE** festgelegt ist, ist es möglich, die Datei mit der [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) zu öffnen.

    Solche gleichzeitigen Instanzen des Öffnens dieser Schnittstelle unterliegen den folgenden Einschränkungen: Der *dwShareMode-Parameter* in der [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) muss das **FILE SHARE \_ \_ READ-Flag** angeben, und der *dwAccess-Parameter* darf nicht das **DELETE-Flag** angeben. Außerdem dürfen die Funktionen [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) und [**MoveFile**](/windows/desktop/api/winbase/nf-winbase-movefile) nicht für eine Datei aufgerufen werden, für die diese Eigenschaftensatzschnittstellen geöffnet sind, da diese Funktionen **DELETE-Zugriff** auf die Datei erfordern.

-   Wenn eine [**NTFS-IPropertySetStorage-Methode**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) als schreibgeschützt geöffnet wird und die Datei derzeit über keine Eigenschaftensätze verfügt, wird die Datei vom zurückgegebenen Objekt nicht geöffnet. Folglich sind andere Öffnungen dieser Datei erfolgreich, auch wenn der Freigabemodus des ursprünglichen geöffneten Vorgangs sie andernfalls ablehnen würde.

    Beispiel: Wenn eine [**NTFS-IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) im Modus **STGM \_ READ \| STGM \_ SHARE \_ EXCLUSIVE** geöffnet wird und die Datei keine Eigenschaftensätze hat, ist es möglich, gleichzeitig die Datei **STGM \_ READWRITE \| STGM \_ SHARE \_ EXCLUSIVE** zu öffnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPropertyStorage-NTFS-Dateisystemimplementierung](ipropertystorage-ntfs-file-system-implementation.md)
</dt> <dt>

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage::EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[**PROPSETFLAG-Konstanten**](propsetflag-constants.md)
</dt> <dt>

[**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> </dl>

 

 