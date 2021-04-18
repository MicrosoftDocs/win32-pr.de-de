---
title: Remotesessionaktionstyp-Enumeration
description: Wird verwendet, um den Typ der Remote Aktion anzugeben.
ms.assetid: C0DA0FA2-6FE0-4B40-B169-4592A1BE2AD6
ms.tgt_platform: multiple
keywords:
- Remotesessionaktionstyp-Enumeration Remotedesktopdienste
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
ms.openlocfilehash: 291bb9fdd2cadfef3881bc27a47f9fc1bb1bce68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340318"
---
# <a name="remotesessionactiontype-enumeration"></a>Remotesessionaktionstyp-Enumeration

Wird verwendet, um den Typ der Remote Aktion anzugeben.

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

<span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**Remotesessionaktionszeichen**
</dt> <dd>

Zeigt die Charms in der Remote Sitzung an.

</dd> <dt>

<span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**Remotesessionaktionsleiste**
</dt> <dd>

Hiermit wird die APP-Leiste in der Remote Sitzung angezeigt.

</dd> <dt>

<span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**Remotesessionaktionssnap**
</dt> <dd>

Dockt die Anwendung in der Remote Sitzung an. Diese Option wurde als veraltet markiert und sollte nicht verwendet werden.

</dd> <dt>

<span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**Remotesessionaction Startscreen**
</dt> <dd>

Bewirkt, dass der Startbildschirm in der Remote Sitzung angezeigt wird.

</dd> <dt>

<span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**Remotesessionaktionsswitch**
</dt> <dd>

Bewirkt, dass das Fenster "Anwendungs Switch" in der Remote Sitzung angezeigt wird. Dies ist das gleiche wie beim Drücken von Alt + Tab.

</dd> <dt>

<span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**Remotesessionaktionscenter**
</dt> <dd>

Bewirkt, dass das Aktions Center in der Remote Sitzung angezeigt wird. Dies entspricht dem Benutzer, der "Win + A" drückt.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012 und Windows 8:** Dieser Wert wird vor Windows Server 2016 und Windows 10 nicht unterstützt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClient8:: sendremoteaction**](imsrdpclient8-sendremoteaction.md)
</dt> </dl>

 

 





