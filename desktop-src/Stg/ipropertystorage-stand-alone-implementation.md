---
title: IPropertyStorage-Stand-alone-Implementierung
description: Die vom System bereitgestellte eigenständige Implementierung von IPropertySetStorage umfasst eine Implementierung von IPropertyStorage, der Schnittstelle, die Eigenschaften in einem Eigenschaftensatzspeicher liest und schreibt.
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- IPropertyStorage-Stand-alone-Implementierung
- IPropertyStorage Strctd Stg , Implementierungen, eigenständig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 200d7f328670b8945807b7db7f742feabe58ad32847e3c56aa98a34278a71fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662550"
---
# <a name="ipropertystorage-stand-alone-implementation"></a>IPropertyStorage-Stand-alone-Implementierung

Die vom System bereitgestellte eigenständige Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) umfasst eine Implementierung von [**IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)der Schnittstelle, die Eigenschaften in einem Eigenschaftensatzspeicher liest und schreibt. Die **IPropertySetStorage-Schnittstelle** erstellt und öffnet Eigenschaftensätze in einem Speicher. Die Schnittstellen [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) und [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) werden auch in der eigenständigen Implementierung bereitgestellt.

Um einen Zeiger auf die eigenständige Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)abzurufen, rufen Sie die [**StgCreatePropStg-Funktion**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) auf, um einen neuen Eigenschaftensatz zu erstellen, oder [**StgOpenPropStg,**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) um den Schnittstellenzeiger für einen vorhandenen Eigenschaftensatz abzurufen (oder rufen Sie die [**Create-**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) oder [**Open-Methoden**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) der eigenständigen [**IPropertySetStorage-Implementierung**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) auf).

Die eigenständige Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) erstellt Eigenschaftssätze für alle Speicher- oder Streamobjekte, nicht nur für verbundbasierte Dateispeicher und Streams. Die eigenständige Implementierung ist nicht von Verbunddateien abhängig und kann mit jeder Implementierung strukturierter Speicher verwendet werden. Weitere Informationen zur Verbunddateiimplementierungen dieser Schnittstelle finden Sie unter [IPropertyStorage-Compound File Implementation](ipropertystorage-compound-file-implementation.md).

## <a name="when-to-use"></a>Verwendungs wann

Verwenden Sie [**IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) um Eigenschaften innerhalb eines einzelnen Eigenschaftensatzes zu verwalten. Die Methoden unterstützen das Lesen, Schreiben und Löschen von Eigenschaften und optionalen Zeichenfolgennamen, die Eigenschafts-IDs zugeordnet werden können. Andere Methoden unterstützen die standardmäßigen Commit- und Wiegespeichervorgänge. Es gibt auch eine Methode, die zeiten festlegt, die dem Eigenschaftenspeicher zugeordnet sind, und eine andere , die die Zuweisung einer CLSID ermöglicht, um anderen Code, z. B. Benutzeroberflächencode, dem Eigenschaftensatz zuzuordnen. Die [**Enum-Methode**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) stellt einen Zeiger auf die eigenständige Implementierung von [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)bereit, die die Eigenschaften in der Menge aufzählt.

## <a name="version-0-and-version-1-property-set-formats"></a>Eigenschaftensatzformate der Version 0 und Version 1

Die eigenständige Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) unterstützt sowohl die Serialisierungsformate der Version 0 als auch der Version 1-Eigenschaftensatz. Weitere Informationen finden Sie unter Serialisierung von [Eigenschaftensatz.](version-0-vs--version-1-property-set-serialization.md) Eigenschaftensätze werden im Format Version 0 erstellt und bleiben in diesem Format erhalten, es sei denn, es werden neue Features angefordert. Zu diesem Zeitpunkt wird das Format auf Version 1 aktualisiert.

Wenn beispielsweise ein Eigenschaftensatz mit dem PROPSETFLAG \_ DEFAULT-Flag erstellt wird, lautet das Format Version 0. Solange Eigenschaftstypen, die dem Format version 0 entsprechen, in diesen Eigenschaftensatz geschrieben und daraus gelesen werden, bleibt der Eigenschaftensatz im Format version 0 erhalten. Wenn ein Eigenschaftentyp der Version 1 in den Eigenschaftensatz geschrieben wird, wird der Eigenschaftensatz automatisch auf Version 1 aktualisiert. Anschließend kann dieser Eigenschaftensatz nicht mehr von Implementierungen gelesen werden, die nur Version 0 verstehen.

## <a name="ipropertystorage-and-variant-types"></a>IPropertyStorage- und Variant-Typen

Die eigenständige Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) unterstützt nicht die Variantentypen VT \_ UNKNOWN oder VT \_ DISPATCH im **vt-Member** der [**PROPVARIANT-Struktur.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

Die folgenden Variantentypen werden in einem SafeArray unterstützt: Das bedeutet, dass diese Werte mit VT \_ ARRAY im **vt-Member** der [**PROPVARIANT-Struktur**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) kombiniert werden können.



Variant-Typen, die in SafeArray durch Verbunddateiimplementierungen von [ **IPropertyStorage** unterstützt werden](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)

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

 



 

Wenn VT \_ VARIANT mit VT ARRAY kombiniert \_ wird, enthält SafeArray selbst [**PROPVARIANT-Strukturen.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) Die Typen dieser Elemente müssen jedoch aus der vorherigen Liste stammen, dürfen nicht VT VARIANT sein \_ und dürfen nicht die VT \_ VECTOR-, VT \_ ARRAY- oder VT \_ BYREF-Indikatoren enthalten.

## <a name="ipropertystorage-methods"></a>IPropertyStorage-Methoden

Die eigenständige Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) unterstützt die folgenden Methoden:

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Liest die im *rgpspec-Array* angegebenen Eigenschaften und stellt die Werte aller gültigen Eigenschaften im *rgvar-Array* von [**PROPVARIANT-Elementen**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) zur Verfügung.

