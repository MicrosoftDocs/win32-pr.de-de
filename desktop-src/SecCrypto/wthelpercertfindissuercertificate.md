---
description: Sucht ein Aussteller Zertifikat aus den angegebenen Zertifikat speichern, das mit dem angegebenen Antragsteller Zertifikat übereinstimmt.
ms.assetid: c724f602-fc73-4857-941f-0f22a9e472d1
title: Wthelpercertfinrevoercertificate-Funktion
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
ms.openlocfilehash: 99135ac22509b288726732ca4a16248b304f294b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216197"
---
# <a name="wthelpercertfindissuercertificate-function"></a>Wthelpercertfinrevoercertificate-Funktion

\[Die Funktion " **wthelpercertfinrevoercertificate** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Die **wthelpercertfinrevoercertificate** -Funktion sucht ein Aussteller Zertifikat aus den angegebenen Zertifikat speichern, das mit dem angegebenen Antragsteller Zertifikat übereinstimmt.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Sie müssen die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Wintrust.dll zu verknüpfen.

 

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

*pchildcontext* \[ in\]
</dt> <dd>

Das Antragsteller Zertifikat, für das ein entsprechendes Aussteller Zertifikat gefunden werden soll.

</dd> <dt>

*chstores* \[ in\]
</dt> <dd>

Die Anzahl der Elemente *im Array von* Arrays.

</dd> <dt>

*Filialen* \[ in\]
</dt> <dd>

Ein Array von Zertifikat speichern, in denen gesucht werden soll.

</dd> <dt>

*psftverif-of* \[ in\]
</dt> <dd>

Der Zeitpunkt der Überprüfung.

</dd> <dt>

*dwencoding* \[ in\]
</dt> <dd>

Ein **DWORD** -Wert, der die Codierungs Typen des Zertifikats angibt, das überprüft werden soll. Informationen zu möglichen Codierungs Typen finden Sie unter [Zertifikat-und Nachrichten Codierungs Typen](certificate-and-message-encoding-types.md).

</dd> <dt>

*pdwconfidence* \[ Out, optional\]
</dt> <dd>

Dieser Parameter kann eine bitweise Kombination von 0 (null) oder mehr der folgenden Konfidenz Werte sein.



| Wert                                                                                                                                                                                                                                                                 | Bedeutung                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <dt>**Zertifikat \_ Zuverlässigkeit \_ sig**</dt> <dt> 0x10000000</dt> </dl>                     | Die Signatur des Zertifikats ist gültig.<br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <dt>**Zertifikat \_ Vertrauens \_ Zeit**</dt> <dt> 0x01000000</dt> </dl>                  | Die Zeit des Zertifikat Ausstellers ist gültig.<br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <dt> **CERT \_ Confidence \_ timenest**</dt> <dt>0x00100000</dt> </dl>    | Die Uhrzeit des Zertifikats ist gültig.<br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <dt> **CERT \_ Confidence \_ authidext**</dt> <dt>0x00010000 bis</dt> </dl> | Die Autoritäts-ID-Erweiterung ist gültig.<br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <dt> **Zertifikat \_ Vertrauens \_ Pflege**</dt> <dt>0x00001000</dt> </dl>       | Die Signatur der Zertifikat-und Autoritäts-ID-Erweiterung ist mindestens gültig.<br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <dt> **CERT \_ Confidence \_ höchste**</dt> <dt>0x11111000</dt> </dl>       | Eine Kombination aus allen anderen Vertrauens Werten.<br/>                                 |



 

</dd> <dt>

*dwError* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine **DWORD** -Variable, die ggf. den Fehlerwert für dieses Zertifikat enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein Aussteller Zertifikat, das mit dem vom *pchildcontext* -Parameter angegebenen Antragsteller Zertifikat übereinstimmt.

## <a name="remarks"></a>Bemerkungen

Die folgenden Anforderungen müssen erfüllt sein, damit ein entsprechendes Aussteller Zertifikat gefunden werden kann:

-   Die Signatur des vom *pchildcontext* -Parameter angegebenen betreffzertifikats muss gültig sein.
-   Das **rgextension** -Element des **pcertinfo** -Members des *pchildcontext* -Parameters muss eine Zertifikat Zertifizierungsstellen- [**Schlüssel-ID- \_ \_ \_ \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) Struktur enthalten. Die Member **CertIssuer** und **certserialmember** dieser Struktur Stimmen stark mit den entsprechenden Membern für das Aussteller Zertifikat überein.
-   Der Wert des *psftverisyasof* -Parameters muss innerhalb des Gültigkeits Zeitraums des Antragsteller Zertifikats liegen.
-   Der Gültigkeits Zeitraum des Antragsteller Zertifikats muss innerhalb des Gültigkeits Zeitraums des Aussteller Zertifikats liegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
