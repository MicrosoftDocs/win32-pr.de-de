---
description: Die getdvdtextlanguagelcid-Methode ruft den Gebiets Schema Bezeichner (Locale Identifier, LCID) für den angegebenen Textzeichen folgen Block ab.
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: Getdvdtextlanguagelcid-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66d21b9870982b605d9deeb1e22882a525c5616
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520632"
---
# <a name="getdvdtextlanguagelcid-method"></a>Getdvdtextlanguagelcid-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `GetDVDTextLanguageLCID` Methode ruft den Gebiets Schema Bezeichner (Locale Identifier, LCID) für den angegebenen Textzeichen folgen Block ab.

``` syntax
[ iLCID = ] MSWebDVD.GetDVDTextLanguageLCID(iLangIndex)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*ilangindex*
</dt> <dd>

Gibt den Text Sprach Block auf der Festplatte als Ganzzahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen LCID-Wert zurück, der Informationen zur Angabe der Sprache enthält, in der die Zeichen folgen geschrieben werden.

## <a name="remarks"></a>Bemerkungen

Ergänzende Text Zeichenfolgen werden in zusammenhängenden Blöcken auf der Festplatte gespeichert. Jede Sprache verfügt über einen Block von Zeichen folgen. Eine Anwendung gibt diese Blöcke durch einen Index an, der kleiner als der von [**getdvdtextnumoflanguages**](getdvdtextnumberoflanguages-method.md)zurückgegebene Wert sein muss.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mswebdvd-Objekt](mswebdvd-object.md)
</dt> <dt>

[**Getlangfromlangid**](getlangfromlangid-method.md)
</dt> </dl>

 

 



