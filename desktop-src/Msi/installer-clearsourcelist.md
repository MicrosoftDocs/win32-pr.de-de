---
description: Die ClearSourceList-Methode des Installer-Objekts entfernt alle Netzwerkquellen aus der Quellliste.
ms.assetid: a4e4beb2-a4d7-48e7-9c8d-dd1ae19fe92a
title: Installer.ClearSourceList-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClearSourceList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f16cc37556d217a217b814b5ce87cb705cd3105d4a8c2ad3f503d617aeda2cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633038"
---
# <a name="installerclearsourcelist-method"></a>Installer.ClearSourceList-Methode

Die **ClearSourceList-Methode** des [**Installer-Objekts**](installer-object.md) entfernt alle Netzwerkquellen aus der Quellliste.

## <a name="syntax"></a>Syntax


```JScript
Installer.ClearSourceList(
  Product,
  User
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Produkt* 
</dt> <dd>

Gibt den Produktcode an.

</dd> <dt>

*Benutzer* 
</dt> <dd>

Benutzername für die Installation pro Benutzer; NULL oder eine leere Zeichenfolge für die Installation pro Computer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**MsiSourceListClearAll**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)
</dt> <dt>

[Quellresilienz](source-resiliency.md)
</dt> </dl>

 

 




