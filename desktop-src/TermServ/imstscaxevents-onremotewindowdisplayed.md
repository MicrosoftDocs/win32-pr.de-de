---
title: IMsTscAxEvents OnRemoteWindowDisplayed-Methode
description: Wird aufgerufen, wenn ein RemoteApp-Fenster angezeigt wird.
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- OnRemoteWindowDisplayed-Remotedesktopdienste
- OnRemoteWindowDisplayed-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnRemoteWindowDisplayed-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteWindowDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6985a71fe6351a81b2daef69401dfd5c65543e9984fd64c28a120704a34d5a8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512110"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a>IMsTscAxEvents::OnRemoteWindowDisplayed-Methode

Wird aufgerufen, wenn ein RemoteApp-Fenster angezeigt wird.

## <a name="syntax"></a>Syntax


```C++
void OnRemoteWindowDisplayed(
  [in] VARIANT_BOOL                   vbDisplayed,
  [in] HWND                           hwnd,
  [in] RemoteWindowDisplayedAttribute windowAttribute
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vbDisplayed* \[ In\]
</dt> <dd>

Typ: **VARIANT \_ BOOL**

Gibt an, ob das RemoteApp-Fenster angezeigt oder ausgeblendet wird.

</dd> <dt>

*hwnd* \[ In\]
</dt> <dd>

Typ: **HWND**

Das Handle des angezeigten Fensters.

</dd> <dt>

*windowAttribute* \[ In\]
</dt> <dd>

Typ: **[ **RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**

Ein Wert der [**RemoteWindowDisplayedAttribute-Enumeration,**](remotewindowdisplayedattribute.md) der weitere Informationen zum Ereignis angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





