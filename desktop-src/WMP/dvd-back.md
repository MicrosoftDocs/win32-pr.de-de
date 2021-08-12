---
title: DVD.back-Methode
description: Die back-Methode gibt die Anzeige aus einem Untermenü an das übergeordnete Menü zurück.
ms.assetid: 4b6c3562-6484-4ef0-8c5c-c24d88e02096
keywords:
- Back-Windows Media Player
- back-Methode Windows Media Player , DVD-Klasse
- DVD-Klasse Windows Media Player , back-Methode
topic_type:
- apiref
api_name:
- DVD.back
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 916c16af578e2ccb6b0e4a6717431f7c30f3084bcd12fbedb1dff9f6c0627493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579089"
---
# <a name="dvdback-method"></a>DVD.back-Methode

Die **back-Methode** gibt die Anzeige aus einem Untermenü an das übergeordnete Menü zurück.

## <a name="syntax"></a>Syntax


```JScript
DVD.back()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Jede DVD wird anders verfasst. Einige DVDs werden so verfasst, dass die **Back-Methode** über das Stammmenü verfügbar ist, aber wenn sie aufgerufen wird, wird sie nichts tun.

**Windows Media Player 10 Mobile:** Diese Methode ist immer erfolgreich, führt aber nicht den beabsichtigten Vorgang aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Version<br/>                  | Windows Media Player für Windows XP oder höher.<br/>                           |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DVD-Objekt**](dvd-object.md)
</dt> </dl>

 

 





