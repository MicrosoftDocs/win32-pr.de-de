---
title: WM/wmadrcpeer Target
description: Das WM/wmadrcpeaktarget-Attribut enthält die maximale Volumeebene, die vom Benutzer angefordert wurde. Dieser Wert wird von Windows Media Player für die dynamische Bereichs Steuerung verwendet.
ms.assetid: 94ef5db1-34f4-4cf8-ac56-c85cca10536b
keywords:
- WM/wmadrcpeer Target Windows Media-Format
topic_type:
- apiref
api_name:
- WM/WMADRCPeakTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55eac4ea68cd61e2cfa0b5c185dc1a4ad17e5ce8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718611"
---
# <a name="wmwmadrcpeaktarget"></a>WM/wmadrcpeer Target

Das **WM/wmadrcpeaktarget-** Attribut enthält die maximale Volumeebene, die vom Benutzer angefordert wurde. Dieser Wert wird von Windows Media Player für die dynamische Bereichs Steuerung verwendet.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmwmadrcpeer-Ziel

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ DWORD**

## <a name="remarks"></a>Bemerkungen

Es gibt vier Attribute, die von Windows-Media Player für das dynamische Bereichs Steuerelement verwendet werden: **WM/wmadrcaveragereferenzierung**, **WM/wmadrcpeer Reference**, **WM/wmadrcaveragetarget** und **WM/wmadrcpeer Target**. Alle diese Werte werden vom Writer auf der Grundlage von Informationen aus dem Codec festgelegt, wenn Streams mit dem Windows Media Audio 9-Codec oder Windows Media Audio 9 Professional-Codec geschrieben werden. Die durchschnittlichen Werte werden auf die durchschnittliche Volumeebene des Streams festgelegt, und die Spitzenwerte werden auf die maximale Volumeebene im Stream festgelegt. Die Verweis Werte sind schreibgeschützt. Die Zielwerte werden von Windows Media Player festgelegt, wenn die Datei wiedergegeben wird, um die Einstellungen für die dynamische Bereichs Kontrolle des Benutzers aufzuzeichnen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> <dt>

[**WM/wmadrcaveragereferenzierung**](wm-wmadrcaveragereference.md)
</dt> <dt>

[**WM/wmadrcaveragetarget**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/wmadrcpeer Reference**](wm-wmadrcpeakreference.md)
</dt> </dl>

 

 




