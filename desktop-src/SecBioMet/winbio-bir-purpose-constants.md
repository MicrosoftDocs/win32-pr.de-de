---
title: WINBIO_BIR_PURPOSE Konstanten (winbio \_ types. h)
description: Geben Sie den Zweck an, für den der biometrische Informationsdaten Satz (BIR) vorgesehen ist oder für den er geeignet ist.
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
ms.openlocfilehash: f5a662a5ae045d3afc631f93cdf296508dabccf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956524"
---
# <a name="winbio_bir_purpose-constants"></a>Winbio-und- \_ \_ Zweck-Konstanten

Die folgenden Flags werden vom **Purpose** -Member der [**winbio- \_ \_ Header**](winbio-bir-header.md) Struktur verwendet, um den Zweck anzugeben, für den der biometrische Informationsdaten Satz (BIR) vorgesehen ist oder für den er geeignet ist.



| Konstante                                                                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <dt>**winbio \_ ist \_ nicht \_ verfügbar.**</dt> </dl>                                         | Es wurde kein Zweck angegeben.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <dt>**Überprüfung von winbio- \_ Zwecken \_**</dt> </dl>                                                            | Überprüfen Sie die Identität eines Benutzers.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <dt>**Zweck der winbio- \_ \_ Identifizierung**</dt> </dl>                                                      | Identifizieren Sie einen Benutzer.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <dt>**winbio- \_ Aufgabe \_ registrieren**</dt> </dl>                                                            | Registrieren Sie einen Benutzer.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <dt>**winbio- \_ Zweck \_ für die \_ über \_ Prüfung**</dt> </dl>       | Erfassen Sie ein biometrisches Beispiel, und bestimmen Sie, ob das Beispiel der angegebenen Benutzeridentität entspricht.<br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <dt>**winbio- \_ Zweck \_ \_ zur \_ Identifizierung registrieren**</dt> </dl> | Erfassen eines biometrischen Beispiels und ermitteln, ob es mit einer vorhandenen biometrischen Vorlage übereinstimmt.<br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <dt>**Überprüfung von winbio- \_ Zwecken \_**</dt> </dl>                                                               | Zusätzliche Informationen, die für die Protokollierung oder die Anzeige verwendet werden können. Dieser Wert wird bei der Eingabe von allen Funktionen ignoriert. Bei der Ausgabe ist Sie nur verfügbar, wenn Sie von der biometrischen Einheit unterstützt wird, und Sie geben das **winbio \_ Data \_ Flag \_ RAW** im *Flags* -Parameter der [**winbiocapturesample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) -Funktion an.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Konstanten](client-application-constants.md)
</dt> <dt>

[**winbio- \_ Bir- \_ Header**](winbio-bir-header.md)
</dt> </dl>

 

 





