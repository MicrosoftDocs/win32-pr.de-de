---
title: Attribute mit mehreren Werten (Windows Media Player SDK)
description: Erfahren Sie mehr über Attribute mit mehreren Werten im Windows Media Player SDK. Einige Medienelementattribute können mehrere Werte haben.
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Windows Media Player,Attribute für Medienelemente
- Windows Media Player Objektmodell,Attribute für Medienelemente
- Objektmodell,Attribute für Medienelemente
- Windows Media Player Mobile,Attribute für Medienelemente
- Windows Media Player ActiveX-Steuerelement,Attribute für Medienelemente
- Windows Media Player Mobile ActiveX-Steuerelement,Attribute für Medienelemente
- ActiveX-Steuerelement,Attribute für Medienelemente
- Windows Media Player Bibliothek,Attribute für Medienelemente
- Bibliothek,Attribute für Medienelemente
- Attribute,mehrere Werte
- Mehrere Attributwerte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16baf4bab47dc972ec7b043980dccb0f2aadd57
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262602"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a>Attribute mit mehreren Werten (Windows Media Player SDK)

Einige Medienelementattribute können mehrere Werte haben. Beispielsweise können die **Attribute Author**, **WM/Composer** und **WM/Genre** jeweils mehrere Werte haben. Der Datentyp solcher Attribute ist eine **mehrwertige Zeichenfolge.**

In Windows Media Player zeigt die Bibliothek mehrere Werte in einem einzelnen Feld an, indem die Werte durch Semikolons getrennt werden. Jeder Wert ist jedoch tatsächlich ein separates Attribut im Windows Media-Element.

Sie können Code schreiben, der bestimmt, ob ein bestimmtes Attribut über mehrere Werte verfügt, und dann alle diese Werte abrufen. Sie müssen Media *verwenden.* **getItemInfoByType**. Wenn Sie media *verwenden.* **getItemInfo-Methode** zum Abrufen eines mehrwertigen Attributs. Sie rufen nur den ersten Wert ab.

Im letzten Beispiel im Thema [Lesen von Attributwerten](reading-attribute-values.md) wird die Verwendung von *Media veranschaulicht.* **getAttributeCountByType und** *Media*. **getItemInfoByType-Methoden** zum Abrufen mehrerer Werte für ein bestimmtes Attribut.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Medienelementattribute**](media-item-attributes.md)
</dt> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Lesen von Attributwerten von einer CD oder DVD**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




