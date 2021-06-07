---
title: Befehl "Antwortdatei"
description: Eine Antwortdatei ist eine Textdatei, die eine oder mehrere MIDL-Compilerbefehlszeilenoptionen enthält.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- Befehlszeilenreferenz MIDL, Befehl "Antwortdatei"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cf4d07ce8465239874ff666537646da2c4c564
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387666"
---
# <a name="the-response-file-command"></a>Befehl "Antwortdatei"

Eine Antwortdatei ist eine Textdatei, die eine oder mehrere MIDL-Compilerbefehlszeilenoptionen enthält. Im Gegensatz zu einer Befehlszeile lässt eine Antwortdatei mehrere Zeilen mit Optionen und Dateinamen zu. Dies kann aufgrund von Einschränkungen Ihrer Buildumgebung oder zur Vereinfachung Ihres Buildprozesses nützlich sein.

## <a name="switch-options"></a>Switch-Optionen

``` syntax
midl @response_file
```

<dl> <dt>

<span id="response_file"></span><span id="RESPONSE_FILE"></span>*\_Antwortdatei*
</dt> <dd>

Gibt den Namen einer Antwortdatei an. Der Name der Antwortdatei muss unmittelbar auf das @-Zeichen folgen. Zwischen dem @-Zeichen und dem Namen der Antwortdatei ist kein Leerzeichen zulässig.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Als Alternative zum Platzieren aller Optionen, die einem Schalter in der Befehlszeile zugeordnet sind, akzeptiert der MIDL-Compiler Antwortdateien, die Schalter und Argumente enthalten. Optionen in einer Antwortdatei werden so interpretiert, als ob sie an diesem Speicherort in der MIDL-Befehlszeile vorhanden sind.

Jedes Argument in einer Antwortdatei muss in derselben Zeile beginnen und enden. Der schräge Schrägstrich ( ) kann nicht verwendet werden, um Zeilen \\ zu verketten. Wenn er Teil einer Zeichenfolge in Anführungszeichen in der Antwortdatei ist, kann der schräge Schrägstrich nur vor einem anderen schrägen Schrägstrich oder vor einem doppelten Anführungszeichen () verwendet werden. Wenn er nicht Teil einer Zeichenfolge in Anführungszeichen ist, kann der schräge Schrägstrich nur vor einem doppelten Anführungszeichen verwendet werden.

MIDL unterstützt Befehlszeilenargumente, die eine oder mehrere Antwortdateien in Kombination mit anderen Befehlszeilenschaltern enthalten.

Der MIDL-Compiler unterstützt keine geschachtelten Antwortdateien.

## <a name="examples"></a>Beispiele

**Midl @midl.rsp**

**midl -Oicf @midl1.rsp -env win32 @midl2.rsp itf.idl**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




