---
title: IPropertyStorage-Compound Dateiimplementierung
description: Die COM-Implementierung der Structured Storage-Architektur wird als Verbunddateien bezeichnet.
ms.assetid: c4b4f313-de58-44f2-8ce1-a07cc187d8ca
keywords:
- IPropertyStorage Strctd Stg , Implementierungen, Verbunddatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3c4fffe98c4bfb896f346f25ce988f75bacf1fbb194b9ec27f50e22095c8cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662610"
---
# <a name="ipropertystorage-compound-file-implementation"></a>IPropertyStorage-Compound Dateiimplementierung

Die COM-Implementierung der Structured Storage-Architektur wird als [Verbunddateien bezeichnet.](istorage-compound-file-implementation.md) Storage-Objekte, die in Verbunddateien implementiert werden, enthalten eine Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), der Schnittstelle, die einen einzelnen persistenten Eigenschaftensatz verwaltet, und [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), der Schnittstelle, die Gruppen von persistenten Eigenschaftensätzen verwaltet. Weitere Informationen zur **IPropertyStorage-Schnittstelle** finden Sie unter Überlegungen zu **IPropertyStorage** [und Storage Eigenschaften.](property-storage-considerations.md)

Um einen Zeiger auf die Verbunddateiimplementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)zu erhalten, rufen Sie [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) auf, um ein neues Verbunddateiobjekt zu erstellen, oder [**StgOpenStorageEx,**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) um ein zuvor erstelltes Verbunddateiobjekt zu öffnen. Im Fall von **StgCreateStorageEx** sollte der *stgfmt-Parameter* auf STGFMT STORAGE festgelegt \_ werden. Im Fall von **StgOpenStorageEx** sollte der *stgfmt-Parameter* auf STGFMT \_ STORAGE oder STGFMT ANY festgelegt \_ werden. In beiden Fällen sollte der *riid-Parameter* auf IID \_ IPropertySetStorage festgelegt werden. Beide Funktionen geben einen Zeiger auf die [**IPropertySetStorage-Objektschnittstelle**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) an. Durch Aufrufen der [**Create-**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) oder [**Open-Methode**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) dieser Schnittstelle erhalten Sie einen Zeiger auf die **IPropertyStorage-Schnittstelle,** mit der Sie eine der Methoden aufrufen können.

