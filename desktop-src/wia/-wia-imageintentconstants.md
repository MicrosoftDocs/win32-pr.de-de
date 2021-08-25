---
description: Absichtskonstanten für Bilder geben an, welche Art von Daten das Bild darstellen soll.
ms.assetid: 171228d9-a619-49aa-964e-f72a7f294a9d
title: Bildabsichtkonstanten (Wiadef.h)
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
ms.openlocfilehash: 78130128a26057ed521512dd21acc5a1bd7e98c47ed689eaabc250a972c2a003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814120"
---
# <a name="image-intent-constants"></a>Bildabsichtkonstanten

Absichtskonstanten für Bilder geben an, welche Art von Daten das Bild darstellen soll. Die [**WIA \_ IPS \_ CUR INTENT-Überprüfungseigenschaft \_**](-wia-wiaitempropscanneritem.md) verwendet diese Flags. Um eine Absicht bereitzustellen, kombinieren Sie ein beabsichtigtes Imagetypflag mit einem beabsichtigten Größen-/Qualitätsflag mithilfe des OR-Operators. WIA \_ INTENT NONE sollte nicht mit anderen \_ Flags kombiniert werden. Beachten Sie, dass ein Bild nicht sowohl grau als auch farblich sein darf.

Im Folgenden sind gültige Bildabsichtkonstanten dargestellt:



| Beabsichtigte Imagetypflags           | BESCHREIBUNG                                  |
|-------------------------------------|----------------------------------------------|
| WIA \_ INTENT \_ NONE                   | Standardwert. Voreingestellte Eigenschaften dürfen nicht voreingestellt werden. |
| WIA \_ INTENT \_ IMAGE \_ TYPE \_ COLOR     | Voreingestellte Eigenschaften für Farbinhalte.         |
| WIA \_ INTENT \_ IMAGE \_ TYPE \_ GRAYSCALE | Voreingestellte Eigenschaften für Graustufeninhalte.     |
| WIA \_ INTENT \_ IMAGE \_ TYPE \_ TEXT      | Voreingestellte Eigenschaften für Textinhalt.          |
| WIA \_ INTENT \_ IMAGE \_ TYPE \_ MASK      | Maskierung für alle Bildtypflags.        |



 



| Beabsichtigte Imagegröße/Qualitätsflags | BESCHREIBUNG                                  |
|-----------------------------------|----------------------------------------------|
| WIA \_ INTENT MINIMIZE SIZE (WIA-ABSICHT MINIMIEREN DER \_ \_ GRÖßE)       | Voreingestellte Eigenschaften zum Minimieren der Bildgröße.    |
| \_WIA-ABSICHT: \_ MAXIMIEREN DER \_ QUALITÄT    | Voreingestellte Eigenschaften zum Maximieren der Imagequalität. |
| WIA \_ INTENT \_ SIZE \_ MASK           | Maskierung für alle Größen-/Qualitätsflags.      |
| WIA \_ INTENT \_ BEST \_ PREVIEW        | Gibt die Vorschau der besten Qualität an.          |



 

Die folgende Liste zeigt den C/C++-Konstantennamen gefolgt von dem entsprechenden Namen in Klammern, die bei der Skripterstellung verwendet werden. Die Skriptnamen stammen vom WiaIntent-Enumerationstyp. Beachten Sie, dass nicht alle Konstanten über das Skript verfügbar sind.



| Konstante/Wert                                                                                                                                                                                                                                                                         | BESCHREIBUNG                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| <span id="WIA_INTENT_IMAGE_TYPE_COLOR"></span><span id="wia_intent_image_type_color"></span><dl> <dt>**WIA \_ 0X00000001 DES \_ ABSICHTSBILDTYPS \_ \_**</dt> <dt></dt> </dl>             | Voreingestellte Eigenschaften für Farbinhalte.<br/>         |
| <span id="WIA_INTENT_IMAGE_TYPE_GRAYSCALE"></span><span id="wia_intent_image_type_grayscale"></span><dl> <dt>**WIA \_ INTENT \_ IMAGE \_ TYPE \_ GRAYSCALE**</dt> <dt>0x00000002</dt> </dl> | Voreingestellte Eigenschaften für Graustufeninhalte.<br/>     |
| <span id="WIA_INTENT_IMAGE_TYPE_TEXT"></span><span id="wia_intent_image_type_text"></span><dl> <dt>**WIA \_ 0X00000004 DES \_ \_ ABSICHTSBILDTYPS \_**</dt> <dt></dt> </dl>                | Voreingestellte Eigenschaften für Textinhalt.<br/>          |
| <span id="WIA_INTENT_MINIMIZE_SIZE"></span><span id="wia_intent_minimize_size"></span><dl> <dt>**WIA \_ INTENT \_ MINIMIZE \_ SIZE**</dt> <dt>0x00010000</dt> </dl>                       | Voreingestellte Eigenschaften zum Minimieren der Bildgröße.<br/>    |
| <span id="WIA_INTENT_MAXIMIZE_QUALITY"></span><span id="wia_intent_maximize_quality"></span><dl> <dt>**WIA \_ INTENT \_ MAXIMIZE \_ QUALITY**</dt> <dt>0x00020000</dt> </dl>              | Voreingestellte Eigenschaften zum Maximieren der Imagequalität.<br/> |
| <span id="WIA_INTENT_BEST_PREVIEW"></span><span id="wia_intent_best_preview"></span><dl> <dt>**WIA \_ \_INTENT BEST \_ PREVIEW**</dt> <dt>0x00040000</dt> </dl>                          | Gibt die Vorschau der besten Qualität an.<br/>          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 




