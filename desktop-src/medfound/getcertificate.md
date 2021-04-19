---
description: Ruft ein Zertifikat für einen Anzeigetreiber ab.
ms.assetid: eceaf151-1dae-4ff0-9139-7f1789f6c682
title: GetCertificate-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificate
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 30cb17345177b552e51120afd00758a3f6886584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344979"
---
# <a name="getcertificate-function"></a>GetCertificate-Funktion

> [!IMPORTANT]
> Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen. Anwendungen sollten diese Funktion nicht aufzurufen.

 

Ruft ein Zertifikat für einen Anzeigetreiber ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI GetCertificate(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ BYTE                     *pbCertificate,
  _Out_ ULONG                    ulCertificateLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstrindevicename* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**Unicode- \_ Zeichen**](/windows/win32/api/subauth/ns-subauth-unicode_string) folgen Struktur, die den Namen des Anzeige Geräts enthält, wie von der [**getmonitorinfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) -Funktion zurückgegeben.

</dd> <dt>

*ctpvpcertifialisietype* \[ in\]
</dt> <dd>

Der Zertifikattyp, der als Member der **dxgkmdt- \_ \_ Zertifikattyp** -Enumeration angegeben wird.

</dd> <dt>

*pbcertificate* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der das Zertifikat empfängt.

</dd> <dt>

*ulcertifialisielength* \[ vorgenommen\]
</dt> <dd>

Die Größe des *pbcertificate* -Puffers in Bytes. Um die Größe des Zertifikats abzurufen, nennen Sie [**getcertifikatesize**](getcertificatesize.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben. Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Anwendungen sollten anstelle dieser Funktion die [**IOPMVideoOutput:: startinitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) -Methode aufrufen.

Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[OPM-Funktionen](opm-functions.md)
</dt> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> </dl>

 

 
