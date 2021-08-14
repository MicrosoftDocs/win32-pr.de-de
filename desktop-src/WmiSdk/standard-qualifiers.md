---
description: Alle CIM-kompatiblen Implementierungen müssen einen Standardsatz von Qualifizierern verarbeiten.
ms.assetid: 671ea769-f68d-4788-96f5-c4f86ab3b00e
ms.tgt_platform: multiple
title: Standardqualifizierer
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
ms.openlocfilehash: 67877cfc07a247d6b5e3309270d145bc64fbb814416fa4288c6e85ff2ad2e986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315136"
---
# <a name="standard-qualifiers"></a>Standardqualifizierer

Alle CIM-kompatiblen Implementierungen müssen einen Standardsatz von Qualifizierern verarbeiten. Für ein bestimmtes Objekt sind nicht alle Qualifizierer aufgeführt. In der Regel stellen Erweiterungsklassen zusätzliche Qualifizierer bereit, um die Bereitstellung von Klasseninstanzen und anderen Vorgängen für die Klasse zu vereinfachen.

Es liegt in der Verantwortung des Anbieters, die Qualifizierer zu erzwingen. WMI erzwingt keine Qualifizierer, sondern verwendet sie nur, um den Benutzer darüber zu informieren, wie die Eigenschaft verwendet wird.

> [!Note]  
> WMI ist mit der CIM 2.5-Spezifikation kompatibel.

 

Für Qualifizierer gelten die folgenden Einschränkungen:

-   Nicht alle Standardqualifizierer können zusammen verwendet werden.
-   Nicht alle Qualifizierer können auf alle Konstrukte angewendet werden, z. B. Zuordnung oder Verweis. Diese Einschränkungen sind in der Liste Gilt für aufgeführt.
-   Für ein bestimmtes Konstrukt, z. B. Zuordnung oder Verweis, kann die Verwendung der rechtlichen Qualifizierer weiter eingeschränkt werden, da sich einige Qualifizierer gegenseitig ausschließen, die Verwendung eines Qualifizierers einige Einschränkungen für den Wert eines anderen impliziert usw. Diese Verwendungsregeln sind dokumentiert.
-   Rechtliche Qualifizierer werden nur von Entitäten wie Eigenschaften, Methoden, Instanzen oder Unterklassen geerbt, nicht von Zuordnungen oder Verweisen. Beispielsweise wird  der MaxLen-Qualifizierer, der für Eigenschaften gilt, nicht von Verweisen geerbt.

Im Folgenden werden WMI-Standardqualifizierer aufgeführt.

<dt>

<span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Abstrakt**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Klassen, Zuordnungen, Hinweise

Gibt an, ob die Klasse abstrakt ist und nur als Basis für neue Klassen dient. Der Standardwert ist **FALSE.** Sie können keine Instanzen von abstrakten Klassen erstellen. Das Fehlen dieses Qualifizierers gibt an, dass die Klasse nicht abstrakt ist. daher ist dieser Qualifizierer für alle abstrakten Klassen erforderlich.

</dd> <dt>

<span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Aggregat**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Verweise

Gibt an, ob der Verweis die übergeordnete Komponente einer Aggregationszuordnung ist. Der Standardwert ist **FALSE.**

Verwendung: Die **Aggregations-** und **Aggregatqualifizierer** werden zusammen verwendet   **Aggregation** qualifiziert die Zuordnung, und **Aggregate** gibt den übergeordneten Verweis an.

</dd> <dt>

<span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Aggregation**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Zuordnungen

Gibt an, ob die Zuordnung eine Aggregation ist. Der Standardwert ist **FALSE.** Wird mit **Aggregate** verwendet. Dieser Qualifizierer ist für alle Aggregationszuordnungen erforderlich.

</dd> <dt>

<span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**
</dt> <dd>

Datentyp: **string**

Gilt für: Eigenschaften, Verweise, Methoden

Alternativer Name für eine Eigenschaft oder Methode im Schema. Der Standardwert ist **NULL.**

</dd> <dt>

<span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**
</dt> <dd>

Datentyp: **string**

