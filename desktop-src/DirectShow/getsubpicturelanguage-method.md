---
description: Die getsubpicturelanguage-Methode ruft die Sprache für den angegebenen teilbildstream ab.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: Getsubpicturelanguage-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f87d1bf95ee13a1a15e631e2bc53477b62b789a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346180"
---
# <a name="getsubpicturelanguage-method"></a>Getsubpicturelanguage-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `GetSubpictureLanguage` Methode ruft die Sprache für den angegebenen teilbildstream ab.

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*IStream*
</dt> <dd>

Gibt die Datenstrom Nummer des unter Bilds an, deren Text Sprache Sie als Ganzzahl abrufen möchten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine lesbare Zeichenfolge zurück, die die Sprache des Audiostreams im aktuellen Titel identifiziert.

 

 



