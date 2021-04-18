---
description: Jede Eigenschaft in einer Ansichts Klasse muss über einen Zeichen folgen Array-Qualifizierer namens propertysources verfügen.
ms.assetid: df89680b-8ea7-4f38-81ba-c4132b944f37
ms.tgt_platform: multiple
title: Propertysources-Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertySources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3809977282a2bdf82d0b51ef8f566541b74fe28a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357420"
---
# <a name="propertysources-qualifier"></a>Propertysources-Qualifizierer

Jede Eigenschaft in einer Ansichts Klasse muss über einen Zeichen folgen Array-Qualifizierer namens **propertysources** verfügen. Der **propertysources** -Qualifizierer enthält den Namen der Quell Klassen Eigenschaft oder der Eigenschaften, von denen diese Eigenschaft der Ansichts Klasse Daten abruft. Die Reihenfolge der Werte in diesem Array entspricht der Reihenfolge der Quell Klassen, die für den [viewsources-Qualifizierer](viewsources-qualifier.md)definiert wurden. Im folgenden Beispiel wird gezeigt, wie eine Eigenschaft für eine Union-Ansichts Klasse definiert wird, die die Union der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse von zwei verschiedenen Computern ist:


```mof
[PropertySources{"DeviceID", "DeviceID"},key] String Devname;
```



Die erste **DeviceID** -Eigenschaft entspricht der **DeviceID** -Eigenschaft aus der-Klasse in der ersten Quell Abfrage. Die zweite Eigenschaft " **DeviceID** " ist die Eigenschaft " **DeviceID** " aus der-Klasse in der zweiten Quell Abfrage.

Wenn Sie Eigenschaften für joinansichts Klassen definieren, müssen Sie eine separate Ansichts Eigenschaft für jede der Quell Klasseneigenschaften definieren, es sei denn, die Quell Klasseneigenschaften sind die Basis der joinansichts Klasse. Im folgenden Beispiel werden Eigenschaften in einer joinansichts Klasse für ähnliche Eigenschaften der [**Win32- \_ Drucker**](/windows/desktop/CIMWin32Prov/win32-printer) Quell Klasse und der [**Win32 \_ printerconfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) -Quell Klasse erstellt:


```mof
[PropertySources{"VerticalResolution", ""}] Uint32 Vres;
[PropertySources{"", "YResolution"}] Uint32 Yres;
```



Wenn die beiden Quell Klassen durch eine gemeinsame Eigenschaft verknüpft werden, können Sie nur eine einzelne Ansichts Klassen Eigenschaft definieren, da der Wert beider Quell Klasseneigenschaften immer identisch ist. Im folgenden Beispiel wird gezeigt, wie die [**Win32- \_ Drucker**](/windows/desktop/CIMWin32Prov/win32-printer) Klasse und die [**Win32- \_ printerconfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) durch einen allgemeinen Eigenschafts Wert verknüpft werden:


```mof
[PropertySources{"DeviceId", "DeviceName "}] String Name;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Spezifische Qualifizierer für den Ansichts Anbieter**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

