---
description: Zeitstempel des angegebenen Subjekts. Diese Funktion unterstützt das Zeitstempel von Authenticode. Verwenden Sie die SignerTimeStampEx2-Funktion, um die X. 509-Zeitstempel für die Public Key-Infrastruktur (RFC 3161) auszuführen.
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: Signertimestamp-Funktion
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
ms.openlocfilehash: c4c57f231f70477a76b4d4f6156354ebc847a715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960453"
---
# <a name="signertimestamp-function"></a>Signertimestamp-Funktion

Die **signertimestamp** -Funktion stempelt den angegebenen Betreff. Diese Funktion unterstützt das Zeitstempel von Authenticode. Verwenden Sie die [**SignerTimeStampEx2**](signertimestampex2.md) -Funktion, um die X. 509-Zeitstempel für die Public Key-Infrastruktur (RFC 3161) auszuführen.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.

 

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

*psubjetinfo* \[ in\]
</dt> <dd>

Die Adresse einer [**Signatur Geber- \_ \_ Informations**](signer-subject-info.md) Struktur, die den Betreff darstellt, der mit einem Zeitstempel versehen werden soll.

</dd> <dt>

*pwszhttptimestamp* \[ in\]
</dt> <dd>

Die Adresse einer null-terminierten Unicode-Zeichenfolge, die die URL eines Zeitstempel Servers enthält.

</dd> <dt>

*psrequest* \[ in, optional\]
</dt> <dd>

Die Adresse einer [**crypt- \_ Attribut**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) Struktur, die zusätzliche Attribute enthält, die der Zeitstempel Anforderung hinzugefügt werden.

Dieser Parameter ist optional und kann **null** sein, wenn er nicht eingeschlossen ist.

</dd> <dt>

*psipdata* \[ in, optional\]
</dt> <dd>

Ein 32-Bit-Wert, der als zusätzliche Daten an SIP-Funktionen weitergeleitet wird. Das Format und der Inhalt dieser werden vom SIP-Anbieter definiert.

Dieser Parameter ist optional und kann **null** sein, wenn er nicht eingeschlossen ist.

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



 

 
