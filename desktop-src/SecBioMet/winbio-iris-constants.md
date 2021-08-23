---
title: WINBIO_IRIS Konstanten (Winbio \_ types.h)
description: Geben Sie die Typen für die Iriserkennung an.
ms.assetid: B1A594E3-6DEA-4071-B40F-569B8094E801
topic_type:
- apiref
api_name:
- WINBIO_IRIS_TYPE_UNKNOWN
- WINBIO_IRIS_LEFT_EYE
- WINBIO_IRIS_RIGHT_EYE
- WINBIO_IRIS_UNSPECIFIED_POS_01
- WINBIO_IRIS_UNSPECIFIED_POS_02
- WINBIO_IRIS_BOTH_EYES
- WINBIO_IRIS_EITHER_EYE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd528bc9a902379591fb6d9587fa66bda9df50ad74cb5e5723f8646a53609a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909959"
---
# <a name="winbio_iris-constants"></a>\_WINBIO-IRIS-Konstanten

Die folgenden Konstanten sind **WINBIO \_ BIOMETRIC \_ SUBTYPE-Werte,** die verwendet werden können, um die Typen für die Iriserkennung über ANSI INCITS 379-2004 hinaus anzugeben: "Iris Image Interchange Format", das keine Werte für linke/rechte Augen definiert:



| Konstante/Wert                                                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <dt> **WINBIO \_ IRIS \_ TYPE \_ UNKNOWN**</dt> <dt>0</dt> </dl>                       | Der Iristyp ist unbekannt. <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <dt> **WINBIO \_ IRIS LEFT EYE \_ \_ 0XF5**</dt> <dt></dt> </dl>                               | Der Iristyp ist das linke Auge. <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <dt> **WINBIO \_ IRIS RIGHT EYE \_ \_ 0xF6**</dt> <dt></dt> </dl>                            | Der Iristyp ist das rechte Auge. <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <dt>**WINBIO \_ IRIS \_ UNSPECIFIED \_ POS \_ 01**</dt> <dt>0xF7</dt> </dl>    | Untertyp, der der ersten Vorlage eines Benutzers zugeordnet ist, wenn nur ein Auge ein Kamerarahmen ist und nicht bestimmt werden kann, ob es sich um das linke oder rechte Auge des Benutzers handelt.<br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <dt> **WINBIO \_ IRIS \_ UNPECIFIED \_ POS \_ 02**</dt> <dt>0xF8</dt> </dl> | Untertyp, der der zweiten Vorlage eines Benutzers zugeordnet ist, wenn nur ein Auge ein Kamerarahmen ist und nicht bestimmt werden kann, ob es sich um das linke oder rechte Auge des Benutzers handelt.<br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <dt> **WINBIO \_ IRIS BEIDE AUGEN \_ \_ 0XF9**</dt> <dt></dt> </dl>                             | Der Iristyp ist beide Augen. <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <dt> **WINBIO \_ IRIS \_ EITHER \_ EYE**</dt> <dt>0xFA</dt> </dl>                          | Der Iristyp ist entweder ein Auge. <br/>                                                                                                                              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (einschließlich Winbio.h)</dt> </dl> |



 

 





