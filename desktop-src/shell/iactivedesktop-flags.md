---
description: In diesem Abschnitt werden die von iactivedesktop-Schnittstellen Methoden verwendeten Flags beschrieben.
title: Iactivedesktop-Flags (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d1a2f69-0730-4805-8b50-071332ff7070
api_name:
- AD_APPLY_ALL
- AD_APPLY_BUFFERED_REFRESH
- AD_APPLY_DYNAMICREFRESH
- AD_APPLY_FORCE
- AD_APPLY_HTMLGEN
- AD_APPLY_REFRESH
- AD_APPLY_SAVE
- COMP_ELEM_ALL
- COMP_ELEM_CHECKED
- COMP_ELEM_CURITEMSTATE
- COMP_ELEM_FRIENDLYNAME
- COMP_ELEM_NOSCROLL
- COMP_ELEM_ORIGINAL_CSI
- COMP_ELEM_POS_LEFT
- COMP_ELEM_POS_TOP
- COMP_ELEM_POS_ZINDEX
- COMP_ELEM_RESTORED_CSI
- COMP_ELEM_SIZE_HEIGHT
- COMP_ELEM_SIZE_WIDTH
- COMP_ELEM_SOURCE
- COMP_ELEM_TYPE
- COMP_TYPE_CFHTML
- COMP_TYPE_CONTROL
- COMP_TYPE_HTMLDOC
- COMP_TYPE_MAX
- COMP_TYPE_PICTURE
- COMP_TYPE_WEBSITE
- COMPONENT_TOP
- WPSTYLE_CENTER
- WPSTYLE_MAX
- WPSTYLE_STRETCH
- WPSTYLE_TILE
- WPSTYLE_SPAN
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dae164c696ae54963f802a6ddd5cb1f6862b2f14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982932"
---
# <a name="iactivedesktop-flags"></a>Iactivedesktop-Flags

In diesem Abschnitt werden die von [**iactivedesktop-**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) Schnittstellen Methoden verwendeten Flags beschrieben.

<dl> <dt>

<span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD \_ \_ alle anwenden**
</dt> <dd> <dl> <dt>



Aggregat der * * * * AD Apply \_ \_ Save * * * *, * * * * AD Apply \_ \_ htmlgen * * * * und * * * * AD \_ Apply \_ Refresh * * * *-Werte.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD \_ - \_ gepufferte \_ Aktualisierung anwenden**
</dt> <dd> <dl> <dt>



Startet einen Timer und aggregiert alle Aktualisierungs Anforderungen, die während dieses Zeitintervalls mit diesem Flag durchgeführt werden, in eine einzelne Aktualisierung. Dieses Intervall ist auf fünf Sekunden festgelegt. Am Ende des Intervalls oder wenn eine Aktualisierung während des Intervalls ohne das Flag "* * * * AD \_ Apply \_ Buffered Refresh * * * *" angefordert wird \_ , wird die Aktualisierung durchgeführt, und der Timer wird angehalten. Dieses Flag muss mit dem Flag * * * * AD \_ Apply \_ Refresh * * * * kombiniert werden.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**AD \_ Apply \_ dynamikrefresh**
</dt> <dd> <dl> <dt>



[Version 5,0](versions.md). Verwenden Sie Dynamic HTML, um nur die Elemente zu aktualisieren, die sich seit der letzten Aktualisierung geändert haben, nicht den gesamten Desktop.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**AD \_ Apply \_ Force**
</dt> <dd> <dl> <dt>



Erzwingen einer aktiven Desktop Änderung


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**AD \_ Anwenden von \_ htmlgen**
</dt> <dd> <dl> <dt>



Generieren Sie die HTML-Desktop Datei erneut.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**AD \_ - \_ Aktualisierung anwenden**
</dt> <dd> <dl> <dt>



Aktualisieren Sie das Desktop Element.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**AD \_ Apply \_ Save**
</dt> <dd> <dl> <dt>



Speichern Sie das Desktop Element.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**Alle Comp- \_ Elem \_**
</dt> <dd> <dl> <dt>



Aggregat der Comp- \_ Elem- \_ \* Werte.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**Comp- \_ Elem \_ aktiviert**
</dt> <dd> <dl> <dt>



Das Element wurde geprüft.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**Comp \_ Elem \_ curitemstate**
</dt> <dd> <dl> <dt>



Der aktuelle Zustand des Desktop Elements.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**Comp \_ Elem \_ FriendlyName**
</dt> <dd> <dl> <dt>



Der Anzeige Name des Elements.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**Comp \_ Elem \_ NoScroll**
</dt> <dd> <dl> <dt>



Das Element kann nicht Bild lauffähigen.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**Comp \_ Elem- \_ ursprünglicher \_ CSI**
</dt> <dd> <dl> <dt>



Die ursprünglichen Zustandsinformationen des Desktop Elements.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**Comp-Elem Torys Verb \_ \_ \_ leiben**
</dt> <dd> <dl> <dt>



Die horizontale Position des Elements.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**Comp- \_ Elem \_ \_ tortop**
</dt> <dd> <dl> <dt>



Die vertikale Position des Elements.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**Comp \_ Elem \_ POS \_ ZIndex**
</dt> <dd> <dl> <dt>



Der z-Index des Elements.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**Comp- \_ \_ wiederhergestellte \_ CSI**
</dt> <dd> <dl> <dt>



Die Statusinformationen des wiederhergestellten Desktop Elements.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**Größe der Comp \_ Elem- \_ Größe \_**
</dt> <dd> <dl> <dt>



Die Höhe des Elements.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**Breite der Comp \_ Elem- \_ Größe \_**
</dt> <dd> <dl> <dt>



Die Breite des Elements.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**Comp- \_ Elem- \_ Quelle**
</dt> <dd> <dl> <dt>



Die ursprüngliche Quelle des Elements.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**Comp- \_ Elem- \_ Typ**
</dt> <dd> <dl> <dt>



Der Elementtyp.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**Comp- \_ Typ \_ cfhtml**
</dt> <dd> <dl> <dt>



Komprimiertes HTML-Format.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**Comp \_ - \_ typsteuerelement**
</dt> <dd> <dl> <dt>



Das Element ist ein Steuerelement.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**Comp- \_ Typ \_ htmldoc**
</dt> <dd> <dl> <dt>



Das Element ist ein HTML-Dokument. Dieses Flag sollte nur verwendet werden, wenn es absolut notwendig ist. Es bewirkt, dass ein HTML-Dokument wörtlich in die Datei "Desktop. htt" eingefügt wird, die zum Steuern des Layouts des Desktops verwendet wird. In den meisten Fällen sollten Sie den * * * * Comp \_ Type \_ Website-Flag * * * * verwenden, um dem Desktop Elemente hinzuzufügen.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**Comp- \_ Typ \_ Max**
</dt> <dd> <dl> <dt>



Der Höchstwert eines Comp \_ Type- \_ \* Flags.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**Bild des Comp- \_ Typs \_**
</dt> <dd> <dl> <dt>



Das Element ist ein Bild.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**Comp \_ Type- \_ Website**
</dt> <dd> <dl> <dt>



Das Element ist eine Website.


</dt> </dl> </dd> <dt>

<span id="COMPONENT_TOP"></span><span id="component_top"></span>**\_obere Komponente**
</dt> <dd> <dl> <dt>



Ein z-Reihen folgen Wert, der angibt, dass sich das Element am oberen Rand befindet.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**wpstyle- \_ Center**
</dt> <dd> <dl> <dt>



Das Hintergrundbild wird zentriert.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**wpstyle \_ Max**
</dt> <dd> <dl> <dt>



Der Höchstwert eines wpstyle- \_ \* Flags.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**wpstyle- \_ Streckung**
</dt> <dd> <dl> <dt>



Das Hintergrundbild wird gestreckt, um den gesamten Bildschirm anzupassen.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**wpstyle- \_ Kachel**
</dt> <dd> <dl> <dt>



Das Hintergrundbild wird gekachelt.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**wpstyle- \_ Spanne**
</dt> <dd> <dl> <dt>



**Windows 8 und** höher: das Hintergrundbild umfasst mehrere Monitore.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