Alternativ können Sie einen Zeiger auf die Verbunddateiimplementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) erhalten, indem Sie die älteren [**Funktionen StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) und [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) aufrufen oder einen *riid-Parameter* von IID IStorage für die \_ [**StgCreateStorageEx-**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) oder [**StgOpenStorageEx-Funktion**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) angeben. In beiden Fällen wird ein Zeiger auf die [**IStorage-Schnittstelle**](/windows/desktop/api/Objidl/nn-objidl-istorage) des Objekts zurückgegeben. Rufen Sie bei persistenten Eigenschaftensätzen [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die **IPropertySetStorage-Schnittstelle** auf, und geben Sie dabei den headerdefinierten Namen für die IID-IID \_ IPropertySetStorage an.

## <a name="when-to-use"></a>Verwendung

Verwenden [**Sie IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) um Eigenschaften innerhalb eines einzelnen Eigenschaftensets zu verwalten. Seine Methoden unterstützen das Lesen, Schreiben und Löschen sowohl von Eigenschaften als auch der optionalen Zeichenfolgennamen, die Eigenschaftsbezeichnern zugeordnet werden können. Andere Methoden unterstützen die standardmäßigen Commit- und Rückstellvorgänge für Speicher. Es gibt auch eine -Methode, mit der Sie Zeiten festlegen können, die dem Eigenschaftenspeicher zugeordnet sind, und eine andere, die die Zuweisung einer CLSID ermöglicht, die verwendet werden kann, um anderen Code, z. B. Benutzeroberflächencode, dem Eigenschaftensatz zu zuordnen. Durch Aufrufen [**der Enum-Methode**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) wird ein Zeiger auf die Verbunddateiimplementierung von [**IEnumSTATPROPSTG zur EnumSTATPROPSTG-Methode**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)zur Aufzählung der Eigenschaften in der Gruppe verwendet.

> [!Note]  
> Wenn Sie einen Zeiger auf [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) abrufen, indem Sie [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx,**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) oder [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) in einem Eigenschaftensatzspeicher im einfachen Modus aufrufen, entsprechen die **IPropertyStorage-Methoden** den Regeln von Datenströmen im einfachen Modus. Der Eigenschaftensatzspeicher ist ein einfacher Modus, wenn er für eine Datei ermittelt wurde, die mit dem STGM SIMPLE-Flag erstellt oder \_ geöffnet wurde. In diesem Fall ist es nicht immer möglich, den zugrunde liegenden Stream zu vergrößern, und es ist nicht möglich, vorhandene Eigenschaften durch größere Eigenschaften zu ersetzen. Weitere Informationen finden Sie unter [IPropertySetStorage-Compound File Implementation](ipropertysetstorage-compound-file-implementation.md).

 

## <a name="ipropertystorage-and-caching"></a>IPropertyStorage und Caching

Die Verbunddateiimplementierung [**von IPropertyStorage speichert**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) offene Eigenschaftensätze im Arbeitsspeicher zwischen, um die Leistung zu verbessern. Daher werden Änderungen an einem Eigenschaftensatz erst dann in die Verbunddatei geschrieben, wenn die [**Commit-**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) oder **Release-Methoden** (letzter Verweis) aufgerufen werden.

## <a name="simple-mode-property-sets"></a>Eigenschaftensätze im einfachen Modus

Ein Eigenschaftenspeicherobjekt befindet sich im einfachen Modus, wenn es aus einem Eigenschaftensatz-Speicherobjekt im einfachen Modus erstellt wird. Ein Eigenschaftssatz-Speicherobjekt befindet sich beispielsweise im einfachen Modus, wenn es von der [**StgOpenStorageEx-Funktion**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) mit dem STGM SIMPLE-Flag im \_ *grfMode-Parameter erhalten* würde. Beachten Sie, dass der "einfache Modus" nicht mit "einfachen Eigenschaftensätzen" verknüpft ist. Ein Eigenschaftensatz ist einfach, wenn er durch Aufrufen von [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) mit dem IM GRFFlags-Parameter festgelegten PROPSETFLAG \_ NONSIMPLE-Flag *erstellt* wird. Weitere Informationen zu einfachen und nicht einfachen Eigenschaftensätzen finden Sie unter Storage [und Stream Objects für einen Eigenschaftensatz.](storage-vs--stream-for-a-property-set.md)

Wenn ein Eigenschaftsspeicherobjekt im einfachen Modus erstellt wird, gibt es keine Einschränkungen hinsichtlich seiner Verwendung. Wenn ein vorhandenes Eigenschaftenspeicherobjekt im einfachen Modus geöffnet wird, kann das zugrunde liegende Streamobjekt, das den Eigenschaftensatz speichert, nicht mehr wachsen. Daher ist es nicht immer möglich, ein solches Eigenschaftenspeicherobjekt zu ändern, wenn die Änderung einen größeren Stream erfordert.

## <a name="property-set-formats"></a>Eigenschaftensatzformate

Die Verbunddateiimplementierung [**von IPropertyStorage unterstützt**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) sowohl das Serialisierungsformat für Version 0 als auch die Serialisierung von Eigenschaftensatzversion 1. Das Format Version 1 wird auf Computern unterstützt, auf denen Windows 2000 ausgeführt wird. Weitere Informationen finden Sie unter [Serialisierung von Eigenschaftensatz.](version-0-vs--version-1-property-set-serialization.md) Eigenschaftensätze werden im Format Version 0 erstellt und verbleiben in diesem Format, es sei denn, neue Features werden angefordert. In diesem Fall wird das Format auf Version 1 aktualisiert.

Wenn beispielsweise ein Eigenschaftensatz mit dem FLAG PROPSETFLAG DEFAULT erstellt wird, ist das Format \_ Version 0. Solange Eigenschaftentypen, die dem Version 0-Format entsprechen, in diesen Eigenschaftensatz geschrieben und daraus gelesen werden, verbleibt der Eigenschaftensatz im Format Version 0. Wenn ein Eigenschaftentyp der Version 1 in den Eigenschaftensatz geschrieben wird, wird der Eigenschaftensatz automatisch auf Version 1 aktualisiert. Anschließend kann dieser Eigenschaftensatz nicht mehr von Implementierungen gelesen werden, die nur Version 0 erkennen.

## <a name="ipropertystorage-and-variant-types"></a>IPropertyStorage- und Variant-Typen

Die Verbunddateiimplementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) unterstützt die Variantentypen VT UNKNOWN oder VT DISPATCH im vt-Member der \_ \_ [**PROPVARIANT-Struktur nicht.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 

In der folgenden Tabelle sind varianten Typen aufgeführt, die innerhalb eines SafeArray unterstützt werden. Das heißt, diese Werte können mit VT \_ ARRAY im **vt-Member** der [**PROPVARIANT-Struktur kombiniert**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) werden.



In SafeArray von der Verbunddateiimplementierung von IPropertyStorage unterstützte Variant-Typen

VT \_ I1

VT \_ UI1

VT \_ I2

VT \_ UI2

VT \_ I4

VT \_ UI4

VT \_ INT

VT \_ UINT

VT \_ R4

VT \_ R8

VT \_ CY

VT \_ DATE

VT \_ BSTR

VT \_ BOOL

VT \_ DECIMAL

\_VT-FEHLER

VT \_ VARIANT

 



 

Wenn VT \_ VARIANT mit VT ARRAY kombiniert wird, enthält das \_ SafeArray selbst [**PROPVARIANT-Strukturen.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) Die Typen dieser Elemente müssen jedoch aus der vorherigen Liste übernommen werden, dürfen nicht VT VARIANT sein und können die \_ VT \_ VECTOR-, VT ARRAY- oder \_ VT \_ BYREF-Indikatoren nicht enthalten.

## <a name="ipropertystorage-methods"></a>IPropertyStorage-Methoden

Die Verbunddateiimplementierung [**von IPropertyStorage unterstützt**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) die folgenden Methoden:

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Liest die im *rgpspec-Array* angegebenen Eigenschaften und stellt die Werte aller gültigen Eigenschaften im *rgvar-Array* von PROPVARIANTs zur Auswahl. In der Com-Verbunddateiimplementierung führen doppelte Eigenschaftsbezeichner, die auf Stream- oder Speichertypen verweisen, zu mehreren Aufrufen von [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) oder [**IStorage::OpenStorage,**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) und der Erfolg oder Fehler von **ReadMultiple** hängt von der Fähigkeit der zugrunde liegenden Speicherimplementierung ab, Öffnungsvorgänge gemeinsam zu nutzen. Da in einer Verbunddatei STGM SHARE EXCLUSIVE erzwungen wird, können mehrere offene Versuche \_ \_ nicht mehr erfolgen. Es wird nicht unterstützt, dasselbe Speicherobjekt mehr als einmal aus demselben übergeordneten Speicher zu öffnen. Das STGM \_ SHARE \_ EXCLUSIVE-Flag muss angegeben werden.

Um einen threadsicheren Vorgang sicherzustellen, wenn dieselbe Stream- oder Speicherwerteigenschaft mehrmals über denselben [**IPropertyStorage-Zeiger**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) in der COM-Verbunddateiimplementierung angefordert wird, ist der Öffnungsvorgang erfolgreich oder nicht erfolgreich, je nachdem, ob die Eigenschaft bereits geöffnet ist und ob das zugrunde liegende Dateisystem mehrere Öffnungen eines Streams oder Speichers verarbeitet. Daher führt der **ReadMultiple-Vorgang** für eine Stream- oder Speicherwerteigenschaft immer zu einem Aufruf von [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)oder [**IStorage::OpenStorage,**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)der den Zugriff (STGM READWRITE usw.) und Freigabeflags (STGM SHARE EXCLUSIVE usw.) übergibt, die beim Öffnen oder Erstellen des ursprünglichen Eigenschaftensets angegeben \_ \_ \_ wurden.

Wenn bei der Methode ein Fehler auftritt, sind die in *rgvar geschriebenen* Werte \[ \] nicht definiert. Wenn einige Stream- oder Speicherwerteigenschaften erfolgreich geöffnet werden, aber ein Fehler auftritt, bevor die Ausführung abgeschlossen ist, sollten diese freigegeben werden, bevor die Methode zurückgegeben wird.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Schreibt die im *rgpspec-Array* angegebenen Eigenschaften und weist ihnen die \[ \] [**PROPVARIANT-Tags**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) und -Werte zu, die in *rgvar angegeben* \[ \] sind. Eigenschaften, die bereits vorhanden sind, werden die angegebenen **PROPVARIANT-Werte** zugewiesen. Eigenschaften, die derzeit nicht vorhanden sind, werden erstellt.

</dd> <dt>

<span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::D eleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)
</dt> <dd>

