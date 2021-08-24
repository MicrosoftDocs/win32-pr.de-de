---
title: Aufrufen von Funktionen
description: Aufrufen von Funktionen
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Windows Media Player Skins,Aufrufen von Funktionen in JScript
- Skins,Aufrufen von Funktionen in JScript
- Aufrufen von Funktionen in JScript
- JScript Dateien für Skins, aufrufende Funktionen
- Windows Media Player Skins, ScriptFile-Attribut in JScript
- skins,scriptFile-Attribut in JScript
- attributes,scriptFile in JScript
- scriptFile-Attribut in JScript
- JScript Dateien für Skins, ScriptFile-Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e41b5fdfd6109292a1a42cae43e42e8424348090541fd50a8d83f04d23b8329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764270"
---
# <a name="calling-functions"></a>Aufrufen von Funktionen

Wenn Sie mehr als einige Codezeilen aufrufen müssen, können Sie eine Skriptdatei mithilfe des **scriptFile-Attributs** des **VIEW-Elements** laden und die Funktionen im Skript aufrufen. Sie können mehr als eine Datei pro Ansicht laden:


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



Nachdem die Skriptdateien geladen wurden, können Sie funktionen in ihnen im Abschnitt Ansicht aufrufen. Um beispielsweise eine Funktion namens *myfunction* aufzurufen, wenn auf etwas geklickt wird, geben Sie Folgendes ein:


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> Wenn Sie über mehrere Ansichten verfügen, sind nur die Funktionen in Dateien, die in die aktuelle Ansicht geladen wurden, für den XML-Code verfügbar und JScript Code, der mit der aktuellen Ansicht ausgeführt wird. Dateien, die in anderen Ansichten geladen werden, befinden sich nicht im Gültigkeitsbereich der aktuellen Ansicht.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden von JScript**](using-jscript.md)
</dt> </dl>

 

 




