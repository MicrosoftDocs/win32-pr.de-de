---
description: Die ForceSourceListResolution-Methode des Installer-Objekts zwingt den Windows Installer, die Quellliste nach einer gültigen Produktquelle zu durchsuchen.
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: Installer.ForceSourceListResolution-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ForceSourceListResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cafff03a392fc1977fd19b5b8415ca499d614c2c4ba3fb4f7104edd5344f3a86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630592"
---
# <a name="installerforcesourcelistresolution-method"></a>Installer.ForceSourceListResolution-Methode

Die **ForceSourceListResolution-Methode** des [**Installer-Objekts**](installer-object.md) zwingt das Installationsprogramm, die Quellliste nach einer gültigen Produktquelle zu durchsuchen, wenn eine Quelle das nächste Mal benötigt wird, z. B. wenn das Installationsprogramm eine Installation oder eine Neuinstallation ausführt oder wenn der Pfad für eine Komponente benötigt wird, die von der Quelle ausgeführt werden soll.

## <a name="syntax"></a>Syntax


```JScript
Installer.ForceSourceListResolution(
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

Benutzername für die Installation pro Benutzer; NULL oder leere Zeichenfolge für die Installation pro Computer.

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

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Quellresilienz](source-resiliency.md)
</dt> </dl>

 

 




