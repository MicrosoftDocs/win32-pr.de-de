---
title: UI_PKEY_Label
description: Bezeichnet die Eigenschaft "UI \_ pkey \_ Label".
ms.assetid: 4d704133-bba7-4c32-a552-d748b66455eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245ce8d239e1a0893c907a047aa9a48996cbf606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856416"
---
# <a name="ui_pkey_label"></a>UI- \_ pkey- \_ Bezeichnung

Bezeichnet die Eigenschaft "UI \_ pkey \_ Label".

```
propertyDescription
   name = UI_PKEY_Label
   shellPKey = UI_PKEY_Label
   formatID = 00000004-7363-696e-8441798acf5aebb7
   propID = 4
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Bemerkungen

Die Benutzeroberflächen- \_ pkey- \_ Bezeichnung wird von einer Anwendung verwendet, um den Bezeichnungs Text von Registerkarten, Gruppen, Schaltflächen, Galerie Elementen und anderen Menü Band Steuerelementen abzufragen.

> [!Note]  
> Windows 8 und höher: das Bild der [Anwendungsmenü](windowsribbon-controls-applicationmenu.md) Schaltfläche wurde in Bezeichnung: **File** geändert. Es wird empfohlen, die Datei nicht als Bezeichnung für eine ihrer eigenen Registerkarten zu verwenden.

 

Der Eigenschafts Wert ist eine Zeichenfolge, die auf eine beliebige Sequenz von Zeichen beschränkt ist, einschließlich Leerzeichen und Zeilenumbruch Zeichen.

> [!Note]  
> Verwenden Sie den XML-Zeichen Verweis Universal Character Set (UCS) `&#xA;` , um einen Zeilenumbruch anzugeben.

 

Die Rechte Ausrichtung wird nicht unterstützt.

Die maximale Länge der UI- \_ pkey- \_ Bezeichnung ist unbegrenzt.

Wenn ein Befehl über ein Menü Element verfügbar gemacht wird und der Wert von [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) oder UI \_ pkey \_ Label einen Buchstaben enthält, dem ein kaufmännisches und vorangestellt ist, wie im folgenden Beispiel gezeigt, wird dieser Buchstabe sowohl als KeyTip als auch als Tastaturbeschleuniger für diesen Befehl durch das Multifunktionsleisten-Framework behandelt.


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



Um ein kaufmännisches und-Zeichen in einer Bezeichnung anzuzeigen, versehen Sie die Bezeichnung für Sonderzeichen mit einem doppelten kaufmännisches und-Zeichen ( `&&` ), wie im folgenden Beispiel gezeigt.


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen Eigenschaften](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command. labeltitle**](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[UI \_ pkey \_ labeldescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




