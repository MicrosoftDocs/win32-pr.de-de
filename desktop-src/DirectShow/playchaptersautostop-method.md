---
description: Die playchaptersauto-Methode startet die Wiedergabe im angegebenen Kapitel im angegebenen Titel und für die angegebene Anzahl von Kapiteln.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: Playchaptersaudestoppt-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f542f890a54c755c9ea041c46f7cef3b4b7fd9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213886"
---
# <a name="playchaptersautostop-method"></a>Playchaptersaudestoppt-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `PlayChaptersAutoStop` -Methode startet die Wiedergabe im angegebenen Kapitel im angegebenen Titel und für die angegebene Anzahl von Kapiteln.

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*ititle*
</dt> <dd>

Gibt den Titel als ganzzahligen Wert an.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*ichapter*
</dt> <dd>

Gibt das Start Kapitel als ganzzahligen Wert an.

</dd> <dt>

<span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*ichaptercount*
</dt> <dd>

Gibt die Anzahl der zu Wiedergabe enden Kapitel als ganzzahligen Wert an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Wenn das letzte Kapitel wiedergegeben wurde, bewirkt diese Methode, dass eine EC-DVD-Kapitel-Ereignis Benachrichtigung für [**\_ \_ \_ Automatische Stopps**](ec-dvd-chapter-autostop.md) an die Anwendung gesendet wird.

 

 



