---
title: Itssbresourcepluginstoreex acquiretargetlock-Methode
description: Sperrt ein Ziel.
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- Acquiretargetlock-Methode Remotedesktopdienste
- Acquiretargetlock-Methode Remotedesktopdienste, itssbresourcepluginstoreex-Schnittstelle
- Itssbresourcepluginstoreex-Schnittstelle Remotedesktopdienste, acquiretargetlock-Methode
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
ms.openlocfilehash: 8c18be0a544ebcea2d2cecb40dcea3a08e4bd35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103155"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a>Itssbresourcepluginstoreex:: acquiretargetlock-Methode

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

*TargetName* \[ in\]
</dt> <dd>

Der Name des zu Sperr enden Ziels.

</dd> <dt>

*dwtimeout* \[ in\]
</dt> <dd>

Das Timeout für den Vorgang in Millisekunden.

</dd> <dt>

*ppcontext* \[ vorgenommen\]
</dt> <dd>

Gibt einen Zeiger auf den Kontext der Sperre zurück. Um die Sperre freizugeben, geben Sie diesen Zeiger auf die [**releasetargetlock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) -Methode an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Nachdem die Sperre eingerichtet wurde, wird davon ausgegangen, dass der aufrufende Thread exklusiven Zugriff auf das Zielobjekt hat und daher kein anderer Thread (innerhalb desselben Computers) ihn aktualisieren kann. Daher muss der aufrufende Thread die [**releasetargetlock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) -Methode aufrufen, sobald die erforderlichen Updates für das Zielobjekt vorgenommen wurden.

> [!IMPORTANT]
> Diese Sperre verhindert nicht vollständig, dass Zielobjekte extern geändert werden, wenn mehr als ein Verbindungs Broker in der Bereitstellung vorhanden ist. Der aufrufende Thread muss darauf vorbereitet sein, einen Fehler ordnungsgemäß zu behandeln und das Ziel Update zu wiederholen.

 

Diese Methode ist unter Windows Server 2012 R2 mit installiertem [KB3091411](https://support.microsoft.com/kb/3091411) in der [**itssbresourcepluginstoreex**](itssbresourcepluginstoreex.md) -Schnittstelle verfügbar.

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

 

 





