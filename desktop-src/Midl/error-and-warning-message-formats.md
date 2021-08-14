---
title: Fehler- und Warnmeldungsformate
description: Liste der MIDL-Fehlermeldungs- und Warnmeldungsformate.
ms.assetid: 8eb0f46f-e494-430a-8bb4-b8a21524b62e
keywords:
- Fehler MIDL , Nachrichtenformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cbe6e32109bbe8e4d40b7715c6463e16cd0c27fc77492f5044ce32a7fe57436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384416"
---
# <a name="error-and-warning-message-formats"></a>Fehler- und Warnmeldungsformate

Befehlszeilenfehler werden im folgenden Format angezeigt:

``` syntax
Command line error : MIDLnnnn: <error text> 
[<additional error information>]
```

Das zusätzliche Fehlerinformationsfeld stellt abhängig von der Fehlermeldung kontextspezifische Informationen bereit. Wenn z. B. ein nicht aufgelöster Typdeklarationsfehler auftritt, zeigt das zusätzliche Fehlerinformationsfeld den Namen des Typs an, der nicht aufgelöst werden konnte.

Warnungen zur Kompilierzeit werden im folgenden Format angezeigt:

``` syntax
<FileName>(line#) : warning MIDLnnnn: 
<warning text>
[optional context information]:
```

Kompilierzeitfehler werden im folgenden Format angezeigt:

``` syntax
<FileName>(line#) : error MIDLnnnn: 
<error text>
[optional context information] :
```

Optionale Kontextinformationen beziehen sich auf den Kontext, in dem der Fehler aufgetreten ist. Sie wird generiert, wenn der MIDL-Compiler während der semantischen Analyse von Typ- und Prozedursignaturen einen Fehler erkennt. Der MIDL-Compiler meldet diese Informationen, damit Sie den Fehler schnell in der IDL-Datei finden können.

Systemfehlermeldungen werden im folgenden Format angezeigt:

``` syntax
<FileName>(line#) : MIDL error 0xnnnn: 
"Unexpected internal compiler problem. Try to find a workaround."
```

Diese Meldung wird durch einen unerwarteten Fehler generiert. Die Hexadezimalfehlernummer ist ein Windows XP, Windows 2000, Windows NT, Windows 98 oder Windows 95 Systemfehlerbezeichner. Weitere Informationen finden Sie möglicherweise in Winerror.h oder Ntstatus.h. Weitere Informationen zum Umgehen der Bedingungen, die diesen Fehler verursacht haben, finden Sie im Fehlertext für den [Compilerfehler](compiler-errors.md) MIDL9008.

 

 




