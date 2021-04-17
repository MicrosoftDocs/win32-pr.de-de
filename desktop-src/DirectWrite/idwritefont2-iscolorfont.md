---
title: IDWriteFont2 iscolorfont-Methode
description: Ermöglicht die Ermittlung, ob ein farbrenderingpfad möglicherweise erforderlich ist.
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- Iscolorfont-Methode, direktes Schreiben
- Iscolorfont-Methode Direct Write, IDWriteFont2-Schnittstelle
- IDWriteFont2 Interface Direct Write, iscolorfont-Methode
topic_type:
- apiref
api_name:
- IDWriteFont2.IsColorFont
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353499c5e1c00ae37e585ecc6be47e5a2033d795
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392044"
---
# <a name="idwritefont2iscolorfont-method"></a>IDWriteFont2:: iscolorfont-Methode

Ermöglicht die Ermittlung, ob ein farbrenderingpfad möglicherweise erforderlich ist.

## <a name="syntax"></a>Syntax


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **bool**

Gibt " **true** " zurück, wenn die Schriftart Farbinformationen (colr-und CPAL-Tabellen) aufweist. andernfalls **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteFont2**](idwritefont2.md)
</dt> </dl>

 

 





