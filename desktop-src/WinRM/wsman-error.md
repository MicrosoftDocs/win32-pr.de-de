---
title: WSMAN. Error-Eigenschaft (WSManDisp. h)
description: Ruft zusätzliche Fehlerinformationen, die sich in einem XML-Stream befinden, für den vorhergehenden Aufrufe einer WSMAN-Methode ab, wenn Windows-Remoteverwaltung Dienst kein Sitzungs Objekt, kein ConnectionOptions-Objekt oder ResourceLocator-Objekt erstellen konnte.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Fehler Eigenschaft Windows-Remoteverwaltung
- Error-Eigenschaft Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, Fehler Eigenschaft
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
ms.openlocfilehash: 9f9e7ffd42d67807f2f7b6096a89ed91e3d95af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103803"
---
# <a name="wsmanerror-property"></a>WSMAN. Error (Eigenschaft)

Ruft zusätzliche Fehlerinformationen, die sich in einem XML-Stream befinden, für den vorhergehenden Aufrufe einer [**WSMAN**](wsman.md) -Methode ab, wenn Windows-Remoteverwaltung Dienst kein [**Sitzungs**](session.md) Objekt, kein [**ConnectionOptions**](connectionoptions.md) -Objekt oder [**ResourceLocator**](resourcelocator.md) -Objekt erstellen konnte.

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
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WSMAN**](wsman.md)
</dt> </dl>

 

 





