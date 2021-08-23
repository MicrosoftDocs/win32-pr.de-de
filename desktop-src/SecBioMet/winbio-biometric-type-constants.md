---
title: WINBIO_BIOMETRIC_TYPE Konstanten (Winbio \_ types.h)
description: Vom National Institute of Standards and Technology Information (NISTIR) 6529-A definierte biometrische Standardtypen, auch bekannt als Common Biometric Exchange Formats Framework (CBEFF) –Format A.
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
ms.openlocfilehash: 9c1b6475433d2c0d1432e7501e6cbda46436c5a54fd13d5f254f79b678b3f7bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911069"
---
# <a name="winbio_biometric_type-constants"></a>WINBIO \_ BIOMETRIC \_ TYPE-Konstanten

Die folgenden Konstanten stellen die biometrischen Standardtypen dar, die vom National Institute of Standards and Technology Information (NISTIR) 6529-A definiert werden, auch bekannt als Common Biometric Exchange Formats Framework (CBEFF) Format A. Derzeit wird nur **WINBIO \_ TYPE \_ FINGERPRINT** unterstützt.



| Konstante                                                                                                                                                                                                            | BESCHREIBUNG                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_STANDARD_TYPE_MASK"></span><span id="winbio_standard_type_mask"></span><dl> <dt>**WINBIO \_ STANDARD \_ TYPE \_ MASK**</dt> </dl>                 | Bitmaske, die den unterstützten Satz biometrischer Faktoren angibt.<br/>                                                                |
| <span id="WINBIO_NO_TYPE_AVAILABLE"></span><span id="winbio_no_type_available"></span><dl> <dt>**WINBIO \_ KEIN \_ TYP \_ VERFÜGBAR**</dt> </dl>                    | Es ist kein biometrischer Typ verfügbar.<br/>                                                                                               |
| <span id="WINBIO_TYPE_MULTIPLE"></span><span id="winbio_type_multiple"></span><dl> <dt>**WINBIO \_ TYPE \_ MULTIPLE**</dt> </dl>                                 | Es werden mehrere Typen angegeben.<br/>                                                                                                 |
| <span id="WINBIO_TYPE_FACIAL_FEATURES"></span><span id="winbio_type_facial_features"></span><dl> <dt>**\_GESICHTSMERKMALE DES WINBIO-TYPS \_ \_**</dt> </dl>           | Gesichtsmerkmale werden verwendet, um die Identität einer Person zu bestimmen.<br/>                                                          |
| <span id="WINBIO_TYPE_VOICE"></span><span id="winbio_type_voice"></span><dl> <dt>**WINBIO \_ TYPE \_ VOICE**</dt> </dl>                                          | Häufigkeits- und Lautstärkemuster in der Stimme einer Person werden verwendet, um die Identität einer Person zu bestimmen.<br/>              |
| <span id="WINBIO_TYPE_FINGERPRINT"></span><span id="winbio_type_fingerprint"></span><dl> <dt>**\_WINBIO-FINGERABDRUCKTYP \_**</dt> </dl>                        | Fingerabdruckmuster werden verwendet, um die Identität einer Person zu bestimmen.<br/>                                                     |
| <span id="WINBIO_TYPE_IRIS"></span><span id="winbio_type_iris"></span><dl> <dt>**\_WINBIO-TYP \_ IRIS**</dt> </dl>                                             | Irismuster werden verwendet, um die Identität einer Person zu bestimmen. Dieser Wert wird ab Windows 10 unterstützt.<br/>            |
| <span id="WINBIO_TYPE_RETINA"></span><span id="winbio_type_retina"></span><dl> <dt>**\_WINBIO-TYP \_ NETZNETZ**</dt> </dl>                                       | Vein-Muster in der Netznetzleiste werden verwendet, um die Identität einer Person zu bestimmen.<br/>                                              |
| <span id="WINBIO_TYPE_HAND_GEOMETRY"></span><span id="winbio_type_hand_geometry"></span><dl> <dt>**HANDGEOMETRIE DES \_ WINBIO-TYPS \_ \_**</dt> </dl>                 | Die Form einer Hand einer Person wird verwendet, um die Identität einer Person zu bestimmen.<br/>                                      |
| <span id="WINBIO_TYPE_SIGNATURE_DYNAMICS"></span><span id="winbio_type_signature_dynamics"></span><dl> <dt>**\_WINBIO-TYPSIGNATUR \_ \_ DYNAMICS**</dt> </dl>  | Die Force-Muster, die die Person beim Signieren ihres Namens verwendet, werden verwendet, um die Identität einer Person zu bestimmen.<br/> |
| <span id="WINBIO_TYPE_KEYSTROKE_DYNAMICS"></span><span id="winbio_type_keystroke_dynamics"></span><dl> <dt>**WINBIO \_ TYPE \_ KEYSTROKE \_ DYNAMICS**</dt> </dl>  | Die Geschwindigkeits- und Fehlermuster bei der Eingabe durch eine Person werden verwendet, um die Identität einer Person zu bestimmen.<br/>                  |
| <span id="WINBIO_TYPE_LIP_MOVEMENT"></span><span id="winbio_type_lip_movement"></span><dl> <dt>**WINBIO \_ TYPE \_ LIP \_ MOVEMENT**</dt> </dl>                    | Die Änderungen an den Kanten einer Person, die auftreten, wenn sie sprechen, werden verwendet, um die Identität einer Person zu bestimmen.<br/>      |
| <span id="WINBIO_TYPE_THERMAL_FACE_IMAGE"></span><span id="winbio_type_thermal_face_image"></span><dl> <dt>**BILD DES \_ WINBIO-TYPS \_ \_ "WÄRMEBILD" \_**</dt> </dl> | Die Temperaturmuster im Gesicht einer Person werden verwendet, um die Identität einer Person zu bestimmen.<br/>                    |
| <span id="WINBIO_TYPE_THERMAL_HAND_IMAGE"></span><span id="winbio_type_thermal_hand_image"></span><dl> <dt>**\_WINBIO-TYP \_ : \_ \_ WÄRMEHANDBILD**</dt> </dl> | Die Temperaturmuster in der Hand einer Person werden verwendet, um die Identität einer Person zu bestimmen.<br/>                    |
| <span id="WINBIO_TYPE_GAIT"></span><span id="winbio_type_gait"></span><dl> <dt>**\_WINBIO-TYP \_ GAIT**</dt> </dl>                                             | Die Bewegungsmuster, die auftreten, wenn die einzelnen Durchläufe verwendet werden, um die Identität einer Einzelperson zu bestimmen.<br/>            |
| <span id="WINBIO_TYPE_SCENT"></span><span id="winbio_type_scent"></span><dl> <dt>**\_WINBIO-TYP \_ "FÜSSLING"**</dt> </dl>                                          | Die Identität einer Einzelperson wird verwendet, um die Identität einer Person zu bestimmen.<br/>                                                |
| <span id="WINBIO_TYPE_DNA"></span><span id="winbio_type_dna"></span><dl> <dt>**\_ \_ WINBIO-TYP-DNA**</dt> </dl>                                                | DNA-Sequenzen (Dekreribonucleic Acid) werden verwendet, um die Identität einer Person zu bestimmen.<br/>                                    |
| <span id="WINBIO_TYPE_EAR_SHAPE"></span><span id="winbio_type_ear_shape"></span><dl> <dt>**FORM \_ DES \_ WINBIO-TYPS \_ "EAR"**</dt> </dl>                             | Die Form eines Gehörs der Person wird verwendet, um die Identität einer Person zu bestimmen.<br/>                                     |
| <span id="WINBIO_TYPE_FINGER_GEOMETRY"></span><span id="winbio_type_finger_geometry"></span><dl> <dt>**\_ \_ WINBIO-TYPFINGERGEOMETRIE \_**</dt> </dl>           | Die Formen der Finger einer Einzelperson werden verwendet, um die Identität einer Person zu bestimmen.<br/>                               |
| <span id="WINBIO_TYPE_PALM_PRINT"></span><span id="winbio_type_palm_print"></span><dl> <dt>**WINBIO \_ TYPE \_ PALM \_ PRINT**</dt> </dl>                          | Die Form der Handfläche wird verwendet, um die Identität einer Person zu bestimmen.<br/>                                                     |
| <span id="WINBIO_TYPE_VEIN_PATTERN"></span><span id="winbio_type_vein_pattern"></span><dl> <dt>**\_ \_ WINBIO-TYP-VEIN-MUSTER \_**</dt> </dl>                    | Muster in den Adern unterhalb der Skin der Hand einer Person werden verwendet, um die Identität einer Person zu bestimmen.<br/>   |
| <span id="WINBIO_TYPE_FOOT_PRINT"></span><span id="winbio_type_foot_print"></span><dl> <dt>**\_WINBIO-TYP \_ : \_ FUßDRUCK**</dt> </dl>                          | Die Form des Fußes wird verwendet, um die Identität einer Person zu bestimmen.<br/>                                                     |
| <span id="WINBIO_TYPE_OTHER"></span><span id="winbio_type_other"></span><dl> <dt>**WINBIO \_ TYPE \_ OTHER**</dt> </dl>                                          | Die unterstützten biometrischen Daten werden nicht durch die aktuellen Konstanten definiert.<br/>                                                         |
| <span id="WINBIO_TYPE_PASSWORD"></span><span id="winbio_type_password"></span><dl> <dt>**\_ \_ WINBIO-TYPKENNWORT**</dt> </dl>                                 | Kennwortdaten werden verwendet, um die Identität einer Person zu bestimmen.<br/>                                                             |
| <span id="WINBIO_TYPE_ANY"></span><span id="winbio_type_any"></span><dl> <dt>**WINBIO \_ TYPE \_ ANY**</dt> </dl>                                                | Jede Art von Daten wird verwendet, um die Identität einer Einzelperson zu bestimmen.<br/>                                                          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                                                                                  |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h für Clientanwendungen oder Winbio \_ adapters.h für Adapter einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungskonstanten](client-application-constants.md)
</dt> </dl>

 

 





