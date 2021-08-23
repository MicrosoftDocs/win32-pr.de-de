---
title: IMsTscAxEvents OnWarning-Methode
description: Wird aufgerufen, wenn das Clientsteuer steuerelement eine Fehlerbedingung trifft, die nicht schwerwiegender ist.
ms.assetid: af43d3aa-0ae8-4721-b85d-bb043b20dc40
ms.tgt_platform: multiple
keywords:
- OnWarning-Remotedesktopdienste
- OnWarning-Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnWarning-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnWarning
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbcebe5c86bb50913ba11d4485f30757f399467aa30730f8cd27de50e360c0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657140"
---
# <a name="imstscaxeventsonwarning-method"></a>IMsTscAxEvents::OnWarning-Methode

Wird aufgerufen, wenn das Clientsteuer steuerelement eine Fehlerbedingung trifft, die nicht schwerwiegender ist.

## <a name="syntax"></a>Syntax


```C++
void OnWarning(
  [in] long warningCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*warningCode* \[ In\]
</dt> <dd>

Der Fehlercode.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Der Bitmapcache ist beschädigt.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





