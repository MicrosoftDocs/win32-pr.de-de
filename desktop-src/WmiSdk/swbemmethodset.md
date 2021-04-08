---
description: Ein "taubemmethodset"-Objekt ist eine Sammlung von "taubemmethod"-Objekten. Elemente werden mit der Item-Methode abgerufen. Weitere Informationen finden Sie unter Zugreifen auf eine Sammlung. Dieses Objekt kann nicht durch den VBScript-Befehl "up-Object" erstellt werden.
ms.assetid: 0ca2601f-ed40-472e-b4f2-eee750c8c8d1
ms.tgt_platform: multiple
title: Taubemmethodset-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet
- ISWbemMethodSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d47c4dc8335077d6f8568be4b56200558942ac39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865663"
---
# <a name="swbemmethodset-object"></a>Taubemmethodset-Objekt

Ein " **taubemmethodset** "-Objekt ist eine Sammlung von " [**taubemmethod**](swbemmethod.md) "-Objekten. Elemente werden mit der [**Item**](swbemmethodset-item.md) -Methode abgerufen. Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md). Dieses Objekt kann nicht durch den VBScript-Befehl "up- **Object** " erstellt werden.

> [!Note]  
> In dieser Version der API wird Schreibzugriff auf Methoden Informationen nicht unterstützt. Wenn Sie Methoden definieren oder vorhandene Methoden Definitionen ändern möchten, können Sie die Methoden Änderungen in einer MOF-Datei definieren und die Änderungen mithilfe des MOF-Compilers übermitteln. Alternativ können Sie die WMI-com-API verwenden.

 

## <a name="members"></a>Member

Das Objekt " **Swap-methodset** " verfügt über diese Typen von Membern:

-   [Methoden](#swbemmethodset-object)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **taubemmethodset** -Objekt verfügt über diese Methoden.



| Methode                              | BESCHREIBUNG                                                                                                                                  |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Element**](swbemmethodset-item.md) | Ruft [**ein-**](swbemmethod.md) Objekt aus der-Auflistung ab. Dies ist die standardmäßige Automatisierungs Methode dieses Objekts.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das Objekt " **Swap-methodset** " verfügt über diese Eigenschaften.



| Eigenschaft                                         | Zugriffstyp          | BESCHREIBUNG                                       |
|:-------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Countdown**](swbemmethodset-count.md)<br/> | Schreibgeschützt<br/> | Die Anzahl der Elemente in der Auflistung.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Methode<br/>                                                        |
| IID<br/>                      | IID \_ iswbemmethodset<br/>                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




