---
description: Die volumesavailable-Eigenschaft ruft die Anzahl der Volumes in einem mehrteiligen Satz ab.
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: Volumesavailable (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccdcf32ba8b7bea3958ef469bc0f90f9d41ecc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356260"
---
# <a name="volumesavailable-property"></a>Volumesavailable (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `VolumesAvailable` Eigenschaft ruft die Anzahl der Volumes in einem mehrteiligen Satz ab.

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Volumes im Satz als Ganzzahl zurück.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf. Einige DVD-Titel können als Multidisk-Satz oder-Reihe freigegeben werden. Verwenden Sie diese Methode, um die Volumenummer für den aktuellen Festplattenspeicher zu ermitteln.

 

 



