---
title: MCIWNDM_OPENINTERFACE Meldung (VFW. h)
description: Die mciwndm- \_ openinterface-Nachricht fügt den Datenstrom oder die Datei, die der angegebenen Schnittstelle zugeordnet ist, einem mciwnd-Fenster an. Sie können diese Nachricht explizit oder mithilfe des mciwndopeninterface-Makros senden.
ms.assetid: 73cbd637-d315-4b39-a978-2b72aed1f303
keywords:
- MCIWNDM_OPENINTERFACE-Nachricht (Multimedia)
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
ms.openlocfilehash: 9c40453f4d587429508a5aae19bc432fc46088ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391507"
---
# <a name="mciwndm_openinterface-message"></a>Mciwndm- \_ openinterface-Meldung

Die **mciwndm- \_ openinterface** -Nachricht fügt den Datenstrom oder die Datei, die der angegebenen Schnittstelle zugeordnet ist, einem mciwnd-Fenster an. Sie können diese Nachricht explizit oder mithilfe des [**mciwndopeninterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) -Makros senden.


```C++
MCIWNDM_OPENINTERFACE 
wParam = 0; 
lParam = (LPARAM) (LPUNKNOWN) pUnk; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*Kro*
</dt> <dd>

Zeiger auf eine IAVI-Schnittstelle, die auf eine Datei oder einen Datenstrom in einer Datei zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndopeninterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)
</dt> </dl>

 

 





