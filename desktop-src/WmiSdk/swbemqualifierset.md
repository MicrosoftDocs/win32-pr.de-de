---
description: Ein "taubemqualifierset"-Objekt ist eine Sammlung von "taubemqualifier"-Objekten.
ms.assetid: 7ac5469c-357b-499d-a558-30bf760c5311
ms.tgt_platform: multiple
title: Taubemqualifierset-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet
- ISWbemQualifierSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e74b495313e8061cc6e08e255d1d055bb2f72a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050510"
---
# <a name="swbemqualifierset-object"></a>Taubemqualifierset-Objekt

Ein " **taubemqualifierset** "-Objekt ist eine Sammlung von " [**taubemqualifier**](swbemqualifier.md) "-Objekten. Der Auflistung werden Elemente mithilfe der [**Add**](swbemqualifierset-add.md) -Methode hinzugefügt, die mithilfe der- [**Element**](swbemqualifierset-item.md) Methode aus der Auflistung abgerufen und mithilfe der [**Remove**](swbemqualifierset-remove.md) -Methode aus der Auflistung entfernt werden. Dieses Objekt kann nicht durch den VBScript-Befehl "up- [Object](creating-an-object-using-vbscript.md) " erstellt werden.

Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).

Die [**austaubemqualifier**](swbemqualifier.md) -Objekte, aus denen sich eine **Swap** -Auflistung besteht, beschreiben die Qualifizierer, die an eine WMI-Klasse, eine Instanz, eine Methode oder einen Methoden Parameter angefügt sind.

## <a name="members"></a>Member

Das Objekt " **taubemqualifierset** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **taubemqualifierset** -Objekt verfügt über diese Methoden.



| Methode                                     | BESCHREIBUNG                                                                                                 |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Eren**](swbemqualifierset-add.md)       | Fügt der Auflistung von " **taubemqualifierset** " ein " [**taubemqualifier**](swbemqualifier.md) "-Objekt hinzu.<br/> |
| [**Element**](swbemqualifierset-item.md)     | Gibt [**ein benanntes**](swbemqualifier.md) -Objekt aus der Auflistung zurück.<br/>             |
| [**Aufgeh**](swbemqualifierset-remove.md) | Löscht einen benannten Qualifizierer aus der Auflistung.<br/>                                                   |



 

### <a name="properties"></a>Eigenschaften

Das **taubemqualifierset** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                            | Zugriffstyp          | BESCHREIBUNG                                                                     |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [**Countdown**](swbemqualifierset-count.md)<br/> | Schreibgeschützt<br/> | Enthält die Anzahl der Elemente in einer Auflistung von " **taubemqualifierset** ".<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Gruppe<br/>                                                     |
| IID<br/>                      | IID \_ iswbemqualifierset<br/>                                                      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




