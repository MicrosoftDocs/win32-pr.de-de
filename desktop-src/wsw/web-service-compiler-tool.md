---
title: Webdienst-Compilertool
description: Zur Unterstützung des Dienst Modells generiert wsutil.exe sowohl auf Client-als auch auf Dienst Seite zu verwendende Header. Es generiert bei Bedarf die c-Proxy Datei für die Clientseite und die c-Stub-Datei für die Dienst Seite.
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- Webdienst-Compilertool-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9931f228a36832fc83d84d584a151de41f5868d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391253"
---
# <a name="web-service-compiler-tool"></a>Webdienst-Compilertool

Zur Unterstützung des Dienst Modells generiert wsutil.exe sowohl auf Client-als auch auf Dienst Seite zu verwendende Header. Es generiert bei Bedarf die c-Proxy Datei für die Clientseite und die c-Stub-Datei für die Dienst Seite.


Zur Unterstützung der [Serialisierung](serialization.md)generiert der Compiler Header für Element Beschreibungen für globale Element Definitionen und alle typdefinitions Informationen in der Proxy Datei, die von der Serialisierungs-Engine verwendet werden sollen.

Verbrauch

**\[Schalter Optionen fürWsUtil.exe Befehls Zeilenschalter \[ \] :\]<filename>**

Befehls Zeilenschalter

Gibt WsUtil.exe Compileroptionen an. Schalter können in beliebiger Reihenfolge angezeigt werden. Bindestrich ("-") und Schrägstrich ("/") werden als identisch behandelt.

Liste der Befehlszeilenoptionen

-   @filename Gibt an, dass die Eingabedatei als Antwortdatei behandelt werden soll. Diese Option kann an beliebigen Stellen in der Argumentliste mehrmals verwendet werden.
-   /WSDL: <filename> : <optionale \_ URL> gibt an, dass die Eingabedatei als WSDL-Datei behandelt werden soll. Mehrere WSDL-Eingaben sind zulässig, und alle angegebenen WSDL-Dateien werden verarbeitet. Die optionale \_ URL gibt den Speicherort an, von dem die Metadaten abgerufen wurden. Wenn keine optionale \_ URL angegeben ist, wird von wsutil intern eine eindeutige URL generiert. Siehe auch [Richtlinien Unterstützung](policy-support.md).
-   /XSD: <filename> gibt an, dass der Eingabe Dateiname als Schema Datei behandelt werden soll. Mehrere XSD-Eingaben sind zulässig, und alle angegebenen Schema Dateien werden verarbeitet.
-   /wsp: <filename> : <optionale \_ URL> gibt an, dass der Eingabe Dateiname als Richtlinien Metadaten behandelt werden soll. Mehrere WSP-Eingaben sind zulässig, und alle angegebenen Richtlinien Dateien werden verarbeitet. Die optionale \_ URL gibt den Speicherort an, von dem die Metadaten abgerufen wurden. Wenn keine optionale \_ URL angegeben ist, wird von wsutil intern eine eindeutige URL generiert. Richtlinien Dateien werden ignoriert, wenn/nopolicy-Flag angegeben wird. Siehe auch [Richtlinien Unterstützung](policy-support.md).
-   /nopolicy deaktivieren Sie die Richtlinien Verarbeitung.
-   /Out: <dirname> gibt den Verzeichnisnamen für Ausgabedateien an.
-   /noclient generieren Sie den Client seitigen Stub nicht.
-   /noservice generieren Sie den Dienst seitigen Stub nicht.
-   /Prefix: <string> die angegebene Zeichenfolge wird allen generierten bezeichchern vorangesteht.
-   /FullName fügt einem generierten Bezeichner den normalisierten Dateinamen voran. Standardmäßig wird nur der im Attribut "Name" angegebene Name verwendet, um Bezeichner für Verwandte Beschreibungen zu generieren.
-   /String: <WS \_ String>\|<WCHAR- \*> standardmäßig generiert wsutil WCHAR \* für den XSD: String-Typ. Die Anwendung kann dieses-Flag verwenden, um dieses Verhalten zu überschreiben, und generiert stattdessen die WS- \_ Zeichenfolge für XSD: Type.
-   /Help Anzeigen der Hilfe Meldung
-   /? Identisch mit/Help
-   /W: x Fehler Behandlungsoptionen. Kann "w:0-W: 4 \| WX" lauten.
-   /nologo generieren Sie keine compilerspezifischen Informationen zur Konsolenausgabe.
-   /nostamp generiert keine compilerspezifischen Informationen zu generierten Dateien.

