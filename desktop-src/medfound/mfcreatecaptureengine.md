---
description: Erstellt eine Instanz der Erfassungs-Engine.
ms.assetid: 4B0C9DD6-135D-4412-A585-7E98A84101B5
title: MFCreateCaptureEngine-Funktion
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
ms.openlocfilehash: 18d264b30b8f3ed4d06e80f236908dd7bc81dbe96c4eb9c3231fa330331e34f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940250"
---
# <a name="mfcreatecaptureengine-function"></a>MFCreateCaptureEngine-Funktion

\[MFCreateCaptureEngine wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. \]

Erstellt eine Instanz der Erfassungs-Engine.

## <a name="syntax"></a>Syntax


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppCaptureEngine* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**INTERFACESCaptureEngine-Schnittstelle.**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) Der Aufrufer muss die Schnittstelle freigeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird S \_ OK zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Funktion verfügt über keine zugeordnete Importbibliothek und ist nicht in einer öffentlichen Headerdatei deklariert. Sie müssen die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch mit MFCaptureEngine.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                        |
| DLL<br/>                      | <dl> <dt>MFCaptureEngine.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Functions](media-foundation-functions.md)
</dt> </dl>

 

 
