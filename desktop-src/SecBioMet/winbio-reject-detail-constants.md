---
title: WINBIO_REJECT_DETAIL Konstanten (Winbio \_ types.h)
description: Geben Sie den Grund an, warum ein biometrischer Fingerabdruckerfassungs- oder Identifikationsvorgang nicht erfolgreich war.
ms.assetid: b1ae4e65-9e53-42dd-99ba-1910b72688dd
topic_type:
- apiref
api_name:
- WINBIO_FP_TOO_HIGH
- WINBIO_FP_TOO_LOW
- WINBIO_FP_TOO_LEFT
- WINBIO_FP_TOO_RIGHT
- WINBIO_FP_TOO_FAST
- WINBIO_FP_TOO_SLOW
- WINBIO_FP_POOR_QUALITY
- WINBIO_FP_TOO_SKEWED
- WINBIO_FP_TOO_SHORT
- WINBIO_FP_MERGE_FAILURE
- WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK
- WINBIO_REJECT_DETAIL_POSITION_MASK
- WINBIO_REJECT_DETAIL_REASON_MASK
- WINBIO_IRIS_POOR_QUALITY
- WINBIO_IRIS_TOO_BRIGHT
- WINBIO_IRIS_TOO_DARK
- WINBIO_IRIS_SPOOF_DETECTED
- WINBIO_IRIS_TOO_SKEWED
- WINBIO_IRIS_TOO_CLOSED
- WINBIO_IRIS_GLARE
- WINBIO_IRIS_DIRTY_LENS
- WINBIO_IRIS_POOR_FOCUS
- WINBIO_IRIS_WRONG_ORIENTATION
- WINBIO_IRIS_TOO_HIGH
- WINBIO_IRIS_TOO_LOW
- WINBIO_IRIS_TOO_LEFT
- WINBIO_IRIS_TOO_RIGHT
- WINBIO_IRIS_TOO_NEAR
- WINBIO_IRIS_TOO_FAR
- WINBIO_FACE_POOR_QUALITY
- WINBIO_FACE_TOO_BRIGHT
- WINBIO_FACE_TOO_DARK
- WINBIO_FACE_SPOOF_DETECTED
- WINBIO_FACE_AMBIGUOUS_TARGET
- WINBIO_FACE_EYES_OCCLUDED
- WINBIO_FACE_WRONG_ORIENTATION
- WINBIO_FACE_TOO_HIGH
- WINBIO_FACE_TOO_LOW
- WINBIO_FACE_TOO_LEFT
- WINBIO_FACE_TOO_RIGHT
- WINBIO_FACE_TOO_NEAR
- WINBIO_FACE_TOO_FAR
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad5ac7a2f96555aa8ccfb305c66061ba4e0ffd468f18a1a93be215c367f034be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909348"
---
# <a name="winbio_reject_detail-constants"></a>WINBIO \_ REJECT \_ DETAIL-Konstanten

Die folgenden Konstanten können verwendet werden, um anzugeben, warum ein biometrischer Fingerabdruckerfassungs- oder Identifikationsvorgang nicht erfolgreich war.



