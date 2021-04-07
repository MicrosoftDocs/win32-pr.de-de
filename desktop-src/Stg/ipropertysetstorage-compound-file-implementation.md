---
title: Implementierung der IPropertySetStorage-Compound Datei
description: Die Implementierung des com-Verbund Dateispeicher Objekts umfasst eine Implementierung von IPropertyStorage, die Schnittstelle, die einen einzelnen permanenten Eigenschaften Satz verwaltet, und IPropertySetStorage, die Schnittstelle, die Gruppen von permanenten Eigenschaften Sätzen verwaltet.
ms.assetid: de2cb778-c6eb-4487-996b-87405674f603
keywords:
- IPropertySetStorage-Schnittstellen,-Implementierungen, Verbund Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9053a7cf6bf1ae7e4230b15eb0117c428acb08da
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729081"
---
# <a name="ipropertysetstorage-compound-file-implementation"></a>Implementierung der IPropertySetStorage-Compound Datei

Die [Implementierung des com-Verbund Dateispeicher Objekts](ipropertystorage-compound-file-implementation.md) umfasst eine Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), die Schnittstelle, die einen einzelnen permanenten Eigenschaften Satz verwaltet, und [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), die Schnittstelle, die Gruppen von permanenten Eigenschaften Sätzen verwaltet.

Um einen Zeiger auf die Implementierung der Verbund Datei von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)zu erhalten, geben Sie den Header definierten Namen für den Bezeichner IID \_ IStorage als *riid* -Parameter an, oder verwenden Sie die Funktionen [**stgkreatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) oder [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . Geben Sie in beiden Fällen stgfmt \_ Storage als *stgfmt* -Parameter an. (Stgfmt \_ Beliebige können alternativ im Fall von **stgopenstorageex** angegeben werden.) Geben Sie außerdem den Header definierten Namen für den Schnittstellen Bezeichner (IID) \_ IPropertySetStorage als *riid* -Parameter an. Beide Funktionen stellen einen Zeiger auf die **IPropertySetStorage** -Schnittstelle des Objekts bereit.

Eine andere Möglichkeit, einen Zeiger auf die Implementierung der Verbund Datei zu erhalten, besteht darin, den Header definierten Namen für den Bezeichner IID \_ IStorage als *riid* -Parameter anzugeben oder die Funktionen [**stgkreatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) oder [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) zu verwenden. Dadurch wird ein Zeiger auf die [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle des Objekts bereitgestellt. Wenn Sie persistente Eigenschaften Sätze behandeln möchten, müssen Sie [**IStorage:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle aufrufen.

## <a name="when-to-use-ipropertysetstorage"></a>Verwendungszwecke von IPropertySetStorage

Rufen Sie die Methoden von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) auf, um Eigenschaften Sätze im aktuellen Objekt Satz Speicher für Verbund Dateien zu erstellen, zu öffnen oder zu löschen. Es gibt auch eine Methode, [**IPropertySetStorage:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), die einen Zeiger auf einen Enumerator bereitstellt, der zum Auflisten der Eigenschaften Sätze im Speicher verwendet werden kann.

## <a name="methods"></a>Methoden

[**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)

Erstellt eine neue Eigenschaft im aktuellen Verbund Dateispeicher und stellt bei Rückgabe einen Schnittstellen Zeiger zur Implementierung der Verbund Datei [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) bereit. In dieser Implementierung können Eigenschafts Sätze nur dann transaktiv sein, wenn propsetflag \_ nonsimple angegeben wird. Diese Methode erfordert, dass der im *grsmode* -Parameter angegebene Freigabe Modus "STGM \_ share exklusiv" lautet \_ und dass der Zugriffsmodus entweder STGM- \_ Lese-oder STGM-Lese \_ Schreibvorgänge ist (STGM- \_ Schreibmodus wird nicht unterstützt).

[**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)

Öffnet eine vorhandene Eigenschaft, die im aktuellen Eigenschaften Speicher festgelegt ist. Bei der Rückgabe stellt Sie einen Schnittstellen Zeiger zur Implementierung der Verbund Datei von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)bereit. Diese Methode erfordert, dass der im *grsmode* -Parameter angegebene Freigabe Modus "STGM \_ share \_ exklusiv" ist, und dass der Zugriffsmodus entweder STGM- \_ Lese-oder STGM-Lese \_ Schreibvorgänge ist (STGM-Schreibvorgänge werden \_ nicht unterstützt).

[**IPropertySetStorage::D Elete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)

Löscht eine Eigenschaft, die in diesem Eigenschaften Speicher festgelegt ist.

[**IPropertySetStorage:: Aufzählung**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)

Erstellt ein-Objekt, das zum Aufzählen von [**Status-setstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) -Strukturen verwendet wird. Jede **Status-setstg** -Struktur stellt Daten zu einem einzelnen Eigenschaften Satz bereit.

## <a name="remarks"></a>Bemerkungen

Ab Windows 2000 unterstützt die Verbund Datei Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) den einfachen Modus. Der einfache Modus wird durch Angabe des STGM \_ Simple-Flags für die Funktionen " [**stganatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) " und " [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) " angegeben. Wenn die Verbund Datei im einfachen Modus geöffnet wird, ist die zugehörige **IPropertySetStorage** -Implementierung wie folgt eingeschränkt:

