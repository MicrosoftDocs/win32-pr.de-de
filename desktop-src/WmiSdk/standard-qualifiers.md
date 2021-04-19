---
description: Alle CIM-kompatiblen Implementierungen müssen einen Standardsatz von Qualifizierern verarbeiten.
ms.assetid: 671ea769-f68d-4788-96f5-c4f86ab3b00e
ms.tgt_platform: multiple
title: Standard Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: 710e93e53f9e414a44dc14ebafea426f5d7f9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356622"
---
# <a name="standard-qualifiers"></a>Standard Qualifizierer

Alle CIM-kompatiblen Implementierungen müssen einen Standardsatz von Qualifizierern verarbeiten. Ein bestimmtes Objekt verfügt nicht über alle aufgeführten Qualifizierer. Normalerweise stellen Erweiterungs Klassen zusätzliche Qualifizierer bereit, um die Bereitstellung von Klassen Instanzen und anderen Vorgängen für die Klasse zu vereinfachen.

Der Anbieter muss die Qualifizierer erzwingen. WMI erzwingt keine Qualifizierer, sondern verwendet Sie nur, um den Benutzer darüber zu informieren, wie die-Eigenschaft verwendet wird.

> [!Note]  
> WMI ist mit der CIM 2,5-Spezifikation kompatibel.

 

Qualifizierer weisen die folgenden Einschränkungen auf:

-   Nicht alle Standard Qualifizierer können gleichzeitig verwendet werden.
-   Nicht alle Qualifizierer können auf alle Konstrukte angewendet werden, wie z. b. Association oder Reference. Diese Einschränkungen werden in der Liste gilt für identifiziert.
-   Für ein bestimmtes Konstrukt, wie z. b. Zuordnung oder Verweis, kann die Verwendung der rechtlichen Qualifizierer weiter eingeschränkt werden, da sich einige Qualifizierer gegenseitig ausschließen. die Verwendung eines Qualifizierers impliziert möglicherweise einige Einschränkungen für den Wert eines anderen, usw. Diese Verwendungs Regeln sind dokumentiert.
-   Juristische Qualifizierer werden nur von Entitäten wie Eigenschaften, Methoden, Instanzen oder Unterklassen geerbt, nicht von Zuordnungen oder verweisen. Beispielsweise wird der **maxlen** -Qualifizierer, der sich auf Eigenschaften bezieht, nicht von verweisen geerbt.

Im folgenden werden die WMI-Standard Qualifizierer aufgeführt

<dt>

<span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Kter**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Klassen, Zuordnungen, Hinweise

Gibt an, ob die Klasse abstrakt ist und nur als Basis für neue Klassen fungiert. Der Standardwert ist **false**. Es können keine Instanzen von abstrakten Klassen erstellt werden. Das Fehlen dieses Qualifizierers gibt an, dass die Klasse nicht abstrakt ist. Daher ist dieser Qualifizierer für alle abstrakten Klassen erforderlich.

</dd> <dt>

<span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**End**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Verweise

Gibt an, ob der Verweis die übergeordnete Komponente einer Aggregations Zuordnung ist. Der Standardwert ist **false**.

Verwendung: die **Aggregations** -und **Aggregat** Qualifizierer   **werden zusammen verwendet** , um die Zuordnung zu qualifizieren, und **Aggregat** gibt den übergeordneten Verweis an.

</dd> <dt>

<span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Stellung**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Zuordnungen

Gibt an, ob die Zuordnung eine Aggregation ist. Der Standardwert ist **false**. Wird zusammen mit **Aggregate** verwendet. Dieser Qualifizierer ist für alle Aggregations Zuordnungen erforderlich.

</dd> <dt>

<span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Eigenschaften, Verweise, Methoden

Alternativer Name für eine Eigenschaft oder Methode im Schema. Der Standardwert ist **null**.

</dd> <dt>

<span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Eigenschaften, Parameter

Der Typ des qualifizierten Arrays.

Gültige Werte sind:

