---
description: Erstellt einen bytestreamhandler für die MP3-Medienquelle.
ms.assetid: A213BAEF-D98F-485B-8840-BE131E9B26C0
title: MFCreateMP3ByteStreamPlugin-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateMP3ByteStreamPlugin
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0b8bcd153471ddd8acd648d5775b4dc964693a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348233"
---
# <a name="mfcreatemp3bytestreamplugin-function"></a>MFCreateMP3ByteStreamPlugin-Funktion

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Stattdessen sollten Anwendungen den [quellresolver](source-resolver.md) verwenden, um die MP3-Medienquelle zu erstellen.\]

Erstellt einen bytestreamhandler für die MP3-Medienquelle.

## <a name="syntax"></a>Syntax


```C++
HRESULT __stdcall MFCreateMP3ByteStreamPlugin(
  _In_  REFIID riid,
  _Out_ LPVOID *ppvHandler
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*riid* \[ in\]
</dt> <dd>

Der Schnittstellenbezeichner (Interface Identifier, IID) der angeforderten Schnittstelle. Legen Sie diesen Parameter auf **IID \_ imfbytestreamhandler** fest, um einen Zeiger auf die [**imfbytestreamhandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) -Schnittstelle zu erhalten.

</dd> <dt>

*ppvhandler* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die-Schnittstelle. Der Aufrufer muss die-Schnittstelle freigeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit mf.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows Vista<br/>                             |
| Ende des Supports (Server)<br/>    | Windows Server 2008<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Funktionen](media-foundation-functions.md)
</dt> <dt>

[Schema Handler und Byte-Stream Handler](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Quellresolver](source-resolver.md)
</dt> </dl>

 

 
