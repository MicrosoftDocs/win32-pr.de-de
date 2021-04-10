---
title: EM_GETTOUCHOPTIONS Meldung (RichEdit. h)
description: Ruft die Berührungs Optionen ab, die einem Rich-Edit-Steuerelement zugeordnet sind.
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- Windows-Steuerelemente für EM_GETTOUCHOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_GETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812d37de1972c6da205944d9913dc3fa046c205d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040847"
---
# <a name="em_gettouchoptions-message"></a>EM \_ gettouchoptions-Meldung

Ruft die Berührungs Optionen ab, die einem Rich-Edit-Steuerelement zugeordnet sind.


```C++
#define EM_GETTOUCHOPTIONS       (WM_USER + 310)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Abruf Optionen, die abgerufen werden sollen. Dieses Argument einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                        | Bedeutung                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**RTO- \_ showhandles**</dt> </dl>          | Ruft ab, ob die Fingerabdruck Zieh Geräte sichtbar sind.<br/> |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**RTO- \_ disablehandles**</dt> </dl> | Das Abrufen dieses Flags ist nicht implementiert.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert der Option zurück, die vom *wParam* -Parameter angegeben wird. Der Wert ist ungleich 0 (null), wenn *wParam* eine **RTO \_ showhandles** hat und die Fingerabdruck Zieh Zeichen sichtbar sind; andernfalls 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ settouchoptions**](em-settouchoptions.md)
</dt> </dl>

 

 





