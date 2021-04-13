---
title: Verwenden von COM-Objekten in Active Server Seiten
description: Sie können Skripts für COM-Objekte in Active Server Pages (ASP)-Anwendungen erstellen.
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d73244ce5bd6c56deeda9bf4e3e4986b3d4039
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309359"
---
# <a name="using-com-objects-in-active-server-pages"></a>Verwenden von COM-Objekten in Active Server Seiten

Sie können Skripts für COM-Objekte in Active Server Pages (ASP)-Anwendungen erstellen. Zu diesem Zweck müssen Sie zuerst eine Instanz des Objekts erstellen, indem Sie entweder das Objekttag verwenden oder die CreateObject-Methode des ASP-Server Objekts aufrufen. Nachdem ein COM-Objekt erstellt wurde, können Sie es in nachfolgenden Skripts auf der ASP-Seite verwenden.

Mithilfe von ASP können Sie mit vielen verschiedenen Typen von Skript Modulen arbeiten, die jeweils eine andere Skriptsprache unterstützen. ASP enthält VBScript-und JScript-Skript-Engines. Sie können auch Skript-Engines einbinden, die von anderen Unternehmen entwickelt wurden, um Sprachen wie z. b. Perl Script, Pscript, Python und andere zu unterstützen.

Wenn Sie die Skriptsprache für eine ASP-Seite nicht festlegen, ist VBScript die Standardeinstellung. Wenn Sie eine andere Skriptsprache als VBScript angeben möchten, fügen Sie oben auf jeder ASP-Seite eine Zeile wie die folgende ein:

``` syntax
<%@ LANGUAGE=JScript %>
 
```

Wenn Sie ein COM-Objekt in einer ASP-Seite verwenden möchten, müssen Sie zuerst eine Instanz dieses Objekts erstellen. Verwenden Sie hierzu das Objekttag, und geben Sie den Wert "Server" für das runat-Attribut an, wie im folgenden Beispiel gezeigt. Standardmäßig erstellt das Objekttag eine Instanz des-Objekts auf dem Client. Wenn das runat-Attribut auf Server festgelegt wird, wird das-Objekt auf dem Server erstellt. Das Objekt muss auf dem Server ausgeführt werden, damit es von ASP verwendet werden muss.

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

Sie können auch eine Instanz eines COM-Objekts auf einer ASP-Seite erstellen, indem Sie die CreateObject-Methode des ASP-Server Objekts aufrufen. Die Verwendung von Server. kreateobject ist langsamer als das Erstellen des Objekts mithilfe eines Objekttags, aber es ist etwas besser lesbar, da es den programmatischen Bezeichner anstelle des Klassen Bezeichners des COM-Objekts angibt. Das Server Objekt wird von ASP verfügbar gemacht und muss nicht erstellt werden. Die Vorgehensweise zum Aufrufen von Server. kreateobject wird in den folgenden Beispielen veranschaulicht. Das erste Beispiel ist VBScript:

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

Das Aufrufen von CreateObject ist langsamer als die Verwendung des Objekttags zum Erstellen eines COM-Objekts. In Anwendungen, bei denen die Leistung kritisch ist, sollten Sie das Object-Tag verwenden.

Nachdem Sie eine Instanz des COM-Objekts erstellt haben, können Sie Sie in Skripts verwenden. Dies wird im folgenden VBScript-Beispiel veranschaulicht, mit dem der Wert der Border-Eigenschaft des COM-Objekts festgelegt wird.

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Skripterstellung mit COM-Objekten](scripting-with-com-objects.md)
</dt> </dl>

 

 




