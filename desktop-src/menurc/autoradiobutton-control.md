---
title: AUTORADIOBUTTON-Steuerelement
description: Definiert ein automatisches Optionsfeld-Steuerelement. Dieses Steuerelement führt den gegenseitigen Ausschluss mit den anderen AUTORADIOBUTTON-Steuerelementen in derselben Gruppe automatisch aus. Wenn die Schaltfläche ausgewählt wird, wird die Anwendung mit dem \_ angeklickten BN benachrichtigt.
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- AUTORADIOBUTTON-Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67395437303de0adc8c1af226210f8ca2f45958d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718353"
---
# <a name="autoradiobutton-control"></a>AUTORADIOBUTTON-Steuerelement

Definiert ein automatisches Optionsfeld-Steuerelement. Dieses Steuerelement führt den gegenseitigen Ausschluss mit den anderen **AUTORADIOBUTTON** -Steuerelementen in derselben Gruppe automatisch aus. Wenn die Schaltfläche ausgewählt wird, wird die Anwendung mit **dem \_ angeklickten BN** benachrichtigt.

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

Text, der neben dem Optionsfeld angezeigt wird.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Stile für das Optionsfeld automatisch, bei dem es sich um eine Kombination aus Schaltflächen Klassen Formaten und den folgenden Stilen handeln kann: **WS \_ Tabstopps**, **WS- \_ Deaktivierte** und **WS- \_ Gruppe**.

Wenn Sie keinen Stil angeben, ist der Standardstil `BS_AUTORADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Steuerelement**](control-control.md)
</dt> <dt>

[Options Felder](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[**RadioButton**](radiobutton-control.md)
</dt> </dl>

 

 




