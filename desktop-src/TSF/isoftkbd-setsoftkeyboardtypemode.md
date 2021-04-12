---
title: Icdkbd setsoft keyboardtypemode-Methode (Software-DC. h)
description: Die isoftkbd setsoftkeyboardtypemode-Methode legt den typmodus für eine weiche Tastatur fest.
ms.assetid: 0b5b5056-59b3-41c7-bc43-70b5c3cd51c2
keywords:
- Setsoft keyboardtypemode-Methode, Text Dienste-Framework
- Setsoft keyboardtypemode-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, setsoft keyboardtypemode-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55c01465debc42926888e2cb12a3a5b9d884498b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478210"
---
# <a name="isoftkbdsetsoftkeyboardtypemode-method"></a>ISOFT kbd:: setsoft keyboardtypemode-Methode

Die **isoftkbd:: setsoftkeyboardtypemode** -Methode legt den typmodus für eine weiche Tastatur fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSoftKeyboardTypeMode(
  [in] TYPEMODE TypeMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typemode* \[ in\]
</dt> <dd>

Der typmodus. Mögliche Werte sind für die [**typemode**](typemode.md) -Enumeration definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | BESCHREIBUNG                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>           |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *typemode* -Parameter ist ungültig.<br/> |



 

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

[**Iweichkbd:: getsoftware keyboardtypemode**](isoftkbd-getsoftkeyboardtypemode.md)
</dt> <dt>

[**Typemode**](typemode.md)
</dt> </dl>

 

 





