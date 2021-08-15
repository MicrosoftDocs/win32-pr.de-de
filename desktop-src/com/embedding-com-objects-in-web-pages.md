---
title: Einbetten von COM-Objekten in Webseiten
description: Sie können COM-Objekte auf Webseiten verwenden. Erstellen Sie hierzu zunächst eine Instanz dieses COM-Objekts. Nachdem eine Objektinstanz erstellt wurde, können Sie sie in nachfolgenden Skripts auf dieser Webseite verwenden.
ms.assetid: 7e2c9da7-aeae-4206-8be9-1303240b2b1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d13a92bd2de152e71ac4284ce37b977e8305f25dcb2aef5eb94d6019d115812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736891"
---
# <a name="embedding-com-objects-in-web-pages"></a>Einbetten von COM-Objekten in Webseiten

Sie können COM-Objekte auf Webseiten verwenden. Erstellen Sie hierzu zunächst eine Instanz dieses COM-Objekts. Nachdem eine Objektinstanz erstellt wurde, können Sie sie in nachfolgenden Skripts auf dieser Webseite verwenden.

Um eine COM-Objektinstanz auf einer Webseite zu erstellen, können Sie ein OBJECT-Tag verwenden. Wenn Ihre Skriptsprache eine native Möglichkeit zum Erstellen von COM-Objekten bietet, können Sie alternativ eine Objektinstanz mithilfe eines Skripts erstellen.

Beachten Sie, dass das Einbetten von COM-Objekten in Webseiten nur mit Browsern funktioniert, die ActiveX und COM unterstützen, z. B. Internet Explorer.

Das folgende Beispiel veranschaulicht die Verwendung des OBJECT-Tags zum Einbetten eines COM-Objekts in eine Webseite:

``` syntax
<OBJECT 
  ID = vid 
  CLASSID = "clsid:31263EC0-2957-11CF-A1E5-00AA9EC79700" 
  BORDER = 0 
  VSPACE = 0 
  HSPACE = 0 
  ALIGN = TOP 
  HEIGHT = 100% 
  WIDTH = 100%
>
</OBJECT>
 
```

Sie können auch eine COM-Objektinstanz im Skript erstellen, wenn Ihre Skriptsprache eine Möglichkeit zum Erstellen von COM-Objekten bietet. VBScript stellt beispielsweise die CreateObject-Methode und JScript das ActiveXObject-Objekt bereit. Das Erstellen von Objekten im Skript wird in den folgenden Beispielen veranschaulicht.

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Dim objXL
  Set objXL = CreateObject("Excel.Application")
</SCRIPT>
 
<SCRIPT LANGUAGE = "JScript">
  var objXL = new ActiveXObject("Excel.Application");
</SCRIPT>
 
```

Neben der CreateObject-Methode und dem ActiveXObject-Objekt stellen VBScript und JScript die Methode GetObject bereit, die eine Objektinstanz zurückgibt.

Nachdem ein COM-Objekt erstellt wurde, können Sie in nachfolgenden Skripts darauf verweisen, indem Sie den bezeichner verwenden, der im ID-Attribut des OBJECT-Tags angegeben ist. Im vorherigen Beispiel wurde dieser Bezeichner als "vid" angegeben. Beachten Sie, dass das Skript, das das COM-Objekt verwendet, nach dem OBJECT-Tag oder -Skript angezeigt werden muss, das die Objektinstanz erstellt. Andernfalls ist der Objektbezeichner nicht definiert. Das folgende Skript verwendet das objXL-Objekt, um die Versionsinformationen für Microsoft Excel anzuzeigen.

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Msgbox objXL.Version
</SCRIPT>
 
```

Wenn Sie Skripts schreiben, die in eine Webseite eingebettet sind, macht der Browser auch ein Objektmodell verfügbar, auf das Ihre Skripts zugreifen können. Das von Internet Explorer verwendete Modell entspricht dem vom World Wide Web Consortium (W3C) vorgeschlagenen Dokumentobjektmodell (DOM).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Skripterstellung mit COM-Objekten](scripting-with-com-objects.md)
</dt> </dl>

 

 




