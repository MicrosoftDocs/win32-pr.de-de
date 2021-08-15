---
title: WSMan.Error-Eigenschaft (WSManDisp.h)
description: Ruft zusätzliche Fehlerinformationen in einem XML-Stream für den vorherigen Aufruf einer WSMan-Methode ab, wenn Windows Remoteverwaltungsdienst kein Session-Objekt, ein ConnectionOptions-Objekt oder ein ResourceLocator-Objekt erstellen konnte.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Fehlereigenschaft Windows Remoteverwaltung
- Fehlereigenschaft Windows Remoteverwaltung, WSMan-Objekt
- WSMan-Objekt Windows Remoteverwaltung , Error-Eigenschaft
topic_type:
- apiref
api_name:
- WSMan.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d72c99150d3c6ac95e91e6a9674ab6364e8ea46fabf3d58d50556e129933cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742195"
---
# <a name="wsmanerror-property"></a>WSMan.Error-Eigenschaft

Ruft zusätzliche Fehlerinformationen in einem XML-Stream für den vorherigen Aufruf einer [**WSMan-Methode**](wsman.md) ab, wenn Windows Remoteverwaltungsdienst kein [**Session-Objekt,**](session.md) ein [**ConnectionOptions-Objekt**](connectionoptions.md) oder ein [**ResourceLocator-Objekt**](resourcelocator.md) erstellen konnte.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
WSMan.Error As BSTR
```



## <a name="property-value"></a>Eigenschaftswert

Die XML-Darstellung der Fehlerinformationen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Wsman**](wsman.md)
</dt> </dl>

 

 





