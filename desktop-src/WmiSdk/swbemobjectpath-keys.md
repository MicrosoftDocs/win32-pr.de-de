---
description: Die Keys-Eigenschaft des "errbemubjectpath"-Objekts ist ein "errbemnamedvalueset"-Objekt, das die Schlüsselwert Bindungen enthält. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: 1919403d-6dea-4d41-9bc7-a622a9c9c2c8
ms.tgt_platform: multiple
title: Errbemubjectpath. Keys-Eigenschaft (adoctint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Keys
- ISWbemObjectPath.Keys
- ISWbemObjectPath.get_Keys
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898ae7dac4a9c63273a8ff45a85b5bbb65aaa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042001"
---
# <a name="swbemobjectpathkeys-property"></a>Errbemubjectpath. Keys-Eigenschaft

Die **Keys** -Eigenschaft des " [**errbemubjectpath**](swbemobjectpath.md) "-Objekts ist ein " [**errbemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das die Schlüsselwert Bindungen enthält. Diese Eigenschaft ist schreibgeschützt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemObjectPath.Keys As Object
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="error-codes"></a>Fehlercodes

Nachdem Sie die **Keys** -Eigenschaft abgerufen haben, enthält das **Err** -Objekt möglicherweise den folgenden Fehlercode.

<dl> <dt>

**wbemErrNotSupported** -2147749900 (0x8004100c)
</dt> <dd>

Das Feature bzw. die Operation wird nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn ein Skript versucht, in diese Eigenschaft zu schreiben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                             |
| Header<br/>                   | <dl> <dt>Adoctint. h (Include wbemdisp. h)</dt> </dl> |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl>                    |
| CLSID<br/>                    | CLSID- \_ Swap-Austausch Pfad<br/>                                                                          |
| IID<br/>                      | IID \_ iswbemubjectpath<br/>                                                                           |



 

 




