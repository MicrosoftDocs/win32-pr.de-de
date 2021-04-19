---
description: Die currentvolume-Eigenschaft ruft die Volumenummer für das aktuelle Stammverzeichnis ab.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: Currentvolume (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b91c394be620dfc3f00b8793222848131355f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345387"
---
# <a name="currentvolume-property"></a>Currentvolume (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `CurrentVolume` Eigenschaft ruft die Volumenummer für das aktuelle Stammverzeichnis ab.

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a>Rückgabewert

Gibt einen Integer-Wert zurück, der das aktuelle DVD-Volume darstellt. Wenn eine Festplatte Teil eines Satzes mit mehreren Volumes ist, sollte der ganzzahlige Wert größer als 0 (null) sein.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Volumesesverfügbar**](volumesavailable-property.md)
</dt> </dl>

 

 



