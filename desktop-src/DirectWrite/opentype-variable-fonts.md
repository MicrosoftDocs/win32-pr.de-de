---
title: OpenType-Variablenschriftarten
description: In diesem Thema werden OpenType-Variablen Schriftarten, ihre Unterstützung in DirectWrite und Direct2D und deren Verwendung in Ihrer APP beschrieben. .
ms.assetid: 788558a7-efe7-b075-942f-ac75a5b86b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a9e6bdf27da0d70841973515636736859294dd
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "103869348"
---
# <a name="opentype-variable-fonts"></a>OpenType-Variablenschriftarten

In diesem Thema werden OpenType-Variablen Schriftarten, ihre Unterstützung in DirectWrite und Direct2D und deren Verwendung in Ihrer APP beschrieben. 

-   [Was sind OpenType-Variablen Schriftarten?](#what-are-opentype-variable-fonts)
-   [OpenType-Variablen Schriftart Unterstützung in DirectWrite](#opentype-variable-font-support-in-directwrite)
-   [Verwenden von OpenType-Variablen Schriftarten](#using-opentype-variable-fonts)

## <a name="what-are-opentype-variable-fonts"></a>Was sind OpenType-Variablen Schriftarten?

In Version 1,8 der [OpenType-Schriftart Format Spezifikation](https://www.microsoft.com/typography/otspec/) wurde eine neue Erweiterung in das Format eingeführt, das als [OpenType-Schriftart Variationen](/typography/opentype/spec/otvaroverview)bezeichnet wird. Schriftarten, die diese Erweiterungen verwenden, werden als OpenType-Variablen Schriftarten bezeichnet. Eine OpenType-Variablen Schriftart ist eine einzelne Schriftart, die sich wie mehrere Schriftarten Verhalten kann, indem Sie die fortlaufende Interpolationen zwischen verschiedenen Entwürfen verwendet, die alle innerhalb der einzelnen Schriftart definiert sind.

Eine OpenType-Variablen Schriftart kann eine fortlaufende Variation des Entwurfs an einer oder mehreren unabhängigen Achsen wie Gewichtung oder Breite definieren: 

 

![Zeigt eine OpenType-Variablen Schriftart mit dem Buchstaben "G" an und zeigt verschiedene Variationen entlang einer horizontalen breiten Achse und einer vertikalen Gewichtungs Achse an.](images/opentype-width-weight.png)

Ein Schriftart Entwickler bestimmt einen Satz von Variations Achsen, der in einer angegebenen Schriftart verwendet werden soll. Diese Achsen können eine Reihe von bekannten (oder "registrierten") Achsen von Variationen enthalten, wie z. b. Gewichtung und Breite, aber Sie können auch beliebige, benutzerdefinierte Achsen von Variationen enthalten, die vom Schriftart Entwickler definiert werden.  

Durch Auswahl eines Satzes von Variations Achsen für eine Schriftart definiert der Schriftart Entwickler einen abstrakten, n-dimensionalen Bereich der Entwurfs Variation für die Schriftart. Text-Engines können eine beliebige Position oder "Instance" innerhalb dieses kontinuierlichen Raums zum Anordnen und Rendern von Text angeben. 

Der Schriftart Entwickler kann auch bestimmte Instanzen innerhalb des Entwurfs Variations Raums auswählen und Namen zuweisen. Diese werden als "benannte Instanzen" bezeichnet. Beispielsweise kann eine Schriftart mit Gewichtungs Abweichung eine fortlaufende Variation zwischen sehr hellen und sehr hohen Strichen unterstützen, während der Schriftart Entwickler bestimmte Gewichtungen entlang dieses Kontinuums ausgewählt hat und ihm Namen zugewiesen hat, wie z. b. "Light", "Regular" und "Semibold". 

Das Format der OpenType-Variablen Schriftart verwendet Datentabellen, die in herkömmlichen OpenType-Schriftarten enthalten sind, sowie bestimmte zusätzliche Tabellen, die beschreiben, wie sich die Werte verschiedener Datenelemente für verschiedene Instanzen ändern. Das Format gibt eine Variation-Instanz als "Standard Instanz" an, die herkömmliche Tabellen verwendet, um Standardwerte zu erhalten. Alle anderen Instanzen sind von den Standarddaten und anderen Delta Daten abhängig. Beispielsweise kann eine "glyf"-Tabelle eine Bezier-Kurven Beschreibung einer nominalen Glyphe-Form aufweisen, die für die Standard Instanz verwendet wird, während eine "gvar"-Tabelle beschreibt, wie die Bezier-Steuerpunkte für das Symbol für andere Instanzen angepasst werden. Ebenso können andere Schriftart Werte einen nominalen Wert und Delta Daten aufweisen, die beschreiben, wie sich diese Werte für verschiedene Instanzen ändern. z. b. x-Height und andere Schriftart weite Metriken oder Symbol spezifische Markierungen zur Markierung und Markierung. 

Da Variablen Schriftarten einen beliebigen Satz von Variationen von Variationen unterstützen können, benötigen Sie ein erweiterbares Modell von Schriftfamilien, das direkt widerspiegelt, wie Schriftart-Designer Schriftarten von Schriftarten erstellen: eine Schriftfamilie wird durch einen Familiennamen und bestimmte Entwurfs Merkmale definiert, die konstant sind, und eine beliebige Zahl (vom Schriftart Entwickler festgelegt), mit der der Entwurf variieren kann. Eine Schriftfamilie kann mit Varianten für Gewichtung erstellt werden, aber es kann eine andere Schriftfamilie mit Varianten für x-Height, Serif-Size, "Funkiness" oder was von der Schriftart Entwickler Wunsch erstellt werden. In diesem Modell wird eine Schriftart Auswahl am besten mit dem allgemeinen oder "bevorzugten" oder "Typographic", dem Familiennamen und einem Satz von Schlüssel-Wert-Paaren, die jeweils eine Art von Variation und einem bestimmten Wert darstellen, beschrieben, wobei die Arten der Variation im Allgemeinen eine erweiterbare Menge darstellen. Dieses allgemeine Konzept einer Schriftfamilie kann auf herkömmliche, nicht Variablen Schriftarten sowie auf Variablen Schriftarten angewendet werden. Beispielsweise kann die Familie "Selawik VF" unter diesem allgemeinen typografiefamilienmodell Variationen der Gewichtung, der optischen Größe und des Serif-Entwurfs mit Instanzen wie "menoutbanner Sans" aufweisen. 

Einige vorhandene Software Implementierungen, einschließlich vorhandener DirectWrite-APIs, können jedoch mit einem eingeschränkteren Modell von Schriftfamilien entworfen werden. Einige Anwendungen können z. b. davon ausgehen, dass eine Schriftfamilie höchstens reguläre, Fett, kursiv und Fett formatierte Varianten haben kann. Die vorhandenen [**idwrite-FontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) -und [**idwrite-FontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) -Schnittstellen nehmen ein Gewichtungs-/streckungs-/Stil-Familienmodell ("WSS"), das die Angabe von Varianten innerhalb einer Familie mithilfe der [**Schrift Breite dwrite \_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight), der [**dwrite-Schriftart \_ \_ Streckung**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) oder der [**dwrite \_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) -Enumerationen als Parameter ermöglicht. Im vorherigen Beispiel werden die optischen Größe und die Serif-Achsen nicht als familieninterne Achsen Variationen im WSS-Modell behandelt. 

Die umfassende Unterstützung für Variablen Schriftarten erfordert APIs, die es ermöglichen, dass ein Familienmitglied mit potenziell mehreren Parametern angegeben werden kann, wie von der Schriftart festgelegt. Vorhandene API-Entwürfe können jedoch partielle Unterstützung für Variablen Schriftarten bieten, indem die benannten Instanzen, die in einer Variablen Schriftart definiert sind, in die stärker begrenzten Schriftfamilien Modelle projiziert werden. Im vorherigen Beispiel konnte "Selawik VF-alight Banner Sans" in das WSS-Modell als "Selawik VF Banner Sans"-Familie mit "menmilight" als Gewichtungs Variante projiziert werden. 

Ein weiteres Beispiel ist eine typografische Schriftfamilie wie Sitka mit Gewichtungs-und optischen Größen Varianten. Benannte Varianten innerhalb der Familie umfassen Sitka Text Regular und Sitka Banner Bold (plus viele weitere). Der typografiefamilienname ist "Sitka", während die Gesichts Namen für diese Varianten im typografischen Familienmodell "Text Regular" und "Banner Bold" lauten. Die vier-und WSS-Familienmodelle lassen keine Varianten der optischen Größe innerhalb einer Familie zu, sodass die Unterschiede bei der optischen Größe wie Unterschiede auf Familienebene behandelt werden müssen. In der folgenden Tabelle wird veranschaulicht, wie eine Auswahl von Schriftarten aus der Sitka typografische-Familie im WSS-Familienmodell behandelt wird: 



Typografisches Familienmodell

WSS-Familienmodell

Familie

Gesichtserkennung

Familie

Gesichtserkennung

Sitka

Regulärer Text

Sitka-Text

Regulär

Sitka

Banner Fett

Sitka-Banner

Fett

Sitka

Beschriftung kursiv

Sitka-Beschriftung

Kursiv



 

Die Projektion von Namen aus einem typografischen Familienmodell zum WSS-Familienmodell kann auf nicht-Variablen Schriftarten und auf die benannten Instanzen von Variablen Schriftarten angewendet werden. Dies kann jedoch nicht für andere, nicht benannte Instanzen aus dem fortlaufenden Entwurfs Variationsbereich einer Variablen Schriftart erfolgen. Aus diesem Grund erfordert die Unterstützung für die gesamte Funktionalität von Variablen Schriftarten APIs, die für den Verweis auf Gesichter innerhalb einer typografischen Familie in Bezug auf einen nicht eingeschränkten Satz von Variations Achsen und Achsen Werten entworfen wurden. 

## <a name="opentype-variable-font-support-in-directwrite"></a>OpenType-Variablen Schriftart Unterstützung in DirectWrite

Ab der Veröffentlichung von Windows 10 Creators Update ist das Schriftformat der OpenType-Variablen weiterhin sehr neu, und Schriftart Hersteller, Plattformen und apps werden noch immer das neue Format implementieren. Dieses Update bietet eine anfängliche Implementierung für dieses Format in DirectWrite. 

DirectWrite-internale wurden aktualisiert, um OpenType-Variablen Schriftarten zu unterstützen. Mithilfe der aktuellen APIs bietet diese Unterstützung für alle benannten Instanzen einer Variablen Schriftart. Diese Unterstützung kann für komplette Workflows verwendet werden – von der Enumeration der benannten Instanzen, der Auswahl einer benannten Instanz, der Verwendung von Layout und Strukturierung bis hin zum Rendern und drucken. Der Vorteil von apps, die auch GDI-Text Interop für bestimmte Vorgänge verwenden, wurde in vorhandenen GDI-APIs ebenfalls hinzugefügt. 

In Windows 10 Creators Update unterstützt DirectWrite keine beliebigen Instanzen, die die Funktion zur kontinuierlichen Variation von Variablen Schriftarten nutzen.

In vielen Vorgängen kann das Verhalten von benannten Instanzen einer Variablen Schriftart in DirectWrite nicht vom Verhalten nicht variabler Schriftarten unterschieden werden. Und da die Unterstützung mithilfe vorhandener DirectWrite-APIs bereitgestellt wird, können die benannten Instanzen von Variablen Schriftarten sogar in vielen vorhandenen DirectWrite-apps ohne Änderungen funktionieren. Ausnahmen können jedoch in bestimmten Situationen zutreffen:  

-   , Wenn eine APP Schriftart Daten direkt für bestimmte Vorgänge verarbeitet. Wenn z. b. eine APP Glyphe in der Schriftart Datei direkt aus der Schriftart Datei liest, um bestimmte visuelle Effekte zu erstellen.
-   Wenn eine APP für bestimmte Vorgänge eine Bibliothek eines Drittanbieters verwendet. Wenn eine App z. b. DirectWrite für das Layout verwendet, um abschließende Symbol Indizes und Positionen zu erhalten, wird dann eine Drittanbieter Bibliothek zum Rendern verwendet.
-   Wenn eine APP Schriftart Daten in ein Dokument einbettet oder auf andere Weise Schriftart Daten an einen downstreamprozess übergibt.

Wenn Vorgänge mit Implementierungen ausgeführt werden, die keine Variablen Schriftarten unterstützen, führen diese Vorgänge möglicherweise nicht zu den erwarteten Ergebnissen. Beispielsweise können Symbol Positionen für eine benannte Instanz der Variablen Schriftart berechnet werden, aber die Symbole werden möglicherweise mit einer anderen benannten Instanz gerendert. Abhängig von der Anwendungs Implementierung können Ergebnisse in einigen Kontexten, aber nicht in anderen Kontexten funktionieren, in denen andere Bibliotheken verwendet werden können. Beispielsweise kann Text auf dem Bildschirm ordnungsgemäß angezeigt werden, jedoch nicht, wenn er gedruckt wird. Wenn End-to-End-Workflows nur mit DirectWrite implementiert werden, kann das richtige Verhalten für benannte Instanzen einer Variablen Schriftart erwartet werden. 

Da vorhandene DirectWrite-APIs die Gesichts Auswahl mithilfe des Gewichtungs-/streckungs-/stilmodells unterstützen, werden die benannten Instanzen von Schriftarten, die andere Schnittstellen verwenden, vom allgemeinen typografischen Familienmodell in das WSS-Modell projiziert, wie oben beschrieben. Dies basiert auf einer Variablen Schriftart, die eine "style Attribute"-Tabelle ("stat") mit Achsen-Wert-unter Tabellen enthält, die von dwrite verwendet werden, um die Gesichts Namen Token zu unterscheiden, die Attribute für Gewichtung, Streckung oder Stile von Token, die andere Schnittstellen der Variation betreffen, bestimmen.  

Wenn eine Variablen Schriftart keine "stat"-Tabelle enthält, wie dies für die Variablen Schriftarten durch die OpenType-Spezifikation erforderlich ist, behandelt DirectWrite die Schriftart als nicht Variablen Schriftart, die nur die Standard Instanz enthält.  

Wenn eine Schriftart eine Tabelle ' stat ' enthält, aber keine entsprechenden Achsen Wert-unter Tabellen enthält, kann dies zu unerwarteten Ergebnissen führen, z. b. Wenn mehrere Gesichter mit identischen Gesichts Namen vorhanden sind. Diese Schriftarten werden zurzeit nicht unterstützt. 

Die OpenType-Spezifikation ermöglicht das darstellen von Symbol Gliederungs Daten in einem von zwei Formaten: das Verwenden einer "glyf"-Tabelle, die das TrueType-Gliederung-und-Hinweise-Format verwendet, oder das Verwenden einer CFF-Tabelle, in der die Darstellung des Compact-Schriftart Formats ("CFF") verwendet wird. In einer Variablen Schriftart mit TrueType-Gliederungen wird die Tabelle "glyf" weiterhin verwendet und mit einer "gvar"-Tabelle ergänzt, die die Variations Daten für die Kontur bereitstellt. Dies bedeutet, dass die Standard Instanz einer Variablen Schriftart mit TrueType-Gliederungen nur herkömmliche OpenType-Tabellen verwendet, die in älteren Software unterstützt werden, die keine Unterstützung für unterschiedliche Schriftarten aufweist. In einer Variablen Schriftart mit CFF-gliedern wird jedoch die Tabelle "CFF" durch die Tabelle "CFF2" abgelöst, die die Standard Gliederungs Daten und die zugehörigen Variations Daten in einer Tabelle kapselt. CFF-Daten werden von einem separaten Raster aus verarbeitet, der für TrueType-Daten verwendet wird, und für eine "CFF2"-Tabelle ist ein aktualisierter CFF-Raster mit "CFF2"-Unterstützung erforderlich. Eine ' CFF2 '-Tabelle kann nicht von älteren CFF-rasterizern verarbeitet werden. Bei einer Variablen Schriftart mit CFF-Gliederungs Daten bedeutet dies, dass auch die Standard Instanz in älterer Software nicht funktioniert. 

In Windows 10 Creators Update unterstützt DirectWrite keine Variablen Schriftarten mit CFF-Gliederungs Daten mithilfe der Tabelle "CFF2". 

## <a name="using-opentype-variable-fonts"></a>Verwenden von OpenType-Variablen Schriftarten

OpenType-Variablen Schriftarten können einfach zu verwenden sein, wobei die oben aufgeführten aktuellen Einschränkungen beachtet werden: 

-   Zurzeit werden nur benannte Instanzen einer Variablen Schriftart unterstützt.
-   Zurzeit werden nur Variablen Schriftarten unterstützt, die TrueType-Glyphe-Daten (keine CFF-Gliederung) verwenden. 
-   Für Schriftarten, die Achsen mit anderen Entwurfs Variationen als Gewichtung, Streckung oder Stil verwenden, werden benannte Instanzen in das WSS-Familienmodell projiziert, was dazu führen kann, dass einige benannte Instanzen als separate Familien angezeigt werden (wie in der Vergangenheit bei nicht Variablen Schriftarten Vorkommen). Um dies zu unterstützen, müssen Variablen Schriftarten eine Tabelle "stat" aufweisen, die entsprechende Achsen Wert-unter Tabellen enthält.
-   Benannte Instanzen von Variablen Schriftarten werden in DirectWrite-APIs unterstützt. Wenn jedoch bestimmte Vorgänge in älteren Implementierungen ausgeführt werden, die keine Variablen Schriftarten unterstützen, kann dies zu falschen Ergebnissen führen. 
-   Bestimmte DirectWrite-APIs verwenden die Schrift Breite " [**dwrite \_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)", die [**dwrite-Schriftart \_ \_ Streckung**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) und die [**dwrite \_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) -Enumerationen zum Angeben von Gewichtung, Stretch und Stil Attributen bei der Auswahl von Gesichtern. Wenn eine Variablen Schriftart entsprechende Variations Achsen verwendet, aber viele benannte Instanzen, die eine präzisere Granularität erfordern, werden nicht alle benannten Instanzen in diesen APIs auswählbar sein.

OpenType-Variablen Schriftarten, die diesen Anforderungen entsprechen, können genauso wie andere OpenType-Schriftarten von der Windows-Shell installiert werden und können auch in benutzerdefinierten Schriftart Sätzen verwendet werden, die von einer App erstellt wurden.  

Bei der Installation im System werden alle benannten Instanzen einer Variablen Schriftart in den Schriftart Satz eingeschlossen, der durch Aufrufen der IDWriteFontFamily3::[**getsystemfontset**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) -Methode zurückgegeben wird. Beachten Sie, dass ein Schriftart Satz eine flache Liste ohne eine Hierarchie von Familien Gruppierungen ist, aber jedes Element im Satz verfügt über eine Family-Name-Eigenschaft, die auf dem WSS-Familienmodell basiert. Der Schriftart Satz kann mithilfe der [**idwrite-FONTSET:: getmatchingfonts**](idwritefontset-getmatchingfonts-overload.md) -Methoden für eine bestimmte benannte Instanz der Variablen Schriftart gefiltert werden. Wenn Sie jedoch die **getmatchingfonts** -Überladung verwenden, die einen familyName annimmt, muss der angegebene familyName den Namen verwenden, der mit dem WSS-Schriftfamilien Modell übereinstimmt. Die komplette Liste der mit WSS kompatiblen Familiennamen, die in einem Schriftart Satz auftreten, kann mithilfe der [**idwrite-FONTSET:: GetPropertyValues**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) -Methoden mithilfe der dwrite-Schriftart für die Schriftart-Eigenschaften-ID abgerufen werden \_ \_ \_ \_ \_ .  

Ebenso werden alle benannten Instanzen einer Variablen Schriftart in der Schriftart Auflistung dargestellt, die von der idschreitefactory::[**getsystemfontcollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) -Methode zurückgegeben wird. Da es sich bei den Elementen einer Schriftart Auflistung um Schriftfamilien handelt, die auf dem WSS-Modell basieren, können die benannten Instanzen einer Variablen Schriftart in einer Auflistung als Mitglieder von mindestens zwei Schriftfamilien dargestellt werden. Wenn die [**idwrite-FontCollection:: findfamilyname**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-findfamilyname) -Methode verwendet wird, muss der familyName-Parameter ein WSS-kompatibler Familienname sein. Um alle WSS-kompatiblen Familiennamen aus einer Schriftart Auflistung zu ermitteln, kann eine APP jede Familie durchlaufen und " [**idschreitefontfamily:: getfamilynames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames)" aufrufen, aber es ist möglicherweise einfacher, einen entsprechenden Schriftsatz zu erhalten und die [**GetPropertyValues**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) -Methode wie oben beschrieben zu verwenden. 

Bei der Arbeit mit benutzerdefinierten Schriftarten können verschiedene im Thema [benutzerdefinierte Schriftart Sätze](custom-font-sets-win10.md) beschriebene Ansätze zum Erstellen eines Schriftart Satzes verwendet werden. Zum Hinzufügen einer Variablen Schriftart zu einem benutzerdefinierten Schriftart Satz wird die [**IDWriteFontSetBuilder1:: AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) -Methode empfohlen, da Sie Variablen Schriftarten unterstützt und alle benannten Instanzen einer Variablen Schriftart in einem einzelnen-Befehl hinzufügt. Zurzeit ist es nicht möglich, einzelne benannte Instanzen einer benutzerdefinierten Variablen Schriftart einem Schriftart Satz mit den [**idwrite-fontsetbuilder:: addfontfacereferenzierungsmethoden**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) hinzuzufügen, da es keine Möglichkeit gibt, einen Schriftart Verweis zu erstellen, der angibt, welche der benannten Instanzen aus einer Variablen Schriftart Datei beabsichtigt ist. Dies bedeutet, dass es derzeit nicht möglich ist, benannte Instanzen einer benutzerdefinierten Schriftart einem benutzerdefinierten Schriftart Satz mit zugewiesenen benutzerdefinierten Eigenschaften hinzuzufügen. Dies bedeutet wiederum, dass benutzerdefinierte Variablen Schriftarten derzeit nicht in Verbindung mit DirectWrite-APIs für Remote Schriftarten verwendet werden können. Wenn benannte Instanzen einer Variablen Schriftart in einem System Schriftart Satz enthalten sind, sind die Schriftart Verweise für jede benannte Instanz bereits vorhanden, und diese können zu benutzerdefinierten Schriftart Sätzen hinzugefügt werden, einschließlich der Verwendung von benutzerdefinierten Eigenschafts Werten. Weitere Informationen finden Sie im Thema benutzerdefinierte Schriftart Sätze. 

Wenn Sie mit Variablen Schriftarten arbeiten, sind die Enumerationen für das DirectWrite-dwrite und die [**dwrite- \_ Schriftart \_ Streckung**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) eng mit den in der OpenType-Spezifikation definierten Gewichtungs Achsen für Gewichtung und Breite verbunden, sind jedoch nicht identisch. [**\_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight) Erstens unterstützt die numerische Skala für eine beliebige Variations Achse immer Bruchzahlen, während FontWeight und FontStretch ganze Zahlen verwenden. Die Größe der OpenType-Gewichtungs Achse verwendet Werte zwischen 1 und 1000, die auch von FontWeight unterstützt werden. Folglich ist die Änderung von einem Wert der Variations Gewichtungs Achse zu FontWeight relativ gering: das für eine benannte Instanz gemeldete FontWeight kann aus dem exakten Wert gerundet werden, der zum Definieren der benannten Instanz innerhalb der Schriftart verwendet wird. Der Unterschied zwischen DirectWrite FontStretch und der OpenType-Breite Achsen Skala ist größer: DirectWrite verwendet Werte von 1 bis 9 und folgt den [usWidthClass](/typography/opentype/spec/os2#uswidthclass) -Werten der OpenType OS/2-Tabelle, während die OpenType-Achse für die breiten Achse positive Werte verwendet, die einen Prozentsatz der normalen Breite darstellen. Die [Dokumentation zu](/typography/opentype/spec/os2#uswidthclass) der Dokumentation in der OpenType-Spezifikation stellt eine Zuordnung zwischen den Werten 1 bis 9 und den Prozentsatz der normalen Werte bereit. Der für eine benannte Instanz gemeldete FontStretch-Wert kann beim Umrechnen von Werten der breiten Achse eine Rundung einschließen. 

Beim Erstellen eines [**idwrite-Textformats**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)müssen eine Schriftart Auflistung und WSS-kompatible Schriftart Eigenschaften (Familienname, Gewichtung, Streckung und Stil) angegeben werden. Dies gilt auch, wenn Sie Schriftart Formatierungs Eigenschaften für einen [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Textbereich festlegen. Die Eigenschaften können aus einem [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) -Objekt oder aus [**idwrite**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) -und [**idwrite-FontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) -Objekten abgerufen werden, die eine bestimmte benannte Instanz darstellen. Wie bereits erwähnt, können die von den Methoden getweight und getstretch zurückgegebenen Werte gerundete Näherungen für die tatsächlichen Achsen Werte sein, die zum Definieren der benannten Instanz verwendet werden. DirectWrite ordnet jedoch die Kombination der Eigenschaften wieder der gewünschten benannten Instanz zu. 

Ebenso gilt: Wenn eine APP [**idschreitefontfallbackbuilder**](idwritefontfallbackbuilder.md) zum Erstellen benutzerdefinierter Schriftart-Fall Back-Daten verwendet, werden Familien für Zeichen Bereichs Zuordnungen mithilfe von WSS-kompatiblen Familiennamen angegeben. Der Schriftart-Fall Back innerhalb von DirectWrite basiert auf Familien mit DirectWrite und wählt eine Variante in einer Fall Back Familie aus, die für die Variante der Start Familie am nächsten liegt. Für Varianten, die andere Dimensionen als Gewichtung, Streckung und Stil enthalten, wäre DirectWrite derzeit nicht in der Lage, solche Varianten innerhalb einer Fall Back Familie auszuwählen, es sei denn, es wurden benutzerdefinierte Fall Back Daten erstellt, um Fall Back Zuordnungen für Familien bereitzustellen, die über bestimmte nicht-WSS-Attribute verfügen, wie z. b. die Varianten der optischen Größe "

 

 