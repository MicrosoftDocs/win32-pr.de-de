---
title: IMsTscAxEvents OnAuthenticationWarningDisplayed-Methode
description: Wird aufgerufen, bevor ein ActiveX-Steuerelement ein Authentifizierungsdialogfeld anzeigt (z. B. das Dialogfeld zertifikatfehler).
ms.assetid: ce307e5f-5e26-4041-bbd5-6871c0678da4
ms.tgt_platform: multiple
keywords:
- OnAuthenticationWarningDisplayed-Methode Remotedesktopdienste
- OnAuthenticationWarningDisplayed-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnAuthenticationWarningDisplayed-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df2de56a612c748db720e485d9f1e6e5750c9fc3281500dfddd751f41aed1641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118854008"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a>IMsTscAxEvents::OnAuthenticationWarningDisplayed-Methode

Wird aufgerufen, bevor ein ActiveX-Steuerelement ein Authentifizierungsdialogfeld anzeigt (z. B. das Dialogfeld zertifikatfehler).

## <a name="syntax"></a>Syntax


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Bei Bedarf kann die [**UIParentWindowHandle-Eigenschaft**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) der [**IMsRdpClientNonScriptable2-Schnittstelle**](imsrdpclientnonscriptable2.md) verwendet werden, um sicherzustellen, dass das anzuzeigende modale Authentifizierungsdialogfeld von einem angegebenen Fenster übergeordnet wird (dies kann erforderlich sein, um zu verhindern, dass Benutzer andere Dialogfelder verwenden, während das Authentifizierungsdialogfeld angezeigt wird). Standardmäßig ist das übergeordnete Element das ActiveX Steuerelementfenster.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008, Windows Server 2008 mit SP1<br/>                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





