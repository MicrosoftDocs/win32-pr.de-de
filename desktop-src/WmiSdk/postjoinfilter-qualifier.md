---
description: Sie können die Instanzen einer Joinansichtsklasse filtern, indem Sie dem PostJoinFilter-Qualifizierer eine WQL-Abfrage zuweisen.
ms.assetid: 926a7262-ea6b-4a5a-8aa7-6ec0ae389031
ms.tgt_platform: multiple
title: PostJoinFilter-Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostJoinFilter
api_type:
- NA
api_location: ''
ms.openlocfilehash: be491c0bfefe77c2bf016789786212047d5ca8d00570c84057b8e8e346fb382e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317024"
---
# <a name="postjoinfilter-qualifier"></a>PostJoinFilter-Qualifizierer

Sie können die Instanzen einer Joinansichtsklasse filtern, indem Sie dem **PostJoinFilter-Qualifizierer** eine WQL-Abfrage zuweisen. Der Wert der WQL-Abfrage wird auf die Instanzen der Joinansichtsklasse angewendet. Sie können diesen Qualifizierer verwenden, um die Instanzen Ihrer Ansichtsklasse auf Instanzen zu beschränken, die bestimmte Bedingungen erfüllen. Die folgende WQL-Abfrage filtert Instanzen einer Joinklasse namens basierend auf Instanzen von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



Es gibt mehrere Einschränkungen für die Verwendung dieses Qualifizierers:

-   **PostJoinFilter** ist nur zum Verbinden von Ansichtsklassen verfügbar.
-   Die in der Abfrage angegebenen Klassennamen und Eigenschaftennamen verweisen auf die Eigenschaften der Ansichtsklasse, nicht auf die Quellklasse.
-   Es ist kein Ausschluss von Eigenschaften zulässig. nur `SELECT *` Typabfragen sind zulässig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Qualifizierer, die für den Ansichtsanbieter spezifisch sind**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

