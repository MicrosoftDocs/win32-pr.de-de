---
title: Iweichkbd destroysoft keyboardwindow-Methode (Software-DC. h)
description: Die isoftkbd destroysoftkeyboardwindow-Methode zerstört ein weiches Tastatur Fenster.
ms.assetid: 44030934-7b4a-46c1-95ea-709fc9004e43
keywords:
- Destroysoft keyboardwindow-Methode, Text Dienste-Framework
- Destroysoft keyboardwindow-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, destroysoft keyboardwindow-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.DestroySoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb0c460912e8b891503771425fc72484fcc471ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338761"
---
# <a name="isoftkbddestroysoftkeyboardwindow-method"></a>ISOFT kbd::D estroysoft keyboardwindow-Methode

Die **isoftkbd::D estroysoftkeyboardwindow** -Methode zerstört ein weiches Tastatur Fenster.

## <a name="syntax"></a>Syntax


```C++
HRESULT DestroySoftKeyboardWindow();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                | BESCHREIBUNG                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode entfernt ein vorläufiges Tastatur Fenster, das zuvor mit einem Aufrufen von [**isoftkbd:: kreatesoftkeyboardwindow**](isoftkbd-createsoftkeyboardwindow.md)erstellt wurde.

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

[**Iweichkbd:: kreatesoftkeyboardwindow**](isoftkbd-createsoftkeyboardwindow.md)
</dt> </dl>

 

 





