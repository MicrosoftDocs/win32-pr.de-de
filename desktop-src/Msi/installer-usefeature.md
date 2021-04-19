---
description: Die usefeature-Methode des Installer-Objekts erhöht den Verwendungs Zähler für eine bestimmte Funktion und gibt den Installationsstatus für diese Funktion zurück. Diese Methode sollte verwendet werden, um anzugeben, dass die Absicht einer Anwendung ist, eine Funktion zu verwenden.
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: Installer. usefeature-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UseFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 355e7f4e64a5cb69ffc0371473cb0db1ac6313a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362089"
---
# <a name="installerusefeature-method"></a>Installer. usefeature-Methode

Die **usefeature** -Methode des [**Installer**](installer-object.md) -Objekts erhöht den Verwendungs Zähler für eine bestimmte Funktion und gibt den Installationsstatus für diese Funktion zurück. Diese Methode sollte verwendet werden, um anzugeben, dass die Absicht einer Anwendung ist, eine Funktion zu verwenden.

## <a name="syntax"></a>Syntax


```JScript
Installer.UseFeature(
  Product,
  Feature,
  InstallMode
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Produkt* 
</dt> <dd>

Gibt den Produktcode des Produkts an.

</dd> <dt>

*Feature* 
</dt> <dd>

Identifiziert die zu verwendende Funktion.

</dd> <dt>

*InstallMode* 
</dt> <dd>

Dieser Parameter muss " *msiinstallmudenoerkennungs*" lauten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **usefeature** -Methode sollte nur für Funktionen verwendet werden, die bekanntermaßen veröffentlicht werden. Die Anwendung sollte den Status der Funktion ermitteln, indem Sie entweder die [**featurestate**](installer-featurestate.md) -Eigenschaft oder die [**Features**](installer-features.md) -Eigenschaft oder deren API-Entsprechungen aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msiusefeatureex**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 




