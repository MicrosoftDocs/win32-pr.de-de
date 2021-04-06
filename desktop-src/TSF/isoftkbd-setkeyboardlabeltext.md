---
title: Icdkbd setkeyboardlabeltext-Methode (Software BDC. h)
description: Die isoftkbd setkeyboardlabeltext-Methode legt den Beschriftungs Text aus dem Layout für eine weiche Tastatur fest.
ms.assetid: 86c45c37-fe50-4596-b4c9-960de760a2e0
keywords:
- Setkeyboardlabeltext-Methode, Text Dienste-Framework
- Setkeyboardlabeltext-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, setkeyboardlabeltext-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelText
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862341182b9c97a751ba4a130566d5cf18437c2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742792"
---
# <a name="isoftkbdsetkeyboardlabeltext-method"></a>ISOFT kbd:: setkeyboardlabeltext-Methode

Die **isoftkbd:: setkeyboardlabeltext** -Methode legt den Beschriftungs Text aus dem Layout für eine weiche Tastatur fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetKeyboardLabelText(
  [in] HKL hKl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HKL* \[ in\]
</dt> <dd>

Handle, das zum Abrufen des installierten Layouts für die weiche Tastatur verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | BESCHREIBUNG                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>      |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *HKL* -Parameter ist ungültig.<br/> |



 

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

[**Icdkbd:: setkeyboardlabeltextkombination**](isoftkbd-setkeyboardlabeltextcombination.md)
</dt> </dl>

 

 





