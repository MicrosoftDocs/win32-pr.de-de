---
title: Benutzerdefinierte Schriftartenkombinationen
description: In diesem Thema werden verschiedene Möglichkeiten beschrieben, wie Sie benutzerdefinierte Schriftarten in Ihrer APP verwenden können.
ms.assetid: 50842838-d150-df9a-f1b7-67ce5ea2bc80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a79f1ccfcb1dadd355c5f582417aacb5041ecf8b
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "104391204"
---
# <a name="custom-font-sets"></a>Benutzerdefinierte Schriftartenkombinationen

In diesem Thema werden verschiedene Möglichkeiten beschrieben, wie Sie benutzerdefinierte Schriftarten in Ihrer APP verwenden können.

-   [Einführung ](#introduction)
-   [Übersicht über die APIs](#summary-of-apis)
-   [Wichtige Begriffe](#key-concepts)
-   [Schriftarten und Schriftarten Dateiformate](#fonts-and-font-file-formats)
-   [Schriftart Sätze und Schriftart Sammlungen](#font-sets-and-font-collections)
-   [Gängige Szenarios](#common-scenarios)
    -   [Erstellen eines Schriftart Satzes mit beliebigen Schriftarten im lokalen Dateisystem](#creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system)
    -   [Erstellen eines Schriftart Satzes mit bekannten Schriftarten im lokalen Dateisystem](#creating-a-font-set-using-known-fonts-in-the-local-file-system)
    -   [Erstellen eines benutzerdefinierten Schriftart Satzes mit bekannten Remote Schriftarten im Web](#creating-a-custom-font-set-using-known-remote-fonts-on-the-web)
    -   [Erstellen eines benutzerdefinierten Schrift Satzes mit in den Arbeitsspeicher geladenen Schriftart Daten](#creating-a-custom-font-set-using-font-data-loaded-into-memory)
-   [Erweiterte Szenarios](#advanced-scenarios)
    -   [Kombinieren von Schriftart Sätzen](#combining-font-sets)
    -   [Verwenden von lokalen WOFF-oder WOFF2-Schriftart Daten ](#using-local-woff-or-woff2-font-data)
    -   [Verwenden von DirectWrite-Remote Schriftart Mechanismen mit benutzerdefinierter Netzwerk Implementierung auf niedriger Ebene ](#using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation)
    -   [Unterstützende Szenarien in früheren Windows-Versionen ](#supporting-scenarios-on-earlier-windows-versions)

## <a name="introduction"></a>Einführung

In den meisten Fällen verwenden Apps die Schriftarten, die lokal auf dem System installiert sind. DirectWrite ermöglicht den Zugriff auf diese Schriftarten mithilfe der Methoden [**IDWriteFactory3:: getsystemfontset**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) oder [**idschreitefactory:: getsystemfontcollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . In einigen Fällen möchten Apps möglicherweise auch Schriftarten verwenden, die als Teil von Windows 10 enthalten, aber zurzeit nicht auf dem aktuellen System installiert sind. Auf solche Schriftarten kann vom Windows-Schriftart Dienst mithilfe der **getsystemfontset** -Methode zugegriffen werden, oder durch Aufrufen von [**IDWriteFactory3:: getsystemfontcollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection) , wobei includedownloadablefonts auf true festgelegt ist. 

In manchen Anwendungsszenarien müssen apps jedoch Schriftarten verwenden, die nicht im System installiert sind und nicht vom Windows-Schriftart Dienst bereitgestellt werden. Im folgenden finden Sie Beispiele für derartige Szenarien:

-   Schriftarten werden als Ressourcen innerhalb einer APP-Binärdatei eingebettet.
-   Schriftart Dateien werden innerhalb eines App-Pakets gebündelt und auf dem Datenträger im Installationsordner der APP gespeichert.
-   Bei der App handelt es sich um ein Tool zur Schriftart Entwicklung, das benutzerdefinierte Schriftart Dateien laden muss. 
-   Schriftarten werden in Dokument Dateien eingebettet, die in der App angezeigt oder bearbeitet werden können. 
-   Die APP verwendet Schriftarten, die von einem öffentlichen Webschriftart Dienst abgerufen werden. 
-   Die APP verwendet Schriftart Daten, die über ein privates Netzwerkprotokoll gestreamt werden. 

DirectWrite stellt APIs zum Arbeiten mit benutzerdefinierten Schriftarten in diesen und anderen ähnlichen Szenarien bereit. Die benutzerdefinierten Schriftart Daten können aus Dateien im lokalen Dateisystem stammen. aus Remote cloudbasierten Quellen, auf die über HTTP zugegriffen wird oder aus beliebigen Quellen, nachdem Sie in einen Arbeitsspeicher Puffer geladen wurden. 

> [!Note]  
> Obwohl DirectWrite APIs zum Arbeiten mit benutzerdefinierten Schriftarten seit Windows 7 bereitgestellt hat, wurden neuere APIs in Windows 10 und erneut in Windows 10 Creators Update (Preview Build 15021 oder höher) hinzugefügt, die die Implementierung mehrerer der erwähnten Szenarien vereinfachen. Dieses Thema konzentriert sich auf APIs, die in Windows 10 verfügbar sind. Anwendungen, die in früheren Windows-Versionen funktionieren müssen, finden Sie unter [benutzerdefinierte Schriftart Auflistungen (Windows 7/8)](custom-font-collections.md). 

 

## <a name="summary-of-apis"></a>Übersicht über die APIs

In diesem Thema werden die Funktionen der folgenden APIs behandelt: 

-   [**Idschreitefontset**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) -Schnittstelle
-   [**Idschreitefontsetbuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) -Schnittstelle
-   [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) -Schnittstelle 
-   [**Idwrite Test fontfakereferenzierungsschnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)
-   [**Idschreitefontfile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) -Schnittstelle
-   [**Idschreitefactory:: kreatefontfilereferenzierungsmethode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) 
-   [**Idwrite Team Factory:: erkreatecustomfontfilereferenzierungsmethode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) 
-   [**IDWriteFactory3:: kreatefontfacereferenzierungsmethoden**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontresource-createfontfacereference) 
-   [**Dwrite \_ Schriftart \_ Eigenschafts**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) Struktur 
-   [**Dwrite \_ Schriftart- \_ Eigenschaften- \_ ID**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) -Enumeration 
-   [**Idschreitefontfileloader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) -Schnittstelle 
-   [**Idschreitefactory:: registerfontfileloader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader) -Methode 
-   [**Idschreitefactory:: unregisterfontfileloader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontfileloader) -Methode 
-   [**IDWriteFactory5:: kreateinmemoryfontfileloader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createinmemoryfontfileloader) -Methode 
-   [**Idwrite teinmemoryfontfileloader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) -Schnittstelle 
-   [**IDWriteFactory5:: kreatehttpfontfileloader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createhttpfontfileloader) -Methode 
-   [**Idschreiteremotefontfileloader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) -Schnittstelle 
-   [**Idschreitefontdownloadqueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) -Schnittstelle 
-   [**Idschreitefontdownloadlistener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) -Schnittstelle 
-   [**Idschreitefontfilestream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) -Schnittstelle 
-   [**Idschreiteremotefontfilestream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) -Schnittstelle 
-   [**Idschreiteasynkresult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) -Schnittstelle 
-   [**IDWriteFactory5:: analyzecontainertype**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-analyzecontainertype) -Methode 
-   [**IDWriteFactory5:: unpackfontfile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile) -Methode 

 

## <a name="key-concepts"></a>Wichtige Begriffe

Um die DirectWrite-APIs für die Arbeit mit benutzerdefinierten Schriftarten zu verstehen, kann es hilfreich sein, das konzeptionelle Modell zu verstehen, das diesen APIs zugrunde liegt. Wichtige Konzepte werden hier beschrieben. 

Wenn DirectWrite das tatsächliche Text Layout oder Rendering durchführt, muss es auf tatsächliche Schriftart Daten zugreifen. Ein Schriftart Objekt enthält tatsächliche Schriftart Daten, die im lokalen System vorhanden sein müssen. Für andere Vorgänge, wie z. b. das Überprüfen der Verfügbarkeit einer bestimmten Schriftart oder das darstellen von Schriftart Optionen für einen Benutzer, benötigen Sie lediglich einen Verweis auf eine bestimmte Schriftart, nicht die eigentlichen Schriftart Daten. In DirectWrite enthält ein Schriftart Referenzobjekt nur die Informationen, die erforderlich sind, um eine Schriftart zu suchen und zu instanziieren. Da der Verweis auf die Schriftart nicht die eigentlichen Daten enthält, kann DirectWrite mit Verweisen auf die Schriftart für die Schriftart umgehen, bei denen sich die tatsächlichen Daten an einem Remote Netzwerk Speicherort befinden und die eigentlichen Daten lokal sind.

Bei einem Schriftart Satz handelt es sich um einen Satz von Schriftart verweisen sowie bestimmte grundlegende Informations Eigenschaften, die verwendet werden können, um auf die Schriftart zu verweisen oder um Sie mit anderen Schriftarten zu vergleichen, wie z. b. dem Familiennamen oder einem Wert für die Schrift Breite. Die tatsächlichen Daten für die verschiedenen Schriftarten können lokal sein, oder es kann sich um eine Remote-oder eine Mischung handeln.

Ein Schriftart Satz kann verwendet werden, um ein entsprechendes Schriftart Sammlungsobjekt abzurufen. Weitere Informationen finden Sie unten unter Schriftart Sätze und Schriftart Auflistungen. 

Die idwrite-FONTSET-Schnittstelle stellt Methoden bereit, die das Abfragen von Eigenschafts Werten ermöglichen, z. b. Familienname oder Schrift Breite, oder für Verweise auf Schriftart, die bestimmten Eigenschafts Werten entsprechen. Nach dem Filtern auf eine bestimmte Auswahl kann eine Instanz der [**idwrite-fontfacereferenzierungsschnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) mit Methoden zum Herunterladen abgerufen werden (wenn die eigentlichen Schriftart Daten derzeit Remote sind), um das entsprechende [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) -Objekt zu erhalten, das für Layout und Rendering verwendet werden kann. 

Die idwrite-fontfile-Schnittstelle unterliegt den einzelnen Schriftart-oder Schriftart verweisen. Dies stellt den Speicherort einer Schriftart Datei dar und verfügt über zwei Komponenten: einen Schriftart Datei Lader und einen Schriftart Datei Schlüssel. Das Schriftart Datei Lade Tool ([**idschreitefontfileloader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader)) wird verwendet, um bei Bedarf eine Datei zu öffnen, und gibt einen Stream mit den Daten ([**idschreitefontfilestream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)) zurück. Abhängig vom Lade Modul befinden sich die Daten möglicherweise in einem lokalen Dateipfad, einer Remote-URL oder in einem Arbeitsspeicher Puffer. Der Schlüssel ist ein vom Lade Modul definierter Wert, der die Datei im Lade Lade Kontext eindeutig identifiziert und dem Lade Modul ermöglicht, die Daten zu finden und einen Stream dafür zu erstellen. 

Benutzerdefinierte Schriftarten können einfach zu einem benutzerdefinierten Schriftart Satz hinzugefügt werden, der wiederum zum Filtern oder organisieren von Schriftart Informationen verwendet werden kann, z. b. zum Erstellen einer Benutzeroberfläche mit Schriftart Auswahl. Der Schriftart Satz kann auch verwendet werden, um eine Schriftart Auflistung für die Verwendung in APIs auf höherer Ebene zu erstellen, wie z. b. [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) und [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). Die [**idwrite-fontsetbuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) -Schnittstelle kann verwendet werden, um einen benutzerdefinierten Schriftart Satz zu erstellen, der mehrere benutzerdefinierte Schriftarten umfasst. Sie kann auch verwendet werden, um einen benutzerdefinierten Schriftart Satz zu erstellen, der benutzerdefinierte Schriftarten und vom System bereitgestellte Schriftarten kombiniert. oder, das Schriftarten mit verschiedenen Quellen für die eigentlichen Daten kombiniert – lokaler Speicher, Remote-URLs und Arbeitsspeicher. 

Wie bereits erwähnt, kann ein Verweis auf die Schriftart auf Schriftart Daten an einer Remote Quelle verweisen, aber die Daten müssen lokal sein, um ein Schriftart Objekt zu erhalten, das für Layout und Rendering verwendet werden kann. Das Herunterladen von Remote Daten erfolgt durch eine Schriftart Download Warteschlange. Apps können die [**idwrite-fontdownloadqueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) -Schnittstelle verwenden, um Anforderungen zum Herunterladen von Remote Schriftarten in die Warteschlange zu stellen, um den Downloadvorgang zu initiieren und ein [**idwrite-fontdownloadlistener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) -Objekt zu registrieren, um beim Abschluss des Downloadvorgangs Maßnahmen zu ergreifen. 

Für die meisten Schnittstellen, die hier beschrieben werden, bietet DirectWrite System Implementierungen. Die einzige Ausnahme ist die [**idwrite-fontdownloadlistener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) -Schnittstelle, die eine APP implementiert, um App-spezifische Aktionen auszuführen, wenn Remote Schriftarten lokal heruntergeladen wurden. Apps können einen Grund haben, eigene benutzerdefinierte Implementierungen für bestimmte andere Schnittstellen bereitzustellen, die jedoch nur in bestimmten, komplexeren Szenarien benötigt werden. Beispielsweise müsste eine APP eine benutzerdefinierte Implementierung der [**idschreitefontfileloader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) -Schnittstelle bereitstellen, um Schriftart Dateien im lokalen Speicher zu verarbeiten, die das WOFF2-Containerformat verwenden. Unten finden Sie weitere Details. 

## <a name="fonts-and-font-file-formats"></a>Schriftarten und Schriftarten Dateiformate

Ein weiteres wichtiges Konzept, das zum Verständnis hilfreich ist, ist die Beziehung zwischen einzelnen Schriftart-und Schriftart Dateien, die Sie enthalten. Die Idee einer OpenType-Schriftart Datei (. ttf oder. OTF), die eine einzelne Schriftart enthält, ist vertraut. Das OpenType-Schriftformat ermöglicht jedoch auch eine OpenType-Schriftart Auflistung (. TTC oder. OTC), bei der es sich um eine einzelne Datei handelt, die mehrere Schriftarten enthält. OpenType-Auflistungs Dateien werden häufig für große Schriftarten verwendet, die eng miteinander verknüpft sind und identische Werte für bestimmte Schriftart Daten aufweisen: indem die Schriftarten in einer einzelnen Datei kombiniert werden, können die allgemeinen Daten dupliziert werden. Aus diesem Grund muss ein Schriftart-oder Schriftart Referenz Verweis nicht nur auf eine Schriftart Datei (oder eine entsprechende Datenquelle) verweisen, sondern auch einen Schriftart Index in dieser Datei angeben, für den allgemeinen Fall, in dem die Datei eine Sammlungs Datei sein kann. 

Bei im Web verwendeten Schriftarten werden Schriftart Daten häufig in bestimmte Containerformate, WOFF oder WOFF2 verpackt, die eine Komprimierung der Schriftart Daten und ein gewisses Maß an Schutz vor Piraterie und Verletzung von Schriftart Lizenzen bereitstellen. Funktional, eine WOFF-oder WOFF2-Datei entspricht einer OpenType-Schriftart oder einer Schriftart Sammlungs Datei, aber die Daten werden in einem anderen Format codiert, das entpackt werden muss, bevor es verwendet werden kann. 

Bestimmte DirectWrite-APIs verarbeiten möglicherweise einzelne Schriftart Flächen, während andere APIs Dateien verarbeiten können, die möglicherweise OpenType-Auflistungs Dateien enthalten, die mehrere Gesichter enthalten. Ebenso befassen sich bestimmte APIs nur mit unformatierten Daten im OpenType-Format, während andere APIs die gepackten, WOFF-und WOFF2-Containerformate verarbeiten können. Diese Details werden in der nachfolgenden Diskussion bereitgestellt. 

## <a name="font-sets-and-font-collections"></a>Schriftart Sätze und Schriftart Sammlungen

Einige Anwendungen können für die Arbeit mit Schriftarten mithilfe der [**idschreitefontcollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) -Schnittstelle implementiert werden. Es gibt eine direkte Entsprechung zwischen einer Schriftart Auflistung und einem Schriftart Satz. Jede kann die gleichen Schriftarten enthalten, Sie stellen Sie jedoch einer anderen Organisation zur Verfügung. Aus einer beliebigen Schriftart Auflistung kann ein entsprechender Schriftart Satz abgerufen werden und umgekehrt.

Wenn Sie mit einer Reihe von benutzerdefinierten Schriftarten arbeiten, ist es am einfachsten, eine Schriftart Satz-Generator-Schnittstelle zum Erstellen eines benutzerdefinierten Schriftart Satzes zu verwenden und dann eine Schriftart Auflistung abzurufen, nachdem der Schriftsatz erstellt wurde. Der Vorgang zum Erstellen eines benutzerdefinierten Schriftart Satzes wird im folgenden ausführlich beschrieben. Zum Abrufen einer [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) -Schnittstelle aus einem Schriftart Satz wird die [**IDWriteFactory3:: kreatefontcollectionfromfontset**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-createfontcollectionfromfontset) -Methode verwendet.

Wenn die APP über ein Auflistungs Objekt verfügt und einen entsprechenden Schriftart Satz abrufen muss, kann dies mithilfe der [**IDWriteFontCollection1:: getfontset**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontcollection1-getfontset) -Methode erfolgen. 

## <a name="common-scenarios"></a>Häufige Szenarien

In diesem Abschnitt werden einige der gängigsten Szenarien im Zusammenhang mit benutzerdefinierten Schriftart Sätzen beschrieben:

-   Erstellen eines benutzerdefinierten Schriftart Satzes mit beliebigen Schriftarten in Pfaden im lokalen Dateisystem.
-   Erstellen eines benutzerdefinierten Schrift Satzes mit bekannten Schriftarten (möglicherweise mit der APP gebündelt), die im lokalen Dateisystem gespeichert sind.
-   Erstellen eines benutzerdefinierten Schriftart Satzes mit bekannten Remote Schriftarten im Web.
-   Erstellen eines benutzerdefinierten Schrift Satzes mit Schriftart Daten, die in den Arbeitsspeicher geladen werden.

Umfassende Implementierungen für diese Szenarien finden Sie im [Beispiel für benutzerdefinierte DirectWrite-Schriftart Sätze](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). Dieses Beispiel veranschaulicht auch ein erweitertes Szenario für die Behandlung von Schriftart Daten, die in WOFF-oder WOFF2-Containerformaten gepackt sind, die im folgenden erläutert werden. 

### <a name="creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system"></a>Erstellen eines Schriftart Satzes mit beliebigen Schriftarten im lokalen Dateisystem

Beim Umgang mit einem beliebigen Satz von Schriftart Dateien im lokalen Speicher ist die [**IDWriteFontSetBuilder1:: AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) -Methode praktisch, da Sie in einem einzelnen-Befehl alle Schriftart Gesichter innerhalb einer OpenType-Schriftart Sammlungs Datei sowie alle Instanzen für eine OpenType-Variablen Schriftart verarbeiten kann. Diese ist in Windows 10 Creators Update (Preview Build 15021 oder höher) verfügbar und wird empfohlen, wenn verfügbar. 

Verwenden Sie den folgenden Prozess, um diese Methode zu verwenden.

<dl> 1. Beginnen Sie mit dem Erstellen der <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5">IDWriteFactory5</a> -Schnittstelle: 


```C++
IDWriteFactory5* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
  DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



   
2. Verwenden Sie die Factory zum Abrufen der <a href=""></a> [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) -Schnittstelle: 


```C++
IDWriteFontSetBuilder1* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
}  
                
```



  
3. Erstellen Sie für jede Schriftart Datei im lokalen Dateisystem eine [**idwrite-fontfile-Datei**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) , die darauf verweist: 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



   
4. Fügen Sie das [**idwrite-fontfile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) -Objekt dem Schriftart Satz-Generator mithilfe der [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) -Methode hinzu: 


```C++
hr = pFontSetBuilder->AddFontFile(pFontFile); 
```

Wenn der Dateipfad, der beim Aufrufen von " [**anatefontfilereferenzierung**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) " angegeben wurde, etwas anderes als eine unterstützte OpenType-Datei referenziert ist, wird beim Aufrufen von " [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) " der Fehler "dwrite \_ E File Format" zurückgegeben \_ .

5. Nachdem alle Dateien dem Schriftart Satz-Generator hinzugefügt wurden, kann der benutzerdefinierte Schriftart Satz erstellt werden: 


```C++
IDWriteFontSet* pFontSet; 
hr = pFontSetBuilder->CreateFontSet(&pFontSet); 
```



   
</dl>

Wenn die APP auf Windows 10-Versionen vor Windows 10 Creators Update ausgeführt werden muss, ist die AddFontFile-Methode nicht verfügbar. Die Verfügbarkeit kann durch Erstellen einer [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) -Schnittstelle und anschließendes Verwenden von QueryInterface zum Abrufen einer [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) -Schnittstelle erkannt werden: Wenn dies erfolgreich ist, sind auch die [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) -Schnittstelle und die [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) -Methode verfügbar.

Wenn die AddFontFile-Methode nicht verfügbar ist, muss die [**idwrite-fontsetbuilder:: addfontfacereferenzierungsmethode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) zum Hinzufügen einzelner Schriftart Flächen verwendet werden. Um Dateien mit OpenType-Schriftarten Auflistungen zuzulassen, die mehrere Gesichter enthalten, kann die [**idschreitefontfile:: Analysis**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) -Methode verwendet werden, um die Anzahl der in der Datei enthaltenen Gesichter zu bestimmen. Der Prozess ist wie folgt.

<dl> 1. Beginnen Sie mit dem Erstellen der <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3</a> -Schnittstelle: 


```C++
IDWriteFactory3* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



  
2. Verwenden Sie die Factory zum Abrufen der [**idschreitefontsetbuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) -Schnittstelle: 


```C++
IDWriteFontSetBuilder* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
} 
```



  
3. Erstellen Sie für jede Schriftart Datei wie oben beschrieben eine [**idschreitefontfile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile): 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



Anstatt die Datei direkt dem Schriftart Satz-Generator hinzuzufügen, müssen wir die Anzahl der Gesichter ermitteln und einzelne [**idwrite-fontfakereferenzierungsobjekte**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) erstellen.   
4. Verwenden Sie die Methode [**analysieren**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) , um die Anzahl der Gesichter in der Datei zu erhalten. 


```C++
BOOL isSupported; 
DWRITE_FONT_FILE_TYPE fileType; 
UINT32 numberOfFonts; 
hr = pFontFile->Analyze(&isSupported, &fileType, /* face type */ nullptr, &numberOfFonts); 
```



Die [**Analyse**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) Methode legt auch Werte für die Parameter "IsSupported" und "filetype" fest. Wenn es sich bei der Datei nicht um ein unterstütztes Format handelt, ist IsSupported false, und die entsprechende Aktion (z. b. das Ignorieren der Datei) kann durchgeführt werden.   
5. Schleife über die Anzahl von Schriftarten, die im Parameter "numoffonts" festgelegt sind. Erstellen Sie innerhalb der-Schleife eine [**idwrite-fontfakereferenzierung**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) für jedes Datei-/Index-Paar, und fügen Sie diese dem Schriftart Satz-Generator hinzu. 


```C++
for (uint32_t fontIndex = 0; fontIndex < numberOfFonts; fontIndex++) 
{ 
  IDWriteFontFaceReference* pFontFaceReference;
  hr = pDWriteFactory->CreateFontFaceReference(pFontFile, fontIndex, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);

  if (SUCCEEDED(hr))
  {
    hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference);
  }
} 
```



  
6. Nachdem alle Gesichter zum Schriftart Satz-Generator hinzugefügt wurden, erstellen Sie den benutzerdefinierten Schriftart Satz, wie oben gezeigt.  
</dl>

Eine APP kann so entworfen werden, dass Sie die bevorzugte [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) -Methode verwendet, wenn Sie auf dem Windows 10 Creators Update ausgeführt wird, aber bei Ausführung unter früheren Windows 10-Versionen die [**addfontfacereferenzierungsmethode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) verwenden. Testen Sie die Verfügbarkeit der [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) -Schnittstelle, wie oben beschrieben, und Verzweigen Sie dann entsprechend. Diese Vorgehensweise wird im [Beispiel für benutzerdefinierte DirectWrite-Schriftart Sätze](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)veranschaulicht. 

### <a name="creating-a-font-set-using-known-fonts-in-the-local-file-system"></a>Erstellen eines Schriftart Satzes mit bekannten Schriftarten im lokalen Dateisystem

Wie bereits erwähnt, ist jeder Schriftart Verweis in einem Schriftart Satz bestimmten Informations Eigenschaften zugeordnet, z. b. dem Familiennamen und der Schrift Breite. Wenn einem Schriftart Satz-Generator mithilfe der oben aufgeführten API-Aufrufe benutzerdefinierte Schriftarten hinzugefügt werden, werden diese Informations Eigenschaften direkt aus den eigentlichen Schriftart Daten abgerufen, die beim Hinzufügen der Schriftart gelesen werden. In einigen Situationen kann es jedoch vorkommen, dass eine APP eine andere Quelle von Informationen über eine Schriftart enthält, wenn Sie jedoch auch eigene benutzerdefinierte Werte für diese Eigenschaften bereitstellen möchten. 

Ein Beispiel dafür, wie dies nützlich sein kann, besteht darin, dass eine APP einige Schriftarten bündeln, die für die Darstellung bestimmter Benutzeroberflächen Elemente innerhalb der APP verwendet werden. Zu Zeiten, z. b. mit einer neuen App-Version, müssen sich die für diese Elemente verwendeten Schriftarten möglicherweise ändern. Wenn die APP Verweise auf bestimmte Schriftarten codiert hat, muss bei der Ersetzung einer Schriftart mit einer anderen eine Schriftart geändert werden. Wenn die APP stattdessen benutzerdefinierte Eigenschaften verwendet, um funktionale Aliase basierend auf dem Typ des gerenderten Elements oder Texts zuzuweisen, ordnet jeden Alias an einem Ort einer bestimmten Schriftart zu und verwendet dann die Aliase in allen Kontexten, in denen Schriftarten erstellt und manipuliert werden. Anschließend wird eine Schriftart durch andere ersetzt 

Benutzerdefinierte Werte für Informations Eigenschaften können zugewiesen werden, wenn die [**idwrite-fontsetbuilder:: addfontfacereferenzierungsmethode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) aufgerufen wird. Die Methode hierfür lautet wie folgt: Dies kann für jede Windows 10-Version verwendet werden. 

Beginnen Sie wie oben gezeigt mit dem Abrufen der Schnittstellen [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) und [**idschreitefontset**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) . Erstellen Sie für jede benutzerdefinierte Schriftart, die hinzugefügt werden soll, eine [**idschreitefontfakereferenzierung**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference), wie oben gezeigt. Bevor diese zum Schriftart Satz-Generator hinzugefügt wird (in der-Schleife in Schritt 5, siehe oben), definiert die APP jedoch die zu verwendenden benutzerdefinierten Eigenschaftswerte. 

Ein Satz benutzerdefinierter Eigenschaftswerte wird mithilfe eines Arrays von [**dwrite- \_ Schriftart \_ Eigenschafts**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) Strukturen definiert. Jede dieser Eigenschaften gibt eine bestimmte Eigenschaft aus der [**dwrite- \_ Schriftart- \_ Eigenschaften- \_ ID**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) -Enumeration und den entsprechenden Eigenschafts Wert an, der verwendet werden soll.  

Beachten Sie, dass alle Eigenschaftswerte als Zeichen folgen zugewiesen werden. Wenn diese später Benutzern angezeigt werden, werden möglicherweise alternative Werte für eine bestimmte Eigenschaft für verschiedene Sprachen festgelegt, dies ist jedoch nicht erforderlich. Beachten Sie auch Folgendes: Wenn benutzerdefinierte Eigenschaftswerte von der APP festgelegt werden, werden nur die angegebenen Werte innerhalb des Schrift Satzes verwendet. DirectWrite leitet keine Werte direkt aus der Schriftart für Informations Eigenschaften ab, die in einem Schriftart Satz verwendet werden. 

Im folgenden Beispiel werden benutzerdefinierte Werte für drei Informations Eigenschaften definiert: Family Name, Full Name und Font Weight. 


```C++
DWRITE_FONT_PROPERTY props[] = 
{ 
  { DWRITE_FONT_PROPERTY_ID_FAMILY_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_FULL_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_WEIGHT, L"400", nullptr } 
}; 
               
            
```



Nachdem Sie das gewünschte Array von Eigenschafts Werten für eine Schriftart definiert haben, führen Sie einen Anrufe an addfontfakerefence aus, und übergeben Sie dabei das Eigenschafts Array sowie den Schriftart Verweis. 


```C++
hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference, props, ARRAYSIZE(props)); 
```



 

Nachdem alle benutzerdefinierten Schriftart Flächen zum Schriftart Satz-Generator hinzugefügt wurden, erstellen Sie zusammen mit den benutzerdefinierten Eigenschaften den benutzerdefinierten Schriftart Satz, wie oben gezeigt. 

### <a name="creating-a-custom-font-set-using-known-remote-fonts-on-the-web"></a>Erstellen eines benutzerdefinierten Schriftart Satzes mit bekannten Remote Schriftarten im Web

Benutzerdefinierte Eigenschaften sind wichtig für die Arbeit mit Remote Schriftarten. Jeder Schriftart Verweis muss einige Informations Eigenschaften aufweisen, um die Schriftart zu charakterisieren und von anderen Schriftarten zu unterscheiden. Da die Schriftart Daten für Remote Schriftarten nicht lokal sind, kann DirectWrite Eigenschaften nicht direkt aus den Schriftart Daten ableiten. Daher müssen Eigenschaften beim Hinzufügen einer Remote Schriftart zum Schriftart Satz-Generator explizit bereitgestellt werden.

Die Sequenz von API-aufrufen zum Hinzufügen von Remote Schriftarten zu einem Schriftart Satz ähnelt der für das vorherige Szenario beschriebenen Sequenz. Da es sich bei den Schriftart Daten um Remote Daten handelt, unterscheiden sich die zum Lesen der eigentlichen Schriftart Daten beteiligten Vorgänge von der Arbeit mit Dateien im lokalen Speicher. In dieser Situation wurde dem Windows 10 Creators Update eine neue Unterebene ( [**idbeschreib teremotefontfileloader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader)) hinzugefügt. 

Um das Remote Schriftart Datei-Lade Tool zu verwenden, muss es zuerst bei einer DirectWrite-Factory registriert werden. Das Lade Modul muss von der APP aufbewahrt werden, solange die damit verbundenen Schriftarten verwendet werden. Wenn die Schriftarten nicht mehr verwendet werden, und bevor die Factory zerstört wird, muss die Registrierung des Lade Moduls aufgehoben werden. Dies kann im Dekonstruktor für die Klasse erfolgen, die das Loader-Objekt besitzt. Diese Schritte werden unten dargestellt. 

Die Methode zum Erstellen eines benutzerdefinierten Schriftart Satzes mit Remote Schriftarten lautet wie folgt: hierfür ist das Windows 10 Creators Update erforderlich.  

<dl> 1. Erstellen Sie eine IDWriteFactory5-Schnittstelle, wie oben gezeigt.   
2. Erstellen Sie eine <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">idschreitefontsetbuilder</a> -Schnittstelle, wie oben gezeigt.   
3. Verwenden Sie die Factory zum Abrufen eines <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader">idschreiteremotefontfileloader</a>. 


```C++
IDWriteRemoteFontFileLoader* pRemoteFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateHttpFontFileLoader( 
        /* referrerURL */ nullptr, 
        /* extraHeaders */ nullptr, 
        &pRemoteFontFileLoader 
    ); 
} 
```



Dies gibt eine vom System bereitgestellte Implementierung der Remote Schriftart Datei-Lade Tool Schnittstelle zurück, die HTTP-Interaktionen für das Herunterladen von Schriftart Daten im Auftrag der APP verarbeiten kann. Eine referenrer-URL oder zusätzliche Header können angegeben werden, wenn Sie für den Schriftart Dienst oder die Dienste, die die Quelle für die Schriftarten sind, erforderlich sind.    

> [!IMPORTANT]
> Sicherheitshinweis: beim Versuch, eine Remote Schriftart abzurufen, besteht die Möglichkeit, dass ein Angreifer den vorgesehenen Server SPO, der aufgerufen wird. In diesem Fall werden die Ziel-und Verweiser-URLs und Header Details dem Angreifer offengelegt. App-Entwickler sind dafür verantwortlich, dieses Risiko zu mindern. Es wird empfohlen, anstelle von http das HTTPS-Protokoll zu verwenden. 

 

Ein einzelnes Remote-Schriftart Datei-Lade Tool kann für mehrere Schriftarten verwendet werden, obwohl verschiedene Lade Programme verwendet werden können, wenn Schriftarten von mehreren Diensten abgerufen werden, die unterschiedliche Anforderungen an die Verweis-URL oder zusätzliche Header haben.   
4. Registrieren Sie das Remote Schriftart Datei-Lade Tool bei der Factory. 


```C++
 if (SUCCEEDED(hr)) 
 { 
     hr = pDWriteFactory->RegisterFontFileLoader(pRemoteFontFileLoader); 
 } 
```



Ab diesem Zeitpunkt sind die Schritte zum Erstellen des benutzerdefinierten Schriftart Satzes mit den für bekannte, lokale Schriftart Dateien beschriebenen Schritten vergleichbar, die zwei wichtige Ausnahmen haben. Zuerst wird das [**idwrite-fontfile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) -Objekt über die Remote-Schriftart Datei-Lade Tool Schnittstelle erstellt, anstatt die Factory zu verwenden. Zweitens kann die Analysemethode nicht verwendet werden, da die Schriftart Daten nicht lokal sind. Stattdessen muss die APP wissen, ob es sich bei der Remote Schriftart Datei um eine OpenType-Schriftart Sammlungs Datei handelt. wenn dies der Fall ist, muss Sie wissen, welche der Schriftarten in der Auflistung verwendet werden soll, sowie den Index für jede. Folglich sind die restlichen Schritte wie folgt.   
5. Verwenden Sie für jede Remote Schriftart Datei die Remote Schriftart-Datei Lade Tool-Schnittstelle, um eine [**idwrite-fontfile-Datei**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)zu erstellen, die die URL angibt, die für den Zugriff auf die Schriftart Datei 


```C++
 IDWriteFontFile* pFontFile; 
 hr = pRemoteFontFileLoader->CreateFontFileReferenceFromUrl( 
     pDWriteFactory, 
     /* baseUrl */ L"https://github.com/", 
     /* fontFileUrl */ L"winjs/winjs/blob/master/src/fonts/Symbols.ttf?raw=true", 
     &pFontFile 
 ); 
```



Beachten Sie, dass die gesamte URL im fontfileurl-Parameter angegeben werden kann, oder Sie kann in Basis-und relative Teile aufgeteilt werden. Wenn eine Basis-URL angegeben wird, muss die Verkettung der Werte baseurl und fontfileurl die vollständige URL bereitstellen – DirectWrite stellt kein zusätzliches Trennzeichen bereit.  

> [!IMPORTANT]
> Sicherheits-/Leistungshinweis: beim Versuch, eine Remote Schriftart abzurufen, gibt es keine Garantie dafür, dass Windows eine Antwort vom Server empfängt. In einigen Fällen antwortet ein Server möglicherweise mit einem Fehler aufgrund einer Datei nicht gefunden für einen ungültigen relative URL, reagiert jedoch nicht mehr, wenn er mehrere ungültige Anforderungen empfängt. Wenn der Server nicht antwortet, wird von Windows schließlich ein Timeout ausgelöst. Dies kann jedoch einige Minuten in Anspruch nehmen, wenn mehrere Abruf Vorgänge initiiert werden. Sie sollten das tun, was Sie tun können, um sicherzustellen, dass URLs gültig sind, wenn Aufrufe durchgeführt werden. 

 

Beachten Sie auch, dass die URL auf eine unformatierte OpenType-Schriftart Datei (. ttf,. OTF,. TTC,. OTC) verweisen kann, aber auch auf Schriftarten in einer WOFF-oder WOFF2-Containerdatei verweisen kann. Wenn auf eine WOFF-oder WOFF2-Datei verwiesen wird, entpackt die DirectWrite-Implementierung des Remote Schriftart Datei-Lade Moduls automatisch die Schriftart Daten aus der Containerdatei.   
6. Erstellen Sie für jeden Schriftart Index der Schriftart in der zu verwendenden Remote Schriftart Datei eine [**idwrite-fontfakereferenzierung**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference). 


```C++
 IDWriteFontFaceReference* pFontFaceReference; 
 hr = pDWriteFactory->CreateFontFaceReference(pFontFile, /* faceIndex */ 0, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);
```



  
7. Definieren Sie benutzerdefinierte Eigenschaften für das Schriftart Gesicht, wie oben gezeigt.   
8. Fügen Sie dem Schriftart Satz-Generator, wie oben gezeigt, den Schriftart Verweis auf Schriftart zusammen mit benutzerdefinierten Eigenschaften hinzu.   
9. Nachdem dem Schriftart Satz-Generator alle Schriftarten hinzugefügt wurden, erstellen Sie wie oben gezeigt den Schriftart Satz.   
10. Wenn die Remote Schriftarten nicht mehr verwendet werden, heben Sie die Registrierung des Remote Schriftart Datei-Lade Moduls auf. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pRemoteFontFileLoader); 
```



  
</dl>

Sobald ein benutzerdefinierter Schriftart Satz mit benutzerdefinierten Remote Schriftarten erstellt wurde, enthält der Schriftart Satz Verweise und Informations Eigenschaften für die Remote Schriftarten, aber die tatsächlichen Daten sind immer noch Remote. Die DirectWrite-Unterstützung für Remote Schriftarten ermöglicht das Beibehalten eines Schriftart Verweises im Schrift Schnitt und das Auswählen einer Schriftart für die Verwendung im Layout und Rendering, aber die tatsächlichen Daten werden erst heruntergeladen, wenn Sie tatsächlich benötigt werden, z. b. wenn das Text Layout ausgeführt wird.  

Eine APP kann einen vorab Ansatz ergreifen, indem Sie anfordert, dass DirectWrite die Schriftart Daten herunterlädt und dann auf die Bestätigung eines erfolgreichen Downloads wartet, bevor eine Verarbeitung mit der Schriftart begonnen wird. Ein Netzwerk Download impliziert jedoch eine Latenz der unvorhersehbaren Dauer, und der Erfolg ist auch unsicher. Aus diesem Grund ist es normalerweise besser, einen anderen Ansatz zu verwenden, sodass Layout und Rendering anfänglich mit alternativen oder Fall Back Schriftarten durchgeführt werden können, die bereits lokal sind. gleichzeitig wird der Download der gewünschten Remote Schriftart parallel angefordert, und die Ergebnisse werden aktualisiert, sobald die gewünschte Schriftart heruntergeladen wurde. 

Um anzufordern, dass die gesamte Schriftart vor der Verwendung heruntergeladen wird, kann die [**idwrite-fontfacereferenzierungsmethode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuefontdownloadrequest) verwendet werden. Wenn die Schriftart sehr groß ist, ist möglicherweise nur ein Teil der Daten für die Verarbeitung bestimmter Zeichen folgen erforderlich. DirectWrite stellt zusätzliche Methoden bereit, mit denen Teile der Schriftart Daten angefordert werden können, die für bestimmte Inhalte, [**enqueuecharakteridownloadrequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuecharacterdownloadrequest) und [**enqueueglyphdownloadrequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueueglyphdownloadrequest)benötigt werden.  

Angenommen, der Ansatz, der in der APP verwendet werden soll, besteht darin, die Verarbeitung zunächst mit lokalen, Alternativen oder Fall Back Schriftarten durchgeführt zu haben. Die idwrite-fontfallback::[**mapcharacters**](idwritefontfallback-mapcharacters.md) -Methode kann verwendet werden, um lokale Fall Back-Schriftarten zu identifizieren, und eine Anforderung zum Herunterladen der bevorzugten Schriftart wird automatisch in die Warteschlange eingereiht. Wenn [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) verwendet wird und ein Teil oder der gesamte Text im Layout mithilfe eines Remote-Schriftart Verweises formatiert wird, verwendet DirectWrite automatisch die **mapcharacters** -Methode, um lokale Fall Back-Schriftarten zu erhalten und eine Anforderung zum Herunterladen der Remote Schriftart Daten in die Warteschlange zu stellen. 

DirectWrite verwaltet eine Schriftart Download Warteschlange für jede Factory, und die mit den oben erwähnten Methoden erfolgten Anforderungen werden dieser Warteschlange hinzugefügt. Die Schriftart Download Warteschlange kann mithilfe der [**IDWriteFactory3:: getfontdownloadqueue**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getfontdownloadqueue) -Methode abgerufen werden. 

Wenn eine Download Anforderung erfolgt ist, aber die Schriftart Daten bereits lokal sind, führt dies zu einem No-op-Vorgang: nichts wird der Download Warteschlange hinzugefügt. Eine APP kann überprüfen, ob die Warteschlange leer ist oder ob ausstehende Download Anforderungen vorhanden sind, indem die [**idwrite-fontdownloadqueue:: IsEmpty**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-isempty) -Methode aufgerufen wird. 

Nachdem der Warteschlange Remote-Schriftart Anforderungen hinzugefügt wurden, muss der Downloadvorgang initiiert werden. Wenn Remote Schriftarten in [**idwrite-Text Layout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)verwendet werden, wird der Download automatisch initiiert, wenn die APP **idschreitetextlayout** -Methoden aufruft, die Layout-oder Renderingvorgänge erzwingen, wie z. b. getLineMetrics oder Draw-Methoden. In anderen Szenarien muss die APP den Download direkt initiieren, indem Sie " [**idschreitefontdownloadqueue:: BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload)" aufrufen.  

Wenn ein Download abgeschlossen ist, muss die APP die entsprechenden Aktionen ausführen – mit ausstehenden Vorgängen oder wiederholten Vorgängen, die anfänglich mit Fall Back Schriftarten durchgeführt wurden. (Wenn das Text Layout von DirectWrite verwendet wird, kann [**IDWriteTextLayout3:: invalidatelayout**](idwritetextlayout3-invalidatelayout.md) verwendet werden, um die temporären Ergebnisse zu löschen, die mithilfe von Fall Back-Schriftarten berechnet werden.) Damit die APP benachrichtigt wird, wenn der Downloadvorgang abgeschlossen ist, und um entsprechende Aktionen durchführen zu können, muss die APP eine Implementierung der [**idschreitefontdownloadlistener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) -Schnittstelle bereitstellen und diese an den BeginDownload-Befehl übergeben. 

> [!IMPORTANT]
> Sicherheits-/Leistungshinweis: beim Versuch, eine Remote Schriftart abzurufen, gibt es keine Garantie dafür, dass Windows eine Antwort vom Server empfängt. Wenn der Server nicht antwortet, tritt bei Windows schließlich ein Timeout auf, dies kann jedoch einige Minuten in Anspruch nehmen, wenn mehrere Remote Schriftarten abgerufen werden, aber nicht. Der BeginDownload-Befehl wird sofort zurückgegeben. Apps sollten die Benutzeroberfläche nicht blockieren, während darauf gewartet wird, dass [**idwrite-fontdownloadlistener::D ownloadabgeschlossene**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadlistener-downloadcompleted) aufgerufen wird. 

 

Beispiel Implementierungen dieser Interaktionen mit der Schriftart Download Warteschlange von DirectWrite und der [**idschreitefontdownloadlistener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) -Schnittstelle finden Sie im [Beispiel zu benutzerdefinierten DirectWrite-Schriftart Sätzen](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)und auch im Beispiel für das [herunterladbare Verzeichnis von DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont). 

### <a name="creating-a-custom-font-set-using-font-data-loaded-into-memory"></a>Erstellen eines benutzerdefinierten Schrift Satzes mit in den Arbeitsspeicher geladenen Schriftart Daten

Ebenso wie die Low-Level-Vorgänge zum Lesen von Daten aus einer Schriftart Datei für Dateien auf einem lokalen Datenträger und Remote Dateien im Web unterscheiden, gilt dasselbe auch für Schriftart Daten, die in einen Arbeitsspeicher Puffer geladen werden. In Windows 10 Creators Update, [**idschreiteinmemoryfontfileloader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader), wurde eine neue Low-Level-Schnittstelle zum Verarbeiten von Schriftart Daten im Arbeitsspeicher hinzugefügt. 

Wie bei einem Remote-Schriftart Datei Lade Tool muss ein Schriftart Datei-Lade Tool in-Memory zuerst bei einer DirectWrite-Factory registriert werden. Das Lade Modul muss von der APP aufbewahrt werden, solange die damit verbundenen Schriftarten verwendet werden. Wenn die Schriftarten nicht mehr verwendet werden, und bevor die Factory zerstört wird, muss die Registrierung des Lade Moduls aufgehoben werden. Dies kann im Dekonstruktor für die Klasse erfolgen, die das Loader-Objekt besitzt. Diese Schritte werden unten dargestellt. 

Wenn die APP getrennte Informationen über die von den Daten dargestellten Schriftart Gesichter enthält, kann Sie einzelne Schriftart Verweise auf einen Schriftart Satz Generator mit den angegebenen benutzerdefinierten Eigenschaften hinzufügen. Da sich die Schriftart Daten im lokalen Arbeitsspeicher befinden, ist dies jedoch nicht erforderlich. DirectWrite kann die Daten direkt lesen, um die Eigenschaftswerte abzuleiten. 

DirectWrite geht davon aus, dass die Schriftart Daten im unformatierten OpenType-Format vorliegen, das einer OpenType-Datei (. ttf,. OTF,. TTC,. OTC), aber im Arbeitsspeicher und nicht auf dem Datenträger entspricht. Die Daten dürfen nicht in einem WOFF-oder WOFF2-Containerformat vorliegen. Die Daten können eine OpenType-Schriftart Auflistung darstellen. Wenn keine benutzerdefinierten Eigenschaften verwendet werden, kann die [**IDWriteFontSetBuilder1:: AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) -Methode zum Hinzufügen aller Schriftart Gesichter in den Daten in einem einzelnen-Befehl verwendet werden. 

Ein wichtiger Aspekt des in-Memory-Szenarios ist die Lebensdauer der Daten. Wenn ein Zeiger auf den Puffer für DirectWrite bereitgestellt wird, ohne dass ein Besitzer vorhanden ist, erstellt DirectWrite eine Kopie der Daten in einem neuen Arbeitsspeicher Puffer, den er besitzt. Um das Kopieren von Daten und die zusätzliche Speicher Belegung zu vermeiden, kann die APP ein Daten Besitzer Objekt übergeben, das IUnknown implementiert, und das den Speicherpuffer mit den Schriftart Daten besitzt. Durch Implementieren dieser Schnittstelle kann DirectWrite den Verweis Zähler des Objekts hinzufügen, um die Lebensdauer der eigenen Daten sicherzustellen. 

Die Methode zum Erstellen eines benutzerdefinierten Schriftart Satzes mithilfe von Schriftart Daten im Arbeitsspeicher lautet wie folgt: hierfür ist das Windows 10 Creators Update erforderlich. Dabei wird ein von der APP implementiertes Daten Besitzer Objekt angenommen, das IUnknown implementiert und auch über Methoden verfügt, die einen Zeiger auf den Speicherpuffer und die Größe des Puffers zurückgeben. 

<dl> 1. Erstellen Sie eine IDWriteFactory5-Schnittstelle, wie oben gezeigt.  
2. Erstellen Sie eine [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) -Schnittstelle, wie oben gezeigt.  
3. Verwenden Sie die Factory zum Abrufen eines idschreiteinmemoryfontfileloader. 


```C++
 IDWriteInMemoryFontFileLoader* pInMemoryFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateInMemoryFontFileLoader(&pInMemoryFontFileLoader); 
}
```



Dadurch wird eine vom System bereitgestellte Implementierung der in-Memory-Schriftart Datei Lade Tool-Schnittstelle zurückgegeben.   
4. Registrieren Sie das in-Memory-Schriftart Datei Lade Tool bei der Factory. 


```C++
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->RegisterFontFileLoader(pInMemoryFontFileLoader); 
}
```



   
5. Verwenden Sie für jede Schriftart im Arbeitsspeicher das Schriftart Datei-Lade Tool in-Memory, um eine [**idwrite-fontfile-Datei**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)zu erstellen. 


```C++
IDWriteFontFile* pFontFile; 
hr = pInMemoryFontFileLoader->CreateInMemoryFontFileReference( 
    pDWriteFactory, 
    pFontDataOwner->fontData /* returns void* */, 
    pFontDataOwner->fontDataSize /* returns UINT32 */, 
    pFontDataOwner /* ownerObject, owns the memory with font data and implements IUknown */, 
    &pFontFile 
); 
```



   
6. Fügen Sie dem Schriftart Satz-Generator das [**idwrite-fontfile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) -Objekt mithilfe der [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) -Methode hinzu, wie oben gezeigt.  Wenn ein Bedarf vorliegt, kann die APP stattdessen einzelne [**idwrite Items fontfacereferenzierungsobjekte**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) basierend auf der **idwrite-fontfile** erstellen, optional benutzerdefinierte Eigenschaften für jeden Schriftart Verweis definieren und dann den Schriftart Verweis mit benutzerdefinierten Eigenschaften mithilfe der [**addfontfacereferenzierungsmethode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) hinzufügen, wie oben gezeigt.   
7. Nachdem dem Schriftart Satz-Generator alle Schriftarten hinzugefügt wurden, erstellen Sie den benutzerdefinierten Schriftart Satz, wie oben gezeigt.   
8. Wenn die in-Memory-Schriftarten nicht mehr verwendet werden, heben Sie die Registrierung des in-Memory-Schriftart Datei Laders auf. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pInMemoryFontFileLoader);
```



  
</dl>

 

## <a name="advanced-scenarios"></a>Erweiterte Szenarios

Einige apps verfügen möglicherweise über besondere Anforderungen, die eine erweiterte Verarbeitung erfordern, als oben beschrieben wird. 

### <a name="combining-font-sets"></a>Kombinieren von Schriftart Sätzen

Einige apps müssen möglicherweise einen Schriftart Satz erstellen, der eine Kombination von Elementen aus anderen Schriftart Sätzen umfasst. Beispielsweise kann eine APP einen Schriftart Satz erstellen, der alle auf dem System installierten Schriftarten mit einer Auswahl benutzerdefinierter Schriftarten kombiniert oder installierte Schriftarten kombiniert, die bestimmten Kriterien mit anderen Schriftarten entsprechen. DirectWrite verfügt über APIs zur Unterstützung der Bearbeitung und Kombination von Schriftart Sätzen. 

Um zwei oder mehr Schriftart Sätze zu kombinieren, fügt die [**idwrite-fontsetbuilder:: addfontset**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontset) -Methode alle Schriftarten in einem angegebenen Schriftart Satz hinzu, die einem Schriftart Satz-Generator in einem einzelnen-Befehl hinzugefügt werden sollen. Wenn im neuen Schriftart Satz nur bestimmte Schriftarten aus einem vorhandenen Schriftart Satz gewünscht werden, kann die [**idwrite-FONTSET:: getmatchingfonts**](idwritefontset-getmatchingfonts-overload.md) -Methode verwendet werden, um ein neues Schriftart Satz Objekt abzuleiten, das so gefiltert wurde, dass nur Schriftarten eingeschlossen werden, die mit den angegebenen Eigenschaften übereinstimmen. Diese Methoden bieten eine einfache Möglichkeit zum Erstellen eines benutzerdefinierten Schriftart Satzes, der Schriftarten aus mindestens zwei vorhandenen Schriftart Sätzen kombiniert. 

### <a name="using-local-woff-or-woff2-font-data"></a>Verwenden von lokalen WOFF-oder WOFF2-Schriftart Daten

Wenn eine APP Schriftart Dateien im lokalen Dateisystem oder in einem Arbeitsspeicher Puffer aufweist, Sie jedoch die WOFF-oder WOFF2-Containerformate verwenden, bietet DirectWrite (Windows 10 Creator Update oder höher) eine Methode zum Entpacken des Container Formats [**IDWriteFactory5:: unpackfontfile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile), das einen [**idwrite-fontfilestream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)zurückgibt. 

Die APP benötigt jedoch eine Möglichkeit, den [**idwrite-fontfilestream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) in ein Schriftart Datei-Lade Lade Objekt zu übernehmen. Eine Möglichkeit besteht darin, eine benutzerdefinierte [**idschreitefontfileloader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) -Implementierung zu erstellen, die den Datenstrom umschließt. Wie bei anderen Schriftart Datei Lade Programmen muss dies vor der Verwendung registriert und die Registrierung aufgehoben werden, bevor die Factory den Gültigkeitsbereich verlässt.  

Wenn das benutzerdefinierte Lade Tool auch mit unformatierten (nicht verpackten) Schriftart Dateien verwendet wird, muss die APP auch eine benutzerdefinierte Implementierung der [**idschreitefontfilestream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) -Schnittstelle zum Verarbeiten dieser Dateien bereitstellen. Es gibt jedoch einfachere Möglichkeiten, wie Sie die oben erläuterten APIs für die Behandlung von rohschriftart Dateien verwenden können. Die Notwendigkeit einer benutzerdefinierten Stream-Implementierung kann vermieden werden, indem separate Codepfade für gepackte Schriftart Dateien im Vergleich zu unformatierten Schriftart Dateien verwendet werden. 

Nachdem ein benutzerdefiniertes Schriftart Datei-Lade Objekt erstellt wurde, werden die Daten der geladenen Schriftart Datei dem Lade Tool auf App-spezifische Weise hinzugefügt. Das Lade Tool kann mehrere Schriftart Dateien verarbeiten, die jeweils mit einem App-definierten Schlüssel identifiziert werden, der für DirectWrite nicht transparent ist. Nachdem dem Lade Tool eine gepackte Schriftart Datei hinzugefügt wurde, wird die [**idwrite-Factory:: deecustomfontfilereferenzierungsmethode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) verwendet, um eine [**idwrite-fontfile-Datei**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) abzurufen, die auf diesem Lade Tool für die durch einen bestimmten Schlüssel identifizierten Schriftart Daten basiert.  

Das eigentliche Entpacken der Schriftart Daten kann erfolgen, wenn dem Lade Tool Schriftarten hinzugefügt werden. Sie können jedoch auch in der [**idschreitefontfileloader:: deestreamfromkey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) -Methode behandelt werden, die von DirectWrite beim ersten Lesen der Schriftart Daten aufgerufen wird. 

Nachdem ein idwrite-fontfile-Objekt erstellt wurde, werden die restlichen Schritte zum Hinzufügen der Schriftarten zu einem benutzerdefinierten Schriftart Satz wie oben beschrieben beschrieben. 

Eine Implementierung, bei der dieser Ansatz verwendet wird, wird im [Beispiel für benutzerdefinierte DirectWrite-Schriftart Sätze](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)veranschaulicht. 

### <a name="using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation"></a>Verwenden von DirectWrite-Remote Schriftart Mechanismen mit benutzerdefinierter Netzwerk Implementierung auf niedriger Ebene

Die DirectWrite-Mechanismen für die Handhabung von Remote Schriftarten können in Mechanismen höherer Ebene aufgeteilt werden – mit Schriftart Sätzen, die Schriftart Verweise für Remote Schriftarten enthalten, das Überprüfen der Lokalität der Schriftart Daten und die Verwaltung der Warteschlange für Schriftart Download Anforderungen – und die Mechanismen auf niedrigerer Ebene, die den tatsächlichen Download verarbeiten. Einige apps möchten möglicherweise die Remote Schriftart Mechanismen höherer Ebene verwenden, erfordern jedoch auch benutzerdefinierte Netzwerk Interaktionen, wie z. b. die Kommunikation mit Servern über andere Protokolle als http. 

In dieser Situation muss eine APP eine benutzerdefinierte Implementierung der [**idbeschreib teremotefontfileloader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) -Schnittstelle erstellen, die mit anderen Schnittstellen auf niedrigerer Ebene in den erforderlichen Punkten interagiert. Die APP muss außerdem benutzerdefinierte Implementierungen dieser untergeordneten Schnittstellen bereitstellen: [**idbeschreib teremotefontfilestream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream)und [**idschreiteasynkresult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult). Diese drei Schnittstellen verfügen über Rückruf Methoden, die von DirectWrite während Download Vorgängen aufgerufen werden. 

Wenn " [**idschreitefontdownloadqueue:: BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload) " aufgerufen wird, führt DirectWrite Abfragen an den Remote-Schriftart Datei Lader zum Ort der Daten aus und fordert den Remotestream an. Wenn die Daten nicht lokal sind, wird die BeginDownload-Methode des Streams aufgerufen. Die streamimplementierung sollte bei diesem-Befehl nicht blockieren, sondern sofort zurückgeben und ein [**idwrite-asynkresult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) -Objekt zurückgeben, das den Wait-Handle bereitstellt, den DirectWrite zum warten auf den asynchronen Downloadvorgang verwendet. Die Implementierung des benutzerdefinierten Streams ist für die Verarbeitung der Remote Kommunikation zuständig. Wenn das Abschluss Ereignis aufgetreten ist, ruft DirectWrite [**idschreiteasynkresult:: GetResult**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteasyncresult-getresult) auf, um das Ergebnis des Vorgangs zu bestimmen. Wenn das Ergebnis erfolgreich ist, wird erwartet, dass nachfolgende Read-Fragment-Aufrufe an den Datenstrom für die heruntergeladenen Bereiche erfolgreich sind. 

> [!IMPORTANT]
> Sicherheits-/leistungstokenhinweis: beim Versuch, eine Remote Schriftart abzurufen, besteht das Potenzial im Allgemeinen darin, dass ein Angreifer den vorgesehenen Server spoweder, noch reagiert der Server möglicherweise nicht. Wenn Sie benutzerdefinierte Netzwerk Interaktionen implementieren, haben Sie möglicherweise eine bessere Kontrolle über die entschärfungen als beim Umgang mit Drittanbieter Servern. Es ist jedoch ratsam, dass Sie geeignete entschärfungen in Erwägung gezogen, um Offenlegung von Informationen oder Denial-of-Service zu vermeiden. Es werden sichere Protokolle wie z. b. HTTPS empfohlen. Außerdem sollten Sie in einem Timeout erstellen, damit das an DirectWrite zurückgegebene Ereignis handle letztendlich festgelegt wird. 

 

### <a name="supporting-scenarios-on-earlier-windows-versions"></a>Unterstützende Szenarien in früheren Windows-Versionen

Die beschriebenen Szenarios können in DirectWrite unter früheren Versionen von Windows unterstützt werden, erfordern jedoch viel mehr benutzerdefinierte Implementierung für den Teil der APP, wobei die restriktivsten APIs verwendet werden, die vor Windows 10 verfügbar waren. Weitere Informationen finden Sie unter [benutzerdefinierte Schriftart Auflistungen (Windows 7/8)](custom-font-collections.md).

 

 