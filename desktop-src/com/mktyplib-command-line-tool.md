---
title: MkTypLib-Command-Line Tool
description: MkTypLib ist eine Befehlszeilen Anwendung, die eine IDL-Datei verarbeitet, um eine Typbibliothek zu entwickeln. Sie kann auch verwendet werden, um eine C-oder C++-Header Datei zu generieren.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc392351327124777c2d52d0bbe0653853dcb52
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730640"
---
# <a name="mktyplib-command-line-tool"></a>MkTypLib-Command-Line Tool

\[Das Mktyplib.exe Tool ist veraltet. Verwenden Sie stattdessen den Mittel l-Compiler. Wenn Sie Abwärtskompatibilität mit alten Automatisierungs Programmen benötigen, verwenden Sie den mittlerer l-Compiler mit der **/mktyplib203** -Option.\]

MkTypLib ist eine Befehlszeilen Anwendung, die eine IDL-Datei verarbeitet, um eine Typbibliothek zu entwickeln. Sie kann auch verwendet werden, um eine C-oder C++-Header Datei zu generieren.

So generieren Sie eine Typbibliothek aus einer ODL-Datei:

-   Führen Sie an der Eingabeaufforderung den folgenden Befehl aus:

    **mktyplibs * * * Dateiname*

    wobei *filename* der Name der ODL-Datei ist.

MkTypLib unterstützt auch mehrere optionale Parameter. Um eine komplette Liste zu erhalten, führen Sie die folgende Befehlszeile aus:

**MkTypLib/?**

Da MkTypLib eine veraltete Anwendung ist, kann Sie keine IDL-Dateien oder-Dateien mit Schnittstellen analysieren, die außerhalb einer [**Library**](/windows/desktop/Midl/library) -Anweisung definiert sind. Weitere Informationen finden Sie [unter Unterschiede zwischen mittlerer l und MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in C++](translating-to-c--.md)
</dt> </dl>

 

 