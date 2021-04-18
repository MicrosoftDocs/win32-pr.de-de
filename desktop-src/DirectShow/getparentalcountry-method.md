---
description: Die dvdadm. getsamentalcountry-Methode ruft das Eltern Land/die Region ab, das zuletzt in der Registrierung gespeichert wurde.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: Getcentalcountry-Methode (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fcee63fd3cad64498d95ca74e81a9f02804a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365560"
---
# <a name="getparentalcountry-method"></a>Getsamentalcountry-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DVDAdm.GetParentalCountry` -Methode ruft das Eltern Land/die Region ab, das zuletzt in der Registrierung gespeichert wurde.

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a>Rückgabewert

Gibt eine ganze Zahl zurück, die den in der Registrierung gespeicherten Standard Code für Land/Region angibt.

## <a name="remarks"></a>Bemerkungen

Das Land bzw. die Region, das von dieser Methode abgerufen wird, ist nicht notwendigerweise dasselbe Land/eine Region, das zurzeit im mswebdvd-Objekt gespeichert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Msdvdadm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 




