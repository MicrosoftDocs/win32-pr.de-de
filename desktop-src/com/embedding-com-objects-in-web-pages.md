---
title: Einbetten von COM-Objekten in Webseiten
description: Sie können COM-Objekte in Webseiten verwenden. Erstellen Sie zu diesem Zweck zunächst eine Instanz dieses COM-Objekts. Nachdem eine Objektinstanz erstellt wurde, können Sie Sie in nachfolgenden Skripts auf dieser Webseite verwenden.
ms.assetid: 7e2c9da7-aeae-4206-8be9-1303240b2b1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4762dd01d4bc07aab5c0b146c56cdb1aec3cb28f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309728"
---
# <a name="embedding-com-objects-in-web-pages"></a>Einbetten von COM-Objekten in Webseiten

Sie können COM-Objekte in Webseiten verwenden. Erstellen Sie zu diesem Zweck zunächst eine Instanz dieses COM-Objekts. Nachdem eine Objektinstanz erstellt wurde, können Sie Sie in nachfolgenden Skripts auf dieser Webseite verwenden.

Um eine com-Objektinstanz auf einer Webseite zu erstellen, können Sie ein Objekttag verwenden. Wenn Ihre Skriptsprache eine native Methode zum Erstellen von COM-Objekten bereitstellt, können Sie alternativ eine Objektinstanz mithilfe eines Skripts erstellen.

Beachten Sie, dass das Einbetten von COM-Objekten in Webseiten nur mit Browsern funktioniert, die ActiveX und com unterstützen, z.b. Internet Explorer.

Im folgenden Beispiel wird veranschaulicht, wie das Objekttag zum Einbetten eines COM-Objekts in eine Webseite verwendet wird:

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

Sie können auch eine com-Objektinstanz im Skript erstellen, wenn Ihre Skriptsprache eine Möglichkeit zum Erstellen von COM-Objekten bietet. VBScript stellt z. b. die Methode "-Methode" und "JScript" das ActiveXObject-Objekt bereit. Das Erstellen von Objekten in Skripts wird in den folgenden Beispielen veranschaulicht.

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Dim objXL
  Set objXL = CreateObject("Excel.Application")
</SCRIPT>
 
<SCRIPT LANGUAGE = "JScript">
  var objXL = new ActiveXObject("Excel.Application");
</SCRIPT>
 
```

Neben der Methode "kreateobject" und dem ActiveXObject-Objekt wird von VBScript und JScript die Methode "GetObject" bereitgestellt, die eine Objektinstanz zurückgibt.

Nachdem ein COM-Objekt erstellt wurde, können Sie es in nachfolgenden Skripts mit dem im ID-Attribut des Objekttags angegebenen Bezeichner referenzieren. Im vorherigen Beispiel wurde dieser Bezeichner als "vid" angegeben. Beachten Sie, dass das Skript, das das COM-Objekt verwendet, nach dem Objekttag oder dem Skript angezeigt werden muss, das die Objektinstanz erstellt. Andernfalls ist der Objekt Bezeichner nicht definiert. Im folgenden Skript wird das objxl-Objekt verwendet, um die Versionsinformationen für Microsoft Excel anzuzeigen.

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Msgbox objXL.Version
</SCRIPT>
 
```

Wenn Sie Skripts schreiben, die auf einer Webseite eingebettet sind, stellt der Browser auch ein Objektmodell bereit, auf das Ihre Skripts zugreifen können. Das Modell, das von Internet Explorer verwendet wird, entspricht dem vom World Wide Web Consortium (W3C) vorgeschlagenen Dokumentobjektmodell (DOM).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Skripterstellung mit COM-Objekten](scripting-with-com-objects.md)
</dt> </dl>

 

 




