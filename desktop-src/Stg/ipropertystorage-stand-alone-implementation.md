---
title: IPropertyStorage-eigenständige Implementierung
description: Die vom System bereitgestellte, eigenständige Implementierung von IPropertySetStorage enthält eine Implementierung von IPropertyStorage, die Schnittstelle, die Eigenschaften in einem Eigenschaften Satz-Speicher liest und schreibt.
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- IPropertyStorage-eigenständige Implementierung
- IPropertyStorage-Schnittstellen-STG, Implementierungen, eigenständige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35965831b0105557044461236030e3543c13217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390486"
---
# <a name="ipropertystorage-stand-alone-implementation"></a>IPropertyStorage-eigenständige Implementierung

Die vom System bereitgestellte, eigenständige Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) enthält eine Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), die Schnittstelle, die Eigenschaften in einem Eigenschaften Satz-Speicher liest und schreibt. Mit der **IPropertySetStorage** -Schnittstelle werden Eigenschafts Sätze in einem Speicher erstellt und geöffnet. Die Schnittstellen [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) und [**ienumstatus propsetstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) werden auch in der eigenständigen Implementierung bereitgestellt.

Rufen Sie zum Abrufen eines Zeigers auf die eigenständige Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)die [**stgfoatepropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) -Funktion auf, um einen neuen Eigenschaften Satz zu erstellen, oder [**stgopenpropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) , um den Schnittstellen Zeiger auf einen vorhandenen Eigenschaften Satz abzurufen (oder rufen Sie die [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) -oder [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) -Methode der eigenständigen [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Implementierung auf).

Die eigenständige Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) erstellt Eigenschafts Sätze für beliebige Speicher-oder Streamobjekte, nicht nur für zusammengesetzte Dateispeicher und Streams. Die eigenständige Implementierung ist nicht von Verbund Dateien abhängig und kann mit jeder Implementierung strukturierter Speicher verwendet werden. Weitere Informationen zur Implementierung der Verbund Datei dieser Schnittstelle finden Sie unter [IPropertyStorage-Verbund Datei Implementierung](ipropertystorage-compound-file-implementation.md).

## <a name="when-to-use"></a>Verwendungs Zeitpunkt

Verwenden Sie [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , um Eigenschaften innerhalb eines einzelnen Eigenschaften Satzes zu verwalten. Die Methoden unterstützen das Lesen, schreiben und Löschen von Eigenschaften und den optionalen Zeichen folgen Namen, die Eigenschaften-IDs zugeordnet werden können. Andere Methoden unterstützen die standardcommit-und Wiederherstellungs Speichervorgänge. Es gibt auch eine-Methode, die die dem Eigenschaften Speicher zugeordneten Zeiten festlegt, und einen anderen, der die Zuweisung einer CLSID ermöglicht, um anderen Code, z. b. Benutzeroberflächen Code, mit dem Eigenschaften Satz zuzuordnen. Die [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) -Methode stellt einen Zeiger auf die eigenständige Implementierung von [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)zur Verfügung, die die Eigenschaften im Satz auflistet.

## <a name="version-0-and-version-1-property-set-formats"></a>Eigenschaften Satz Formate Version 0 und Version 1

Die eigenständige Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) unterstützt sowohl Version 0 als auch die Eigenschaften Satz-Serialisierungsformate der Version 1. Weitere Informationen finden Sie unter [Eigenschaften Satz-Serialisierung](version-0-vs--version-1-property-set-serialization.md). Eigenschafts Sätze werden im Format Version 0 erstellt und bleiben in diesem Format, es sei denn, es werden neue Funktionen angefordert. Zu diesem Zeitpunkt wird das Format auf Version 1 aktualisiert.

