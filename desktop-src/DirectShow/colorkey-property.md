---
description: Die ColorKey-Eigenschaft legt den bei Untertiteln verwendeten Farbschlüssel fest oder ruft den Farbschlüssel ab.
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: ColorKey-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abca1dabbdb67f4380dbe32acbf2948862695b7c424dfd08629ec16237bb88c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073734"
---
# <a name="colorkey-property"></a>ColorKey-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `ColorKey` -Eigenschaft legt den bei Untertiteln verwendeten Farbschlüssel fest oder ruft den Farbschlüssel ab.

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die Farbe darstellt, die als transparenter Hintergrund für Untertiteltext verwendet werden soll. Der Standardwert in 256 Farben ist Magenta und off-black in jeder anderen Farbtiefe.

## <a name="remarks"></a>Hinweise

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff. Diese Eigenschaft gilt nur für Untertitel, sofern vorhanden, nicht für den Bildstrom.

 

 



