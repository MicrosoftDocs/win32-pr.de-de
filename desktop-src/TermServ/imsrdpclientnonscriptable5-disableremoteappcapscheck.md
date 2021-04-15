---
title: IMsRdpClientNonScriptable5 disableremoteappcapscheck (Eigenschaft)
description: Gibt an, ob das Remotedesktop ActiveX-Steuerelement den Server nicht auf RemoteApp-Funktionen überprüfen soll.
ms.assetid: dcc44d4b-ece5-4f5b-a00a-f90d7a2fa11a
ms.tgt_platform: multiple
keywords:
- Disableremoteappcapscheck-Eigenschaft Remotedesktopdienste
- Disableremoteappcapscheck-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, disableremoteappcapscheck-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.get_DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.put_DisableRemoteAppCapsCheck
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f65b0e1b56b3a1152f71aff25d4cf65a4420d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479287"
---
# <a name="imsrdpclientnonscriptable5disableremoteappcapscheck-property"></a>IMsRdpClientNonScriptable5::D isableremoteappcapscheck-Eigenschaft

Gibt an, ob das Remotedesktop ActiveX-Steuerelement den Server nicht auf RemoteApp-Funktionen überprüfen soll. Wenn diese Eigenschaft **Variant \_ true** enthält, sollte das Steuerelement den Server nicht auf RemoteApp-Funktionen überprüfen. Wenn diese Eigenschaft **Variant \_ false** enthält, kann das Steuerelement den Server auf RemoteApp-Funktionen überprüfen.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DisableRemoteAppCapsCheck(
  [in]          VARIANT_BOOL fDisableRemoteAppCapsCheck
);

HRESULT get_DisableRemoteAppCapsCheck(
  [out, retval] VARIANT_BOOL *pfDisableRemoteAppCapsCheck
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt den neuen Eigenschafts Wert an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                             |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 ist als 4f 6996d5-d7b1-412c-b0ff-063718566907 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





