---
title: ISoftKbd GetSoftKeyboardTypeMode-Methode (Softkbdc.h)
description: Die ISoftKbd GetSoftKeyboardTypeMode-Methode ruft den Typmodus für eine soft-Tastatur ab.
ms.assetid: 77294652-b82e-4b69-bb55-5ebebc3c97c7
keywords:
- GetSoftKeyboardTypeMode-Textdienstframework
- GetSoftKeyboardTypeMode-Methode Textdienstframework , ISoftKbd-Schnittstelle
- ISoftKbd-Schnittstelle Textdienstframework , GetSoftKeyboardTypeMode-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab1205f0d9f59e027db75d2df580917392c445e812425c714b1688ce784a68ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952577"
---
# <a name="isoftkbdgetsoftkeyboardtypemode-method"></a>ISoftKbd::GetSoftKeyboardTypeMode-Methode

Die **ISoftKbd::GetSoftKeyboardTypeMode-Methode** ruft den Typmodus für eine soft-Tastatur ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoftKeyboardTypeMode(
  [out] TYPEMODE *lpTypeMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpTypeMode* \[ out\]
</dt> <dd>

Zeiger auf einen Puffer, in dem diese Methode den Typmodus abruft. Mögliche Werte werden für die [**TYPEMODE-Enumeration**](typemode.md) definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | Beschreibung                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der *lpTypeMode-Parameter* ist ungültig.<br/> |



 

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

[**ISoftKbd::SetSoftKeyboardTypeMode**](isoftkbd-setsoftkeyboardtypemode.md)
</dt> <dt>

[**TYPEMODE**](typemode.md)
</dt> </dl>

 

 





