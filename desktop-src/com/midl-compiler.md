---
title: MIDL-Compiler
description: MIDL-Compiler
ms.assetid: ce3d40b7-49fd-4689-9100-fdbad4f0c557
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db4afbbe8c7a82f4335855b40e578fe2eea046fa4c7f0560e3e297b559a67ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736429"
---
# <a name="midl-compiler"></a>MIDL-Compiler

Der MIDL-Compiler verarbeitet eine IDL-Datei, um eine Typbibliothek und Ausgabedateien zu generieren. Der Typ der vom MIDL-Compiler generierten Ausgabedateien hängt von den Attributen ab, die in der Schnittstellenattributliste der IDL-Datei angegeben sind.

Wenn die Attributliste das Object-Schlüsselwort enthält, generiert der MIDL-Compiler COM-Schnittstellenausgabedateien: eine Schnittstellenproxydatei, eine Schnittstellenheaderdatei und eine \[ [](/windows/desktop/Midl/object) \] GUID-Datei (Globally Unique Identifier) für die Schnittstelle. Wenn die IDL-Datei eine [**Bibliotheks-Anweisung**](/windows/desktop/Midl/library) enthält, generiert MIDL eine Typbibliotheksdatei mit der Dateierweiterung TLB. Wenn schnittstellen in der IDL-Datei enthalten sind, die nicht über das Schlüsselwort object verfügen und nicht in eine Bibliotheks-Anweisung eingeschlossen sind, generiert der MIDL-Compiler Schnittstellenausgabedateien, die für Remoteprozeduraufrufe (RPCs) geeignet sind: eine Clientstubdatei, eine Serverstubdatei und eine \[  \] Headerdatei.  Weitere Informationen finden Sie in den Themen [Schnittstellendefinitionen und Typbibliotheken](/windows/desktop/Midl/interface-definitions-and-type-libraries) und [Generieren einer Typbibliothek mit MIDL.](/windows/desktop/Midl/generating-a-type-library-with-midl-2)

So generieren Sie eine Typbibliothek und Ausgabedateien aus einer IDL-Datei:

-   Führen Sie an der Eingabeaufforderung aus.

    **midl** *filename*

    wobei *filename* der Name der IDL-Datei ist.

Der MIDL-Compiler unterstützt auch mehrere optionale Parameter. Eine vollständige Liste finden Sie unter "MIDL Command-Line Reference" in der Visual C++dokumentation, oder führen Sie die folgende Befehlszeile aus:

**midl /?**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft Interface Definition Language](/windows/desktop/Midl/midl-start-page)
</dt> <dt>

[Übersetzen in C++](translating-to-c--.md)
</dt> </dl>

 

 