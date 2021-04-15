---
title: Aufrufen von Funktionen
description: Aufrufen von Funktionen
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Windows Media Player Skins, Aufrufen von Funktionen in JScript
- Skins, Aufrufen von Funktionen in JScript
- Aufrufen von Funktionen in JScript
- JScript-Dateien für Skins, Aufrufen von Funktionen
- Windows Media Player Skins, scriptfile-Attribut in JScript
- Skins, scriptfile-Attribut in JScript
- Attribute, scriptfile in JScript
- scriptfile-Attribut in JScript
- JScript-Dateien für Skins, scriptfile-Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9450c8ca09b75f66f6206c850a656192bb1bb9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516077"
---
# <a name="calling-functions"></a>Aufrufen von Funktionen

Wenn Sie mehr als ein paar Codezeilen aufzurufen müssen, können Sie eine Skriptdatei mit dem **scriptfile** -Attribut des **View** -Elements laden und die Funktionen im Skript aufzurufen. Sie können mehr als eine Datei pro Ansicht laden:


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



Nachdem die Skriptdateien geladen wurden, können Sie die darin enthaltenen Funktionen innerhalb Ihres Ansichts Abschnitts abrufen. Wenn Sie z. b. eine Funktion mit dem Namen *MyFunction* aufrufen möchten, wenn auf etwas geklickt wird, geben Sie Folgendes ein:


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> Wenn Sie mehr als eine Ansicht haben, sind nur die Funktionen in den in die aktuelle Ansicht geladenen Dateien für den XML-und JScript-Code verfügbar, der mit der aktuellen Ansicht ausgeführt wird. Dateien, die in andere Sichten geladen wurden, befinden sich nicht im Gültigkeitsbereich der aktuellen Ansicht.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden von JScript**](using-jscript.md)
</dt> </dl>

 

 