Gilt für: Eigenschaften, Parameter

Typ des qualifizierten Arrays.

Gültige Werte sind:

-   bag (Standard)
-   Indiziert
-   geordnete

Verwendung: Wenden Sie diesen Typ von Qualifizierer nur auf Eigenschaften und Parameter an, bei denen es sich um Arrays handelt (definiert mithilfe der Klammersyntax).

</dd> <dt>

<span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap**
</dt> <dd>

Datentyp: **Zeichenfolgenarray**

Gilt für: Eigenschaften, Methoden, Parameter

Zuordnung signifikanter Bitpositionen, bei denen jede signifikante Position "on" oder "off" sein kann. Jedes "on"-Bit wird einem entsprechenden Wert im **BitValues-Array** zugeordnet. Wenn mehrere Bits "on" vorliegen, werden mehrere gleichzeitige Werte im **BitValues-Array** angegeben. Der Standardwert ist **NULL.**

Weitere Informationen finden Sie unter [BitMap und BitValues.](bitmap-and-bitvalues.md)

</dd> <dt>

<span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**
</dt> <dd>

Datentyp: **Zeichenfolgenarray**

Gilt für: Eigenschaften, Methoden, Parameter

Übersetzung eines Bitpositionswerts in eine zugeordnete **Zeichenfolge**. Der Standardwert ist **NULL.**

Weitere Informationen finden Sie unter [BitMap und BitValues.](bitmap-and-bitvalues.md)

</dd> <dt>

<span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Konstruktor**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Methoden

Gibt an, ob die Methode -Instanzen erstellt. Diese Methoden sind nicht darauf beschränkt, auf eine einzelne Instanz oder eine einzelne Klasse zu agieren. Beispielsweise kann ein Konstruktor Zuordnungsinstanzen sowie Instanzen der Klasse erstellen, die den Konstruktor definiert.

Der **Konstruktorqualifizierer** ist nur für Informationen vorgesehen, und es wird nicht erwartet, dass er vom Objekt-Manager angewendet wird. Der Objekt-Manager muss keine Konstruktormethoden aufrufen, wenn ein Objekt erstellt wird. Wenn ein Konstruktor aufgerufen wird, muss der Objekt-Manager auch keine Konstruktormethoden aufrufen, die für eine übergeordnete Klasse der ursprünglichen Klasse definiert sind. Der Standardwert ist **FALSE.**

</dd> <dt>

<span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**
</dt> <dd>

Datentyp: **string**

Gilt für: Klassen

Name der Methode, mit der Instanzen dieser Klasse erstellt werden. Der Wert ist entweder "PutInstance" oder der Name einer anderen Methode, die die Instanzen erstellt. Der Standardwert ist **NULL.**

Verwendung: Dieser Qualifizierer kann nur verwendet werden, wenn der **SupportsCreate-Qualifizierer** vorhanden ist.

</dd> <dt>

<span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**
</dt> <dd>

Datentyp: **string**

Gilt für: Klassen

Name der Methode, mit der Instanzen dieser Klasse gelöscht werden. Der Wert ist entweder "DeleteInstance" oder der Name einer anderen Methode, die die Instanzen löscht. Der Standardwert ist **NULL.**

Verwendung: Dieser Qualifizierer kann nur verwendet werden, wenn der **SupportsDelete-Qualifizierer** vorhanden ist.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Datentyp: **string**

Gilt für: beliebige

Beschreibung eines benannten Elements. Der Standardwert ist **NULL.**

</dd> <dt>

<span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destruktor**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Methoden

Gibt an, ob die -Methode -Instanzen löscht. Methoden, die den **Destruktorqualifizierer** verwenden, löschen die Instanzen, auf die der Destruktor angewendet wird, und sind nicht darauf beschränkt, auf eine einzelne Instanz oder Klasse zu agieren. Beispielsweise kann ein Destruktor Zuordnungsinstanzen sowie Instanzen der Klasse löschen, die den Destruktor definiert.

