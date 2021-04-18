---
title: "\"Tviewcookie\" (textstor. h)"
description: Der Datentyp "tviewcookie" identifiziert eine Kontextansicht.
ms.assetid: e649b799-d0d6-4f2d-b9f1-28070eea9b16
keywords:
- "\"T\""
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb43f888f76410e83e89d037f39ea665ca548ec9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338128"
---
# <a name="tsviewcookie"></a>"T"

Der Datentyp " **tviewcookie** " identifiziert eine Kontextansicht.


```C++
typedef DWORD TsViewCookie;
```



## <a name="remarks"></a>Bemerkungen

Eine Anwendung muss für jede erstellte Ansicht **einen eindeutigen Wert** für den Wert von "Wert" angeben.

Der TSF-Manager erhält diesen Wert aus der Anwendung durch Aufrufen von [ITextStoreACP:: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) oder [itextstoreanchor:: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview). Der TSF-Manager verwendet diesen Wert, um die Sicht zu identifizieren, wenn verschiedene [ITextStoreACP-](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) oder [itextstoreanchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) -Methoden aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                             |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                         |
| Header<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITextStoreACP**](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[**ITextStoreACP:: GetActiveView**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview)
</dt> <dt>

[**Itextstoreanchor:: GetActiveView**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview)
</dt> </dl>

 

 





