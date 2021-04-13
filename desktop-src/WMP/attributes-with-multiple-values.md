---
title: Attribute mit mehreren Werten (Windows Media Player SDK)
description: Attribute mit mehreren Werten
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Windows Media Player, Attribute für Medienelemente
- Windows Media Player-Objektmodell, Attribute für Medienelemente
- Objektmodell, Attribute für Medienelemente
- Windows Media Player Mobile, Attribute für Medienelemente
- Windows Media Player ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player Mobile ActiveX-Steuerelement, Attribute für Medienelemente
- ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player-Bibliothek, Attribute für Medienelemente
- Bibliothek, Attribute für Medienelemente
- Attribute, mehrere Werte
- mehrere Attributwerte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad93c4025d09a234b1834a32e4ca3789bcaa4a35
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391442"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a>Attribute mit mehreren Werten (Windows Media Player SDK)

Einige Medien Element Attribute können mehrere Werte aufweisen. Beispielsweise können die Attribute **Author**, **WM/Composer** und **WM/Genre** jeweils mehr als einen Wert aufweisen. Der Datentyp dieser Attribute ist eine **mehrwertige Zeichenfolge**.

In Windows Media Player werden in der Bibliothek mehrere Werte in einem einzelnen Feld angezeigt, wobei die Werte durch Semikolons getrennt werden. Jeder Wert ist jedoch tatsächlich ein separates Attribut im Windows Media-Element.

Sie können Code schreiben, mit dem bestimmt wird, ob ein bestimmtes Attribut über mehrere Werte verfügt, und dann alle diese Werte abrufen. Sie müssen- *Medien* verwenden. **getItemInfoByType**. Wenn Sie die *Medien* verwenden. **getiteminfo** -Methode zum Abrufen eines mehrwertigen Attributs wird nur der erste Wert abgerufen.

Das abschließende Beispiel im Thema [Lesen von Attributwerten](reading-attribute-values.md) veranschaulicht die Verwendung des *Mediums*. **getattributezähltbytype** und *Medium*. **getItemInfoByType** -Methoden zum Abrufen mehrerer Werte für ein bestimmtes Attribut.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Medien Element Attribute**](media-item-attributes.md)
</dt> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Lesen von Attributwerten von einer CD oder DVD**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




