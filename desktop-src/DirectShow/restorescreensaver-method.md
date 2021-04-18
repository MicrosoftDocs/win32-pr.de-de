---
description: Die dvdadm. restoreskreensaver-Methode stellt die Einstellungen des System Bildschirmschoners wieder her.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: Restoreskreensaver-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b747aa21815bb37cc7db2296347c9890a06914
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343551"
---
# <a name="restorescreensaver-method"></a>Restoreskreensaver-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `DVDAdm.RestoreScreenSaver` Methode stellt die Einstellungen des System Bildschirmschoners wieder her.

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Im allgemeinen deaktiviert eine DVD-Anwendung beim Start den Bildschirmschoner des Systems, indem die [**disablescreen**](disablescreensaver-property.md) -Eigenschaft auf true festgelegt wird. Anschließend wird der Bildschirmschoner erneut aktiviert, wenn die DVD-Anwendung durch Aufrufen von geschlossen wird `RestoreScreenSaver` . Wenn eine Anwendung die Bildschirmschoner Einstellungen des Systems nicht verwendet, muss diese Methode nicht aufgerufen oder die **disablescreen** -Eigenschaft festgelegt werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Msdvdadm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 



