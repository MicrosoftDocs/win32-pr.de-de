---
title: ISoftKbd SetSoftKeyboardPosSize-Methode (Softkbdc.h)
description: Die ISoftKbd SetSoftKeyboardPosSize-Methode legt die Anfangsposition und Größe einer Softtastatur fest.
ms.assetid: bf827b07-0e8b-4d5a-8178-45d75af83551
keywords:
- SetSoftKeyboardPosSize-Methode Textdienstframework
- SetSoftKeyboardPosSize-Methode Textdienstframework , ISoftKbd-Schnittstelle
- ISoftKbd-Schnittstelle Textdienstframework , SetSoftKeyboardPosSize-Methode
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
ms.openlocfilehash: b624bea0496b7d7ea8ede3fce2f74c7704b17cd9a66e7f1d9b7ce5bdbf9d98e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952567"
---
# <a name="isoftkbdsetsoftkeyboardpossize-method"></a>ISoftKbd::SetSoftKeyboardPosSize-Methode

Die **ISoftKbd::SetSoftKeyboardPosSize-Methode** legt die Anfangsposition und Größe einer Softtastatur fest.

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

*StartPoint* \[ In\]
</dt> <dd>

Eine [POINT-Struktur,](/previous-versions//dd162805(v=vs.85)) die die Koordinaten der oberen linken Position der soft-Tastatur angibt.

</dd> <dt>

*Breite* \[ In\]
</dt> <dd>

Breite der soft-Tastatur.

</dd> <dt>

*Höhe* \[ In\]
</dt> <dd>

Höhe der Softtastatur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | Beschreibung                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Einer der Parameter ist ungültig.<br/> |



 

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
</dt> </dl>

 

