---
description: Die ActivateButton-Methode aktiviert die ausgewählte Menüschaltfläche.
ms.assetid: 1da486a0-dadc-4c92-b3d3-83aeace01e39
title: ActivateButton-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64853a191f688758deb42061e95c91308ff88c00fe9482cce677f8b00926f26f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873520"
---
# <a name="activatebutton-method"></a>ActivateButton-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die ActivateButton-Methode aktiviert die ausgewählte Menüschaltfläche.

``` syntax
        MSWebDVD.ActivateButton()
```

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, wenn Sie eine benutzerdefinierte Mausbehandlung implementieren, nachdem [**Sie DisableAutoMouseProcessing auf**](disableautomouseprocessing-property.md) **TRUE festlegen.**

Verwenden Sie diese Methode, um eine Schaltfläche zu aktivieren, die über die [**SelectLeftButton-,**](selectleftbutton-method.md) [**SelectLowerButton-,**](selectlowerbutton-method.md) [**SelectUpperButton-**](selectupperbutton-method.md)oder [**SelectRightButton-Methode ausgewählt**](selectrightbutton-method.md) wurde.

 

 