Der **Destruktorqualifizierer** ist nur für Informationen vorgesehen, und es wird nicht erwartet, dass er vom Objekt-Manager angewendet wird. Der Objekt-Manager muss keine Methode aufrufen, die über den **Destruktorqualifizierer** verfügt, wenn eine Instanz gelöscht wird. Wenn ein Destruktor aufgerufen wird, muss der Objekt-Manager außerdem keine Destruktormethoden aufrufen, die für eine übergeordnete Klasse der ursprünglichen Klasse definiert sind. Der Standardwert ist **FALSE.**

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Displayname**
</dt> <dd>

Datentyp: **string**

Gilt für: beliebige

Name, der auf der Benutzeroberfläche anstelle des tatsächlichen Namens des Elements angezeigt wird. Der Standardwert ist **NULL.**

</dd> <dt>

<span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**
</dt> <dd>

Datentyp: **string**

Gilt für: beliebige

Das qualifizierte Zeichenfolgentypelement enthält eine eingebettete Instanz. Der Qualifiziererwert gibt den Namen einer CIM-Klasse im selben Namespace wie die Klasse an, die das qualifizierte Element besitzt. Die eingebettete Instanz ist eine Instanz der angegebenen Klasse, einschließlich Instanzen ihrer Unterklassen. Der Standardwert ist **NULL.**

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Messgerät**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: beliebige

Gibt an, ob die -Eigenschaft eine nicht negative ganze Zahl darstellt, die sich erhöhen oder verringern kann, aber nie einen Höchstwert überschreitet. Der Standardwert ist **FALSE.**

Der maximale Wert der Eigenschaft darf nicht größer als 2^*n* - 1 sein. *N* kann je nach Datentyp der Eigenschaft, auf die dieser Qualifizierer angewendet wird, 8, 16, 32 oder 64 sein. Der Wert eines Messgeräts hat seinen Maximalwert, wenn die zu modellierten Informationen größer oder gleich diesem Maximalwert sind. Wenn die modellierten Informationen anschließend unter den Maximalwert fallen, nimmt auch das Messgerät ab. Dieser Qualifizierer gilt nur für Eigenschaften mit einem ganzzahligen Datentyp ohne Vorzeichen.

</dd> <dt>

<span id="In"></span><span id="in"></span><span id="IN"></span>**In**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Parameter

Gibt an, ob der -Parameter verwendet wird, um Werte an eine Methode zu übergeben. Der Standardwert ist **TRUE.**

</dd> <dt>

<span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, Out**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Parameter

Gibt an, ob der Parameter sowohl ein Eingabe- als auch ein Ausgabeparameter ist.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Schlüssel**](key-qualifier.md)
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Eigenschaften, Verweise

Gibt an, ob die Eigenschaft Teil des Namespacehandle ist. Wenn mehr als eine Eigenschaft über den [**Schlüsselqualifizierer**](key-qualifier.md) verfügt, bilden alle diese Eigenschaften zusammen den Schlüssel (einen zusammengesetzten Schlüssel). Zusammen müssen die Schlüsseleigenschaften einen eindeutigen Verweis für jede Klasseninstanz bereitstellen. Wenn dieser Qualifizierer für eine Eigenschaft platziert wird, ist nur der Wert **TRUE** zulässig.

</dd> <dt>

<span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Faul**
</dt> <dd>

Gilt für: Eigenschaften

Gibt an, dass die -Eigenschaft ressourcenintensiv für die Rückgabe ist und viel Prozessorzeit und Arbeitsspeicher erfordert. WMI verbessert die Leistung von Abfragen, indem nicht versucht wird, die mit dem **verzögerten** Qualifizierer markierten Eigenschaften zurückzugeben.

</dd> <dt>

<span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**
</dt> <dd>

Datentyp: **Zeichenfolgenarray**

Gilt für: Klassen, Eigenschaften, Zuordnungen, Hinweise, Verweise

Ein Satz von Werten, die einen Pfad zu einem Speicherort angeben, an dem Sie weitere Informationen zum Ursprung einer Eigenschaft, Klasse, Zuordnung, Angabe oder eines Verweises finden. Die Zuordnungszeichenfolge kann ein Verzeichnispfad, eine URL, ein Registrierungsschlüssel, eine Includedatei, ein Verweis auf eine CIM-Klasse oder ein anderes Format sein. Der Standardwert ist **NULL.**

