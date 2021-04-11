---
description: Zeitstempel des angegebenen Subjekts und unterstützen das Festlegen von Zeitstempeln für mehrere Signaturen.
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
ms.openlocfilehash: 538b92160ddbbb9ca9515a65575fdea67990de5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128089"
---
# <a name="signertimestampex3-function"></a>SignerTimeStampEx3-Funktion

Der **SignerTimeStampEx3** -Funktions Zeitstempel des angegebenen Subjekts und unterstützt das Festlegen von Zeitstempeln für mehrere Signaturen.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.

 

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

*dwFlags* \[ in\]
</dt> <dd>

Flag, das den Typ des zu generierenden Zeitstempels angibt. Dieser Parameter kann einen der folgenden Werte annehmen. Die Werte schließen sich gegenseitig aus.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </dl></td>
<td>Gibt einen Authenticode-Zeitstempel an.<br/>
<blockquote>
[!Note]<br />
Authenticode ist nicht mehr der bevorzugte Typ des Zeitstempels. Die Unterstützung für Authenticode-Zeitstempel kann in Zukunft entfernt werden. Es wird empfohlen, stattdessen RFC 3161 zu verwenden.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </dl></td>
<td>Gibt einen RFC 3161 – kompatiblen Zeitstempel an.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Gibt die Sequenznummer der Signatur an, der der Zeitstempel hinzugefügt wird. Wenn dieser Wert 0 (null) ist, wird die äußere Signatur mit einem Zeitstempel versehen.

</dd> <dt>

*psubjetinfo* \[ in\]
</dt> <dd>

Die Adresse einer [**Signatur Geber- \_ \_ Informations**](signer-subject-info.md) Struktur, die den Betreff darstellt, der mit einem Zeitstempel versehen werden soll.

</dd> <dt>

*pwszhttptimestamp* \[ in\]
</dt> <dd>

Die Adresse einer null-terminierten Unicode-Zeichenfolge, die die URL eines Zeitstempel Servers enthält.

</dd> <dt>

*pszalgorithmuid* \[ in\]
</dt> <dd>

Ein Hash Algorithmus, der zum Ausführen von RFC 3161 – kompatiblen Zeitstempeln verwendet werden soll. Dieser Parameter wird bei Authenticode-Zeitstempeln ignoriert.

</dd> <dt>

*psrequest* \[ in, optional\]
</dt> <dd>

Dies ist optional. Die Adresse einer [**crypt- \_ Attribut**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) Struktur, die zusätzliche Attribute enthält, die der Zeitstempel Anforderung hinzugefügt werden.

Dieser Parameter ist optional und kann **null** sein, wenn er nicht eingeschlossen ist.

</dd> <dt>

*psipdata* \[ in, optional\]
</dt> <dd>

Dies ist optional. Ein 32-Bit-Wert, der als zusätzliche Daten an SIP-Funktionen ( [*Subject Interface Package, subject Interface Package*](../secgloss/s-gly.md) ) weitergeleitet wird. Das Format und der Inhalt dieses Parameters werden vom SIP-Anbieter definiert.

Dieser Parameter ist optional und kann **null** sein, wenn er nicht eingeschlossen ist.

</dd> <dt>

*ppsignercontext* \[ vorgenommen\]
</dt> <dd>

Dies ist optional. Die Adresse eines Zeigers auf die [**Signatur Geber- \_ Kontext**](signer-context.md) Struktur, die das signierte BLOB enthält. Wenn Sie die Signatur Geber- **\_ Kontext** Struktur nicht mehr verwenden, können Sie Sie durch Aufrufen der [**signerfreesignercontext**](signerfreesignercontext.md) -Funktion freigeben.

</dd> <dt>

*pcryptopolicy* \[ in, optional\]
</dt> <dd>

Falls vorhanden, ein Zeiger auf eine [**CERT \_ Strong \_ Sign \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) Structure-Struktur, die die Parameter enthält, die für die Überprüfung auf starke Signaturen verwendet werden. Der Zeitstempel muss diese Kryptografierichtlinie bestehen.

</dd> <dt>

*erhaltene* 
</dt> <dd>

Reserviert. Dieser Wert muss **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion S \_ OK zurück.

Wenn die Funktion fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Mögliche Fehlercodes, die von dieser Funktion zurückgegeben werden, sind u. a. die folgenden. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rückgabecode</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> </dl></td>
<td>Dieser Fehler kann unter folgenden Bedingungen zurückgegeben werden:<br/>
<ul>
<li>Sie müssen entweder <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> oder <strong>SIGNER_TIMESTAMP_RFC3161</strong> für den <em>dwFlags</em> -Parameter festlegen.</li>
<li>Der <em></em> beibehaltene Parameter muss <strong>null</strong>sein.</li>
<li>Wenn Sie das <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> -Flag im <em>dwFlags</em> -Parameter festgelegt haben, müssen Sie den <em>dwIndex</em> -Parameter auf 0 (null) festlegen.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signertimestamp**](signertimestamp.md)
</dt> <dt>

[**Signertimestampex**](signertimestampex.md)
</dt> <dt>

[**SignerTimeStampEx2**](signertimestampex2.md)
</dt> </dl>

 

 
