---
title: Formate für Fehler-und Warnmeldungen
description: Die Liste der mittleren Fehlermeldungs-und Warn Nachrichtenformate.
ms.assetid: 8eb0f46f-e494-430a-8bb4-b8a21524b62e
keywords:
- Fehler-Mittell, Nachrichtenformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42552b8106b72d82b2b13b69a7cba7ac2e99e64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388704"
---
# <a name="error-and-warning-message-formats"></a>Formate für Fehler-und Warnmeldungen

Befehlszeilen Fehler werden im folgenden Format angezeigt:

``` syntax
Command line error : MIDLnnnn: <error text> 
[<additional error information>]
```

Das Feld zusätzliche Fehlerinformationen enthält kontextspezifische Informationen, die von der Fehlermeldung abhängig sind. Wenn beispielsweise ein nicht aufgelöster typdeklarations Fehler auftritt, zeigt das Feld zusätzliche Fehlerinformationen den Namen des Typs an, der nicht aufgelöst werden konnte.

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

Optionale Kontextinformationen beziehen sich auf den Kontext, in dem der Fehler aufgetreten ist. Es wird generiert, wenn der Mittelwert Compiler während der semantischen Analyse von Typ-und Prozedur Signaturen einen Fehler ermittelt. Der mittlerer l-Compiler meldet diese Informationen, damit Sie den Fehler in der IDL-Datei schnell finden können.

System Fehlermeldungen werden im folgenden Format angezeigt:

``` syntax
<FileName>(line#) : MIDL error 0xnnnn: 
"Unexpected internal compiler problem. Try to find a workaround."
```

Diese Meldung wird von einem unerwarteten Fehler generiert. Die hexadezimale Fehlernummer ist eine Windows XP-, Windows 2000-, Windows NT-, Windows 98-oder Windows 95-Systemfehler Kennung. Weitere Informationen finden Sie unter "Winerror. h" oder "NTSTATUS. h". Weitere Informationen zum Umgehen der Bedingungen, die diesen Fehler verursacht haben, finden Sie im Fehlertext für [Compilerfehler](compiler-errors.md) MIDL9008.

 

 




