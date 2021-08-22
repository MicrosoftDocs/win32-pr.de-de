---
title: Erstellen und Ausführen des StoClien-Beispiels
description: StoClien arbeitet in Zusammenarbeit mit einem COPaper-Objekt auf einem COM-Server, um eine dauerhafte Speicherung von Zeichnungen in COM-Verbunddateien zu erreichen.
ms.assetid: bf622104-10dd-4649-88f0-e2bfb15289b1
keywords:
- Erstellen und Ausführen des StoClien-Beispiels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3d9526e81fc3fb2d6a0cfb03e8943ccf68688096588122da87861d8c88e531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663460"
---
# <a name="create-and-run-stoclien-sample"></a>Erstellen und Ausführen des StoClien-Beispiels

**StoClien arbeitet** in Zusammenarbeit mit einem COPaper-Objekt auf einem COM-Server, um eine dauerhafte Speicherung von Zeichnungen in COM-Verbunddateien zu erreichen. Weitere Informationen zur Verwendung von Streams durch COPaper in der Verbunddatei, die von **StoClien** für COPaper bereitgestellt wird, finden Sie unter [**StoServe-Beispiel**](structured-storage-server-sample--stoserve-.md) und STOSERVE.HTM. Die Konstruktion von COPaper und die IPaper-Schnittstelle werden auch im **StoServe-Beispiel** behandelt.

## <a name="code-tour"></a>Code Tour

Die wichtigsten Themen, die in dieser Code tour behandelt werden, sind:

-   Wie **CGuiPaper das** GUI-Verhalten des elektronischen Zeichnungsdokuments von **StoClien** kapselt
-   Erfassen und Anzeigen interaktiver Zeichnungsaktivitäten durch **StoClien**
-   Verwendung von **COPaper durch das CGuiPaper-Objekt** zum Aufzeichnen von Zeichnungsdaten
-   Verwendung einer IPaperSink-Verbindung beim Neupainting
-   Verwenden des strukturierten Speichers in Verbunddateien durch die Methoden CPapFile **Load** und **Save**

Da die **CGuiBall-Klasse,** die in den FRECLIEN- und CONCLIEN-Beispielen verwendet wird, das Verhalten einer Springkugel gekapselt hat, verwendet **StoClien** eine **CGuiPaper-C++-Klasse,** um die Daten und das GUI-Verhalten des elektronischen Zeichnungsdokuments zu kapseln.

In der folgenden Tabelle sind die Dateien aufgeführt, die für das **StoClien-Beispiel** relevant sind.



| Files        | Beschreibung                                                                                                                      |
|--------------|----------------------------------------------------------------------------------------------------------------------------------|
| STOCLIEN.TXT | Kurze Beispielbeschreibung.                                                                                                        |
| Makefile     | Das generische Makefile zum Erstellen des Codebeispiels.                                                                               |
| STOCLIEN. H   | Die Includedatei für die **StoClien-Anwendung.** Enthält Klassendeklarationen, Funktionsprototypen und Ressourcenbezeichner.   |
| STOCLIEN. Cpp | Die Hauptimplementierungsdatei für STOCLIEN.EXE. Verfügt über die WinMain- und CMainWindow-Implementierung sowie die Hauptmenü-Dispatching. |
| STOCLIEN. Rc  | Die Definitionsdatei der Anwendungsressource.                                                                                        |
| STOCLIEN. Ico | Die Anwendungssymbolressource.                                                                                                   |
| STOCLIEN. Pap | Eine Standardmäßige Papierzeichnungsdatei für die Anwendung.                                                                                |
| Bleistift. Cur   | Ein Stiftbild für den Clientfenstercursor.                                                                                     |
| Waschbecken. H       | Die Klassendeklaration für die COM-Objektklasse COPaperSink.                                                                      |
| Waschbecken. Cpp     | Implementierungsdatei für die COM-Objektklasse COPaperSink.                                                                        |
| PAPFILE. H    | Die Klassendeklaration für die **C++-Klasse CPapFile.**                                                                            |
| PAPFILE. Cpp  | Implementierungsdatei für die **C++-Klasse CPapFile.**                                                                              |
| GUIPAPER. H   | Die Klassendeklaration für die **CGuiPaper-C++-Klasse.**                                                                           |
| GUIPAPER. Cpp | Implementierungsdatei für die **C++-Klasse "CGuiPaper".**                                                                             |
| STOCLIEN. Dsp | Microsoft Visual Studio Project Datei.                                                                                            |



 

## <a name="compound-files"></a>Verbunddateien

**StoClien nutzt** COPaper zum Aufzeichnen von Zeichnungsdaten. Außerdem wird COPaper verwendet, um die Daten in einer Verbunddatei zu speichern. In einer typischen Arbeitsteilung zwischen COM-Client und -Server ist **StoClien** jedoch teil der Verantwortung für die Dateispeicherung. Diese Arbeitsteilung ist in COM-Anwendungen wichtig, bei denen der Client ein Container und der Server ein eingebettetes Objekt ist. Bei dieser Anordnung ist der Client für das Erstellen oder Öffnen einer strukturierten Speicherdatei verantwortlich, während das Serverobjekt für die Verwendung dieses Speichers für seine eigenen Datenspeicherzwecke verantwortlich ist. Dies kann dazu gehören, dass das Serverobjekt Unterspeicher in dem Speicher erstellt, der ihm gegeben ist. In der Regel wird das Serverobjekt zum Erstellen von Streamobjekten im Speicher verwendet. Die Verwendung von Speicherdatenströmen durch COPaper ist im **StoClien-Beispiel** ausführlich.

Die [**IStorage-Schnittstelle**](/windows/desktop/api/Objidl/nn-objidl-istorage) wird sowohl vom Client- als auch vom Serverobjekt zum Ausführen von Dateivorgängen verwendet. Die Verbunddateienimplementierung der Structured Storage-Architektur wird verwendet. Standarddienstfunktionen werden für Vorgänge für Verbunddateien verwendet. Beispielsweise erstellt die [**StgCreateDocfile-Funktion**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) anfänglich eine Verbunddatei und übergibt einen **IStorage-Zeiger** zurück, der zum Bearbeiten der Datei verwendet werden kann. Diese spezielle Funktion wird in **StoClien aufgerufen.** Die **von ihm erhaltene IStorage-Schnittstelle** wird zur Verwendung als Parameter an COPaper übergeben. Das COPaper-Objekt erstellt oder öffnet verbundorientierte Dateien nicht selbst: Es verwendet die **IStorage-** und [**IStream-Schnittstellen,**](/windows/desktop/api/Objidl/nn-objidl-istream) um in Verbunddateien zu arbeiten, die ihm gegeben sind.

Diese [**IStorage-**](/windows/desktop/api/Objidl/nn-objidl-istorage) und [**IStream-Schnittstellen**](/windows/desktop/api/Objidl/nn-objidl-istream) werden nicht in **StoClien oder** **StoServe implementiert.** Sie werden in den COM-Bibliotheken implementiert. Wenn ein Zeiger auf eine dieser Schnittstellen erhalten wird, werden ihre Methoden im Wesentlichen als Gruppe von Diensten verwendet, um eine Verbunddatei zu verwenden.

 

 




