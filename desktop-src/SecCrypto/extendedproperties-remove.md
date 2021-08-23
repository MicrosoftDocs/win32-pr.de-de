---
description: Entfernt eine erweiterte Eigenschaft aus der Auflistung.
ms.assetid: 0329a158-758d-4e73-95a5-bab7307e7d70
title: ExtendedProperties.Remove-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 684d5abc0a0114e0d2bedb0dc544d50e13337631bb41fb457480dfbe8c5364e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007218"
---
# <a name="extendedpropertiesremove-method"></a>ExtendedProperties.Remove-Methode

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen Platform Invocation Services (PInvoke), um die Win32-API-Funktion [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) aufzurufen und die Eigenschaften abzurufen. Informationen zu PInvoke finden Sie unter [Tutorial zu Plattformaufrufen.](https://msdn.microsoft.com/library/aa288468.aspx) Die [Unterabschnitte .NET und CryptoAPI über P/Invoke: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.NET und CryptoAPI über P/Invoke: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) der Erweiterung der [.NET-Kryptografie mit CAPICOM und P/Invoke](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Die **Remove-Methode** entfernt eine erweiterte Eigenschaft aus der Auflistung.

## <a name="syntax"></a>Syntax


```VB
ExtendedProperties.Remove( _
  ByVal propID _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*propID* \[ In\]
</dt> <dd>

Ein Wert der [**CAPICOM \_ PROPID-Enumeration,**](capicom-propid.md) der die CAPICOM-Eigenschaftenbezeichner der zu entfernenden erweiterten Eigenschaft definiert. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROPID_UNKNOWN"></span><span id="capicom_propid_unknown"></span><dl> <dt>**CAPICOM \_ PROPID \_ UNKNOWN**</dt> </dl>                                                                       | Der Typ der Eigenschaft ist nicht bekannt.<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_KEY_PROV_HANDLE"></span><span id="capicom_propid_key_prov_handle"></span><dl> <dt>**CAPICOM \_ PROPID \_ KEY \_ PROV \_ HANDLE**</dt> </dl>                                             | Ein Handle für einen Schlüsselcontainer innerhalb eines [*Kryptografiedienstanbieters (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP).<br/>                                                                                        |
| <span id="CAPICOM_PROPID_KEY_PROV_INFO"></span><span id="capicom_propid_key_prov_info"></span><dl> <dt>**CAPICOM \_ PROPID \_ KEY \_ PROV \_ INFO**</dt> </dl>                                                   | Informationen zu einem Schlüsselcontainer in einem CSP.<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_SHA1_HASH"></span><span id="capicom_propid_sha1_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ SHA1 \_ HASH**</dt> </dl>                                                                | Ein SHA1-Hashobjekt.<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_HASH_PROP"></span><span id="capicom_propid_hash_prop"></span><dl> <dt>**CAPICOM \_ PROPID \_ HASH \_ PROP**</dt> </dl>                                                                | Die Eigenschaften eines Hashobjekts.<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_MD5_HASH"></span><span id="capicom_propid_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ MD5 \_ HASH**</dt> </dl>                                                                   | Ein MD5-Hashobjekt.<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_KEY_CONTEXT"></span><span id="capicom_propid_key_context"></span><dl> <dt>**CAPICOM \_ PROPID \_ KEY \_ CONTEXT**</dt> </dl>                                                          | Der [*Schlüsselkontext*](../secgloss/c-gly.md).<br/>                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_KEY_SPEC"></span><span id="capicom_propid_key_spec"></span><dl> <dt>**SPEZIFIKATION DES \_ CAPICOM-PROPID-SCHLÜSSELS \_ \_**</dt> </dl>                                                                   | Die Spezifikationen für einen Schlüssel.<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_IE30_RESERVED"></span><span id="capicom_propid_ie30_reserved"></span><dl> <dt>**CAPICOM \_ PROPID \_ IE30 \_ RESERVIERT**</dt> </dl>                                                    | Informationen darüber, ob das Objekt in Internet Explorer 3.0 reserviert ist.<br/>                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_PUBKEY_HASH_RESERVED"></span><span id="capicom_propid_pubkey_hash_reserved"></span><dl> <dt>**CAPICOM \_ PROPID \_ PUBKEY \_ HASH \_ RESERVIERT**</dt> </dl>                              | Informationen darüber, ob der Hash des öffentlichen Schlüssels reserviert ist.<br/>                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_ENHKEY_USAGE"></span><span id="capicom_propid_enhkey_usage"></span><dl> <dt>**CAPICOM \_ PROPID \_ ENHKEY \_ USAGE**</dt> </dl>                                                       | Eine erweiterte Schlüsselverwendung (Enhanced [*Key Usage,*](../secgloss/e-gly.md) EKU).<br/>                                                                                                                                                              |
| <span id="CAPICOM_PROPID_CTL_USAGE"></span><span id="capicom_propid_ctl_usage"></span><dl> <dt>**CAPICOM \_ PROPID \_ CTL \_ USAGE**</dt> </dl>                                                                | Verwendung einer [*Zertifikatvertrauensliste*](../secgloss/c-gly.md) (Certificate Trust List, CTL).<br/>                                                                                                                                             |
| <span id="CAPICOM_PROPID_NEXT_UPDATE_LOCATION"></span><span id="capicom_propid_next_update_location"></span><dl> <dt>**CAPICOM \_ PROPID \_ SPEICHERORT DES NÄCHSTEN \_ UPDATES \_**</dt> </dl>                              | Der Speicherort des nächsten Updates der [*Zertifikatsperrliste*](../secgloss/c-gly.md) (Certificate Revocation List, CRL).<br/>                                                                                               |
| <span id="CAPICOM_PROPID_FRIENDLY_NAME"></span><span id="capicom_propid_friendly_name"></span><dl> <dt>**ANZEIGENAME DER \_ CAPICOM-PROPID \_ \_**</dt> </dl>                                                    | Ein für Menschen lesbarer Name.<br/>                                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_PVK_FILE"></span><span id="capicom_propid_pvk_file"></span><dl> <dt>**CAPICOM \_ PROPID \_ \_ PVK-DATEI**</dt> </dl>                                                                   | Eine Datei, die einen privaten Schlüssel enthält.<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_DESCRIPTION"></span><span id="capicom_propid_description"></span><dl> <dt>**CAPICOM \_ PROPID \_ DESCRIPTION**</dt> </dl>                                                           | Eine lesbare Beschreibung.<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ACCESS_STATE"></span><span id="capicom_propid_access_state"></span><dl> <dt>**CAPICOM \_ PROPID \_ ACCESS \_ STATE**</dt> </dl>                                                       | Der Zustand des Zugriffs.<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SIGNATURE_HASH"></span><span id="capicom_propid_signature_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ SIGNATURE \_ HASH**</dt> </dl>                                                 | Ein Hash der Signatur.<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SMART_CARD_DATA"></span><span id="capicom_propid_smart_card_data"></span><dl> <dt>**CAPICOM \_ \_ PROPID-SMARTCARDDATEN \_ \_**</dt> </dl>                                             | Smartcarddaten.<br/>                                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_EFS"></span><span id="capicom_propid_efs"></span><dl> <dt>**CAPICOM \_ PROPID \_ EFS**</dt> </dl>                                                                                   | Ein verschlüsselndes Dateisystem (EFS).<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_FORTEZZA_DATA"></span><span id="capicom_propid_fortezza_data"></span><dl> <dt>**CAPICOM \_ PROPID \_ FORTEZZA \_ DATA**</dt> </dl>                                                    | Daten, die mit den kryptografischen Protokollen und Algorithmen des [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) erstellt wurden.<br/> |
| <span id="CAPICOM_PROPID_ARCHIVED"></span><span id="capicom_propid_archived"></span><dl> <dt>**CAPICOM \_ PROPID \_ ARCHIVED**</dt> </dl>                                                                    | Informationen darüber, ob das Objekt archiviert wird.<br/>                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_KEY_IDENTIFIER"></span><span id="capicom_propid_key_identifier"></span><dl> <dt>**CAPICOM \_ PROPID \_ KEY \_ IDENTIFIER**</dt> </dl>                                                 | Ein Schlüsselbezeichner.<br/>                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_AUTO_ENROLL"></span><span id="capicom_propid_auto_enroll"></span><dl> <dt>**CAPICOM \_ PROPID \_ AUTO \_ ENROLL**</dt> </dl>                                                          | Informationen zur automatischen Registrierung für ein Zertifikat.<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_PUBKEY_ALG_PARA"></span><span id="capicom_propid_pubkey_alg_para"></span><dl> <dt>**CAPICOM \_ PROPID \_ PUBKEY \_ ALG \_ PARA**</dt> </dl>                                             | Parameter für einen Algorithmus mit öffentlichem Schlüssel.<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_CROSS_CERT_DIST_POINTS"></span><span id="capicom_propid_cross_cert_dist_points"></span><dl> <dt>**CAPICOM \_ PROPID \_ – ZERTIFIKATÜBERGREIFENDE \_ \_ \_ DIST-PUNKTE**</dt> </dl>                       | Informationen, die zum Aktualisieren dynamischer zertifikatübergreifender Zertifikate verwendet werden.<br/>                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_ISSUER_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_issuer_public_key_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ ISSUER \_ PUBLIC \_ KEY \_ MD5 \_ HASH**</dt> </dl>          | Der MD5-Hash des öffentlichen Schlüssels des Ausstellers.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SUBJECT_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_subject_public_key_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ SUBJECT \_ PUBLIC \_ KEY \_ MD5 \_ HASH**</dt> </dl>       | Der MD5-Hash des öffentlichen Schlüssels des Antragstellers.<br/>                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROPID_ENROLLMENT"></span><span id="capicom_propid_enrollment"></span><dl> <dt>**CAPICOM \_ \_ PROPID-REGISTRIERUNG**</dt> </dl>                                                              | Informationen zur Registrierung des Zertifikats.<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_DATE_STAMP"></span><span id="capicom_propid_date_stamp"></span><dl> <dt>**CAPICOM \_ PROPID \_ DATE \_ STAMP**</dt> </dl>                                                             | Ein Datumsstempel.<br/>                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ISSUER_SERIAL_NUMBER_MD5_HASH"></span><span id="capicom_propid_issuer_serial_number_md5_hash"></span><dl> <dt>**MD5-HASH DER SERIENNUMMER DES \_ CAPICOM-PROPID-AUSSTELLERS \_ \_ \_ \_ \_**</dt> </dl> | Der MD5-Hash der Seriennummer des Ausstellers.<br/>                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROPID_SUBJECT_NAME_MD5_HASH"></span><span id="capicom_propid_subject_name_md5_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ SUBJECT \_ NAME \_ MD5 \_ HASH**</dt> </dl>                          | Der MD5-Hash des Antragstellernamens.<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_EXTENDED_ERROR_INFO"></span><span id="capicom_propid_extended_error_info"></span><dl> <dt>**\_ \_ ERWEITERTE \_ \_ FEHLERINFORMATIONEN ZU CAPICOM PROPID**</dt> </dl>                                 | Erweiterte Informationen zu einem Fehler.<br/>                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROPID_RENEWAL"></span><span id="capicom_propid_renewal"></span><dl> <dt>**CAPICOM \_ PROPID \_ RENEWAL**</dt> </dl>                                                                       | Informationen zur Erneuerung einer [*Zertifizierungsstelle.*](../secgloss/c-gly.md)<br/>                                                                                                                     |
| <span id="CAPICOM_PROPID_ARCHIVED_KEY_HASH"></span><span id="capicom_propid_archived_key_hash"></span><dl> <dt>**CAPICOM \_ PROPID \_ ARCHIVED \_ KEY \_ HASH**</dt> </dl>                                       | Ein archivierter Hash eines Schlüssels.<br/>                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_FIRST_RESERVED"></span><span id="capicom_propid_first_reserved"></span><dl> <dt>**CAPICOM \_ PROPID \_ FIRST \_ RESERVIERT**</dt> </dl>                                                 | Informationen zur ersten Reservierung.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_LAST_RESERVED"></span><span id="capicom_propid_last_reserved"></span><dl> <dt>**CAPICOM \_ PROPID \_ LAST \_ RESERVED**</dt> </dl>                                                    | Informationen zur letzten Reservierung.<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_FIRST_USER"></span><span id="capicom_propid_first_user"></span><dl> <dt>**CAPICOM \_ PROPID \_ FIRST \_ USER**</dt> </dl>                                                             | Informationen zum ersten Benutzer.<br/>                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_LAST_USER"></span><span id="capicom_propid_last_user"></span><dl> <dt>**CAPICOM \_ PROPID \_ LAST \_ USER**</dt> </dl>                                                                | Informationen zum letzten Benutzer.<br/>                                                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
