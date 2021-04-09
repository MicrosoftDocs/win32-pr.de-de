---
title: Implementierung der IPropertyStorage-Compound Datei
description: Die com-Implementierung der strukturierten Speicherarchitektur wird als Verbund Dateien bezeichnet.
ms.assetid: c4b4f313-de58-44f2-8ce1-a07cc187d8ca
keywords:
- IPropertyStorage-Schnittstellen-STG, Implementierungen, Verbund Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d927b0145077f12e5ba508ca65554ca33633a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858319"
---
# <a name="ipropertystorage-compound-file-implementation"></a>Implementierung der IPropertyStorage-Compound Datei

Die com-Implementierung der strukturierten Speicherarchitektur wird als [Verbund Dateien](istorage-compound-file-implementation.md)bezeichnet. Speicher Objekte, die in Verbund Dateien implementiert werden, beinhalten eine Implementierung von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), die Schnittstelle, die einen einzelnen permanenten Eigenschaften Satz verwaltet, und [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), die Schnittstelle, die Gruppen von persistenten Eigenschaften Sätzen verwaltet. Weitere Informationen zur **IPropertyStorage** -Schnittstelle finden Sie unter Überlegungen zu **IPropertyStorage** und [Eigenschaften Speicher](property-storage-considerations.md).

Rufen Sie zum Abrufen eines Zeigers auf die Implementierung der Verbund Datei von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) [**stgfoatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) auf, um ein neues Verbund Datei Objekt zu erstellen, oder [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) , um ein zuvor erstelltes Verbund Datei Objekt zu öffnen. Im Fall von **stgkreatestorageex** sollte der *stgfmt* -Parameter auf stgfmt Storage festgelegt werden \_ . Im Fall von " **stgopenstorageex**" sollte der *stgfmt* -Parameter auf "stgfmt \_ Storage" oder "stgfmt any" festgelegt werden \_ . In beiden Fällen sollte der *riid* -Parameter auf IID \_ IPropertySetStorage festgelegt werden. Beide Funktionen stellen einen Zeiger auf die [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle des Objekts bereit. Wenn Sie entweder die [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) -oder [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) -Methode dieser Schnittstelle aufrufen, erhalten Sie einen Zeiger auf die **IPropertyStorage** -Schnittstelle, die Sie verwenden können, um beliebige Methoden aufzurufen.

Eine alternative Möglichkeit, einen Zeiger auf die Implementierung der Verbund Datei von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) zu erhalten, besteht darin, die älteren Funktionen " [**stgforatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) " und " [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) " aufzurufen oder einen *riid* -Parameter von IID \_ IStorage für die Funktion " [**stganatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) " oder " [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) " anzugeben. In beiden Fällen wird ein Zeiger auf die [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle des Objekts zurückgegeben. Mit permanenten Eigenschaften Sätzen können Sie [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die **IPropertySetStorage** -Schnittstelle aufrufen und dabei den Header definierten Namen für den Schnittstellen Bezeichner (IID) \_ IPropertySetStorage angeben.

## <a name="when-to-use"></a>Verwendungs Zeitpunkt

Verwenden Sie [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , um Eigenschaften innerhalb eines einzelnen Eigenschaften Satzes zu verwalten. Die Methoden unterstützen das Lesen, schreiben und Löschen von Eigenschaften und den optionalen Zeichen folgen Namen, die Eigenschafts Bezeichnernamen zugeordnet werden können. Andere Methoden unterstützen die standardcommit-und Wiederherstellungs Speichervorgänge. Es gibt auch eine-Methode, die es Ihnen ermöglicht, Zeiten festzulegen, die dem Eigenschaften Speicher zugeordnet sind, und einen anderen, der die Zuweisung einer CLSID zulässt, die verwendet werden kann, um anderen Code, z. b. Benutzeroberflächen Code, mit dem Eigenschaften Satz zuzuordnen. Der Aufruf der [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) -Methode liefert einen Zeiger auf die Implementierung der Verbund Datei von [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), mit der Sie die Eigenschaften in der Menge auflisten können.

> [!Note]  
> Wenn Sie einen Zeiger auf [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) abrufen, indem Sie [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**stgcreatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) oder [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) in einem Speicher für eine Eigenschaft im einfachen Modus aufrufen, entsprechen die **IPropertyStorage** -Methoden den Regeln von Datenströmen im einfachen Modus. Der Eigenschaften Satz Speicher ist der einfache Modus, wenn er für eine Datei abgerufen wurde, die mit dem "STGM Simple"-Flag erstellt oder geöffnet wurde \_ . In diesem Fall ist es nicht immer möglich, den zugrunde liegenden Stream zu vergrößern, und es ist nicht möglich, vorhandene Eigenschaften durch größere Eigenschaften zu ersetzen. Weitere Informationen finden Sie unter [IPropertySetStorage-Verbund Datei Implementierung](ipropertysetstorage-compound-file-implementation.md).

 

## <a name="ipropertystorage-and-caching"></a>IPropertyStorage und Caching

Die Implementierung der Verbund Datei von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) speichert geöffnete Eigenschaften Sätze im Speicher zwischen, um die Leistung zu verbessern. Folglich werden Änderungen an einem Eigenschaften Satz erst dann in die Verbund Datei geschrieben, wenn die [**Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) -oder **Release** -Methoden (Last Reference) aufgerufen werden.

## <a name="simple-mode-property-sets"></a>Eigenschafts Gruppen im einfachen Modus

Ein Eigenschaften Speicher Objekt befindet sich im einfachen Modus, wenn es aus einem Eigenschaften Satz-Speicher Objekt im einfachen Modus erstellt wird. Beispielsweise würde sich ein Eigenschaften Satz-Speicher Objekt im einfachen Modus befinden, wenn es aus der [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) -Funktion abgerufen wurde, wobei das einfache STGM- \_ Flag im *GRF Mode* -Parameter festgelegt wurde. Beachten Sie, dass der "einfache Modus" nicht mit "einfachen Eigenschaften Sätzen" verknüpft ist. Ein Eigenschaften Satz ist einfach, wenn er durch Aufrufen von [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) erstellt wird, wobei das \_ nicht einfache Flag propsetflag im *grfFlags* -Parameter festgelegt ist. Weitere Informationen zu einfachen und nicht einfachen Eigenschafts Sätzen finden Sie unter [Speicher-und Streamobjekte für einen Eigenschaften Satz](storage-vs--stream-for-a-property-set.md).

Wenn ein Eigenschaften Speicher Objekt für den einfachen Modus erstellt wird, gibt es keine Einschränkungen hinsichtlich der Verwendung. Wenn ein vorhandenes Speicher Objekt für eine Eigenschaft im einfachen Modus geöffnet wird, kann das zugrunde liegende Streamobjekt, das den Eigenschaften Satz speichert, nicht vergrößert werden. Folglich ist es nicht immer möglich, ein solches Eigenschafts Speicher Objekt zu ändern, wenn die Änderung einen größeren Stream erfordert.

## <a name="property-set-formats"></a>Eigenschaften Satz Formate

Die Implementierung der Verbund Datei von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) unterstützt sowohl Version 0 als auch die Eigenschaften Satz-Serialisierungsformate der Version 1. Das Format Version 1 wird auf Computern unter Windows 2000 unterstützt. Weitere Informationen finden Sie unter [Eigenschaften Satz-Serialisierung](version-0-vs--version-1-property-set-serialization.md). Eigenschafts Sätze werden im Format Version 0 erstellt und bleiben in diesem Format, es sei denn, es werden neue Funktionen angefordert. Wenn dies der Fall ist, wird das Format auf Version 1 aktualisiert.

Wenn z. b. ein Eigenschaften Satz mit dem Standardflag propsetflag erstellt wird \_ , ist sein Format Version 0. Solange die Eigenschaften Typen, die dem Format Version 0 entsprechen, in diesen Eigenschaften Satz geschrieben und daraus gelesen werden, verbleibt der Eigenschaften Satz im Format Version 0. Wenn ein Eigenschaftentyp der Version 1 in den Eigenschaften Satz geschrieben wird, wird der Eigenschaften Satz automatisch auf Version 1 aktualisiert. Anschließend kann dieser Eigenschaften Satz nicht mehr von Implementierungen gelesen werden, die nur Version 0 erkennen.

## <a name="ipropertystorage-and-variant-types"></a>IPropertyStorage-und Variant-Typen

Die Implementierung der Verbund Datei von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) unterstützt nicht die Variant-Typen VT \_ unknown oder VT \_ Dispatch im **VT** -Member der [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur.

In der folgenden Tabelle sind Variant-Typen aufgeführt, die in einem SafeArray unterstützt werden. Das heißt, diese Werte können mit dem VT- \_ Array im **VT** -Member der [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur kombiniert werden.



In SAFEARRAY Unterstützte Variant-Typen durch die Implementierung der Verbund Datei von IPropertyStorage

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

Die Implementierung der Verbund Datei von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) unterstützt die folgenden Methoden:

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage:: Read Multiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Liest die im *rgpspec* -Array angegebenen Eigenschaften und liefert die Werte aller gültigen Eigenschaften im *rgvar* -Array von propvarianten. In der Implementierung der com-Verbund Datei führen doppelte Eigenschaften Bezeichner, die auf Stream-oder Speichertypen verweisen, zu mehreren Aufrufen von [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) oder [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) , und der Erfolg oder Misserfolg von "read **Multiple** " hängt von der Fähigkeit der zugrunde liegenden Speicher Implementierung ab, Öffnungsvorgänge gemeinsam zu nutzen. Da in einer Verbund Datei STGM- \_ Freigabe \_ exklusiv erzwungen wird, können mehrere offene Versuche fehlschlagen. Das gleichzeitige Öffnen desselben Speicher Objekts aus demselben übergeordneten Speicher wird nicht unterstützt. Das Flag "STGM- \_ Freigabe \_ exklusiv" muss angegeben werden.

Um einen Thread sicheren Vorgang sicherzustellen, wenn dieselbe Stream-oder Speicher Wert Eigenschaft mehrmals durch denselben [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Zeiger in der Implementierung der com-Verbund Datei angefordert wird, wird der Öffnungsvorgang in Abhängigkeit davon, ob die Eigenschaft bereits geöffnet ist und ob das zugrunde liegende Dateisystem mehrere Neustarts eines Streams oder Speichers verarbeitet, erfolgreich ausgeführt. Folglich führt der Read **Multiple** -Vorgang für eine Stream-oder Speicher Wert-Eigenschaft immer zu einem Aufrufen von [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)oder [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), der den Zugriff (STGM- \_ Lese schreiben usw.) und freigabeflags (STGM \_ -Freigabe \_ exklusiv usw.) für das Öffnen oder Erstellen des ursprünglichen Eigenschaften Satzes übergibt.

Wenn die Methode fehlschlägt, sind die in *rgvar* geschriebenen Werte nicht \[ \] definiert. Wenn einige Stream-oder Speicher Wert Eigenschaften erfolgreich geöffnet werden, aber vor dem Abschluss der Ausführung ein Fehler auftritt, sollten diese vor der Rückgabe der-Methode freigegeben werden.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage:: Write Multiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Schreibt die im *rgpspec* \[ \] -Array angegebenen Eigenschaften und weist Ihnen die in *rgvar* angegebenen [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Tags und-Werte zu \[ \] . Eigenschaften, die bereits vorhanden sind, werden die angegebenen **PROPVARIANT** -Werte zugewiesen. Eigenschaften, die derzeit nicht vorhanden sind, werden erstellt.

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

Löscht Eigenschaftsnamen für die im *rgpropid* -Array angegebenen Eigenschaften \[ \] .

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage:: setClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Legt die **CLSID** des Eigenschaften Satz-Streams fest. In der Implementierung der Verbund Datei wird durch Festlegen der CLSID für einen nicht einfachen Eigenschaften Satz (einer, der Speicher-oder streamwerteigenschaften enthalten kann, wie in [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)beschrieben, auch die CLSID für den zugrunde liegenden unter Speicher festgelegt, sodass Sie durch einen Aufrufen von [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)abgerufen werden kann.

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Bei einfachen und nicht einfachen Eigenschafts Sätzen leert das Image für den Eigenschaften Satz Speicher in den zugrunde liegenden Speicher. Außerdem führt diese Methode für nicht einfache Eigenschaften Sätze im Transaktionsmodus einen Commit (z. b. [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)) für den Speicher aus, der den Eigenschaften Satz enthält.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage:: Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Nur für nicht einfache Eigenschaften Sätze Ruft die [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) -Methode des zugrunde liegenden Speichers auf und öffnet den "Content"-Stream erneut. Bei einfachen Eigenschaften Sätzen gibt diese Schnittstelle immer \_ OK zurück. Nicht einfache Eigenschaften Sätze sind solche, die mit dem nonsimple-Flag propsetflag \_ in der [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) -Methode erstellt wurden. Weitere Informationen finden Sie unter [Speichern und Streamen von Objekten für einen Eigenschaften Satz](storage-vs--stream-for-a-property-set.md) .

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage:: Aufzählung**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Erstellt eine Instanz von [**ienumstatus propstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), deren Methoden aufgerufen werden können, um die [**Status**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) Wert-Strukturen aufzulisten, die Informationen zu den einzelnen Eigenschaften im Satz bereitstellen. Diese Implementierung erstellt ein Array, in das der gesamte Eigenschaften Satz gelesen wird und der freigegeben werden kann, wenn **ienumstatus propstg:: Clone** aufgerufen wird. Änderungen am Eigenschaften Satz werden in einer geöffneten **ienumstatupropstg** -Instanz nicht widergespiegelt. Um solche Änderungen anzuzeigen, muss eine neue Instanz dieses Enumerators erstellt werden.

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage:: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Füllt die Member einer Status- [**setstg**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) -Struktur aus, die Daten über die als Ganzes festgelegte Eigenschaft enthält. Stellt bei der Rückgabe einen Zeiger auf die-Struktur bereit. Bei nicht einfachen Speicher Sätzen ruft diese Implementierung [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (oder [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) auf, um die Uhrzeiten aus dem zugrunde liegenden Speicher oder Stream zu erhalten. Für einfache Speicher Sätze werden keine Zeiten beibehalten.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage:: settimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Für nicht einfache Eigenschaften Sätze legt die vom zugrunde liegenden Speicher unterstützten Zeiten fest. Die Implementierung der Verbund Dateispeicherung unterstützt alle drei: Änderungen, Zugriffe und Erstellung. Diese Implementierung von [**settimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) Ruft die [**IStorage:: setelementtimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) -Methode des zugrunde liegenden Speichers auf, um diese Zeiten abzurufen.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage::/telementtimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> </dl>

 

 