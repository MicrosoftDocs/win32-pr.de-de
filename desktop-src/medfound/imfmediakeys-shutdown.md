---
description: 'Weitere Informationen finden Sie unter: IMF Media Keys:: Shutdown-Methode'
ms.assetid: 464b598c-5fa7-40af-83ba-8619fbd84b04
title: 'IMF Media Keys:: Shutdown-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.Shutdown
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9fcee861b53aaf0c9fda2c6265f50fcee60f674c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351568"
---
# <a name="imfmediakeysshutdown-method"></a>IMF Media Keys:: Shutdown-Methode

## <a name="syntax"></a>Syntax


```C++
HRESULT Shutdown();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Das **herunter** fahren sollte von der Anwendung vor der endgültigen Freigabe aufgerufen werden. An dieser Stelle wird der CDM-Verweis (Content entschlüsseln Module) und alle anderen Ressourcen veröffentlicht. Verwandte Sitzungen werden jedoch nicht freigegeben oder geschlossen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>MF mediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMF Media Keys**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




