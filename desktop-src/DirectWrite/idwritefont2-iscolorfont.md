---
title: IDWriteFont2 IsColorFont-Methode
description: Ermöglicht die Bestimmung, ob ein Farbrenderingpfad potenziell erforderlich ist.
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- IsColorFont-Methode – Direkter Schreibzugriff
- IsColorFont-Methode Direct Write, IDWriteFont2-Schnittstelle
- IDWriteFont2-Schnittstelle Direct Write, IsColorFont-Methode
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
ms.openlocfilehash: 144aded290c7a4121dd785a1844971e3c1b5501b8ae78707d8da5378c44b002a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650184"
---
# <a name="idwritefont2iscolorfont-method"></a>IDWriteFont2::IsColorFont-Methode

Ermöglicht die Bestimmung, ob ein Farbrenderingpfad potenziell erforderlich ist.

## <a name="syntax"></a>Syntax


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **BOOL**

Gibt **TRUE zurück,** wenn die Schriftart Farbinformationen enthält (COLR- und CPAL-Tabellen). **andernfalls FALSE**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Desktop-Apps \| UWP-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1- und Windows Runtime-Apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IDWriteFont2**](idwritefont2.md)
</dt> </dl>

 

 





