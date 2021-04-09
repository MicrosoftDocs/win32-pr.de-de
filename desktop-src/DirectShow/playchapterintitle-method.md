---
description: Die playchapterintitle-Methode gibt das angegebene Kapitel im angegebenen Titel wieder.
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: Playchapterintitle-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381a63c36c61a8853dcba6a587adb1f078b8cfaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859946"
---
# <a name="playchapterintitle-method"></a>Playchapterintitle-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `PlayChapterInTitle` Methode gibt das angegebene Kapitel im angegebenen Titel wieder.

``` syntax
MSWebDVD.PlayChapterInTitle(iTitle, iChapter)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*ititle*
</dt> <dd>

Gibt den Titel als ganzzahligen Wert an.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*ichapter*
</dt> <dd>

Gibt das Kapitel als ganzzahligen Wert an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Diese Methode startet die Wiedergabe im angegebenen Kapitel und wird dann unbegrenzt wiedergegeben. Wenn Sie nur ein bestimmtes Kapitel wiedergeben möchten, verwenden Sie [**playchaptersauto stoppt**](playchaptersautostop-method.md).

 

 



