---
title: WM/wmadrcpeer Reference
description: Das WM/wmadrcpeakreference-Attribut enthält die maximale Volumeebene der Datei als codiert. Dieser Wert wird von Windows Media Player für die dynamische Bereichs Steuerung verwendet. Dieser Wert wird vom Codec festgelegt und ist schreibgeschützt.
ms.assetid: c732ee88-437b-4970-8f17-61aed2d91022
keywords:
- WM/wmadrcpeer Reference Windows Media-Format
topic_type:
- apiref
api_name:
- WM/WMADRCPeakReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59660f950c748c45a1affccee10ae86e38998f23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389215"
---
# <a name="wmwmadrcpeakreference"></a>WM/wmadrcpeer Reference

Das **WM/wmadrcpeakreference-** Attribut enthält die maximale Volumeebene der Datei als codiert. Dieser Wert wird von Windows Media Player für die dynamische Bereichs Steuerung verwendet. Dieser Wert wird vom Codec festgelegt und ist schreibgeschützt.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmwmadrcpeer Reference

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

[**WM/wmadrcpeer Target**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