</dd> <dt>

<span id="Max"></span><span id="max"></span><span id="MAX"></span>**Max**
</dt> <dd>

Datentyp: **int**

Gilt für: Verweise

Die maximale Anzahl von Werten, die ein angegebener Verweis für jeden Satz anderer Verweiswerte in der Zuordnung aufweisen kann. Der Standardwert ist **NULL.** Wenn beispielsweise eine Zuordnung A-Instanzen mit B-Instanzen verknüpft und für jede B-Instanz höchstens eine A-Instanz vorhanden sein muss, sollte der Verweis auf A maximal einen Qualifizierer aufweisen.

</dd> <dt>

<span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**
</dt> <dd>

Datentyp: **int**

Gilt für: Eigenschaften, Methoden, Parameter

Maximale Länge (in Zeichen) eines Zeichenfolgendatenelements und Gibt die Unterstützung von Arrays fester Länge an. 

Wenn ein Array fester Länge gefunden  wird, enthält der MaxLen-Qualifizierer die feste Länge, die während der Analyse gefunden wurde. Wenn ein Array variabler Länge gefunden wird, wird dieser Qualifizierer nicht verwendet. **MaxLen** wird verwendet, um die maximale Anzahl von Elementen vorzuschlagen, die in einem Array gespeichert werden sollen. Beim Überschreiben des Standardwerts kann jeder ganzzahlige Wert ohne Vorzeichen (**uint32**) angegeben werden. Der Wert **NULL** (Standard) impliziert eine unbegrenzte Länge.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**Maxvalue**
</dt> <dd>

Datentyp: **int**

Gilt für: Eigenschaften, Methoden, Parameter

Maximalwert des Objekts. Der Standardwert ist **NULL.**

</dd> <dt>

<span id="Min"></span><span id="min"></span><span id="MIN"></span>**Min**
</dt> <dd>

Datentyp: **int**

Gilt für: Verweise

Minimale Kardinalität des Verweises (die Mindestanzahl von Werten, die ein bestimmter Verweis für jeden Satz anderer Verweiswerte in der Zuordnung aufweisen kann). Die Standardeinstellung ist 0.

Wenn beispielsweise eine Zuordnung A-Instanzen mit B-Instanzen verknüpft und für jede B-Instanz mindestens eine A-Instanz vorhanden sein muss, sollte der Verweis auf A mindestens einen Qualifizierer aufweisen.

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**Minvalue**
</dt> <dd>

Datentyp: **int**

Gilt für: Eigenschaften, Methoden, Parameter

Gibt den Minimalwert des Objekts an. Der Standardwert ist **NULL.**

</dd> <dt>

<span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**
</dt> <dd>

Datentyp: **Zeichenfolgenarray**

Gilt für: Eigenschaften

Ein Satz von Werten, die eine Entsprechung zwischen der -Eigenschaft eines Objekts und anderen Eigenschaften im CIM-Schema angeben. Der Standardwert ist **NULL.**

Objekteigenschaften werden mithilfe der folgenden Syntax identifiziert.

<schema name> "\_" <class or association name> "." <property name>

</dd> <dt>

<span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Nichtlokale**
</dt> <dd>

Datentyp: **string**

Gilt für: Verweise

Speicherort einer Instanz, deren Wert <*Namespacetyp*>://<*namespacehandle*> Der Standardwert ist **NULL.**

Verwendung: Dieser Qualifizierer kann nicht mit dem **NonlocalType-Qualifizierer** verwendet werden.

</dd> <dt>

<span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**
</dt> <dd>

Datentyp: **string**

Gilt für: Verweise

Typ des Speicherorts einer Instanz. Der Wert ist <namespacetype> . Der Standardwert ist **NULL.**

Verwendung: Dieser Qualifizierer kann nicht mit dem **nichtlokalen Qualifizierer** verwendet werden.

</dd> <dt>

