---
description: Die productstate-Eigenschaft ist eine schreibgeschützte Eigenschaft, die die Installations Zustandsinformationen für ein Produkt zurückgibt.
ms.assetid: 9ae3bc86-aa13-41b3-b058-4037607f7dd5
title: Installer. productstate-Eigenschaften Methode
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
ms.openlocfilehash: cdd1397def1cd25405d0a80a6d5cfde2ee6ef77e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368576"
---
# <a name="installerproductstate-property-method"></a>Installer. productstate-Eigenschaften Methode

Die **productstate-Eigenschaft** ist eine schreibgeschützte Eigenschaft, die die Installations Zustandsinformationen für ein Produkt zurückgibt.

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

## <a name="remarks"></a>Bemerkungen

Gibt einen der in der folgenden Tabelle aufgeführten Werte zurück.



| Installationsstatus        | BESCHREIBUNG                                      |
|---------------------------|--------------------------------------------------|
| msiinstallstatemissing     | Das Produkt wird für einen anderen Benutzer installiert.   |
| msiinstallstatedefault    | Das Produkt ist für den aktuellen Benutzer installiert.   |
| msiinstallstateangekündigten | Das Produkt wird angekündigt, aber nicht installiert.     |
| msiinstallstatueingevalidarg | An die Funktion wurde ein ungültiger Parameter übergeben. |
| msiinstallstateunknown    | Das Produkt ist weder angekündigt noch installiert. |
| msiinstallstatebadconfig  | Die Konfigurationsdaten sind beschädigt.               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msiqueryproductstate**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




