---
title: Erkennen des Players
description: Erkennen des Players
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Windows Media Player Onlineshops,Erkennen von Playern
- Onlineshops,Erkennen von Playern
- Geben Sie 1 Onlineshops ein, und erkennen Sie Player.
- Geben Sie 2 Onlineshops ein, und erkennen Sie Player.
- Windows Media Player Onlineshops, Playererkennung
- Onlineshops, Playererkennung
- Typ 1 Onlineshops, Playererkennung
- Typ 2 Onlineshops, Playererkennung
- Playererkennung
- Erkennen von Playern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d511fc8c14a901c6823715293c5eb621b45762cd5e9fae78d8c4df503a03bf38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863510"
---
# <a name="detecting-the-player"></a>Erkennen des Players

Wenn Sie eine Webseite für Ihren Onlineshop erstellen, können Sie festlegen, dass Benutzer die Seite in einem Webbrowser oder in Windows Media Player anzeigen können sollen. Sie können ein ASP-Skript verwenden, um zu bestimmen, ob Ihre Webseite im Player gehostet wird.

Der folgende Beispielcode ruft den Versionsparameter aus der URL-Abfragezeichenfolge ab, um zu bestimmen, ob die Seite in Windows Media Player gehostet wird:


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



Beachten Sie, dass im vorherigen Code davon ausgegangen wird, dass der Versionsparameter in der Abfragezeichenfolge vorhanden ist, wenn er in Windows Media Player gehostet wird. Dies gilt für Seiten, die vom Benutzer geöffnet werden, aber möglicherweise nicht für Seiten, die mit **External.NavigateTaskPaneURL** geöffnet wurden. Damit die Versionsabfragezeichenfolge beim programmgesteuerten Navigieren vorhanden ist, müssen Sie dem Methodenaufruf den Versionsparameter hinzufügen oder die Version dynamisch an die Basis-URL des **Navigate-Elements** Ihres ServiceInfo-Dokuments anfügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Dynamisches Erstellen des ServiceInfo-Dokuments**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**External.NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Allgemeine Informationen zu Onlineshops vom Typ 1 und Typ 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