<span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**Nullvalue**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Eigenschaften

Ein Wert, der angibt, dass die zugeordnete Eigenschaft **NULL ist** (die Eigenschaft hat keinen gültigen oder aussagekräftigen Wert). Der Standardwert ist **NULL.**

Die Konventionen und Einschränkungen, die zum Definieren von **NULL-Werten** verwendet werden, sind mit denen identisch, die für den **ValueMap-Qualifizierer** gelten. Beachten Sie, dass dieser Qualifizierer nicht überschrieben werden kann. Es ist nicht sinnvoll, einer Unterklasse zu erlauben, einen anderen **NULL-Wert** als den der übergeordneten Klasse zurückgibt.

</dd> <dt>

<span id="Out"></span><span id="out"></span><span id="OUT"></span>**Out**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Parameter

Gibt an, ob der Parameter Werte von einer Methode zurückgibt. Der Standardwert ist **FALSE.**

</dd> <dt>

<span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Überschreiben**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Eigenschaften, Methoden, Verweise

Übergeordnete Klasse oder untergeordnetes Konstrukt (Eigenschaft, Methode oder Verweis), das durch die Eigenschaft, Methode oder einen Verweis desselben Namens in der abgeleiteten Klasse überschrieben wird. Der Standardwert ist **NULL.**

Das Format lautet:

\[<*-klasse*>. \] < *untergeordnetes Konstrukt*>

Wenn der Klassenname weggelassen wird, gilt die Überschreibung für das untergeordnete Konstrukt in der übergeordneten Klasse in der Klassenhierarchie.

Verwendung:  Der Override-Qualifizierer kann nur auf Konstrukte verweisen, die auf demselben Metamodell basieren. Es ist nicht zulässig, einen Konstruktnamen oder eine Signatur während eines Überschreibungsvorgang zu ändern.

</dd> <dt>

<span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**
</dt> <dd>

Gilt für: Klassen

Gibt an, ob der Eigenschaftswert für eine Unterklasse den Wert in einer übergeordneten Klasse überschreibt. Die funktionale Auswirkung ist, dass das übergeordnete Element eine -Instanz mit dem überschriebenen Wert zurückgeben muss, wenn Sie eine Abfrage für die übergeordnete Klasse ausführen und ihre **WHERE-Klausel** diese Eigenschaft enthält. Daher passt Windows Management die **WHERE-Klausel** der Abfrage an, die an die übergeordnete Klasse gesendet wird, um Verweise auf diese Eigenschaft auszuschließen.

</dd> <dt>

<span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Weitergegeben**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Eigenschaften

Der Name des Schlüssels, der propagiert wird. Der Standardwert ist **NULL.**

Bei Verwendung dieses Qualifizierers wird davon ausgegangen, dass nur ein schwacher Qualifizierer für einen Verweis mit der enthaltenden Klasse als Ziel existiert. Die zugeordnete Eigenschaft muss den gleichen Wert wie die Eigenschaft haben, die vom Qualifizierer in der Klasse auf der anderen Seite der schwachen Zuordnung benannt wird. Das Format lautet:

\[<*-klasse*>. \] < *untergeordnetes Konstrukt*>

Verwendung: Wenn der **Propagated-Qualifizierer** verwendet wird, muss der Schlüsselqualifizierer mit dem Wert TRUE angegeben **werden.** [](key-qualifier.md)

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>**Lesen**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Eigenschaften

Gibt an, ob die Eigenschaft lesbar ist. Der Standardwert ist **TRUE.**

</dd> <dt>

<span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Erforderlich**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Eigenschaften

Gibt an, ob für die Eigenschaft ein Wert erforderlich ist, der nicht NULL ist. Der Standardwert ist **FALSE.**

</dd> <dt>

<span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Revision**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Klassen, Zuordnungen, Hinweise, Schemas

Nebenrevisionsnummer des Schemaobjekts. Der Standardwert ist **NULL.**

Verwendung: Der **Versionsqualifizierer** muss vorhanden sein, um die Hauptversionsnummer bei Verwendung des Revisionsqualifizierers zu verwenden. 

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Schema**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Eigenschaften, Methoden