-   Bag (Standard)
-   Indiziert
-   geordnete

Syntax: wenden Sie diese Art von Qualifizierer auf Eigenschaften und Parameter an (definiert durch Klammern-Syntax).

</dd> <dt>

<span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap**
</dt> <dd>

Datentyp: **Zeichen folgen Array**

Gilt für: Eigenschaften, Methoden, Parameter

Zuordnung von wichtigen Bitpositionen, bei denen jede bedeutende Position "on" oder "Off" sein kann. Jedes "on"-Bit ist einem entsprechenden Wert im **BitValues** -Array zugeordnet. Wenn Sie über mehrere Bits "on" verfügen, werden mehrere gleichzeitige Werte im **BitValues** -Array angegeben. Der Standardwert ist **null**.

Weitere Informationen finden Sie unter [Bitmap und BitValues](bitmap-and-bitvalues.md).

</dd> <dt>

<span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**
</dt> <dd>

Datentyp: **Zeichen folgen Array**

Gilt für: Eigenschaften, Methoden, Parameter

Übersetzung eines bitpositions Werts in eine zugeordnete **Zeichenfolge**. Der Standardwert ist **null**.

Weitere Informationen finden Sie unter [Bitmap und BitValues](bitmap-and-bitvalues.md).

</dd> <dt>

<span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Konstruktor**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Methoden

Gibt an, ob die Methode-Instanzen erstellt. Diese Methoden sind nicht darauf beschränkt, für eine einzelne Instanz oder eine einzelne Klasse zu agieren. Ein Konstruktor kann z. b. Zuordnungs Instanzen und Instanzen der Klasse erstellen, die den Konstruktor definiert.

Der **konstruktorqualifizierer** ist nur für Informationen vorgesehen, und es wird nicht erwartet, dass er vom Objekt-Manager bearbeitet wird. Der Objekt-Manager muss beim Erstellen eines Objekts keine Konstruktormethoden aufzurufen. Wenn ein Konstruktor aufgerufen wird, muss der Objekt-Manager auch keine Konstruktormethoden aufrufen, die für eine übergeordnete Klasse der ursprünglichen Klasse definiert wurden. Der Standardwert ist **false**.

</dd> <dt>

<span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**Mit der**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Klassen

Der Name der Methode, mit der Instanzen dieser Klasse erstellt werden. Der Wert ist entweder "PutInstance" oder der Name einer anderen Methode, mit der die Instanzen erstellt werden. Der Standardwert ist **null**.

Verwendung: dieser Qualifizierer kann nur verwendet werden, wenn der **SupportsCreate-Qualifizierer** vorhanden ist.

</dd> <dt>

<span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**Deleteby**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Klassen

Der Name der Methode, mit der Instanzen dieser Klasse gelöscht werden. Der Wert ist entweder "Delta einstance" oder der Name einer anderen Methode, mit der die Instanzen gelöscht werden. Der Standardwert ist **null**.

Verwendung: dieser Qualifizierer kann nur verwendet werden, wenn der **SupportsDelete** -Qualifizierer vorhanden ist.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: beliebig

Beschreibung eines benannten Elements. Der Standardwert ist **null**.

</dd> <dt>

<span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destruktor**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Methoden

Gibt an, ob die-Methode-Instanzen löscht. Methoden, die den **dekonstruktorqualifizierer** verwenden, löschen die Instanz (en), auf die der Dekonstruktor angewendet wird, und sind nicht darauf beschränkt, für eine einzelne Instanz oder Klasse zu agieren. Beispielsweise kann ein Dekonstruktor Zuordnungs Instanzen und Instanzen der Klasse löschen, die den Dekonstruktor definiert.

Der **debuggerqualifizierer** ist nur für Informationen vorgesehen, und es wird nicht erwartet, dass er vom Objekt-Manager bearbeitet wird. Es ist nicht zulässig, dass der Objekt-Manager eine Methode aufruft, die den **Dekonstruktor** -Qualifizierer aufweist, wenn eine Instanz gelöscht wird. Wenn ein Dekonstruktor aufgerufen wird, muss der Objekt-Manager auch keine dekonstruktormethoden aufrufen, die für eine übergeordnete Klasse der ursprünglichen Klasse definiert wurden. Der Standardwert ist **false**.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Display Name**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: beliebig

