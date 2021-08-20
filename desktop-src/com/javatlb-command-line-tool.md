---
title: JavaTLB Command-Line Tool
description: JavaTLB Command-Line Tool
ms.assetid: b46d7bcc-ccd9-4242-9b19-f398d2cb8f91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ade0a20a1c41310422c08310f2d0534914993d79909f51990c48aa04df0a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918624"
---
# <a name="javatlb-command-line-tool"></a>JavaTLB Command-Line Tool

JavaTLB ist eine Komponente von Visual J++ 5.0. JavaTLB ist eine Befehlszeilenanwendung, die Klassendateien für ein COM-Objekt generiert. Methoden, die Datentypen enthalten, die in Java nicht genau und sicher dargestellt werden können, werden nicht konvertiert.

Im Gegensatz zum [Java-Typbibliotheks-Assistenten](java-type-library-wizard.md)generiert JavaTLB keine Zusammenfassungsdatei, die die Java-Typbibliotheksinformationen enthält.

Führen Sie an der Eingabeaufforderung Folgendes aus, um Java-Klassendateien für ein einzelnes COM-Objekt zu generieren:

**javatlb** *filename*

dabei ist *filename* der Name der Datei, die die Typbibliothek enthält. Diese Datei kann eine der folgenden Dateinamenerweiterungen aufweisen: TLB, OLB, OCX, .dll oder .exe.

Führen Sie an der Eingabeaufforderung Folgendes aus, um Java-Klassendateien für mehrere COM-Objekte zu generieren:

**javatlb @**_TextFile_

Dabei ist *TextFile* der Name einer Textdatei, die eine Liste der Dateien enthält, die die Typbibliotheken des COM-Objekts enthalten.

> [!Note]  
> In Visual J++ 6.0 wird das JavaTLB-Befehlszeilentool durch das [JActiveX-Tool](jactivex-command-line-tool.md)ersetzt. Weitere Informationen finden Sie in der Dokumentation zu Visual J++ 6.0.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in Java](translating-to-java.md)
</dt> </dl>

 

 




