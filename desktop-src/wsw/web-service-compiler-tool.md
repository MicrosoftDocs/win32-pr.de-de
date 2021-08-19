---
title: Webdienstcompilertool
description: Zur Unterstützung des Dienstmodells generiert wsutil.exe Header, der sowohl auf Client- als auch auf Dienstseite verwendet werden soll. Bei Bedarf werden die C-Proxydatei für die Clientseite und die C-Stubdatei für die Dienstseite generiert.
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- Webdienstcompilertool-Webdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92e1195cd9d3a8e8d9fa1b7be94421d68f3cbdf2242be6fa0d05be5cc3c743f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962839"
---
# <a name="web-service-compiler-tool"></a>Webdienstcompilertool

Zur Unterstützung des Dienstmodells generiert wsutil.exe Header, der sowohl auf Client- als auch auf Dienstseite verwendet werden soll. Bei Bedarf werden die C-Proxydatei für die Clientseite und die C-Stubdatei für die Dienstseite generiert.


Zur Unterstützung [der Serialisierung](serialization.md)generiert der Compiler Header für Elementbeschreibungen für globale Elementdefinitionen und alle Typdefinitionsinformationen in der Proxydatei, die von der Serialisierungs-Engine verwendet werden sollen.

Verbrauch

**WsUtil.exe \[ Befehlszeilenschalter \[ switch-options: \]\]<filename>**

Befehlszeilenschalter

Gibt WsUtil.exe Compileroptionen an. Schalter können in beliebiger Reihenfolge angezeigt werden. Bindestrich ('-') und Schrägstrich ('/') werden gleich behandelt.

Liste der Befehlszeilenoptionen

-   @filename Gibt an, dass die Eingabedatei als Antwortdatei behandelt werden soll. Diese Option kann mehrmals an beliebigen Stellen in der Argumentliste verwendet werden.
-   /wsdl: :<optional url> Gibt an, dass die Eingabedatei als <filename> \_ WSDL-Datei behandelt werden soll. Mehrere wsdl-Eingaben sind zulässig, und alle angegebenen WSDL-Dateien werden verarbeitet. Die \_ optionale URL gibt den Speicherort an, von dem die Metadaten abgerufen wurden. Wenn keine optionale \_ URL angegeben wird, generiert Wsutil intern eine eindeutige URL. Siehe auch [Richtlinienunterstützung.](policy-support.md)
-   /xsd: <filename> Gibt an, dass der Eingabedateiname als Schemadatei behandelt werden soll. Mehrere xsd-Eingaben sind zulässig, und alle angegebenen Schemadateien werden verarbeitet.
-   /wsp: :<optional url> Gibt an, dass der <filename> \_ Eingabedateiname als Richtlinienmetadaten behandelt werden soll. Mehrere wsp-Eingaben sind zulässig, und alle angegebenen Richtliniendateien werden verarbeitet. Die \_ optionale URL gibt den Speicherort an, von dem die Metadaten abgerufen wurden. Wenn keine optionale \_ URL angegeben wird, generiert Wsutil intern eine eindeutige URL. Richtliniendateien werden ignoriert, wenn das Flag /nopolicy angegeben wird. Siehe auch [Richtlinienunterstützung.](policy-support.md)
-   /nopolicy Deaktiviert die Richtlinienverarbeitung.
-   /out: <dirname> Gibt den Verzeichnisnamen für Ausgabedateien an.
-   /noclient Generieren Sie den clientseitigen Stub nicht.
-   /noservice Generieren Sie den dienstseitigen Stub nicht.
-   /prefix: <string> Stellen Sie allen generierten Bezeichnern eine angegebene Zeichenfolge voran.
-   /fullname: Prepend normalized filename to generated identifiers. Standardmäßig wird nur der im Attribut "name" angegebene Name verwendet, um Bezeichner für verwandte Beschreibungen zu generieren.
-   /string:<WS STRING><WCHAR> Standardmäßig generiert \_ \| \* wsutil WCHAR für \* den xsd:string-Typ. Die Anwendung kann dieses Flag verwenden, um dieses Verhalten zu überschreiben, und generiert stattdessen WS \_ STRING für xsd:type.
-   /help Hilfemeldung anzeigen
-   /? Identisch mit /help
-   /W:x Fehlerbehandlungsoptionen. Könnte W:0-W:4 \| WX sein.
-   /nologo Generieren Sie keine compilerspezifischen Informationen in der Konsolenausgabe.
-   /nostamp Generieren Sie keine compilerspezifischen Informationen zu generierten Dateien.

