---
title: ISoftKbd SetKeyboardLabelTextCombination-Methode (Softkbdc.h)
description: Die ISoftKbd SetKeyboardLabelTextCombination-Methode legt eine Kombination aus Bezeichnung und Text fest, die zum Beschreiben einer soft-Tastatur verwendet wird.
ms.assetid: fe054eae-1a44-41ad-9a44-bc0b46df7c7b
keywords:
- SetKeyboardLabelTextCombination-Methode Textdienstframework
- SetKeyboardLabelTextCombination-Methode Textdienstframework , ISoftKbd-Schnittstelle
- ISoftKbd-Schnittstelle Textdienstframework , SetKeyboardLabelTextCombination-Methode
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
ms.openlocfilehash: 39b01d4335e52bf20aca1b5cd59b5bc1dd926f6c4752f2b0f421e613d48b2f94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952555"
---
# <a name="isoftkbdsetkeyboardlabeltextcombination-method"></a>ISoftKbd::SetKeyboardLabelTextCombination-Methode

Die **ISoftKbd::SetKeyboardLabelTextCombination-Methode** legt eine Kombination aus Bezeichnung und Text fest, die zum Beschreiben einer soft-Tastatur verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetKeyboardLabelTextCombination(
  [in] DWORD nModifierCombination
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nModifierCombination* \[ In\]
</dt> <dd>

Kombination aus Bezeichnung und Text, die zum Beschreiben der soft-Tastatur verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | Beschreibung                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der *nModifierCombination-Parameter* ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | TSF 1.0 auf Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::SetKeyboardLabelText**](isoftkbd-setkeyboardlabeltext.md)
</dt> </dl>

 

 