Standardmäßig generiert der Compiler die folgenden Dateien für die WSDL-Datei oder WSDL, die vom Metadatenaustausch zurückgegeben wurde:

-   Client Proxy ({InputFilename}. c)
-   Dienstub ({InputFilename}. c)
-   Header Datei ({InputFilename}. h)

    Der Stamm des generierten Datei namens ist der Name der Eingabedatei. Die ursprünglichen Eingabedatei Erweiterungen werden beibehalten, um den Dateinamen Konflikt für generierte Dateien zu verhindern. Standardmäßig werden Client-und dienststubs in der gleichen Datei generiert, wobei ein Stub-Dienst Code nach dem Proxycode generiert wird.

    Standardmäßig generiert der Compiler die folgenden Dateien für eine XSD-Datei für das Schema, das vom Metadatenaustausch zurückgegeben wird:

-   serialisierungsbeschreibungen ({InputFilename}. c)
-   Header Datei ({InputFilename}. h)

    Der Stamm des Datei namens ist der Dienst Name.

Wsutil.exe generiert einen "Stempel"-Abschnitt am Anfang aller generierten Dateien, die die Compileroption, die Tool Version, die Befehlszeilenoption anwendbar usw. angeben. Dieser Abschnitt kann mithilfe der Option/nostamp deaktiviert werden, um das Vergleichen generierter Dateien zu vermeiden.

Wsutil unterstützt das Herunterladen von Metadaten nicht

Der wsutil-Compiler funktioniert nur aus der lokalen Metadatendatei. Das Tool unterstützt nicht das Herunterladen von Metadaten aus dem Ausführen von Webdiensten. Entwickler können andere unterstützte Webdienst Tools, wie z. b. Svcutil, verwenden, um Metadaten auf den lokalen Computer herunterzuladen, die gespeicherten Dateien zu überprüfen und diese Dateien an wsutil.exe zur Kompilierung zu übergeben.

Unterstützung mehrerer Eingabe-/Ausgabedateien

WSDL und XML-Schema ermöglichen das einschließen/Importieren von Definitionen aus anderen Namespaces, die in anderen Speicherorten/Dateien angegeben sind. Wsutil unterstützt mehrere Schema-/WSDL-/richtlinieneingaben und generiert eine Gruppe von Stub/Header für jede Eingabedatei. Wsutil befolgt nicht die include-und Import-Anweisungen. Stattdessen sollte die Anwendung Dateien, die alle erforderlichen Namespaces enthalten, an wsutil übergeben, sodass das Tool alle Abhängigkeiten während der Kompilierung auflösen kann.

**WsUtil.exe/XSD: StockQuote. xsd/WSDL: StockQuote. WSDL/WSDL: StockQuoteService. WSDL**

wsutil generiert drei Sätze von Ausgabedateien:

-   StockQuote. xsd. c StockQuote. xsd. h
-   StockQuote. WSDL. c StockQuote. WSDL. h
-   StockQuoteService. WSDL. h stockquoteservices. WSDL. c

Format der Ausgabedatei

Für jede Ausgabedatei generiert wsutil extern verfügbare Definitionen in der Header Datei. Abgesehen von C-Strukturdefinitionen und Stub-Funktionsprototypen werden alle anderen Webdienst bezogenen Definitionen in einer globalen Struktur mit dem Namen mit dem normalisierten Dateinamen gekapselt.

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

