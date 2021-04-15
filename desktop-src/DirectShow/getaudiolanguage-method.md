---
description: Die getaudiolanguage-Methode ruft eine Zeichenfolge ab, die angibt, welche Sprache im angegebenen Audiostream verfügbar ist.
ms.assetid: 5ff12058-eb00-4a2c-8d39-88282f68f001
title: Getaudiolanguage-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af71ad7943fe5442ded09f0b599c64c4b7215dac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520648"
---
# <a name="getaudiolanguage-method"></a>Getaudiolanguage-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `GetAudioLanguage` Methode ruft eine Zeichenfolge ab, die angibt, welche Sprache im angegebenen Audiostream verfügbar ist.

``` syntax
[ slang = ] MSWebDVD.GetAudioLanguage(iStream)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*IStream*
</dt> <dd>

Gibt die audiostreamnummer im aktuellen Titel als Ganzzahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine lesbare Zeichenfolge zurück, die die Sprache des Audiostreams im aktuellen Titel identifiziert.

 

 



