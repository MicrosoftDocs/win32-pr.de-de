---
title: WINBIO_BIOMETRIC_TYPE Konstanten (winbio \_ types. h)
description: Standard mäßige biometrische Typen, die vom National Institute of Standards and Technology Information (nistir) 6529-A definiert werden, auch bekannt als "Common biometrische Exchange Formats Framework (CBEFF)"-patronatformat A.
ms.assetid: DCBDB5F9-FF81-44C1-B439-2B8C02483212
topic_type:
- apiref
api_name:
- WINBIO_STANDARD_TYPE_MASK
- WINBIO_NO_TYPE_AVAILABLE
- WINBIO_TYPE_MULTIPLE
- WINBIO_TYPE_FACIAL_FEATURES
- WINBIO_TYPE_VOICE
- WINBIO_TYPE_FINGERPRINT
- WINBIO_TYPE_IRIS
- WINBIO_TYPE_RETINA
- WINBIO_TYPE_HAND_GEOMETRY
- WINBIO_TYPE_SIGNATURE_DYNAMICS
- WINBIO_TYPE_KEYSTROKE_DYNAMICS
- WINBIO_TYPE_LIP_MOVEMENT
- WINBIO_TYPE_THERMAL_FACE_IMAGE
- WINBIO_TYPE_THERMAL_HAND_IMAGE
- WINBIO_TYPE_GAIT
- WINBIO_TYPE_SCENT
- WINBIO_TYPE_DNA
- WINBIO_TYPE_EAR_SHAPE
- WINBIO_TYPE_FINGER_GEOMETRY
- WINBIO_TYPE_PALM_PRINT
- WINBIO_TYPE_VEIN_PATTERN
- WINBIO_TYPE_FOOT_PRINT
- WINBIO_TYPE_OTHER
- WINBIO_TYPE_PASSWORD
- WINBIO_TYPE_ANY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2d2ab5c41a3c2af26312c97a67d1179b50fd759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342433"
---
# <a name="winbio_biometric_type-constants"></a>Winbio- \_ biometrische \_ Typkonstanten

Die folgenden Konstanten stellen die standardmäßigen biometrischen Typen dar, die durch das National Institute of Standards und Technology Information (nistir) 6529-A definiert sind. Diese werden auch als "Common biometrische Exchange Formats Framework" (CBEFF)-patronenformat A bezeichnet. Derzeit wird nur der **winbio- \_ \_ typfingerabdruck** unterstützt.



