---
title: Icdkbd setsoft keyboardcolors-Methode (Software-DC. h)
description: Die isoftkbd setsoftkeyboardcolors-Methode legt die weiche Tastatur Farbe für den angegebenen Farbtyp fest.
ms.assetid: 1abbff35-a5ef-4119-9367-60b6e0961c59
keywords:
- Setsoft keyboardcolors-Methode, Text Dienste-Framework
- Setsoft keyboardcolors-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, setsoft keyboardcolors-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38357331db2440c35ca7557d08c97729fde9c9f0
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2021
ms.locfileid: "106355698"
---
# <a name="isoftkbdsetsoftkeyboardcolors-method"></a>ISOFT kbd:: setsoft keyboardcolors-Methode

Die **isoftkbd:: setsoftkeyboardcolors** -Methode legt die weiche Tastatur Farbe für den angegebenen Farbtyp fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSoftKeyboardColors(
  [in] COLORTYPE colorType,
  [in] COLORREF  Color
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ColorType* \[ in\]
</dt> <dd>

Ein-Wert, der den Farbtyp für die weiche Tastatur angibt. Mögliche Werte sind für die [**ColorType**](/windows/win32/api/icm/ne-icm-colortype) -Enumeration definiert.

</dd> <dt>

*Farbe* \[ in\]
</dt> <dd>

Ein 32-Bit- [**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der eine RGB-Farbe angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | BESCHREIBUNG                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>        |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Einer der Parameter ist ungültig.<br/> |



 

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

[**Iweichkbd:: getsoft keyboardcolors**](isoftkbd-getsoftkeyboardcolors.md)
</dt> <dt>

[**ColorType**](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> </dl>

 

