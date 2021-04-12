---
title: Itssbresourcepluginstoreex releasetargetlock-Methode
description: Gibt eine Sperre für ein Ziel frei.
ms.assetid: ab2ae9f3-2d38-4b31-9889-58297c574bd4
ms.tgt_platform: multiple
keywords:
- Releasetargetlock-Methode Remotedesktopdienste
- Releasetargetlock-Methode Remotedesktopdienste, itssbresourcepluginstoreex-Schnittstelle
- Itssbresourcepluginstoreex-Schnittstelle Remotedesktopdienste, releasetargetlock-Methode
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.ReleaseTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc34bdb27e40316ea1271bf0faa5d8c6b0abfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104300"
---
# <a name="itssbresourcepluginstoreexreleasetargetlock-method"></a>Itssbresourcepluginstoreex:: releasetargetlock-Methode

Gibt eine Sperre für ein Ziel frei.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReleaseTargetLock(
  [in] IUnknown *pContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContext* \[ in\]
</dt> <dd>

Ein Zeiger auf den Kontext, der von der [**acquiretargetlock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) -Methode zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode ist nur unter Windows Server 2012 R2 mit installiertem [KB3091411](https://support.microsoft.com/kb/3091411) in der [**itssbresourcepluginstoreex**](itssbresourcepluginstoreex.md) -Schnittstelle verfügbar. Diese Methode ist in der [**itssbresourcepluginstore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) -Schnittstelle ab Windows Server 2016 verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                             |
| Ende des Supports (Server)<br/>    | Windows Server 2012 R2<br/>                                                             |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl>          |
| IID<br/>                      | IID \_ itssbresourcepluginstoreex ist als 80b83ffd-625d-11e5-bea1-a0481c7e9064 definiert<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itssbresourcepluginstoreex**](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





