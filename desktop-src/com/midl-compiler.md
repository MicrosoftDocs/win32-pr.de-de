---
title: Mittlerer l-Compiler
description: Mittlerer l-Compiler
ms.assetid: ce3d40b7-49fd-4689-9100-fdbad4f0c557
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fa57131e31e9c6273270a771f9ba862d73bc142
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730633"
---
# <a name="midl-compiler"></a>Mittlerer l-Compiler

Der mittlerer l-Compiler verarbeitet eine IDL-Datei, um eine Typbibliothek und Ausgabedateien zu generieren. Der Typ der vom Mittel l-Compiler generierten Ausgabedateien hängt von den Attributen ab, die in der Schnittstellen Attribut Liste der IDL-Datei angegeben sind.

Wenn die Attribut Liste das \[ [**Object**](/windows/desktop/Midl/object) - \] Schlüsselwort enthält, generiert der Mittell-Compiler COM-Schnittstellen Ausgabedateien: eine Schnittstellen Proxy Datei, eine Schnittstellen Header Datei und eine Globally Unique Identifier-Datei (GUID) für die Schnittstelle. Wenn die IDL-Datei eine [**Library**](/windows/desktop/Midl/library) -Anweisung enthält, generiert "Mittel l" eine Typbibliotheks Datei mit der Dateinamenerweiterung ". tlb". Wenn in der IDL-Datei Schnittstellen vorhanden sind, die nicht über das \[ **Object** \] -Schlüsselwort verfügen und nicht in eine **Library** -Anweisung eingeschlossen sind, generiert der-Mittelwert Compiler Schnittstellen Ausgabedateien, die für Remote Prozedur Aufrufe (RPCs) geeignet sind: eine Client-Stub-Datei, eine Server-Stub-Datei und eine Header Datei. Weitere Informationen finden Sie in den Themen [Schnittstellendefinitionen und Typbibliotheken](/windows/desktop/Midl/interface-definitions-and-type-libraries) und [Erstellen einer Typbibliothek mit mittlerer l](/windows/desktop/Midl/generating-a-type-library-with-midl-2).

So generieren Sie eine Typbibliothek und Ausgabedateien aus einer IDL-Datei:

-   Führen Sie an der Eingabeaufforderung Folgendes aus:

     *Dateiname* für mittlere

    wobei *filename* der Name der IDL-Datei ist.

Der mittlerer l-Compiler unterstützt auch mehrere optionale Parameter. Eine vollständige Liste finden Sie unter "mittlere Command-Line Referenz" in der Visual C++-Dokumentation, oder führen Sie die folgende Befehlszeile aus:

**Mittel l/?**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft Interface Definition Language](/windows/desktop/Midl/midl-start-page)
</dt> <dt>

[Übersetzen in C++](translating-to-c--.md)
</dt> </dl>

 

 