Der in der Benutzeroberfläche angezeigte Name und nicht der tatsächliche Name des Elements. Der Standardwert ist **null**.

</dd> <dt>

<span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**Embeddecodinstance**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: beliebig

Das qualifizierte String Type-Element enthält eine eingebettete-Instanz. Der qualifiziererwert gibt den Namen einer CIM-Klasse im gleichen Namespace wie die Klasse an, die das qualifizierte Element besitzt. Die eingebettete Instanz ist eine Instanz der angegebenen Klasse, einschließlich Instanzen der zugehörigen Unterklassen. Der Standardwert ist **null**.

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Mess Gerät**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: beliebig

Gibt an, ob die-Eigenschaft eine nicht negative ganze Zahl darstellt, die vergrößert oder verringert werden kann, aber nie einen maximalen Wert überschreitet. Der Standardwert ist **false**.

Der maximale Wert der Eigenschaft darf nicht größer als 2 ^*n* -1 sein. *N* kann je nach Datentyp der Eigenschaft, auf die dieser Qualifizierer angewendet wird, 8, 16, 32 oder 64 sein. Der Wert eines Messgerätes hat seinen maximalen Wert, wenn die zu modellierenden Informationen größer oder gleich diesem maximalen Wert sind. Wenn die zu modellierenden Informationen dann unter den maximalen Wert sinken, sinkt auch das Messgerät. Dieser Qualifizierer ist nur auf Eigenschaften mit einem Integer-Datentyp ohne Vorzeichen anwendbar.

</dd> <dt>

<span id="In"></span><span id="in"></span><span id="IN"></span>**In**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Parameter

Gibt an, ob der-Parameter verwendet wird, um Werte an eine Methode zu übergeben. Der Standardwert ist " **true**".

</dd> <dt>

<span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, out**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Parameter

Gibt an, ob der Parameter ein Eingabe-und ein Ausgabeparameter ist.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Wichtigen**](key-qualifier.md)
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Eigenschaften, Verweise

Gibt an, ob die Eigenschaft Teil des Namespace Handles ist. Wenn mehr als eine Eigenschaft den [**Schlüssel**](key-qualifier.md) Qualifizierer aufweist, bilden alle diese Eigenschaften zusammen den Schlüssel (einen Verbund Schlüssel). Bei gemeinsamer Erstellung müssen die Schlüsseleigenschaften einen eindeutigen Verweis für jede Klasseninstanz angeben. Wenn dieser Qualifizierer für eine Eigenschaft platziert wird, ist nur der Wert **true** zulässig.

</dd> <dt>

<span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Lazy**
</dt> <dd>

Gilt für: Eigenschaften

Gibt an, dass die Eigenschaft für die Rückgabe ressourcenintensiv ist und viel Prozessorzeit und Arbeitsspeicher erfordert. WMI verbessert die Leistung von Abfragen, indem nicht versucht wird, die mit dem **Lazy** -Qualifizierer markierten Eigenschaften zurückzugeben.

</dd> <dt>

<span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**Mappingstrings**
</dt> <dd>

Datentyp: **Zeichen folgen Array**

Gilt für: Klassen, Eigenschaften, Zuordnungen, Hinweise, Verweise

Ein Satz von Werten, die einen Pfad zu einem Speicherort angeben, an dem Sie weitere Informationen über den Ursprung einer Eigenschaft, Klasse, Zuordnung, Angabe oder eines Verweises finden können. Bei der zuordnungszeichenfolge kann es sich um einen Verzeichnispfad, eine URL, einen Registrierungsschlüssel, eine Includedatei, einen Verweis auf eine CIM-Klasse oder ein anderes Format handeln. Der Standardwert ist **null**.

