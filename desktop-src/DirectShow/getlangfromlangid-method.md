---
description: Die GetLangFromLangID-Methode ruft eine für Menschen lesbare Zeichenfolge ab, wenn eine primäre Sprach-ID angegeben wird.
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: GetLangFromLangID-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6041f12c82f0e659928db9f5aa02fd916d3ff9907bf3114eb40c525b8b1d8d2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756750"
---
# <a name="getlangfromlangid-method"></a>GetLangFromLangID-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `GetLangFromLangID` -Methode ruft eine für Menschen lesbare Zeichenfolge ab, wenn eine primäre Sprach-ID angegeben wird.

``` syntax
[ sLanguage = ] MSWebDVD.GetLangFromLangID(iPrimaryLangID)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*
</dt> <dd>

Gibt die primäre Sprach-ID als ganze Zahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine Zeichenfolgendarstellung der Sprache zurück, die auf der Benutzeroberfläche der Anwendung angezeigt werden kann.

## <a name="remarks"></a>Hinweise

Obwohl diese Methode den Namen `GetLangFromLangID` hat, ist der übergebene Parameter tatsächlich die primäre Sprach-ID, nicht die Sprach-ID.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> <dt>

[**GetDVDTextLanguageLCID**](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



