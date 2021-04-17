---
title: ISoftware Type getsoft keyboardtypemode-Methode (Software-DC. h)
description: Die isoftkbd getsoftkeyboardtypemode-Methode ruft den typmodus für eine weiche Tastatur ab.
ms.assetid: 77294652-b82e-4b69-bb55-5ebebc3c97c7
keywords:
- Getsoft keyboardtypemode-Methode, Text Dienste-Framework
- Getsoft keyboardtypemode-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, getsoft keyboardtypemode-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6aad6d60c50ee0050cf418018dd6db1c7a33efc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391495"
---
# <a name="isoftkbdgetsoftkeyboardtypemode-method"></a>ISOFT kbd:: getsoft keyboardtypemode-Methode

Die **isoftkbd:: getsoftkeyboardtypemode** -Methode ruft den typmodus für eine weiche Tastatur ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoftKeyboardTypeMode(
  [out] TYPEMODE *lpTypeMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lptypemode* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Puffer, in dem diese Methode den typmodus abruft. Mögliche Werte sind für die [**typemode**](typemode.md) -Enumeration definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | BESCHREIBUNG                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>             |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *lptypemode* -Parameter ist ungültig.<br/> |



 

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

[**Icdkbd:: setsoft keyboardtypemode**](isoftkbd-setsoftkeyboardtypemode.md)
</dt> <dt>

[**Typemode**](typemode.md)
</dt> </dl>

 

 





