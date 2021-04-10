---
description: Erweitert die Funktionalität von Swap Services.
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.tgt_platform: multiple
title: Taubemservicesex-Objekt (wbemdisp. h)
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
ms.openlocfilehash: 8ed41cbab38e24958705c24aefc9ea5e9e67357e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130972"
---
# <a name="swbemservicesex-object"></a>Taubemservicesex-Objekt

Das Objekt " **taubemservicesex** " erweitert die Funktionalität von " [**Swap Services**](swbemservices.md)". Die [**Put**](swbemservicesex-put.md) -Methode und die [**putasync**](swbemservicesex-putasync.md) -Methode ermöglichen es, eine Klasse oder eine Instanz in mehreren Namespaces oder in einem anderen Namespace als dem zu speichern, in dem eine Instanz erstellt wurde. Dieses Objekt kann nicht durch den VBScript-Befehl "up- [Object](/previous-versions//xzysf6hc(v=vs.85)) " erstellt werden.

## <a name="members"></a>Member

Das Objekt " **taubemservicesex** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das Objekt " **taubemservicesex** " verfügt über diese Methoden.



| Methode                                       | BESCHREIBUNG                                                                                                                                                                                                               |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Stellte**](swbemservicesex-put.md)           | Speichert das Objekt in dem Namespace, der an das Objekt " **errbemservicesex** " gebunden ist, und gibt ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt zurück, das den Pfad des Objekts enthält, in das die Daten geschrieben wurden.<br/> |
| [**Putasync**](swbemservicesex-putasync.md) | Speichert ein-Objekt asynchron in einem Namespace.<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Die Methoden in dieser Klasse können entweder im semisynchronen oder im asynchronen Modus aufgerufen werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ iswbemservicesex<br/>                                                      |
| IID<br/>                      | IID \_ iswbemservicesex<br/>                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

