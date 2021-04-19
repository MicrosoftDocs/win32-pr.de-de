---
description: Mit der setasclass-Methode des Objekts "errbemubjectpath" erzwingt der Pfad die Adressierung einer WMI-Klasse.
ms.assetid: d341b980-bac9-4db4-a55f-eb971fb385da
ms.tgt_platform: multiple
title: "' Errbemubjectpath. '-Eigenschaft (wbemdisp. h)"
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
ms.openlocfilehash: 371fe95c3a7152767c45849191658c4bcb661750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356874"
---
# <a name="swbemobjectpathsetasclass-property"></a>' Errbemubjectpath. '-Eigenschaft

Mit der **setasclass** -Methode des Objekts " [**errbemubjectpath**](swbemobjectpath.md) " erzwingt der Pfad die Adressierung einer WMI-Klasse.

Diese Eigenschaft ist lesegeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemObjectPath.SetAsClass
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="error-codes"></a>Fehlercodes

Nachdem Sie die **setasclass** -Eigenschaft erhalten oder festgelegt haben, enthält das **Err** -Objekt möglicherweise den folgenden Fehlercode.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Austausch Pfad<br/>                                                       |
| IID<br/>                      | IID \_ iswbemubjectpath<br/>                                                        |



 

 




