---
title: ITsSbResourcePluginStoreEx ReleaseTargetLock-Methode
description: Gibt eine Sperre für ein Ziel frei.
ms.assetid: ab2ae9f3-2d38-4b31-9889-58297c574bd4
ms.tgt_platform: multiple
keywords:
- ReleaseTargetLock-Remotedesktopdienste
- ReleaseTargetLock-Methode Remotedesktopdienste , ITsSbResourcePluginStoreEx-Schnittstelle
- ITsSbResourcePluginStoreEx-Schnittstelle Remotedesktopdienste , ReleaseTargetLock-Methode
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
ms.openlocfilehash: b7fbe40d0fc7a28697d0e2fa9727f9e844eb39759db0dddf02c1d9e01bd843c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989910"
---
# <a name="itssbresourcepluginstoreexreleasetargetlock-method"></a>ITsSbResourcePluginStoreEx::ReleaseTargetLock-Methode

Gibt eine Sperre für ein Ziel frei.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReleaseTargetLock(
  [in] IUnknown *pContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContext* \[ In\]
</dt> <dd>

Ein Zeiger auf den Kontext, der von der [**AcquireTargetLock-Methode zurückgegeben**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode ist nur auf Windows Server 2012 R2 mit [KB3091411](https://support.microsoft.com/kb/3091411) verfügbar, das in der [**ITsSbResourcePluginStoreEx-Schnittstelle installiert**](itssbresourcepluginstoreex.md) ist. Diese Methode ist auf der [**ITsSbResourcePluginStore-Schnittstelle**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) verfügbar, beginnend mit Windows Server 2016.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                             |
| Ende des Supports (Server)<br/>    | Windows Server 2012 R2<br/>                                                             |
| Idl<br/>                      | <dl> <dt>SbTsV.idl</dt> </dl>          |
| IID<br/>                      | IID \_ ITsSbResourcePluginStoreEx ist als 80b83ffd-625d-11e5-bea1-a0481c7e9064 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





