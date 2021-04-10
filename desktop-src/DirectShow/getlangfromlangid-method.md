---
description: Die getlangfromlangid-Methode ruft eine lesbare Zeichenfolge ab, wenn eine primäre Sprach-ID angegeben ist.
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: Getlangfromlangid-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23afddf746852028c26732eb658e786588f7e9ec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860265"
---
# <a name="getlangfromlangid-method"></a>Getlangfromlangid-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `GetLangFromLangID` -Methode ruft eine lesbare Zeichenfolge ab, wenn eine primäre Sprach-ID angegeben ist.

``` syntax
[ sLanguage = ] MSWebDVD.GetLangFromLangID(iPrimaryLangID)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iprimarylangid*
</dt> <dd>

Gibt die primäre Sprach-ID als ganze Zahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine Zeichen folgen Darstellung der Sprache zurück, die in der Benutzeroberfläche der Anwendung angezeigt werden kann.

## <a name="remarks"></a>Bemerkungen

Obwohl diese Methode den Namen `GetLangFromLangID` hat, ist der Parameter, den Sie übergeben, tatsächlich die primäre Sprachen-ID, nicht die Sprachen-ID.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getaudiolanguage**](getaudiolanguage-method.md)
</dt> <dt>

[**Getdvdtextlanguagelcid**](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



