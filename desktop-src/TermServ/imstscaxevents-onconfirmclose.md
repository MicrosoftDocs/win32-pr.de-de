---
title: Imstscaxevents onconfirmclose-Methode
description: Wird aufgerufen, wenn der Client die Methode "imsrdpclient RequestClose" aufruft.
ms.assetid: fb149fbc-9415-4c4c-8d4b-e22214ac38cb
ms.tgt_platform: multiple
keywords:
- Onconfirmclose-Methode Remotedesktopdienste
- Onconfirmclose-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onconfirmclose-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConfirmClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623196033e23a964857a6a604c7eca3904f32c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106485"
---
# <a name="imstscaxeventsonconfirmclose-method"></a>Imstscaxevents:: onconfirmclose-Methode

Wird aufgerufen, wenn der Client die [**imsrdpclient:: RequestClose**](imsrdpclient-requestclose.md) -Methode aufruft. Als Reaktion auf dieses Ereignis sollte der Benutzer aufgefordert werden, das Schließen der Verbindung zu bestätigen. Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".

## <a name="syntax"></a>Syntax


```C++
void OnConfirmClose(
  [out] VARIANT_BOOL *pfAllowClose
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfallowclose* \[ vorgenommen\]
</dt> <dd>

Wenn **Variant \_ true** ist, bedeutet der Standardwert, dass der Benutzer die Verbindung schließen möchte. Wenn **Variant \_ false** ist, wird angegeben, dass der Benutzer die Verbindung nicht schließen möchte. Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn eine Containeranwendung die [**imsrdpclient:: RequestClose**](imsrdpclient-requestclose.md) -Methode aufruft, gibt diese Methode einen Wert zurück, der angibt, ob der Container auf das Eintreten eines **onconfirmclose** -Ereignisses warten soll, bevor die Steuerelement Verbindung geschlossen wird. Wenn **RequestClose** " **controlclosewaitforevents**" zurückgibt und der Benutzer verbunden ist und bei seiner Remotedesktopdienste Sitzung angemeldet ist, wird das **onconfirmclose** -Ereignis ausgelöst. An diesem Punkt kann die Containeranwendung den Benutzer auffordern und Fragen, ob der Benutzer die Verbindung schließen möchte. Wenn der Benutzer die Verbindung schließen möchte, sollte die Anwendung den Parameter *pfallowclose* auf **Variant \_ true** festlegen und das Schließen der Verbindung fortsetzen. Wenn der Benutzer nicht schließen möchte, sollte die Anwendung *pfallowclose* auf **Variant \_ false** festlegen und die Verbindung geöffnet lassen.

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

 

 





