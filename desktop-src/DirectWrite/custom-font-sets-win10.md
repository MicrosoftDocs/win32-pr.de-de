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
-   [Schriftarten und Schriftdateiformate](#fonts-and-font-file-formats)
-   [Schriftartsätze und Schriftartauflistungen](#font-sets-and-font-collections)
-   [Gängige Szenarios](#common-scenarios)
    -   [Erstellen eines Schriftartsatzes mithilfe beliebiger Schriftarten im lokalen Dateisystem](#creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system)
    -   [Erstellen eines Schriftartsatzes mit bekannten Schriftarten im lokalen Dateisystem](#creating-a-font-set-using-known-fonts-in-the-local-file-system)
    -   [Erstellen eines benutzerdefinierten Schriftartensatzes mit bekannten Remoteschriftarten im Web](#creating-a-custom-font-set-using-known-remote-fonts-on-the-web)
    -   [Erstellen eines benutzerdefinierten Schriftartsatzes mit in den Arbeitsspeicher geladenen Schriftartdaten](#creating-a-custom-font-set-using-font-data-loaded-into-memory)
-   [Erweiterte Szenarien](#advanced-scenarios)
    -   [Kombinieren von Schriftartsätzen](#combining-font-sets)
    -   [Verwenden lokaler WOFF- oder WOFF2-Schriftartdaten ](#using-local-woff-or-woff2-font-data)
    -   [Verwenden von DirectWrite Remoteschriftartmechanismen mit benutzerdefinierter Netzwerkimplementierungen auf niedriger Ebene](#using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation)
    -   [Unterstützen von Szenarien in früheren Windows Versionen](#supporting-scenarios-on-earlier-windows-versions)

## <a name="introduction"></a>Einführung

In den meisten Jahren verwenden Apps die Schriftarten, die lokal auf dem System installiert sind. DirectWrite ermöglicht den Zugriff auf diese Schriftarten mithilfe der Methoden [**IDWriteFactory3::GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) oder [**IDWriteFactory::GetSystemFontCollection.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) In einigen Fällen möchten Apps möglicherweise auch Schriftarten verwenden, die als Teil von Windows 10 enthalten sind, aber derzeit nicht auf dem aktuellen System installiert sind. Auf diese Schriftarten kann über den Windows Schriftartdienst zugegriffen werden, indem die **GetSystemFontSet-Methode** oder [**IDWriteFactory3::GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection) aufgerufen wird, wobei includeDownloadableFonts auf TRUE festgelegt ist. 

In einigen Anwendungsszenarien müssen Apps jedoch Schriftarten verwenden, die nicht im System installiert sind und nicht vom Windows Font Service bereitgestellt werden. Im Folgenden finden Sie Beispiele für solche Szenarien:

-   Schriftarten werden als Ressourcen in eine App-Binärdatei eingebettet.
-   Schriftartdateien werden in einem App-Paket gebündelt und auf dem Datenträger im Installationsordner der App gespeichert.
-   Die App ist ein Tool für die Entwicklung von Schriftarten, das benutzerdefinierte Schriftartdateien laden muss. 
-   Schriftarten werden in Dokumentdateien eingebettet, die in der App angezeigt oder bearbeitet werden können. 
-   Die App verwendet Schriftarten, die von einem öffentlichen Webdienst abgerufen wurden. 
-   Die App verwendet Schriftartdaten, die über ein privates Netzwerkprotokoll gestreamt werden. 

DirectWrite bietet APIs für die Arbeit mit benutzerdefinierten Schriftarten in diesen und anderen ähnlichen Szenarien. Die benutzerdefinierten Schriftartdaten können aus Dateien im lokalen Dateisystem stammen. aus remoten, cloudbasierten Quellen, auf die über HTTP zugegriffen wird; oder aus beliebigen Quellen, nachdem sie in einen Speicherpuffer geladen wurden. 

> [!Note]  
> Während DirectWrite seit Windows 7 APIs für die Arbeit mit benutzerdefinierten Schriftarten bereitgestellt hat, wurden neuere APIs in Windows 10 und erneut im Windows 10 Creators Update (Vorschaubuild 15021 oder höher) hinzugefügt, die die Implementierung mehrerer der erwähnten Szenarien vereinfachen. Dieses Thema konzentriert sich auf APIs, die in Fenster 10 verfügbar sind. Informationen zu Anwendungen, die mit früheren Windows Versionen funktionieren müssen, finden Sie unter [Custom Font Collections (Windows 7/8) (Benutzerdefinierte Schriftartsammlungen (Windows 7/8)).](custom-font-collections.md) 

 

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

Um die DirectWrite APIs für die Arbeit mit benutzerdefinierten Schriftarten zu verstehen, kann es hilfreich sein, das konzeptionelle Modell zu verstehen, das diesen APIs zugrundeliegt. Wichtige Konzepte werden hier beschrieben. 

Wenn DirectWrite das tatsächliche Textlayout oder -rendern übernimmt, muss auf die tatsächlichen Schriftartdaten zugegriffen werden. Ein Schriftart-Gesichtsobjekt enthält tatsächliche Schriftartdaten, die im lokalen System vorhanden sein müssen. Für andere Vorgänge, z. B. das Überprüfen der Verfügbarkeit einer bestimmten Schriftart oder das Präsentieren von Schriftartoptionen für einen Benutzer, ist nur ein Verweis auf eine bestimmte Schriftart erforderlich, nicht auf die tatsächlichen Schriftartdaten selbst. In DirectWrite enthält ein Schriftart-Gesichtsverweisobjekt nur die Informationen, die zum Suchen und Instanziieren einer Schriftart erforderlich sind. Da der Schriftarten-Gesichtsverweis keine tatsächlichen Daten enthält, können DirectWrite mit Schriftart-Gesichtsverweisen umgehen, für die sich die tatsächlichen Daten an einem Remotenetzwerkspeicherort befinden und wenn die tatsächlichen Daten lokal sind.

Ein Schriftsatz ist ein Satz von Schriftartgesichtsverweisen zusammen mit bestimmten grundlegenden Informationseigenschaften, die beim Verweisen auf die Schriftart oder beim Vergleichen mit anderen Schriftarten, z. B. dem Familiennamen, oder einem Schriftbreitenwert verwendet werden können. Die tatsächlichen Daten für die verschiedenen Schriftarten können lokal oder remote oder eine Mischung sein.

Ein Schriftsatz kann verwendet werden, um ein entsprechendes Schriftartauflistungsobjekt abzurufen. Weitere Informationen finden Sie weiter unten unter Schriftartensätze und Schriftartsammlungen. 

Die IDWriteFontSet-Schnittstelle stellt Methoden bereit, die das Abfragen von Eigenschaftswerten wie family name oder font-weight oder für Schriftartengesichtsverweise ermöglichen, die mit bestimmten Eigenschaftswerten übereinstimmen. Nach dem Filtern nach einer bestimmten Auswahl kann eine Instanz der [**IDWriteFontFaceReference-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) mit Methoden zum Herunterladen (wenn sich die tatsächlichen Schriftartdaten derzeit remote befinden) zum Abrufen des entsprechenden [**IDWriteFontFace3-Objekts**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) abgerufen werden, das für Layout und Rendering verwendet werden kann. 

Die IDWriteFontFile-Schnittstelle unterliegt jedem Schriftart- oder Schriftart-Gesichtsverweis. Dies stellt den Speicherort einer Schriftartdatei dar und besteht aus zwei Komponenten: einem Schriftartdateiladeprogramm und einem Schriftartdateischlüssel. Das Schriftartdateiladeprogramm ([**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader)) wird verwendet, um bei Bedarf eine Datei zu öffnen, und gibt einen Stream mit den Daten zurück ([**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)). Je nach Ladeprogramm können sich die Daten in einem lokalen Dateipfad, einer Remote-URL oder in einem Speicherpuffer befinden. Der Schlüssel ist ein vom Ladeprogramm definierter Wert, der die Datei innerhalb des Ladeprogrammkontexts eindeutig identifiziert, sodass das Ladeprogramm die Daten suchen und einen Datenstrom dafür erstellen kann. 

Benutzerdefinierte Schriftarten können problemlos einem benutzerdefinierten Schriftartensatz hinzugefügt werden, der wiederum zum Filtern oder Organisieren von Schriftartinformationen für Zwecke wie das Erstellen einer Benutzeroberfläche für die Schriftartauswahl verwendet werden kann. Der Schriftsatz kann auch verwendet werden, um eine Schriftartauflistung für die Verwendung in übergeordneten APIs wie [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) und [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)zu erstellen. Die [**IDWriteFontSetBuilder-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) kann verwendet werden, um einen benutzerdefinierten Schriftartensatz zu erstellen, der mehrere benutzerdefinierte Schriftarten enthält. Sie kann auch verwendet werden, um einen benutzerdefinierten Schriftartensatz zu erstellen, der benutzerdefinierte Schriftarten und vom System bereitgestellte Schriftarten kombiniert. oder , das Schriftarten mit verschiedenen Quellen für die tatsächlichen Daten kombiniert: lokaler Speicher, Remote-URLs und Arbeitsspeicher. 

Wie bereits erwähnt, kann ein Schriftarten-Gesichtsverweis auf Schriftartdaten in einer Remotequelle verweisen, aber die Daten müssen lokal sein, um ein Schriftart-Gesichtsobjekt zu erhalten, das für Layout und Rendering verwendet werden kann. Das Herunterladen von Remotedaten wird von einer Warteschlange zum Herunterladen von Schriftarten verarbeitet. Apps können die [**IDWriteFontDownloadQueue-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) verwenden, um Anforderungen zum Herunterladen von Remoteschriftarten in die Queue einzubetten, um den Downloadvorgang zu initiieren, und um ein [**IDWriteFontDownloadListener-Objekt**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) zu registrieren, um maßnahmen zu ergreifen, wenn der Downloadvorgang abgeschlossen ist. 

Für die meisten der hier beschriebenen Schnittstellen stellt DirectWrite Systemimplementierungen bereit. Eine Ausnahme ist die [**IDWriteFontDownloadListener-Schnittstelle,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) die eine App implementiert, um app-spezifische Aktionen auszuführen, wenn Remoteschriftarten lokal heruntergeladen wurden. Apps haben möglicherweise Grund, ihre eigenen benutzerdefinierten Implementierungen für bestimmte andere Schnittstellen bereitzustellen, obwohl dies nur in bestimmten, komplexeren Szenarien erforderlich wäre. Beispielsweise muss eine App eine benutzerdefinierte Implementierung der [**IDWriteFontFileLoader-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) bereitstellen, um Schriftartdateien im lokalen Speicher zu verarbeiten, die das WOFF2-Containerformat verwenden. Weitere Details finden Sie weiter unten. 

## <a name="fonts-and-font-file-formats"></a>Schriftarten und Schriftdateiformate

Ein weiteres wichtiges Konzept, das Sie verstehen können, ist die Beziehung zwischen einzelnen Schriftarten und Schriftartdateien, die diese enthalten. Die Idee einer OpenType-Schriftartdatei (TTF oder OTF), die eine einzelne Schriftart enthält, ist vertraut. Das OpenType-Schriftformat ermöglicht jedoch auch eine OpenType-Schriftartenauflistung (TTC oder .protokoll), bei der es sich um eine einzelne Datei handelt, die mehrere Schriftarten enthält. OpenType Collection-Dateien werden häufig für große Schriftarten verwendet, die eng miteinander verknüpft sind und identische Werte für bestimmte Schriftartdaten aufweisen: Durch Kombinieren der Schriftarten in einer einzelnen Datei können die allgemeinen Daten dedupliziert werden. Aus diesem Grund muss ein Schriftarten- oder Schriftartgesichtsverweis nicht nur auf eine Schriftartdatei (oder eine entsprechende Datenquelle) verweisen, sondern auch einen Schriftartindex innerhalb dieser Datei angeben, für den allgemeinen Fall, in dem die Datei eine Sammlungsdatei sein kann. 

Bei Schriftarten, die im Web verwendet werden, werden Schriftartdaten häufig in bestimmte Containerformate (WOFF oder WOFF2) gepackt, die eine gewisse Komprimierung der Schriftartdaten und ein gewisses Maß an Schutz vor Verstößen und Verstößen gegen Schriftartlizenzen bieten. Funktionell entspricht eine WOFF- oder WOFF2-Datei einer OpenType-Schriftart oder einer Schriftartsammlungsdatei, aber die Daten werden in einem anderen Format codiert, das entpackt werden muss, bevor sie verwendet werden können. 

Bestimmte DirectWrite-APIs können mit einzelnen Schriftarten umgehen, während andere APIs Dateien verarbeiten können, die OpenType Collection-Dateien enthalten können, die mehrere Gesichter enthalten. Auf ähnliche Weise verarbeiten bestimmte APIs nur unformatierte Daten im OpenType-Format, während andere APIs die gepackten Containerformate WOFF und WOFF2 verarbeiten können. Diese Details finden Sie in der folgenden Erläuterung. 

## <a name="font-sets-and-font-collections"></a>Schriftartsätze und Schriftartauflistungen

Einige Anwendungen können implementiert werden, um mit Schriftarten zu arbeiten, die die [**IDWriteFontCollection-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) verwenden. Es gibt eine direkte Entsprechung zwischen einer Schriftartsammlung und einem Schriftartsatz. Jede kann die gleichen Schriftarten enthalten, aber sie stellen sie in einer anderen Organisation dar. Aus einer beliebigen Schriftartenauflistung kann ein entsprechender Schriftsatz abgerufen werden (und umgekehrt).

Wenn Sie mit einer Reihe von benutzerdefinierten Schriftarten arbeiten, ist es am einfachsten, eine Schriftartensatz-Generator-Schnittstelle zu verwenden, um einen benutzerdefinierten Schriftartensatz zu erstellen und dann eine Schriftartenauflistung abzurufen, nachdem der Schriftartensatz erstellt wurde. Der Prozess zum Erstellen eines benutzerdefinierten Schriftartsatzes wird unten ausführlich beschrieben. Um eine [**IDWriteFontCollection1-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) aus einem Schriftartsatz abzurufen, wird die [**IDWriteFactory3::CreateFontCollectionFromFontSet-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-createfontcollectionfromfontset) verwendet.

Wenn die App über ein Sammlungsobjekt verfügt und einen entsprechenden Schriftartsatz abrufen muss, kann dies mit der [**IDWriteFontCollection1::GetFontSet-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontcollection1-getfontset) erfolgen. 

## <a name="common-scenarios"></a>Häufige Szenarien

In diesem Abschnitt werden einige der gängigsten Szenarien mit benutzerdefinierten Schriftartsätzen beschrieben:

-   Erstellen eines benutzerdefinierten Schriftartsatzes mithilfe beliebiger Schriftarten in Pfaden im lokalen Dateisystem.
-   Erstellen eines benutzerdefinierten Schriftartsatzes mit bekannten Schriftarten (möglicherweise gebündelt mit der App), die im lokalen Dateisystem gespeichert sind.
-   Erstellen eines benutzerdefinierten Schriftartsatzes mit bekannten Remoteschriftarten im Web.
-   Erstellen eines benutzerdefinierten Schriftartsatzes mithilfe von Schriftartdaten, die in den Arbeitsspeicher geladen werden.

Vollständige Implementierungen für diese Szenarien finden Sie im DirectWrite Beispiel für [benutzerdefinierte Schriftartensätze.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/) Dieses Beispiel veranschaulicht auch ein erweitertes Szenario für die Verarbeitung von Schriftartdaten, die in WOFF- oder WOFF2-Containerformaten verpackt sind. Dies wird im Folgenden erläutert. 

### <a name="creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system"></a>Erstellen eines Schriftartsatzes mithilfe beliebiger Schriftarten im lokalen Dateisystem

Beim Umgang mit einem beliebigen Satz von Schriftartdateien im lokalen Speicher ist die [**IDWriteFontSetBuilder1::AddFontFile-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) praktisch, da sie in einem einzelnen Aufruf alle Schriftartgesichter in einer OpenType-Schriftartauflistungsdatei sowie alle Instanzen für eine OpenType-Variablenschriftart verarbeiten kann. Dies ist im Windows 10 Creators Update (Vorschauversion Build 15021 oder höher) verfügbar und wird empfohlen, sofern verfügbar. 

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



   
2. Verwenden Sie die Factory, um die <a href=""></a> [**IDWriteFontSetBuilder1-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) abzurufen: 


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



   
4. Fügen Sie das [**IDWriteFontFile-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) mithilfe der [**AddFontFile-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) dem Schriftartensatz-Generator hinzu: 


```C++
hr = pFontSetBuilder->AddFontFile(pFontFile); 
```

Wenn der im Aufruf von [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) angegebene Dateipfad auf eine andere als eine unterstützte OpenType-Datei verweist, gibt der Aufruf von [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) einen Fehler zurück, DWRITE \_ E \_ FILEFORMAT.

5. Nachdem alle Dateien dem Schriftartensatz-Generator hinzugefügt wurden, kann der benutzerdefinierte Schriftsatz erstellt werden: 


```C++
IDWriteFontSet* pFontSet; 
hr = pFontSetBuilder->CreateFontSet(&pFontSet); 
```



   
</dl>

Wenn die App auf Windows 10 Versionen vor dem Windows 10 Creators Update ausgeführt werden muss, ist die AddFontFile-Methode nicht verfügbar. Verfügbarkeit kann durch Erstellen einer [**IDWriteFactory3-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) und anschließendes Verwenden von QueryInterface zum Abrufen einer [**IDWriteFactory5-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) erkannt werden: Wenn dies erfolgreich ist, sind auch die [**IDWriteFontSetBuilder1-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) und die [**AddFontFile-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) verfügbar.

Wenn die AddFontFile-Methode nicht verfügbar ist, muss die [**IDWriteFontSetBuilder::AddFontFaceReference-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) verwendet werden, um einzelne Schriftartgesichter hinzuzufügen. Um OpenType-Schriftartsammlungsdateien zu ermöglichen, die mehrere Gesichter enthalten, kann die [**IDWriteFontFile::Analyze-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) verwendet werden, um die Anzahl der in der Datei enthaltenen Gesichter zu bestimmen. Der Prozess sieht wie folgt aus.

<dl> 1.Erstellen Sie zunächst die <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3-Schnittstelle:</a> 


```C++
IDWriteFactory3* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



  
2. Verwenden Sie die Factory, um die [**IDWriteFontSetBuilder-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) abzurufen: 


```C++
IDWriteFontSetBuilder* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
} 
```



  
3. Erstellen Sie für jede Schriftartdatei eine [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)wie oben beschrieben: 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



Anstatt die Datei direkt dem Schriftartensatz-Generator hinzuzufügen, müssen wir die Anzahl der Gesichter bestimmen und einzelne [**IDWriteFontFaceReference-Objekte**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) erstellen.   
4. Verwenden Sie die [**Analyze-Methode,**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) um die Anzahl der Gesichter in der Datei abzurufen. 


```C++
BOOL isSupported; 
DWRITE_FONT_FILE_TYPE fileType; 
UINT32 numberOfFonts; 
hr = pFontFile->Analyze(&isSupported, &fileType, /* face type */ nullptr, &numberOfFonts); 
```



Die [**Analyze-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) legt auch Werte für die Parameter isSupported und fileType fest. Wenn die Datei kein unterstütztes Format hat, lautet isSupported FALSE, und es können entsprechende Aktionen wie das Ignorieren der Datei ausgeführt werden.   
5. Durchlaufen Sie die Anzahl der Schriftarten, die im numberOfFonts-Parameter festgelegt sind. Erstellen Sie innerhalb der Schleife einen [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) für jedes Datei-Index-Paar, und fügen Sie diesen dem Schriftartensatz-Generator hinzu. 


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



  
6. Nachdem alle Gesichter dem Schriftartensatz-Generator hinzugefügt wurden, erstellen Sie den benutzerdefinierten Schriftsatz, wie oben gezeigt.  
</dl>

Eine App kann so entworfen werden, dass sie die bevorzugte [**AddFontFile-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) verwendet, wenn sie auf der Windows 10 Creators Update ausgeführt wird. Wenn sie auf früheren Windows 10 Versionen ausgeführt wird, wird jedoch ein Fallback auf die [**AddFontFaceReference-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) ausgeführt. Testen Sie wie oben beschrieben, ob die [**IDWriteFactory5-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) verfügbar ist, und verzweigen Sie sie dann entsprechend. Dieser Ansatz wird im [DirectWrite Beispiel für benutzerdefinierte Schriftartsätze](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)veranschaulicht. 

### <a name="creating-a-font-set-using-known-fonts-in-the-local-file-system"></a>Erstellen eines Schriftartsatzes mit bekannten Schriftarten im lokalen Dateisystem

Wie bereits erwähnt, wird jeder Schriftarten-Gesichtsverweis in einem Schriftsatz bestimmten Informationseigenschaften zugeordnet, z. B. Dem Familiennamen und der Schriftbreite. Wenn einem Schriftartengenerator benutzerdefinierte Schriftarten mithilfe der oben aufgeführten API-Aufrufe hinzugefügt werden, werden diese Informationseigenschaften direkt aus den tatsächlichen Schriftartdaten abgerufen, die beim Hinzufügen der Schriftart gelesen werden. Wenn eine App jedoch in einigen Situationen über eine andere Quelle von Informationen zu einer Schriftart verfügt, kann es sinnvoll sein, eigene benutzerdefinierte Werte für diese Eigenschaften bereitzustellen. 

Angenommen, eine App bündelt einige Schriftarten, die zum Darstellen bestimmter Benutzeroberflächenelemente innerhalb der App verwendet werden. Manchmal, z. B. bei einer neuen App-Version, müssen sich möglicherweise die spezifischen Schriftarten ändern, die die App für diese Elemente verwendet. Wenn die App codierte Verweise auf die spezifischen Schriftarten aufweist, erfordert das Ersetzen einer Schriftart durch eine andere, dass jeder dieser Verweise geändert werden muss. Wenn die App stattdessen benutzerdefinierte Eigenschaften verwendet, um funktionale Aliase basierend auf dem Typ des zu rendernden Elements oder Texts zuzuweisen, ordnet jeden Alias einer bestimmten Schriftart an einer Stelle zu und verwendet dann die Aliase in allen Kontexten, in denen Schriftarten erstellt und bearbeitet werden. Zum Ersetzen einer Schriftart durch eine andere muss nur die Stelle geändert werden, an der der Alias einer bestimmten Schriftart zugeordnet ist. 

Benutzerdefinierte Werte für Informationseigenschaften können zugewiesen werden, wenn die [**IDWriteFontSetBuilder::AddFontFaceReference-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) aufgerufen wird. Die Methode hierfür lautet wie folgt: kann auf jeder Windows 10 Version verwendet werden. 

Wie oben gezeigt, beginnen Sie mit dem Abrufen der Schnittstellen [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) und [**IDWriteFontSet.**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) Erstellen Sie für jedes hinzuzufügende benutzerdefinierte Schriftartgesicht eine [**IDWriteFontFaceReference,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)wie oben gezeigt. Bevor dies dem Schriftartensatz-Generator hinzugefügt wird (innerhalb der Schleife in Schritt 5, siehe oben), definiert die App jedoch die zu verwendenden benutzerdefinierten Eigenschaftswerte. 

Ein Satz benutzerdefinierter Eigenschaftswerte wird mithilfe eines Arrays von [**DWRITE \_ FONT \_ PROPERTY-Strukturen**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) definiert. Jede dieser Eigenschaften identifiziert eine bestimmte Eigenschaft aus der [**DWRITE \_ FONT \_ PROPERTY \_ ID-Enumeration**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) und den entsprechenden Eigenschaftswert, der verwendet werden soll.  

Beachten Sie, dass alle Eigenschaftswerte als Zeichenfolgen zugewiesen werden. Wenn diese später benutzern angezeigt werden, können alternative Werte für eine bestimmte Eigenschaft für verschiedene Sprachen festgelegt werden, dies ist jedoch nicht erforderlich. Beachten Sie außerdem, dass nur die angegebenen Werte innerhalb des Schriftartsatzes verwendet werden, wenn benutzerdefinierte Eigenschaftswerte von der App festgelegt werden. DirectWrite leitet keine Werte direkt von der Schriftart für Informationseigenschaften ab, die in einem Schriftartsatz verwendet werden. 

Im folgenden Beispiel werden benutzerdefinierte Werte für drei Informationseigenschaften definiert: Familienname, vollständiger Name und Schriftbreite. 


```C++
DWRITE_FONT_PROPERTY props[] = 
{ 
  { DWRITE_FONT_PROPERTY_ID_FAMILY_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_FULL_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_WEIGHT, L"400", nullptr } 
}; 
               
            
```



Nachdem Sie das gewünschte Array von Eigenschaftswerten für eine Schriftart definiert haben, rufen Sie AddFontFaceRefence auf, und übergeben Sie das Eigenschaftenarray sowie den Schriftart-Gesichtsverweis. 


```C++
hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference, props, ARRAYSIZE(props)); 
```



 

Nachdem alle benutzerdefinierten Schriftarten dem Schriftartensatz-Generator hinzugefügt wurden, erstellen Sie den benutzerdefinierten Schriftsatz zusammen mit ihren benutzerdefinierten Eigenschaften, wie oben gezeigt. 

### <a name="creating-a-custom-font-set-using-known-remote-fonts-on-the-web"></a>Erstellen eines benutzerdefinierten Schriftartensatzes mit bekannten Remoteschriftarten im Web

Benutzerdefinierte Eigenschaften sind wichtig für die Arbeit mit Remoteschriftarten. Jeder Schriftart-Gesichtsverweis muss über einige Informationseigenschaften verfügen, um die Schriftart zu charakterisieren und von anderen Schriftarten zu unterscheiden. Da die Schriftartdaten für Remoteschriftarten nicht lokal sind, können DirectWrite eigenschaften nicht direkt von den Schriftartdaten ableiten. Daher müssen Eigenschaften explizit bereitgestellt werden, wenn dem Schriftartensatz-Generator eine Remoteschriftart hinzugefügt wird.

Die Sequenz von API-Aufrufen zum Hinzufügen von Remoteschriftarten zu einem Schriftartensatz ähnelt der im vorherigen Szenario beschriebenen Sequenz. Da es sich bei den Schriftartdaten jedoch um Remotedaten handelt, unterscheiden sich die Vorgänge zum Lesen der tatsächlichen Schriftartdaten von der Arbeit mit Dateien im lokalen Speicher. In diesem Fall wurde dem Windows 10 Creators Update eine neue Schnittstelle auf niedrigerer Ebene hinzugefügt: [**IDWriteRemoteFontFileLoader.**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) 

Um das Remote-Schriftartdateiladeprogramm zu verwenden, muss es zuerst bei einer DirectWrite Factory registriert werden. Das Ladeprogramm muss von der App so lange aufbewahrt werden, wie die ihr zugeordneten Schriftarten verwendet werden. Sobald die Schriftarten nicht mehr verwendet werden und zu einem bestimmten Zeitpunkt, bevor die Factory zerstört wird, muss die Registrierung des Ladeprogramm aufgehoben werden. Dies kann im Destruktor für die Klasse erfolgen, die das Ladeprogrammobjekt besitzt. Diese Schritte werden unten gezeigt. 

Die Methode zum Erstellen eines benutzerdefinierten Schriftartsatzes mitHilfe von Remoteschriftarten lautet wie folgt: dies erfordert die Windows 10 Creators Update.  

<dl> 1. Erstellen Sie wie oben gezeigt eine IDWriteFactory5-Schnittstelle.   
2.Erstellen Sie wie oben gezeigt eine <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">IDWriteFontSetBuilder-Schnittstelle.</a>   
3. Verwenden Sie die Factory, um einen <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader">IDWriteRemoteFontFileLoader</a>abzurufen. 


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



Dadurch wird eine vom System bereitgestellte Implementierung der Schnittstelle für das Laden von Remoteschriftdateien zurückgegeben, die HTTP-Interaktionen zum Herunterladen von Schriftartdaten im Auftrag der App verarbeiten kann. Eine Verweis-URL oder zusätzliche Header können angegeben werden, wenn dies für den Schriftartdienst oder Dienste erforderlich ist, die die Quelle für die Schriftarten sind.    

> [!IMPORTANT]
> Sicherheitshinweis: Wenn versucht wird, eine Remoteschriftart abzurufen, besteht das Potenzial, dass ein Angreifer den vorgesehenen Server spooft, der aufgerufen wird. In diesem Fall werden die Ziel- und Verweis-URLs und Headerdetails dem Angreifer offengelegt. App-Entwickler sind für die Risikominderung verantwortlich. Es wird empfohlen, das HTTPS-Protokoll anstelle von HTTP zu verwenden. 

 

Ein einzelnes Remoteladeprogramm für Schriftartdateien kann für mehrere Schriftarten verwendet werden, obwohl verschiedene Ladefunktionen verwendet werden können, wenn Schriftarten von mehreren Diensten abgerufen werden, die unterschiedliche Anforderungen an Verweiser-URL oder zusätzliche Header haben.   
4. Registrieren Sie das Remoteladeprogramm für Schriftartdateien bei der Factory. 


```C++
 if (SUCCEEDED(hr)) 
 { 
     hr = pDWriteFactory->RegisterFontFileLoader(pRemoteFontFileLoader); 
 } 
```



Ab diesem Punkt ähneln die Schritte zum Erstellen des benutzerdefinierten Schriftartsatzes denen, die für bekannte lokale Schriftartdateien beschrieben werden, mit zwei wichtigen Ausnahmen. Zunächst wird das [**IDWriteFontFile-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) mithilfe der Schnittstelle für das Remote-Schriftartdateiladeprogramm anstelle der Factory erstellt. Zweitens kann die Analyze-Methode nicht verwendet werden, da die Schriftartdaten nicht lokal sind. Stattdessen muss die App wissen, ob es sich bei der Remoteschriftartdatei um eine OpenType-Schriftartauflistungsdatei handelt. Wenn ja, muss sie wissen, welche Schriftarten in der Sammlung sie verwenden wird, und den Index für jede. Daher sind die verbleibenden Schritte wie folgt.   
5. Verwenden Sie für jede Remoteschriftartdatei die Schnittstelle remote font file loader , um eine [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)zu erstellen, und geben Sie dabei die URL an, die für den Zugriff auf die Schriftartdatei erforderlich ist. 


```C++
 IDWriteFontFile* pFontFile; 
 hr = pRemoteFontFileLoader->CreateFontFileReferenceFromUrl( 
     pDWriteFactory, 
     /* baseUrl */ L"https://github.com/", 
     /* fontFileUrl */ L"winjs/winjs/blob/master/src/fonts/Symbols.ttf?raw=true", 
     &pFontFile 
 ); 
```



Beachten Sie, dass die vollständige URL im fontFileUrl-Parameter angegeben oder in Basis- und relative Teile aufgeteilt werden kann. Wenn eine Basis-URL angegeben wird, muss die Verkettung der BaseUrl- und fontFileUrl-Werte die vollständige URL bereitstellen. DirectWrite stellt kein zusätzliches Trennzeichen bereit.  

> [!IMPORTANT]
> Sicherheits-/Leistungshinweis: Wenn versucht wird, eine Remoteschriftart abzurufen, gibt es keine Garantie dafür, dass Windows eine Antwort vom Server erhalten. In einigen Fällen antwortet ein Server möglicherweise mit einem Dateifehler, der nicht gefunden wurde, auf eine ungültige relative URL, reagiert aber nicht mehr, wenn er mehrere ungültige Anforderungen empfängt. Wenn der Server nicht antwortet, tritt für Windows schließlich ein Time out auf, obwohl dies einige Minuten dauern kann, wenn mehrere Abrufe initiiert werden. Sie sollten alles tun, um sicherzustellen, dass URLs gültig sind, wenn Aufrufe erfolgen. 

 

Beachten Sie auch, dass die URL auf eine unformatierte OpenType-Schriftartdatei (TTF, OTF, TTC, PROTOKOLLDATEI) verweisen kann, aber sie kann auch auf Schriftarten in einer WOFF- oder WOFF2-Containerdatei verweisen. Wenn auf eine WOFF- oder WOFF2-Datei verwiesen wird, entpackt die DirectWrite Implementierung des Remoteladeprogramms für Schriftartdateien automatisch die Schriftartdaten aus der Containerdatei.   
6. Erstellen Sie für jeden Schriftartengesichtsindex in der zu verwendenden Remoteschriftartdatei einen [**IDWriteFontFaceReference.**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) 


```C++
 IDWriteFontFaceReference* pFontFaceReference; 
 hr = pDWriteFactory->CreateFontFaceReference(pFontFile, /* faceIndex */ 0, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);
```



  
7. Definieren Sie benutzerdefinierte Eigenschaften für die Schriftart, wie oben gezeigt.   
8. Fügen Sie wie oben gezeigt den Schriftartengesichtsverweis zusammen mit benutzerdefinierten Eigenschaften dem Schriftartensatz-Generator hinzu.   
9. Nachdem alle Schriftarten dem Schriftartensatz-Generator hinzugefügt wurden, erstellen Sie den Schriftartensatz wie oben gezeigt.   
10. Wenn die Remoteschriftarten nicht mehr verwendet werden, sollten Sie die Registrierung des Remoteschriftartdateiladers aufheben. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pRemoteFontFileLoader); 
```



  
</dl>

Sobald ein benutzerdefinierter Schriftartensatz mit benutzerdefinierten Remoteschriftarten erstellt wurde, enthält der Schriftartensatz Verweise und Informationseigenschaften für die Remoteschriftarten, aber die tatsächlichen Daten sind weiterhin remote. DirectWrite Unterstützung für Remoteschriftarten ermöglicht es, einen Schriftartengesichtsverweis im Schriftsatz zu verwalten und eine Schriftart für die Verwendung im Layout und Rendering auszuwählen, aber dass die tatsächlichen Daten erst heruntergeladen werden, wenn sie tatsächlich verwendet werden müssen, z. B. wenn das Textlayout ausgeführt wird.  

Eine App kann vorab vorgehen, indem sie anfordert, dass DirectWrite die Schriftartdaten herunterladen und dann auf die Bestätigung eines erfolgreichen Downloads warten, bevor eine Verarbeitung mit der Schriftart gestartet wird. Ein Netzwerkdownload impliziert jedoch eine gewisse Latenz mit unvorhersehbarer Dauer, und der Erfolg ist ebenfalls unsicher. Aus diesem Grund ist es in der Regel besser, einen anderen Ansatz zu verfolgen, sodass Layout und Rendering anfänglich mit alternativen oder Fallbackschriftarten durchgeführt werden können, die bereits lokal sind. Gleichzeitig wird der Download der gewünschten Remoteschriftart angefordert und die Ergebnisse aktualisiert, sobald die gewünschte Schriftart heruntergeladen wurde. 

Um anzufordern, dass die gesamte Schriftart heruntergeladen wird, bevor sie verwendet wird, kann die [**IDWriteFontFaceReference::EnqueueFontDownloadRequest-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuefontdownloadrequest) verwendet werden. Wenn die Schriftart sehr groß ist, kann nur ein Teil der Daten für die Verarbeitung bestimmter Zeichenfolgen benötigt werden. DirectWrite stellt zusätzliche Methoden bereit, mit denen Teile der Schriftartdaten angefordert werden können, die für bestimmte Inhalte benötigt werden, [**EnqueueCharacterDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuecharacterdownloadrequest) und [**EnqueueGlyphDownloadRequest.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueueglyphdownloadrequest)  

Angenommen, der Ansatz, der in der App verwendet werden soll, besteht darin, die Verarbeitung zunächst mit lokalen, alternativen oder Fallbackschriftarten zu ermöglichen. Die IDWriteFontFallback::[**MapCharacters-Methode**](idwritefontfallback-mapcharacters.md) kann verwendet werden, um lokale Fallbackschriftarten zu identifizieren. Außerdem wird automatisch eine Anforderung zum Herunterladen der bevorzugten Schriftart in die Quehnung eingerückt. Wenn [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) verwendet wird und ein Teil oder der gesamte Text im Layout mit einem Remoteschriftartverweis formatiert wird, verwendet DirectWrite automatisch die **MapCharacters-Methode,** um lokale Fallbackschriftarten abzurufen und eine Anforderung zum Herunterladen der Remoteschriftartdaten in die Schublade zu stellen. 

DirectWrite verwaltet eine Warteschlange zum Herunterladen von Schriftarten für jede Factory, und die Anforderungen, die mit den oben genannten Methoden ausgeführt werden, werden dieser Warteschlange hinzugefügt. Die Downloadwarteschlange für Schriftarten kann mithilfe der [**IDWriteFactory3::GetFontDownloadQueue-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getfontdownloadqueue) abgerufen werden. 

Wenn eine Downloadanforderung gestellt wird, die Schriftartdaten jedoch bereits lokal sind, führt dies zu einem No-Op-Ergebnis: Der Downloadwarteschlange wird nichts hinzugefügt. Eine App kann überprüfen, ob die Warteschlange leer ist oder ob Downloadanforderungen ausstehen, indem sie die [**IDWriteFontDownloadQueue::IsEmpty-Methode aufruft.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-isempty) 

Nachdem der Warteschlange Remoteschriftartenanforderungen hinzugefügt wurden, muss der Downloadvorgang initiiert werden. Wenn Remoteschriftarten in [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)verwendet werden, wird der Download automatisch initiiert, wenn die App **IDWriteTextLayout-Methoden aufruft,** die Layout- oder Renderingvorgänge erzwingen, z. B. die GetLineMetrics- oder Draw-Methoden. In anderen Szenarien muss die App den Download direkt initiieren, indem [**SIE IDWriteFontDownloadQueue::BeginDownload aufruft.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload)  

Wenn ein Download abgeschlossen ist, liegt es an der App, entsprechende Maßnahmen zu ergreifen– mit ausstehenden Vorgängen fortzufahren oder Vorgänge zu wiederholen, die anfänglich mit Fallbackschriftarten durchgeführt wurden. (Wenn das Textlayout DirectWrite verwendet wird, kann [**IDWriteTextLayout3::InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) verwendet werden, um die temporären Ergebnisse zu löschen, die mit Fallbackschriftarten berechnet wurden.) Damit die App benachrichtigt wird, wenn der Downloadvorgang abgeschlossen ist, und entsprechende Aktionen ausführen zu können, muss die App eine Implementierung der [**IDWriteFontDownloadListener-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) bereitstellen und diese an den BeginDownload-Aufruf übergeben. 

> [!IMPORTANT]
> Sicherheits-/Leistungshinweis: Wenn versucht wird, eine Remoteschriftart abzurufen, gibt es keine Garantie dafür, dass Windows eine Antwort vom Server erhalten. Wenn der Server nicht antwortet, tritt für Windows schließlich ein Time out auf. Dies kann jedoch einige Minuten dauern, wenn mehrere Remoteschriftarten abgerufen werden, aber ein Fehler aufgetreten ist. Der BeginDownload-Aufruf wird sofort zurückgegeben. Apps sollten die Benutzeroberfläche nicht blockieren, während darauf gewartet wird, dass [**IDWriteFontDownloadListener::D ownloadCompleted**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadlistener-downloadcompleted) aufgerufen wird. 

 

Beispielimplementierungen dieser Interaktionen mit der Warteschlange zum Herunterladen von Schriftarten DirectWrite und der [**IDWriteFontDownloadListener-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) finden Sie im [DirectWrite Beispiel für benutzerdefinierte Schriftartensätze](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)sowie im [DirectWrite Beispiel für herunterladbare Schriftarten.](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont) 

### <a name="creating-a-custom-font-set-using-font-data-loaded-into-memory"></a>Erstellen eines benutzerdefinierten Schriftartsatzes mit in den Arbeitsspeicher geladenen Schriftartdaten

So wie sich die Low-Level-Vorgänge zum Lesen von Daten aus einer Schriftartdatei für Dateien auf einem lokalen Datenträger und für Remotedateien im Web unterscheiden, gilt dies auch für Schriftartdaten, die in einen Speicherpuffer geladen werden. Im Windows 10 Creators Update [**idWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader)wurde eine neue Schnittstelle auf niedriger Ebene für die Verarbeitung von In-Memory-Schriftartdaten hinzugefügt. 

Wie bei einem Remoteladeprogramm für Schriftartdateien muss ein In-Memory-Schriftartdateiladeprogramm zuerst bei einer DirectWrite Factory registriert werden. Das Ladeprogramm muss von der App so lange aufbewahrt werden, wie die ihr zugeordneten Schriftarten verwendet werden. Sobald die Schriftarten nicht mehr verwendet werden und zu einem bestimmten Zeitpunkt, bevor die Factory zerstört wird, muss die Registrierung des Ladeprogramm aufgehoben werden. Dies kann im Destruktor für die Klasse erfolgen, die das Ladeprogrammobjekt besitzt. Diese Schritte werden unten gezeigt. 

Wenn die App über separate Informationen zu den durch die Daten dargestellten Schriftartflächen verfügt, kann sie einem Schriftartensatz-Generator mit angegebenen benutzerdefinierten Eigenschaften einzelne Schriftartengesichtsverweise hinzufügen. Da sich die Schriftartdaten jedoch im lokalen Speicher befinden, ist dies nicht erforderlich. DirectWrite können die Daten direkt lesen, um die Eigenschaftswerte abzuleiten. 

DirectWrite geht davon aus, dass die Schriftartdaten im Format raw, OpenType vorliegen und einer OpenType-Datei (.ttf, .otf, .ttc, .val) entsprechen, aber im Arbeitsspeicher und nicht auf dem Datenträger. Die Daten dürfen nicht im WOFF- oder WOFF2-Containerformat vorliegen. Die Daten können eine OpenType-Schriftartauflistung darstellen. Wenn keine benutzerdefinierten Eigenschaften verwendet werden, kann die [**IDWriteFontSetBuilder1::AddFontFile-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) verwendet werden, um alle Schriftartengesichter in den Daten in einem einzigen Aufruf hinzuzufügen. 

Ein wichtiger Aspekt für das In-Memory-Szenario ist die Lebensdauer der Daten. Wenn ein Zeiger auf den Puffer für DirectWrite ohne eindeutigen Hinweis darauf bereitgestellt wird, dass ein Besitzer vorhanden ist, erstellt DirectWrite eine Kopie der Daten in einen neuen Speicherpuffer, den er besitzt. Um das Kopieren von Daten und zusätzliche Speicherbelegung zu vermeiden, kann die App ein Datenbesitzerobjekt übergeben, das IUnknown implementiert und der besitzer des Speicherpuffers ist, der die Schriftartdaten enthält. Durch die Implementierung dieser Schnittstelle können DirectWrite zur Ref-Anzahl des Objekts hinzufügen und so die Lebensdauer der eigenen Daten sicherstellen. 

Die Methode zum Erstellen eines benutzerdefinierten Schriftartsatzes mithilfe von In-Memory-Schriftartdaten lautet wie folgt: dies erfordert die Windows 10 Creators Update. Dabei wird von einem von der App implementierten Datenbesitzerobjekt ausgegangen, das IUnknown implementiert und über Methoden verfügt, die einen Zeiger auf den Speicherpuffer und die Größe des Puffers zurückgeben. 

<dl> 1. Erstellen Sie wie oben gezeigt eine IDWriteFactory5-Schnittstelle.  
2.Erstellen Sie wie oben gezeigt eine [**IDWriteFontSetBuilder1-Schnittstelle.**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1)  
3. Verwenden Sie die Factory, um einen IDWriteInMemoryFontFileLoader abzurufen. 


```C++
 IDWriteInMemoryFontFileLoader* pInMemoryFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateInMemoryFontFileLoader(&pInMemoryFontFileLoader); 
}
```



Dadurch wird eine vom System bereitgestellte Implementierung der In-Memory-Schriftart-Dateiladeprogrammschnittstelle zurückgegeben.   
4. Registrieren Sie das In-Memory-Schriftartdateiladeprogramm bei der Factory. 


```C++
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->RegisterFontFileLoader(pInMemoryFontFileLoader); 
}
```



   
5. Verwenden Sie für jede In-Memory-Schriftartdatei das In-Memory-Schriftartdateiladeprogramm, um eine [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)zu erstellen. 


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



   
6. Fügen Sie das [**IDWriteFontFile-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) wie oben gezeigt mithilfe der [**AddFontFile-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) dem Schriftartensatz-Generator hinzu.  Wenn eine Notwendigkeit besteht, kann die App stattdessen einzelne [**IDWriteFontFaceReference-Objekte**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) basierend auf **idWriteFontFile** erstellen, optional benutzerdefinierte Eigenschaften für jeden Schriftartengesichtsverweis definieren und dann den Schriftartengesichtsverweis mit benutzerdefinierten Eigenschaften wie oben gezeigt mithilfe der [**AddFontFaceReference-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) dem Schriftartsatz hinzufügen.   
7. Nachdem alle Schriftarten dem Schriftartensatz-Generator hinzugefügt wurden, erstellen Sie den benutzerdefinierten Schriftartensatz, wie oben gezeigt.   
8. Wenn die In-Memory-Schriftarten nicht mehr verwendet werden, sollten Sie die Registrierung des In-Memory-Schriftartdateiladers aufheben. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pInMemoryFontFileLoader);
```



  
</dl>

 

## <a name="advanced-scenarios"></a>Erweiterte Szenarios

Einige Apps haben möglicherweise spezielle Anforderungen, die eine erweiterte Verarbeitung erfordern, als oben beschrieben. 

### <a name="combining-font-sets"></a>Kombinieren von Schriftartsätzen

Einige Apps müssen möglicherweise einen Schriftartsatz erstellen, der eine Kombination von Elementen aus anderen Schriftartsätzen umfasst. Beispielsweise kann eine App einen Schriftartensatz erstellen, der alle auf dem System installierten Schriftarten mit einer Auswahl benutzerdefinierter Schriftarten kombiniert, oder installierte Schriftarten, die bestimmte Kriterien erfüllen, mit anderen Schriftarten kombinieren. DirectWrite verfügt über APIs zur Unterstützung der Bearbeitung und Kombination von Schriftartsätzen. 

Um zwei oder mehr Schriftartsätze zu kombinieren, fügt die [**IDWriteFontSetBuilder::AddFontSet-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontset) alle Schriftarten in einem angegebenen Schriftartsatz hinzu, die einem Schriftartensatz-Generator in einem einzigen Aufruf hinzugefügt werden sollen. Wenn im neuen Schriftartensatz nur bestimmte Schriftarten aus einem vorhandenen Schriftartensatz gewünscht werden, kann die [**IDWriteFontSet::GetMatchingFonts-Methode**](idwritefontset-getmatchingfonts-overload.md) verwendet werden, um ein neues Schriftartensatzobjekt abzuleiten, das gefiltert wurde, sodass nur Schriftarten enthalten sind, die den angegebenen Eigenschaften entsprechen. Diese Methoden bieten eine einfache Möglichkeit, einen benutzerdefinierten Schriftartensatz zu erstellen, der Schriftarten aus zwei oder mehr vorhandenen Schriftartsätzen kombiniert. 

### <a name="using-local-woff-or-woff2-font-data"></a>Verwenden lokaler WOFF- oder WOFF2-Schriftartdaten

Wenn eine App über Schriftartdateien im lokalen Dateisystem oder in einem Speicherpuffer verfügt, sie jedoch die WOFF- oder WOFF2-Containerformate verwendet, stellt DirectWrite (Windows 10 Creator Update oder höher) eine Methode zum Entpacken des Containerformats [**IDWriteFactory5::UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile)bereit, die einen [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)zurückgibt. 

Die App benötigt jedoch eine Möglichkeit, [**den IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) in ein Schriftartdateiladeprogrammobjekt abzurufen. Eine Möglichkeit besteht darin, eine benutzerdefinierte [**IDWriteFontFileLoader-Implementierung**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) zu erstellen, die den Stream umschließt. Wie bei anderen Ladeprogramm für Schriftartdateien muss diese vor der Verwendung registriert und die Registrierung aufgehoben werden, bevor die Factory den Gültigkeitsbereich überspringt.  

Wenn das benutzerdefinierte Ladeprogramm auch mit unformatierten (nicht gepackten) Schriftartdateien verwendet wird, muss die App auch eine benutzerdefinierte Implementierung der [**IDWriteFontFileStream-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) für die Verarbeitung dieser Dateien bereitstellen. Es gibt jedoch einfachere Möglichkeiten, die oben beschriebenen APIs für die Verarbeitung von Rohschriftartdateien zu verwenden. Die Notwendigkeit einer benutzerdefinierten Streamimplementierungen kann vermieden werden, indem separate Codepfade für gepackte Schriftartdateien im Vergleich zu unformatierten Schriftartdateien verwendet werden. 

Nachdem ein benutzerdefiniertes Schriftartdateiladeprogramm-Objekt erstellt wurde, werden die gepackten Schriftartdateidaten dem Ladeprogramm auf app-spezifische Weise hinzugefügt. Das Ladeprogramm kann mehrere Schriftartdateien verarbeiten, von denen jede mithilfe eines app-definierten Schlüssels identifiziert wird, der für DirectWrite nicht transparent ist. Nachdem dem Ladeprogramm eine gepackte Schriftartdatei hinzugefügt wurde, wird die [**IDWriteFactory::CreateCustomFontFileReference-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) verwendet, um eine [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) basierend auf diesem Ladeprogramm für die durch einen bestimmten Schlüssel identifizierten Schriftartdaten abzurufen.  

Das eigentliche Entpacken der Schriftartdaten kann beim Hinzufügen von Schriftarten zum Ladeprogramm erfolgen, kann aber auch in der [**IDWriteFontFileLoader::CreateStreamFromKey-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) verarbeitet werden, die DirectWrite aufruft, wenn die Schriftartdaten zum ersten Mal gelesen werden müssen. 

Nachdem ein IDWriteFontFile-Objekt erstellt wurde, werden die verbleibenden Schritte zum Hinzufügen der Schriftarten zu einem benutzerdefinierten Schriftartensatz wie oben beschrieben ausgeführt. 

Eine Implementierung mit diesem Ansatz wird im [DirectWrite Beispiel für benutzerdefinierte Schriftartsätze](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)veranschaulicht. 

### <a name="using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation"></a>Verwenden DirectWrite Remoteschriftartmechanismen mit benutzerdefinierter Netzwerkimplementierungen auf niedriger Ebene

Die DirectWrite Mechanismen für die Behandlung von Remoteschriftarten können in Mechanismen auf höherer Ebene unterteilt werden– mit Schriftartsätzen, die Schriftartenreferenzen für Remoteschriftarten enthalten, die Lokalität der Schriftartdaten überprüfen und die Warteschlange für Downloadanforderungen für Schriftarten verwalten – und die Mechanismen auf niedrigerer Ebene, die den tatsächlichen Download verarbeiten. Einige Apps möchten möglicherweise die Remoteschriftartmechanismen auf höherer Ebene verwenden, erfordern aber auch benutzerdefinierte Netzwerkinteraktionen, z. B. die Kommunikation mit Servern mit anderen Protokollen als HTTP. 

In diesem Fall muss eine App eine benutzerdefinierte Implementierung der [**IDWriteRemoteFontFileLoader-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) erstellen, die auf die erforderliche Weise mit anderen Schnittstellen auf niedrigerer Ebene interagiert. Die App muss auch benutzerdefinierte Implementierungen dieser Schnittstellen auf niedrigerer Ebene bereitstellen: [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream)und [**IDWriteAsyncResult.**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) Diese drei Schnittstellen verfügen über Rückrufmethoden, die DirectWrite während download-Vorgängen aufruft. 

Wenn [**IDWriteFontDownloadQueue::BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload) aufgerufen wird, führt DirectWrite Abfragen an das Remoteschriftartdateiladeprogramm zur Lokalität der Daten durch und fordert den Remotestream an. Wenn die Daten nicht lokal sind, wird die BeginDownload-Methode des Streams aufrufen. Die Streamimplementierung sollte für diesen Aufruf nicht blockieren, sondern sollte sofort zurückgeben und ein [**IDWriteAsyncResult-Objekt**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) zurückgeben, das das Wait-Handle angibt, das DirectWrite verwendet, um auf den asynchronen Downloadvorgang zu warten. Die benutzerdefinierte Streamimplementierung ist für die Verarbeitung der Remotekommunikation verantwortlich. Wenn das Abschlussereignis aufgetreten ist, wird DirectWrite [**IDWriteAsyncResult::GetResult**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteasyncresult-getresult) aufrufen, um das Ergebnis des Vorgangs zu bestimmen. Wenn das Ergebnis erfolgreich ist, wird erwartet, dass nachfolgende ReadFragment-Aufrufe des Streams für die heruntergeladenen Bereiche erfolgreich sind. 

> [!IMPORTANT]
> Sicherheits-/Leistungshinweis: Wenn versucht wird, eine Remoteschriftart zu abrufen, besteht im Allgemeinen die Möglichkeit, dass ein Angreifer den beabsichtigten Server, der aufgerufen wird, spooft, oder dass der Server möglicherweise nicht reagiert. Wenn Sie benutzerdefinierte Netzwerkinteraktionen implementieren, haben Sie möglicherweise mehr Kontrolle über die Entschärfungen als beim Umgang mit Servern von Drittanbietern. Es liegt jedoch an Ihnen, geeignete Gegenmaßnahmen zu erwägen, um die Offenlegung von Informationen oder Denial-of-Service-Angriffen zu vermeiden. Sichere Protokolle wie HTTPS werden empfohlen. Außerdem sollten Sie ein Timeout erstellen, damit das Ereignishand handle, das an DirectWrite zurückgegeben wird, schließlich festgelegt wird. 

 

### <a name="supporting-scenarios-on-earlier-windows-versions"></a>Unterstützende Szenarien für frühere Windows Versionen

Die beschriebenen Szenarien können in DirectWrite in früheren Versionen von Windows unterstützt werden, erfordern jedoch eine wesentlich benutzerdefiniertere Implementierung durch die App mithilfe der eingeschränkteren APIs, die vor Windows 10. Weitere Informationen finden Sie unter [Benutzerdefinierte Schriftartsammlungen (Windows 7/8).](custom-font-collections.md)

 

 