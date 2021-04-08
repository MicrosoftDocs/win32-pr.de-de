---
title: UI_PKEY_LabelDescription
description: Bezeichnet die Benutzeroberflächen- \_ pkey- \_ labeldescription-Eigenschaft.
ms.assetid: e7dfbe7e-c9c9-44fe-9e2d-39e20f5f7062
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb81e723d5f55dcfd63f1bb89bff4741b4e088e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856415"
---
# <a name="ui_pkey_labeldescription"></a>UI \_ pkey \_ labeldescription

Bezeichnet die Benutzeroberflächen- \_ pkey- \_ labeldescription-Eigenschaft.

```
propertyDescription
   name = UI_PKEY_LabelDescription
   shellPKey = UI_PKEY_LabelDescription
   formatID = 00000002-7363-696e-8441798acf5aebb7
   propID = 2
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Bemerkungen

UI \_ pkey \_ labeldescription wird von einer Anwendung verwendet, um die einer [UI- \_ pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)zugeordnete Beschreibung abzufragen.

Der Eigenschafts Wert ist eine Zeichenfolge, die auf eine beliebige Sequenz von Zeichen beschränkt ist, einschließlich Leerzeichen und Zeilenumbruch Zeichen.

> [!Note]  
> Verwenden Sie den XML-Zeichen Verweis Universal Character Set (UCS) `&#xA;` , um einen Zeilenumbruch anzugeben.

 

Die maximale Länge ist unbegrenzt.

Die Rechte Ausrichtung wird nicht unterstützt.

Der folgende Screenshot veranschaulicht die Verwendung einer Bezeichnung und eine zugehörige Bezeichnungs Beschreibung in einem Anwendungsmenü.

![Screenshot, in dem eine Bezeichnung und eine zugehörige Bezeichnungs Beschreibung in einem Anwendungsmenü angezeigt werden.](images/properties/ui-pkey-labeldescription.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen Eigenschaften](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command. labeldescription**](windowsribbon-element-command-labeldescription.md)
</dt> <dt>

[UI- \_ pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 