-   Es können nur einfache Eigenschaften Sätze erstellt werden. Das heißt, dass der Wert "propsetflag \_ nicht Simple" im Parameter " *grfFlags* " für die Methode " [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) " einen Fehler verursacht.
-   Nachdem Sie mit [**stganatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) eine Verbund Datei mithilfe von STGM \_ Simple erstellt und die [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle abgefragt haben, können Sie [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) nur einmal aufrufen. Anschließend müssen Sie die [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle freigeben, bevor Sie die **Create** -Methode erneut aufrufen. Weitere Informationen zum einfachen Modus finden Sie unter [**STGM-Konstanten**](stgm-constants.md).
-   Sie können die [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) -Methode nicht verwenden, um einen Eigenschaften Satz zu öffnen, nachdem Sie [**stgkreatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) zum Erstellen des Speicher Objekts verwendet haben. Stattdessen müssen Sie [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) verwenden, bevor Sie [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) Abfragen und die **Open** -Methode aufrufen.
-   Nachdem Sie mit dem STGM Simple-Flag eine Verbund Datei mit [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) geöffnet \_ und die [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle abgefragt haben, können Sie mit [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)jeweils einen Eigenschaften Satz öffnen. Außerdem ist es möglicherweise nicht möglich, die Gesamtgröße der Eigenschaften Gruppe zu erhöhen, während der Eigenschaften Satz geöffnet ist.

Einfache Eigenschaften Sätze können nicht transaagiert werden. Sie können STGM \_ -Transaktionen nicht im *grfMode* -Parameter der [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) -und [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) -Methode angeben, es sei denn, Sie geben auch propsetflag \_ nonsimple im *grfFlags* -Parameter an. Beachten Sie, dass einfache und nicht einfache Eigenschaften Sätze nicht mit den oben beschriebenen Eigenschaften Sätzen im einfachen Modus in Zusammenhang stehen. Weitere Informationen zu einfachen und nicht einfachen Eigenschafts Sätzen finden Sie unter [Speicher-und Streamobjekte für einen Eigenschaften Satz](storage-vs--stream-for-a-property-set.md).

> [!Note]  
> Die documentsummaryinformation und die benutzerdefinierten Eigenschaften Sätze sind insofern eindeutig, als Sie möglicherweise zwei Eigenschaften Satz Abschnitte aufweisen. Weitere Informationen finden Sie in [den Eigenschaften Sätzen documentsummaryinformation und UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPropertyStorage-Implementierung der Verbund Datei](ipropertystorage-compound-file-implementation.md)
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

 

 