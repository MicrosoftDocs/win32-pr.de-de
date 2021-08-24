---
description: Die Play-Methode gibt den aktuellen DVD-Titel wieder.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Play-Methode (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d4cea7dc53afc6a116ad052da9a4ca0d52c2e8687d99bde854d3f89fa60a9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633560"
---
# <a name="play-method-directshow"></a>Play-Methode (DirectShow)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `Play` -Methode gibt den aktuellen DVD-Titel wieder.

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Wenn die Wiedergabe angehalten oder beendet wird und [**EnableResetOnStop**](enableresetonstop-property.md) true ist, setzt der Aufruf von **Play** die Wiedergabe an der aktuellen Position mit normaler Geschwindigkeit wieder auf. Wenn die Wiedergabe beendet wird und **EnableResetOnStop** auf FALSE festgelegt ist, wird beim Aufrufen von **Play** die Wiedergabe des Datenträgers am Anfang des ersten Titels gestartet.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Fortsetzen**](resume-method.md)
</dt> </dl>

 

 