Name des Schemas, in dem das Feature definiert ist. Der Standardwert ist **NULL.**

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Quelle**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Klassen, Zuordnungen, Hinweise, Verweise

Speicherort einer Instanz. Der Standardwert ist **NULL.**

Der Wert des Qualifizierers ist <*Namespacetyp>://<* *namespacehandle>.*

Verwendung: Der **Quellqualifizierer** kann nicht mit dem **SourceType-Qualifizierer** verwendet werden.

</dd> <dt>

<span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**Sourcetype**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Klassen, Zuordnungen, Hinweise, Verweise

Typ des Speicherorts einer Instanz. Der Wert dieses Qualifizierers ist <*Namespacetyp>.* Der Standardwert ist **NULL.**

Verwendung:  Der SourceType-Qualifizierer kann nicht mit dem **Quellqualifizierer** verwendet werden.

</dd> <dt>

<span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsErzeugen**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Klassen

Gibt an, ob die -Klasse die Erstellung von -Instanzen unterstützt. Der Standardwert ist **FALSE.**

</dd> <dt>

<span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Klassen

Gibt an, ob die -Klasse das Löschen von -Instanzen unterstützt. Der Standardwert ist **FALSE.**

</dd> <dt>

<span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Klassen

Gibt an, ob die -Klasse die Änderung (Aktualisierung) von -Instanzen unterstützt. Der Standardwert ist **FALSE.**

</dd> <dt>

<span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Terminal**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Klassen

Gibt an, ob die Klasse Unterklassen haben kann. Der Standardwert ist **FALSE.**

Wenn eine Unterklasse deklariert wird, generiert der Compiler einen Fehler.

Verwendung: Dieser Qualifizierer darf nicht mit dem **Abstract-Qualifizierer** koexistieren. Wenn sowohl die **Terminal-** als auch die Abstract-Qualifizierer angegeben sind, generiert der Compiler einen Fehler. 

</dd> <dt>

<span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Einheiten**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Eigenschaften, Methoden, Parameter

Typ der Einheit, in der das zugeordnete Datenelement ausgedrückt wird. Der Standardwert ist **NULL.**

Beispielsweise kann ein Größendatenelement für Einheiten den Wert "bytes" **haben.**

</dd> <dt>

<span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**
</dt> <dd>

Datentyp: **Zeichenfolgenarray**

Gilt für: Eigenschaften, Methoden, Parameter

Satz zulässiger Werte für eine Eigenschaft, einen Methoden-Rückgabetyp oder einen Methodenparameter. Der Standardwert ist **NULL.**

Verwendung: Dieser Qualifizierer kann allein oder in Kombination mit dem **Values-Qualifizierer** verwendet werden. Bei Verwendung in  Kombination mit dem Values-Qualifizierer stellt die Position des Werts im **ValueMap-Array** die Position des entsprechenden Eintrags im **Values-Array** zur Auswahl. Verwenden Sie den ValueMap-Qualifizierer nur mit Zeichenfolgen- und Ganzzahlwerten.  Die Syntax für die Darstellung eines ganzzahligen Werts im Wertzuordnungsarray ist \[ + \| = \] die \[ \* Ziffernziffer \] . Der Inhalt, die maximale Anzahl von Ziffern und der dargestellte Wert werden durch den Typ der zugeordneten Eigenschaft eingeschränkt. Beispielsweise darf uint8 nicht signiert sein, muss kleiner als vier Ziffern sein und muss einen Wert kleiner als 256 darstellen.

</dd> <dt>

<span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Werte**
</dt> <dd>

Datentyp: **Zeichenfolgenarray**

Gilt für: Eigenschaften, Methoden, Parameter

Satz von Werten, die einen ganzzahligen Wert in eine zugeordnete Zeichenfolge übersetzen. Der Standardwert ist **NULL.**

