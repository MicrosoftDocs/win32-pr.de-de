---
title: WINBIO_IRIS Konstanten (winbio \_ types. h)
description: Geben Sie die Typen für die Schwert Erkennung an.
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
ms.openlocfilehash: b61e65505b8ef55b0fdc2dc9d8f5312e24856602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477490"
---
# <a name="winbio_iris-constants"></a>Winbio \_ IRIS-Konstanten

Die folgenden Konstanten sind SubType-Werte für den **\_ \_ Subtyp "winbio** ", die zum Angeben der Typen für die Iris-Erkennung jenseits der ANSI-Werte verwendet werden können 379-2004: "IRIS-Bildaustausch Format", die keine linken/rechten Augen Werte definiert:



| Konstante/Wert                                                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <dt> **Winbio \_ IRIS \_ Type \_ Unknown**</dt> <dt>0</dt> </dl>                       | Der Iris-Typ ist unbekannt. <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <dt> **Winbio \_ IRIS \_ left \_ Eye**</dt> <dt>0xF 5</dt> </dl>                               | Der Iris-Typ ist das linke Auge. <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <dt> **Winbio \_ IRIS \_ right \_ Eye**</dt> <dt>0xF 6</dt> </dl>                            | Der Iris-Typ ist das rechte Auge. <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <dt>**Winbio \_ \_Nicht spezifizierte Schwert- \_ POS \_ 01**</dt> <dt>0xF 7</dt> </dl>    | Ein Untertyp, der der ersten Vorlage eines Benutzers zugeordnet ist, wenn nur ein Auge den Kamera Rahmen hat und nicht bestimmt werden kann, ob es sich um den Benutzer Links oder rechts handelt.<br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <dt> **Winbio \_ IRIS \_ nicht angegebene \_ POS \_ 02**</dt> <dt>0xF 8</dt> </dl> | Ein Untertyp, der der zweiten Vorlage eines Benutzers zugeordnet ist, wenn nur ein Auge den Kamera Rahmen hat und nicht bestimmt werden kann, ob es sich um den Benutzer Links oder rechts handelt.<br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <dt> **Winbio \_ IRIS \_ beide \_ Augen**</dt> <dt>0xF 9</dt> </dl>                             | Der Iris-Typ ist beide Augen. <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <dt> **Winbio \_ IRIS \_ entweder \_ Eye**</dt> <dt>0xFA</dt> </dl>                          | Der Typ "Iris" ist entweder "Eye". <br/>                                                                                                                              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



 

 





