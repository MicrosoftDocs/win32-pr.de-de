---
description: Die SetAsClass-Methode des SWbemObjectPath-Objekts erzwingt, dass der Pfad eine WMI-Klasse adressiert.
ms.assetid: d341b980-bac9-4db4-a55f-eb971fb385da
ms.tgt_platform: multiple
title: SWbemObjectPath.SetAsClass-Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsClass
- ISWbemObjectPath.SetAsClass
- ISWbemObjectPath.put_SetAsClass
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2083dd2ef3d6edd40148a11b6a3d034d4199b2507855b53c164de3c34ba0a93f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503730"
---
# <a name="swbemobjectpathsetasclass-property"></a>SWbemObjectPath.SetAsClass(Eigenschaft)

Die **SetAsClass-Methode** des [**SWbemObjectPath-Objekts**](swbemobjectpath.md) erzwingt, dass der Pfad eine WMI-Klasse adressiert.

Diese Eigenschaft ist lesegeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemObjectPath.SetAsClass
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="error-codes"></a>Fehlercodes

Nachdem Sie die **SetAsClass-Eigenschaft erhalten** oder festgelegt haben, enthält das **Err-Objekt** möglicherweise den folgenden Fehlercode.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



 

 




