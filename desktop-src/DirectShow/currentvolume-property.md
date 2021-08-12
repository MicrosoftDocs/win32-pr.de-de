---
description: Die CurrentVolume-Eigenschaft ruft die Volumenummer für das aktuelle Stammverzeichnis ab.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: CurrentVolume-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d07f9d82facc243654bad2e16e9a028e8cf920a51f15dd92cc879b0ea1340d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654602"
---
# <a name="currentvolume-property"></a>CurrentVolume-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `CurrentVolume` -Eigenschaft ruft die Volumenummer für das aktuelle Stammverzeichnis ab.

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der das aktuelle DVD-Volume darstellt. Wenn ein Datenträger Teil eines Mehrvolumesatzes ist, sollte der ganzzahlige Wert größer als 0 (null) sein.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt und hat keinen Standardwert.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**VolumesVerfügbar**](volumesavailable-property.md)
</dt> </dl>

 

 



