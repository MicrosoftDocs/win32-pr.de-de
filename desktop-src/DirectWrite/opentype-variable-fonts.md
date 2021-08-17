---
title: OpenType-Variablenschriftarten
description: In diesem Thema werden OpenType-Variablenschriftarten, ihre Unterstützung in DirectWrite und Direct2D sowie deren Verwendung in Ihrer App beschrieben. .
ms.assetid: 788558a7-efe7-b075-942f-ac75a5b86b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c671bebce73cf3bdec42d1f7f570add914db7eb33b8a6bfd1b196d569b9975d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649392"
---
# <a name="opentype-variable-fonts"></a>OpenType-Variablenschriftarten

In diesem Thema werden OpenType-Variablenschriftarten, ihre Unterstützung in DirectWrite und Direct2D sowie deren Verwendung in Ihrer App beschrieben. 

-   [Was sind OpenType-Variablenschriftarten?](#what-are-opentype-variable-fonts)
-   [OpenType-Variablenschriftartunterstützung in DirectWrite](#opentype-variable-font-support-in-directwrite)
-   [Verwenden von OpenType-Variablenschriftarten](#using-opentype-variable-fonts)

## <a name="what-are-opentype-variable-fonts"></a>Was sind OpenType-Variablenschriftarten?

In Version 1.8 der Spezifikation für das [OpenType-Schriftformat](https://www.microsoft.com/typography/otspec/) wurde eine neue Erweiterung für das Format eingeführt, das als [OpenType-Schriftartvariationen](/typography/opentype/spec/otvaroverview)bezeichnet wird. Schriftarten, die diese Erweiterungen verwenden, werden als OpenType-Variablenschriftarten bezeichnet. Eine OpenType-Variablenschriftart ist eine einzelne Schriftart, die sich wie mehrere Schriftarten verhalten kann, indem kontinuierliche Interpolation zwischen verschiedenen Designs verwendet wird, die alle innerhalb der einzelnen Schriftart definiert sind.

Eine OpenType-Variablenschriftart kann fortlaufende Variationen ihres Entwurfs entlang einer oder mehrerer unabhängiger Achsen definieren, z. B. Gewichtung oder Breite: 

 

![Zeigt eine OpenType-Variablenschriftart mit dem Buchstaben "G" an und zeigt verschiedene Variationen entlang einer horizontalen Breitenachse und einer vertikalen Gewichtungsachse an.](images/opentype-width-weight.png)

Ein Schriftartentwickler bestimmt eine Reihe von Variationsachsen, die in einer bestimmten Schriftart verwendet werden sollen. Diese Achsen können eine Reihe bekannter (oder "registrierter") Variationsachsen wie Gewichtung und Breite enthalten, aber sie können auch beliebige, benutzerdefinierte Variationsachsen enthalten, die vom Schriftartentwickler definiert werden.  

Durch Auswahl eines Satzes von Variationsachsen für eine Schriftart definiert der Schriftartentwickler einen abstrakten, n-dimensionalen Bereich der Entwurfsvariation für die Schriftart. Text-Engines können potenziell eine beliebige Position oder "Instanz" innerhalb dieses kontinuierlichen Leerzeichens angeben, um Text zu erstellen und zu rendern. 

Der Schriftartentwickler kann auch Namen für bestimmte Instanzen innerhalb des Entwurfsvariationsbereichs auswählen und zuweisen. diese werden als "benannte Instanzen" bezeichnet. Beispielsweise kann eine Schriftart mit Gewichtungsvariation eine kontinuierliche Variation zwischen sehr einfachen und sehr starken Strichen unterstützen, während der Schriftentwickler bestimmte Gewichtungen entlang dieses Kontinuums ausgewählt und ihnen Namen wie "Light", "Regular" und "Semibold" zugewiesen hat. 

Das Schriftartformat der OpenType-Variablen verwendet Datentabellen in herkömmlichen OpenType-Schriftarten sowie bestimmte zusätzliche Tabellen, die beschreiben, wie sich die Werte verschiedener Datenelemente für verschiedene Instanzen ändern. Das Format legt eine Variationsinstanz als "Standardinstanz" fest, die herkömmliche Tabellen verwendet, um Standardwerte abzurufen. Alle anderen Instanzen hängen von den Standarddaten und anderen Deltadaten ab. Eine "glyf"-Tabelle kann z. B. eine Bezierkurvenbeschreibung einer nominalen Glyphenform aufweisen. Dies ist die Form, die für die Standardinstanz verwendet wird, während eine GVAR-Tabelle beschreibt, wie die Béziersteuerpunkte für das Glyphen für andere Instanzen angepasst werden. Auf ähnliche Weise können andere Schriftartwerte einen nominalen Wert plus Deltadaten aufweisen, die beschreiben, wie sich diese Werte für verschiedene Instanzen ändern. z. B. x-Höhe und andere schriftartweite Metriken oder Glyphenspezifische Markierungsankerpositionen und Kerninganpassungen. 

Da variable Schriftarten einen beliebigen Satz von Variationsachsen unterstützen können, erfordern sie ein erweiterbares Modell von Schriftfamilien, das die Art und Weise, in der Schriftarten-Designer Schriftarten erstellen, direkter widerspiegelt: Eine Schriftfamilie wird durch einen Familiennamen und bestimmte, konstante Entwurfsmerkmale definiert, mit einer beliebigen Zahl (bestimmt durch den Schriftartentwickler), in der der Entwurf variieren kann. Eine Schriftfamilie kann mit Varianten für die Gewichtung erstellt werden, aber eine andere Schriftfamilie kann mit Varianten für x-Höhe, Serifgröße, "Funkiness" oder was auch immer der Schriftentwickler möchte. In diesem Modell wird eine Auswahl des Schriftartengesichts am besten mit dem allgemeinen oder "bevorzugten" oder "typografischen" Namen und einem Satz von Schlüssel-Wert-Paaren beschrieben, die jeweils eine Art von Variation und einen bestimmten Wert darstellen, wobei die Arten von Variationen im Allgemeinen eine erweiterbare Menge sind. Dieses allgemeine Konzept einer Schriftfamilie kann sowohl für herkömmliche, nicht variable Schriftarten als auch für variable Schriftarten gelten. Bei diesem allgemeinen typografischen Familienmodell kann eine Familie "Selawik VF" variationen hinsichtlich Gewicht, optischer Größe und Serifendesign aufweisen, mit Instanzen wie "Semilight Banner Sans". 

Einige vorhandene Softwareimplementierungen, einschließlich vorhandener DirectWrite-APIs, können jedoch unter der Annahme eines eingeschränkteren Modells von Schriftfamilien entworfen werden. Einige Anwendungen gehen beispielsweise davon aus, dass eine Schriftfamilie höchstens die Varianten Regular, Bold, Italic und Bold Italic aufweisen kann. Die vorhandenen [**Schnittstellen IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) und [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) setzen ein Gewichtungs-/Stretch/Style-Familienmodell ("WSS") voraus, sodass Varianten innerhalb einer Familie mithilfe der [**DWRITE \_ FONT \_ WEIGHT-,**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight) [**DWRITE \_ FONT \_ STRETCH-**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) oder [**DWRITE \_ FONT \_ STYLE-Enumerationen**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) als Parameter angegeben werden können. Im vorherigen Beispiel würden die optische Größe und die Serifenachsen nicht als familieninterne Variationsachsen im WSS-Modell behandelt werden. 

Die vollständige Unterstützung für variable Schriftarten erfordert APIs, die es ermöglichen, ein Familienmitglied mit potenziell mehreren Parametern anzugeben, wie von der Schriftart bestimmt. Vorhandene API-Entwürfe können jedoch teilweise Unterstützung für Variablenschriftarten bereitstellen, indem die benannten Instanzen, die in einer Variablenschriftart definiert sind, in die eingeschränkteren Schriftfamilienmodelle projiziert werden. Im vorherigen Beispiel konnte "Selawik VF Semilight Banner Sans" als "Selawik VF Banner Sans"-Familie mit "Semilight" als Gewichtungsvariante in das WSS Modell projiziert werden. 

Ein weiteres Beispiel ist eine typografische Schriftfamilie wie Sitka mit Varianten von Gewichtung und optischer Größe. Zu den benannten Varianten innerhalb der Familie gehören Sitka Text Regular und Sitka Banner Bold (und viele andere). Der typografische Familienname ist "Sitka", während die Gesichtsnamen für diese Varianten im typografischen Familienmodell "Text Regular" und "Banner Bold" wären. Die Modelle mit vier Mitgliedern und WSS-Familie lassen keine optischen Größenvarianten innerhalb einer Familie zu. Daher müssen optische Größenunterscheidungen wie Unterscheidungen auf Familienebene behandelt werden. Die folgende Tabelle veranschaulicht, wie eine Auswahl von Schriftarten aus der typografischen Sitka-Familie im WSS-Familienmodell behandelt wird: 



Typografisches Familienmodell

WSS-Familienmodell

Familie

Gesicht

Familie

Gesicht

Sitka

Regulärer Text

Sitka-Text

Regulär

Sitka

Banner fett formatiert

Sitka-Banner

Fett

Sitka

Beschriftung italisch

Sitka-Beschriftung

Kursiv



 

Die Projektion von Namen aus einem typografischen Familienmodell auf das WSS Familienmodell kann auf nicht variable Schriftarten und auf die benannten Instanzen von Variablenschriftarten angewendet werden. Dies kann jedoch nicht für andere, nicht benannte Instanzen aus dem fortlaufenden Entwurfsvariationsbereich einer Variablenschriftart erfolgen. Aus diesem Grund erfordert die Unterstützung der vollständigen Funktionalität variabler Schriftarten APIs, die auf Gesichter innerhalb einer typografischen Familie im Hinblick auf einen uneingeschränkten Satz von Variationsachsen und Achsenwerten verweisen. 

## <a name="opentype-variable-font-support-in-directwrite"></a>OpenType-Variablenschriftartunterstützung in DirectWrite

Ab der Veröffentlichung des Windows 10 Creators Update ist das OpenType-Variablenschriftformat noch sehr neu, und Schriftartanbieter, Plattformen und Apps sind noch dabei, das neue Format zu implementieren. Dieses Update stellt die erste Implementierung für dieses Format in DirectWrite bereit. 

DirectWrite Internals wurden aktualisiert, um OpenType-Variablenschriftarten zu unterstützen. Mit aktuellen APIs bietet dies Unterstützung für alle benannten Instanzen einer Variablenschriftart. Diese Unterstützung kann für vollständige Workflows verwendet werden – von der Enumeration der benannten Instanzen, der Auswahl einer benannten Instanz, der Verwendung beim Layout und der Strukturierung bis hin zum Rendern und Drucken. Für Apps, die auch GDI-Text interop für bestimmte Vorgänge verwenden, wurde eine ähnliche Unterstützung auch in vorhandenen GDI-APIs hinzugefügt. 

Im Windows 10 Creators Update unterstützt DirectWrite keine beliebigen Instanzen, die die Funktion für kontinuierliche Variation variabler Schriftarten nutzen.

In vielen Vorgängen kann das Verhalten in DirectWrite benannter Instanzen einer Variablenschriftart nicht vom Verhalten nicht variabler Schriftarten unterschieden werden. Da unterstützung mit vorhandenen DirectWrite-APIs bereitgestellt wird, können die benannten Instanzen von variablen Schriftarten sogar in vielen vorhandenen DirectWrite-Apps ohne Änderungen funktionieren. Ausnahmen können jedoch in bestimmten Situationen gelten:  

-   Wenn eine App Schriftartdaten direkt für bestimmte Vorgänge verarbeitet. Wenn eine App beispielsweise Glyphengliederungsdaten direkt aus der Schriftartdatei liest, um bestimmte visuelle Effekte zu erstellen.
-   Wenn eine App eine Drittanbieterbibliothek für bestimmte Vorgänge verwendet. Wenn eine App beispielsweise DirectWrite für das Layout verwendet, um endgültige Glyphenindizes und Positionen abzurufen, verwendet dann jedoch eine Drittanbieterbibliothek für das Rendering.
-   Wenn eine App Schriftartdaten in ein Dokument einbettet oder auf andere Weise Schriftartdaten an einen Downstreamprozess übergibt.

Wenn Vorgänge mitHilfe von Implementierungen ausgeführt werden, die keine variablen Schriftarten unterstützen, führen diese Vorgänge möglicherweise nicht zu den erwarteten Ergebnissen. Beispielsweise können Glyphenpositionen für eine benannte Instanz der Variablenschriftart berechnet werden, aber die Glyphen können unter der Annahme einer anderen benannten Instanz gerendert werden. Abhängig von der Anwendungsimplementation können Ergebnisse in einigen Kontexten funktionieren, aber nicht in anderen Kontexten, in denen andere Bibliotheken verwendet werden können. Beispielsweise kann Text auf dem Bildschirm ordnungsgemäß angezeigt werden, jedoch nicht beim Drucken. Wenn End-to-End-Workflows nur mit DirectWrite implementiert werden, kann das richtige Verhalten für benannte Instanzen einer Variablenschriftart erwartet werden. 

Da vorhandene DirectWrite-APIs die Gesichtsauswahl mit dem Gewichtungs-/Stretch-/Stilmodell unterstützen, werden die benannten Instanzen von Schriftarten, die andere Variationsachsen verwenden, wie oben beschrieben vom allgemeinen typografischen Familienmodell in das WSS Modell projiziert. Dies basiert auf einer Variablenschriftart, einschließlich einer Tabelle mit "Stilattributen" ('STAT') mit Untertabellen für Achsenwerte, die DWrite verwendet, um Gesichtsnamentoken, die Gewichtungs-, Stretch- oder Stilattribute bestimmen, von Token zu unterscheiden, die sich auf andere Variationsachsen beziehen.  

Wenn eine Variablenschriftart keine STAT-Tabelle enthält, wie dies für variable Schriftarten gemäß der OpenType-Spezifikation erforderlich ist, behandelt DirectWrite die Schriftart als nicht variable Schriftart, die nur die Standardinstanz enthält.  

Wenn eine Schriftart eine STAT-Tabelle enthält, aber keine geeigneten Untertabellen für Achsenwerte enthält, kann dies zu unerwarteten Ergebnissen führen, z. B. zu mehreren Gesichtern mit identischen Gesichtsnamen. Solche Schriftarten werden derzeit nicht unterstützt. 

Die OpenType-Spezifikation ermöglicht die Darstellung von Glyphengliederungsdaten in einem von zwei Formaten: die Verwendung einer glyf-Tabelle, die das TrueType-Kontur- und Hinweisformat verwendet, oder die Verwendung einer CFF-Tabelle, die die CFF-Darstellung (Compact Font Format) verwendet. In einer Variablenschriftart mit TrueType-Konturen wird die Tabelle "glyf" weiterhin verwendet und durch eine "gvar"-Tabelle ergänzt, die die Variationsdaten für die Konturen liefert. Dies bedeutet, dass die Standardinstanz einer Variablenschriftart mit TrueType-Konturen nur herkömmliche OpenType-Tabellen verwendet, die in älterer Software ohne Unterstützung für Variablenschriftarten unterstützt werden. In einer Variablenschriftart mit CFF-Konturen wird die CFF-Tabelle jedoch durch die Tabelle "CFF2" ersetzt, die die Standardgliederungsdaten und die zugeordneten Variationsdaten in einer Tabelle kapselt. CFF-Daten werden von einem separaten Rasterizer verarbeitet, der für TrueType-Daten verwendet wird, und eine CFF2-Tabelle erfordert einen aktualisierten CFF-Rasterizer, der "CFF2" unterstützt. Eine CFF2-Tabelle kann nicht von älteren CFF-Rasterizern verarbeitet werden. Bei einer Variablenschriftart mit CFF-Konturdaten bedeutet dies, dass selbst die Standardinstanz in älterer Software nicht funktioniert. 

Im Windows 10 Creators Update unterstützt DirectWrite keine variablen Schriftarten mit CFF-Konturdaten, die die Tabelle "CFF2" verwenden. 

## <a name="using-opentype-variable-fonts"></a>Verwenden von OpenType-Variablenschriftarten

OpenType-Variablenschriftarten können einfach zu verwenden sein, unter Berücksichtigung der oben genannten aktuellen Einschränkungen: 

-   Derzeit werden nur benannte Instanzen einer Variablenschriftart unterstützt.
-   Derzeit werden nur variable Schriftarten unterstützt, die TrueType-Glyphenkonturdaten (keine CFF-Konturen) verwenden. 
-   Für Schriftarten, die andere Achsen als Gewichtung, Stretching oder Stil verwenden, werden benannte Instanzen in das WSS-Familienmodell projiziert, was dazu führen kann, dass einige benannte Instanzen als separate Familien angezeigt werden (wie es in der Vergangenheit bei nicht variablen Schriftarten der Fall wäre). Um dies zu unterstützen, müssen variablen Schriftarten über eine STAT-Tabelle verfügen, die entsprechende Achsenwert-Untertabellen enthält.
-   Benannte Instanzen von variablen Schriftarten werden in DirectWrite-APIs unterstützt. Wenn jedoch bestimmte Vorgänge in älteren Implementierungen ausgeführt werden, die keine variablen Schriftarten unterstützen, können diese zu falschen Ergebnissen führen. 
-   Bestimmte DirectWrite-APIs verwenden die Enumerationen [**DWRITE \_ FONT \_ WEIGHT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight), [**DWRITE \_ FONT \_ STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) und [**DWRITE FONT \_ \_ STYLE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) zum Angeben von Gewichtungs-, Stretch- und Stilattributen bei der Auswahl von Gesichtern. Wenn eine variable Schriftart entsprechende Variationsachsen verwendet, aber über viele benannte Instanzen verfügt, die eine genauere Granularität erfordern, können nicht alle benannten Instanzen in diesen APIs ausgewählt werden.

OpenType-Variablenschriftarten, die diesen Anforderungen entsprechen, können wie andere OpenType-Schriftarten über die Windows-Shell installiert werden und können auch in benutzerdefinierten Schriftartensätzen verwendet werden, die von einer App erstellt wurden.  

Bei der Installation im System werden alle benannten Instanzen einer Variablenschriftart in den Schriftartensatz aufgenommen, der durch Aufrufen der IDWriteFontFamily3::[**GetSystemFontSet-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) zurückgegeben wird. Beachten Sie, dass es sich bei einem Schriftartensatz um eine flache Liste ohne Familiengruppenhierarchie handelt, aber jedes Element in der Gruppe über eine Eigenschaft für den Familiennamen verfügt, die auf dem WSS basiert. Der Schriftartensatz kann mithilfe der [**IDWriteFontSet::GetMatchingFonts-Methoden**](idwritefontset-getmatchingfonts-overload.md) nach einer bestimmten benannten Instanz mit variabler Schriftart gefiltert werden. Bei Verwendung der **GetMatchingFonts-Überladung,** die einen familyName anfordert, muss der angegebene familyName jedoch den Namen verwenden, der dem WSS-Schriftfamilienmodell entspricht. Die vollständige Liste WSS-kompatiblen Familiennamen, die in einem Schriftartensatz auftreten, kann mithilfe der [**IDWriteFontSet::GetPropertyValues-Methoden**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) mithilfe der DWRITE \_ FONT \_ \_ PROPERTY-ID FAMILY NAME ermittelt \_ \_ werden.  

Ebenso werden alle benannten Instanzen einer Variablenschriftart in der Schriftartauflistung dargestellt, die von der IDWriteFactory::[**GetSystemFontCollection-Methode zurückgegeben**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) wird. Da es sich bei den Elementen einer Schriftartauf auflistung um Schriftfamilien handelt, die auf dem WSS-Modell basieren, können die benannten Instanzen einer variablen Schriftart in einer Auflistung als Member von zwei oder mehr Schriftfamilien dargestellt werden. Wenn die [**IDWriteFontCollection::FindFamilyName-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-findfamilyname) verwendet wird, muss der familyName-Parameter ein WSS kompatibler Familienname sein. Um alle WSS-kompatiblen Familiennamen aus einer Schriftartsammlung zu finden, kann eine App jede Familie durchschleifen und [**IDWriteFontFamily::GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames)aufrufen. Es kann jedoch einfacher sein, einen entsprechenden Schriftartensatz zu erhalten und die [**GetPropertyValues-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) wie oben beschrieben zu verwenden. 

Beim Arbeiten mit benutzerdefinierten Schriftarten können verschiedene Im Thema [Benutzerdefinierte](custom-font-sets-win10.md) Schriftartensätze beschriebene Ansätze verwendet werden, um einen Schriftartensatz zu erstellen. Zum Hinzufügen einer Variablenschriftart zu einem benutzerdefinierten Schriftartensatz wird die [**IDWriteFontSetBuilder1::AddFontFile-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) empfohlen, da sie variable Schriftarten unterstützt und alle benannten Instanzen einer Variablenschriftart in einem einzigen Aufruf hinzufüge. Derzeit gibt es keine Möglichkeit, einzelne benannte Instanzen einer benutzerdefinierten Variablenschriftart mithilfe der [**IDWriteFontSetBuilder::AddFontFaceReference-Methoden**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) zu einem Schriftartensatz hinzuzufügen, da es keine Möglichkeit gibt, einen Schriftartengesichtsverweis zu erstellen, um anzugeben, welche der benannten Instanzen aus einer Variablenschriftdatei vorgesehen ist. Dies bedeutet, dass es derzeit keine Möglichkeit gibt, einem benutzerdefinierten Schriftartsatz mit zugewiesenen benutzerdefinierten Eigenschaften benannte Instanzen einer benutzerdefinierten Schriftart hinzuzufügen. Dies bedeutet wiederum, dass benutzerdefinierte Variablenschriftarten derzeit nicht einfach in Verbindung mit DirectWrite-APIs für Remoteschriftarten verwendet werden können. Wenn benannte Instanzen einer Variablenschriftart in einem Systemschriftsatz enthalten sind, sind jedoch bereits Schriftartverweise für jede benannte Instanz vorhanden, und diese können benutzerdefinierten Schriftartensätzen hinzugefügt werden, einschließlich der Verwendung benutzerdefinierter Eigenschaftswerte. Weitere Informationen finden Sie im Thema Benutzerdefinierte Schriftartensätze. 

Bei der Arbeit mit variablen Schriftarten sind die stretch-Enumerationen DirectWrite [**DWRITE \_ FONT \_ WEIGHT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight) und [**DWRITE \_ FONT \_ eng**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) mit den Invarianzachsen für Gewichtung und Breite verbunden, die in der OpenType-Spezifikation definiert sind, sind jedoch nicht identisch. Erstens unterstützt die numerische Skala für jede Variationsachse immer Bruchwerte, während fontWeight und fontStretch ganze Zahlen verwenden. Die Skalierung der OpenType-Gewichtungsachse verwendet Werte im Bereich von 1 bis 1000, was auch von fontWeight unterstützt wird. Daher ist die Änderung von einem Wert der Variationsgewichtungsachse zu fontWeight relativ gering: Das für eine benannte Instanz gemeldete fontWeight-Wert kann aus dem genauen Wert gerundet werden, der zum Definieren der benannten Instanz innerhalb der Schriftart verwendet wird. Der Unterschied zwischen DirectWrite fontStretch und der Breite der OpenType-Achsenskala ist größer: DirectWrite verwendet Werte von 1 bis 9, die auf die [usWidthClass-Werte](/typography/opentype/spec/os2#uswidthclass) der OpenType OS/2-Tabelle folgen, während die Breite der OpenType-Achsenskala positive Werte verwendet, die einen Prozentsatz der normalen Breite darstellen. Die [usWidthClass-Dokumentation](/typography/opentype/spec/os2#uswidthclass) in der OpenType-Spezifikation stellt eine Zuordnung zwischen den Werten 1 bis 9 und dem Prozentwert des Normalwerts zur Verfügung. Der für eine benannte Instanz gemeldete fontStretch-Wert kann beim Konvertieren von Breitenachsenwerten eine Rundung beinhalten. 

Beim Erstellen eines [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)müssen eine Schriftartsammlung und WSS kompatible Schriftarteigenschaften (Familienname, Gewichtung, Stretching und Stil) angegeben werden. Dies gilt auch beim Festlegen von Schriftartformatierungseigenschaften für einen [**IDWriteTextLayout-Textbereich.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) Die Eigenschaften können aus einem [**IDWriteFontFace3-Objekt**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) oder aus [**IDWriteFont-**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) und [**IDWriteFontFamily-Objekten**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) ermittelt werden, die eine bestimmte benannte Instanz darstellen. Wie oben erwähnt, können die von den GetWeight- und GetStretch-Methoden zurückgegebenen Werte gerundete Näherungen für die tatsächlichen Achsenwerte sein, die zum Definieren der benannten Instanz verwendet werden. DirectWrite wird die Kombination der Eigenschaften jedoch wieder der gewünschten benannten Instanz zuordnen. 

Wenn eine App [**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md) verwendet, um benutzerdefinierte Schriftartfallbackdaten zu erstellen, werden Familien für Zeichenbereichszuordnungen mit WSS kompatiblen Familiennamen angegeben. Das Schriftartfallback in DirectWrite basiert auf Familien mit DirectWrite, die eine Variante innerhalb einer Fallbackfamilie auswählen, die eine nächste Übereinstimmung für die Variante der Anfangsfamilie ist. Für Varianten, die andere Dimensionen als Gewichtung, Streckung und Stil umfassen, kann DirectWrite diese Varianten derzeit nicht innerhalb einer Fallbackfamilie auswählen, es sei denn, benutzerdefinierte Fallbackdaten wurden speziell erstellt, um Fallbackzuordnungen für Familien mit bestimmten nicht WSS-Attributen wie optischen Größenvarianten "Caption" zu bieten.

 

 