Wenn z. b. ein Eigenschaften Satz mit dem Standardflag propsetflag erstellt wird \_ , ist sein Format Version 0. Solange die Eigenschaften Typen, die dem Format Version 0 entsprechen, in diesen Eigenschaften Satz geschrieben und daraus gelesen werden, verbleibt der Eigenschaften Satz im Format Version 0. Wenn ein Eigenschaftentyp der Version 1 in den Eigenschaften Satz geschrieben wird, wird der Eigenschaften Satz automatisch auf Version 1 aktualisiert. Anschließend kann dieser Eigenschaften Satz nicht mehr von Implementierungen gelesen werden, die nur Version 0 verstehen.

## <a name="ipropertystorage-and-variant-types"></a>IPropertyStorage-und Variant-Typen

Die eigenständige Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) unterstützt nicht die Variant-Typen VT \_ unknown oder VT \_ Dispatch im **VT** -Member der [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur.

Die folgenden Variant-Typen werden in einem SafeArray unterstützt. Das heißt, diese Werte können mit dem VT- \_ Array im **VT** -Member der [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur kombiniert werden.



In SAFEARRAY Unterstützte Variant-Typen durch die Implementierung der Verbund Datei von [ **IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)

VT \_ I1

VT \_ UI1

VT \_ I2

VT \_ UI2

VT \_ I4

VT \_ UI4

VT \_ int

VT \_ uint

VT \_ R4

VT \_ R8

VT- \_ CY

VT- \_ Datum

VT \_ BSTR

VT \_ bool

VT ( \_ dezimal)

VT- \_ Fehler

VT- \_ Variante

 



 

Wenn die VT- \_ Variante mit dem VT-Array kombiniert wird \_ , enthält das SAFEARRAY selbst [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Strukturen. Allerdings müssen die Typen dieser Elemente aus der vorangehenden Liste entnommen werden, können nicht als VT \_ -Variant verwendet werden und dürfen keine VT- \_ Vektor-, VT \_ Array-oder VT- \_ ByRef-Indikatoren enthalten.

## <a name="ipropertystorage-methods"></a>IPropertyStorage-Methoden

Die eigenständige Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) unterstützt die folgenden Methoden:

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage:: Read Multiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Liest die im *rgpspec* -Array angegebenen Eigenschaften und gibt die Werte aller gültigen Eigenschaften im *rgvar* -Array von [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Elementen an.

In der vom System bereitgestellten eigenständigen Implementierung führen doppelte Eigenschaften Bezeichner, die auf Stream-oder Speichertypen verweisen, zu mehreren Aufrufen von [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) oder [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) , und der Erfolg oder Misserfolg von "read [**Multiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) " hängt von der zugrunde liegenden Speicher Implementierung der Freigabe offener Storages ab.

Um einen Thread sicheren Vorgang sicherzustellen, wenn dieselbe Stream-oder Speicher Wert Eigenschaft mehrmals durch denselben [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Zeiger angefordert wird, wird der offene Vorgang in Abhängigkeit davon, ob die Eigenschaft bereits geöffnet ist oder nicht, unabhängig davon, ob das zugrunde liegende Dateisystem mehrere Starts eines Streams oder Speichers verarbeitet, erfolgreich ausgeführt. Folglich führt der Read [**Multiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) -Vorgang für eine Stream-oder Speicher Wert Eigenschaft immer zum Aufrufen von [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)oder [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), wobei der Zugriff (z. b. STGM \_ -Lese schreiben) und die Freigabe Werte (z. b. STGM- \_ Freigabe \_ exklusiv) angegeben werden, wenn der Eigenschafts Satz ursprünglich geöffnet oder erstellt wurde.

Wenn die Methode fehlschlägt, sind die in *rgvar* geschriebenen Werte nicht \[ \] definiert. Wenn einige Stream-oder Speicher Wert Eigenschaften erfolgreich geöffnet werden, aber vor dem Abschluss der Ausführung ein Fehler auftritt, sollten diese Eigenschaften vor der Rückgabe der Methode freigegeben werden.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage:: Write Multiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Schreibt die im *rgpspec* \[ \] -Array angegebenen Eigenschaften und weist Ihnen die in *rgvar* angegebenen [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Tags und-Werte zu \[ \] . Eigenschaften, die bereits vorhanden sind, werden die angegebenen **PROPVARIANT** -Werte zugewiesen, und Eigenschaften, die derzeit nicht vorhanden sind, werden erstellt.

</dd> <dt>

<span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::D eletemultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)
</dt> <dd>

Löscht die in der *rgpspec* angegebenen Eigenschaften \[ \] .

</dd> <dt>

<span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage:: Read PropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)
</dt> <dd>

Liest vorhandene Zeichen folgen Namen, die den im *rgpropid* -Array angegebenen Eigenschaften-IDs zugeordnet sind \[ \] .

</dd> <dt>

<span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage:: Beschreib tepropertynames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)
</dt> <dd>

Weist den im *rgpropid* -Array angegebenen Eigenschaften-IDs Zeichen folgen Namen zu, die im *rglpwstrinname* -Array angegeben sind.

</dd> <dt>

<span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::D eletepropertynames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)
</dt> <dd>

Löscht die Zeichen folgen Namen der Eigenschaften-IDs, die im *rgpropid* -Array angegeben sind, indem **null** in den Eigenschaftsnamen geschrieben wird.

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage:: setClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Legt die **CLSID** des Eigenschaften Satz-Streams fest. In der eigenständigen Implementierung wird durch das Festlegen der CLSID für einen nicht einfachen Eigenschaften Satz (einer, der Speicher-oder streamwerteigenschaften enthalten kann, wie in [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)beschrieben, auch die CLSID für den zugrunde liegenden unter Speicher festgelegt, sodass Sie durch einen Aufrufen von [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)abgerufen werden kann.

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Bei einfachen und nicht einfachen Eigenschafts Sätzen leert das Speicher Image in das Datenträger Subsystem. Außerdem ruft diese Methode für nicht einfache Eigenschaften Sätze im Transaktionsmodus [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) für den Eigenschaften Satz auf.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage:: Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Nur für nicht einfache Eigenschaften Sätze Ruft die [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) -Methode des zugrunde liegenden Speichers auf und öffnet den "Content"-Stream erneut. Bei einfachen Eigenschaften Sätzen wird nur E OK zurückgegeben \_ .

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage:: Aufzählung**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Erstellt ein Enumeratorobjekt, das [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)implementiert. die Methoden von können aufgerufen werden, um die [**Status**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) Wert-Strukturen aufzulisten, die Informationen zu den einzelnen Eigenschaften im Satz bereitstellen.

Diese Implementierung erstellt ein Array, in das der gesamte Eigenschaften Satz gelesen wird und der freigegeben werden kann, wenn [**ienumstatus propstg:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) aufgerufen wird.

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage:: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Füllt die Member einer Status- [**setstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) -Struktur aus, die Informationen über die als Ganzes festgelegte Eigenschaft enthält. Stellt bei der Rückgabe einen Zeiger auf die-Struktur bereit.

Bei nicht einfachen Speicher Sätzen ruft diese Implementierung [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (oder [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) auf, um die Informationen aus dem zugrunde liegenden Speicher oder Stream zu erhalten.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage:: settimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Für nicht einfache Eigenschaften Sätze legt die vom zugrunde liegenden Speicher unterstützten Zeiten fest. Diese Implementierung von [**settimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) Ruft die [**IStorage:: setelementtimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) -Methode des zugrunde liegenden Speichers auf, um die Zeiten zu ändern. Es unterstützt die von der zugrunde liegenden Methode unterstützten Zeiten, die Änderungszeit, Zugriffszeit oder Erstellungszeit aufweisen können.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPropertySetStorage-eigenständige Implementierung](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage::/telementtimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[**Stgopenpropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**Stgkreatepropstg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**Stgkreatepropsetstg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 