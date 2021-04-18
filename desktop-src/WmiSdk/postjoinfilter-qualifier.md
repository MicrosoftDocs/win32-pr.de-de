---
description: Sie können die Instanzen einer Verknüpfungs Ansichts Klasse filtern, indem Sie dem postjoinfilter-Qualifizierer eine WQL-Abfrage zuweisen.
ms.assetid: 926a7262-ea6b-4a5a-8aa7-6ec0ae389031
ms.tgt_platform: multiple
title: Postjoinfilter-Qualifizierer
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
ms.openlocfilehash: ac86aeafefc8057a1612c5007e55e7633c655c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352196"
---
# <a name="postjoinfilter-qualifier"></a>Postjoinfilter-Qualifizierer

Sie können die Instanzen einer Verknüpfungs Ansichts Klasse filtern, indem Sie dem **postjoinfilter** -Qualifizierer eine WQL-Abfrage zuweisen. Der Wert der WQL-Abfrage wird auf die Instanzen der joinansichts Klasse angewendet. Sie können diesen Qualifizierer verwenden, um die Instanzen der Ansichts Klasse auf jene zu beschränken, die bestimmte Bedingungen erfüllen. Die folgende WQL-Abfrage filtert Instanzen einer Verknüpfungs Klasse, die auf der Grundlage von Instanzen von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)aufgerufen wird.


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



Es gibt mehrere Einschränkungen bei der Verwendung dieses Qualifizierers:

-   **Postjoinfilter** ist nur für Verknüpfungs Ansichts Klassen verfügbar.
-   Die in der Abfrage angegebenen Klassennamen und Eigenschaftsnamen verweisen auf die Eigenschaften der Ansichts Klasse, nicht auf die Quell Klasse.
-   Es ist kein Ausschluss der Eigenschaften zulässig. nur `SELECT *` typabfragen sind zulässig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Spezifische Qualifizierer für den Ansichts Anbieter**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

