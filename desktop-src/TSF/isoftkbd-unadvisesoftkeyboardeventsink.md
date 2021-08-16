---
title: ISoftKbd UnadviseSoftKeyboardEventSink-Methode (Softkbdc.h)
description: Die ISoftKbd UnadviseSoftKeyboardEventSink-Methode entfernt eine Softtastaturereignissenke.
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- UnadviseSoftKeyboardEventSink-Methode Textdienstframework
- UnadviseSoftKeyboardEventSink-Methode Textdienstframework , ISoftKbd-Schnittstelle
- ISoftKbd-Schnittstelle Textdienstframework , UnadviseSoftKeyboardEventSink-Methode
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
ms.openlocfilehash: 90552c09e47d8a51f413f0588b12c8da5d44e665a6a5a51a79dc31717c6d56c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877110"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a>ISoftKbd::UnadviseSoftKeyboardEventSink-Methode

Die **ISoftKbd::UnadviseSoftKeyboardEventSink-Methode** entfernt eine Softtastatur-Ereignissenke.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tid* \[ In\]
</dt> <dd>

Bezeichner des Clients, der die Softtastatur-Ereignissenke besitzt. Dieser Wert wurde übergeben, als die Ereignissenke mit [ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md)installiert wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                                   | BESCHREIBUNG                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Die Methode war erfolgreich.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Der *tid-Parameter* ist ungültig.<br/>                    |
| <dl> <dt>**CONNECT \_ E \_ NOCONNECTION**</dt> </dl> | Die durch *tid identifizierte* Advise-Senke wurde nicht gefunden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | TSF 1.0 auf Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





