---
title: ISoftware. getsoft keyboardcolors-Methode (Software BDC. h)
description: Die isoftkbd getsoftkeyboardcolors-Methode ruft die weiche Tastatur Farbe ab, die dem angegebenen Farbtyp entspricht.
ms.assetid: d59d249c-a1c4-4d6a-add6-632be55a7549
keywords:
- Getsoft keyboardcolors-Methode, Text Dienste-Framework
- Getsoft keyboardcolors-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, getsoft keyboardcolors-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f8f184dc04ddcbef18a9279000b1a68acd35bd3
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2021
ms.locfileid: "106366349"
---
# <a name="isoftkbdgetsoftkeyboardcolors-method"></a>ISOFT kbd:: getsoft keyboardcolors-Methode

Die **isoftkbd:: getsoftkeyboardcolors** -Methode ruft die weiche Tastatur Farbe ab, die dem angegebenen Farbtyp entspricht.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoftKeyboardColors(
  [in]  COLORTYPE colorType,
  [out] COLORREF  *lpColor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ColorType* \[ in\]
</dt> <dd>

Ein-Wert, der den für die weiche Tastatur abzurufenden Farbtyp angibt. Mögliche Werte sind für die [**ColorType**](/windows/win32/api/icm/ne-icm-colortype) -Enumeration definiert.

</dd> <dt>

*lpcolor* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, in dem diese Methode einen 32-Bit- [**COLORREF**](/windows/desktop/gdi/colorref) -Wert abruft, der eine RGB-Farbe angibt.

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

[**Iweichkbd:: setsoft keyboardcolors**](/windows/desktop/TSF/isoftkbd-setsoftkeyboardcolors)
</dt> <dt>

[**ColorType**](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> </dl>

 

