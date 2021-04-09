---
description: Die playperiodintitleautostoppt-Methode startet die Wiedergabe zum angegebenen Zeitpunkt im angegebenen Titel bis zur angegebenen Endzeit.
ms.assetid: 0c4df76d-3991-4a6c-a8e5-5fd713eeffc2
title: Playperiodintitleautostoppt-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05899b66b7f1a11f8f5b177d311b9634a52595b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860180"
---
# <a name="playperiodintitleautostop-method"></a>Playperiodintitleautostoppt-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `PlayPeriodInTitleAutoStop` Methode startet die Wiedergabe zum angegebenen Zeitpunkt im angegebenen Titel bis zur angegebenen Endzeit.

``` syntax
MSWebDVD.PlayPeriodInTitleAutoStop(iTitle, sStartTime, sEndTime)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*ititle*
</dt> <dd>

Gibt den Titel als Ganzzahl an.

</dd> <dt>

<span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sstarttime*
</dt> <dd>

Gibt die Startzeit als Zeichenfolge im Format "hh: mm: SS: FF" an (Stunden, Minuten, Sekunden, Rahmen werden angegeben).

</dd> <dt>

<span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sendtime*
</dt> <dd>

Gibt die Endzeit als Zeichenfolge im Format "hh: mm: SS: FF" an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Playchaptersauto-Beendigung**](playchaptersautostop-method.md)
</dt> </dl>

 

 



