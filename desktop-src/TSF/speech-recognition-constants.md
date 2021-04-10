---
title: Sprach Erkennungs Konstanten (ctffunc. h)
description: Die folgenden Werte werden mit dem sprach Erkennungs Text-Dienst verwendet.
ms.assetid: ac433d15-738a-46ab-8f69-0fbfb6a8b654
topic_type:
- apiref
api_name:
- TF_DICTATION_ON
- TF_DICTATION_ENABLED
- TF_COMMANDING_ENABLED
- TF_COMMANDING_ON
- TF_SPEECHUI_SHOWN
- TF_SHOW_BALLOON
- TF_DISABLE_BALLOON
- TF_DISABLE_SPEECH
- TF_DISABLE_DICTATION
- TF_DISABLE_COMMANDING
api_location:
- Ctffunc.h
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04c9cfd340e79415d12202765a8db1578abba74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103015"
---
# <a name="speech-recognition-constants"></a>Sprach Erkennungs Konstanten

Die folgenden Werte werden mit dem sprach Erkennungs Text-Dienst verwendet.



| Konstante/Wert                                                                                                                                                                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DICTATION_ON"></span><span id="tf_dictation_on"></span><dl> <dt>**Tf \_ Diktat \_ auf**</dt> <dt>0x00000001</dt> </dl>                   | Wenn dieses Bit 1 ist, ist die Spracherkennung aktiv. Andernfalls ist die Spracherkennung inaktiv. Dieser Wert kann nicht mit dem TF-Befehlswert kombiniert werden \_ \_ . Wird mit dem [GUID \_ Depot \_ Speech-Skript " \_ ditationstat](predefined-compartments.md) " verwendet.<br/> |
| <span id="TF_DICTATION_ENABLED"></span><span id="tf_dictation_enabled"></span><dl> <dt>**Tf \_ Diktierung \_ aktiviert**</dt> <dt>0x00000002</dt> </dl>    | Wenn dieses Bit 1 ist, ist die Spracherkennung aktiviert. Andernfalls ist die Spracherkennung deaktiviert. Wird mit dem [GUID \_ Depot \_ Speech-Skript " \_ ditationstat](predefined-compartments.md) " verwendet.<br/>                                                       |
| <span id="TF_COMMANDING_ENABLED"></span><span id="tf_commanding_enabled"></span><dl> <dt>**Tf \_ Befehls \_ fähige**</dt> Funktion <dt>0x00000004</dt> </dl> | Wenn dieses Bit 1 ist, ist der Sprachbefehl aktiviert. Andernfalls ist der Sprachbefehl deaktiviert. Wird mit dem [GUID \_ Depot \_ Speech-Skript " \_ ditationstat](predefined-compartments.md) " verwendet.<br/>                                                           |
| <span id="TF_COMMANDING_ON"></span><span id="tf_commanding_on"></span><dl> <dt>**Tf \_ Befehls \_ auf**</dt> <dt>0x00000008</dt> </dl>                | Wenn dieses Bit 1 ist, ist der Sprachbefehl aktiv. Andernfalls ist der Sprachbefehl inaktiv. Dieser Wert kann nicht mit der TF- \_ diktierung für kombiniert werden \_ . Wird mit dem [GUID \_ Depot \_ Speech-Skript " \_ ditationstat](predefined-compartments.md) " verwendet.<br/>      |
| <span id="TF_SPEECHUI_SHOWN"></span><span id="tf_speechui_shown"></span><dl> <dt>**Tf \_ Sprach Benutzeroberfläche \_ angezeigt**</dt> <dt>0x00000010</dt> </dl>             | Derzeit nicht verwendet.<br/>                                                                                                                                                                                                                              |
| <span id="TF_SHOW_BALLOON"></span><span id="tf_show_balloon"></span><dl> <dt>**Tf \_ Sprech \_**</dt> Blase <dt>0x00000001</dt> anzeigen </dl>                   | Derzeit nicht verwendet. Wird mit dem [Benutzeroberflächen \_ - \_ \_ \_ Status Depot der GUID](predefined-compartments.md) -Depot Sprache verwendet.<br/>                                                                                                                              |
| <span id="TF_DISABLE_BALLOON"></span><span id="tf_disable_balloon"></span><dl> <dt>**Tf \_ Sprech \_**</dt> Blase <dt>0x00000002</dt> deaktivieren </dl>          | Wenn dieses Bit 1 ist, ist die Sprechblasen Anzeige für den aktuellen Sprachmodus deaktiviert. Andernfalls ist die Sprechblasen Anzeige für den aktuellen Sprachmodus aktiviert. Wird mit dem [Benutzeroberflächen \_ - \_ \_ \_ Status Depot der GUID](predefined-compartments.md) -Depot Sprache verwendet.<br/>    |
| <span id="TF_DISABLE_SPEECH"></span><span id="tf_disable_speech"></span><dl> <dt>**Tf \_ \_Sprache**</dt> <dt>0x00000001</dt> deaktivieren </dl>             | Wenn dieses Bit 1 ist, ist die Spracheingabe deaktiviert. Andernfalls ist die Spracheingabe aktiviert. Wird mit dem Depot " [GUID Depot \_ \_ Sprache \_ deaktiviert](predefined-compartments.md) " verwendet.<br/>                                                                    |
| <span id="TF_DISABLE_DICTATION"></span><span id="tf_disable_dictation"></span><dl> <dt>**Tf \_ \_Diktat**</dt> ' <dt>0x00000002</dt> ' deaktivieren </dl>    | Wenn dieses Bit 1 ist, ist die Spracherkennung deaktiviert. Andernfalls ist die Spracherkennung aktiviert. Wird mit dem Depot " [GUID Depot \_ \_ Sprache \_ deaktiviert](predefined-compartments.md) " verwendet.<br/>                                                            |
| <span id="TF_DISABLE_COMMANDING"></span><span id="tf_disable_commanding"></span><dl> <dt>**Tf \_ \_Befehls**</dt> - <dt>0x00000004</dt> deaktivieren </dl> | Wenn dieses Bit 1 ist, ist der Sprachbefehl deaktiviert. Andernfalls ist der Sprachbefehl aktiviert. Wird mit dem Depot " [GUID Depot \_ \_ Sprache \_ deaktiviert](predefined-compartments.md) " verwendet.<br/>                                                                |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                    |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                                                                                         |
| Header<br/>                   | <dl> <dt>Ctffunc. h; </dt> <dt>Msctf. h</dt> </dl>     |
| IDL<br/>                      | <dl> <dt>Ctffunc. idl; </dt> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vordefinierte Depots](predefined-compartments.md)
</dt> </dl>

 

 





