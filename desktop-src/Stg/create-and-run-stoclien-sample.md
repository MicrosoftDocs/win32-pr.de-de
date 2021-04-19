---
title: Erstellen und Ausführen von "stoclien Sample"
description: Stoclien arbeitet in Zusammenarbeit mit einem copaper-Objekt in einem com-Server zusammen, um eine permanente Speicherung von Zeichnungen in com-Verbund Dateien zu erzielen.
ms.assetid: bf622104-10dd-4649-88f0-e2bfb15289b1
keywords:
- Erstellen und Ausführen von "stoclien Sample"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f00274293c05e21e660dc8e9448ca95946cab8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342048"
---
# <a name="create-and-run-stoclien-sample"></a>Erstellen und Ausführen von "stoclien Sample"

**Stoclien** arbeitet in Zusammenarbeit mit einem copaper-Objekt in einem com-Server zusammen, um eine permanente Speicherung von Zeichnungen in com-Verbund Dateien zu erzielen. Weitere Informationen zur copaper-Verwendung von Streams in der Verbund Datei, die für copaper von **stoclien** bereitgestellt wird, finden Sie unter [**stoservice**](structured-storage-server-sample--stoserve-.md) Sample and STOSERVE.HTM. Die Erstellung des copaper und seine iPaper-Schnittstelle werden ebenfalls im **stoservice** -Beispiel behandelt.

## <a name="code-tour"></a>Codetour

Die wichtigsten Themen, die in dieser codetour behandelt werden, sind:

-   Wie **cguipaper** das GUI-Verhalten von **stoclien** Electronic Drawing Paper kapselt
-   Erfassen und anzeigen interaktiver Zeichnungs Aktivitäten durch **stoclien**
-   Verwendung von copaper durch das **cguipaper** -Objekt zum Aufzeichnen von Zeichnungsdaten
-   Verwendung einer ipapersink-Verbindung beim Neuzeichnen
-   Verwendung der strukturierten Speicherung in Verbund Dateien durch cpapfile-Methoden zum **Laden** und **Speichern**

Da die **cguiball** -Klasse, die in den Beispielen Freclien und in der-Klasse verwendet wird, das Verhalten eines Sprung-Balls gekapselt hat, verwendet **stoclien** eine **cguipaper** C++-Klasse, um das Daten-und GUI-Verhalten von elektronischen Zeichnungs Papier zu kapseln.

In der folgenden Tabelle sind die für das **stoclien** -Beispiel relevanten Dateien aufgeführt.



| Dateien        | BESCHREIBUNG                                                                                                                      |
|--------------|----------------------------------------------------------------------------------------------------------------------------------|
| STOCLIEN.TXT | Kurze Beispiel Beschreibung.                                                                                                        |
| Makefile     | Das generische Makefile zum Entwickeln des Code Beispiels.                                                                               |
| Stoclien. Micha   | Die Includedatei für die **stoclien** -Anwendung. Enthält Klassen Deklarationen, Funktionsprototypen und Ressourcen Bezeichner.   |
| Stoclien. CPP | Die Haupt Implementierungs Datei für STOCLIEN.EXE. Hat die Implementierung von winmain und CMainWindow sowie die Haupt Menü Verteilung. |
| Stoclien. RC  | Die Anwendungs Ressourcen-Definitionsdatei.                                                                                        |
| Stoclien. ICO | Die Anwendungssymbol Ressource.                                                                                                   |
| Stoclien. PAP | Eine standardmäßige Papier Zeichnungs Datei für die Anwendung.                                                                                |
| Stift. CUR   | Ein Stift Bild für den Client Fenster Cursor.                                                                                     |
| Körper. Micha       | Die Klassen Deklaration für die copapersink-com-Objektklasse.                                                                      |
| Körper. CPP     | Implementierungs Datei für die copapersink-com-Objektklasse.                                                                        |
| Papfile. Micha    | Die Klassen Deklaration für die **cpapfile** C++-Klasse.                                                                            |
| Papfile. CPP  | Implementierungs Datei für die **cpapfile** C++-Klasse.                                                                              |
| Guipaper. Micha   | Die Klassen Deklaration für die **cguipaper** C++-Klasse.                                                                           |
| Guipaper. CPP | Implementierungs Datei für die **cguipaper** C++-Klasse.                                                                             |
| Stoclien. DSP | Microsoft Visual Studio Projektdatei.                                                                                            |



 

## <a name="compound-files"></a>Verbunddateien

**Stoclien** basiert auf copaper, um Zeichnungsdaten aufzuzeichnen. Außerdem wird copaper zum Speichern der Daten in einer Verbund Datei unterstützt. Bei einer typischen Arbeitsabteilung zwischen com-Client und Server teilt **stoclien** jedoch einen Teil der Verantwortung für den Dateispeicher. Diese Arbeitsabteilung ist in com-Anwendungen wichtig, bei denen der Client ein Container ist und der Server ein eingebettetes Objekt ist. Bei dieser Anordnung ist der Client dafür verantwortlich, eine strukturierte Speicherdatei zu erstellen oder zu öffnen, während das Server Objekt dafür verantwortlich ist, diesen Speicher für seine eigenen Datenspeicher Zwecke zu verwenden. Dies kann dazu führen, dass das Server Objekt substorages im Speicher erstellt, das ihm zugewiesen ist. Dies umfasst in der Regel das Server Objekt, das Streamobjekte im Speicher erstellt. Die Verwendung von speicherstreams durch copaper wird im **stoclien** -Beispiel ausführlich erläutert.

Die [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle wird sowohl vom Client als auch vom Server Objekt zum Ausführen von Datei Vorgängen verwendet. Die Implementierung der Verbund Dateien der strukturierten Speicherarchitektur wird verwendet. Standard Dienstfunktionen werden für Vorgänge in Verbund Dateien verwendet. Beispielsweise erstellt die [**stgkreatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) -Funktion anfänglich eine Verbund Datei und gibt einen **IStorage** -Zeiger zurück, der zum Bearbeiten der Datei verwendet werden kann. Diese bestimmte Funktion wird in **stoclien** aufgerufen. Die von ihr abzurufende **IStorage** -Schnittstelle wird als Parameter an copaper übergeben, um Sie zu verwenden. Das copaper-Objekt erstellt oder öffnet keine Verbund Dateien eigenständig: es verwendet die **IStorage** -und [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Schnittstellen, um in Verbund Dateien zu arbeiten, die ihm übergeben werden.

Diese [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -und [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Schnittstellen sind nicht in **stoclien** oder **stoservice** implementiert. Sie werden innerhalb der com-Bibliotheken implementiert. Wenn ein Zeiger auf eine dieser Schnittstellen abgerufen wird, werden die zugehörigen Methoden im Wesentlichen als eine Gruppe von Diensten für eine Verbund Datei verwendet.

 

 




