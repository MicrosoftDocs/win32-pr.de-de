---
title: MkTypLib Command-Line Tool
description: MkTypLib ist eine Befehlszeilenanwendung, die eine IDL-Datei verarbeitet, um eine Typbibliothek zu erstellen. Sie kann auch verwendet werden, um eine C- oder C++-Headerdatei zu generieren.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b712ed8220dd609dd3ba189bdac6b5ee11d2805f26ff5a1f146c20f17c1f8ab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047938"
---
# <a name="mktyplib-command-line-tool"></a>MkTypLib Command-Line Tool

\[Das Mktyplib.exe Tool ist veraltet. Verwenden Sie stattdessen den MIDL-Compiler. Wenn Sie Abwärtskompatibilität mit alten Automation-Programmen benötigen, verwenden Sie den MIDL-Compiler mit der Option **/mktyplib203.**\]

MkTypLib ist eine Befehlszeilenanwendung, die eine IDL-Datei verarbeitet, um eine Typbibliothek zu erstellen. Sie kann auch verwendet werden, um eine C- oder C++-Headerdatei zu generieren.

So generieren Sie eine Typbibliothek aus einer ODL-Datei:

-   Führen Sie an der Eingabeaufforderung den folgenden Befehl aus:

    **mktyplibÂ **_Dateiname_

    dabei ist *filename* der Name der ODL-Datei.

MkTypLib unterstützt auch mehrere optionale Parameter. Führen Sie die folgende Befehlszeile aus, um eine vollständige Liste anzuzeigen:

**mktyplib /?**

Da MkTypLib eine veraltete Anwendung ist, können keine IDL-Dateien oder -Dateien mit Schnittstellen analysiert werden, die außerhalb einer [**Bibliotheks-Anweisung**](/windows/desktop/Midl/library) definiert sind. Weitere Informationen finden Sie unter [Unterschiede zwischen MIDL und MkTypLib.](/windows/desktop/Midl/differences-between-midl-and-mktyplib)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in C++](translating-to-c--.md)
</dt> </dl>

 

 