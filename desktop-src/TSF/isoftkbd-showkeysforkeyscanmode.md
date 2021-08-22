---
title: ISoftKbd ShowKeysForKeyScanMode-Methode (Softkbdc.h)
description: Die ISoftKbd ShowKeysForKeyScanMode-Methode zeigt die Schlüssel an, die für den Schlüsselscanmodus für eine Softtastatur verwendet werden.
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- ShowKeysForKeyScanMode-Methode Textdienstframework
- ShowKeysForKeyScanMode-Methode Textdienstframework , ISoftKbd-Schnittstelle
- ISoftKbd-Schnittstelle Textdienstframework , ShowKeysForKeyScanMode-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.ShowKeysForKeyScanMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 844c9f39529e1a66437c83672acc8b2d3ad2a3e3ff3a1ad31c4d9bd97248d010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877272"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a>ISoftKbd::ShowKeysForKeyScanMode-Methode

Die **ISoftKbd::ShowKeysForKeyScanMode-Methode** zeigt die Schlüssel an, die für den Schlüsselscanmodus für eine Softtastatur verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT ShowKeysForKeyScanMode(
  [in] KEYID *lpKeyID,
  [in] INT   iKeyNum,
  [in] BOOL  fHighL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpKeyID* \[ In\]
</dt> <dd>

Zeiger auf ein Array von KEYID-Elementen, das die Bezeichner der anzuzeigenden Schlüssel angibt.

</dd> <dt>

*iKeyNum* \[ In\]
</dt> <dd>

Die Anzahl der anzuzeigenden Schlüssel.

</dd> <dt>

*fHighL* \[ In\]
</dt> <dd>

TRUE, wenn die Methode die Schlüssel hervorheben soll, **andernfalls FALSE.**

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> </dl>

 

 





