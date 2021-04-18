---
description: Die getdvdtextnumofstrings-Methode ruft die Anzahl von Text Zeichenfolgen ab, die für die angegebene Sprache verfügbar sind.
ms.assetid: 84d2b5b7-b474-48a4-9058-ea9da8109398
title: Getdvdtextnummeriofstrings-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c9c4fadfd28d6cddc8b9013a6e426aebe9f816
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341110"
---
# <a name="getdvdtextnumberofstrings-method"></a>Getdvdtextnummeriofstrings-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `GetDVDTextNumberOfStrings` Methode ruft die Anzahl von Text Zeichenfolgen ab, die für die angegebene Sprache verfügbar sind.

``` syntax
[ iStrings = ] MSWebDVD.GetDVDTextNumberOfStrings(iLangIndex)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*ilangindex*
</dt> <dd>

Gibt die Sprache als Ganzzahl an. Der Wert muss zwischen 0 (null) und einem Wert liegen, der kleiner als der von [**getdvdtextnumoflanguages**](getdvdtextnumberoflanguages-method.md)zurückgegebene Wert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der angibt, wie viele Zeichen folgen die Diskette in der angegebenen Sprache enthält.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mswebdvd-Objekt](mswebdvd-object.md)
</dt> </dl>

 

 



