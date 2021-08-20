---
title: IMsTscAx ConnectingText (Eigenschaft)
description: Gibt den Text an, der zentriert im -Steuerelement angezeigt wird, während das Steuerelement eine Verbindung verbindet.
ms.assetid: 9bc82074-988f-491b-80e3-00c3f7ba437a
ms.tgt_platform: multiple
keywords:
- Eigenschafteneigenschaft "ConnectingText Remotedesktopdienste
- ConnectingText-Eigenschaft Remotedesktopdienste , IMsTscAx-Schnittstelle
- IMsTscAx-Schnittstelle Remotedesktopdienste , ConnectingText-Eigenschaft
- ConnectingText-Eigenschaft Remotedesktopdienste , IMsRdpClient-Schnittstelle
- IMsRdpClient-Schnittstelle Remotedesktopdienste , ConnectingText-Eigenschaft
- ConnectingText-Eigenschaft Remotedesktopdienste , IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste , ConnectingText-Eigenschaft
- ConnectingText-Eigenschaft Remotedesktopdienste , IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste , ConnectingText-Eigenschaft
- ConnectingText-Eigenschaft Remotedesktopdienste , IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste , ConnectingText-Eigenschaft
- ConnectingText-Eigenschaft Remotedesktopdienste , IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste , ConnectingText-Eigenschaft
- ConnectingText-Eigenschaft Remotedesktopdienste , IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste , ConnectingText-Eigenschaft
- ConnectingText-Eigenschaft Remotedesktopdienste , IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste , ConnectingText-Eigenschaft
- ConnectingText-Eigenschaft Remotedesktopdienste , IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste , ConnectingText-Eigenschaft
- ConnectingText-Eigenschaft Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , ConnectingText-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.ConnectingText
- IMsTscAx.get_ConnectingText
- IMsTscAx.put_ConnectingText
- IMsRdpClient.ConnectingText
- IMsRdpClient.get_ConnectingText
- IMsRdpClient.put_ConnectingText
- IMsRdpClient2.ConnectingText
- IMsRdpClient2.get_ConnectingText
- IMsRdpClient2.put_ConnectingText
- IMsRdpClient3.ConnectingText
- IMsRdpClient3.get_ConnectingText
- IMsRdpClient3.put_ConnectingText
- IMsRdpClient4.ConnectingText
- IMsRdpClient4.get_ConnectingText
- IMsRdpClient4.put_ConnectingText
- IMsRdpClient5.ConnectingText
- IMsRdpClient5.get_ConnectingText
- IMsRdpClient5.put_ConnectingText
- IMsRdpClient6.ConnectingText
- IMsRdpClient6.get_ConnectingText
- IMsRdpClient6.put_ConnectingText
- IMsRdpClient7.ConnectingText
- IMsRdpClient7.get_ConnectingText
- IMsRdpClient7.put_ConnectingText
- IMsRdpClient8.ConnectingText
- IMsRdpClient8.get_ConnectingText
- IMsRdpClient8.put_ConnectingText
- IMsRdpClient9.ConnectingText
- IMsRdpClient9.get_ConnectingText
- IMsRdpClient9.put_ConnectingText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7342e47658e77d9fb29ef03ab1995e5263c78a8e31d2f020852e5fa10864a031
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129672"
---
# <a name="imstscaxconnectingtext-property"></a>IMsTscAx::ConnectingText (Eigenschaft)

Gibt den Text an, der zentriert im -Steuerelement angezeigt wird, während das Steuerelement eine Verbindung verbindet.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ConnectingText(
  [in]  BSTR newVal
);

HRESULT get_ConnectingText(
  [out] BSTR *pConnectingText
);
```



## <a name="property-value"></a>Eigenschaftswert

Der neue Anzeigetext.

## <a name="error-codes"></a>Fehlercodes

Geben Sie **S \_ OK zurück,** wenn erfolgreich.

Gibt ein **HRESULT** ungleich 0 (null) zurück, wenn ein Fehler auftritt.

## <a name="remarks"></a>Hinweise

Ein Beispiel für den Verbindungstext ist "Herstellen einer Verbindung mit dem Server...".

Das Festlegen der **ConnectingText-Eigenschaft** ist optional. Wenn es nicht festgelegt ist, wird das Steuerelement leer angezeigt, bevor eine Verbindung hergestellt wird.

Diese Eigenschaft kann nur festgelegt werden, wenn sich das Steuerelement nicht im verbundenen Zustand befindet. Sie gibt **E \_ FAIL zurück,** wenn sie aufgerufen wird, wenn das Steuerelement verbunden ist. Sie können überprüfen, ob das Steuerelement verbunden ist, indem Sie auf Verbindungsereignisse in [**IMsTscAxEvents**](imstscaxevents-interface.md) reagieren oder die [**Connected-Eigenschaft**](imstscax-connected.md) untersuchen.

Die **Get \_ ConnectingText-Eigenschaftsmethode** weist den erforderlichen Arbeitsspeicher für den Puffer zu, auf den der *pConnectingText-Parameter* zeigt. Beim Aufrufen von C/C++-Anwendungen muss der Arbeitsspeicher mit einem Aufruf der [**SysFreeString-Funktion frei**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) werden. Dies ist für Clients mit Visual Basic Skripterstellung nicht erforderlich.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx ist als 8C11EFAE-92C3-11D1-BC1E-00C04FA31489 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

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

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

