---
title: ITsSbResourcePluginStoreEx AcquireTargetLock-Methode
description: Sperrt ein Ziel.
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- AcquireTargetLock-Remotedesktopdienste
- AcquireTargetLock-Methode Remotedesktopdienste , ITsSbResourcePluginStoreEx-Schnittstelle
- ITsSbResourcePluginStoreEx-Schnittstelle Remotedesktopdienste , AcquireTargetLock-Methode
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.AcquireTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80a2ab7068ec754a89e384028f2d43989345e9801c4ededb800117d211b0f8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128457"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a>ITsSbResourcePluginStoreEx::AcquireTargetLock-Methode

Sperrt ein Ziel.

## <a name="syntax"></a>Syntax


```C++
HRESULT AcquireTargetLock(
  [in]  BSTR     targetName,
  [in]  DWORD    dwTimeout,
  [out] IUnknown **ppContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*targetName* \[ In\]
</dt> <dd>

Der Name des zu sperrenden Ziels.

</dd> <dt>

*dwTimeout* \[ In\]
</dt> <dd>

Das Timeout für den Vorgang in Millisekunden.

</dd> <dt>

*ppContext* \[ out\]
</dt> <dd>

Gibt einen Zeiger auf den Kontext der Sperre zurück. Um die Sperre frei zu machen, geben Sie diesen Zeiger auf die [**ReleaseTargetLock-Methode**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Nachdem die Sperre erhalten wurde, wird davon ausgegangen, dass der aufrufende Thread exklusiven Zugriff auf das Zielobjekt hat und daher kein anderer Thread (auf demselben Computer) es aktualisieren kann. Daher muss der aufrufende Thread die [**ReleaseTargetLock-Methode**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) aufrufen, sobald er die erforderlichen Aktualisierungen am Zielobjekt vorgenommen hat.

> [!IMPORTANT]
> Diese Sperre verhindert nicht vollständig, dass Zielobjekte extern geändert werden, wenn in der Bereitstellung mehrere Verbindungsbroker vorhanden sind. Der aufrufende Thread muss darauf vorbereitet sein, einen Fehler ordnungsgemäß zu behandeln und das Zielupdate zu wiederholen.

 

Diese Methode ist auf Windows Server 2012 R2 mit [KB3091411](https://support.microsoft.com/kb/3091411) verfügbar, das in der [**ITsSbResourcePluginStoreEx-Schnittstelle installiert**](itssbresourcepluginstoreex.md) ist.

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

 

 





