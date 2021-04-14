---
title: Imstscax connectingtext-Eigenschaft
description: Gibt den Text an, der im-Steuerelement zentriert angezeigt wird, während das Steuerelement eine Verbindung herstellt.
ms.assetid: 9bc82074-988f-491b-80e3-00c3f7ba437a
ms.tgt_platform: multiple
keywords:
- Connectingtext-Eigenschaft Remotedesktopdienste
- Connectingtext-Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
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
ms.openlocfilehash: 433da7d159f1fe5bf44114a0b76ed9b4d807046f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392073"
---
# <a name="imstscaxconnectingtext-property"></a>Imstscax:: connectingtext-Eigenschaft

Gibt den Text an, der im-Steuerelement zentriert angezeigt wird, während das Steuerelement eine Verbindung herstellt.

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

Der neue Anzeige Text.

## <a name="error-codes"></a>Fehlercodes

Gibt **\_ OK** zurück, wenn erfolgreich.

Gibt ein **HRESULT** ungleich 0 (null) zurück, wenn ein Fehler auftritt.

## <a name="remarks"></a>Bemerkungen

Ein Beispiel für den Verbindungs Text lautet "Verbindung mit Server wird hergestellt...".

Das Festlegen der **connectingtext** -Eigenschaft ist optional. Wenn Sie nicht festgelegt ist, wird das Steuerelement leer angezeigt, bevor eine Verbindung hergestellt wird.

Diese Eigenschaft kann nur festgelegt werden, wenn sich das Steuerelement nicht im verbundenen Zustand befindet. Es wird ein Fehler zurückgegeben, wenn er aufgerufen wird **, wenn das \_** Steuerelement verbunden ist. Sie können überprüfen, ob das Steuerelement verbunden ist, indem Sie auf Verbindungs Ereignisse in [**imstscaxevents**](imstscaxevents-interface.md) reagieren oder die [**verbundene**](imstscax-connected.md) Eigenschaft untersuchen.

Die Eigenschaften Methode **get \_ connectingtext** ordnet den für den Puffer erforderlichen Arbeitsspeicher zu, auf den der *pconnectingtext* -Parameter verweist. Beim Aufrufen von C/C++-Anwendungen muss der Arbeitsspeicher durch einen Aufruf der [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) -Funktion freigegeben werden. Dies ist für Visual Basic-und Skript Clients nicht erforderlich.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.<br/>            |



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

[**Imstscax**](imstscax-interface.md)
</dt> </dl>

 

