---
title: Imstscaxevents onremotewindowview-Methode
description: Wird aufgerufen, wenn ein RemoteApp-Fenster angezeigt wird.
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- Onremotewindowview-Methode Remotedesktopdienste
- Onremotewindowview-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onremotewindowview-Methode
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
ms.openlocfilehash: f03029f31e1ce2133c74c92c0d6d57f192e4d85f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392023"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a>Imstscaxevents:: onremotewindowview-Methode

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

*vbangezeigte* \[ in\]
</dt> <dd>

Typ: **Variant \_ bool**

Gibt an, ob das RemoteApp-Fenster angezeigt oder ausgeblendet wird.

</dd> <dt>

*HWND* \[ in\]
</dt> <dd>

Typ: **HWND**

Das Handle des angezeigten Fensters.

</dd> <dt>

*windowattribute* \[ in\]
</dt> <dd>

Typ: **[ **remotewindowdisplayedattribute**](remotewindowdisplayedattribute.md)**

Ein Wert der [**remotewindowdisplayedattribute**](remotewindowdisplayedattribute.md) -Enumeration, der weitere Informationen über das Ereignis angibt.

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

[**Remotewindowdisplayedattribute**](remotewindowdisplayedattribute.md)
</dt> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





