---
title: IMsTscAxEvents OnAuthenticationWarningDismissed-Methode
description: Wird aufgerufen, nachdem ein ActiveX-Steuerelement ein Authentifizierungsdialogfeld anzeigt (z. B. das Dialogfeld "Zertifikatfehler").
ms.assetid: bf5dbe4a-9129-47b3-9808-ed09d9010099
ms.tgt_platform: multiple
keywords:
- OnAuthenticationWarningDismissed-Methode Remotedesktopdienste
- OnAuthenticationWarningDismissed-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnAuthenticationWarningDismissed-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDismissed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a55af8450160e271e96c53d4d5a9d4390393ab7880d2c2bb143cf0e6a1cb3bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125230"
---
# <a name="imstscaxeventsonauthenticationwarningdismissed-method"></a>IMsTscAxEvents::OnAuthenticationWarningDismissed-Methode

Wird aufgerufen, nachdem ein ActiveX-Steuerelement ein Authentifizierungsdialogfeld anzeigt (z. B. das Dialogfeld "Zertifikatfehler").

## <a name="syntax"></a>Syntax


```C++
void OnAuthenticationWarningDismissed();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Bei Bedarf kann die [**UIParentWindowHandle-Eigenschaft**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) der [**IMsRdpClientNonScriptable2-Schnittstelle**](imsrdpclientnonscriptable2.md) verwendet werden, um alle übergeordneten Daten wiezu kehren, die möglicherweise in der [**OnAuthenticationWarningDisplayed-Methode**](imstscaxevents-onauthenticationwarningdisplayed.md) durchgeführt wurden.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008, Windows Server 2008 mit SP1<br/>                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





