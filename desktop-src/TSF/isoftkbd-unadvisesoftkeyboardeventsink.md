---
title: ISOFT kbd unadvisesoftkeyboardeventsink-Methode (Software-BDC. h)
description: Die Methode isoftkbd unadvisesoftkeyboardeventsink entfernt eine weiche Tastaturereignis Senke.
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- Unadvisesoftkeyboardeventsink-Methode, Text Dienste-Framework
- Unadvisesoftkeyboardeventsink-Methode Text Dienst Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, unadvisesoftkeyboardeventsink-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.UnadviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a77129d1b5df024964af4ab19318963708d4b3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742785"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a>Iweichkbd:: unadvisesoftkeyboardeventsink-Methode

Die **isoftkbd:: unadvisesoftkeyboardeventsink** -Methode entfernt eine weiche Tastaturereignis Senke.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TID* \[ in\]
</dt> <dd>

Der Bezeichner des Clients, der die weiche Tastaturereignis Senke besitzt. Dieser Wert wurde übermittelt, als die Ereignis Senke mithilfe von iSoftware installiert wurde: [: advisesoftkeyboarabventsink](isoftkbd-advisesoftkeyboardeventsink.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                                   | BESCHREIBUNG                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Die Methode war erfolgreich.<br/>                         |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>            | Der *TID* -Parameter ist ungültig.<br/>                    |
| <dl> <dt>**\_E \_ NOCONNECTION verbinden**</dt> </dl> | Die von *TID* identifizierte Benachrichtigungs Senke wurde nicht gefunden.<br/> |



 

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

[Iweichkbd:: advisesoftkeyboarabventsink](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





