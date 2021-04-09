---
title: IPropertySetStorage-eigenständige Implementierung
description: Die vom System bereitgestellte, eigenständige Implementierung von IPropertySetStorage enthält eine Implementierung von IPropertyStorage und IPropertySetStorage.
ms.assetid: 0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2
keywords:
- IPropertySetStorage-Klasse,-Implementierungen,-Implementierungen
- IPropertySetStorage-Schnittstellen-STG, Implementierungen, eigenständige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9fd0afe31775b06b3a5f61f4c79939be976e98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039097"
---
# <a name="ipropertysetstorage-stand-alone-implementation"></a>IPropertySetStorage-eigenständige Implementierung

Die vom System bereitgestellte, eigenständige Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) enthält eine Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) und **IPropertySetStorage**. [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) ist die Schnittstelle, die Eigenschaften in einem Eigenschaften Satz-Speicher liest und schreibt. [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ist die Schnittstelle, mit der Eigenschafts Sätze in einem Speicher erstellt und geöffnet werden. Die Schnittstellen [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) und [**ienumstatus propsetstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) werden auch in der eigenständigen Implementierung bereitgestellt.

Um die eigenständige Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)zu verwenden, rufen Sie zunächst einen Zeiger auf die vom System bereitgestellte, eigenständige Implementierung ab, und ordnen Sie die vom System bereitgestellte Implementierung dem Speicher Objekt zu. Zum Abrufen eines Zeigers auf die eigenständige Implementierung von **IPropertySetStorage** müssen Sie die Funktion " [**stgkreatepropsetstg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) " aufrufen und den *pstorage* -Parameter angeben, der das Speicher Objekt angibt, das den Eigenschaften Satz enthalten soll. Diese Funktion stellt einen Zeiger auf die neue **IPropertySetStorage** -Schnittstelle für das angegebene Speicher Objekt bereit.

Die eigenständige Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) erstellt Eigenschafts Sätze für ein beliebiges Speicher Objekt, nicht nur für Verbund Dateispeicher. Die eigenständige Implementierung ist nicht von Verbund Dateien abhängig und kann mit jeder Implementierung strukturierter Speicher verwendet werden. Alle Einschränkungen der vom Aufrufer bereitgestellten strukturierten Speicher gelten für diese Implementierung von Eigenschaften Sätzen. Wenn Sie z. b. einen Speicher im einfachen Modus für [**stgopenpropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)bereitstellen, wird der resultierende **IPropertySetStorage** durch den bereitgestellten [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)eingeschränkt.

Weitere Informationen zur Implementierung der Verbund Datei dieser Schnittstelle finden Sie im Abschnitt [IPropertySetStorage-Verbund Datei Implementierung](ipropertysetstorage-compound-file-implementation.md).

## <a name="when-to-use"></a>Verwendungs Zeitpunkt

Rufen Sie die Methoden von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) auf, um Eigenschafts Sätze in strukturiertem Speicher zu erstellen, zu öffnen und zu löschen. Es gibt auch eine-Methode, die einen Zeiger auf den [**ienumstatus propsetstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) -Enumerator bereitstellt, der zum Auflisten der Eigenschaften Sätze im Speicher verwendet werden kann.

Die eigenständige Implementierung stellt zusätzlich zu den Methoden " [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) " und " [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) " auch die Hilfsfunktionen " [**stgfoatepropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) " und " [**stgopenpropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) " bereit, um Eigenschafts Sätze zu erstellen und zu öffnen. Diese beiden Funktionen unterstützen den \_ nicht gepufferten Wert propsetflag, sodass Sie Änderungen direkt in den Eigenschaften Satz schreiben können, anstatt Sie in einem Cache zu puffern. Weitere Informationen finden Sie unter [**propsetflag-Konstanten**](propsetflag-constants.md).

## <a name="methods"></a>Methoden

Die eigenständige Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) unterstützt die folgenden Methoden.

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

Erstellt eine neue im Speicher festgelegte Eigenschaft und gibt einen Zeiger auf die [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle für den Eigenschaften Satz zurück.

Wenn Sie den nicht gepufferten Wert "propsetflag" verwenden möchten \_ , verwenden Sie stattdessen die Funktion " [**stgkreatepropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) ", um den neuen Eigenschaften Satz zu erstellen und zu öffnen und einen Zeiger auf die eigenständige Implementierung für die [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle für den Eigenschaften Satz zu erhalten.

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

Öffnet eine vorhandene im Speicher festgelegte Eigenschaft und gibt einen Zeiger auf die [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle für den Eigenschaften Satz zurück.

Wenn Sie den nicht gepufferten Wert "propsetflag" verwenden möchten \_ , verwenden Sie stattdessen die Funktion " [**stgopenpropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) ", um einen Zeiger auf die eigenständige Implementierung von " [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) " für den angegebenen Eigenschaften Satz zu erhalten.

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D Elete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

Löscht eine Eigenschaft, die in diesem Eigenschaften Satz Speicher festgelegt ist.

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage:: Aufzählung**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

Erstellt ein-Objekt, das zum Auflisten von [**Status**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) Wert-Strukturen verwendet werden kann. Jede **Status-setstg** -Struktur stellt Daten zu einem einzelnen Eigenschaften Satz bereit.

> [!Note]  
> Die Eigenschaft "documentsummaryinformation" und "UserDefined" sind insofern eindeutig, als Sie möglicherweise zwei Eigenschaften Satz Abschnitte in einem einzelnen zugrunde liegenden Stream enthalten. Weitere Informationen finden Sie in [den Eigenschaften Sätzen documentsummaryinformation und UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md) .

 

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPropertyStorage-eigenständige Implementierung](ipropertystorage-stand-alone-implementation.md)
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
</dt> <dt>

[**Stgkreatepropsetstg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> <dt>

[**Stgkreatepropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**Stgopenpropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**STGM-Konstanten**](stgm-constants.md)
</dt> </dl>

 

 