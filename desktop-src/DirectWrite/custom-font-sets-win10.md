---
title: Benutzerdefinierte Schriftartenkombinationen
description: In diesem Thema werden verschiedene Möglichkeiten beschrieben, wie Sie benutzerdefinierte Schriftarten in Ihrer App verwenden können.
ms.assetid: 50842838-d150-df9a-f1b7-67ce5ea2bc80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4b8b9c49895c2b137aaa33cf0788d9518a1d53834c74eb27feb6b44fa045d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650284"
---
# <a name="custom-font-sets"></a>Benutzerdefinierte Schriftartenkombinationen

In diesem Thema werden verschiedene Möglichkeiten beschrieben, wie Sie benutzerdefinierte Schriftarten in Ihrer App verwenden können.

-   [Einführung ](#introduction)
-   [Übersicht über die APIs](#summary-of-apis)
-   [Wichtige Begriffe](#key-concepts)
-   [Schriftarten und Schriftartdateiformate](#fonts-and-font-file-formats)
-   [Schriftartensätze und Schriftartauf auflistungen](#font-sets-and-font-collections)
-   [Gängige Szenarios](#common-scenarios)
    -   [Erstellen eines Schriftartensets mit beliebigen Schriftarten im lokalen Dateisystem](#creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system)
    -   [Erstellen eines Schriftartensets mithilfe bekannter Schriftarten im lokalen Dateisystem](#creating-a-font-set-using-known-fonts-in-the-local-file-system)
    -   [Erstellen eines benutzerdefinierten Schriftartensets mit bekannten Remoteschriftarten im Web](#creating-a-custom-font-set-using-known-remote-fonts-on-the-web)
    -   [Erstellen eines benutzerdefinierten Schriftartensets mithilfe der in den Arbeitsspeicher geladenen Schriftartdaten](#creating-a-custom-font-set-using-font-data-loaded-into-memory)
-   [Erweiterte Szenarien](#advanced-scenarios)
    -   [Kombinieren von Schriftartsätzen](#combining-font-sets)
    -   [Verwenden von lokalen WOFF- oder WOFF2-Schriftartdaten ](#using-local-woff-or-woff2-font-data)
    -   [Verwenden DirectWrite Remoteschriftartmechanismen mit benutzerdefinierter Low-Level-Netzwerkimplementierung](#using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation)
    -   [Unterstützende Szenarien für frühere Windows Versionen](#supporting-scenarios-on-earlier-windows-versions)

## <a name="introduction"></a>Einführung

In den meisten Jahren verwenden Apps die Schriftarten, die lokal auf dem System installiert sind. DirectWrite ermöglicht den Zugriff auf diese Schriftarten mithilfe der [**Methoden IDWriteFactory3::GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) oder [**IDWriteFactory::GetSystemFontCollection.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) In einigen Fällen möchten Apps möglicherweise auch Schriftarten verwenden, die als Teil von Windows 10, aber derzeit nicht auf dem aktuellen System installiert sind. Auf diese Schriftarten kann über den Windows-Schriftartdienst mithilfe der **GetSystemFontSet-Methode** oder durch Aufrufen von [**IDWriteFactory3::GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection) zugegriffen werden, wenn includeDownloadableFonts auf TRUE festgelegt ist. 

In einigen Anwendungsszenarien müssen Apps jedoch Schriftarten verwenden, die nicht im System installiert sind und nicht vom Windows Bereitgestellt werden. Im Folgenden finden Sie Beispiele für solche Szenarien:

-   Schriftarten werden als Ressourcen in eine App-Binärdatei eingebettet.
-   Schriftartdateien werden in einem App-Paket gebündelt und auf dem Datenträger im Installationsordner der App gespeichert.
-   Die App ist ein Schriftartentwicklungstool, das vom Benutzer angegebene Schriftartdateien laden muss. 
-   Schriftarten werden in Dokumentdateien eingebettet, die in der App angezeigt oder bearbeitet werden können. 
-   Die App verwendet Schriftarten, die von einem öffentlichen Webschriftartdienst erhalten wurden. 
-   Die App verwendet Schriftartdaten, die über ein privates Netzwerkprotokoll gestreamt werden. 

DirectWrite stellt APIs für die Arbeit mit benutzerdefinierten Schriftarten in diesen und anderen ähnlichen Szenarien zur Verfügung. Die benutzerdefinierten Schriftartdaten können aus Dateien im lokalen Dateisystem stammen. aus cloudbasierten Remotequellen, auf die über HTTP zugegriffen wird; oder aus beliebigen Quellen, nachdem sie in einen Speicherpuffer geladen wurden. 

> [!Note]  
> Während DirectWrite seit Windows 7 APIs für die Arbeit mit benutzerdefinierten Schriftarten bereitgestellt hat, wurden neuere APIs in Windows 10 und erneut im Windows 10 Creators Update (Vorschauversion Build 15021 oder höher) hinzugefügt, die die Implementierung mehrerer der erwähnten Szenarien vereinfachen. Dieses Thema konzentriert sich auf APIs, die in Fenster 10 verfügbar sind. Informationen zu Anwendungen, die mit früheren Versionen Windows arbeiten müssen, finden Sie unter [Benutzerdefinierte Schriftartenaufsammlungen (Windows 7/8).](custom-font-collections.md) 

 

## <a name="summary-of-apis"></a>Übersicht über die APIs

Dieses Thema konzentriert sich auf die Funktionen, die von den folgenden APIs bereitgestellt werden: 

-   [**IDWriteFontSet-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
-   [**IDWriteFontSetBuilder-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
-   [**IDWriteFontSetBuilder1-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) 
-   [**IDWriteFontFaceReference-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)
-   [**IDWriteFontFile-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)
-   [**IDWriteFactory::CreateFontFileReference-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) 
-   [**IDWriteFactory::CreateCustomFontFileReference-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) 
-   [**IDWriteFactory3::CreateFontFaceReference-Methoden**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontresource-createfontfacereference) 
-   [**DWRITE \_ FONT \_ PROPERTY-Struktur**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) 
-   [**DWRITE \_ FONT \_ PROPERTY \_ ID-Enumeration**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) 
-   [**IDWriteFontFileLoader-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) 
-   [**IDWriteFactory::RegisterFontFileLoader-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader) 
-   [**IDWriteFactory::UnregisterFontFileLoader-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontfileloader) 
-   [**IDWriteFactory5::CreateInMemoryFontFileLoader-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createinmemoryfontfileloader) 
-   [**IDWriteInMemoryFontFileLoader-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) 
-   [**IDWriteFactory5::CreateHttpFontFileLoader-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createhttpfontfileloader) 
-   [**IDWriteRemoteFontFileLoader-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) 
-   [**IDWriteFontDownloadQueue-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) 
-   [**IDWriteFontDownloadListener-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) 
-   [**IDWriteFontFileStream-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 
-   [**IDWriteRemoteFontFileStream-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) 
-   [**IDWriteAsyncResult-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) 
-   [**IDWriteFactory5::AnalyzeContainerType-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-analyzecontainertype) 
-   [**IDWriteFactory5::UnpackFontFile-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile) 

 

## <a name="key-concepts"></a>Wichtige Begriffe

Um die DirectWrite-APIs für die Arbeit mit benutzerdefinierten Schriftarten zu verstehen, kann es hilfreich sein, das konzeptionelle Modell zu verstehen, das diesen APIs zugrunde liegt. Wichtige Konzepte werden hier beschrieben. 

Wenn DirectWrite tatsächlich textlayout oder rendert, muss sie auf die tatsächlichen Schriftartdaten zugreifen. Ein Schriftartenobjekt enthält tatsächliche Schriftartdaten, die im lokalen System vorhanden sein müssen. Für andere Vorgänge, z. B. das Überprüfen der Verfügbarkeit einer bestimmten Schriftart oder das Präsentieren von Schriftartoptionen für einen Benutzer, ist jedoch nur ein Verweis auf eine bestimmte Schriftart erforderlich, nicht die tatsächlichen Schriftartdaten selbst. In DirectWrite enthält ein Schriftartverweisobjekt nur die Informationen, die zum Suchen und Instanziieren einer Schriftart erforderlich sind. Da der Schriftartgesichtsverweis keine tatsächlichen Daten auftrat, kann DirectWrite mit Schriftartgesichtsverweisen umgehen, für die sich die tatsächlichen Daten an einem Remotenetzwerkstandort befinden, und wenn die tatsächlichen Daten lokal sind.

Ein Schriftartensatz ist ein Satz von Schriftartgesichtsverweisen sowie bestimmte grundlegende, informationsbasierte Eigenschaften, die verwendet werden können, um auf die Schriftart zu verweisen oder sie mit anderen Schriftarten, z. B. dem Familiennamen, oder einem Schriftgradwert zu vergleichen. Die tatsächlichen Daten für die verschiedenen Schriftarten können lokal oder alle remote oder eine Mischung sein.

Ein Schriftartensatz kann verwendet werden, um ein entsprechendes Auflistungsobjekt für Schriftarten zu erhalten. Weitere Informationen finden Sie weiter unten unter Schriftartensätze und Schriftartsammlungen. 

Die IDWriteFontSet-Schnittstelle stellt Methoden bereit, die das Abfragen von Eigenschaftswerten wie Familienname oder Schriftgewichtung oder für Schriftartverweise ermöglichen, die bestimmten Eigenschaftswerten entsprechen. Nach dem Filtern bis zu einer bestimmten Auswahl kann eine Instanz der [**IDWriteFontFaceReference-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) mit Methoden zum Herunterladen (wenn die tatsächlichen Schriftartdaten derzeit remote sind) zum Abrufen des entsprechenden [**IDWriteFontFace3-Objekts,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) das für Layout und Rendering verwendet werden kann, ermittelt werden. 

Die IDWriteFontFile-Schnittstelle liegt jedem Schriftarten- oder Schriftartgesichtsverweis zugrunde. Dies stellt den Speicherort einer Schriftartdatei dar und verfügt über zwei Komponenten: ein Schriftartdateilader und einen Schriftartdateischlüssel. Das Ladeprogramm der Schriftartdatei ([**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader)) wird verwendet, um bei Bedarf eine Datei zu öffnen, und gibt einen Stream mit den Daten zurück ([**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)). Je nach Lademodul können sich die Daten unter einem lokalen Dateipfad, einer Remote-URL oder in einem Speicherpuffer befinden. Der Schlüssel ist ein vom Lader definierter Wert, der die Datei innerhalb des Ladekontexts eindeutig identifiziert, sodass das Lader die Daten finden und einen Stream dafür erstellen kann. 

Benutzerdefinierte Schriftarten können problemlos einem benutzerdefinierten Schriftartensatz hinzugefügt werden, der wiederum zum Filtern oder Organisieren von Schriftartinformationen für Zwecke wie das Erstellen einer Benutzeroberfläche für die Schriftartauswahl verwendet werden kann. Der Schriftartensatz kann auch verwendet werden, um eine Schriftartsammlung für die Verwendung in APIs höherer Ebene wie [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) und [**IDWriteTextLayout zu erstellen.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) Die [**IDWriteFontSetBuilder-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) kann verwendet werden, um einen benutzerdefinierten Schriftartensatz zu erstellen, der mehrere benutzerdefinierte Schriftarten enthält. Sie kann auch verwendet werden, um einen benutzerdefinierten Schriftartensatz zu erstellen, der benutzerdefinierte Schriftarten und vom System bereitgestellte Schriftarten gemischt. oder , die Schriftarten mit verschiedenen Quellen für die tatsächlichen Daten kombinieren – lokaler Speicher, Remote-URLs und Arbeitsspeicher. 

Wie bereits erwähnt, kann ein Schriftartengesicht-Verweis auf Schriftartdaten an einer Remotequelle verweisen, aber die Daten müssen lokal sein, um ein Schriftarten-Gesichtsobjekt zu erhalten, das für Layout und Rendering verwendet werden kann. Das Herunterladen von Remotedaten wird von einer Downloadwarteschlange für Schriftarten verarbeitet. Apps können die [**IDWriteFontDownloadQueue-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) verwenden, um Anforderungen zum Herunterladen von Remoteschriftarten zum Initiieren des Downloadprozesses in die Queue zu setzen und ein [**IDWriteFontDownloadListener-Objekt**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) zu registrieren, um Maßnahmen zu ergreifen, wenn der Downloadvorgang abgeschlossen ist. 

Für die meisten der hier beschriebenen Schnittstellen stellt DirectWrite Systemimplementierung bereit. Die einzige Ausnahme ist die [**IDWriteFontDownloadListener-Schnittstelle,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) die eine App implementiert, um app-spezifische Aktionen durchzuführen, wenn Remoteschriftarten lokal heruntergeladen wurden. Apps haben möglicherweise Grund, ihre eigenen benutzerdefinierten Implementierungen für bestimmte andere Schnittstellen zur Verfügung zu stellen, dies wäre jedoch nur in bestimmten, fortgeschritteneren Szenarien erforderlich. Beispielsweise müsste eine App eine benutzerdefinierte Implementierung der [**IDWriteFontFileLoader-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) bereitstellen, um Schriftartdateien im lokalen Speicher zu verarbeiten, die das WOFF2-Containerformat verwenden. Weitere Details finden Sie weiter unten. 

## <a name="fonts-and-font-file-formats"></a>Schriftarten und Schriftartdateiformate

Ein weiteres wichtiges Konzept, das hilfreich zu verstehen ist, ist die Beziehung zwischen einzelnen Schriftartgesichtern und Schriftartdateien, die sie enthalten. Die Idee einer OpenType-Schriftartdatei (TTF oder OTF), die eine einzelne Schriftart enthält, ist vertraut. Das OpenType-Schriftformat ermöglicht jedoch auch eine OpenType-Schriftartsammlung (.ttc oder .font), bei der es sich um eine einzelne Datei handelt, die mehrere Schriftarten enthält. OpenType Collection-Dateien werden häufig für große Schriftarten verwendet, die eng miteinander verknüpft sind und identische Werte für bestimmte Schriftartdaten haben: Wenn die Schriftarten in einer einzelnen Datei kombiniert werden, können die allgemeinen Daten dedupliziert werden. Aus diesem Grund muss ein Schriftarten- oder Schriftartgesichtverweis nicht nur auf eine Schriftartdatei (oder eine entsprechende Datenquelle) verweisen, sondern auch einen Schriftartindex in dieser Datei angeben, für den allgemeinen Fall, in dem die Datei eine Sammlungsdatei sein kann. 

Für Schriftarten, die im Web verwendet werden, werden Schriftartdaten häufig in bestimmte Containerformate gepackt, WOFF oder WOFF2, die eine gewisse Komprimierung der Schriftartdaten und ein gewisses Maß an Schutz vor Verletzungen und Verstößen gegen Schriftartlizenzen bieten. Funktionell entspricht eine WOFF- oder WOFF2-Datei einer OpenType-Schriftart oder einer Schriftartsammlungsdatei, aber die Daten werden in einem anderen Format codiert, das vor der Verwendung entpackt werden muss. 

Bestimmte DirectWrite-APIs können einzelne Schriftarten verarbeiten, während andere APIs Dateien verarbeiten können, die OpenType-Sammlungsdateien enthalten können, die mehrere Gesichter enthalten. Ebenso behandeln bestimmte APIs nur Rohdaten im OpenType-Format, während andere APIs die gepackten, WOFF- und WOFF2-Containerformate verarbeiten können. Diese Details werden in der folgenden Diskussion bereitgestellt. 

## <a name="font-sets-and-font-collections"></a>Schriftartensätze und Schriftartauf auflistungen

Einige Anwendungen können implementiert werden, um mit Schriftarten über die [**IDWriteFontCollection-Schnittstelle zu**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) arbeiten. Es gibt eine direkte Entsprechung zwischen einer Schriftartsammlung und einem Schriftartensatz. Jede kann die gleichen Schriftarten enthalten, aber sie stellen sie einer anderen Organisation vor. Aus jeder Schriftartsammlung kann ein entsprechender Schriftartensatz und umgekehrt ermittelt werden.

Wenn Sie mit einer Reihe von benutzerdefinierten Schriftarten arbeiten, ist es am einfachsten, eine Schriftartensatz-Generator-Schnittstelle zu verwenden, um einen benutzerdefinierten Schriftartensatz zu erstellen und dann eine Schriftartsammlung zu erhalten, nachdem der Schriftartensatz erstellt wurde. Der Prozess zum Erstellen eines benutzerdefinierten Schriftartensets wird unten ausführlich beschrieben. Zum Abrufen einer [**IDWriteFontCollection1-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) aus einem Schriftartensatz wird die [**IDWriteFactory3::CreateFontCollectionFromFontSet-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-createfontcollectionfromfontset) verwendet.

Wenn die App über ein Sammlungsobjekt verfügt und einen entsprechenden Schriftartensatz abrufen muss, kann dies mithilfe der [**IDWriteFontCollection1::GetFontSet-Methode erfolgen.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontcollection1-getfontset) 

## <a name="common-scenarios"></a>Häufige Szenarien

In diesem Abschnitt werden einige der häufigsten Szenarien mit benutzerdefinierten Schriftarten beschrieben:

-   Erstellen eines benutzerdefinierten Schriftartensets mit beliebigen Schriftarten in Pfaden im lokalen Dateisystem.
-   Erstellen eines benutzerdefinierten Schriftartensets mithilfe bekannter Schriftarten (möglicherweise gebündelt mit der App), die im lokalen Dateisystem gespeichert sind.
-   Erstellen eines benutzerdefinierten Schriftartensets mit bekannten Remoteschriftarten im Web.
-   Erstellen eines benutzerdefinierten Schriftartensets mithilfe von Schriftartdaten, die in den Arbeitsspeicher geladen werden.

Vollständige Implementierungen für diese Szenarien finden Sie im DirectWrite [Beispiel für benutzerdefinierte Schriftarten.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/) Dieses Beispiel veranschaulicht auch ein erweitertes Szenario für die Verarbeitung von Schriftartdaten, die in WOFF- oder WOFF2-Containerformaten gepackt sind. Dies wird im Folgenden erläutert. 

### <a name="creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system"></a>Erstellen eines Schriftartensets mit beliebigen Schriftarten im lokalen Dateisystem

Beim Umgang mit einem beliebigen Satz von Schriftartdateien im lokalen Speicher ist die [**IDWriteFontSetBuilder1::AddFontFile-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) praktisch, da sie in einem einzigen Aufruf alle Schriftartgesichter in einer OpenType-Schriftartsammlungsdatei sowie alle Instanzen für eine OpenType-Variablenschriftart verarbeiten kann. Dies ist im Windows 10 Creators Update (Vorschauversion Build 15021 oder höher) verfügbar und wird immer empfohlen, wenn verfügbar. 

Um diese Methode zu verwenden, verwenden Sie den folgenden Prozess.

<dl> 1.Erstellen Sie zunächst die <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5">IDWriteFactory5-Schnittstelle:</a> 


```C++
IDWriteFactory5* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
  DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



   
2. Verwenden Sie die Factory, um die <a href=""></a> [**IDWriteFontSetBuilder1-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) zu erhalten: 


```C++
IDWriteFontSetBuilder1* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
}  
                
```



  
3. Erstellen Sie für jede Schriftartdatei im lokalen Dateisystem eine [**IDWriteFontFile,**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) die darauf verweist: 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



   
4. Fügen Sie das [**IDWriteFontFile-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) mithilfe der [**AddFontFile-Methode dem Schriftartensatz-Generator**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) hinzu: 


```C++
hr = pFontSetBuilder->AddFontFile(pFontFile); 
```

Wenn der im Aufruf von [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) angegebene Dateipfad auf einen anderen Wert als eine unterstützte OpenType-Datei verwiesen hat, gibt der Aufruf von [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) den Fehler DWRITE \_ E \_ FILEFORMAT zurück.

5. Nachdem alle Dateien dem Schriftartensatz-Generator hinzugefügt wurden, kann der benutzerdefinierte Schriftartensatz erstellt werden: 


```C++
IDWriteFontSet* pFontSet; 
hr = pFontSetBuilder->CreateFontSet(&pFontSet); 
```



   
</dl>

Wenn die App auf Windows 10 Versionen vor dem Windows 10 Creators Update ausgeführt werden muss, ist die AddFontFile-Methode nicht verfügbar. Die Verfügbarkeit kann erkannt werden, indem eine [**IDWriteFactory3-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) erstellt und dann mithilfe von QueryInterface versucht wird, eine [**IDWriteFactory5-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) zu erhalten: Wenn dies erfolgreich ist, sind auch die [**IDWriteFontSetBuilder1-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) und die [**AddFontFile-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) verfügbar.

Wenn die AddFontFile-Methode nicht verfügbar ist, muss die [**IDWriteFontSetBuilder::AddFontFaceReference-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) verwendet werden, um einzelne Schriftartgesichter hinzuzufügen. Um OpenType-Schriftartsammlungsdateien zu ermöglichen, die mehrere Gesichter enthalten, kann die [**IDWriteFontFile::Analyze-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) verwendet werden, um die Anzahl der in der Datei enthaltenen Gesichter zu bestimmen. Der Prozess ist wie folgt.

<dl> 1.Erstellen Sie zunächst die <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3-Schnittstelle:</a> 


```C++
IDWriteFactory3* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



  
2. Verwenden Sie die Factory, um die [**IDWriteFontSetBuilder-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) zu erhalten: 


```C++
IDWriteFontSetBuilder* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
} 
```



  
3. Erstellen Sie für jede Schriftartdatei wie oben beschrieben eine [**IDWriteFontFile:**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



Anstatt die Datei direkt dem Schriftartensatz-Generator hinzufügen zu müssen wir die Anzahl der Gesichter bestimmen und einzelne [**IDWriteFontFaceReference-Objekte**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) erstellen.   
4. Verwenden [](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) Sie die Analyze-Methode, um die Anzahl der Gesichter in der Datei zu erhalten. 


```C++
BOOL isSupported; 
DWRITE_FONT_FILE_TYPE fileType; 
UINT32 numberOfFonts; 
hr = pFontFile->Analyze(&isSupported, &fileType, /* face type */ nullptr, &numberOfFonts); 
```



Die [**Analyze-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) setzt auch Werte für die Parameter isSupported und fileType. Wenn die Datei kein unterstütztes Format ist, hat isSupported den Wert FALSE, und es können entsprechende Aktionen wie das Ignorieren der Datei ergriffen werden.   
5. Schleife über die Anzahl der im numberOfFonts-Parameter festgelegten Schriftarten. Erstellen Sie innerhalb der Schleife eine [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) für jedes Datei-Index-Paar, und fügen Sie diese dem Schriftartensatz-Generator hinzu. 


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



  
6. Nachdem alle Gesichter dem Schriftartensatz-Generator hinzugefügt wurden, erstellen Sie den benutzerdefinierten Schriftartensatz, wie oben gezeigt.  
</dl>

Eine App kann so entworfen werden, dass sie die bevorzugte [**AddFontFile-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) verwendet, wenn sie auf der Windows 10 Creators Update ausgeführt wird. Bei der Ausführung in früheren Versionen von Windows 10 wird jedoch auf die [**AddFontFaceReference-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) zurückgefallen. Testen Sie wie oben beschrieben [**die Verfügbarkeit der IDWriteFactory5-Schnittstelle,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) und verzweigen Sie sie anschließend entsprechend. Dieser Ansatz wird im beispiel DirectWrite [Custom Font Sets veranschaulicht.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/) 

### <a name="creating-a-font-set-using-known-fonts-in-the-local-file-system"></a>Erstellen eines Schriftartensets mithilfe bekannter Schriftarten im lokalen Dateisystem

Wie bereits erwähnt, ist jeder Schriftartenverweis in einem Schriftartensatz bestimmten Informationseigenschaften zugeordnet, z. B. Familienname und Schriftgrad. Wenn einem Schriftartensatz-Generator mithilfe der oben aufgeführten API-Aufrufe benutzerdefinierte Schriftarten hinzugefügt werden, werden diese Informationseigenschaften direkt aus den tatsächlichen Schriftartdaten erhalten, die gelesen werden, wenn die Schriftart hinzugefügt wird. In einigen Situationen kann es jedoch sein, dass eine App, die über eine andere Quelle von Informationen zu einer Schriftart verfügt, eigene benutzerdefinierte Werte für diese Eigenschaften bereitstellen möchte. 

Angenommen, eine App bündelt einige Schriftarten, die zum Präsentieren bestimmter Benutzeroberflächenelemente in der App verwendet werden. Manchmal, z. B. bei einer neuen App-Version, müssen die spezifischen Schriftarten, die die App für diese Elemente verwendet, möglicherweise geändert werden. Wenn die App über codierte Verweise auf die spezifischen Schriftarten verfügt, erfordert das Ersetzen einer Schriftart durch eine andere, dass jeder dieser Verweise geändert wird. Wenn die App stattdessen benutzerdefinierte Eigenschaften verwendet, um funktionale Aliase basierend auf dem Typ des zu rendernden Elements oder Texts zu zuweisen, ordnet jeder Alias einer bestimmten Schriftart an einer Stelle zu und verwendet dann die Aliase in allen Kontexten, in denen Schriftarten erstellt und bearbeitet werden. Das Ersetzen einer Schriftart durch eine andere erfordert nur das Ändern der einen Stelle, an der der Alias einer bestimmten Schriftart zugeordnet ist. 

Benutzerdefinierte Werte für Informationseigenschaften können zugewiesen werden, wenn die [**IDWriteFontSetBuilder::AddFontFaceReference-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) aufgerufen wird. Dies ist die folgende Methode: kann in jeder version Windows 10 werden. 

Wie oben gezeigt, beginnen Sie mit dem Abrufen der [**Schnittstellen IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) und [**IDWriteFontSet.**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) Erstellen Sie für jedes benutzerdefinierte Schriftartgesicht, das hinzugefügt werden soll, eine [**IDWriteFontFaceReference,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)wie oben gezeigt. Bevor dies dem Schriftartensatz-Generator hinzugefügt wird (innerhalb der Schleife in Schritt 5, wie oben gezeigt), definiert die App jedoch die zu verwendenden benutzerdefinierten Eigenschaftswerte. 

Ein Satz benutzerdefinierter Eigenschaftswerte wird mithilfe eines Arrays von [**DWRITE \_ FONT \_ PROPERTY-Strukturen**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) definiert. Jede dieser Eigenschaften identifiziert eine bestimmte Eigenschaft aus der [**DWRITE \_ FONT PROPERTY \_ ID-Aufzählnummer \_**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) und den entsprechenden Eigenschaftswert, der verwendet werden soll.  

Beachten Sie, dass alle Eigenschaftswerte als Zeichenfolgen zugewiesen werden. Wenn diese möglicherweise später benutzern angezeigt werden, können alternative Werte für eine bestimmte Eigenschaft für verschiedene Sprachen festgelegt werden, dies ist jedoch nicht erforderlich. Beachten Sie außerdem, dass nur die angegebenen Werte innerhalb des Schriftartensets verwendet werden, wenn benutzerdefinierte Eigenschaftswerte von der App festgelegt werden. DirectWrite werden keine Werte direkt aus der Schriftart für Informationseigenschaften, die in einem Schriftartensatz verwendet werden, ableiten. 

Im folgenden Beispiel werden benutzerdefinierte Werte für drei Informationseigenschaften definiert: Familienname, vollständiger Name und Schriftgrad. 


```C++
DWRITE_FONT_PROPERTY props[] = 
{ 
  { DWRITE_FONT_PROPERTY_ID_FAMILY_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_FULL_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_WEIGHT, L"400", nullptr } 
}; 
               
            
```



Nachdem Sie das gewünschte Array von Eigenschaftswerten für eine Schriftart definiert haben, rufen Sie AddFontFaceRefence auf, und übergeben Sie dabei das Eigenschaftenarray sowie den Schriftartgesichtsverweis. 


```C++
hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference, props, ARRAYSIZE(props)); 
```



 

Nachdem alle benutzerdefinierten Schriftartgesichter dem Schriftartensatz-Generator und ihren benutzerdefinierten Eigenschaften hinzugefügt wurden, erstellen Sie den benutzerdefinierten Schriftartensatz, wie oben gezeigt. 

### <a name="creating-a-custom-font-set-using-known-remote-fonts-on-the-web"></a>Erstellen eines benutzerdefinierten Schriftartensets mit bekannten Remoteschriftarten im Web

Benutzerdefinierte Eigenschaften sind wichtig für die Arbeit mit Remoteschriftarten. Jeder Schriftartverweis muss über einige Informationseigenschaften verfügen, um die Schriftart zu charakterisieren und von anderen Schriftarten zu unterscheiden. Da die Schriftartdaten für Remoteschriftarten nicht lokal sind, DirectWrite Eigenschaften nicht direkt von den Schriftartdaten ableiten. Daher müssen Eigenschaften explizit bereitgestellt werden, wenn dem Schriftartensatz-Generator eine Remoteschriftart hinzugefügt wird.

Die Reihenfolge der API-Aufrufe zum Hinzufügen von Remoteschriftarten zu einem Schriftartensatz ähnelt der im vorherigen Szenario beschriebenen Sequenz. Da es sich bei den Schriftartdaten jedoch um Remotedaten handelt, unterscheiden sich die Vorgänge zum Lesen der tatsächlichen Schriftartdaten von den Vorgängen bei der Arbeit mit Dateien im lokalen Speicher. In diesem Fall wurde eine neue Schnittstelle der unteren Ebene, [**IDWriteRemoteFontFileLoader,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader)in die Windows 10 Creators Update. 

Um das Remote-Schriftartdateilader verwenden zu können, muss es zuerst bei einer DirectWrite werden. Das Lader muss von der App so lange gehalten werden, wie die zugeordneten Schriftarten verwendet werden. Sobald die Schriftarten nicht mehr verwendet werden und irgendwann, bevor die Factory zerstört wird, muss die Registrierung des Ladeers aufgehoben werden. Dies kann im Destruktor für die Klasse erfolgen, die das Ladeobjekt besitzt. Diese Schritte werden unten gezeigt. 

Die Methode zum Erstellen eines benutzerdefinierten Schriftartensets mithilfe von Remoteschriftarten lautet wie folgt: dies erfordert die Windows 10 Creators Update.  

<dl> 1. Erstellen Sie wie oben gezeigt eine IDWriteFactory5-Schnittstelle.   
2.Erstellen Sie <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">wie oben gezeigt eine IDWriteFontSetBuilder-Schnittstelle.</a>   
3.Verwenden Sie die Factory, um einen <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader">IDWriteRemoteFontFileLoader zu erhalten.</a> 


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



Dadurch wird eine vom System bereitgestellte Implementierung der Schnittstelle für das Remoteschriftdateilader zurückgegeben, die HTTP-Interaktionen zum Herunterladen von Schriftartdaten im Auftrag der App verarbeiten kann. Eine Verweiser-URL oder zusätzliche Header können angegeben werden, wenn dies für den Schriftartdienst oder die Dienste erforderlich ist, die die Quelle für die Schriftarten sind.    

> [!IMPORTANT]
> Sicherheitshinweis: Wenn versucht wird, eine Remoteschriftart zu erhalten, besteht das Potenzial für einen Angreifer, den vorgesehenen Server zu spoofen, der aufgerufen wird. In diesem Fall würden die Ziel- und Verweiser-URLs und Headerdetails dem Angreifer offengelegt. App-Entwickler sind für die Minderung dieses Risikos verantwortlich. Die Verwendung des HTTPS-Protokolls anstelle von HTTP wird empfohlen. 

 

Ein einzelnes Remote-Schriftartdateilader kann für mehrere Schriftarten verwendet werden, obwohl unterschiedliche Lader verwendet werden können, wenn Schriftarten von mehreren Diensten bezogen werden, die unterschiedliche Anforderungen für Verweis-URL oder zusätzliche Header haben.   
4. Registrieren Sie das Remote-Schriftartdateilader bei der Factory. 


```C++
 if (SUCCEEDED(hr)) 
 { 
     hr = pDWriteFactory->RegisterFontFileLoader(pRemoteFontFileLoader); 
 } 
```



Ab diesem Zeitpunkt ähneln die Schritte zum Erstellen des benutzerdefinierten Schriftartensets den Schritten, die für bekannte, lokale Schriftartdateien beschrieben werden, mit zwei wichtigen Ausnahmen. Zunächst wird das [**IDWriteFontFile-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) mithilfe der Schnittstelle des Remoteschriftartdateiladeers erstellt, anstatt die Factory zu verwenden. Zweitens kann die Analyze-Methode nicht verwendet werden, da die Schriftartdaten nicht lokal sind. Stattdessen muss die App wissen, ob es sich bei der Remoteschriftartdatei um eine OpenType-Schriftartsammlungsdatei handelt. Wenn ja, muss sie wissen, welche der Schriftarten in der Sammlung sie verwenden wird, und den Index für die einzelnen Schriftarten. Daher sind die verbleibenden Schritte wie folgt.   
5. Verwenden Sie für jede Remoteschriftartdatei die Schnittstelle zum Laden der Remoteschriftartdatei, um eine [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)zu erstellen, und geben Sie dabei die URL an, die für den Zugriff auf die Schriftartdatei erforderlich ist. 


```C++
 IDWriteFontFile* pFontFile; 
 hr = pRemoteFontFileLoader->CreateFontFileReferenceFromUrl( 
     pDWriteFactory, 
     /* baseUrl */ L"https://github.com/", 
     /* fontFileUrl */ L"winjs/winjs/blob/master/src/fonts/Symbols.ttf?raw=true", 
     &pFontFile 
 ); 
```



Beachten Sie, dass die vollständige URL im fontFileUrl-Parameter angegeben oder in Basis- und relative Teile aufgeteilt werden kann. Wenn eine Basis-URL angegeben wird, muss die Verkettung der Werte baseUrl und fontFileUrl die vollständige URL bereitstellen– DirectWrite stellt kein zusätzliches Trennzeichen zur Verfügung.  

> [!IMPORTANT]
> Sicherheits-/Leistungshinweis: Wenn versucht wird, eine Remoteschriftart zu abrufen, gibt es keine Garantie dafür, dass Windows eine Antwort vom Server erhalten. In einigen Fällen antwortet ein Server möglicherweise mit einem Dateifehler, der nicht gefunden wurde, auf eine ungültige relative URL, reagiert aber nicht mehr, wenn er mehrere ungültige Anforderungen empfängt. Wenn der Server nicht antwortet, Windows schließlich ein Time out, obwohl dies einige Minuten dauern kann, wenn mehrere Abrufe initiiert werden. Sie sollten alles tun, um sicherzustellen, dass URLs gültig sind, wenn Aufrufe vorgenommen werden. 

 

Beachten Sie auch, dass die URL auf eine Unformatiert-OpenType-Schriftartdatei (TTF, OTF, TTC, .fs) verweisen kann, aber auch auf Schriftarten in einer WOFF- oder WOFF2-Containerdatei verweisen kann. Wenn auf eine WOFF- oder WOFF2-Datei verwiesen wird, entpackt die DirectWrite-Implementierung des Remoteschriftartdateiladeers automatisch die Schriftartdaten aus der Containerdatei.   
6. Erstellen Sie für jeden Schriftartenindex in der Remoteschriftartdatei, die verwendet werden soll, eine [**IDWriteFontFaceReference.**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) 


```C++
 IDWriteFontFaceReference* pFontFaceReference; 
 hr = pDWriteFactory->CreateFontFaceReference(pFontFile, /* faceIndex */ 0, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);
```



  
7. Definieren Sie benutzerdefinierte Eigenschaften für das Schriftartgesicht, wie oben gezeigt.   
8. Fügen Sie dem Schriftartsatz-Generator den Schriftartengesichtsverweis zusammen mit benutzerdefinierten Eigenschaften hinzu, wie oben gezeigt.   
9. Nachdem alle Schriftarten dem Schriftartensatz-Generator hinzugefügt wurden, erstellen Sie den Schriftartensatz, wie oben gezeigt.   
10. Wenn die Remoteschriftarten nicht mehr verwendet werden, müssen Sie die Registrierung des Remoteschriftartdateiladeers aufheben. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pRemoteFontFileLoader); 
```



  
</dl>

Sobald ein benutzerdefinierter Schriftartensatz mit benutzerdefinierten Remoteschriftarten erstellt wurde, enthält der Schriftartensatz Verweise und Informationseigenschaften für die Remoteschriftarten, die tatsächlichen Daten sind jedoch weiterhin remote. DirectWrite-Unterstützung für Remoteschriftarten ermöglicht das Beibehalten eines Schriftartenverweises im Schriftartensatz und die Auswahl einer Schriftart für die Verwendung in Layout und Rendering, aber dass die tatsächlichen Daten erst heruntergeladen werden, wenn sie tatsächlich verwendet werden müssen, z. B. wenn das Textlayout ausgeführt wird.  

Eine App kann einen Ansatz im Vorhin verfolgen, indem sie anfing, DirectWrite die Schriftartdaten herunterzuladen und dann auf die Bestätigung eines erfolgreichen Downloads zu warten, bevor mit der Verarbeitung der Schriftart begonnen wird. Ein Netzwerkdownload impliziert jedoch eine gewisse Wartezeit von unvorhersehbarer Dauer, und der Erfolg ist ebenfalls unsicher. Aus diesem Grund ist es in der Regel besser, einen anderen Ansatz zu wählen, sodass Layout und Rendering zunächst mit alternativen oder Fallbackschriftarten erfolgen können, die bereits lokal sind, während gleichzeitig das Herunterladen der gewünschten Remoteschriftart und das anschließende Aktualisieren der Ergebnisse nach dem Herunterladen der gewünschten Schriftart erforderlich ist. 

Um anfordern, dass die gesamte Schriftart heruntergeladen wird, bevor sie verwendet wird, kann die [**IDWriteFontFaceReference::EnqueueFontDownloadRequest-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuefontdownloadrequest) verwendet werden. Wenn die Schriftart sehr groß ist, ist möglicherweise nur ein Teil der Daten für die Verarbeitung bestimmter Zeichenfolgen erforderlich. DirectWrite stellt zusätzliche Methoden zur Verfügung, mit denen Teile der Schriftartdaten angefordert werden können, die für bestimmte Inhalte benötigt werden: [**EnqueueCharacterDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuecharacterdownloadrequest) und [**EnqueueGlyphDownloadRequest.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueueglyphdownloadrequest)  

Angenommen, der Ansatz, der in der App verwendet werden soll, besteht in der Möglichkeit, die Verarbeitung zunächst mit lokalen, alternativen oder Fallbackschriftarten zu ermöglichen. Die IDWriteFontFallback::[**MapCharacters-Methode**](idwritefontfallback-mapcharacters.md) kann verwendet werden, um lokale Fallbackschriftarten zu identifizieren, und es wird auch automatisch eine Anforderung zum Herunterladen der bevorzugten Schriftart in die Quege gestellt. Wenn [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) verwendet wird und ein Teil oder der ganze Text im Layout mithilfe eines Remoteschriftartverweises formatiert wird, verwendet DirectWrite automatisch die **MapCharacters-Methode,** um lokale Fallbackschriftarten zu erhalten und eine Anforderung zum Herunterladen der Remoteschriftartdaten in die Enqueue zu stellen. 

DirectWrite verwaltet eine Downloadwarteschlange für Schriftarten für jede Factory, und die Anforderungen, die mit den oben genannten Methoden gesendet werden, werden dieser Warteschlange hinzugefügt. Die Downloadwarteschlange für Schriftarten kann mithilfe der [**IDWriteFactory3::GetFontDownloadQueue-Methode ermittelt**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getfontdownloadqueue) werden. 

Wenn eine Downloadanforderung erfolgt, die Schriftartdaten aber bereits lokal sind, führt dies zu einem No-Op: Der Downloadwarteschlange wird nichts hinzugefügt. Eine App kann überprüfen, ob die Warteschlange leer ist oder Downloadanforderungen ausstehen, indem sie die [**IDWriteFontDownloadQueue::IsEmpty-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-isempty) aufruft. 

Nachdem der Warteschlange Remoteschriftartanforderungen hinzugefügt wurden, muss der Downloadprozess initiiert werden. Wenn Remoteschriftarten in [**IDWriteTextLayout verwendet**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)werden, wird der Download automatisch initiiert, wenn die App **IDWriteTextLayout-Methoden** aufruft, die Layout- oder Renderingvorgänge erzwingen, z. B. die GetLineMetrics- oder Draw-Methoden. In anderen Szenarien muss die App den Download direkt initiieren, indem sie [**IDWriteFontDownloadQueue::BeginDownload aufruft.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload)  

Wenn ein Download abgeschlossen ist, muss die App entsprechende Aktionen ausführen– mit ausstehenden Vorgängen fortfahren oder Vorgänge wiederholen, die anfänglich mit Fallbackschriftarten durchgeführt wurden. (Wenn DirectWrite Textlayout von DirectWrite, kann [**IDWriteTextLayout3::InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) verwendet werden, um die temporären Ergebnisse zu löschen, die mit Fallbackschriftarten berechnet wurden.) Damit die App benachrichtigt wird, wenn der Downloadvorgang abgeschlossen ist, und um entsprechende Aktionen durchzuführen, muss die App eine Implementierung der [**IDWriteFontDownloadListener-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) bereitstellen und diese an den BeginDownload-Aufruf übergeben. 

> [!IMPORTANT]
> Sicherheits-/Leistungshinweis: Wenn versucht wird, eine Remoteschriftart zu abrufen, gibt es keine Garantie dafür, dass Windows eine Antwort vom Server erhalten. Wenn der Server nicht antwortet, Windows schließlich ein Time out. Dies kann jedoch einige Minuten dauern, wenn mehrere Remoteschriftarten abgerufen werden, aber ein Fehler auftut. Der BeginDownload-Aufruf wird sofort angezeigt. Apps sollten die Benutzeroberfläche nicht blockieren, während darauf gewartet wird, [**dass IDWriteFontDownloadListener::D ownloadCompleted**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadlistener-downloadcompleted) aufgerufen wird. 

 

Beispielimplementierungen dieser Interaktionen mit der Downloadwarteschlange für Schriftarten von DirectWrite und der [**IDWriteFontDownloadListener-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) finden Sie im [DirectWrite Custom Font Sets-Beispiel](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)und im [DirectWrite Downloadable Fonts-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont). 

### <a name="creating-a-custom-font-set-using-font-data-loaded-into-memory"></a>Erstellen eines benutzerdefinierten Schriftartensets mithilfe von in den Arbeitsspeicher geladenen Schriftartdaten

So wie sich die Low-Level-Vorgänge zum Lesen von Daten aus einer Schriftartdatei für Dateien auf einem lokalen Datenträger und Remotedateien im Web unterscheiden, gilt dies auch für Schriftartdaten, die in einen Speicherpuffer geladen werden. Eine neue Schnittstelle auf niedriger Ebene für die Verarbeitung von In-Memory-Schriftartdaten wurde im Windows 10 Creators Update [**IDWriteInMemoryFontFileLoader hinzugefügt.**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) 

Wie bei einem Remote-Schriftartdateilademodul muss ein In-Memory-Schriftartdateilademodul zuerst bei einer DirectWrite werden. Das Lader muss von der App so lange gehalten werden, wie die zugeordneten Schriftarten verwendet werden. Sobald die Schriftarten nicht mehr verwendet werden und irgendwann, bevor die Factory zerstört wird, muss die Registrierung des Ladeers aufgehoben werden. Dies kann im Destruktor für die Klasse erfolgen, die das Ladeobjekt besitzt. Diese Schritte werden unten gezeigt. 

Wenn die App separate Informationen zu den Schriftartgesichtern enthält, die durch die Daten dargestellt werden, kann sie einem Schriftartensatz-Generator mit angegebenen benutzerdefinierten Eigenschaften einzelne Schriftartenverweise hinzufügen. Da sich die Schriftartdaten jedoch im lokalen Speicher befindet, ist dies nicht erforderlich. DirectWrite können die Daten direkt lesen, um die Eigenschaftswerte zu ableiten. 

DirectWrite davon aus, dass die Schriftartdaten im OpenType-Rohformat vorliegen, das einer OpenType-Datei entspricht (TTF-, OTF-, TTC-, ABER-DATEI), aber im Arbeitsspeicher und nicht auf dem Datenträger. Die Daten dürfen nicht im WOFF- oder WOFF2-Containerformat vorliegen. Die Daten können eine OpenType-Schriftartsammlung darstellen. Wenn keine benutzerdefinierten Eigenschaften verwendet werden, kann die [**IDWriteFontSetBuilder1::AddFontFile-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) verwendet werden, um alle Schriftartgesichter in den Daten in einem einzigen Aufruf hinzuzufügen. 

Ein wichtiger Aspekt für das In-Memory-Szenario ist die Lebensdauer der Daten. Wenn ein Zeiger auf den Puffer für DirectWrite ohne einen eindeutigen Hinweis darauf bereitgestellt wird, dass ein Besitzer vorhanden ist, macht DirectWrite eine Kopie der Daten in einen neuen Speicherpuffer, den er besitzt. Um das Kopieren von Daten und zusätzliche Speicherzuweisungen zu vermeiden, kann die App ein Datenbesitzerobjekt übergeben, das IUnknown implementiert und den Speicherpuffer besitzt, der die Schriftartdaten enthält. Durch die Implementierung dieser Schnittstelle kann DirectWrite verweisanzahl des Objekts hinzufügen und so die Lebensdauer der eigenen Daten sicherstellen. 

Die Methode zum Erstellen eines benutzerdefinierten Schriftartensets mit In-Memory-Schriftartdaten lautet wie folgt: dies erfordert die Windows 10 Creators Update. Dabei wird von einem von der App implementierten Datenbesitzerobjekt ausgegangen, das IUnknown implementiert und über Methoden verfügt, die einen Zeiger auf den Speicherpuffer und die Größe des Puffers zurückgeben. 

<dl> 1. Erstellen Sie wie oben gezeigt eine IDWriteFactory5-Schnittstelle.  
2.Erstellen Sie [**wie oben gezeigt eine IDWriteFontSetBuilder1-Schnittstelle.**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1)  
3. Verwenden Sie die Factory, um einen IDWriteInMemoryFontFileLoader zu erhalten. 


```C++
 IDWriteInMemoryFontFileLoader* pInMemoryFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateInMemoryFontFileLoader(&pInMemoryFontFileLoader); 
}
```



Dadurch wird eine vom System bereitgestellte Implementierung der Schnittstelle des In-Memory-Schriftartdateilademoduls zurückgegeben.   
4. Registrieren Sie das In-Memory-Schriftartdateilademodul bei der Factory. 


```C++
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->RegisterFontFileLoader(pInMemoryFontFileLoader); 
}
```



   
5. Verwenden Sie für jede In-Memory-Schriftartdatei das In-Memory-Schriftartdateiladeprogramm, um eine [**IDWriteFontFile zu erstellen.**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) 


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



   
6. Fügen Sie [**das IDWriteFontFile-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) dem Schriftartensatz-Generator mithilfe der [**AddFontFile-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) hinzu, wie oben gezeigt.  Wenn dies notwendig ist, kann die App stattdessen einzelne [**IDWriteFontFaceReference-Objekte**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) basierend auf **idWriteFontFile** erstellen, optional benutzerdefinierte Eigenschaften für jeden Schriftartgesichtsverweis definieren und dann den Schriftartengesichtsverweis mit benutzerdefinierten Eigenschaften dem Schriftartensatz mithilfe der [**AddFontFaceReference-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) hinzufügen, wie oben gezeigt.   
7. Nachdem alle Schriftarten dem Schriftartensatz-Generator hinzugefügt wurden, erstellen Sie den benutzerdefinierten Schriftartensatz, wie oben gezeigt.   
8. Wenn die Schriftarten im Arbeitsspeicher nicht mehr verwendet werden, müssen Sie die Registrierung des In-Memory-Schriftartdateilademoduls aufheben. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pInMemoryFontFileLoader);
```



  
</dl>

 

## <a name="advanced-scenarios"></a>Erweiterte Szenarios

Einige Apps verfügen möglicherweise über besondere Anforderungen, die eine erweiterte Verarbeitung erfordern, als oben beschrieben. 

### <a name="combining-font-sets"></a>Kombinieren von Schriftartsätzen

Einige Apps müssen möglicherweise einen Schriftartensatz erstellen, der eine Kombination aus Elementen aus anderen Schriftartensätzen umfasst. Beispielsweise kann eine App einen Schriftartensatz erstellen, der alle auf dem System installierten Schriftarten mit einer Auswahl benutzerdefinierter Schriftarten kombiniert oder installierte Schriftarten kombiniert, die bestimmte Kriterien mit anderen Schriftarten erfüllen. DirectWrite verfügt über APIs zur Unterstützung der Bearbeitung und Kombination von Schriftartsätzen. 

Um zwei oder mehr Schriftartensätze zu kombinieren, fügt die [**IDWriteFontSetBuilder::AddFontSet-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontset) alle Schriftarten in einem angegebenen Schriftartensatz hinzu, die einem Schriftartensatz-Generator in einem einzigen Aufruf hinzugefügt werden sollen. Wenn nur bestimmte Schriftarten aus einem vorhandenen Schriftartensatz im neuen Schriftartensatz verwendet werden sollen, kann die [**IDWriteFontSet::GetMatchingFonts-Methode**](idwritefontset-getmatchingfonts-overload.md) verwendet werden, um ein neues Schriftartensatzobjekt zu leiten, das gefiltert wurde, um nur Schriftarten zu enthalten, die mit den angegebenen Eigenschaften übereinstimmen. Diese Methoden bieten eine einfache Möglichkeit, einen benutzerdefinierten Schriftartensatz zu erstellen, der Schriftarten aus zwei oder mehr vorhandenen Schriftartensätzen kombiniert. 

### <a name="using-local-woff-or-woff2-font-data"></a>Verwenden von lokalen WOFF- oder WOFF2-Schriftartdaten

Wenn eine App Schriftartdateien im lokalen Dateisystem oder in einem Speicherpuffer enthält, aber das WOFF- oder WOFF2-Containerformat verwendet, stellt DirectWrite (Windows 10 Creator Update oder höher) eine Methode zum Entpacken des Containerformats, [**IDWriteFactory5::UnpackFontFile,**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile)zur Verfügung, die [**idWriteFontFileStream zurückgibt.**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 

Die App benötigt jedoch eine Möglichkeit, [**idWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) in ein Ladeobjekt der Schriftartdatei zu übertragen. Eine Möglichkeit besteht in der Erstellung einer benutzerdefinierten [**IDWriteFontFileLoader-Implementierung,**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) die den Stream umschließt. Wie bei anderen Schriftartdateiladern muss dies vor der Verwendung registriert und die Registrierung aufgehoben werden, bevor die Factory den Gültigkeitsbereich übergeht.  

Wenn das benutzerdefinierte Ladeprogramm auch mit unformatiert (nicht gepackten) Schriftartdateien verwendet wird, muss die App auch eine benutzerdefinierte Implementierung der [**IDWriteFontFileStream-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) für die Verarbeitung dieser Dateien bereitstellen. Es gibt jedoch einfachere Möglichkeiten, apIs, die oben erläutert werden, für die Verarbeitung von Unformatieren von Schriftartdateien zu verwenden. Die Notwendigkeit einer benutzerdefinierten Streamimplementierung kann vermieden werden, indem separate Codepfade für gepackte Schriftartdateien im Vergleich zu unformatierten Schriftartdateien verwendet werden. 

Nachdem ein benutzerdefiniertes Schriftartdateiladeobjekt erstellt wurde, werden die gepackten Schriftartdateidaten app-spezifisch zum Lader hinzugefügt. Das Lader kann mehrere Schriftartdateien verarbeiten, von denen jede mithilfe eines von der App definierten Schlüssels identifiziert wird, der nicht transparent DirectWrite. Nachdem dem Ladeprogramm eine gepackte Schriftartdatei hinzugefügt wurde, wird die [**IDWriteFactory::CreateCustomFontFileReference-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) verwendet, um eine [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) basierend auf diesem Ladeprogramm für die Schriftartdaten zu erhalten, die durch einen bestimmten Schlüssel identifiziert werden.  

Das eigentliche Entpacken der Schriftartdaten kann durchgeführt werden, wenn Schriftarten zum Ladeprogramm hinzugefügt werden, aber auch in der [**IDWriteFontFileLoader::CreateStreamFromKey-Methode,**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) die DirectWrite aufruft, wenn die Schriftartdaten zum ersten Mal gelesen werden müssen. 

Nachdem ein IDWriteFontFile-Objekt erstellt wurde, sind die verbleibenden Schritte zum Hinzufügen der Schriftarten zu einem benutzerdefinierten Schriftartensatz wie oben beschrieben. 

Eine Implementierung, die diesen Ansatz verwendet, wird im beispiel DirectWrite [Custom Font Sets veranschaulicht.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/) 

### <a name="using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation"></a>Verwenden DirectWrite Remoteschriftartmechanismen mit benutzerdefinierter Low-Level-Netzwerkimplementierung

Die DirectWrite-Mechanismen für die Verarbeitung von Remoteschriftarten können in Mechanismen auf höherer Ebene unterteilt werden, die Schriftartensätze enthalten, die Schriftartverweise für Remoteschriftarten enthalten, die Ortslage der Schriftartdaten überprüfen und die Warteschlange für Downloadanforderungen von Schriftarten verwalten, und die Mechanismen auf niedrigerer Ebene, die den tatsächlichen Download verarbeiten. Einige Apps möchten möglicherweise die remoten Schriftartmechanismen auf höherer Ebene nutzen, erfordern aber auch benutzerdefinierte Netzwerkinteraktionen, z. B. die Kommunikation mit Servern mit anderen Protokollen als HTTP. 

In diesem Fall muss eine App eine benutzerdefinierte Implementierung der [**IDWriteRemoteFontFileLoader-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) erstellen, die auf die erforderliche Weise mit anderen Schnittstellen auf niedrigerer Ebene interagiert. Die App muss auch benutzerdefinierte Implementierungen dieser Schnittstellen auf niedrigerer Ebene bereitstellen: [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream)und [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult). Diese drei Schnittstellen verfügen über Rückrufmethoden, DirectWrite während Downloadvorgängen aufrufen. 

Wenn [**IDWriteFontDownloadQueue::BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload) aufgerufen wird, fragt DirectWrite das Remoteschriftartdateiladeprogramm über die Lokalität der Daten ab und fordert den Remotestream an. Wenn die Daten nicht lokal sind, rufen sie die BeginDownload-Methode des Streams auf. Die Streamimplementierung sollte bei diesem Aufruf nicht blockieren, sondern sofort zurückgeben und ein [**IDWriteAsyncResult-Objekt**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) zurückgeben, das das Wait-Handle bereitstellt, das DirectWrite verwendet, um auf den asynchronen Downloadvorgang zu warten. Die implementierung des benutzerdefinierten Streams ist für die Verarbeitung der Remotekommunikation verantwortlich. Wenn das Abschlussereignis aufgetreten ist, ruft DirectWrite [**IDWriteAsyncResult::GetResult**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteasyncresult-getresult) auf, um das Ergebnis des Vorgangs zu bestimmen. Wenn das Ergebnis erfolgreich ist, wird erwartet, dass nachfolgende ReadFragment-Aufrufe des Streams für die heruntergeladenen Bereiche erfolgreich sind. 

> [!IMPORTANT]
> Sicherheits-/Leistungshinweis: Wenn versucht wird, eine Remoteschriftart abzurufen, besteht im Allgemeinen das Potenzial, dass ein Angreifer den vorgesehenen Server spooft oder dass der Server möglicherweise nicht reagiert. Wenn Sie benutzerdefinierte Netzwerkinteraktionen implementieren, haben Sie möglicherweise mehr Kontrolle über Risikominderungen als bei Drittanbieterservern. Es liegt jedoch an Ihnen, geeignete Gegenmaßnahmen in Betracht zu ziehen, um die Offenlegung von Informationen oder Denial-of-Service zu vermeiden. Sichere Protokolle wie HTTPS werden empfohlen. Außerdem sollten Sie ein Timeout erstellen, damit das an DirectWrite zurückgegebene Ereignishandle schließlich festgelegt wird. 

 

### <a name="supporting-scenarios-on-earlier-windows-versions"></a>Unterstützen von Szenarien in früheren Windows Versionen

Die beschriebenen Szenarien können in DirectWrite in früheren Versionen von Windows unterstützt werden, erfordern jedoch eine viel mehr benutzerdefinierte Implementierung durch die App mit den eingeschränkteren APIs, die vor Windows 10 verfügbar waren. Weitere Informationen finden Sie unter [Benutzerdefinierte Schriftartsammlungen (Windows 7/8).](custom-font-collections.md)

 

 