</dd> <dt>

<span id="Max"></span><span id="max"></span><span id="MAX"></span>**Max**
</dt> <dd>

Datentyp: **int**

Gilt für: Verweise

Maximale Anzahl von Werten, die ein bestimmter Verweis für jeden Satz anderer Verweis Werte in der Zuordnung aufweisen kann. Der Standardwert ist **null**. Wenn eine Zuordnung z. b. eine-Instanz mit B-Instanzen verknüpft und höchstens eine-Instanz für jede B-Instanz vorhanden sein muss, sollte der Verweis auf einen-Wert maximal einen Qualifizierer aufweisen.

</dd> <dt>

<span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**
</dt> <dd>

Datentyp: **int**

Gilt für: Eigenschaften, Methoden, Parameter

Maximale Länge (in Zeichen) eines **Zeichen** folgen Datenelements und gibt die Unterstützung von Arrays mit fester Länge an.

Wenn ein Array mit fester Länge gefunden wird, enthält der **maxlen** -Qualifizierer die festgelegte Länge, die beim Parsen gefunden wurde. Wenn ein Array variabler Länge gefunden wird, wird dieser Qualifizierer nicht verwendet. **Maxlen** wird verwendet, um die maximale Anzahl von Elementen vorzuschlagen, die in einem Array gespeichert werden sollen. Wenn Sie den Standardwert überschreiben, können alle ganzzahligen Werte ohne Vorzeichen (**UInt32**) angegeben werden. Der Wert **null** (Standard) impliziert eine unbegrenzte Länge.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**
</dt> <dd>

Datentyp: **int**

Gilt für: Eigenschaften, Methoden, Parameter

Der Höchstwert des Objekts. Der Standardwert ist **null**.

</dd> <dt>

<span id="Min"></span><span id="min"></span><span id="MIN"></span>**Man**
</dt> <dd>

Datentyp: **int**

Gilt für: Verweise

Minimale Kardinalität des Verweises (die minimale Anzahl von Werten, die ein bestimmter Verweis für jeden Satz anderer Verweis Werte in der Zuordnung aufweisen kann). Die Standardeinstellung ist 0.

Wenn eine Zuordnung z. b. eine-Instanz mit B-Instanzen verknüpft und mindestens eine-Instanz für jede b-Instanz vorhanden sein muss, sollte der Verweis auf eine mindestens einen Qualifizierer aufweisen.

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**
</dt> <dd>

Datentyp: **int**

Gilt für: Eigenschaften, Methoden, Parameter

Gibt den minimalen Wert des-Objekts an. Der Standardwert ist **null**.

</dd> <dt>

<span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**Modelkorrespondenz**
</dt> <dd>

Datentyp: **Zeichen folgen Array**

Gilt für: Eigenschaften

Ein Satz von Werten, die die Übereinstimmung zwischen der-Eigenschaft eines Objekts und anderen Eigenschaften im CIM-Schema angeben. Der Standardwert ist **null**.

Objekteigenschaften werden mit der folgenden Syntax identifiziert.

<schema name> "\_" <class or association name> "." <property name>

</dd> <dt>

<span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Nicht lokalen**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Verweise

Speicherort einer Instanz, deren Wert <*NamespaceType*>://<*namespacehandle* ist> der Standardwert ist **null**.

Verwendung: dieser Qualifizierer kann nicht mit dem **nonlocaltype** -Qualifizierer verwendet werden.

</dd> <dt>

<span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**Nonlocaltype**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Verweise

Der Typ des Speicher Orts einer Instanz. Der Wert ist <namespacetype> . Der Standardwert ist **null**.

Verwendung: dieser Qualifizierer kann nicht mit dem **nicht lokalen** Qualifizierer verwendet werden.

</dd> <dt>

<span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Eigenschaften

Ein Wert, der angibt, dass die zugeordnete Eigenschaft **null** ist (die-Eigenschaft hat keinen gültigen oder sinnvollen Wert). Der Standardwert ist **null**.