Diese Eigenschaft gibt auch ein Array von Zeichenfolgenwerten an, die einer Enumerationseigenschaft zugeordnet werden sollen. Dieser Qualifizierer kann entweder auf eine ganzzahlige Eigenschaft oder eine Zeichenfolgeneigenschaft angewendet werden, und die Zuordnung kann implizit oder explizit sein. Wenn die Zuordnung implizit ist, stellen Ganzzahl- oder Zeichenfolgeneigenschaftswerte Ordnungspositionen im **Values-Array** dar. Wenn die Zuordnung explizit ist, muss die Eigenschaft eine ganze Zahl sein,  und gültige Eigenschaftswerte werden im Array aufgeführt, das durch den ValueMap-Qualifizierer definiert wird. Weitere Informationen finden Sie unter [Wertzuordnung.](value-map.md)

Wenn kein ValueMap-Qualifizierer vorhanden ist, wird das **Values-Array** mithilfe des Werts in der zugeordneten Eigenschaft, dem Rückgabetyp der Methode oder dem Methodenparameter indiziert (null relativ).  Wenn  ein ValueMap-Qualifizierer vorhanden ist, wird der Werteindex durch die Position des Eigenschaftswerts in der Wertzuordnung definiert.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Klassen, Schemas, Zuordnungen, Hinweise

Hauptversionsnummer des Schemaobjekts. Der Standardwert ist **NULL.** Die Versionsnummer wird erhöht, wenn Änderungen am Schema vorgenommen werden, die die Schnittstelle ändern.

</dd> <dt>

<span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Schwach**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Verweise

Gibt an, ob die Schlüssel der Klasse, auf die verwiesen wird, die Schlüssel der anderen Teilnehmer in der Zuordnung enthalten. Der Standardwert ist **FALSE.**

Dieser Qualifizierer wird verwendet, wenn die Identität der Klasse, auf die verwiesen wird, von der Identität der anderen Teilnehmer in der Zuordnung abhängt. Nicht mehr als ein Verweis auf eine bestimmte Klasse kann schwach sein. Die anderen Klassen in der Zuordnung müssen einen Schlüssel definieren. Die Schlüssel der anderen Klassen in der Zuordnung werden in der Klasse, auf die verwiesen wird, wiederholt und mit einem **propagierten Qualifizierer** gekennzeichnet.

</dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Schreiben**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Eigenschaften

Gibt an, dass Anwendungen oder Skripts den Eigenschaftswert ändern können. Das Konto, unter dem die Anwendung ausgeführt wird, muss Zugriff auf den Namespace haben, der Instanzen der -Klasse enthält. Die Anbieterimplementierung kann auch den Zugriff auf Anbieterdaten einschränken. Der Wert **TRUE gibt an,** dass die Eigenschaft für Benutzer lesbar und schreibbar ist, denen der Zugriff durch WMI und den Anbieter gestattet wird. Der Standardwert ist **FALSE.**

Eine Eigenschaft ohne **Schreibqualifizierer** kann möglicherweise weiterhin geschrieben werden. Die Anbieterimplementierung lässt möglicherweise zu, dass alle  Eigenschaften in den Anbieterklassen geändert werden, unabhängig davon, ob der Schreibqualifizierer vorhanden ist.

</dd> <dt>

<span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Eigenschaften

Gibt an, ob die Eigenschaft bei der Instanzerstellung schreibbar ist. Dieser Qualifizierer kann in Verbindung mit dem **WriteAtCreate-Qualifizierer** verwendet werden. Der Standardwert ist **FALSE.**

</dd> <dt>

<span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Eigenschaften

Gibt an, ob die Eigenschaft beim Instanzupdate schreibbar ist. Dieser Qualifizierer kann in Verbindung mit dem **WriteAtCreate-Qualifizierer** verwendet werden. Der Standardwert ist **FALSE.**

</dd> </dl>

## <a name="examples"></a>Beispiele

Weitere Informationen zum Abrufen von Qualifizierern finden Sie im [PowerShell-Codebeispiel Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) im TechNet-Katalog.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[WMI-Qualifizierer](wmi-qualifiers.md)
</dt> <dt>

[Hinzufügen eines Qualifizierers](adding-a-qualifier.md)
</dt> </dl>

 

 




