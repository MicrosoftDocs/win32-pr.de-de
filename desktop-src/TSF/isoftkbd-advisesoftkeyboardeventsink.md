---
title: ISOFT kbd advisesoftkeyboardeventsink-Methode (Software BDC. h)
description: Die isoftkbd advisesoftkeyboardeventsink-Methode installiert eine weiche Tastaturereignis Senke, um onkeyselection-Benachrichtigungen von der Soft Tastatur zu verarbeiten.
ms.assetid: f7a441dc-7bef-4fc0-bc62-c153a55a844c
keywords:
- Advisesoftkeyboardeventsink-Methode, Text Dienste-Framework
- Advisesoftkeyboardeventsink-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, advisesoftkeyboardeventsink-Methode
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
ms.openlocfilehash: 6ab17de2104c6104b044f027152cfc45cca968b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392107"
---
# <a name="isoftkbdadvisesoftkeyboardeventsink-method"></a>ISOFT kbd:: advisesoftkeyboardeventsink-Methode

Die **isoftkbd:: advisesoftkeyboardeventsink** -Methode installiert eine weiche Tastaturereignis Senke, um onkeyselection-Benachrichtigungen von der Soft Tastatur zu verarbeiten.

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

*dwkeyboardid* \[ in\]
</dt> <dd>

Der Bezeichner der Soft Tastatur.

</dd> <dt>

*riid* \[ in\]
</dt> <dd>

Der Schnittstellen Bezeichner für die Sink-Schnittstelle.

</dd> <dt>

*Punk* \[ in\]
</dt> <dd>

Zeiger auf [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) für die Senke-Schnittstelle, die von *riid* angegeben wird. Dieser Parameter kann nicht auf **null** festgelegt werden.

</dd> <dt>

*pdwcookie* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den Puffer, in dem diese Methode das weiche Tastatur-"Cookie" abruft, das für die Verbindung mit dem Client verwendet wird. Das Cookie muss für jede Verbindung eindeutig sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | BESCHREIBUNG                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>          |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Mindestens ein Parameter ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Software-Domänen Controller. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Software. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iweichkbd**](isoftkbd.md)
</dt> <dt>

[**Iweichkbd:: unadvisesoftkeyboarabventsink**](isoftkbd-unadvisesoftkeyboardeventsink.md)
</dt> </dl>

 

