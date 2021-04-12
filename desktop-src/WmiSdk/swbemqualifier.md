---
description: Sie können die Eigenschaften des "taubemqualifier"-Objekts verwenden, um einen einzelnen Qualifizierer für eine WMI-Klasse, eine Instanz, eine Eigenschaft oder einen Methoden Parameter darzustellen. Dieses Objekt kann nicht durch den VBScript-Befehl "up-Object" erstellt werden.
ms.assetid: b5dbe98a-e1d8-4679-a563-c88760d08b79
ms.tgt_platform: multiple
title: Taubemqualifiziererobjekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifier
- ISWbemQualifier
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5e9a49832ffa1e38fbe6ee0f71e1f6a39c1b0ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215312"
---
# <a name="swbemqualifier-object"></a>Taubemqualifiziererobjekt

Sie können die Eigenschaften des " **taubemqualifier** "-Objekts verwenden, um einen einzelnen Qualifizierer für eine WMI-Klasse, eine Instanz, eine Eigenschaft oder einen Methoden Parameter darzustellen. Dieses Objekt kann nicht durch den VBScript-Befehl "up- [Object](creating-an-object-using-vbscript.md) " erstellt werden.

## <a name="members"></a>Member

Das Objekt " **Swap-Qualifizierer** " enthält diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **taubemqualifier** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                       | Zugriffstyp           | BESCHREIBUNG                                                                                           |
|:-------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------|
| [**Isänderte**](swbemqualifier-isamended.md)<br/>                       | Schreibgeschützt<br/>  | Boolescher Wert, der angibt, ob dieser Qualifizierer mit einem Zusammenarbeits Vorgang lokalisiert wurde.<br/> |
| [**IsLocal**](swbemqualifier-islocal.md)<br/>                           | Schreibgeschützt<br/>  | Boolescher Wert, der angibt, ob dieser Qualifizierer lokal ist.<br/>                                   |
| [**Isoverridable**](swbemqualifier-isoverridable.md)<br/>               | Lesen/Schreiben<br/> | Boolescher Wert, der angibt, ob dieser Qualifizierer bei der Weitergabe überschrieben werden kann.<br/>          |
| [**Name**](swbemqualifier-name.md)<br/>                                 | Schreibgeschützt<br/>  | Der Name dieses Qualifizierers.<br/>                                                                    |
| [**Propagatestoinstance**](swbemqualifier-propagatestoinstance.md)<br/> | Lesen/Schreiben<br/> | Boolescher Wert, der angibt, ob dieser Qualifizierer an eine-Instanz weitergegeben werden kann.<br/>           |
| [**Propagatestosubclass**](swbemqualifier-propagatestosubclass.md)<br/> | Schreibgeschützt<br/>  | Boolescher Wert, der angibt, ob dieser Qualifizierer an eine Unterklasse weitergegeben werden kann.<br/>            |
| [**Wert**](swbemqualifier-value.md)<br/>                               | Lesen/Schreiben<br/> | Der Variant-Wert dieses Qualifizierers. Dies ist die Standard Eigenschaft dieses Objekts.<br/>              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austausch Qualifizierer<br/>                                                        |
| IID<br/>                      | IID \_ iswbemqualifizierer<br/>                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




