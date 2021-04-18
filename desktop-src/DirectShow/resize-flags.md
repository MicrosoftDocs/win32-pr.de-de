---
description: Diese Flags geben an, wie eine Videoquelle gerendert wird, wenn ihre Größe nicht den Ausgabe Dimensionen entspricht.
ms.assetid: f740b732-ba05-4fda-aafb-ed04bc3efd33
title: Größenänderung von Flags ("qedit. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RESIZEF_STRETCH
- RESIZEF_CROP
- RESIZEF_PRESERVEASPECTRATIO
- RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 9e2ef2766f7f54fea4fad16fc26242a8c2ee08db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371243"
---
# <a name="resize-flags"></a>Größenänderung von Flags

\[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

Diese Flags geben an, wie eine Videoquelle gerendert wird, wenn ihre Größe nicht den Ausgabe Dimensionen entspricht.



| Konstante/Wert                                                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RESIZEF_STRETCH"></span><span id="resizef_stretch"></span><dl> <dt>**Resizef \_ Stretch**</dt> <dt>0</dt> </dl>                                                                          | Das Bild wird so gestreckt, dass es der Zielframe Größe in beiden Dimensionen entspricht, ohne das Seitenverhältnis beizubehalten.<br/>                                                                                                            |
| <span id="RESIZEF_CROP"></span><span id="resizef_crop"></span><dl> <dt>**Resizef \_ Ernte**</dt> <dt>1</dt> </dl>                                                                                   | Die Größe des Bilds wird nicht geändert. Wenn das Bild kleiner als der Zielframe ist, ist der umgebende Bereich schwarz. Wenn das Bild größer als der Zielframe ist, wird das Bild abgeschnitten.<br/>                                             |
| <span id="RESIZEF_PRESERVEASPECTRATIO"></span><span id="resizef_preserveaspectratio"></span><dl> <dt>**Resizef \_ Preserveaspectratio**</dt> <dt>2</dt> </dl>                                      | Die Größe des Bilds wird so angepasst, dass es an den Zielframe entlang einer Dimension angepasst wird, wobei das Seitenverhältnis beibehalten wird. Wenn das Verhältnis zwischen Breite und Höhe im Bild nicht mit dem Verhältnis im Zielframe identisch ist, wird ein Letterbox-Wert erstellt.<br/> |
| <span id="RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX"></span><span id="resizef_preserveaspectratio_noletterbox"></span><dl> <dt>**Resizef \_ Preserveaspectratio \_ noletterbox**</dt> <dt>3</dt> </dl> | Die Größe des Bilds wird geändert, um den gesamten Zielframe auszufüllen und gleichzeitig das Seitenverhältnis beizubehalten. Anstatt ein Letterbox-Feld zu erstellen, erstellt dieser Modus das Bild entweder entlang der Seite oder über den oberen und unteren Rand.<br/>                 |



## <a name="remarks"></a>Bemerkungen

Die folgenden Abbildungen zeigen die Auswirkungen dieser Flags.

![Größenänderung von Flags](images/stretch14.png)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>"Qedit. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iamtimelinesrc:: getstretchmode**](iamtimelinesrc-getstretchmode.md)
</dt> <dt>

[**Iamtimelinesrc:: setstretchmode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 




