---
description: Gibt die von der ieaxiservice-Schnittstelle verwendeten Ressourcen frei.
ms.assetid: 11f5cfdc-dcdd-4b41-b02c-b19b9452509e
title: 'Ieaxiservice:: Cleanup-Methode'
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
ms.openlocfilehash: b29784ae360ec78b9f7e01d2045617615333a5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217164"
---
# <a name="ieaxiservicecleanup-method"></a>Ieaxiservice:: Cleanup-Methode

Die **cleanupmethode** gibt Ressourcen frei, die von der [**ieaxiservice**](ieaxiservice.md) -Schnittstelle verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Cleanup();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                 |
| IID<br/>                      | IID \_ ieaxiservice ist definiert als E9E92380-9ecd-4982-A0EB-6815a56ccb27<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ieaxiservice**](ieaxiservice.md)
</dt> </dl>

 

