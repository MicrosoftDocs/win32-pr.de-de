---
description: Zeitstempel des angegebenen Subjekts und gibt optional einen Zeiger auf eine Signatur Geber- \_ Kontext Struktur zurück, die einen Zeiger auf ein BLOB enthält.
ms.assetid: f3a910f6-64f8-4cf5-b008-2a16872f9a98
title: Signertimestampex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a4562ca84f8b3376a22d00a5e9501947152ed875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758772"
---
# <a name="signertimestampex-function"></a>Signertimestampex-Funktion

Die **signertimestampex** -Funktion stempelt das angegebene Subjekt und gibt optional einen Zeiger auf eine Signatur Geber- [**\_ Kontext**](signer-context.md) Struktur zurück, die einen Zeiger auf ein [*BLOB*](../secgloss/b-gly.md)enthält. Diese Funktion unterstützt das Zeitstempel von Authenticode. Verwenden Sie die [**SignerTimeStampEx2**](signertimestampex2.md) -Funktion, um die X. 509-Zeitstempel für die Public Key-Infrastruktur (RFC 3161) auszuführen.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI SignerTimeStampEx(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Reserviert. Dieser Parameter muss auf 0 (null) festgelegt werden.

</dd> <dt>

*psubjetinfo* \[ in\]
</dt> <dd>

Die Adresse einer [**Signatur Geber- \_ \_ Informations**](signer-subject-info.md) Struktur, die den Betreff darstellt, der mit einem Zeitstempel versehen werden soll.

</dd> <dt>

*pwszhttptimestamp* \[ in\]
</dt> <dd>

Die Adresse einer null-terminierten Unicode-Zeichenfolge, die die URL eines Zeitstempel Servers enthält.

</dd> <dt>

*psrequest* \[ in\]
</dt> <dd>

Dies ist optional. Die Adresse einer [**crypt- \_ Attribut**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) Struktur, die zusätzliche Attribute enthält, die der Zeitstempel Anforderung hinzugefügt werden.

Dieser Parameter ist optional und kann **null** sein, wenn er nicht eingeschlossen ist.

</dd> <dt>

*psipdata* \[ in\]
</dt> <dd>

Dies ist optional. Ein 32-Bit-Wert, der als zusätzliche Daten an SIP-Funktionen ( [*Subject Interface Package, subject Interface Package*](../secgloss/s-gly.md) ) weitergeleitet wird. Das Format und der Inhalt dieses Parameters werden vom SIP-Anbieter definiert.

Dieser Parameter ist optional und kann **null** sein, wenn er nicht eingeschlossen ist.

</dd> <dt>

*ppsignercontext* \[ vorgenommen\]
</dt> <dd>

Dies ist optional. Die Adresse eines Zeigers auf die [**Signatur Geber- \_ Kontext**](signer-context.md) Struktur, die das signierte BLOB enthält. Wenn Sie die Signatur Geber- **\_ Kontext** Struktur nicht mehr verwenden, können Sie Sie durch Aufrufen der [**signerfreesignercontext**](signerfreesignercontext.md) -Funktion freigeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion S \_ OK zurück.

Wenn die Funktion fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>


</dt> <dt>

[**Signertimestamp**](signertimestamp.md)
</dt> </dl>

 

 
