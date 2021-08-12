---
description: Die VolumesAvailable-Eigenschaft ruft die Anzahl der Volumes in einem Multivolumesatz ab.
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: VolumesAvailable-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0ab5b07f30e49f1bbe7655a2d66d9aaa683099df64cadf94b5dfffdd3b3af0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650937"
---
# <a name="volumesavailable-property"></a>VolumesAvailable-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `VolumesAvailable` -Eigenschaft ruft die Anzahl der Volumes in einem Multivolumesatz ab.

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Volumes in der Menge als ganze Zahl zurück.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt und hat keinen Standardwert. Einige DVD-Titel werden möglicherweise als Multidisc-Satz oder Serie veröffentlicht. Verwenden Sie diese Methode, um die Volumenummer für den aktuellen Datenträger zu bestimmen.

 

 



