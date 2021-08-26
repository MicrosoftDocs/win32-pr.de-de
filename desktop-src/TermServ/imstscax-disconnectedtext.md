---
title: IMsTscAx DisconnectedText-Eigenschaft
description: Gibt den Text an, der im Steuerelement zentriert angezeigt wird, bevor eine Verbindung beendet wird.
ms.assetid: ec7efe7a-8fb9-4c45-8e16-78951365de13
ms.tgt_platform: multiple
keywords:
- DisconnectedText-Eigenschaft Remotedesktopdienste
- DisconnectedText-Eigenschaft Remotedesktopdienste , IMsTscAx-Schnittstelle
- IMsTscAx-Schnittstelle Remotedesktopdienste , DisconnectedText-Eigenschaft
- DisconnectedText-Eigenschaft Remotedesktopdienste , IMsRdpClient-Schnittstelle
- IMsRdpClient-Schnittstelle Remotedesktopdienste , DisconnectedText-Eigenschaft
- DisconnectedText-Eigenschaft Remotedesktopdienste , IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste , DisconnectedText-Eigenschaft
- DisconnectedText-Eigenschaft Remotedesktopdienste , IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste , DisconnectedText-Eigenschaft
- DisconnectedText-Eigenschaft Remotedesktopdienste , IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste , DisconnectedText-Eigenschaft
- DisconnectedText-Eigenschaft Remotedesktopdienste , IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste , DisconnectedText-Eigenschaft
- DisconnectedText-Eigenschaft Remotedesktopdienste , IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste , DisconnectedText-Eigenschaft
- DisconnectedText-Eigenschaft Remotedesktopdienste , IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste , DisconnectedText-Eigenschaft
- DisconnectedText-Eigenschaft Remotedesktopdienste , IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste , DisconnectedText-Eigenschaft
- DisconnectedText-Eigenschaft Remotedesktopdienste , IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste , DisconnectedText-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.DisconnectedText
- IMsTscAx.get_DisconnectedText
- IMsTscAx.put_DisconnectedText
- IMsRdpClient.DisconnectedText
- IMsRdpClient.get_DisconnectedText
- IMsRdpClient.put_DisconnectedText
- IMsRdpClient2.DisconnectedText
- IMsRdpClient2.get_DisconnectedText
- IMsRdpClient2.put_DisconnectedText
- IMsRdpClient3.DisconnectedText
- IMsRdpClient3.get_DisconnectedText
- IMsRdpClient3.put_DisconnectedText
- IMsRdpClient4.DisconnectedText
- IMsRdpClient4.get_DisconnectedText
- IMsRdpClient4.put_DisconnectedText
- IMsRdpClient5.DisconnectedText
- IMsRdpClient5.get_DisconnectedText
- IMsRdpClient5.put_DisconnectedText
- IMsRdpClient6.DisconnectedText
- IMsRdpClient6.get_DisconnectedText
- IMsRdpClient6.put_DisconnectedText
- IMsRdpClient7.DisconnectedText
- IMsRdpClient7.get_DisconnectedText
- IMsRdpClient7.put_DisconnectedText
- IMsRdpClient8.DisconnectedText
- IMsRdpClient8.get_DisconnectedText
- IMsRdpClient8.put_DisconnectedText
- IMsRdpClient9.DisconnectedText
- IMsRdpClient9.get_DisconnectedText
- IMsRdpClient9.put_DisconnectedText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bcee521e5956242380c48fb07020db32eafeadb88f919ec6a20bdf2a10c4a23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125449"
---
# <a name="imstscaxdisconnectedtext-property"></a>IMsTscAx::D isconnectedText-Eigenschaft

Gibt den Text an, der im Steuerelement zentriert angezeigt wird, bevor eine Verbindung beendet wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DisconnectedText(
  [in]  BSTR newVal
);

HRESULT get_DisconnectedText(
  [out] BSTR *pDisconnectedText
);
```



## <a name="property-value"></a>Eigenschaftswert

Der neue Anzeigetext.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Hinweise

Das Festlegen der **DisconnectedText-Eigenschaft** ist optional. Wenn es nicht angegeben ist, wird das Steuerelement leer angezeigt, bevor eine Verbindung hergestellt wird.

Diese Eigenschaft kann nur festgelegt werden, wenn sich das Steuerelement nicht im verbundenen Zustand befindet. Die -Methode gibt **E \_ FAIL** zurück, wenn sie aufgerufen wird, nachdem das Steuerelement verbunden wurde. Sie können überprüfen, ob das Steuerelement verbunden ist, indem Sie auf Verbindungsereignisse in [**IMsTscAxEvents**](imstscaxevents-interface.md) reagieren oder die [**Connected-Eigenschaft**](imstscax-connected.md) untersuchen.

Diese Methode belegt den Arbeitsspeicher, der für den Puffer erforderlich ist, auf den der *pDisconnectedText-Parameter* zeigt. Beim Aufrufen von C/C++-Anwendungen muss der Arbeitsspeicher durch einen Aufruf der [**SysFreeString-Funktion**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) freigegeben werden. Dies ist für Visual Basic- und Skriptclients nicht erforderlich.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

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

 

