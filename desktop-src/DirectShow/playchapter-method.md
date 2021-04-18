---
description: Die playchapter-Methode startet die Wiedergabe aus dem angegebenen Kapitel innerhalb des aktuellen Titels.
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: Playchapter-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab4600d8d4fc09c4b63fa423c66823e92e95a2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339644"
---
# <a name="playchapter-method"></a>Playchapter-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `PlayChapter` Methode startet die Wiedergabe aus dem angegebenen Kapitel innerhalb des aktuellen Titels.

``` syntax
MSWebDVD.PlayChapter(iChapter)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*ichapter*
</dt> <dd>

Gibt den Kapitel Index im aktuellen Titel als Ganzzahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Wenn das Ende des angegebenen Kapitels erreicht ist, setzt diese Methode fort, wenn vorhandene Kapitel vorhanden sind. Wenn Sie nur ein bestimmtes Kapitel wiedergeben möchten, verwenden Sie [**playchaptersauto stoppt**](playchaptersautostop-method.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Playchapterintitle**](playchapterintitle-method.md)
</dt> </dl>

 

 



