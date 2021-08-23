---
title: IMsTscAxEvents OnConfirmClose-Methode
description: Wird aufgerufen, wenn der Client die IMsRdpClient RequestClose-Methode aufruft.
ms.assetid: fb149fbc-9415-4c4c-8d4b-e22214ac38cb
ms.tgt_platform: multiple
keywords:
- OnConfirmClose-Remotedesktopdienste
- OnConfirmClose-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnConfirmClose-Methode
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
ms.openlocfilehash: 2effd50552ab227e8e065844b8b19da0e022f6b8e36d1d86701ad0614b821126
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512470"
---
# <a name="imstscaxeventsonconfirmclose-method"></a>IMsTscAxEvents::OnConfirmClose-Methode

Wird aufgerufen, wenn der Client die [**IMsRdpClient::RequestClose-Methode**](imsrdpclient-requestclose.md) aufruft. Als Reaktion auf dieses Ereignis sollte der Benutzer aufgefordert werden, das Schließen der Verbindung zu bestätigen. Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".

## <a name="syntax"></a>Syntax


```C++
void OnConfirmClose(
  [out] VARIANT_BOOL *pfAllowClose
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfAllowClose* \[ out\]
</dt> <dd>

Bei **VARIANT \_ TRUE** gibt der Standardwert an, dass der Benutzer die Verbindung schließen möchte. Bei **VARIANT \_ FALSE gibt** an, dass der Benutzer die Verbindung nicht schließen möchte. Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn eine Containeranwendung die [**IMsRdpClient::RequestClose-Methode**](imsrdpclient-requestclose.md) aufruft, gibt diese Methode einen Wert zurück, der angibt, ob der Container auf ein **OnConfirmClose-Ereignis** warten soll, bevor die Steuerungsverbindung geschlossen wird. Wenn **RequestClose** **controlCloseWaitForEvents** zurückgibt und der Benutzer mit seiner Remotedesktopdienste-Sitzung verbunden und angemeldet ist, wird das **OnConfirmClose-Ereignis** ausgelöst. An diesem Punkt kann die Containeranwendung den Benutzer auffordern, zu fragen, ob der Benutzer die Verbindung schließen möchte. Wenn der Benutzer die Verbindung schließen möchte, sollte die Anwendung den *Parameter pfAllowClose* auf **VARIANT \_ TRUE** festlegen und mit dem Schließen der Verbindung fortfahren. Wenn der Benutzer nicht schließen möchte, sollte die Anwendung *pfAllowClose* auf **VARIANT \_ FALSE** festlegen und die Verbindung geöffnet lassen.

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

 

 





