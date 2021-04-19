---
description: Die Methode "Accept-Parser-allevelchange" akzeptiert oder lehnt die neue temporäre Jugend Verwaltungsebene ab.
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: Akzeptparser-allevelchange-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b2e81d1d82c4ede14580ed65d88566738dac1b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346829"
---
# <a name="acceptparentallevelchange-method"></a>Akzeptparser-allevelchange-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die Methode "Accept-Parser-allevelchange" akzeptiert oder lehnt die neue temporäre Jugend Verwaltungsebene ab.

``` syntax
        MSWebDVD.AcceptParentalLevelChange(bAccept)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*baccept*
</dt> <dd>

Gibt die neue elternebene als booleschen Wert an.



| Wert | BESCHREIBUNG                               |
|-------|-------------------------------------------|
| true  | Akzeptieren Sie die neue Jugend Verwaltungsebene. |
| false | Lehnen Sie die neue Jugend Verwaltungsebene ab. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Geben Sie diese Methode als Reaktion auf eine Änderung des Änderungs Ereignisses für eine EC- \_ DVD an \_ \_ \_ , um anzugeben, ob der DVD-Navigator den Inhalt mit der neuen Jugendebene wiedergeben soll.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Erzwingen von Eltern Verwaltungsebenen](enforcing-parental-management-levels.md)
</dt> <dt>

[**Getplayerparameentalcountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**Getplayerparser**](getplayerparentallevel-method.md)
</dt> <dt>

[**Gettitleparamevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**Notifyparametriallevelchange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**Selectpartalcountry**](selectparentalcountry-method.md)
</dt> <dt>

[**Selectparser-allevel**](selectparentallevel-method.md)
</dt> </dl>

 

 



