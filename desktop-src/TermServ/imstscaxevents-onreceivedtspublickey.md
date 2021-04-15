---
title: Imstscaxevents onreceivedtspublickey-Methode
description: Wird während der Verbindungs Sequenz aufgerufen, wenn der Client den öffentlichen Schlüssel vom Server abruft. Dieses Ereignis wird nur aufgerufen, wenn die notifytspublickey-Eigenschaft Variant \_ true ist.
ms.assetid: 1db98b8b-2f08-4252-ad8b-6764fa25b300
ms.tgt_platform: multiple
keywords:
- Onreceivedtspublickey-Methode Remotedesktopdienste
- Onreceivedtspublickey-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onreceivedtspublickey-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnReceivedTSPublicKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337a9efabe48dee7a5a4194c3b796b95f35a0592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477433"
---
# <a name="imstscaxeventsonreceivedtspublickey-method"></a>Imstscaxevents:: onreceivedtspublickey-Methode

Wird während der Verbindungs Sequenz aufgerufen, wenn der Client den öffentlichen Schlüssel vom Server abruft. Dieses Ereignis wird nur aufgerufen, wenn die **notifytspublickey** -Eigenschaft **Variant \_ true** ist. Dies erfolgt nach dem [**onconnecting**](imstscaxevents-onconnecting.md)-Prozess, aber vor [**onauthenticationwarninganzeige**](imstscaxevents-onauthenticationwarningdisplayed.md) und [**onconnected**](imstscaxevents-onconnected.md).

## <a name="syntax"></a>Syntax


```C++
void OnReceivedTSPublicKey(
  [in]  BSTR         publicKey,
  [out] VARIANT_BOOL *pfContinueLogon
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PublicKey* \[ in\]
</dt> <dd>

Enthält den öffentlichen Schlüssel des Remote Computers.

</dd> <dt>

*pfcontinuelogon* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine **Variant- \_ boolesche** Variable, die empfängt, ob der Anmeldevorgang fortgesetzt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008, Windows Server 2008 mit SP1<br/>                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





