---
title: Webdienstcompilertool
description: Zur Unterstützung des Dienstmodells generiert wsutil.exe Header, der sowohl auf client- als auch dienstseitiger Seite verwendet werden soll. Bei Bedarf wird eine C-Proxydatei für die Clientseite und eine C-Stubdatei für die Dienstseite generiert.
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- Webdienste des Webdienstcompilertools für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6789b9e2b6e38d89e422adc363326656b8f693e2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880989"
---
# <a name="web-service-compiler-tool"></a>Webdienstcompilertool

Zur Unterstützung des Dienstmodells generiert wsutil.exe Header, der sowohl auf client- als auch dienstseitiger Seite verwendet werden soll. Bei Bedarf wird eine C-Proxydatei für die Clientseite und eine C-Stubdatei für die Dienstseite generiert.


Zur Unterstützung der [Serialisierung](serialization.md)generiert der Compiler Header für Elementbeschreibungen für globale Elementdefinitionen und alle Typdefinitionsinformationen in der Proxydatei, die von der Serialisierungs-Engine genutzt werden sollen.

Verwendung

**WsUtil.exe \[ Befehlszeilenschalter \[ switch-options : \] \] &lt; dateiname&gt;**

Befehlszeilenschalter

Gibt WsUtil.exe Compileroptionen an. Schalter können in beliebiger Reihenfolge angezeigt werden. Bindestrich ('-') und Schrägstrich ('/') werden als identisch behandelt.

Liste der Befehlszeilenoptionen

-   @filename Gibt an, dass die Eingabedatei als Antwortdatei behandelt werden soll. Diese Option kann an beliebigen Stellen in der Argumentliste mehrmals verwendet werden.
-   /wsdl: &lt; Dateiname &gt; :<optionale \_ URL> Gibt an, dass die Eingabedatei als wsdl-Datei behandelt werden soll. Mehrere wsdl-Eingaben sind zulässig, und alle angegebenen WSDL-Dateien werden verarbeitet. Die optionale \_ URL gibt den Speicherort an, von dem die Metadaten abgerufen wurden. Wenn keine optionale \_ URL angegeben wird, generiert Wsutil intern eine eindeutige URL. Siehe auch [Richtlinienunterstützung.](policy-support.md)
-   /xsd: &lt; filename &gt; Gibt an, dass der Eingabedateiname als Schemadatei behandelt werden soll. Mehrere xsd-Eingaben sind zulässig, und alle angegebenen Schemadateien werden verarbeitet.
-   /wsp: &lt; Dateiname &gt; :<optionale \_ URL> Gibt an, dass der Eingabedateiname als Richtlinienmetadaten behandelt werden soll. Mehrere wsp-Eingaben sind zulässig, und alle angegebenen Richtliniendateien werden verarbeitet. Die optionale \_ URL gibt den Speicherort an, von dem die Metadaten abgerufen wurden. Wenn keine optionale \_ URL angegeben wird, generiert Wsutil intern eine eindeutige URL. Richtliniendateien werden ignoriert, wenn das Flag /nopolicy angegeben wird. Siehe auch [Richtlinienunterstützung.](policy-support.md)
-   /nopolicy Richtlinienverarbeitung deaktivieren.
-   /out: &lt; dirname &gt; Gibt den Verzeichnisnamen für Ausgabedateien an.
-   /noclient Generieren Sie den clientseitigen Stub nicht.
-   /noservice Generieren Sie den dienstseitigen Stub nicht.
-   /prefix: &lt; Zeichenfolge Setzt allen &gt; generierten Bezeichnern eine angegebene Zeichenfolge voran.
-   /fullname Setzt dem generierten Bezeichner einen normalisierten Dateinamen voran. Standardmäßig wird nur der im Attribut "name" angegebene Name verwendet, um Bezeichner für verwandte Beschreibungen zu generieren.
-   /string:<WS \_ STRING><\| WCHAR \*> Standardmäßig generiert wsutil WCHAR für \* den Typ xsd:string. Die Anwendung kann dieses Flag verwenden, um dieses Verhalten zu überschreiben, und generiert stattdessen WS \_ STRING für xsd:type.
-   /help Hilfemeldung anzeigen
-   /? Identisch mit /help
-   /W:x Fehlerbehandlungsoptionen. Kann W:0-W:4 \| WX sein
-   /nologo Generieren Sie keine compilerspezifischen Informationen in der Konsolenausgabe.
-   /nostamp Generieren Sie keine compilerspezifischen Informationen zu generierten Dateien.

Standardmäßig generiert der Compiler die folgenden Dateien für die WSDL-Datei oder die vom Metadatenaustausch zurückgegebene WSDL:

-   Clientproxy ({inputfilename}.c)
-   Dienststub ({Eingabedateiname}.c)
-   Headerdatei ({inputfilename}.h)

    Der Stamm des generierten Dateinamens ist der Name der Eingabedatei. Ursprüngliche Eingabedateierweiterungen werden beibehalten, um Konflikte mit Dateinamen für generierte Dateien zu verhindern. Standardmäßig werden Client- und Dienststubs in derselben Datei generiert, wobei Dienststubcode nach dem Proxycode generiert wird.

    Standardmäßig generiert der Compiler die folgenden Dateien für eine XSD-Datei für das Schema, das vom Metadatenaustausch zurückgegeben wird:

-   Serialisierungsbeschreibungen ({inputfilename}.c)
-   Headerdatei ({inputfilename}.h)

    Der Stamm des Dateinamens ist der Dienstname.

Wsutil.exe generiert am Anfang aller generierten Dateien einen Abschnitt "stamp", der die Compileroption, die Toolversion, die zutreffende Befehlszeilenoption usw. angibt. Dieser Abschnitt kann mithilfe der Option /nostamp deaktiviert werden, um Rauschen beim Vergleichen generierter Dateien zu vermeiden.

