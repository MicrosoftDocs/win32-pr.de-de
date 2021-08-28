---
title: WM/WMADRCAverageReference
description: Das WM/WMADRCAverageReference-Attribut enthält die durchschnittliche Volumeebene der Datei als codiert.
ms.assetid: 994614e3-06e2-48f0-bdac-6de5ab0c0eff
keywords:
- WM/WMADRCAverageReference windows Media Format
topic_type:
- apiref
api_name:
- WM/WMADRCAverageReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9948d71739aaee4f5f24f54701f8e335f8b7b79486c8820f7a5fdf48c068e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026948"
---
# <a name="wmwmadrcaveragereference"></a>WM/WMADRCAverageReference

Das **WM/WMADRCAverageReference-Attribut** enthält die durchschnittliche Volumeebene der Datei als codiert.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMWMADRCAverageReference

## <a name="data-type"></a>Datentyp

**\_WMT-TYP \_ DWORD**

## <a name="remarks"></a>Hinweise

Es gibt vier Attribute, die von Windows Media Player für die Dynamische Bereichssteuerung verwendet werden: **WM/WMADRCAverageReference,** **WM/WMADRCPeakReference,** **WM/WMADRCAverageTarget** und **WM/WMADRCPeakTarget.** Alle diese Werte werden vom Writer basierend auf Informationen vom Codec festgelegt, wenn Streams mit dem Windows Media Audio 9-Codec oder Windows Media Audio 9 Professional Codec geschrieben werden. Die Durchschnittswerte werden auf die durchschnittliche Volumenebene des Streams und die Spitzenwerte auf die maximale Volumeebene im Stream festgelegt. Die Verweiswerte sind schreibgeschützt. Die Zielwerte werden durch Windows Media Player festgelegt, wenn die Datei wiedergegeben wird, um die Einstellungen der Dynamischen Bereichssteuerung des Benutzers aufzuzeichnen.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> <dt>

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




