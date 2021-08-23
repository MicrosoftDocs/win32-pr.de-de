---
description: Die GetDVDTextLanguageLCID-Methode ruft den Locale Identifier (LCID) für den angegebenen Textzeichenfolgenblock ab.
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: GetDVDTextLanguageLCID-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c60abedc3a986bfec766cc14c2251d9bed83650ee737762a4e870af9d283a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748720"
---
# <a name="getdvdtextlanguagelcid-method"></a>GetDVDTextLanguageLCID-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `GetDVDTextLanguageLCID` -Methode ruft den Locale Identifier (LCID) für den angegebenen Textzeichenfolgenblock ab.

``` syntax
[ iLCID = ] MSWebDVD.GetDVDTextLanguageLCID(iLangIndex)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*
</dt> <dd>

Gibt den Textsprachblock auf dem Datenträger als ganze Zahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen LCID-Wert zurück, der Informationen enthält, die die Sprache angeben, in der die Zeichenfolgen geschrieben werden.

## <a name="remarks"></a>Hinweise

Zusätzliche Textzeichenfolgen werden in zusammenhängenden Blöcken auf dem Datenträger gespeichert. Jede Sprache verfügt über einen Zeichenfolgenblock. Eine Anwendung gibt diese Blöcke durch einen Index an, der kleiner als der von [**GetDVDTextNumberOfLanguages zurückgegebene Wert sein muss.**](getdvdtextnumberoflanguages-method.md)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MSWebDVD-Objekt](mswebdvd-object.md)
</dt> <dt>

[**GetLangFromLangID**](getlangfromlangid-method.md)
</dt> </dl>

 

 



