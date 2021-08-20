---
description: Die GetAudioLanguage-Methode ruft eine Zeichenfolge ab, die angibt, welche Sprache im angegebenen Audiostream verfügbar ist.
ms.assetid: 5ff12058-eb00-4a2c-8d39-88282f68f001
title: GetAudioLanguage-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f4842e370a11fde655ee1695e56dc148f9ebece2de01969b2603225efad7af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118000380"
---
# <a name="getaudiolanguage-method"></a>GetAudioLanguage-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `GetAudioLanguage` -Methode ruft eine Zeichenfolge ab, die angibt, welche Sprache im angegebenen Audiostream verfügbar ist.

``` syntax
[ slang = ] MSWebDVD.GetAudioLanguage(iStream)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Gibt die Audiostreamnummer im aktuellen Titel als Ganze Zahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine lesbare Zeichenfolge zurück, die die Sprache des Audiostreams im aktuellen Titel identifiziert.

 

 



