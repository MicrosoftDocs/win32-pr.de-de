---
title: ISoftKbd GetSoftKeyboardPosSize-Methode (Softkbdc.h)
description: Die ISoftKbd GetSoftKeyboardPosSize-Methode ruft die Anfangsposition und Größe einer Softtastatur ab.
ms.assetid: d4482e34-1723-4fe2-a488-e7c18eb3f68e
keywords:
- GetSoftKeyboardPosSize-Methode Textdienstframework
- GetSoftKeyboardPosSize-Methode Textdienstframework , ISoftKbd-Schnittstelle
- ISoftKbd-Schnittstelle Textdienstframework , GetSoftKeyboardPosSize-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 388176e0dd0c45650366c940f3c8302d99e1cf7e49cd61fc95ef3cb8227ea7d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952587"
---
# <a name="isoftkbdgetsoftkeyboardpossize-method"></a>ISoftKbd::GetSoftKeyboardPosSize-Methode

Die **ISoftKbd::GetSoftKeyboardPosSize-Methode** ruft die Anfangsposition und Größe einer soft-Tastatur ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoftKeyboardPosSize(
  [out] POINT *lpStartPoint,
  [out] WORD  *lpwidth,
  [out] WORD  *lpheight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpStartPoint* \[ out\]
</dt> <dd>

Zeiger auf einen Puffer, in dem diese Methode eine [POINT-Struktur](/previous-versions//dd162805(v=vs.85)) abruft, die die Koordinaten der oberen linken Position der soft-Tastatur angibt.

</dd> <dt>

*lpwidth* \[ out\]
</dt> <dd>

Zeiger auf einen Puffer, in dem diese Methode die Breite der soft-Tastatur abruft.

</dd> <dt>

*lpheight* \[ out\]
</dt> <dd>

Zeiger auf einen Puffer, in dem diese Methode die Höhe der soft-Tastatur abruft.

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
| Verteilbare Komponente<br/>          | TSF 1.0 on Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::SetSoftKeyboardPosSize**](isoftkbd-setsoftkeyboardpossize.md)
</dt> </dl>

 

