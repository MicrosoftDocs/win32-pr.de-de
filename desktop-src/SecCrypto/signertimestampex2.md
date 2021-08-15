---
description: Stempelt den angegebenen Betreff und gibt optional einen Zeiger auf eine SIGNER CONTEXT-Struktur zurück, die einen Zeiger \_ auf ein BLOB enthält. Diese Funktion kann verwendet werden, um X.509 Public Key Infrastructure, RFC 3161&\# 8211;kompatibel, Zeitstempel durchzuführen.
ms.assetid: fb82545b-c00f-44eb-96f4-aa27a125c8d9
title: SignerTimeStampEx2-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c5a9bfc81c3196657f611c9263e0d957ca867a64479b34900dce7078237e195f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898269"
---
# <a name="signertimestampex2-function"></a>SignerTimeStampEx2-Funktion

Die **SignerTimeStampEx2-Funktion** stempelt den angegebenen Betreff und gibt optional einen Zeiger auf eine [**SIGNER \_ CONTEXT-Struktur**](signer-context.md) zurück, die einen Zeiger auf ein [*BLOB enthält.*](../secgloss/b-gly.md) Diese Funktion kann verwendet werden, um X.509 Public Key Infrastructure, RFC 3161-konforme Zeitstempel, durchzuführen.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit Mssign32.dll.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI SignerTimeStampEx2(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       ALG_ID              dwAlgId,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Ein Wert, der den Typ des zu generierenden Zeitstempels angibt. Dieser Parameter kann einen der folgenden Werte annehmen. Die Werte schließen sich gegenseitig aus.



| Wert                                                                                                                                                                                                          | Bedeutung                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt>**SIGNER \_ TIMESTAMP \_ AUTHENTICODE**</dt> </dl> | Gibt einen Authenticode-Zeitstempel an.<br/>       |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt>**SIGNATURER \_ TIMESTAMP \_ RFC3161**</dt> </dl>                | Gibt einen RFC 3161-kompatiblen Zeitstempel an.<br/> |



 

</dd> <dt>

*pSubjectInfo* \[ In\]
</dt> <dd>

Die Adresse einer [**SIGNER \_ SUBJECT \_ INFO-Struktur,**](signer-subject-info.md) die das Subjekt darstellt, für das ein Zeitstempel verwendet werden soll.

</dd> <dt>

*pwszHttpTimeStamp* \[ In\]
</dt> <dd>

Die Adresse einer auf NULL beendeten Unicode-Zeichenfolge, die die URL eines Zeitstempelservers enthält.

</dd> <dt>

*dwAlgId* \[ In\]
</dt> <dd>

Gibt einen Hashalgorithmus an, der zum Ausführen von RFC 3161-kompatiblen Zeitstempeln verwendet werden soll. Dieser Parameter wird für Authenticode-Zeitstempel ignoriert.

</dd> <dt>

*psRequest* \[ In\]
</dt> <dd>

Optional. Die Adresse einer [**CRYPT \_ ATTRIBUTES-Struktur,**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) die zusätzliche Attribute enthält, die der Zeitstempelanforderung hinzugefügt werden.

Dieser Parameter ist optional und kann **NULL sein,** wenn er nicht enthalten ist.

</dd> <dt>

*pSipData* \[ In\]
</dt> <dd>

Optional. Ein 32-Bit-Wert, der als zusätzliche Daten an DIE-Funktionen [*(Subject Interface Package)*](../secgloss/s-gly.md) übergeben wird. Das Format und der Inhalt dieses Parameters werden vom SIP-Anbieter definiert.

Dieser Parameter ist optional und kann **NULL sein,** wenn er nicht enthalten ist.

</dd> <dt>

*ppSignerContext* \[ out\]
</dt> <dd>

Optional. Die Adresse eines Zeigers auf die [**SIGNER \_ CONTEXT-Struktur,**](signer-context.md) die das signierte BLOB enthält. Wenn Sie die **SIGNER \_ CONTEXT-Struktur** nicht mehr verwenden, geben Sie sie frei, indem Sie die [**SignerFreeSignerContext-Funktion**](signerfreesignercontext.md) aufrufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt sie S \_ OK zurück.

Wenn die Funktion fehlschlägt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> </dl>

 

 
