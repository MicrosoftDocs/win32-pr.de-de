---
title: Icdkbd setkeyboardlabeltextcombination-Methode (Software-DC. h)
description: Mit der isoftkbd setkeyboardlabeltextcombination-Methode wird eine Kombination aus Bezeichnung und Text festgelegt, mit der eine weiche Tastatur beschrieben wird.
ms.assetid: fe054eae-1a44-41ad-9a44-bc0b46df7c7b
keywords:
- Setkeyboardlabeltextcombination-Methode, Text Dienste-Framework
- Setkeyboardlabeltextcombination-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, setkeyboardlabeltextcombination-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelTextCombination
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98dad124455625f0da3ada1a717c692437398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346106"
---
# <a name="isoftkbdsetkeyboardlabeltextcombination-method"></a>Icdkbd:: setkeyboardlabeltextcombination-Methode

Die **isoftkbd:: setkeyboardlabeltextcombination** -Methode legt eine Kombination aus Bezeichnung und Text fest, mit der eine weiche Tastatur beschrieben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetKeyboardLabelTextCombination(
  [in] DWORD nModifierCombination
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nmodifierkombination* \[ in\]
</dt> <dd>

Eine Kombination aus Bezeichnung und Text, mit der die weiche Tastatur beschrieben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | BESCHREIBUNG                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>                       |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *nmodifiercombination* -Parameter ist ungültig.<br/> |



 

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

[**Icdkbd:: setkeyboardlabeltext**](isoftkbd-setkeyboardlabeltext.md)
</dt> </dl>

 

 