Die Konventionen und Einschränkungen, die zum Definieren von **null** -Werten verwendet werden, entsprechen den Konventionen für den **ValueMap** -Qualifizierer. Hinweis Dieser Qualifizierer kann nicht überschrieben werden. Es ist nicht sinnvoll, einer Unterklasse die Rückgabe eines anderen **null** -Werts als der der übergeordneten Klasse zuzulassen.

</dd> <dt>

<span id="Out"></span><span id="out"></span><span id="OUT"></span>**Vorgenommen**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Parameter

Gibt an, ob der Parameterwerte aus einer Methode zurückgibt. Der Standardwert ist **false**.

</dd> <dt>

<span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Dire**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Eigenschaften, Methoden, Verweise

Die übergeordnete Klasse oder das untergeordnete Konstrukt (Eigenschaft, Methode oder Verweis), die durch die Eigenschaft, die Methode oder den Verweis desselben Namens in der abgeleiteten Klasse überschrieben wird. Der Standardwert ist **null**.

Das Format lautet:

\[<*Klassen*>. \] < unter *geordnetes Konstrukt*>

Wenn der Klassenname weggelassen wird, gilt die außer Kraft setzung für das untergeordnete Konstrukt in der übergeordneten Klasse in der Klassenhierarchie.

Verwendung: der **Überschreibungs** Qualifizierer kann auf Konstrukte verweisen, die auf dem gleichen Meta-Modell basieren. Es ist nicht zulässig, bei einem Überschreibungs Vorgang einen Konstruktnamen oder eine Signatur zu ändern.

</dd> <dt>

<span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**Override Value**
</dt> <dd>

Gilt für: Klassen

Gibt an, ob der Eigenschafts Wert einer Unterklasse den Wert in einer übergeordneten Klasse überschreibt. Wenn Sie eine Abfrage für die übergeordnete Klasse ausführen und die **Where** -Klausel diese Eigenschaft enthält, muss das übergeordnete Element eine Instanz mit dem überschriebenen Wert zurückgeben. Folglich passt die Windows-Verwaltung die **Where** -Klausel der Abfrage an, die an die übergeordnete Klasse gesendet wird, um Verweise auf diese Eigenschaft auszuschließen.

</dd> <dt>

<span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Gepflanzt**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Eigenschaften

Der Name des Schlüssels, der weitergegeben wird. Der Standardwert ist **null**.

Die Verwendung dieses Qualifizierers geht davon aus, dass es nur einen schwachen Qualifizierer für einen Verweis gibt, der die enthaltende Klasse als Ziel hat. Die zugeordnete Eigenschaft muss denselben Wert wie die Eigenschaft aufweisen, die durch den Qualifizierer in der Klasse auf der anderen Seite der schwachen Zuordnung benannt wird. Das Format lautet:

\[<*Klassen*>. \] < unter *geordnetes Konstrukt*>

Verwendung: Wenn der **propagierte** Qualifizierer verwendet wird, muss der [**Schlüssel**](key-qualifier.md) Qualifizierer mit dem Wert " **true**" angegeben werden.

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>**Dazu**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Eigenschaften

Gibt an, ob die-Eigenschaft lesbar ist. Der Standardwert ist " **true**".

</dd> <dt>

<span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Erforderlich**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Eigenschaften

Gibt an, ob ein nicht-NULL-Wert für die-Eigenschaft erforderlich ist. Der Standardwert ist **false**.

</dd> <dt>

<span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Novel**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Klassen, Zuordnungen, Hinweise, Schemas

Die neben Versionsnummer des Schema Objekts. Der Standardwert ist **null**.

Verwendung: der **Versions** Qualifizierer muss vorhanden sein, um die Hauptversionsnummer anzugeben, wenn der **Revisions** Qualifizierer verwendet wird.

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Chaos**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Eigenschaften, Methoden

Der Name des Schemas, in dem das Feature definiert ist. Der Standardwert ist **null**.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Ausgangs**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Klassen, Zuordnungen, Hinweise, Verweise

