---
title: Imstscaxevents onauthenticationwarninggezeigte-Methode
description: Wird aufgerufen, bevor ein ActiveX-Steuerelement ein Authentifizierungs Dialogfeld (z. b. das Dialogfeld Zertifikat Fehler) anzeigt.
ms.assetid: ce307e5f-5e26-4041-bbd5-6871c0678da4
ms.tgt_platform: multiple
keywords:
- Onauthenticationwarningangezeigte-Methode Remotedesktopdienste
- Onauthenticationwarningangezeigte Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onauthenticationwarninggezeigte-Methode
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
ms.openlocfilehash: 33307adf103536cce5841effe2843a7c48fda357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103527"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a>Imstscaxevents:: onauthenticationwarninggezeigte-Methode

Wird aufgerufen, bevor ein ActiveX-Steuerelement ein Authentifizierungs Dialogfeld (z. b. das Dialogfeld Zertifikat Fehler) anzeigt.

## <a name="syntax"></a>Syntax


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Bei Bedarf kann die [**uiparameentwindowhandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) -Eigenschaft der [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) -Schnittstelle verwendet werden, um sicherzustellen, dass das Dialogfeld für die modale Authentifizierung, das angezeigt wird, von einem angegebenen Fenster übergeordnet wird (Dies ist möglicherweise erforderlich, um zu verhindern, dass Benutzer andere Dialogfelder verwenden, während das Authentifizierungs Dialogfeld angezeigt wird). Standardmäßig ist das übergeordnete Element das Fenster "ActiveX-Steuerelement".

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008, Windows Server 2008 mit SP1<br/>                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Onauthenticationwarningverworfen**](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[**Uianentwindowhandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





