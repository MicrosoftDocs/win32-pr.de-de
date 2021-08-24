---
title: RemoteSessionActionType-Enumeration
description: Wird verwendet, um den Typ der Remoteaktion anzugeben.
ms.assetid: C0DA0FA2-6FE0-4B40-B169-4592A1BE2AD6
ms.tgt_platform: multiple
keywords:
- RemoteSessionActionType-Remotedesktopdienste
topic_type:
- apiref
api_name:
- RemoteSessionActionType
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a107ee44f058d776a906fef37b2e384ed6d8970224c44a6846b257c5f336c515
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865710"
---
# <a name="remotesessionactiontype-enumeration"></a>RemoteSessionActionType-Enumeration

Wird verwendet, um den Typ der Remoteaktion anzugeben.

## <a name="syntax"></a>Syntax


```C++
typedef enum _RemoteSessionActionType { 
  RemoteSessionActionCharms        = 0,
  RemoteSessionActionAppbar        = 1,
  RemoteSessionActionSnap          = 2,
  RemoteSessionActionStartScreen   = 3,
  RemoteSessionActionAppSwitch     = 4,
  RemoteSessionActionActionCenter  = 4
} RemoteSessionActionType;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**RemoteSessionActionCharms**
</dt> <dd>

Zeigt die Charms in der Remotesitzung an.

</dd> <dt>

<span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**RemoteSessionActionAppbar**
</dt> <dd>

Zeigt die App-Leiste in der Remotesitzung an.

</dd> <dt>

<span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**RemoteSessionActionSnap**
</dt> <dd>

Dockt die Anwendung in der Remotesitzung an. Diese Option ist veraltet und sollte nicht verwendet werden.

</dd> <dt>

<span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**RemoteSessionActionStartScreen**
</dt> <dd>

Bewirkt, dass der Startbildschirm in der Remotesitzung angezeigt wird.

</dd> <dt>

<span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**RemoteSessionActionAppSwitch**
</dt> <dd>

Bewirkt, dass das Fenster des Anwendungswechsels in der Remotesitzung angezeigt wird. Dies ist identisch mit dem Benutzer, der ALT+TAB drückt.

</dd> <dt>

<span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**RemoteSessionActionActionCenter**
</dt> <dd>

Bewirkt, dass das Action Center in der Remotesitzung angezeigt wird. Dies ist identisch mit dem Benutzer, der Win+A drückt.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012 und Windows 8:** Dieser Wert wird nicht unterstützt, bevor Windows Server 2016 und Windows 10.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClient8::SendRemoteAction**](imsrdpclient8-sendremoteaction.md)
</dt> </dl>

 

 





