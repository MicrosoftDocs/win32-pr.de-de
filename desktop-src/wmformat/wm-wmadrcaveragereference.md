---
title: WM/wmadrcaveragereferenzierung
description: Das WM/wmadrcaveragereferenzierungsattribut enthält die durchschnittliche Volumeebene der Datei als codiert.
ms.assetid: 994614e3-06e2-48f0-bdac-6de5ab0c0eff
keywords:
- WM/wmadrcaveragereferenzierung Windows Media-Format
topic_type:
- apiref
api_name:
- WM/WMADRCAverageReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7059b68658d070ca71a738a5e20658474139558
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341899"
---
# <a name="wmwmadrcaveragereference"></a>WM/wmadrcaveragereferenzierung

Das **WM/wmadrcaveragereferenzierungsattribut** enthält die durchschnittliche Volumeebene der Datei als codiert.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmwmadrcaveragereferenzierung

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ DWORD**

## <a name="remarks"></a>Bemerkungen

Es gibt vier Attribute, die von Windows-Media Player für das dynamische Bereichs Steuerelement verwendet werden: **WM/wmadrcaveragereferenzierung**, **WM/wmadrcpeer Reference**, **WM/wmadrcaveragetarget** und **WM/wmadrcpeer Target**. Alle diese Werte werden vom Writer auf der Grundlage von Informationen aus dem Codec festgelegt, wenn Streams mit dem Windows Media Audio 9-Codec oder Windows Media Audio 9 Professional-Codec geschrieben werden. Die durchschnittlichen Werte werden auf die durchschnittliche Volumeebene des Streams festgelegt, und die Spitzenwerte werden auf die maximale Volumeebene im Stream festgelegt. Die Verweis Werte sind schreibgeschützt. Die Zielwerte werden von Windows Media Player festgelegt, wenn die Datei wiedergegeben wird, um die Einstellungen für die dynamische Bereichs Kontrolle des Benutzers aufzuzeichnen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> <dt>

[**WM/wmadrcaveragetarget**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/wmadrcpeer Reference**](wm-wmadrcpeakreference.md)
</dt> <dt>

[**WM/wmadrcpeer Target**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




