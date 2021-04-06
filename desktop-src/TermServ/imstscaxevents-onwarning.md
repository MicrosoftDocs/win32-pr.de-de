---
title: Imstscaxevents OnWarning-Methode
description: Wird aufgerufen, wenn das Client Steuerelement einen Fehlerzustand erkennt, der nicht schwerwiegend ist.
ms.assetid: af43d3aa-0ae8-4721-b85d-bb043b20dc40
ms.tgt_platform: multiple
keywords:
- OnWarning-Methode Remotedesktopdienste
- OnWarning-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, OnWarning-Methode
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
ms.openlocfilehash: aadc7013f34c93406f93841896a9041bbb1b7cfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742081"
---
# <a name="imstscaxeventsonwarning-method"></a>Imstscaxevents:: OnWarning-Methode

Wird aufgerufen, wenn das Client Steuerelement einen Fehlerzustand erkennt, der nicht schwerwiegend ist.

## <a name="syntax"></a>Syntax


```C++
void OnWarning(
  [in] long warningCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*warningCode* \[ in\]
</dt> <dd>

Der Fehlercode.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Der Bitmap-Cache ist beschädigt.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





