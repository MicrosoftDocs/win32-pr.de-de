---
description: Die DVDAdm.RestoreScreenSaver-Methode stellt die Einstellungen des Systembildschirmschonrs wieder her.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: RestoreScreenSaver-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 684250b237105e391472237a5e7093855dd82ef5b59ffbbaa20ebecf386da302
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696970"
---
# <a name="restorescreensaver-method"></a>RestoreScreenSaver-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DVDAdm.RestoreScreenSaver` -Methode stellt die Einstellungen des Systembildschirmschonrs wieder her.

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Im Allgemeinen deaktiviert eine DVD-Anwendung den Bildschirmschoner des Systems beim Start, indem die [**DisableScreenSaver-Eigenschaft**](disablescreensaver-property.md) auf TRUE festgelegt wird, und aktiviert dann den Bildschirmschoner erneut, wenn die DVD-Anwendung durch Aufrufen von geschlossen `RestoreScreenSaver` wird. Wenn eine Anwendung die Bildschirmschonereinstellungen des Systems nicht verwendet, muss sie diese Methode nicht aufrufen oder die **DisableScreenSaver-Eigenschaft** festlegen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MSDVDAdm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 



