---
title: Imstscaxevents onremoteprogramview-Methode
description: Wird aufgerufen, wenn ein RemoteApp-Programm angezeigt wird.
ms.assetid: 24f5ea52-0c13-4024-9448-5c2c1896ca8b
ms.tgt_platform: multiple
keywords:
- Onremoteprogramview-Methode Remotedesktopdienste
- Onremoteprogramview-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onremoteprogramview-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 584e54c487ec24a3c165fdd5eb8e22f243e07f23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742112"
---
# <a name="imstscaxeventsonremoteprogramdisplayed-method"></a>Imstscaxevents:: onremoteprogramview-Methode

Wird aufgerufen, wenn ein RemoteApp-Programm angezeigt wird.

## <a name="syntax"></a>Syntax


```C++
VOID OnRemoteProgramDisplayed(
  [in] VARIANT_BOOL vbDisplayed,
  [in] ULONG        uDisplayInformation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vbangezeigte* \[ in\]
</dt> <dd>

Gibt an, ob das RemoteApp-Programm angezeigt oder ausgeblendet wird.

</dd> <dt>

*udisplayinformation* \[ in\]
</dt> <dd>

Die Anzeigeinformationen.

<dt>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**Schiene \_ appdisplay \_ autoreconnct**


</dt> <dd>

Die automatische Wiederherstellung der Verbindung wird gerade ausgeführt.

</dd> <dt>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**Schiene \_ appdisplay \_ desktophooked**


</dt> <dd>

Der RemoteApp-Zähler wurde einfach auf NULL gesetzt.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Implementieren Sie diese Methode in der Ereignis Senke, um die Benachrichtigung zu erhalten, dass eine RemoteApp angezeigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



 

 





