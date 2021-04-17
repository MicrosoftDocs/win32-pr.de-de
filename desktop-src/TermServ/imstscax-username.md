---
title: Imstscax username (Eigenschaft)
description: Gibt die Anmelde Informationen für den Benutzernamen an.
ms.assetid: 9be25003-b9aa-41bb-a5a9-512546175114
ms.tgt_platform: multiple
keywords:
- Username-Eigenschaft Remotedesktopdienste
- Username-Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, UserName-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.UserName
- IMsTscAx.get_UserName
- IMsTscAx.put_UserName
- IMsRdpClient.UserName
- IMsRdpClient.get_UserName
- IMsRdpClient.put_UserName
- IMsRdpClient2.UserName
- IMsRdpClient2.get_UserName
- IMsRdpClient2.put_UserName
- IMsRdpClient3.UserName
- IMsRdpClient3.get_UserName
- IMsRdpClient3.put_UserName
- IMsRdpClient4.UserName
- IMsRdpClient4.get_UserName
- IMsRdpClient4.put_UserName
- IMsRdpClient5.UserName
- IMsRdpClient5.get_UserName
- IMsRdpClient5.put_UserName
- IMsRdpClient6.UserName
- IMsRdpClient6.get_UserName
- IMsRdpClient6.put_UserName
- IMsRdpClient7.UserName
- IMsRdpClient7.get_UserName
- IMsRdpClient7.put_UserName
- IMsRdpClient8.UserName
- IMsRdpClient8.get_UserName
- IMsRdpClient8.put_UserName
- IMsRdpClient9.UserName
- IMsRdpClient9.get_UserName
- IMsRdpClient9.put_UserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a94a7f7d9fe5d6532de55f36a50094205fe1d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479029"
---
# <a name="imstscaxusername-property"></a>Imstscax:: Username-Eigenschaft

Gibt die Anmelde Informationen für den Benutzernamen an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_UserName(
  [in]  BSTR newVal
);

HRESULT get_UserName(
  [out] BSTR *pUserName
);
```



## <a name="property-value"></a>Eigenschaftswert

Der neue Benutzername.

## <a name="error-codes"></a>Fehlercodes

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="remarks"></a>Bemerkungen

Das Festlegen der **username** -Eigenschaft ist optional. Wenn Sie nicht angegeben ist, kann der Benutzer einen Benutzernamen angeben, wenn das Windows-Anmelde Dialogfeld während der Verbindung angezeigt wird.

Diese Eigenschaft kann nur festgelegt werden, wenn sich das Steuerelement nicht im verbundenen Zustand befindet. Es wird ein Fehler zurückgegeben, wenn er aufgerufen wird **, wenn das \_** Steuerelement verbunden ist. Sie können überprüfen, ob das Steuerelement verbunden ist, indem Sie auf Verbindungs Ereignisse in [**imstscaxevents**](imstscaxevents-interface.md) reagieren oder die [**verbundene**](imstscax-connected.md) Eigenschaft untersuchen.

Mit der Eigenschaften Methode **get \_ username** wird der erforderliche Arbeitsspeicher für den Puffer zugewiesen, auf den der *pVersion* -Parameter verweist. Beim Aufrufen von C/C++-Anwendungen muss der Arbeitsspeicher durch einen Aufruf der [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) -Funktion freigegeben werden. Dies ist für Visual Basic-und Skript Clients nicht erforderlich.

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

 

