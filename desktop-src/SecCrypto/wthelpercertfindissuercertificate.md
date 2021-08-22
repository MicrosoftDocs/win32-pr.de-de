---
description: Sucht ein Ausstellerzertifikat aus den angegebenen Zertifikatspeichern, das dem angegebenen Zertifikat des Betreffs entspricht.
ms.assetid: c724f602-fc73-4857-941f-0f22a9e472d1
title: WTHelperCertFindIssuerCertificate-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperCertFindIssuerCertificate
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 3c6c7957e969d04eaf65014e023a5f64e0826b6285fb878d9afefbd7cda25721
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895832"
---
# <a name="wthelpercertfindissuercertificate-function"></a>WTHelperCertFindIssuerCertificate-Funktion

\[Die **WTHelperCertFindIssuerCertificate-Funktion** ist für die Verwendung in den Im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Die **WTHelperCertFindIssuerCertificate-Funktion** sucht ein Ausstellerzertifikat aus den angegebenen Zertifikatspeichern, das dem angegebenen Zertifikat des Betreffs entspricht.

> [!Note]  
> Dieser Funktion ist keine Importbibliothek zugeordnet. Sie müssen die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit Wintrust.dll.

 

## <a name="syntax"></a>Syntax


```C++
PCCERT_CONTEXT WINAPI WTHelperCertFindIssuerCertificate(
  _In_      PCCERT_CONTEXT pChildContext,
  _In_      DWORD          chStores,
  _In_      HCERTSTORE     *pahStores,
  _In_      FILETIME       *psftVerifyAsOf,
  _In_      DWORD          dwEncoding,
  _Out_opt_ DWORD          *pdwConfidence,
  _Out_     DWORD          *dwError
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pChildContext* \[ In\]
</dt> <dd>

Das Zertifikat des Subjekts, für das ein entsprechendes Ausstellerzertifikat zu finden ist.

</dd> <dt>

*chStores* \[ In\]
</dt> <dd>

Die Anzahl der Elemente im *pahStores-Array.*

</dd> <dt>

*pahStores* \[ In\]
</dt> <dd>

Ein Array von Zertifikatspeichern, in denen gesucht werden soll.

</dd> <dt>

*psftVerifyAsOf* \[ In\]
</dt> <dd>

Der Zeitpunkt der Überprüfung.

</dd> <dt>

*dwEncoding* \[ In\]
</dt> <dd>

Ein **DWORD-Wert,** der die Codierungstypen des zu überprüfenden Zertifikats angibt. Informationen zu möglichen Codierungstypen finden Sie unter [Zertifikat- und Nachrichtencodierungstypen.](certificate-and-message-encoding-types.md)

</dd> <dt>

*pdwConfidence* \[ out, optional\]
</dt> <dd>

Dieser Parameter kann eine bitweise Kombination von 0 (null) oder mehr der folgenden Konfidenzwerte sein.



| Wert                                                                                                                                                                                                                                                                 | Bedeutung                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <dt>**CERT \_ CONFIDENCE \_ SIG**</dt> <dt> 0x10000000</dt> </dl>                     | Die Signatur des Zertifikats ist gültig.<br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <dt>**CERT \_ CONFIDENCE \_ TIME**</dt> <dt> 0x01000000</dt> </dl>                  | Der Zeitpunkt, zu dem der Zertifikataussteller gültig ist.<br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <dt> **CERT \_ CONFIDENCE \_ TIMENEST**</dt> <dt>0x00100000</dt> </dl>    | Der Zeitpunkt, zu dem das Zertifikat gültig ist.<br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <dt> **CERT \_ CONFIDENCE \_ AUTHIDEXT**</dt> <dt>0x00010000</dt> </dl> | Die Erweiterung der Autoritäts-ID ist gültig.<br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <dt> **CERT \_ CONFIDENCE \_ CONFIDENCE**</dt> <dt>0X00001000</dt> </dl>       | Die Signatur der Zertifikat- und Zertifizierungsstelle-ID-Erweiterung ist mindestens gültig.<br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <dt> **CERT \_ CONFIDENCE \_ HIGHEST**</dt> <dt>0X11111000</dt> </dl>       | Eine Kombination aller anderen Konfidenzwerte.<br/>                                 |



 

</dd> <dt>

*dwError* \[ out\]
</dt> <dd>

Ein Zeiger auf eine **DWORD-Variable,** die ggf. den Fehlerwert für dieses Zertifikat enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein Ausstellerzertifikat, das dem durch den *pChildContext-Parameter angegebenen* Zertifikat des Betreffs entspricht.

## <a name="remarks"></a>Hinweise

Um erfolgreich ein entsprechendes Ausstellerzertifikat zu finden, müssen die folgenden Anforderungen erfüllt sein:

-   Die Signatur des vom *pChildContext-Parameter* angegebenen Zertifikats muss gültig sein.
-   Das **rgExtension-Element** des **pCertInfo-Mitglieds** des *pChildContext-Parameters* muss eine [**CERT \_ AUTHORITY KEY \_ \_ ID \_ INFO-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) enthalten. Die **Member CertIssuer** und **CertSerialMember** dieser Struktur passen stark zu den entsprechenden Membern für das Ausstellerzertifikat.
-   Der Wert des *psftVerifyAsOf-Parameters* muss innerhalb der Gültigkeitsdauer des Zertifikats des Betreffs sein.
-   Die Gültigkeitsdauer des Zertifikats des Subjekts muss innerhalb der Gültigkeitsdauer des Ausstellerzertifikats sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
