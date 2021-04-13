---
title: IMsRdpClientAdvancedSettings3 connectionbarshowrestorebutton (Eigenschaft)
description: Gibt an, ob die Schaltfläche Wiederherstellen auf der Verbindungs Leiste angezeigt werden soll.
ms.assetid: a56c3c05-d253-404a-bf49-9c1d804802e0
ms.tgt_platform: multiple
keywords:
- Connectionbarshowrestorebutton-Eigenschaft Remotedesktopdienste
- Connectionbarshowrestorebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, connectionbarshowrestorebutton-Eigenschaft
- Connectionbarshowrestorebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, connectionbarshowrestorebutton-Eigenschaft
- Connectionbarshowrestorebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, connectionbarshowrestorebutton-Eigenschaft
- Connectionbarshowrestorebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, connectionbarshowrestorebutton-Eigenschaft
- Connectionbarshowrestorebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, connectionbarshowrestorebutton-Eigenschaft
- Connectionbarshowrestorebutton-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, connectionbarshowrestorebutton-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowRestoreButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae83ecde31461eff9c553782b8bfa3ae760fb54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391602"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowrestorebutton-property"></a>IMsRdpClientAdvancedSettings3:: connectionbarshowrestorebutton-Eigenschaft

Gibt an, ob die Schaltfläche **Wiederherstellen** auf der Verbindungs Leiste angezeigt werden soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ConnectionBarShowRestoreButton(
  [in]  VARIANT_BOOL fShowRestore
);

HRESULT get_ConnectionBarShowRestoreButton(
  [out] VARIANT_BOOL *pfShowRestore
);
```



## <a name="property-value"></a>Eigenschaftswert

Legen Sie **auf Variant \_ true** fest, um die Schaltfläche **Wiederherstellen** anzuzeigen, und auf **Variant \_ false** , um die Anzeige der Schaltfläche **Wiederherstellen** zu deaktivieren.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann nicht festgelegt werden, wenn das Steuerelement verbunden ist.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings3 ist als 19cd856b-c542-4c53-ACee-B127 e3be1a59 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





