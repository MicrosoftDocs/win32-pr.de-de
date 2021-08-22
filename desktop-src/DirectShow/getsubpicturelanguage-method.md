---
description: Die GetSubpictureLanguage-Methode ruft die Sprache für den angegebenen Unterbilddatenstrom ab.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: GetSubpictureLanguage-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdedc90789efb331b1438744a0f64a42782bf1d1e363170ce626ed023d2e542a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536930"
---
# <a name="getsubpicturelanguage-method"></a>GetSubpictureLanguage-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `GetSubpictureLanguage` -Methode ruft die Sprache für den angegebenen Unterbilddatenstrom ab.

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Gibt die Unterbilddatenstromnummer an, deren Textsprache Sie als Ganze Zahl abrufen möchten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine lesbare Zeichenfolge zurück, die die Sprache des Audiostreams im aktuellen Titel identifiziert.

 

 



