---
title: Icdkbd setsoft keyboardpossize-Methode (Software-DC. h)
description: Die isoftkbd setsoftkeyboardpossize-Methode legt die Anfangsposition und die Größe einer Soft Tastatur fest.
ms.assetid: bf827b07-0e8b-4d5a-8178-45d75af83551
keywords:
- Setsoft keyboardpossize-Methode, Text Dienste-Framework
- Setsoft keyboardpossize-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, setsoft keyboardpossize-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7131d9c46c90917f2ebdf471916f872aedb2e33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478207"
---
# <a name="isoftkbdsetsoftkeyboardpossize-method"></a>ISOFT kbd:: setsoft keyboardpossize-Methode

Die **isoftkbd:: setsoftkeyboardpossize** -Methode legt die Anfangsposition und die Größe einer Soft Tastatur fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSoftKeyboardPosSize(
  [in] POINT StartPoint,
  [in] WORD  width,
  [in] WORD  height
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Startpunkt* \[ in\]
</dt> <dd>

Eine [Punkt](/previous-versions//dd162805(v=vs.85)) Struktur, die die Koordinaten der oberen linken Position der Soft Tastatur angibt.

</dd> <dt>

*Breite* \[ in\]
</dt> <dd>

Breite der Bildschirmtastatur.

</dd> <dt>

*Höhe* \[ in\]
</dt> <dd>

Höhe der Bildschirmtastatur.

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
</dt> </dl>

 

