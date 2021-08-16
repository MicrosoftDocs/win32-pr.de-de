---
title: ISoftKbd SetKeyboardLabelText-Methode (Softkbdc.h)
description: Die ISoftKbd-Methode SetKeyboardLabelText legt den Bezeichnungstext aus dem Layout für eine weiche Tastatur fest.
ms.assetid: 86c45c37-fe50-4596-b4c9-960de760a2e0
keywords:
- SetKeyboardLabelText-Textdienstframework
- SetKeyboardLabelText-Methode Textdienstframework , ISoftKbd-Schnittstelle
- ISoftKbd-Schnittstelle Textdienstframework , SetKeyboardLabelText-Methode
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
ms.openlocfilehash: d15e81e2ff29affaa6bf6e87f87410d9c9d3ef7e913998a1bffa1ab6b0dff3fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877415"
---
# <a name="isoftkbdsetkeyboardlabeltext-method"></a>ISoftKbd::SetKeyboardLabelText-Methode

Die **ISoftKbd::SetKeyboardLabelText-Methode** legt den Bezeichnungstext aus dem Layout für eine weiche Tastatur fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetKeyboardLabelText(
  [in] HKL hKl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hKl* \[ In\]
</dt> <dd>

Handle, das zum Abrufen des installierten Layouts für die Softtastatur verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | BESCHREIBUNG                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der *hKl-Parameter* ist ungültig.<br/> |



 

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

[**ISoftKbd::SetKeyboardLabelTextCombination**](isoftkbd-setkeyboardlabeltextcombination.md)
</dt> </dl>

 

 





