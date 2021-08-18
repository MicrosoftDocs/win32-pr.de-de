---
description: Die ProductState-Eigenschaft ist eine schreibgeschützte Eigenschaft, die die Installationsstatusinformationen für ein Produkt zurückgibt.
ms.assetid: 9ae3bc86-aa13-41b3-b058-4037607f7dd5
title: Installer.ProductState-Eigenschaftsmethode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c19a712c4838905296026a2a0bea4c9e1abc1c49465a854692dd603734e0bd89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763620"
---
# <a name="installerproductstate-property-method"></a>Installer.ProductState-Eigenschaftsmethode

Die **ProductState-Eigenschaft** ist eine schreibgeschützte Eigenschaft, die die Installationsstatusinformationen für ein Produkt zurückgibt.

## <a name="syntax"></a>Syntax


```JScript
Installer.ProductState Property(
  Product
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Produkt* 
</dt> <dd>

Gibt den Produktcode des Produkts an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Gibt einen der in der folgenden Tabelle gezeigten Werte zurück.



| Installationsstatus        | Beschreibung                                      |
|---------------------------|--------------------------------------------------|
| msiInstallStateAbsent     | Das Produkt wird für einen anderen Benutzer installiert.   |
| msiInstallStateDefault    | Das Produkt wird für den aktuellen Benutzer installiert.   |
| msiInstallStateAdvertised | Das Produkt wird angekündigt, aber nicht installiert.     |
| msiInstallStateInvalidArg | An die Funktion wurde ein ungültiger Parameter übergeben. |
| msiInstallStateUnknown    | Das Produkt wird weder angekündigt noch installiert. |
| msiInstallStateBadConfig  | Die Konfigurationsdaten sind beschädigt.               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




