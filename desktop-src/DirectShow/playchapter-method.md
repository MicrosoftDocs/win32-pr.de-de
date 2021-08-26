---
description: Die PlayChapter-Methode startet die Wiedergabe aus dem angegebenen Kapitel innerhalb des aktuellen Titels.
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: PlayChapter-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832b1da6940b26a3cc3a4ab5bdba8653806966f8a399b74eb5adf50600e22293
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102340"
---
# <a name="playchapter-method"></a>PlayChapter-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `PlayChapter` -Methode beginnt mit der Wiedergabe aus dem angegebenen Kapitel innerhalb des aktuellen Titels.

``` syntax
MSWebDVD.PlayChapter(iChapter)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Gibt den Kapitelindex im aktuellen Titel als ganze Zahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Wenn das Ende des angegebenen Kapitels erreicht ist, setzt diese Methode die Wiedergabe nachfolgender Kapitel fort, sofern vorhanden. Wenn Sie nur ein bestimmtes Kapitel wiedergeben möchten, verwenden Sie [**PlayChaptersAutoStop**](playchaptersautostop-method.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PlayChapterInTitle**](playchapterintitle-method.md)
</dt> </dl>

 

 



