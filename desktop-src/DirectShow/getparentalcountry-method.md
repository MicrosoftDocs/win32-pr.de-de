---
description: Die DVDAdm.GetParentalCountry-Methode ruft das Land bzw. die Region der Eltern ab, das bzw. die zuletzt in der Registrierung gespeichert wurde.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: GetParentalCountry-Methode (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeeee55a3e39449c48e1af6b2674db85d5c4a964e730e5a66bb91be6dca2c393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756760"
---
# <a name="getparentalcountry-method"></a>GetParentalCountry-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DVDAdm.GetParentalCountry` -Methode ruft das Land/die Region der Eltern ab, das bzw. die zuletzt in der Registrierung gespeichert wurde.

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a>Rückgabewert

Gibt eine ganze Zahl zurück, die den in der Registrierung gespeicherten Standardcode für Land/Region angibt.

## <a name="remarks"></a>Hinweise

Das Land/die Region der Eltern, das bzw. die diese Methode abruft, entspricht nicht unbedingt dem Land/der Region, das bzw. die derzeit im MSWebDVD-Objekt gespeichert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MSDVDAdm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 




