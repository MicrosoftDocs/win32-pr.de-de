---
description: Stempelt den angegebenen Betreff und unterstützt das Festlegen von Zeitstempeln für mehrere Signaturen.
ms.assetid: A290ED4F-8803-4EAA-8CE1-68879F7F754A
title: SignerTimeStampEx3-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx3
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 7eb5c19292b451b1a3d0265da4bb178eafcc6f00
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468557"
---
# <a name="signertimestampex3-function"></a>SignerTimeStampEx3-Funktion

Die **SignerTimeStampEx3-Funktion** stempelt den angegebenen Betreff und unterstützt das Festlegen von Zeitstempeln für mehrere Signaturen.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch eine Verknüpfung mit Mssign32.dll.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI SignerTimeStampEx3(
  _In_       DWORD                  dwFlags,
  _In_       DWORD                  dwIndex,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       PCWSTR                 pwszHttpTimeStamp,
  _In_       PCWSTR                 pszAlgorithmOid,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Flag, das den Typ des zu generierenden Zeitstempels angibt. Dieser Parameter kann einen der folgenden Werte annehmen. Die Werte schließen sich gegenseitig aus.




| Wert | Bedeutung | 
|-------|---------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt></dl> | Gibt einen Authenticode-Zeitstempel an.<br /><blockquote>[!Note]<br />Authenticode ist nicht mehr der bevorzugte Typ des Zeitstempels. Die Unterstützung für Authenticode-Zeitstempel wird möglicherweise in Zukunft entfernt. Es wird empfohlen, stattdessen RFC 3161 zu verwenden.</blockquote><br /> | 
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt></dl> | Gibt einen RFC 3161-kompatiblen Zeitstempel an.<br /> | 




 

</dd> <dt>

*dwIndex* \[ In\]
</dt> <dd>

Gibt die Sequenznummer der Signatur an, der der Zeitstempel hinzugefügt wird. Wenn dieser Wert null (0) ist, wird die äußere Signatur mit einem Zeitstempel versehen.

</dd> <dt>

*pSubjectInfo* \[ In\]
</dt> <dd>

Die Adresse einer [**SIGNER \_ SUBJECT \_ INFO-Struktur,**](signer-subject-info.md) die das Subjekt darstellt, für das ein Zeitstempel verwendet werden soll.

</dd> <dt>

*pwszHttpTimeStamp* \[ In\]
</dt> <dd>

Die Adresse einer auf NULL beendeten Unicode-Zeichenfolge, die die URL eines Zeitstempelservers enthält.

</dd> <dt>

*pszAlgorithmOid* \[ In\]
</dt> <dd>

Ein Hashalgorithmus, der zum Ausführen von RFC 3161-konformen Zeitstempeln verwendet werden soll. Dieser Parameter wird für Authenticode-Zeitstempel ignoriert.

</dd> <dt>

*psRequest* \[ in, optional\]
</dt> <dd>

Optional. Die Adresse einer [**CRYPT \_ ATTRIBUTES-Struktur,**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) die zusätzliche Attribute enthält, die der Zeitstempelanforderung hinzugefügt werden.

Dieser Parameter ist optional und kann **NULL sein,** wenn er nicht enthalten ist.

</dd> <dt>

*pSipData* \[ in, optional\]
</dt> <dd>

Optional. Ein 32-Bit-Wert, der als zusätzliche Daten an DIE-Funktionen [*(Subject Interface Package)*](../secgloss/s-gly.md) übergeben wird. Das Format und der Inhalt dieses Parameters werden vom SIP-Anbieter definiert.

Dieser Parameter ist optional und kann **NULL sein,** wenn er nicht enthalten ist.

</dd> <dt>

*ppSignerContext* \[ out\]
</dt> <dd>

Optional. Die Adresse eines Zeigers auf die [**SIGNER \_ CONTEXT-Struktur,**](signer-context.md) die das signierte BLOB enthält. Wenn Sie die **SIGNER \_ CONTEXT-Struktur** nicht mehr verwenden, geben Sie sie frei, indem Sie die [**SignerFreeSignerContext-Funktion**](signerfreesignercontext.md) aufrufen.

</dd> <dt>

*pCryptoPolicy* \[ in, optional\]
</dt> <dd>

Falls vorhanden, ein Zeiger auf eine [**CERT \_ STRONG SIGN \_ \_ PARA-Struktur,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) die die Parameter enthält, die zum Überprüfen auf starke Signaturen verwendet werden. Der Zeitstempel muss diese kryptografische Richtlinie bestehen.

</dd> <dt>

*Erhalten* 
</dt> <dd>

Reserviert. Dieser Wert muss NULL **sein.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt sie S \_ OK zurück.

Wenn die Funktion fehlschlägt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Mögliche Fehlercodes, die von dieser Funktion zurückgegeben werden, sind u. a. folgende. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).




| Rückgabecode | Beschreibung | 
|-------------|-------------|
| <dl><dt><strong>E_INVALIDARG</strong></dt></dl> | Dieser Fehler kann für die folgenden Bedingungen zurückgegeben werden:<br /><ul><li>Sie müssen entweder <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> oder <strong>SIGNER_TIMESTAMP_RFC3161</strong> <em>dwFlags-Parameter</em> festlegen.</li><li>Der <em>pReserved-Parameter</em> muss NULL <strong>sein.</strong></li><li>Wenn Sie das <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> im <em>dwFlags-Parameter</em> festlegen, müssen Sie den <em>dwIndex-Parameter</em> auf 0 (null) festlegen.</li></ul> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> <dt>

[**SignerTimeStampEx2**](signertimestampex2.md)
</dt> </dl>

 

 
