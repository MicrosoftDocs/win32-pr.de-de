---
title: ISOFT kbd ShowSoft Keyboard-Methode (Software-DC. h)
description: Die isoftkbd showsoftkeyboard-Methode zeigt eine weiche Tastatur an.
ms.assetid: 7e24bef1-accb-40f6-a549-fb676abf9971
keywords:
- ShowSoft Keyboard-Methode, Text Dienste-Framework
- ShowSoft Keyboard-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, ShowSoft Keyboard-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.ShowSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b319e7782a19571cf827175566e1af056c34cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040062"
---
# <a name="isoftkbdshowsoftkeyboard-method"></a>ISOFT kbd:: ShowSoft Keyboard-Methode

Die **isoftkbd:: showsoftkeyboard** -Methode zeigt eine weiche Tastatur an.

## <a name="syntax"></a>Syntax


```C++
HRESULT ShowSoftKeyboard(
  [in] INT iShow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IShow* \[ in\]
</dt> <dd>

Eine ganze Zahl, die den Typ der anzuzeigenden Bildschirmtastatur angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                | BESCHREIBUNG                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

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

 

 





