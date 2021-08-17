---
title: IMsRdpClientNonScriptable5 DisableConnectionBar-Eigenschaft
description: Gibt an, ob das Remotedesktop ActiveX-Steuerelement die Verbindungsleiste deaktivieren soll.
ms.assetid: 82c57b93-f976-43e6-97f9-3602bf97e466
ms.tgt_platform: multiple
keywords:
- DisableConnectionBar-Eigenschaft Remotedesktopdienste
- DisableConnectionBar-Eigenschaft Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , DisableConnectionBar-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableConnectionBar
- IMsRdpClientNonScriptable5.put_DisableConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f74fce650eb82514538eed7066b937c29f8618aba1eab7531f3bdb7e1127da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138743"
---
# <a name="imsrdpclientnonscriptable5disableconnectionbar-property"></a>IMsRdpClientNonScriptable5::D isableConnectionBar-Eigenschaft

Gibt an, ob das Remotedesktop ActiveX-Steuerelement die Verbindungsleiste deaktivieren soll. Wenn diese Eigenschaft **VARIANT \_ TRUE** enthält, sollte die Verbindungsleiste deaktiviert werden. Wenn diese Eigenschaft **VARIANT \_ FALSE** enthält, sollte die Verbindungsleiste aktiviert werden.

Diese Eigenschaft ist lesegeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DisableConnectionBar(
  [in] VARIANT_BOOL fDisableConnectionBar
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt den neuen Eigenschaftswert an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                             |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | \_IID-IMsRdpClientNonScriptable5 ist als 4f6996d5-d7b1-412c-b0ff-063718566907 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





