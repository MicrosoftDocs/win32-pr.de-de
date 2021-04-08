---
title: WINBIO_REJECT_DETAIL Konstanten (winbio \_ types. h)
description: Geben Sie den Grund an, warum eine biometrische Fingerabdruck Erfassung oder-Identifikation nicht erfolgreich war.
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
ms.openlocfilehash: 4d9d23dcf568e5ed25fb5081283a421b1c0dbb07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743864"
---
# <a name="winbio_reject_detail-constants"></a>Winbio- \_ Ablehnungs \_ Detail Konstanten

Die folgenden Konstanten können verwendet werden, um den Grund anzugeben, warum ein biometrische Fingerabdruck Erfassungs-oder Identifikationsverfahren nicht erfolgreich war.



| Konstante                                                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FP_TOO_HIGH"></span><span id="winbio_fp_too_high"></span><dl> <dt>**winbio \_ FP \_ zu \_ hoch**</dt> </dl>                                                                  | Der Fingerscan begann zu hoch.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_LOW"></span><span id="winbio_fp_too_low"></span><dl> <dt>**winbio \_ FP \_ zu \_ niedrig**</dt> </dl>                                                                     | Der Fingerscan war zu niedrig.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_LEFT"></span><span id="winbio_fp_too_left"></span><dl> <dt>**winbio \_ FP \_ zu \_ Links**</dt> </dl>                                                                  | Der Finger war während des Scans zu weit links.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_RIGHT"></span><span id="winbio_fp_too_right"></span><dl> <dt>**winbio \_ FP \_ zu \_ Recht**</dt> </dl>                                                               | Der Finger war zu weit rechts während des Scans.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_FAST"></span><span id="winbio_fp_too_fast"></span><dl> <dt>**winbio \_ FP \_ zu \_ schnell**</dt> </dl>                                                                  | Der Finger wurde auf dem Sensor zu schnell weitergeleitet.<br/>                                                                                                                                                                                                                                       |
| <span id="WINBIO_FP_TOO_SLOW"></span><span id="winbio_fp_too_slow"></span><dl> <dt>**winbio \_ FP \_ zu \_ langsam**</dt> </dl>                                                                  | Der Finger wurde auf dem Sensor zu langsam weitergeleitet.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_FP_POOR_QUALITY"></span><span id="winbio_fp_poor_quality"></span><dl> <dt>**winbio \_ fp, \_ schlechte \_ Qualität**</dt> </dl>                                                      | Die Scanqualität war zu schlecht.<br/>                                                                                                                                                                                                                                                         |
| <span id="WINBIO_FP_TOO_SKEWED"></span><span id="winbio_fp_too_skewed"></span><dl> <dt>**winbio \_ FP \_ zu \_ verzerrt**</dt> </dl>                                                            | Der Finger konnte nicht direkt über den Sensor übergeben werden.<br/>                                                                                                                                                                                                                                    |
| <span id="WINBIO_FP_TOO_SHORT"></span><span id="winbio_fp_too_short"></span><dl> <dt>**winbio \_ FP \_ zu \_ kurz**</dt> </dl>                                                               | Nicht genug, dass der Finger gescannt wurde.<br/>                                                                                                                                                                                                                                                  |
| <span id="WINBIO_FP_MERGE_FAILURE"></span><span id="winbio_fp_merge_failure"></span><dl> <dt>**winbio \_ FP- \_ Merge- \_ Fehler**</dt> </dl>                                                   | Die Fingerabdruck Erfassungen konnten nicht kombiniert werden.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK____"></span><span id="winbio_reject_detail_anti_spoof_mask____"></span><dl> <dt>**Winbio \_ \_ \_ \_ spophierungmaske für \_ Details ablehnen**</dt> </dl> | Diese Maske deckt die oberen 8 Bits des Ablehnungs Detail Werts ab, in denen sich das Verhalten der Nachweisfähigkeit befindet. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_POSITION_MASK______"></span><span id="winbio_reject_detail_position_mask______"></span><dl> <dt>**Winbio \_ \_Detail \_ Positions \_ Maske ablehnen**</dt> </dl>    | Diese Maske deckt den Bereich von Bits ab, der für Positionsfehler verwendet wird. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                                                         |
| <span id="WINBIO_REJECT_DETAIL_REASON_MASK"></span><span id="winbio_reject_detail_reason_mask"></span><dl> <dt>**winbio- \_ Ablehnungs \_ Detail- \_ Grund \_ Maske**</dt> </dl>                       | Diese Maske deckt die unteren 16 Bits ab, bei denen sich der enumerationsgrund für die Ablehnung befindet. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                           |
| <span id="WINBIO_IRIS_POOR_QUALITY"></span><span id="winbio_iris_poor_quality"></span><dl> <dt>**winbio \_ IRIS \_ schlechte \_ Qualität**</dt> </dl>                                                | Die Bedingungen haben bewirkt, dass die Kamera ein schlechtes Bild erfasst. Weisen Sie den Benutzer an, den Sensor zu bereinigen und erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                        |
| <span id="WINBIO_IRIS_TOO_BRIGHT"></span><span id="winbio_iris_too_bright"></span><dl> <dt>**winbio \_ IRIS \_ zu \_ hell**</dt> </dl>                                                      | Das Bild enthält zu viele Umgebungsbeleuchtung, um eine gute Stimmung zu erzielen. Weisen Sie den Benutzer an, sicherzustellen, dass keine andere helle Lichtquelle angezeigt wird. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                        |
| <span id="WINBIO_IRIS_TOO_DARK"></span><span id="winbio_iris_too_dark"></span><dl> <dt>**winbio \_ IRIS \_ zu \_ dunkel**</dt> </dl>                                                            | Das Bild ist zu dunkel, um eine gute Stimmung zu erzielen. Weisen Sie den Benutzer an, sicherzustellen, dass die Iris nicht durch Elemente wie einen Schleier, eine dunkle Brille oder farbige Kontakte verdeckt wird. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                     |
| <span id="WINBIO_IRIS_SPOOF_DETECTED"></span><span id="winbio_iris_spoof_detected"></span><dl> <dt>**winbio \_ IRIS \_ Spoof \_ erkannt**</dt> </dl>                                          | Die Erkennungs Komponente ist der Meinung, dass die Iris nicht Live ist, sondern von einem wiedergegebenen Videofeed, einem Foto oder einer 3D-Skulptur stammt. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                   |
| <span id="WINBIO_IRIS_TOO_SKEWED"></span><span id="winbio_iris_too_skewed"></span><dl> <dt>**winbio \_ IRIS \_ zu \_ verzerrt**</dt> </dl>                                                      | Der Benutzer sucht nicht direkt auf der Kamera. Weisen Sie den Benutzer an, die Kamera direkt einzusehen und erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                       |
| <span id="WINBIO_IRIS_TOO_CLOSED"></span><span id="winbio_iris_too_closed"></span><dl> <dt>**winbio \_ IRIS \_ zu \_ geschlossen**</dt> </dl>                                                      | Die eyelids des Benutzers verschleiern die Iris. Weisen Sie den Benutzer an, die Augen etwas mehr zu öffnen und erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                          |
| <span id="WINBIO_IRIS_GLARE"></span><span id="winbio_iris_glare"></span><dl> <dt>**winbio \_ IRIS- \_ glare**</dt> </dl>                                                                      | Das Image enthält die "Lens"-glare. Weisen Sie den Benutzer an, Ihre Gläser zu entfernen und erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                               |
| <span id="WINBIO_IRIS_DIRTY_LENS"></span><span id="winbio_iris_dirty_lens"></span><dl> <dt>**winbio \_ IRIS ( \_ Dirty \_ Lens)**</dt> </dl>                                                      | Der Kamera Foto wurde geändert. Weisen Sie den Benutzer an, den Lens zu bereinigen und erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                                         |
| <span id="WINBIO_IRIS_POOR_FOCUS"></span><span id="winbio_iris_poor_focus"></span><dl> <dt>**winbio \_ Iris ist \_ schlecht \_ fokussiert.**</dt> </dl>                                                      | Diese IRIS ist nicht fokussiert. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                                                                                             |
| <span id="WINBIO_IRIS_WRONG_ORIENTATION"></span><span id="winbio_iris_wrong_orientation"></span><dl> <dt>**winbio \_ IRIS- \_ falsche \_ Ausrichtung**</dt> </dl>                                 | Die Kameraausrichtung entspricht nicht der obligatorischen Ausrichtung, die von der erweiterten Struktur des [**winbio- \_ \_ Sensors \_**](winbio-extended-sensor-info.md) angegeben wird. Weisen Sie den Benutzer an, die Kameraausrichtung zu ändern und erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/> |
| <span id="WINBIO_IRIS_TOO_HIGH"></span><span id="winbio_iris_too_high"></span><dl> <dt>**winbio \_ IRIS \_ zu \_ hoch**</dt> </dl>                                                            | Die IRIS wird angezeigt. Weisen Sie den Benutzer an, etwas zu suchen und erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LOW"></span><span id="winbio_iris_too_low"></span><dl> <dt>**winbio \_ IRIS \_ zu \_ niedrig**</dt> </dl>                                                               | Die IRIS wird angezeigt. Weisen Sie den Benutzer an, etwas zu suchen und erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LEFT"></span><span id="winbio_iris_too_left"></span><dl> <dt>**winbio \_ IRIS \_ zu \_ Links**</dt> </dl>                                                            | Die Iris ist zu weit links. Weisen Sie den Benutzer an, etwas mehr nach rechts zu suchen und die Überprüfung erneut auszuführen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_RIGHT"></span><span id="winbio_iris_too_right"></span><dl> <dt>**winbio \_ IRIS \_ zu \_ Rechts**</dt> </dl>                                                         | Die Iris ist zu weit nach rechts. Weisen Sie den Benutzer an, auf der linken Seite etwas mehr zu sehen und es erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_NEAR"></span><span id="winbio_iris_too_near"></span><dl> <dt>**winbio \_ IRIS \_ zu \_ nah**</dt> </dl>                                                            | Die Iris ist zu nah an der Kamera. Weisen Sie den Benutzer an, etwas weiter zu verschieben und erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                   |
| <span id="WINBIO_IRIS_TOO_FAR"></span><span id="winbio_iris_too_far"></span><dl> <dt>**winbio \_ IRIS \_ zu \_ weit**</dt> </dl>                                                               | Die Iris ist zu weit von der Kamera. Weisen Sie den Benutzer an, etwas genauer zu verschieben und erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                         |
| <span id="WINBIO_FACE_POOR_QUALITY"></span><span id="winbio_face_poor_quality"></span><dl> <dt>**winbio \_ - \_ Qualität mit schlechter \_ Qualität**</dt> </dl>                                                | Die Bedingungen haben bewirkt, dass die Kamera ein schlechtes Bild erfasst. Weisen Sie den Benutzer an, den Sensor zu bereinigen und erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                        |
| <span id="WINBIO_FACE_TOO_BRIGHT"></span><span id="winbio_face_too_bright"></span><dl> <dt>**winbio- \_ Gesicht \_ zu \_ hell**</dt> </dl>                                                      | Das Bild enthält zu viele Umgebungsbeleuchtung, um eine gute Stimmung zu erzielen. Weisen Sie den Benutzer an, sicherzustellen, dass keine andere helle Lichtquelle angezeigt wird. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                        |
| <span id="WINBIO_FACE_TOO_DARK"></span><span id="winbio_face_too_dark"></span><dl> <dt>**winbio- \_ Gesicht \_ zu \_ dunkel**</dt> </dl>                                                            | Das Bild ist zu dunkel, um eine gute Stimmung zu erzielen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                                                                             |
| <span id="WINBIO_FACE_SPOOF_DETECTED"></span><span id="winbio_face_spoof_detected"></span><dl> <dt>**winbio- \_ Gesichts \_ Spoof \_ erkannt**</dt> </dl>                                          | Die Erkennungs Komponente ist der Meinung, dass das Gesicht nicht Live ist, sondern aus einem wiedergegebenen Videofeed, einem Foto oder einer 3D-Skulptur stammt. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                   |
| <span id="WINBIO_FACE_AMBIGUOUS_TARGET"></span><span id="winbio_face_ambiguous_target"></span><dl> <dt>**winbio \_ - \_ Ziel mehrdeutiges \_ Ziel**</dt> </dl>                                    | Zwei oder mehr Gesichter überlappen sich im Kamera Rahmen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                                                                     |
| <span id="WINBIO_FACE_EYES_OCCLUDED"></span><span id="winbio_face_eyes_occluded"></span><dl> <dt>**winbio- \_ Gesichtserkennung \_ \_**</dt> </dl>                                             | Die Augen des Benutzers werden ausgeblendet. Weisen Sie den Benutzer an, sicherzustellen, dass Ihre Augen nicht durch Elemente wie einen Schleier, eine dunkle Brille oder farbige Kontakte verdeckt werden. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                 |
| <span id="WINBIO_FACE_WRONG_ORIENTATION"></span><span id="winbio_face_wrong_orientation"></span><dl> <dt>**winbio \_ mit \_ falscher \_ Ausrichtung**</dt> </dl>                                 | Die Kameraausrichtung entspricht nicht der obligatorischen Ausrichtung, die von der erweiterten Struktur des [**winbio- \_ \_ Sensors \_**](winbio-extended-sensor-info.md) angegeben wird. Weisen Sie den Benutzer an, die Kameraausrichtung zu ändern und erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/> |
| <span id="WINBIO_FACE_TOO_HIGH"></span><span id="winbio_face_too_high"></span><dl> <dt>**winbio- \_ Gesicht \_ zu \_ hoch**</dt> </dl>                                                            | Die Vorderseite wird angezeigt. Weisen Sie den Benutzer an, etwas zu suchen und erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LOW"></span><span id="winbio_face_too_low"></span><dl> <dt>**winbio- \_ Gesicht \_ zu \_ niedrig**</dt> </dl>                                                               | Die Vorderseite wird angezeigt. Weisen Sie den Benutzer an, etwas zu suchen und erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LEFT"></span><span id="winbio_face_too_left"></span><dl> <dt>**winbio-Seite \_ \_ zu \_ Links**</dt> </dl>                                                            | Die Fläche ist zu weit links. Weisen Sie den Benutzer an, etwas mehr nach rechts zu verschieben und die Überprüfung erneut durchführen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_RIGHT"></span><span id="winbio_face_too_right"></span><dl> <dt>**winbio- \_ Gesicht \_ zu \_ Rechts**</dt> </dl>                                                         | Das Gesicht ist zu weit nach rechts. Weisen Sie den Benutzer an, etwas mehr nach Links zu verschieben und den Scanvorgang erneut durchführen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_NEAR"></span><span id="winbio_face_too_near"></span><dl> <dt>**winbio- \_ Gesicht \_ zu \_ nah**</dt> </dl>                                                            | Das Gesicht ist zu nah an der Kamera. Weisen Sie den Benutzer an, etwas weiter zu verschieben und erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                   |
| <span id="WINBIO_FACE_TOO_FAR"></span><span id="winbio_face_too_far"></span><dl> <dt>**winbio- \_ Gesicht \_ zu \_ weit**</dt> </dl>                                                               | Die Vorderseite ist zu weit von der Kamera. Weisen Sie den Benutzer an, etwas genauer zu verschieben und erneut zu scannen. Dieser Wert wird ab Windows 10 unterstützt.<br/>                                                                                                                                         |



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

 

 





