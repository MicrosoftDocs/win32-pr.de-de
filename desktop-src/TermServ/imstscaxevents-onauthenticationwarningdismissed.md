---
title: Imstscaxevents onauthenticationwarningverworfen-Methode
description: Wird aufgerufen, nachdem ein ActiveX-Steuerelement ein Authentifizierungs Dialogfeld (z. b. das Dialogfeld Zertifikat Fehler) anzeigt.
ms.assetid: bf5dbe4a-9129-47b3-9808-ed09d9010099
ms.tgt_platform: multiple
keywords:
- Onauthenticationwarningverwerfen-Methode Remotedesktopdienste
- Onauthenticationwarningverwerfen-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onauthenticationwarningverworfen-Methode
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
ms.openlocfilehash: 86bdadfdbc8e0a1387a1f3aaf712188689d0f808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391873"
---
# <a name="imstscaxeventsonauthenticationwarningdismissed-method"></a>Imstscaxevents:: onauthenticationwarningverwerfen-Methode

Wird aufgerufen, nachdem ein ActiveX-Steuerelement ein Authentifizierungs Dialogfeld (z. b. das Dialogfeld Zertifikat Fehler) anzeigt.

## <a name="syntax"></a>Syntax


```C++
void OnAuthenticationWarningDismissed();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Bei Bedarf kann die [**uiparameentwindowhandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) -Eigenschaft der [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) -Schnittstelle verwendet werden, um die in der [**onauthenticationwarningused**](imstscaxevents-onauthenticationwarningdisplayed.md) -Methode möglicherweise ausgeführten übergeordneten Objekte rückgängig zu machen.

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

[**Onauthenticationwarningangezeigte**](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[**Uianentwindowhandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





