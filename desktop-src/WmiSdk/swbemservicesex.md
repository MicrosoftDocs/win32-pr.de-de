---
description: Erweitert die Funktionalität von SWbemServices.
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.tgt_platform: multiple
title: SWbemServicesEx-Objekt (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx
- ISWbemServicesEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f7b63cbf6bc048350546b431b4f967c815450abf2d79c7ba79ab8f84e562a1bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107838"
---
# <a name="swbemservicesex-object"></a>SWbemServicesEx-Objekt

Das **SWbemServicesEx-Objekt** erweitert die Funktionalität von [**SWbemServices**](swbemservices.md). Die [**Put-**](swbemservicesex-put.md) und [**PutAsync-Methoden**](swbemservicesex-putasync.md) ermöglichen das Speichern einer Klasse oder Instanz in mehreren Namespaces oder in einem anderen Namespace als dem, in dem eine Instanz erstellt wurde. Dieses Objekt kann nicht durch den [VBScript-CreateObject-Aufruf](/previous-versions//xzysf6hc(v=vs.85)) erstellt werden.

## <a name="members"></a>Member

Das **SWbemServicesEx-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **SWbemServicesEx-Objekt** verfügt über diese Methoden.



| Methode                                       | BESCHREIBUNG                                                                                                                                                                                                               |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Put**](swbemservicesex-put.md)           | Speichert das -Objekt im Namespace, der an das **SWbemServicesEx-Objekt** gebunden ist, und gibt ein [**SWbemObjectPath-Objekt**](swbemobjectpath.md) zurück, das den Pfad des Objekts enthält, in das die Daten geschrieben wurden.<br/> |
| [**PutAsync**](swbemservicesex-putasync.md) | Speichert ein Objekt asynchron in einem Namespace.<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>Hinweise

Die Methoden in dieser Klasse können entweder im semisynchronen Modus oder im asynchronen Modus aufgerufen werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ ISWbemServicesEx<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemServicesEx<br/>                                                        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Skripterstellung für API-Objekte](scripting-api-objects.md)
</dt> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

