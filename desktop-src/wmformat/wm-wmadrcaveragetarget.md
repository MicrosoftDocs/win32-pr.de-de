---
title: WM/WMADRCAverageTarget
description: Das WM/WMADRCAverageTarget-Attribut enthält die vom Benutzer angeforderte durchschnittliche Volumeebene. Dieser Wert wird von Windows Media Player für die dynamische Bereichssteuerung verwendet.
ms.assetid: 8173b5ab-27e4-4af9-aea8-6c1310f065f5
keywords:
- WM/WMADRCAverageTarget windows Media Format
topic_type:
- apiref
api_name:
- WM/WMADRCAverageTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd08dd09b6db671a0af1d816162923624cb781148f557ce4bee21fe2dc9a933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083914"
---
# <a name="wmwmadrcaveragetarget"></a>WM/WMADRCAverageTarget

Das **WM/WMADRCAverageTarget-Attribut enthält** die vom Benutzer angeforderte durchschnittliche Volumeebene. Dieser Wert wird von Windows Media Player für die dynamische Bereichssteuerung verwendet.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMWMADRCAverageTarget

## <a name="data-type"></a>Datentyp

**WMT \_ TYPE \_ DWORD**

## <a name="remarks"></a>Hinweise

Es gibt vier Attribute, die von Windows Media Player für die dynamische Bereichssteuerung verwendet werden: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** und **WM/WMADRCPeakTarget**. Alle diese Werte werden vom Writer basierend auf Informationen aus dem Codec festgelegt, wenn Streams mit dem Windows Media Audio 9-Codec oder Windows Media Audio 9-Professional werden. Die Durchschnittswerte werden auf die durchschnittliche Volumeebene des Streams und die Spitzenwerte auf die maximale Volumeebene im Stream festgelegt. Die Verweiswerte sind schreibgeschützt. Die Zielwerte werden von der Windows Media Player, wenn die Datei abgespielt wird, um die Einstellungen für das dynamische Bereichssteuerprogramm des Benutzers zu erfassen.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)
</dt> <dt>

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> <dt>

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




