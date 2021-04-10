---
description: Das taubemprivilege-Objekt stellt eine einzelne Berechtigung dar. Dieses Objekt kann nicht durch den VBScript-Befehl "up-Object" erstellt werden.
ms.assetid: 18ee4587-6347-4075-b5e9-c5fb02f3cbf7
ms.tgt_platform: multiple
title: Taubemprivilege-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege
- ISWbemPrivilege
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c3be448b4088011cd4d628a7d98b448af550b010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050512"
---
# <a name="swbemprivilege-object"></a>Taubemprivilege-Objekt

Das **taubemprivilege** -Objekt stellt eine einzelne Berechtigung dar. Dieses Objekt kann nicht durch den VBScript-Befehl "up- **Object** " erstellt werden.

## <a name="members"></a>Member

Das **taubemprivilege** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **taubemprivilege** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                     | Zugriffstyp           | BESCHREIBUNG                                                                      |
|:-------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------|
| [**Display Name**](swbemprivilege-displayname.md)<br/> | Schreibgeschützt<br/>  | Anzeige Name dieser Berechtigung.<br/>                                       |
| [**Bezeichner**](swbemprivilege-identifier.md)<br/>   | Lesen/Schreiben<br/> | Eine ganze Zahl, die die Berechtigung darstellt, die festgelegt oder abgerufen wird.<br/> |
| [**isEnabled**](swbemprivilege-isenabled.md)<br/>     | Lesen/Schreiben<br/> | Boolescher Wert, der angibt, ob dieses Privileg aktiviert ist.<br/>            |
| [**Name**](swbemprivilege-name.md)<br/>               | Schreibgeschützt<br/>  | Der Name dieser Berechtigung.<br/>                                               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Berechtigung<br/>                                                        |
| IID<br/>                      | IID \_ iswbemprivilege<br/>                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ausführen privilegierter Vorgänge](executing-privileged-operations.md)
</dt> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




