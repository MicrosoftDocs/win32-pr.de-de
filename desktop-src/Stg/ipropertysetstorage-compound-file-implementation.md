---
title: IPropertySetStorage-Compound Dateiimplementierung
description: Die Com-Verbunddateispeicherobjektimplementierung umfasst eine Implementierung von IPropertyStorage, der Schnittstelle, die einen einzelnen persistenten Eigenschaftensatz verwaltet, und IPropertySetStorage, der Schnittstelle, die Gruppen von persistenten Eigenschaftensätzen verwaltet.
ms.assetid: de2cb778-c6eb-4487-996b-87405674f603
keywords:
- IPropertySetStorage Strctd Stg , Implementierungen, Verbunddatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3bc0d423b304b6d456ccddab158a48ba0b6d5f3f310d293c6aed0dedb2a556
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662660"
---
# <a name="ipropertysetstorage-compound-file-implementation"></a>IPropertySetStorage-Compound Dateiimplementierung

Die Implementierung des COM-Verbunddateispeicherobjekts enthält eine Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), der Schnittstelle, die einen einzelnen persistenten Eigenschaftensatz verwaltet, und [**IPropertySetStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)der Schnittstelle, die Gruppen von persistenten Eigenschaftensätzen verwaltet. [](ipropertystorage-compound-file-implementation.md)

Um einen Zeiger auf die Verbunddateiimplementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)zu erhalten, geben Sie den headerdefinierten Namen für den Bezeichner IID IStorage als riid-Parameter an, oder verwenden Sie die \_ [**StgCreateStorageEx-**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) oder  [**StgOpenStorageEx-Funktionen.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) Geben Sie in beiden Fällen STGFMT \_ STORAGE als *stgfmt-Parameter* an. (STGFMT \_ ANY kann auch im Fall von **StgOpenStorageEx angegeben werden.)** Geben Sie außerdem den headerdefinierten Namen für die IID-IID \_ IPropertySetStorage als *riid-Parameter* an. Beide Funktionen geben einen Zeiger auf die **IPropertySetStorage-Objektschnittstelle** an.

Eine weitere Möglichkeit, einen Zeiger auf die Verbunddateiimplementierung zu erhalten, besteht in der Angabe des headerdefinierten Namens für den Bezeichner IID IStorage als riid-Parameter oder der Verwendung der \_ [**StgCreateDocfile-**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) oder  [**StgOpenStorage-Funktionen.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) Dadurch wird ein Zeiger auf die [**IStorage-Schnittstelle des Objekts**](/windows/desktop/api/Objidl/nn-objidl-istorage) angezeigt. Wenn Sie persistente Eigenschaftensätze behandeln möchten, rufen Sie [**IStorage::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die [**IPropertySetStorage-Schnittstelle**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) auf.

## <a name="when-to-use-ipropertysetstorage"></a>Verwendung von IPropertySetStorage

Rufen Sie die Methoden von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) auf, um Eigenschaftensätze im aktuellen Verbunddatei-Eigenschaftensatzspeicher zu erstellen, zu öffnen oder zu löschen. Es gibt auch eine [**Methode, IPropertySetStorage::Enum,**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)die einen Zeiger auf einen Enumerator liefert, der zum Aufzählen der Eigenschaftensätze im Speicher verwendet werden kann.

## <a name="methods"></a>Methoden

[**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)

Erstellt einen neuen Eigenschaftensatz im aktuellen Verbunddateispeicher und stellt bei Rückgabe einen Schnittstellenzeiger auf die [**IPropertyStorage-Verbunddateiimplementierung**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) bereit. In dieser Implementierung können Eigenschaftensätze nur dann transaktiv werden, wenn PROPSETFLAG \_ NONSIMPLE angegeben ist. Diese Methode erfordert, dass der im *grfMode-Parameter* angegebene Freigabemodus STGM SHARE EXCLUSIVE und der Zugriffsmodus \_ \_ STGM READ oder \_ STGM \_ READWRITE ist (der STGM WRITE-Modus wird nicht \_ unterstützt).

[**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)

