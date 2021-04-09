---
description: Mit der dvdadm. disablescreen-Eigenschaft wird der Bildschirmschoner des Systems aktiviert oder deaktiviert.
ms.assetid: 78a0512f-456a-45b6-8717-13593461a765
title: Disablebildschirm (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d651026f2bf09f872655a0ef58accb3a6173dcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860011"
---
# <a name="disablescreensaver-property"></a>Disablebildschirm (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Mit der- `DVDAdm.DisableScreenSaver` Eigenschaft wird der Bildschirmschoner des Systems ein-oder ausgeschaltet.

``` syntax
[ bDisabled = ] DVD.DVDAdm.DisableScreenSaver
```

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob die Bildschirmschoner Einstellungen des Systems für die DVD-Player-Anwendung deaktiviert sind. "true" bedeutet, dass die Einstellungen deaktiviert sind.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft verfügt über Lese-/Schreibzugriff mit dem Standardwert true. Beim Anzeigen einer DVD-Video Diskette verwendet ein Benutzer in der Regel nicht die Maus oder Tastatur für einen längeren Zeitraum. Das mswebdvd-ActiveX-®-Steuerelement deaktiviert daher standardmäßig den Bildschirmschoner des Systems. Object

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Restoreskreensaver**](restorescreensaver-method.md)
</dt> <dt>

[Msdvdadm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 



