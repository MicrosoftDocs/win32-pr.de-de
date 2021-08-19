---
description: Die DVDAdm.DisableScreenSaver-Eigenschaft aktiviert oder deaktiviert den Systembildschirmschoner.
ms.assetid: 78a0512f-456a-45b6-8717-13593461a765
title: DisableScreenSaver-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bc714dbbdc3e9b144f2d49cb54871cdf09baad5df39f8e18b962d7fc415d44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821128"
---
# <a name="disablescreensaver-property"></a>DisableScreenSaver-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die -Eigenschaft aktiviert oder deaktiviert `DVDAdm.DisableScreenSaver` den Systembildschirmschoner.

``` syntax
[ bDisabled = ] DVD.DVDAdm.DisableScreenSaver
```

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob die Bildschirmschonereinstellungen des Systems für die DVD-Playeranwendung deaktiviert sind. TRUE bedeutet, dass die Einstellungen deaktiviert sind.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist mit dem Standardwert true gelesen/geschrieben. Beim Anzeigen DVD-Video Datenträgers verwendet ein Benutzer die Maus oder Tastatur in der Regel nicht für längere Zeit. Das MSWebDVD ActiveX®-Steuerelement deaktiviert daher standardmäßig den Systembildschirmschoner. Object

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RestoreScreenSaver**](restorescreensaver-method.md)
</dt> <dt>

[MSDVDAdm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 