Öffnet einen vorhandenen Eigenschaftensatz im aktuellen Eigenschaftenspeicher. Bei der Rückgabe stellt sie einen Schnittstellenzeiger auf die Verbunddateiimplementierung von [**IPropertyStorage bereit.**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) Diese Methode erfordert, dass der im *grfMode-Parameter* angegebene Freigabemodus STGM SHARE EXCLUSIVE und der Zugriffsmodus \_ \_ STGM READ oder \_ STGM \_ READWRITE ist (STGM WRITE wird nicht \_ unterstützt).

[**IPropertySetStorage::D elete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)

Löscht einen In diesem Eigenschaftsspeicher festgelegten Eigenschaftensatz.

[**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)

Erstellt ein -Objekt, das zum Aufzählen von [**STATPROPSETSTG-Strukturen verwendet**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) wird. Jede **STATPROPSETSTG-Struktur** liefert Daten zu einem einzelnen Eigenschaftensatz.

## <a name="remarks"></a>Hinweise

Ab Windows 2000 unterstützt die Verbunddateiimplementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) den einfachen Modus. Der einfache Modus wird durch Angeben des STGM SIMPLE-Flags für die \_ [**Funktionen StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) und [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) angegeben. Wenn die Verbunddatei im einfachen Modus geöffnet wird, ist die zugehörige **IPropertySetStorage-Implementierung** wie folgt beschränkt:

-   Es können nur einfache Eigenschaftensätze erstellt werden. Das heißt, die Angabe des PROPSETFLAG \_ NONSIMPLE-Werts im *grfFlags-Parameter* für die [**IPropertySetStorage::Create-Methode**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) führt zu einem Fehler.
-   Nachdem Sie eine Verbunddatei mit [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) mit STGM SIMPLE erstellt und eine Abfrage für die \_ [**IPropertySetStorage-Schnittstelle**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ausgeführt haben, können Sie [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) nur einmal aufrufen. Anschließend müssen Sie die [**IPropertyStorage-Schnittstelle veröffentlichen,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) bevor Sie die **Create-Methode erneut** aufrufen. Weitere Informationen zum einfachen Modus finden Sie unter [**STGM-Konstanten**](stgm-constants.md).
-   Sie können die [**IPropertySetStorage::Open-Methode**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) nicht verwenden, um einen Eigenschaftensatz zu öffnen, nachdem [**Sie stgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) zum Erstellen des Speicherobjekts verwendet haben. Stattdessen müssen Sie [**StgOpenStorageEx verwenden,**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) bevor Sie [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) abfragen und die **Open-Methode** aufrufen.
-   Nachdem Sie eine Verbunddatei mit [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) mithilfe des STGM SIMPLE-Flags geöffnet und eine Abfrage für die \_ [**IPropertySetStorage-Schnittstelle**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ausgeführt haben, können Sie mithilfe von [**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)einen Eigenschaftensatz gleichzeitig öffnen. Außerdem ist es möglicherweise nicht möglich, die Gesamtgröße des Eigenschaftensets zu erhöhen, während der Eigenschaftensatz geöffnet ist.

Einfache Eigenschaftensätze können nicht transaktiviert werden. Sie können STGM TRANSACTED nicht im grfmode-Parameter der Create- und Open-Methoden angeben, es sei denn, Sie geben \_ auch PROPSETFLAG  [](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) [](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) \_ NONSIMPLE im *grfFlags-Parameter* an. Beachten Sie, dass einfache und nicht einfache Eigenschaftensätze nicht mit den oben beschriebenen Eigenschaftensätzen im einfachen Modus in Zusammenhang stehen. Weitere Informationen zu einfachen und nicht einfachen Eigenschaftensätzen finden Sie unter Storage [und Stream Objects für einen Eigenschaftensatz.](storage-vs--stream-for-a-property-set.md)

> [!Note]  
> Die Eigenschaftensätze DocumentSummaryInformation und UserDefined sind eindeutig, da sie möglicherweise über zwei Eigenschaftensatzabschnitte verfügen. Weitere Informationen finden Sie unter [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPropertyStorage – Verbunddateiimplementierung](ipropertystorage-compound-file-implementation.md)
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

 

 