Wsutil unterstützt das Herunterladen von Metadaten nicht.

Der Wsutil-Compiler funktioniert nur aus der lokalen Metadatendatei. Das Tool unterstützt das Herunterladen von Metadaten aus ausgeführten Webdiensten nicht. Entwickler können andere unterstützte Webdiensttools wie svcutil verwenden, um Metadaten auf den lokalen Computer herunterzuladen, die gespeicherten Dateien zu untersuchen und diese Dateien zur Kompilierung an wsutil.exe zu übergeben.

Unterstützung mehrerer Eingabe-/Ausgabedateien

Das WSDL- und XML-Schema ermöglicht das Einschließen/Importieren von Definitionen aus anderen Namensbereichen, die an anderen Speicherorten/Dateien angegeben sind. Wsutil unterstützt mehrere schema/wsdl/policy-Eingaben und generiert einen Satz stub/header für jede Eingabedatei. Wsutil folgt nicht den Include- und Importanweisungen. Stattdessen sollte die Anwendung Dateien mit allen erforderlichen Namespaces an wsutil übergeben, damit das Tool alle Abhängigkeiten während der Kompilierung auflösen kann.

**WsUtil.exe /xsd:stockquote.xsd /wsdl:stockquote.wsdl /wsdl:stockquoteservice.wsdl**

wsutil generiert drei Sätze von Ausgabedateien:

-   stockquote.xsd.c stockquote.xsd.h
-   stockquote.wsdl.c stockquote.wsdl.h
-   stockquoteservice.wsdl.h stockquoteservices.wsdl.c

Format der Ausgabedatei

Für jede Ausgabedatei generiert wsutil extern verfügbare Definitionen in der Headerdatei. Abgesehen von C-Strukturdefinitionen und Stubfunktionsprototypen werden alle anderen webdienstbezogenen Definitionen in einer globalen Struktur namens mit normalisiertem Dateinamen gekapselt.

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

Beachten Sie, dass nicht alle Felder für die globale Struktur generiert werden. Ein Feld der obersten Ebene wird nur generiert, wenn die zugehörigen Definitionen in der Eingabedatei angegeben sind. Beispielsweise werden keine Felder für Nachrichten, Vorgänge und Verträge für xsd-Dateien generiert.

Warnstufen und Fehlerstufe

Ähnlich wie beim C-Compiler unterstützt WsUtil.exe vier Warnstufen und eine Fehlerstufe:

-   WsUtil.exe generiert Fehler mit nicht behebbaren Fehlern, z. B. ungültige wsdl-Datei, ungültige Compileroptionen usw.
-   WsUtil generiert W1-Warnungen mit schwerwiegenden wiederherstellbaren Problemen. Der Compiler kann weitermachen, aber der Benutzer sollte sich des Problems bewusst sein. Beispielsweise wird eine W1-Warnung generiert, wenn nicht unterstützte Attribute wie einige WSDL-Facets in wsdl vorhanden sind, die sich nicht auf die Codegenerierung auswirken.
-   WsUtil generiert W2-Warnungen mit weniger schwerwiegenden Problemen. Die Funktionalität geht nicht verloren, aber anwendungsentwickler möchten dies vielleicht wissen. Ähnlich wie Verhaltensweisen, die sich von anderen Plattformen unterscheiden können.
-   WsUtil generiert W3-Warnungen mit minimalen Auswirkungen auf generierten Code. Beispielsweise generiert wsutil.exe eine W3-Warnung, wenn sich die normalisierte Zeichenfolge von der ursprünglichen Zeichenfolge unterscheidet.
-   W4-Warnungen ähneln eher "Informationswarnungen", und WsUtil gibt W4 in Fällen wie dem Ignorieren des Dokumentationsattributs in WSDL aus.
-   WX gibt an, dass der Compiler Warnungen als Fehler behandelt. Beispielsweise generiert wsutil einen Fehler für alle W1-Warnungen, wenn /W:1 /WX angegeben ist.

/W:{N} geben Sie an, welche Warnstufe generiert werden soll. /W:1 bedeutet, dass Warnungen der Warnstufe 1 generiert werden müssen, und Warnungen der Warnstufe 2 und darunter sollten maskiert und nicht vom Tool generiert werden.

## <a name="fullname"></a>/fullname

Diese Option gibt an, dass WsUtil.exe einen vollständigen Namen für Bezeichner generiert, um potenzielle Namenskonflikte zu vermeiden. In example.xsd haben wir beispielsweise Folgendes:

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

Wenn jedoch die Befehlszeilenoption /fullname angegeben ist, generiert WsUtil.exe stattdessen die folgende Strukturdefinition:

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a>Globalisierung

Das Tool ist sprachneutral und kann in verschiedene Sprachen lokalisiert werden. Alle Fehlermeldungen/Konsolenausgabe können lokalisiert werden. Die Befehlszeilenoptionen bleiben jedoch auf Englisch.

## <a name="environment-variable"></a>Umgebungsvariable

WsUtil.exe verwendet keine Umgebungsvariablen.

## <a name="platform-independent"></a>Plattformunabhängig

Ausgabedateien von WsUtil.exe sind plattformunabhängig. Im Stub wird kein architekturabhängiger Code generiert. Alle architekturspezifischen Aufgaben werden vom C-Compiler übernommen. Der Stub kann auf allen plattformen verwendet werden, die wir unterstützen.

Eine Beschreibung wsutil.exe Ausgabe finden Sie unter [WSDL-Unterstützung](wsdl-support.md) und [Schemaunterstützung.](schema-support.md)

 

 




