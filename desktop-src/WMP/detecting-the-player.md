---
title: Erkennen des Players
description: Erkennen des Players
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Windows Media Player Online Stores, erkennen von Playern
- Online Stores, erkennen von Playern
- Typ 1 Online Stores, erkennen von Playern
- Typ 2 Online Stores, erkennen von Playern
- Windows Media Player Online Stores, Player Erkennung
- Online Stores, Player Erkennung
- Typ 1 Online Stores, Player Erkennung
- Typ 2 Online Stores, Player Erkennung
- Spieler Erkennung
- Erkennen von Playern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb919e790b07ccf5d8df587abd63d2344534b16b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947793"
---
# <a name="detecting-the-player"></a>Erkennen des Players

Wenn Sie eine Webseite für den Online Shop erstellen, können Sie festlegen, dass Benutzer in der Lage sein sollen, die Seite in einem Webbrowser oder in Windows Media Player anzuzeigen. Sie können ein ASP-Skript verwenden, um zu bestimmen, ob Ihre Webseite im Player gehostet wird.

Der folgende Beispielcode ruft den Versions Parameter aus der URL-Abfrage Zeichenfolge ab, um zu bestimmen, ob die Seite in Windows-Media Player gehostet wird:


```C++
<%
    Dim sVersion

    sVersion = Trim(Request.QueryString("version")) 
 
    If sVersion = "" Then   
        Response.Write "Not hosted in Windows Media Player"
    Else 
        Response.Write "Hosted in Windows Media Player<BR>"
        Response.Write "Version is " & sVersion
    End If
%>
```



Beachten Sie, dass der vorangehende Code davon ausgeht, dass der Versions Parameter in der Abfrage Zeichenfolge vorhanden ist, wenn er in Windows Media Player Dies gilt für Seiten, die vom Benutzer geöffnet werden, aber möglicherweise nicht für Seiten, die mithilfe von " **extern. navigatetaskpaneurl**" geöffnet wurden. Damit die Versions Abfrage Zeichenfolge bei Programm gesteuerter Navigation vorhanden ist, müssen Sie den Versions Parameter dem Methodenaufrufe hinzufügen oder die Version dynamisch an die Basis-URL des **Navigate** -Elements des serviceInfo-Dokuments anhängen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Dynamisches Erstellen des serviceingefo-Dokuments**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Extern. navigatetaskpaneurl**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