| Konstante                                                                                                                                                                                                            | BESCHREIBUNG                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_STANDARD_TYPE_MASK"></span><span id="winbio_standard_type_mask"></span><dl> <dt>**winbio \_ - \_ Standardtyp \_ Maske**</dt> </dl>                 | Bitmaske, die den unterstützten Satz von biometrischen Faktoren angibt.<br/>                                                                |
| <span id="WINBIO_NO_TYPE_AVAILABLE"></span><span id="winbio_no_type_available"></span><dl> <dt>**winbio \_ ist \_ nicht \_ verfügbar.**</dt> </dl>                    | Es ist kein biometrischer Typ verfügbar.<br/>                                                                                               |
| <span id="WINBIO_TYPE_MULTIPLE"></span><span id="winbio_type_multiple"></span><dl> <dt>**winbio- \_ Typ \_ Multiple**</dt> </dl>                                 | Es wurden mehrere Typen angegeben.<br/>                                                                                                 |
| <span id="WINBIO_TYPE_FACIAL_FEATURES"></span><span id="winbio_type_facial_features"></span><dl> <dt>**winbio \_ - \_ typgesichts \_ Merkmale**</dt> </dl>           | Gesichts Funktionen werden verwendet, um die Identität einer Person zu bestimmen.<br/>                                                          |
| <span id="WINBIO_TYPE_VOICE"></span><span id="winbio_type_voice"></span><dl> <dt>**winbio \_ - \_ typstimme**</dt> </dl>                                          | Frequenz-und volumemuster in der Stimme einer Person werden verwendet, um die Identität einer Person zu bestimmen.<br/>              |
| <span id="WINBIO_TYPE_FINGERPRINT"></span><span id="winbio_type_fingerprint"></span><dl> <dt>**winbio \_ - \_ typfingerabdruck**</dt> </dl>                        | Fingerabdruck Muster werden verwendet, um die Identität einer Person zu bestimmen.<br/>                                                     |
| <span id="WINBIO_TYPE_IRIS"></span><span id="winbio_type_iris"></span><dl> <dt>**winbio- \_ Typ \_ IRIS**</dt> </dl>                                             | IRIS-Muster werden verwendet, um die Identität einer Person zu bestimmen. Dieser Wert wird ab Windows 10 unterstützt.<br/>            |
| <span id="WINBIO_TYPE_RETINA"></span><span id="winbio_type_retina"></span><dl> <dt>**winbio- \_ Typ \_ RETINA**</dt> </dl>                                       | Mithilfe von Venen Mustern in der Retina wird die Identität einer Person bestimmt.<br/>                                              |
| <span id="WINBIO_TYPE_HAND_GEOMETRY"></span><span id="winbio_type_hand_geometry"></span><dl> <dt>**winbio \_ Type \_ Hand \_ Geometry**</dt> </dl>                 | Die Form einer Hand einer Person wird zur Bestimmung der Identität einer Person verwendet.<br/>                                      |
| <span id="WINBIO_TYPE_SIGNATURE_DYNAMICS"></span><span id="winbio_type_signature_dynamics"></span><dl> <dt>**winbio \_ - \_ Typsignatur \_ Dynamics**</dt> </dl>  | Die Muster von Force, die die Person beim Signieren Ihres Namens verwendet, wird verwendet, um die Identität einer Person zu bestimmen.<br/> |
| <span id="WINBIO_TYPE_KEYSTROKE_DYNAMICS"></span><span id="winbio_type_keystroke_dynamics"></span><dl> <dt>**winbio- \_ Typ \_ KeyStroke \_ Dynamics**</dt> </dl>  | Die Geschwindigkeit und die Fehlermuster bei der Typisierung durch eine Person werden verwendet, um die Identität einer Person zu bestimmen.<br/>                  |
| <span id="WINBIO_TYPE_LIP_MOVEMENT"></span><span id="winbio_type_lip_movement"></span><dl> <dt>**winbio \_ - \_ typlip- \_ Bewegung**</dt> </dl>                    | Die Änderungen in den Lips einer Person, die bei der Sprache auftreten, werden verwendet, um die Identität einer Person zu bestimmen.<br/>      |
| <span id="WINBIO_TYPE_THERMAL_FACE_IMAGE"></span><span id="winbio_type_thermal_face_image"></span><dl> <dt>**Bild der winbio- \_ typgrafik \_ \_ \_**</dt> </dl> | Die Temperatur Muster im Gesicht einer Person werden verwendet, um die Identität einer Person zu bestimmen.<br/>                    |
| <span id="WINBIO_TYPE_THERMAL_HAND_IMAGE"></span><span id="winbio_type_thermal_hand_image"></span><dl> <dt>**Farbbild des winbio- \_ Typs \_ \_ \_**</dt> </dl> | Die Temperatur Muster in der Hand einer Person werden verwendet, um die Identität einer Person zu bestimmen.<br/>                    |
| <span id="WINBIO_TYPE_GAIT"></span><span id="winbio_type_gait"></span><dl> <dt>**winbio \_ Type \_ Gait**</dt> </dl>                                             | Die Muster der Bewegung, die auftreten, wenn die einzelnen Durchgänge zum Bestimmen der Identität einer Person verwendet werden.<br/>            |
| <span id="WINBIO_TYPE_SCENT"></span><span id="winbio_type_scent"></span><dl> <dt>**winbio \_ - \_ typgeruch**</dt> </dl>                                          | Der Duft einer Person wird zur Bestimmung der Identität einer Person verwendet.<br/>                                                |
| <span id="WINBIO_TYPE_DNA"></span><span id="winbio_type_dna"></span><dl> <dt>**winbio \_ \_ -Typ-DNA**</dt> </dl>                                                | Mithilfe von "inoxyribonucleic Acid"-Sequenzen (DNA) wird die Identität einer Person bestimmt.<br/>                                    |
| <span id="WINBIO_TYPE_EAR_SHAPE"></span><span id="winbio_type_ear_shape"></span><dl> <dt>**winbio- \_ Typ ( \_ \_ Ohrform)**</dt> </dl>                             | Die Form eines Ohr der einzelnen wird verwendet, um die Identität einer Person zu bestimmen.<br/>                                     |
| <span id="WINBIO_TYPE_FINGER_GEOMETRY"></span><span id="winbio_type_finger_geometry"></span><dl> <dt>**winbio \_ - \_ \_ typfingergeometrie**</dt> </dl>           | Die Formen der Finger eines einzelnen werden verwendet, um die Identität einer Person zu bestimmen.<br/>                               |
| <span id="WINBIO_TYPE_PALM_PRINT"></span><span id="winbio_type_palm_print"></span><dl> <dt>**winbio- \_ Typ ( \_ Palmen \_ Druck)**</dt> </dl>                          | Die Form der Palme wird zum Bestimmen der Identität einer Person verwendet.<br/>                                                     |
| <span id="WINBIO_TYPE_VEIN_PATTERN"></span><span id="winbio_type_vein_pattern"></span><dl> <dt>**winbio \_ - \_ \_ Typmuster**</dt> </dl>                    | Muster in den Adern unterhalb der Skin der Hand einer einzelnen Person werden verwendet, um die Identität einer Person zu bestimmen.<br/>   |
| <span id="WINBIO_TYPE_FOOT_PRINT"></span><span id="winbio_type_foot_print"></span><dl> <dt>**winbio- \_ Typ- \_ \_ Fußabdruck**</dt> </dl>                          | Die Form des Fußes wird verwendet, um die Identität einer Person zu bestimmen.<br/>                                                     |
| <span id="WINBIO_TYPE_OTHER"></span><span id="winbio_type_other"></span><dl> <dt>**anderer winbio- \_ Typ \_**</dt> </dl>                                          | Die unterstützten biometrischen Daten werden nicht durch die aktuellen Konstanten definiert.<br/>                                                         |
| <span id="WINBIO_TYPE_PASSWORD"></span><span id="winbio_type_password"></span><dl> <dt>**winbio \_ - \_ typkennwort**</dt> </dl>                                 | Kenn Wort Daten werden verwendet, um die Identität einer Person zu bestimmen.<br/>                                                             |
| <span id="WINBIO_TYPE_ANY"></span><span id="winbio_type_any"></span><dl> <dt>**winbio- \_ Typ \_ beliebig**</dt> </dl>                                                | Jeder Datentyp wird verwendet, um die Identität einer einzelnen Person zu bestimmen.<br/>                                                          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                                                                                  |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Konstanten](client-application-constants.md)
</dt> </dl>

 

 