Beachten Sie, dass nicht alle Felder für die globale Struktur generiert werden. Ein Feld der obersten Ebene wird nur generiert, wenn die zugehörigen Definitionen in der Eingabedatei angegeben werden. Beispielsweise werden keine Nachrichten-, Vorgangs-und Vertrags Felder für XSD-Dateien generiert.

Warn Stufen und Fehlerstufe

Ähnlich wie der C-Compiler unterstützt WsUtil.exe vier Warn Stufen und eine Fehlerstufe:

-   WsUtil.exe generiert Fehler mit nicht BEHEB baren Fehlern, z. b. ungültige WSDL-Dateien, ungültige Compileroptionen usw.
-   Wsutil generiert W1-Warnungen mit schwerwiegenden BEHEB baren Problemen. Der Compiler kann fortfahren, aber der Benutzer sollte das Problem beachten. Beispielsweise wird eine Warnung mit dem Wert W1 generiert, wenn nicht unterstützte Attribute, wie z. b. einige WSDL-Facetten, in WSDL vorhanden sind, die sich nicht auf die Codegenerierung auswirken.
-   Wsutil generiert W2-Warnungen mit weniger ernsten Problemen. Die Funktionalität ist nicht verloren, aber der Anwendungsentwickler möchte dies möglicherweise wissen. Wie Verhalten, die sich von anderen Plattformen unterscheiden können.
-   Wsutil generiert w3-Warnungen mit minimalen Auswirkungen auf generierten Code. Beispielsweise generiert wsutil.exe eine w3-Warnung, wenn sich die normalisierte Zeichenfolge von der ursprünglichen Zeichenfolge unterscheidet.
-   W4 Warning ähnelt eher "Informations Warnungen" und "wsutil Issue W4" in Fällen wie das Ignorieren von Dokumentations Attributen in WSDL.
-   WX gibt an, dass der Compiler die Warnung als Fehler behandelt. Wsutil generiert beispielsweise für alle W1-Warnungen einen Fehler, wenn/W: 1/WX angegeben wird.

/W: {N} geben Sie an, welche Warnstufe der Warnung generiert werden soll. /W: 1 bedeutet, dass Warnungen der Stufe 1 generiert werden müssen. Warnungen der Warnstufe 2 und darunter sollten maskiert und nicht vom Tool generiert werden.

## <a name="fullname"></a>/fullname

Diese Option gibt an, dass WsUtil.exe vollständigen Namen für Bezeichner generiert, um einen potenziellen namens Konflikt zu vermeiden. Beispielsweise haben wir in "Beispiel. xsd" Folgendes:

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

Standardmäßig WsUtil.exe generiert:

``` syntax
typedef struct SimpleStruct {
  int a;
  int b;
};
```

Wenn jedoch die/FullName-Befehlszeilenoption angegeben ist, generiert WsUtil.exe stattdessen die folgende Struktur Definition:

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a>Globalisierung

Das Tool ist sprachneutral und kann in verschiedenen Sprachen lokalisiert werden. Alle Fehlermeldungen/Konsolenausgabe können lokalisiert werden. Die Befehlszeilenoptionen bleiben jedoch in englischer Sprache.

## <a name="environment-variable"></a>Umgebungsvariable

WsUtil.exe verwendet keine Umgebungsvariablen.

## <a name="platform-independent"></a>Plattformunabhängig

Ausgabedateien aus WsUtil.exe sind plattformunabhängig. Im Stub wurde kein Architektur abhängiger Code generiert. der C-Compiler kümmert sich um eine beliebige Architektur spezifischer. Der Stub kann auf allen Plattformen verwendet werden, die wir unterstützen.

Eine Beschreibung der wsutil.exe Ausgabe finden Sie unter [WSDL-Unterstützung](wsdl-support.md) und unter [Stützung für Schema Unterstützung](schema-support.md) .

 

 




