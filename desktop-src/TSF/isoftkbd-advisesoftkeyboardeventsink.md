---
title: ISoftKbd AdviseSoftKeyboardEventSink-Methode (Softkbdc.h)
description: Die ISoftKbd AdviseSoftKeyboardEventSink-Methode installiert eine Ereignissenke für die softe Tastatur, um OnKeySelection-Benachrichtigungen von der soft-Tastatur zu verarbeiten.
ms.assetid: f7a441dc-7bef-4fc0-bc62-c153a55a844c
keywords:
- AdviseSoftKeyboardEventSink-Methode Textdienstframework
- AdviseSoftKeyboardEventSink-Methode Textdienstframework , ISoftKbd-Schnittstelle
- ISoftKbd-Schnittstelle Textdienstframework , AdviseSoftKeyboardEventSink-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.AdviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a3a734e66bb319bb7e24b6ca3b27299f984f33b98772c1cc446c40e3f27426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877987"
---
# <a name="isoftkbdadvisesoftkeyboardeventsink-method"></a>ISoftKbd::AdviseSoftKeyboardEventSink-Methode

Die **ISoftKbd::AdviseSoftKeyboardEventSink-Methode** installiert eine Softtastaturereignissenke, um OnKeySelection-Benachrichtigungen von der soft-Tastatur zu verarbeiten.

## <a name="syntax"></a>Syntax


```C++
HRESULT AdviseSoftKeyboardEventSink(
  [in]  DWORD    dwKeyboardId,
  [in]  REFIID   riid,
  [in]  IUnknown *punk,
  [out] DWORD    *pdwCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwKeyboardId* \[ In\]
</dt> <dd>

Bezeichner der soft-Tastatur.

</dd> <dt>

*riid* \[ In\]
</dt> <dd>

Schnittstellenbezeichner für die Senkenschnittstelle.

</dd> <dt>

*im NSD* \[ In\]
</dt> <dd>

Zeiger auf [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) für die durch *riid* angegebene Senkenschnittstelle. Dieser Parameter kann nicht auf **NULL** festgelegt werden.

</dd> <dt>

*pdwCookie* \[ out\]
</dt> <dd>

Zeiger auf den Puffer, in dem diese Methode das Softtastaturcookie abruft, das für die Verbindung mit dem Client verwendet wird. Das Cookie muss für jede Verbindung eindeutig sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | Beschreibung                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Mindestens ein Parameter ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | TSF 1.0 on Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::UnadviseSoftKeyboardEventSink**](isoftkbd-unadvisesoftkeyboardeventsink.md)
</dt> </dl>

 

