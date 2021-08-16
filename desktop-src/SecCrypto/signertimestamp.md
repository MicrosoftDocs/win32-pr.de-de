---
description: Stempelt den angegebenen Betreff mit einem Zeitstempel. Diese Funktion unterstützt den Authenticode-Zeitstempel. Verwenden Sie die SignerTimeStampEx2-Funktion, um den Zeitstempel der X.509 Public Key Infrastructure (RFC 3161) durchzuführen.
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: SignerTimeStamp-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStamp
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: cb33852cb2860a29d43a41b2331a910a098384b872e972a74cf94f627bebf75a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898296"
---
# <a name="signertimestamp-function"></a>SignerTimeStamp-Funktion

Die **SignerTimeStamp-Funktion** stempelt den angegebenen Betreff. Diese Funktion unterstützt den Authenticode-Zeitstempel. Verwenden Sie die [**SignerTimeStampEx2-Funktion,**](signertimestampex2.md) um den Zeitstempel der X.509 Public Key Infrastructure (RFC 3161) durchzuführen.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit Mssign32.dll.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI SignerTimeStamp(
  _In_     SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_     LPCWSTR             pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES   psRequest,
  _In_opt_ LPVOID              pSipData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSubjectInfo* \[ In\]
</dt> <dd>

Die Adresse einer [**SIGNER \_ SUBJECT \_ INFO-Struktur,**](signer-subject-info.md) die das Subjekt darstellt, für das ein Zeitstempel verwendet werden soll.

</dd> <dt>

*pwszHttpTimeStamp* \[ In\]
</dt> <dd>

Die Adresse einer auf NULL beendeten Unicode-Zeichenfolge, die die URL eines Zeitstempelservers enthält.

</dd> <dt>

*psRequest* \[ in, optional\]
</dt> <dd>

Die Adresse einer [**CRYPT \_ ATTRIBUTES-Struktur,**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) die zusätzliche Attribute enthält, die der Zeitstempelanforderung hinzugefügt werden.

Dieser Parameter ist optional und kann **NULL sein,** wenn er nicht enthalten ist.

</dd> <dt>

*pSipData* \[ in, optional\]
</dt> <dd>

Ein 32-Bit-Wert, der als zusätzliche Daten an DIE SIP-Funktionen übergeben wird. Das Format und der Inhalt dieses wird vom SIP-Anbieter definiert.

Dieser Parameter ist optional und kann **NULL sein,** wenn er nicht enthalten ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt sie S \_ OK zurück.

Wenn die Funktion fehlschlägt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