Standardmäßig generiert der Compiler die folgenden Dateien für die WSDL-Datei oder WSDL, die vom Metadatenaustausch zurückgegeben wird:

-   Clientproxy ({inputfilename}.c)
-   Dienststub ({Eingabedateiname}.c)
-   Headerdatei ({inputfilename}.h)

    Der Stamm des generierten Dateinamens ist der Name der Eingabedatei. Ursprüngliche Eingabedateierweiterungen werden beibehalten, um Dateinamenkollisionen für generierte Dateien zu verhindern. Standardmäßig werden Client- und Dienststubs in derselben Datei generiert, und nach dem Proxycode wird Dienststubcode generiert.

    Standardmäßig generiert der Compiler die folgenden Dateien für eine XSD-Datei für das Schema, das vom Metadatenaustausch zurückgegeben wird:

-   Serialisierungsbeschreibungen ({inputfilename}.c)
-   Headerdatei ({inputfilename}.h)

    Der Stamm des Dateinamens ist der Dienstname.

Wsutil.exe generiert am Anfang aller generierten Dateien einen "Stempel"-Abschnitt, der die Compileroption, Toolversion, anwendbare Befehlszeilenoption usw. angibt. Dieser Abschnitt kann mit der Option /nostamp deaktiviert werden, um Rauschen beim Vergleichen generierter Dateien zu vermeiden.

Wsutil unterstützt das Herunterladen von Metadaten nicht.

Der Wsutil-Compiler funktioniert nur über eine lokale Metadatendatei. Das Tool unterstützt das Herunterladen von Metadaten aus ausgeführten Webdiensten nicht. Entwickler können andere unterstützte Webdiensttools wie svcutil verwenden, um Metadaten auf den lokalen Computer herunterzuladen, die gespeicherten Dateien zu überprüfen und diese Dateien zur Kompilierung an wsutil.exe übergeben.

Unterstützung mehrerer Eingabe-/Ausgabedateien

WSDL- und XML-Schemas ermöglichen das Ein-/Importieren von Definitionen aus anderen Namensräumen, die an anderen Speicherorten/Dateien angegeben sind. Wsutil unterstützt mehrere Schema-/WSDL-/Richtlinieneingaben und generiert einen Satz stub/header für jede Eingabedatei. Wsutil folgt nicht den Include- und Import-Anweisungen. Stattdessen sollte die Anwendung Dateien mit allen erforderlichen Namespaces an wsutil übergeben, damit das Tool alle Abhängigkeiten während der Kompilierung auflösen kann.

**WsUtil.exe /xsd:stockquote.xsd /wsdl:stockquote.wsdl /wsdl:stockquoteservice.wsdl**

wsutil generiert drei Sätze von Ausgabedateien:

-   stockquote.xsd.c stockquote.xsd.h
-   stockquote.wsdl.c stockquote.wsdl.h
-   stockquoteservice.wsdl.h stockquoteservices.wsdl.c

Format der Ausgabedatei

Für jede Ausgabedatei generiert wsutil extern verfügbare Definitionen in der Headerdatei. Neben C-Strukturdefinitionen und Stubfunktionsprototypen werden alle anderen webdienstbezogenen Definitionen in einer globalen Struktur mit dem Namen mit normalisiertem Dateinamen gekapselt.

``` syntax
typedef struct _stockquote_wsdl {
  struct {
  ... // list of WS_STRUCT_DESCRIPTION for all global complex types.
  } globalTypes;
  struct {
  ... // WS_ELEMENT_DESCRIPTION for all global elements.
  } globalElements;
  struct {
  ...
  } messages;
  struct {
  ...
  } contracts;
} _stockquote_wsdl;

EXTERN_C _stockquote_wsdl stockquote_wsdl;
```

