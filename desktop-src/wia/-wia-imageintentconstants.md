---
description: Bild Intent-Konstanten geben an, welche Art von Daten das Image darstellen soll.
ms.assetid: 171228d9-a619-49aa-964e-f72a7f294a9d
title: Bild Intent Konstanten (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_INTENT_IMAGE_TYPE_COLOR
- WIA_INTENT_IMAGE_TYPE_GRAYSCALE
- WIA_INTENT_IMAGE_TYPE_TEXT
- WIA_INTENT_MINIMIZE_SIZE
- WIA_INTENT_MAXIMIZE_QUALITY
- WIA_INTENT_BEST_PREVIEW
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f35c1f7436c8cc5110215a6ccf0383960ec3fb87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959091"
---
# <a name="image-intent-constants"></a>Bild Intent-Konstanten

Bild Intent-Konstanten geben an, welche Art von Daten das Image darstellen soll. Die [**\_ \_ cur \_ INTENT**](-wia-wiaitempropscanneritem.md) Scanner-Eigenschaft für WIA-IPS verwendet diese Flags. Um eine Absicht bereitzustellen, kombinieren Sie ein beabsichtigtes Abbildtyp Kennzeichen mit einem vorgesehenen size/Quality-Flag, indem Sie den or-Operator verwenden. Die WIA- \_ Absicht \_ darf nicht mit anderen Flags kombiniert werden. Beachten Sie, dass ein Bild nicht gleichzeitig Graustufen und Farben sein darf.

Im folgenden finden Sie gültige Abbild Intent-Konstanten:



| Vorgesehene Abbildtyp-Flags           | BESCHREIBUNG                                  |
|-------------------------------------|----------------------------------------------|
| nicht \_ beabsichtigt \_                   | Standardwert. Verwenden Sie keine Eigenschaften. |
| WIA \_ INTENT \_ Image \_ Type \_ Color     | Vordefinierte Eigenschaften für Farb Inhalt.         |
| WIA \_ INTENT \_ Image \_ Type \_ Grayscale | Voreingestellte Eigenschaften für Graustufen Inhalt.     |
| WIA \_ INTENT \_ Image \_ Type \_ Text      | Voreingestellte Eigenschaften für Text Inhalt.          |
| WIA \_ INTENT \_ Image \_ Type \_ Mask      | Maske für alle Bildtyp-Flags.        |



 



| Vorgesehene Image Größe/qualitätsflags | BESCHREIBUNG                                  |
|-----------------------------------|----------------------------------------------|
| \_ \_ Minimieren der \_ Größe       | Voreinstellungs Eigenschaften zum Minimieren der Bildgröße.    |
| WIA- \_ Absicht \_ Maximieren der \_ Qualität    | Voreingestellte Eigenschaften zum Maximieren der Bildqualität. |
| WIA \_ INTENT \_ size \_ Mask           | Maske für alle Größen-/qualitätsflags.      |
| \_ \_ beste \_ Vorschau für WIA        | Gibt die Vorschau der optimalen Qualität an.          |



 

In der folgenden Liste wird der C/C++-Konstantenname gefolgt vom entsprechenden Namen in Klammern angezeigt, der bei der Skripterstellung verwendet wird. Die Skriptnamen stammen aus dem wiaintent-enumerierten Typ. Beachten Sie, dass nicht alle Konstanten über Skripts verfügbar sind.



| Konstante/Wert                                                                                                                                                                                                                                                                         | BESCHREIBUNG                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| <span id="WIA_INTENT_IMAGE_TYPE_COLOR"></span><span id="wia_intent_image_type_color"></span><dl> <dt>**WIA \_ INTENT \_ Image \_ Type \_ Color**</dt> <dt>0x00000001</dt> </dl>             | Vordefinierte Eigenschaften für Farb Inhalt.<br/>         |
| <span id="WIA_INTENT_IMAGE_TYPE_GRAYSCALE"></span><span id="wia_intent_image_type_grayscale"></span><dl> <dt>**WIA \_ INTENT \_ Image \_ Type \_ Grayscale**</dt> <dt>0x00000002</dt> </dl> | Voreingestellte Eigenschaften für Graustufen Inhalt.<br/>     |
| <span id="WIA_INTENT_IMAGE_TYPE_TEXT"></span><span id="wia_intent_image_type_text"></span><dl> <dt>**WIA \_ INTENT \_ Image \_ Type \_ Text**</dt> <dt>0x00000004</dt> </dl>                | Voreingestellte Eigenschaften für Text Inhalt.<br/>          |
| <span id="WIA_INTENT_MINIMIZE_SIZE"></span><span id="wia_intent_minimize_size"></span><dl> <dt>**WIA \_ Beabsichtigte \_ Minimierung der \_ Größe**</dt> <dt>0x00010000 bis</dt> </dl>                       | Voreinstellungs Eigenschaften zum Minimieren der Bildgröße.<br/>    |
| <span id="WIA_INTENT_MAXIMIZE_QUALITY"></span><span id="wia_intent_maximize_quality"></span><dl> <dt>**WIA \_ Absicht \_ Maximieren der \_ Qualität**</dt> <dt>0x00020000</dt> </dl>              | Voreingestellte Eigenschaften zum Maximieren der Bildqualität.<br/> |
| <span id="WIA_INTENT_BEST_PREVIEW"></span><span id="wia_intent_best_preview"></span><dl> <dt>**WIA \_ Beabsichtigte \_ beste \_ Vorschau**</dt> <dt>0x00040000</dt> </dl>                          | Gibt die Vorschau der optimalen Qualität an.<br/>          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




