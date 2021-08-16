---
description: Die AddSource-Methode des Installer-Objekts fügt der Liste gültiger Netzwerkquellen in der Quellliste eine Quelle hinzu.
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: Installer.AddSource-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8c5e2b87a1fc9a660ae835d9fb1cfa465673bb6698144a9695cbfb264535a948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633164"
---
# <a name="installeraddsource-method"></a>Installer.AddSource-Methode

Die **AddSource-Methode** des [**Installer-Objekts**](installer-object.md) fügt der Liste gültiger Netzwerkquellen in der Quellliste eine Quelle hinzu.

## <a name="syntax"></a>Syntax


```JScript
Installer.AddSource(
  Product,
  User,
  Source
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

Benutzername für die Installation pro Benutzer; NULL oder leere Zeichenfolge für die Installation pro Computer.

</dd> <dt>

*Quelle* 
</dt> <dd>

Zeiger auf die Zeichenfolge, die die Quelle angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[Quellresilienz](source-resiliency.md)
</dt> </dl>

 

 




