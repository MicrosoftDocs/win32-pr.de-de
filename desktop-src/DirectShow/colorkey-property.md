---
description: Die Colorkey-Eigenschaft legt den in Untertiteln verwendeten Farbschlüssel fest oder ruft ihn ab.
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: Colorkey-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75620be88a861e02915c27324978382feefc5835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481179"
---
# <a name="colorkey-property"></a>Colorkey-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `ColorKey` Eigenschaft legt den in Untertiteln verwendeten Farbschlüssel fest oder ruft ihn ab.

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die Farbe darstellt, die als transparenter Hintergrund für Closed-beschrifteten Text verwendet werden soll. Der Standardwert in 256 Farben ist Magenta und Off-Black in jeder anderen Farbtiefe.

## <a name="remarks"></a>Bemerkungen

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff. Diese Eigenschaft gilt nur für geschlossene Untertitel, sofern vorhanden, nicht für den subbildstream.

 

 



