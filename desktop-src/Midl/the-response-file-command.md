---
title: Der Antwortdatei Befehl.
description: Eine Antwortdatei ist eine Textdatei, die eine oder mehrere Mittell-Compilerbefehlszeilenoptionen enthält.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- Befehlszeilen Referenz-Mittell, Antwortdatei Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f624f8bb4fd50fa77df604e5d56f48c9e55c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947964"
---
# <a name="the-response-file-command"></a>Der Antwortdatei Befehl.

Eine Antwortdatei ist eine Textdatei, die eine oder mehrere Mittell-Compilerbefehlszeilenoptionen enthält. Im Gegensatz zu einer Befehlszeile ermöglicht eine Antwortdatei mehrere Zeilen von Optionen und Dateinamen. Dies kann aufgrund von Einschränkungen ihrer Buildumgebung oder für Ihren Buildprozess nützlich sein.

## <a name="switch-options"></a>Optionen wechseln

``` syntax
midl @response_file
```

<dl> <dt>

<span id="response_file"></span><span id="RESPONSE_FILE"></span>*Antwort \_ Datei*
</dt> <dd>

Gibt den Namen einer Antwortdatei an. Der Name der Antwortdatei muss unmittelbar auf das @-Zeichen folgen. Zwischen dem @-Zeichen und dem Namen der Antwortdatei ist kein Leerraum zulässig.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Als Alternative zum Platzieren aller Optionen, die einem Switch in der Befehlszeile zugeordnet sind, akzeptiert der Mittell-Compiler Antwort Dateien, die Schalter und Argumente enthalten. Optionen in einer Antwortdatei werden so interpretiert, als ob Sie an dieser Stelle in der Mittell-Befehlszeile vorhanden sind.

Jedes Argument in einer Antwortdatei muss in derselben Zeile beginnen und enden. Der umgekehrte Schrägstrich ( \) kann nicht zum Verketten von Zeilen verwendet werden. Wenn es Teil einer Zeichenfolge in Anführungszeichen in der Antwortdatei ist, kann der umgekehrte Schrägstrich nur vor einem anderen umgekehrten Schrägstrich oder vor einem doppelten Anführungszeichen (") verwendet werden. Wenn Sie nicht Teil einer Zeichenfolge in Anführungszeichen ist, kann der umgekehrte Schrägstrich nur vor einem doppelten Anführungszeichen verwendet werden.

"Mittel l" unterstützt Befehlszeilenargumente, die eine oder mehrere Antwort Dateien in Kombination mit anderen Befehls zeilenschaltern enthalten.

Der mittlerer l-Compiler unterstützt keine netsted Response-Dateien.

## <a name="examples"></a>Beispiele

**MIDL @midl.rsp**

**Mittel l-Oicf @midl1.rsp -"Win32 @midl2.rsp . idl" für Win32**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