| Konstante                                                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FP_TOO_HIGH"></span><span id="winbio_fp_too_high"></span><dl> <dt>**WINBIO \_ FP \_ ZU \_ HOCH**</dt> </dl>                                                                  | Der Fingerscan begann zu hoch am Finger.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_LOW"></span><span id="winbio_fp_too_low"></span><dl> <dt>**WINBIO \_ FP \_ ZU \_ NIEDRIG**</dt> </dl>                                                                     | Der Fingerscan begann zu niedrig am Finger.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_LEFT"></span><span id="winbio_fp_too_left"></span><dl> <dt>**WINBIO \_ FP \_ TOO \_ LEFT**</dt> </dl>                                                                  | Der Finger war beim Scannen zu weit links.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_RIGHT"></span><span id="winbio_fp_too_right"></span><dl> <dt>**WINBIO \_ FP \_ TOO \_ RIGHT**</dt> </dl>                                                               | Der Finger war beim Scannen zu weit rechts.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_FAST"></span><span id="winbio_fp_too_fast"></span><dl> <dt>**WINBIO \_ FP \_ TOO \_ FAST**</dt> </dl>                                                                  | Der Finger wurde zu schnell auf den Sensor gewischt.<br/>                                                                                                                                                                                                                                       |
| <span id="WINBIO_FP_TOO_SLOW"></span><span id="winbio_fp_too_slow"></span><dl> <dt>**WINBIO \_ FP \_ ZU \_ LANGSAM**</dt> </dl>                                                                  | Der Finger wurde auf dem Sensor zu langsam gewischt.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_FP_POOR_QUALITY"></span><span id="winbio_fp_poor_quality"></span><dl> <dt>**WINBIO \_ \_ FP: SCHLECHTE \_ QUALITÄT**</dt> </dl>                                                      | Die Scanqualität war zu schlecht.<br/>                                                                                                                                                                                                                                                         |
| <span id="WINBIO_FP_TOO_SKEWED"></span><span id="winbio_fp_too_skewed"></span><dl> <dt>**WINBIO \_ FP \_ TOO \_ SKEWED**</dt> </dl>                                                            | Der Finger wurde nicht direkt über den Sensor übergeben.<br/>                                                                                                                                                                                                                                    |
| <span id="WINBIO_FP_TOO_SHORT"></span><span id="winbio_fp_too_short"></span><dl> <dt>**WINBIO \_ FP \_ ZU \_ KURZ**</dt> </dl>                                                               | Es wurde nicht genügend Finger gescannt.<br/>                                                                                                                                                                                                                                                  |
| <span id="WINBIO_FP_MERGE_FAILURE"></span><span id="winbio_fp_merge_failure"></span><dl> <dt>**WINBIO \_ \_ \_ FP-MERGEFEHLER**</dt> </dl>                                                   | Die Fingerabdruckerfassungen konnten nicht kombiniert werden.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK____"></span><span id="winbio_reject_detail_anti_spoof_mask____"></span><dl> <dt>**WINBIO \_ ANTIS \_ \_ SPOOFMASKE "DETAILS \_ \_ ABLEHNEN"**</dt> </dl> | Diese Maske deckt die oberen 8 Bits des Ablehnungsdetailwerts ab, in denen sich das Verhalten des Proof of Liveness befindet. Dieser Wert wird ab Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_POSITION_MASK______"></span><span id="winbio_reject_detail_position_mask______"></span><dl> <dt>**WINBIO \_ \_ \_ ABLEHNUNGSDETAILPOSITIONSMASKE \_**</dt> </dl>    | Diese Maske deckt den Bereich der Bits ab, die Positionsfehlern beibezieht. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                                                         |
| <span id="WINBIO_REJECT_DETAIL_REASON_MASK"></span><span id="winbio_reject_detail_reason_mask"></span><dl> <dt>**WINBIO \_ REJECT \_ DETAIL \_ REASON \_ MASK**</dt> </dl>                       | Diese Maske deckt die unteren 16 Bits ab, in denen sich der aufzählte Grund für die Ablehnung befindet. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                           |
| <span id="WINBIO_IRIS_POOR_QUALITY"></span><span id="winbio_iris_poor_quality"></span><dl> <dt>**WINBIO \_ IRIS \_ SCHLECHTE \_ QUALITÄT**</dt> </dl>                                                | Die Bedingungen haben dazu führte, dass die Kamera ein schlechtes Bild erfasste. Weisen Sie den Benutzer an, den Sensor zu bereinigt und erneut zu überprüfen. Dieser Wert wird ab Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_IRIS_TOO_BRIGHT"></span><span id="winbio_iris_too_bright"></span><dl> <dt>**WINBIO \_ IRIS \_ ZU \_ HELL**</dt> </dl>                                                      | Das Bild enthält zu viel Umgebungslicht, um eine gute Übereinstimmung zu erhalten. Weisen Sie den Benutzer an, sicherzustellen, dass keine andere helle Lichtquelle angezeigt wird. Dieser Wert wird ab Windows 10.<br/>                                                                                        |
| <span id="WINBIO_IRIS_TOO_DARK"></span><span id="winbio_iris_too_dark"></span><dl> <dt>**WINBIO \_ IRIS \_ TOO \_ DARK**</dt> </dl>                                                            | Das Bild ist zu dunkel, um eine gute Übereinstimmung zu erhalten. Weisen Sie den Benutzer an, sicherzustellen, dass seine Schwertlilien nicht durch Elemente wie eine Brille, dunkle Brille oder farbige Kontakte verdeckt werden. Dieser Wert wird ab Windows 10.<br/>                                                                     |
| <span id="WINBIO_IRIS_SPOOF_DETECTED"></span><span id="winbio_iris_spoof_detected"></span><dl> <dt>**WINBIO \_ IRIS \_ SPOOF \_ ERKANNT**</dt> </dl>                                          | Die Erkennungskomponente geht davon aus, dass die Iris nicht live ist, sondern von einem wiedergegebenen Videofeed, einem Foto oder einem 3D-3D-3D-3D-Bild stammt. Dieser Wert wird ab Windows 10.<br/>                                                                                                   |
| <span id="WINBIO_IRIS_TOO_SKEWED"></span><span id="winbio_iris_too_skewed"></span><dl> <dt>**WINBIO \_ IRIS \_ TOO \_ SKEWED**</dt> </dl>                                                      | Der Benutzer sieht die Kamera nicht direkt an. Weisen Sie den Benutzer an, die Kamera direkt zu betrachten und erneut zu scannen. Dieser Wert wird ab Windows 10.<br/>                                                                                                                       |
| <span id="WINBIO_IRIS_TOO_CLOSED"></span><span id="winbio_iris_too_closed"></span><dl> <dt>**WINBIO \_ IRIS \_ ZU \_ GESCHLOSSEN**</dt> </dl>                                                      | Die Augenlider des Benutzers verschleieren die Iris. Weisen Sie den Benutzer an, seine Augen ein wenig mehr zu öffnen und erneut zu scannen. Dieser Wert wird ab Windows 10.<br/>                                                                                                                          |
| <span id="WINBIO_IRIS_GLARE"></span><span id="winbio_iris_glare"></span><dl> <dt>**WINBIO \_ IRIS \_ IRISRE**</dt> </dl>                                                                      | Das Bild enthält eine Brille. Weisen Sie den Benutzer an, seine Brille zu entfernen und erneut zu scannen. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                               |
| <span id="WINBIO_IRIS_DIRTY_LENS"></span><span id="winbio_iris_dirty_lens"></span><dl> <dt>**WINBIO \_ IRIS \_ DIRTY \_ LENS**</dt> </dl>                                                      | Das Kameraobjekt war verfeckt. Weisen Sie den Benutzer an, das Ziel zu bereinigt und erneut zu überprüfen. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                                         |
| <span id="WINBIO_IRIS_POOR_FOCUS"></span><span id="winbio_iris_poor_focus"></span><dl> <dt>**WINBIO \_ IRIS \_ POOR \_ FOCUS**</dt> </dl>                                                      | Diese Iris liegt nicht im Fokus. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                                                                                             |
| <span id="WINBIO_IRIS_WRONG_ORIENTATION"></span><span id="winbio_iris_wrong_orientation"></span><dl> <dt>**WINBIO \_ IRIS \_ WRONG \_ ORIENTATION**</dt> </dl>                                 | Die Kameraausrichtung passt nicht zur obligatorischen Ausrichtung, die die [**WINBIO \_ EXTENDED SENSOR \_ \_ INFO-Struktur**](winbio-extended-sensor-info.md) angibt. Weisen Sie den Benutzer an, die Kameraausrichtung zu ändern und erneut zu scannen. Dieser Wert wird ab Windows 10.<br/> |
| <span id="WINBIO_IRIS_TOO_HIGH"></span><span id="winbio_iris_too_high"></span><dl> <dt>**WINBIO \_ IRIS \_ ZU \_ HOCH**</dt> </dl>                                                            | Die Iris wird nach oben gerichtet. Weisen Sie den Benutzer an, ein wenig nach unten zu suchen und erneut zu überprüfen. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LOW"></span><span id="winbio_iris_too_low"></span><dl> <dt>**WINBIO \_ IRIS \_ ZU \_ NIEDRIG**</dt> </dl>                                                               | Die Iris ist nach unten gerichtet. Weisen Sie den Benutzer an, etwas nach oben zu suchen und erneut zu überprüfen. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LEFT"></span><span id="winbio_iris_too_left"></span><dl> <dt>**WINBIO \_ IRIS \_ TOO \_ LEFT**</dt> </dl>                                                            | Die Iris ist zu weit nach links. Weisen Sie den Benutzer an, etwas mehr nach rechts zu suchen und die Überprüfung erneut zu starten. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_RIGHT"></span><span id="winbio_iris_too_right"></span><dl> <dt>**WINBIO \_ IRIS \_ TOO \_ RIGHT**</dt> </dl>                                                         | Die Iris ist zu weit nach rechts. Weisen Sie den Benutzer an, etwas mehr nach links zu suchen und die Überprüfung erneut zu starten. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_NEAR"></span><span id="winbio_iris_too_near"></span><dl> <dt>**WINBIO \_ IRIS \_ ZU \_ NAH**</dt> </dl>                                                            | Die Iris ist zu nah an der Kamera. Weisen Sie den Benutzer an, sich etwas weiter zu bewegen und erneut zu überprüfen. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                   |
| <span id="WINBIO_IRIS_TOO_FAR"></span><span id="winbio_iris_too_far"></span><dl> <dt>**WINBIO \_ IRIS \_ ZU \_ WEIT**</dt> </dl>                                                               | Die Iris ist zu weit von der Kamera entfernt. Weisen Sie den Benutzer an, sich etwas näher zu bewegen und die Überprüfung erneut zu starten. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                         |
| <span id="WINBIO_FACE_POOR_QUALITY"></span><span id="winbio_face_poor_quality"></span><dl> <dt>**\_WINBIO: \_ SCHLECHTE \_ QUALITÄT**</dt> </dl>                                                | Die Bedingungen haben dazu führte, dass die Kamera ein schlechtes Bild erfasste. Weisen Sie den Benutzer an, den Sensor zu bereinigt und erneut zu überprüfen. Dieser Wert wird ab Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_FACE_TOO_BRIGHT"></span><span id="winbio_face_too_bright"></span><dl> <dt>**\_WINBIO-GESICHT \_ ZU \_ HELL**</dt> </dl>                                                      | Das Bild enthält zu viel Umgebungslicht, um eine gute Übereinstimmung zu erhalten. Weisen Sie den Benutzer an, sicherzustellen, dass keine andere helle Lichtquelle angezeigt wird. Dieser Wert wird ab Windows 10.<br/>                                                                                        |
| <span id="WINBIO_FACE_TOO_DARK"></span><span id="winbio_face_too_dark"></span><dl> <dt>**\_WINBIO-GESICHT \_ ZU \_ DUNKEL**</dt> </dl>                                                            | Das Bild ist zu dunkel, um eine gute Übereinstimmung zu erhalten. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                                                                             |
| <span id="WINBIO_FACE_SPOOF_DETECTED"></span><span id="winbio_face_spoof_detected"></span><dl> <dt>**\_WINBIO-GESICHTSS \_ SPOOF \_ ERKANNT**</dt> </dl>                                          | Die Erkennungskomponente geht davon aus, dass das Gesicht nicht live ist, sondern von einem wiedergegebenen Videofeed, einem Foto oder einem 3D-3D-Bild stammt. Dieser Wert wird ab Windows 10.<br/>                                                                                                   |
| <span id="WINBIO_FACE_AMBIGUOUS_TARGET"></span><span id="winbio_face_ambiguous_target"></span><dl> <dt>**\_MEHRDEUTIGES \_ WINBIO-ZIEL FÜR \_ DIE GESICHTSERKENNUNG**</dt> </dl>                                    | Zwei oder mehr Gesichter überlappen sich im Kamerarahmen. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                                                                     |
| <span id="WINBIO_FACE_EYES_OCCLUDED"></span><span id="winbio_face_eyes_occluded"></span><dl> <dt>**WINBIO \_ FACE \_ EYES \_ OCCLUDED**</dt> </dl>                                             | Die Augen des Benutzers sind verblendet. Weisen Sie den Benutzer an, sicherzustellen, dass seine Augen nicht durch Elemente wie eine Brille, dunkle Brille oder farbige Kontakte verdeckt werden. Dieser Wert wird ab Windows 10.<br/>                                                                                 |
| <span id="WINBIO_FACE_WRONG_ORIENTATION"></span><span id="winbio_face_wrong_orientation"></span><dl> <dt>**FALSCHE AUSRICHTUNG DES \_ \_ WINBIO-GESICHTS \_**</dt> </dl>                                 | Die Kameraausrichtung passt nicht zur obligatorischen Ausrichtung, die die [**WINBIO \_ EXTENDED SENSOR \_ \_ INFO-Struktur**](winbio-extended-sensor-info.md) angibt. Weisen Sie den Benutzer an, die Kameraausrichtung zu ändern und erneut zu scannen. Dieser Wert wird ab Windows 10.<br/> |
| <span id="WINBIO_FACE_TOO_HIGH"></span><span id="winbio_face_too_high"></span><dl> <dt>**\_WINBIO-GESICHT \_ ZU \_ HOCH**</dt> </dl>                                                            | Das Gesicht wird nach oben gerichtet. Weisen Sie den Benutzer an, ein wenig nach unten zu suchen und erneut zu überprüfen. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LOW"></span><span id="winbio_face_too_low"></span><dl> <dt>**\_WINBIO-GESICHT \_ ZU \_ NIEDRIG**</dt> </dl>                                                               | Das Gesicht ist nach unten gerichtet. Weisen Sie den Benutzer an, etwas nach oben zu suchen und die Überprüfung erneut zu starten. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LEFT"></span><span id="winbio_face_too_left"></span><dl> <dt>**WINBIO \_ FACE \_ TOO \_ LEFT**</dt> </dl>                                                            | Das Gesicht ist zu weit auf der linken Seite. Weisen Sie den Benutzer an, etwas mehr nach rechts zu verschieben und die Überprüfung erneut zu starten. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_RIGHT"></span><span id="winbio_face_too_right"></span><dl> <dt>**WINBIO \_ FACE \_ TOO \_ RIGHT**</dt> </dl>                                                         | Das Gesicht ist zu weit nach rechts. Weisen Sie den Benutzer an, etwas mehr nach links zu verschieben und erneut zu überprüfen. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_NEAR"></span><span id="winbio_face_too_near"></span><dl> <dt>**\_WINBIO-GESICHT \_ ZU \_ NAH**</dt> </dl>                                                            | Das Gesicht ist zu nah an der Kamera. Weisen Sie den Benutzer an, sich etwas weiter zu bewegen und erneut zu überprüfen. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                   |
| <span id="WINBIO_FACE_TOO_FAR"></span><span id="winbio_face_too_far"></span><dl> <dt>**\_WINBIO-GESICHT \_ ZU \_ WEIT**</dt> </dl>                                                               | Das Gesicht ist zu weit von der Kamera entfernt. Weisen Sie den Benutzer an, sich etwas näher zu bewegen und die Überprüfung erneut zu starten. Dieser Wert wird ab Windows 10.<br/>                                                                                                                                         |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                                                                                  |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h für Clientanwendungen oder Winbio \_ adapters.h für Adapter enthalten)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungskonst constants](client-application-constants.md)
</dt> </dl>

 

 





