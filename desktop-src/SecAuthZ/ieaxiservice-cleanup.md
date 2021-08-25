---
description: Gibt von der IeAxiService-Schnittstelle verwendete Ressourcen frei.
ms.assetid: 11f5cfdc-dcdd-4b41-b02c-b19b9452509e
title: IeAxiService::Cleanup-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Cleanup
api_type:
- COM
api_location: ''
ms.openlocfilehash: de0413c39a4abf47a24913f347ceed0158d0b51aa4e1da0b3005cace1326b53f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908380"
---
# <a name="ieaxiservicecleanup-method"></a>IeAxiService::Cleanup-Methode

Die **Cleanup-Methode** gibt ressourcen frei, die von der [**IeAxiService-Schnittstelle verwendet**](ieaxiservice.md) werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Cleanup();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt die Methode S \_ OK zurück.

Wenn bei der Methode ein Fehler auftritt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService ist als E9E92380-9ECD-4982-A0EB-6815A56CCF27 definiert.<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IeAxiService**](ieaxiservice.md)
</dt> </dl>

 

