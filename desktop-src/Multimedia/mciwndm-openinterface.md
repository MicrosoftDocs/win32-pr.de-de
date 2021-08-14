---
title: MCIWNDM_OPENINTERFACE-Nachricht (Vfw.h)
description: Die MCIWNDM \_ OPENINTERFACE-Nachricht fügt den Datenstrom oder die Datei, der bzw. die der angegebenen Schnittstelle zugeordnet ist, an ein MCIWnd-Fenster an. Sie können diese Nachricht explizit oder mithilfe des MCIWndOpenInterface-Makros senden.
ms.assetid: 73cbd637-d315-4b39-a978-2b72aed1f303
keywords:
- MCIWNDM_OPENINTERFACE Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_OPENINTERFACE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83097ad6301dbfdb4636a8478c2df8e544207df334efd27fe9695f15e0693533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373507"
---
# <a name="mciwndm_openinterface-message"></a>MCIWNDM \_ OPENINTERFACE-Meldung

Die **MCIWNDM \_ OPENINTERFACE-Nachricht** fügt den Datenstrom oder die Datei, der bzw. die der angegebenen Schnittstelle zugeordnet ist, an ein MCIWnd-Fenster an. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndOpenInterface-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) senden.


```C++
MCIWNDM_OPENINTERFACE 
wParam = 0; 
lParam = (LPARAM) (LPUNKNOWN) pUnk; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*Punk*
</dt> <dd>

Zeiger auf eine IAVI-Schnittstelle, die auf eine Datei oder einen Datenstrom in einer Datei verweist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)
</dt> </dl>

 

 





