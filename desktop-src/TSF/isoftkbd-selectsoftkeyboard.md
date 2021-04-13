---
title: Iweichkbd selectsoft Keyboard-Methode (Software-DC. h)
description: Die isoftkbd selectsoftkeyboard-Methode wählt die angegebene weiche Tastatur aus.
ms.assetid: 7e85d346-3741-457d-aadd-11d3a6710e85
keywords:
- Selectsoft Keyboard-Methode, Text Dienste-Framework
- Selectsoft Keyboard-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, selectsoft Keyboard-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.SelectSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda9399297e9776e7fbd7cecb364fd7f6cd4604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518515"
---
# <a name="isoftkbdselectsoftkeyboard-method"></a>ISOFT kbd:: selectsoft Keyboard-Methode

Die **isoftkbd:: selectsoftkeyboard** -Methode wählt die angegebene weiche Tastatur aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT SelectSoftKeyboard(
  [in] DWORD dwKeyboardId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwkeyboardid* \[ in\]
</dt> <dd>

Der Bezeichner der ausgewählten Bildschirmtastatur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | BESCHREIBUNG                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>               |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *dwkeyboardid* -Parameter ist ungültig.<br/> |



 

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
</dt> </dl>

 

 





