---
title: IMsRdpClient RequestClose-Methode
description: Fordert ein ordnungsgemäßes Herunterfahren des Remotedesktop ActiveX-Steuerelements an.
ms.assetid: 0b930a00-f134-4da2-a752-8fd131a22043
ms.tgt_platform: multiple
keywords:
- RequestClose-Methode Remotedesktopdienste
- RequestClose-Methode Remotedesktopdienste , IMsRdpClient-Schnittstelle
- IMsRdpClient-Schnittstelle Remotedesktopdienste , RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste , IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste , RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste , IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste , RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste , IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste , RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste , IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste , RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste , IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste , RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste , IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste , RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste , IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste , RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste , IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste , RequestClose-Methode
topic_type:
- apiref
api_name:
- IMsRdpClient.RequestClose
- IMsRdpClient2.RequestClose
- IMsRdpClient3.RequestClose
- IMsRdpClient4.RequestClose
- IMsRdpClient5.RequestClose
- IMsRdpClient6.RequestClose
- IMsRdpClient7.RequestClose
- IMsRdpClient8.RequestClose
- IMsRdpClient9.RequestClose
- IMsRdpClient10.RequestClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae812c27b0c280ca3a6cd879d5af86181de85793ec6092441fb83b45c74d8656
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010180"
---
# <a name="imsrdpclientrequestclose-method"></a>IMsRdpClient::RequestClose-Methode

Fordert ein ordnungsgemäßes Herunterfahren des Remotedesktop ActiveX-Steuerelements an. Ein ordnungsgemäßes Herunterfahren kann das Beenden der Remotedesktopdienste Sitzung des Benutzers umfassen, aber nicht das Herunterfahren des Remotedesktop-Sitzungshost -Servers (RD-Sitzungshost).

## <a name="syntax"></a>Syntax


```C++
HRESULT RequestClose(
  [out] ControlCloseStatus *pCloseStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCloseStatus* \[ out\]
</dt> <dd>

Wert aus der [**ControlCloseStatus-Enumeration,**](controlclosestatus.md) der angibt, ob die Anwendung das Steuerelement sofort schließen kann. Es folgt eine Liste der möglichen Werte.

<dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000)


</dt> <dd>

Die Containeranwendung kann fortfahren, um das Steuerelement sofort zu schließen. Dieser Wert kann auch angeben, dass die Verbindung bereits beendet wurde.

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001)


</dt> <dd>

Die Containeranwendung sollte das Steuerelement nicht sofort schließen. Die Anwendung sollte warten, bis eines der im folgenden Abschnitt "Hinweise" beschriebenen Ereignisse vor dem Schließen auftritt.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Hinweise

Wenn der *pCloseStatus-Parameter* **controlCloseWaitForEvents** entspricht, sollte die Anwendung warten, bis eines der folgenden Ereignisse eintritt, bevor die Anwendung das Steuerelement schließt:

-   [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md). Wenn der Benutzer nicht bei der Remotedesktopdienste Sitzung angemeldet ist, kann die Anwendung die [**DestroyWindow-Funktion**](/windows/desktop/api/winuser/nf-winuser-destroywindow) aufrufen, um alle Fenster zu zerstören, und dann das Steuerelement schließen.
-   [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md). Wenn der Benutzer bei der Remotedesktopdienste-Sitzung angemeldet ist, löst das Steuerelement ein **OnConfirmClose-Ereignis** aus. Dieses Ereignis ermöglicht der Anwendung, den Benutzer dazu aufzufordern, die Verbindung zu schließen. Wenn der Benutzer ja auf die Eingabeaufforderung antwortet, kann die Containeranwendung [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) aufrufen, um alle Fenster zu zerstören, und das Steuerelement schließen.

**RequestClose** ermöglicht einer Containeranwendung, den Benutzer dazu aufzufordern, eine Verbindung zu schließen. Weitere Informationen finden Sie unter [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient ist als 92b4a539-7115-4b7c-a5a9-e5d9efc2780a definiert.<br/>        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

