---
description: Die PlayChapterInTitle-Methode gibt das angegebene Kapitel im angegebenen Titel wieder.
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: PlayChapterInTitle-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407684ecf8db6053a4d166a4ed069f9cabf0b36f983dd04bfdf9cf85e6c8dc2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830870"
---
# <a name="playchapterintitle-method"></a>PlayChapterInTitle-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `PlayChapterInTitle` -Methode gibt das angegebene Kapitel im angegebenen Titel wieder.

``` syntax
MSWebDVD.PlayChapterInTitle(iTitle, iChapter)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Gibt den Titel als Ganzzahlwert an.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Gibt das Kapitel als Ganzzahlwert an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Diese Methode startet die Wiedergabe am angegebenen Kapitel und setzt dann die Wiedergabe auf unbestimmte Zeit fort. Wenn Sie nur ein bestimmtes Kapitel wieder geben möchten, verwenden Sie [**PlayChaptersAutoStop.**](playchaptersautostop-method.md)

 

 



