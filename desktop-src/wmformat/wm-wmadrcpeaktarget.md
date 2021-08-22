---
title: WM/WMADRCPeakTarget
description: Das WM/WMADRCPeakTarget-Attribut enthält die maximale Volumeebene, die vom Benutzer angefordert wird. Dieser Wert wird von Windows Media Player für die Steuerung des dynamischen Bereichs verwendet.
ms.assetid: 94ef5db1-34f4-4cf8-ac56-c85cca10536b
keywords:
- WM/WMADRCPeakTarget windows Media Format
topic_type:
- apiref
api_name:
- WM/WMADRCPeakTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c87c8d62316bfa3e732d0cdc00e0fcb5295c30e675fd9c21fcd5ac766f239f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590680"
---
# <a name="wmwmadrcpeaktarget"></a>WM/WMADRCPeakTarget

Das **WM/WMADRCPeakTarget-Attribut** enthält die maximale Volumeebene, die vom Benutzer angefordert wird. Dieser Wert wird von Windows Media Player für die Steuerung des dynamischen Bereichs verwendet.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMWMADRCPeakTarget

## <a name="data-type"></a>Datentyp

**\_WMT-TYP \_ DWORD**

## <a name="remarks"></a>Hinweise

Es gibt vier Attribute, die von Windows Media Player für die Dynamische Bereichssteuerung verwendet werden: **WM/WMADRCAverageReference,** **WM/WMADRCPeakReference,** **WM/WMADRCAverageTarget** und **WM/WMADRCPeakTarget.** Alle diese Werte werden vom Writer basierend auf Informationen vom Codec festgelegt, wenn Streams mit dem Windows Media Audio 9-Codec oder Windows Media Audio 9 Professional Codec geschrieben werden. Die Durchschnittswerte werden auf die durchschnittliche Volumenebene des Streams und die Spitzenwerte auf die maximale Volumeebene im Stream festgelegt. Die Verweiswerte sind schreibgeschützt. Die Zielwerte werden durch Windows Media Player festgelegt, wenn die Datei wiedergegeben wird, um die Einstellungen für das Dynamische Bereichssteuerelement des Benutzers aufzuzeichnen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)
</dt> <dt>

[**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> </dl>

 

 




