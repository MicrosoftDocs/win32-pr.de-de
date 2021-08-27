---
title: WINBIO_BIR_PURPOSE Konstanten (Winbio \_ types.h)
description: Geben Sie den Zweck an, für den der Biometrische Informationsdatensatz (BIR) vorgesehen ist oder für den er geeignet ist.
ms.assetid: AAFD3203-4D3D-43B5-A833-1258E1E281D3
topic_type:
- apiref
api_name:
- WINBIO_NO_PURPOSE_AVAILABLE
- WINBIO_PURPOSE_VERIFY
- WINBIO_PURPOSE_IDENTIFY
- WINBIO_PURPOSE_ENROLL
- WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION
- WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION
- WINBIO_PURPOSE_AUDIT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19cffe266cf30155be3c299b0d1b5e6a3d45f9991aa83fd66e62e705ddc4850f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080790"
---
# <a name="winbio_bir_purpose-constants"></a>WINBIO \_ BIR \_ PURPOSE-Konstanten

Die folgenden Flags werden vom **Purpose-Member** der [**WINBIO \_ BIR \_ HEADER-Struktur**](winbio-bir-header.md) verwendet, um den Zweck anzugeben, für den der Biometrische Informationsdatensatz (BIR) vorgesehen ist oder für den er geeignet ist.



| Konstante                                                                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <dt>**WINBIO \_ KEIN \_ ZWECK \_ VERFÜGBAR**</dt> </dl>                                         | Es wird kein Zweck angegeben.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <dt>**WINBIO \_ PURPOSE \_ VERIFY**</dt> </dl>                                                            | Überprüfen Sie die Identität eines Benutzers.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <dt>**WINBIO \_ PURPOSE \_ IDENTIFY**</dt> </dl>                                                      | Identifizieren eines Benutzers.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <dt>**WINBIO \_ PURPOSE \_ ENROLL**</dt> </dl>                                                            | Registrieren sie einen Benutzer.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <dt>**WINBIO \_ PURPOSE \_ ENROLL \_ FOR \_ VERIFICATION**</dt> </dl>       | Erfassen Sie ein biometrisches Beispiel, und bestimmen Sie, ob das Beispiel der angegebenen Benutzeridentität entspricht.<br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <dt>**WINBIO \_ PURPOSE \_ ENROLL \_ FOR \_ IDENTIFICATION**</dt> </dl> | Erfassen Sie ein biometrisches Beispiel, und bestimmen Sie, ob es mit einer vorhandenen biometrischen Vorlage übereinstimmt.<br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <dt>**\_WINBIO-ZWECKÜBERWACHUNG \_**</dt> </dl>                                                               | Zusätzliche Informationen, die für die Protokollierung oder anzeige verwendet werden können. Dieser Wert wird bei der Eingabe durch alle Funktionen ignoriert. Bei der Ausgabe ist sie nur verfügbar, wenn sie von der biometrischen Einheit unterstützt wird, und Sie geben **WINBIO \_ DATA FLAG \_ \_ RAW** im *Flags-Parameter* der [**WinBioCaptureSample-Funktion**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) an.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Clientanwendungskonstanten](client-application-constants.md)
</dt> <dt>

[**WINBIO \_ \_ BIR-HEADER**](winbio-bir-header.md)
</dt> </dl>

 

 