Löscht die in der *rgpspec angegebenen* \[ \] Eigenschaften.

</dd> <dt>

<span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)
</dt> <dd>

Liest vorhandene Zeichenfolgennamen, die den im *rgpropid-Array* angegebenen Eigenschaften-IDs \[ \] zugeordnet sind.

</dd> <dt>

<span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)
</dt> <dd>

Weist im *rglpwstrName-Array* angegebenen Zeichenfolgennamen Eigenschafts-IDs zu, die im *rgpropid-Array angegeben* sind.

</dd> <dt>

<span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::D eletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)
</dt> <dd>

Löscht Eigenschaftsnamen für die eigenschaften, die im *rgpropid-Array angegeben* \[ \] sind.

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Legt die **CLSID des** Eigenschaftensatzstreams fest. In der Verbunddateiimplementierung legt das Festlegen der CLSID für einen nicht einfachen Eigenschaftensatz (einer, der möglicherweise Speicher- oder Streamwerteigenschaften enthalten kann, wie in [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)beschrieben) auch die CLSID für den zugrunde liegenden Unterspeicher fest, sodass sie durch einen Aufruf von [**IStorage::Stat erhalten werden kann.**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Bei einfachen und nicht einfachen Eigenschaftensätzen wird das Speicherimage des Eigenschaftensets in den zugrunde liegenden Speicher geleert. Darüber hinaus führt diese Methode für nicht einfache Eigenschaftensätze im transacted-Modus einen Commit (wie in [**IStorage::Commit)**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)für den Speicher aus, der den Eigenschaftensatz enthält.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage::Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Nur für nicht einfache Eigenschaftensätze ruft die [**Revert-Methode**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) des zugrunde liegenden Speichers auf und öffnet den "contents"-Stream erneut. Bei einfachen Eigenschaftensätzen gibt diese Schnittstelle immer S \_ OK zurück. Nicht einfache Eigenschaftensätze sind diejenigen, die mit dem PROPSETFLAG \_ NONSIMPLE-Flag in der [**IPropertySetStorage::Create-Methode erstellt**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) wurden. Weitere Informationen finden Sie unter Storage [und Streamen von Objekten für einen Eigenschaftensatz.](storage-vs--stream-for-a-property-set.md)

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Erstellt eine Instanz von [**IEnumSTATPROPSTG,**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)deren Methoden aufgerufen werden können, um die [**STATPROPSTG-Strukturen**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) aufzählen zu können, die Informationen zu den einzelnen Eigenschaften in der Gruppe bereitstellen. Diese Implementierung erstellt ein Array, in das der gesamte Eigenschaftensatz gelesen wird und das freigegeben werden kann, wenn **IEnumSTATPROPSTG::Clone** aufgerufen wird. Änderungen am Eigenschaftensatz werden nicht in einer **geöffneten IEnumSTATPROPSTG-Instanz widergespiegelt.** Um solche Änderungen zu sehen, muss eine neue Instanz dieses Enumerators erstellt werden.

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Füllt die Member einer [**STATPROPSETSTG-Struktur**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) aus, die Daten zum Eigenschaftensatz als Ganzes enthält. Gibt bei der Rückgabe einen Zeiger auf die -Struktur an. Bei nicht einfachen Speichersätzen ruft diese Implementierung [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (oder [**IStream::Stat)**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)auf, um die Zeiten aus dem zugrunde liegenden Speicher oder Stream zu erhalten. Bei einfachen Speichersätzen werden keine Zeiten beibehalten.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Legt nur für nicht einfache Eigenschaftensätze die vom zugrunde liegenden Speicher unterstützten Zeiten fest. Die Verbunddateispeicherimplementierung unterstützt alle drei: Änderung, Zugriff und Erstellung. Diese Implementierung von [**SetTimes ruft**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) die [**IStorage::SetElementTimes-Methode**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) des zugrunde liegenden Speichers auf, um diese Zeiten abzurufen.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> </dl>

 

 