Der Speicherort einer Instanz. Der Standardwert ist **null**.

Der Qualifizierer Wert ist <*NamespaceType*>://<*namespacehandle* ->.

Verwendung: der **Quellen** Qualifizierer kann nicht mit dem **sourceType** -Qualifizierer verwendet werden.

</dd> <dt>

<span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Klassen, Zuordnungen, Hinweise, Verweise

Der Typ des Speicher Orts einer Instanz. Der Wert dieses Qualifizierers ist <*NamespaceType*>. Der Standardwert ist **null**.

Verwendung: der **sourceType** -Qualifizierer kann nicht mit dem **Quell** Qualifizierer verwendet werden.

</dd> <dt>

<span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Klassen

Gibt an, ob die-Klasse die Erstellung von-Instanzen unterstützt. Der Standardwert ist **false**.

</dd> <dt>

<span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Klassen

Gibt an, ob die-Klasse das Löschen von-Instanzen unterstützt. Der Standardwert ist **false**.

</dd> <dt>

<span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**Supportsupdate**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Klassen

Gibt an, ob die-Klasse das ändern (aktualisieren) der-Instanzen unterstützt. Der Standardwert ist **false**.

</dd> <dt>

<span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Vergütungen**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Klassen

Gibt an, ob die Klasse Unterklassen aufweisen kann. Der Standardwert ist **false**.

Wenn eine Unterklasse deklariert wird, generiert der Compiler einen Fehler.

Verwendung: dieser Qualifizierer kann nicht mit dem **abstrakten** Qualifizierer koexistieren Wenn sowohl der **Terminal** -als auch der **abstrakte** Qualifizierer angegeben werden, generiert der Compiler einen Fehler.

</dd> <dt>

<span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Einrichtungen**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Eigenschaften, Methoden, Parameter

Der Typ der Einheit, in der das zugeordnete Datenelement ausgedrückt wird. Der Standardwert ist **null**.

Beispielsweise kann ein Größendaten Element für **Einheiten** den Wert "Bytes" aufweisen.

</dd> <dt>

<span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**
</dt> <dd>

Datentyp: **Zeichen folgen Array**

Gilt für: Eigenschaften, Methoden, Parameter

Der Satz zulässiger Werte für eine Eigenschaft, einen Methoden Rückgabetyp oder einen Methoden Parameter. Der Standardwert ist **null**.

Verwendung: dieser Qualifizierer kann allein oder in Kombination mit dem **Werte** Qualifizierer verwendet werden. Bei Verwendung in Kombination mit dem **Values** -Qualifizierer stellt die Position des Werts im **ValueMap** -Array den Speicherort des entsprechenden Eintrags im **Values** -Array bereit. Verwenden Sie den **ValueMap** -Qualifizierer nur mit String-und Integer-Werten. Die Syntax für die Darstellung eines ganzzahligen Werts im Wertkarten Array ist eine \[ + \| = \] Ziffern \[ \* Ziffer \] . Der Inhalt, die maximale Anzahl von Ziffern und der dargestellte Wert werden durch den Typ der zugeordneten Eigenschaft eingeschränkt. Beispielsweise kann Uint8 nicht signiert werden, muss kleiner als vier Ziffern sein und muss einen Wert kleiner als 256 darstellen.

</dd> <dt>

<span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Werte**
</dt> <dd>

Datentyp: **Zeichen folgen Array**

Gilt für: Eigenschaften, Methoden, Parameter

Satz von Werten, der einen ganzzahligen Wert in eine zugeordnete Zeichenfolge übersetzt. Der Standardwert ist **null**.

