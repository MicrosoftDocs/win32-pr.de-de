---
title: UI_PKEY_Label
description: Identifiziert die \_ PKEY \_ Label-Eigenschaft der Benutzeroberfläche.
ms.assetid: 4d704133-bba7-4c32-a552-d748b66455eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13506d1609f915c2eab9824a3f5256383c5f2aecf73ed5787e3372f17b44b435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706431"
---
# <a name="ui_pkey_label"></a>\_ \_ UI-PKEY-Bezeichnung

Identifiziert die \_ PKEY \_ Label-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_Label
   shellPKey = UI_PKEY_Label
   formatID = 00000004-7363-696e-8441798acf5aebb7
   propID = 4
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Hinweise

Ui \_ PKEY \_ Label wird von einer Anwendung verwendet, um den Bezeichnungstext von Registerkarten, Gruppen, Schaltflächen, Katalogelementen und anderen Menübandsteuerelementen abzufragen.

> [!Note]  
> Windows 8 und neuer: Bild der Schaltfläche ["Anwendungsmenü"](windowsribbon-controls-applicationmenu.md) wurde in die Bezeichnung **Datei** geändert. Es wird empfohlen, Datei nicht als Bezeichnung für ihre eigenen Registerkarten zu verwenden.

 

Der -Eigenschaftswert ist eine Zeichenfolge, die auf eine beliebige Zeichensequenz beschränkt ist, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.

> [!Note]  
> Verwenden Sie den UCS-XML-Zeichenverweis (Universal Character Set), `&#xA;` um einen Zeilenbreak anzugeben.

 

Die rechte Ausrichtung wird nicht unterstützt.

Die maximale Länge der \_ Ui-PKEY-Bezeichnung \_ ist nicht gebunden.

Wenn ein Befehl über ein Menüelement verfügbar gemacht wird und der Wert von [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) oder UI \_ PKEY \_ Label einen Buchstaben enthält, dem ein ampersand vorangestellt ist, wie im folgenden Beispiel gezeigt, wird dieser Buchstabe sowohl als KeyTip als auch als Tastaturtaste für diesen Befehl vom Menübandframework behandelt.


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



Um ein ampersand in einer Bezeichnung anzuzeigen, escapen Sie die Sonderzeichenbezeichnung mit einem doppelten Ampersand ( `&&` ), wie im folgenden Beispiel gezeigt.


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourceneigenschaften](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[UI \_ PKEY \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