In der vom System bereitgestellten eigenständigen Implementierung führen doppelte Eigenschaftsbezeichner, die auf Stream- oder Speichertypen verweisen, zu mehreren Aufrufen von [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) oder [**IStorage::OpenStorage,**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) und der Erfolg oder Fehler von [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) hängt von der Fähigkeit der zugrunde liegenden Speicherimplementierung ab, offene Speicher freizugeben.

Um einen threadsicheren Vorgang sicherzustellen, wenn dieselbe Stream- oder Speicherwerteigenschaft mehrmals über den gleichen [**IPropertyStorage-Zeiger**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) angefordert wird, ist das Öffnen erfolgreich oder schlägt fehl, je nachdem, ob die Eigenschaft bereits geöffnet ist und ob das zugrunde liegende Dateisystem mehrere Geöffnete eines Streams oder Speichers behandelt. Daher führt der [**ReadMultiple-Vorgang**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) für eine Stream- oder Speicherwerteigenschaft immer zu einem Aufruf von [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)oder [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), wobei der Zugriff (z. B. STGM \_ READWRITE) und Freigabewerte (z. B. STGM \_ SHARE \_ EXCLUSIVE) übergeben werden, die beim ursprünglichen Öffnen oder Erstellen des Eigenschaftensatzes angegeben wurden.

Wenn die Methode fehlschlägt, sind die in *rgvar* geschriebenen Werte \[ \] nicht definiert. Wenn einige Stream- oder Speicherwerteigenschaften erfolgreich geöffnet werden, aber ein Fehler auftritt, bevor die Ausführung abgeschlossen ist, sollten diese Eigenschaften freigegeben werden, bevor die Methode zurückgegeben wird.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Schreibt die im *rgpspec-Array angegebenen* Eigenschaften \[ \] und weist ihnen die [**PROPVARIANT-Tags**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) und -Werte zu, die in *rgvar* angegeben \[ \] sind. Eigenschaften, die bereits vorhanden sind, werden die angegebenen **PROPVARIANT-Werte** zugewiesen, und Eigenschaften, die derzeit nicht vorhanden sind, werden erstellt.

</dd> <dt>

<span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::D eleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)
</dt> <dd>

Löscht die in *rgpspec angegebenen* \[ \] Eigenschaften.

</dd> <dt>

<span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)
</dt> <dd>

Liest vorhandene Zeichenfolgennamen, die den im *rgpropid-Array* angegebenen Eigenschaften-IDs zugeordnet \[ \] sind.

</dd> <dt>

<span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)
</dt> <dd>

Weist im *rglpwstrName-Array* angegebene Zeichenfolgennamen eigenschaften-IDs zu, die im *rgpropid-Array* angegeben sind.

</dd> <dt>

<span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::D eletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)
</dt> <dd>

Löscht die Zeichenfolgennamen der eigenschaften-IDs, die im *rgpropid-Array* angegeben sind, indem **NULL** in den Eigenschaftennamen geschrieben wird.

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Legt die **CLSID** des Eigenschaftensatzstreams fest. In der eigenständigen Implementierung legt das Festlegen der CLSID für einen nicht einfachen Eigenschaftensatz (eine, die Speicher- oder Streamwerteigenschaften enthalten kann, wie unter [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)beschrieben) auch die CLSID für die zugrunde liegende Unterspeicherung fest, sodass sie durch einen Aufruf von [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)abgerufen werden kann.

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Leert sowohl für einfache als auch für nicht einfache Eigenschaftensätze das Speicherimage in das Datenträgersubsystem. Darüber hinaus ruft diese Methode für nicht einfache Transacted Mode-Eigenschaftensätze [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) für den Eigenschaftensatz auf.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage::Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Nur für Nicht-Imple-Eigenschaftssätze ruft die [**Revert-Methode**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) des zugrunde liegenden Speichers auf und öffnet den Datenstrom "contents" erneut. Bei einfachen Eigenschaftensätzen gibt nur E \_ OK zurück.

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Erstellt ein Enumeratorobjekt, das [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)implementiert, dessen Methoden aufgerufen werden können, um die [**STATPROPSTG-Strukturen**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) aufzuzählen, die Informationen zu den einzelnen Eigenschaften in der Menge bereitstellen.

Diese Implementierung erstellt ein Array, in das der gesamte Eigenschaftensatz gelesen wird und das freigegeben werden kann, wenn [**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) aufgerufen wird.

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Füllt die Member einer [**STATPROPSETSTG-Struktur**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) aus, die Informationen über den gesamten Eigenschaftensatz enthält. Gibt bei der Rückgabe einen Zeiger auf die -Struktur an.

Für nicht einfache Speichersätze ruft diese Implementierung [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (oder [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) auf, um die Informationen aus dem zugrunde liegenden Speicher oder Stream abzurufen.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Legt nur für Nonsimple-Eigenschaftssätze die vom zugrunde liegenden Speicher unterstützten Zeiten fest. Diese Implementierung von [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) ruft die [**IStorage::SetElementTimes-Methode**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) des zugrunde liegenden Speichers auf, um die Zeiten zu ändern. Sie unterstützt die von der zugrunde liegenden Methode unterstützten Zeiten, z. B. Änderungszeit, Zugriffszeit oder Erstellungszeit.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPropertySetStorage-Stand-alone-Implementierung](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 