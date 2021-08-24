---
description: Diese Flags geben an, wie eine Videoquelle gerendert wird, wenn ihre Größe nicht mit den Ausgabedimensionen übereinstimmen soll.
ms.assetid: f740b732-ba05-4fda-aafb-ed04bc3efd33
title: Größenflags ändern (Qedit.h)
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
ms.openlocfilehash: c38f4b1913eb7676832374e57e4d65e14dc87831c13f3cdb0de96edf9b83ebec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747105"
---
# <a name="resize-flags"></a>Ändern der Größe von Flags

\[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

Diese Flags geben an, wie eine Videoquelle gerendert wird, wenn ihre Größe nicht mit den Ausgabedimensionen übereinstimmen soll.



| Konstante/Wert                                                                                                                                                                                                                                                                                      | Beschreibung                                                                                                                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RESIZEF_STRETCH"></span><span id="resizef_stretch"></span><dl> <dt>**RESIZEF \_ STRETCH**</dt> <dt>0</dt> </dl>                                                                          | Das Bild wird so gestreckt, dass es in beiden Dimensionen an die Zielrahmengröße passt, ohne das Seitenverhältnis zu erhalten.<br/>                                                                                                            |
| <span id="RESIZEF_CROP"></span><span id="resizef_crop"></span><dl> <dt>**RESIZEF \_ CROP**</dt> <dt>1</dt> </dl>                                                                                   | Die Größe des Bilds wird nicht geändert. Wenn das Bild kleiner als der Zielrahmen ist, ist die Umgebende schwarz. Wenn das Bild größer als der Zielrahmen ist, wird das Bild zugeschnitten.<br/>                                             |
| <span id="RESIZEF_PRESERVEASPECTRATIO"></span><span id="resizef_preserveaspectratio"></span><dl> <dt>**RESIZEF \_ PRESERVEASPECTRATIO**</dt> <dt>2</dt> </dl>                                      | Die Größe des Bilds wird an den Zielrahmen entlang einer Dimension geändert, wobei das Seitenverhältnis beibehalten wird. Wenn das Verhältnis von Breite zu Höhe im Bild nicht mit dem Verhältnis im Zielrahmen überein passt, wird ein Letterbox-Zeichenfeld erstellt.<br/> |
| <span id="RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX"></span><span id="resizef_preserveaspectratio_noletterbox"></span><dl> <dt>**RESIZEF \_ PRESERVEASPECTRATIO \_ NOLETTERBOX**</dt> <dt>3</dt> </dl> | Die Größe des Bilds wird geändert, um den gesamten Zielrahmen zu füllen und gleichzeitig das Seitenverhältnis zu erhalten. Anstatt einen Buchstabenkasten zu erstellen, wird das Bild in diesem Modus entweder entlang der Seiten oder über den oberen und unteren Rand geschaltet.<br/>                 |



## <a name="remarks"></a>Hinweise

Die folgenden Abbildungen zeigen die Auswirkungen dieser Flags.

![Ändern der Größe von Flags](images/stretch14.png)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMTimelineSrc::GetStretchMode**](iamtimelinesrc-getstretchmode.md)
</dt> <dt>

[**IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 




