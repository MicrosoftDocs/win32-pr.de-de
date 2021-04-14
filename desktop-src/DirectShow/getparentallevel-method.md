---
description: Die dvdadm. getparameentallevel-Methode ruft die Jugend Stufe ab, die zuletzt in der Registrierung gespeichert wurde.
ms.assetid: 2aadcf41-2c65-4f3a-8ce8-0fc9aa580ad9
title: Getparameentallevel-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfa2c2193a9d02249076b2be2225fc50cd1edd5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392365"
---
# <a name="getparentallevel-method"></a>Getparameentallevel-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `DVDAdm.GetParentalLevel` Methode ruft die Jugend Stufe ab, die zuletzt in der Registrierung gespeichert wurde.

``` syntax
[ iParentalLevel = ] DVD.DVDAdm.GetParentalLevel()
```

## <a name="return-value"></a>Rückgabewert

Gibt eine ganze Zahl zwischen 1 und 8 zurück, die die standardmäßige Jugend Stufe angibt.

## <a name="remarks"></a>Bemerkungen

Die von dieser Methode abgerufenen elternebene ist nicht notwendigerweise die gleiche Ebene, die derzeit im mswebdvd-Steuerelement gespeichert ist. um die derzeit im-Steuerelement gespeicherte Ebene abzurufen, nennen Sie die [**getplayerparameentallevel**](getplayerparentallevel-method.md) -Methode. Der Wert-1 gibt an, dass die Eltern Verwaltung deaktiviert ist.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Msdvdadm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 



