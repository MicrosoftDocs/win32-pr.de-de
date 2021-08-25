---
description: Die PlayChaptersAutoStop-Methode startet die Wiedergabe am angegebenen Kapitel im angegebenen Titel und für die angegebene Anzahl von Kapiteln.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: PlayChaptersAutoStop-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58c518496f81f4ca4e662bf8dbc821f2378cd38d27c7546356144910c0c5ba72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830740"
---
# <a name="playchaptersautostop-method"></a>PlayChaptersAutoStop-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `PlayChaptersAutoStop` -Methode startet die Wiedergabe am angegebenen Kapitel im angegebenen Titel und für die angegebene Anzahl von Kapiteln.

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Gibt den Titel als Ganzzahlwert an.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Gibt das Start-Kapitel als Ganzzahlwert an.

</dd> <dt>

<span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*
</dt> <dd>

Gibt die Anzahl der Kapitel an, die als Ganzzahlwert abspielt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Wenn das letzte Kapitel abgespielt wurde, bewirkt diese Methode, dass eine [**EC \_ DVD CHAPTER \_ \_ AUTOTOP-Ereignisbenachrichtigung**](ec-dvd-chapter-autostop.md) an die Anwendung gesendet wird.

 

 