Diese Eigenschaft gibt auch ein Array von Zeichen folgen Werten an, die einer Enumerationseigenschaft zugeordnet werden sollen. Dieser Qualifizierer kann entweder auf eine ganzzahlige Eigenschaft oder eine Zeichen folgen Eigenschaft angewendet werden, und die Zuordnung kann implizit oder explizit sein. Wenn die Zuordnung implizit ist, stellen ganzzahlige Werte oder Zeichen folgen Eigenschaftswerte Ordinalpositionen im **Werte** Array dar. Wenn die Zuordnung explizit ist, muss die-Eigenschaft eine ganze Zahl sein, und gültige Eigenschaftswerte werden in dem Array aufgelistet, das durch den **ValueMap** -Qualifizierer definiert ist. Weitere Informationen finden Sie unter [Value Map](value-map.md).

Wenn kein **ValueMap** -Qualifizierer vorhanden ist, wird das **Values** -Array mit dem Wert in der zugeordneten Eigenschaft, dem Methoden Rückgabetyp oder dem Methoden Parameter indiziert (null-relativ). Wenn ein **ValueMap** -Qualifizierer vorhanden ist, wird der Values-Index durch den Speicherort des Eigenschafts Werts in der Werte Zuordnung definiert.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Klassen, Schemas, Zuordnungen, Hinweise

Die Hauptversionsnummer des Schema Objekts. Der Standardwert ist **null**. Die Versionsnummer wird inkrementiert, wenn Änderungen am Schema vorgenommen werden, die die Schnittstelle ändern.

</dd> <dt>

<span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Weak**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Verweise

Gibt an, ob die Schlüssel der Klasse, auf die verwiesen wird, die Schlüssel der anderen Teilnehmer in der Zuordnung enthalten. Der Standardwert ist **false**.

Dieser Qualifizierer wird verwendet, wenn die Identität der Klasse, auf die verwiesen wird, von der Identität der anderen Teilnehmer in der Zuordnung abhängt. Es kann nicht mehr als ein Verweis auf eine bestimmte Klasse schwach sein. Die anderen Klassen in der Zuordnung müssen einen Schlüssel definieren. Die Schlüssel der anderen Klassen in der Zuordnung werden in der referenzierten Klasse wiederholt und mit einem **propagierten** Qualifizierer gekennzeichnet.

</dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Schreibung**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Eigenschaften

Gibt an, dass Anwendungen oder Skripts den Eigenschafts Wert ändern können. Das Konto, das die Anwendung ausführt, muss Zugriff auf den Namespace haben, der Instanzen der-Klasse enthält. Die Anbieter Implementierung schränkt möglicherweise auch den Zugriff auf Anbieter Daten ein. Der Wert **true** gibt an, dass die Eigenschaft von Consumern lesbar und schreibbar ist, denen der Zugriff durch WMI und den Anbieter gestattet ist. Der Standardwert ist **false**.

Eine Eigenschaft, die nicht über den **Schreib** Qualifizierer verfügt, kann möglicherweise weiterhin geschrieben werden. Die Anbieter Implementierung lässt möglicherweise zu, dass alle Eigenschaften in den Anbieter Klassen geändert werden, unabhängig davon, ob der **Schreib** Qualifizierer vorhanden ist.

</dd> <dt>

<span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**Schreibzugriff erstellen**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Eigenschaften

Gibt an, ob die Eigenschaft bei der Instanzerstellung beschreibbar ist. Dieser Qualifizierer kann in Verbindung mit dem **schreiberstellungs** -Qualifizierer verwendet werden. Der Standardwert ist **false**.

</dd> <dt>

<span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**Write-Update**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Eigenschaften

Gibt an, ob die Eigenschaft beim instanzupdate beschreibbar ist. Dieser Qualifizierer kann in Verbindung mit dem **schreiberstellungs** -Qualifizierer verwendet werden. Der Standardwert ist **false**.

</dd> </dl>

## <a name="examples"></a>Beispiele

Weitere Informationen zum Abrufen von Qualifizierern finden Sie im PowerShell-Codebeispiel [Get-wmiclassmethodsandwrite](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) in der TechNet Gallery.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI Qualifizierer](wmi-qualifiers.md)
</dt> <dt>

[Fügen eines Qualifizierers](adding-a-qualifier.md)
</dt> </dl>

 

 