Beachten Sie, dass nicht alle Felder für die globale Struktur generiert werden. Ein Feld der obersten Ebene wird nur generiert, wenn die zugehörigen Definitionen in der Eingabedatei angegeben werden. Beispielsweise werden keine Meldungs-, Betriebs- und Vertragsfelder für xsd-Dateien generiert.

Warnstufen und Fehlerstufe

Ähnlich wie der C-Compiler unterstützt WsUtil.exe vier Warnstufen und eine Fehlerebene:

-   WsUtil.exe Fehler mit nicht behebbaren Fehlern wie ungültige WSDL-Datei, ungültige Compileroptionen usw.
-   WsUtil generiert W1-Warnungen mit schwerwiegenden wiederherstellbaren Problemen. Der Compiler kann weiter gehen, aber der Benutzer sollte sich des Problems bewusst sein. Beispielsweise wird eine W1-Warnung generiert, wenn in wsdl nicht unterstützte Attribute wie einige WSDL-Facets enthalten sind, die sich nicht auf die Codegenerierung auswirken.
-   WsUtil generiert W2-Warnungen mit weniger schwerwiegenden Problemen. Die Funktionalität geht nicht verloren, aber der Anwendungsentwickler möchte dies vielleicht wissen. Ähnlich wie Verhaltensweisen, die sich von anderen Plattformen unterscheiden können.
-   WsUtil generiert W3-Warnungen mit minimalen Auswirkungen auf generierten Code. Beispielsweise generiert wsutil.exe eine W3-Warnung, wenn sich normalisierte Zeichenfolge von der ursprünglichen Zeichenfolge unterscheiden.
-   Die W4-Warnung ist eher mit "Informationswarnungen" und WsUtil-Problem W4 in Fällen wie dem Ignorieren des Dokumentationsattributs in WSDL gleich.
-   WX gibt an, dass der Compiler Warnungen als Fehler behandelt. Beispielsweise generiert wsutil einen Fehler für alle W1-Warnungen, wenn /W:1 /WX angegeben ist.

/W:{N} gibt an, welche Stufe der Warnmeldung generiert werden soll. /W:1 bedeutet, dass Warnungen der Warnstufe 1 generiert werden sollten, und Warnungen der Warnstufe 2 und darunter sollten maskiert und nicht vom Tool generiert werden.

## <a name="fullname"></a>/fullname

Diese Option gibt an, WsUtil.exe vollständigen Namen für Bezeichner generiert, um potenzielle Namenskollisionen zu vermeiden. In "example.xsd" gibt es beispielsweise Folgendes:

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:element name="SimpleStruct">
   <xs:complexType>
    <xs:sequence>
     <xs:element name="a" type="xs:int" />
     <xs:element name="b" type="xs:int" />
    </xs:sequence>
   </xs:complexType>
  </xs:element>
 </wsdl:types>
</wsdl:definitions>
```

Standardmäßig generiert WsUtil.exe:

``` syntax
typedef struct SimpleStruct {
  int a;
  int b;
};
```

Wenn jedoch die Befehlszeilenoption /fullname angegeben ist, WsUtil.exe stattdessen die folgende Strukturdefinition generiert:

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a>Globalisierung

Das Tool ist sprachneutral und kann in verschiedene Sprachen lokalisiert werden. Alle Fehlermeldungen/Konsolenausgaben können lokalisiert werden. Die Befehlszeilenoptionen bleiben jedoch auf Englisch.

## <a name="environment-variable"></a>Umgebungsvariable

WsUtil.exe verwendet keine Umgebungsvariablen.

## <a name="platform-independent"></a>Plattformunabhängig

Ausgabedateien von WsUtil.exe sind plattformunabhängig. Im Stub wird kein architekturabhängiger Code generiert. Alle Architekturen, die spezifisch sind, werden vom C-Compiler übernommen. Der Stub kann auf allen plattformen verwendet werden, die wir unterstützen.

Eine Beschreibung für wsutil.exe Ausgabe finden Sie unter [WSDL-Unterstützung](wsdl-support.md) und [Schemaunterstützung.](schema-support.md)

 

 




