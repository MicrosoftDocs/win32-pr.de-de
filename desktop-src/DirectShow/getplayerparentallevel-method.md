---
description: "\"Getplayerparameentallevel\" Ruft die im mswebdvd-Objekt festgelegte Jugend Verwaltungsebene ab."
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: Getplayerparameentallevel-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bac51e776a45e0d1fa748fc995240292474e902
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123499"
---
# <a name="getplayerparentallevel-method"></a>Getplayerparameentallevel-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Der `GetPlayerParentalLevel` Ruft die im **mswebdvd** -Objekt festgelegte Jugend Verwaltungsebene ab.

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die aktuelle Jugend Stufe im DVD-Navigator angibt, oder-1, wenn die Eltern Verwaltung deaktiviert ist.

## <a name="remarks"></a>Bemerkungen

Eine Player Anwendung ist für die Erzwingung von Eltern Steuerelementen verantwortlich. Die Jugend Stufe des Players ist ein von einer Anwendung fest gelegteter Wert, der verwendet werden kann, um die höchste Jugend Stufe anzugeben, die der aktuelle Benutzer anzeigen kann. Wenn der DVD-Navigator auf eine neue Jugend Stufe trifft, verwenden Sie diese Methode, um zu bestimmen, ob die neue Ebene größer ist als die Ebene, die von der Anwendung über [**selectparameentallevel**](selectparentallevel-method.md)festgelegt wurde.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Gettitleparamevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**Getplayerparameentalcountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**Selectpartalcountry**](selectparentalcountry-method.md)
</dt> <dt>

[**Selectparser-allevel**](selectparentallevel-method.md)
</dt> </dl>

 

 



