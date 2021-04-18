---
description: Erstellt eine Instanz der Erfassungs-Engine.
ms.assetid: 4B0C9DD6-135D-4412-A585-7E98A84101B5
title: Mfikreatecaptureengine-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateCaptureEngine
api_type:
- DllExport
api_location:
- MFCaptureEngine.dll
ms.openlocfilehash: a2ff0dbf46ca464c11570c8fe78e0b3dbebe3248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343357"
---
# <a name="mfcreatecaptureengine-function"></a>Mfikreatecaptureengine-Funktion

\[Mfikreatecaptureengine wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. \]

Erstellt eine Instanz der Erfassungs-Engine.

## <a name="syntax"></a>Syntax


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppcaptureengine* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**imfcaptureengine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) -Schnittstelle. Der Aufrufer muss die-Schnittstelle freigeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Funktion verfügt über keine zugeordnete Import Bibliothek und ist nicht in einer öffentlichen Header Datei deklariert. Sie müssen die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit MFCaptureEngine.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                        |
| DLL<br/>                      | <dl> <dt>MFCaptureEngine.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Funktionen](media-foundation-functions.md)
</dt> </dl>

 

 
