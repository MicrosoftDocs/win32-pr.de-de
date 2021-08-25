---
title: Verwenden von COM-Objekten in Active Server Pages
description: Sie können SKRIPTS für COM-Objekte in Active Server Pages-Anwendungen (ASP) erstellen.
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8ba1bbdd0729a8893b1c28d1a2347fc5ddea04c8d0de4e1ea413e765ab8df4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896199"
---
# <a name="using-com-objects-in-active-server-pages"></a>Verwenden von COM-Objekten in Active Server Pages

Sie können SKRIPTS für COM-Objekte in Active Server Pages-Anwendungen (ASP) erstellen. Dazu müssen Sie zuerst eine Instanz des -Objekts erstellen, indem Sie entweder das OBJECT-Tag verwenden oder die CreateObject-Methode des ASP Server-Objekts aufrufen. Sobald ein COM-Objekt erstellt wurde, können Sie es in nachfolgenden Skripts auf der ASP-Seite verwenden.

Mit ASP können Sie mit vielen verschiedenen Typen von Skript-Engines arbeiten, von denen jede eine andere Skriptsprache unterstützt. ASP enthält VBScript und JScript-Engines. Sie können auch Skript-Engines verwenden, die von anderen Unternehmen entwickelt wurden, um Sprachen wie PerlScript, PScript, Python und andere zu unterstützen.

Wenn Sie die Skriptsprache für eine ASP-Seite nicht festlegen, ist VBScript die Standardeinstellung. Um eine andere Skriptsprache als VBScript anzugeben, fügen Sie oben auf jeder ASP-Seite eine Zeile wie die folgende ein:

``` syntax
<%@ LANGUAGE=JScript %>
 
```

Um ein COM-Objekt auf einer ASP-Seite zu verwenden, müssen Sie zuerst eine Instanz dieses Objekts erstellen. Verwenden Sie hierzu das OBJECT-Tag, und geben Sie den Wert "SERVER" für das RUNAT-Attribut an, wie im folgenden Beispiel gezeigt. Standardmäßig erstellt das OBJECT-Tag eine Instanz des -Objekts auf dem Client. Wenn Sie das RUNAT-Attribut auf SERVER festlegen, wird das Objekt auf dem Server erstellt. Das -Objekt muss auf dem Server ausgeführt werden, damit es von ASP verwendet werden kann.

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

Sie können auch eine Instanz eines COM-Objekts auf einer ASP-Seite erstellen, indem Sie die CreateObject-Methode des ASP Server-Objekts aufrufen. Die Verwendung von Server.CreateObject ist langsamer als das Erstellen des Objekts mithilfe eines OBJECT-Tags, aber es ist etwas besser lesbar, da es den programmgesteuerten Bezeichner anstelle des Klassenbezeichners des COM-Objekts angibt. Das Server-Objekt wird von ASP verfügbar gemacht und muss nicht erstellt werden. Das Aufrufen von Server.CreateObject wird in den folgenden Beispielen veranschaulicht. Das erste Beispiel ist VBScript:

``` syntax
<% 
  Set MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

Das nächste Beispiel ist JScript:

``` syntax
<% 
  var MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

Das Aufrufen von CreateObject ist langsamer als die Verwendung des OBJECT-Tags zum Erstellen eines COM-Objekts. In Anwendungen, in denen die Leistung wichtig ist, sollten Sie das OBJECT-Tag verwenden.

Nachdem Sie eine Instanz des COM-Objekts erstellt haben, können Sie sie in Skripts verwenden. Dies wird im folgenden VBScript-Beispiel veranschaulicht, das den Wert der Border-Eigenschaft des COM-Objekts legt.

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Skripterstellung mit COM-Objekten](scripting-with-com-objects.md)
</dt> </dl>

 

 




