---
title: Imsrdpclient RequestClose-Methode
description: Fordert ein ordnungsgemäßes Herunterfahren des Remotedesktop ActiveX-Steuer Elements an.
ms.assetid: 0b930a00-f134-4da2-a752-8fd131a22043
ms.tgt_platform: multiple
keywords:
- RequestClose-Methode Remotedesktopdienste
- RequestClose-Methode Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, RequestClose-Methode
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
ms.openlocfilehash: 1679b08680b962cdbff57e9bbbd1c392607d8709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740576"
---
# <a name="imsrdpclientrequestclose-method"></a>Imsrdpclient:: RequestClose-Methode

Fordert ein ordnungsgemäßes Herunterfahren des Remotedesktop ActiveX-Steuer Elements an. Ein ordnungsgemäßes Herunterfahren kann das Beenden der Remotedesktopdienste Sitzung des Benutzers einschließen, aber der Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server wird nicht heruntergefahren.

## <a name="syntax"></a>Syntax


```C++
HRESULT RequestClose(
  [out] ControlCloseStatus *pCloseStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pclosestatus* \[ vorgenommen\]
</dt> <dd>

Der Wert aus der [**controlclosestatus**](controlclosestatus.md) -Enumeration, der angibt, ob die Anwendung das Steuerelement sofort schließen kann. Im folgenden finden Sie eine Liste möglicher Werte.

<dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlclosecanfortsetzung** (0x0000)


</dt> <dd>

Die Containeranwendung kann fortfahren, um das Steuerelement sofort zu schließen. Dieser Wert kann auch darauf hindeuten, dass die Verbindung bereits beendet wurde.

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlclosewaitforevents** (0x0001)


</dt> <dd>

Die Containeranwendung sollte das Steuerelement nicht sofort schließen. die Anwendung sollte warten, bis eines der im folgenden Abschnitt "Hinweise" beschriebenen Ereignisse vor dem Schließen auftritt.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="remarks"></a>Bemerkungen

Wenn der Parameter " *pclosestatus* " gleich " **controlclosewaitforevents**" ist, muss die Anwendung warten, bis eines der folgenden Ereignisse eintritt, bevor die Anwendung das Steuerelement schließt:

-   [**Imstscaxevents:: ongetrennte**](imstscaxevents-ondisconnected.md). Wenn der Benutzer nicht bei der Remotedesktopdienste Sitzung angemeldet ist, kann die Anwendung die [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) -Funktion aufzurufen, um alle Fenster zu zerstören und dann das Steuerelement zu schließen.
-   [**Imstscaxevents:: onconfirmclose**](imstscaxevents-onconfirmclose.md). Wenn der Benutzer bei der Remotedesktopdienste Sitzung angemeldet ist, löst das Steuerelement ein **onconfirmclose** -Ereignis aus. Dieses Ereignis ermöglicht der Anwendung, den Benutzer zur Eingabe aufzufordern, ob die Verbindung geschlossen werden soll. Wenn der Benutzer die Eingabeaufforderung auf Ja antwortet, kann die Containeranwendung [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) zum zerstören aller Fenster und zum Schließen des Steuer Elements auffordern.

**RequestClose** ermöglicht einer Containeranwendung, den Benutzer aufzufordern, ob eine Verbindung geschlossen werden soll. Weitere Informationen finden Sie unter [**imstscaxevents:: onconfirmclose**](imstscaxevents-onconfirmclose.md).

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imsrdpclient ist als 92b4a539-7115-4b7c-a5a9-e5d9efc2780a definiert.<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclient**](imsrdpclient-interface.md)
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

[**Imstscaxevents:: onconfirmclose**](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[**Imstscaxevents:: ongetrennte**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

