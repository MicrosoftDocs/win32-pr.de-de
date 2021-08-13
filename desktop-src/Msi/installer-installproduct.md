---
description: Die InstallProduct-Methode des Installer-Objekts öffnet ein Installationspaket und initialisiert eine Installationssitzung.
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: Installer.InstallProduct-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.InstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1605fc0f2e955d6f0364159779ae90f8f59e9ace0f3ff14a1106f7623ab7d99d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630392"
---
# <a name="installerinstallproduct-method"></a>Installer.InstallProduct-Methode

Die **InstallProduct-Methode** des [**Installer-Objekts**](installer-object.md) öffnet ein Installationspaket und initialisiert eine Installationssitzung.

## <a name="syntax"></a>Syntax


```JScript
Installer.InstallProduct(
  packagePath,
  propertyValues
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*packagePath* 
</dt> <dd>

Erforderliche Zeichenfolge, die den Pfad zum Installationspaket enthält.

</dd> <dt>

*propertyValues* 
</dt> <dd>

Optionale Zeichenfolge, die property=value-Paare enthält, die durch Leerzeichen getrennt sind.

Um eine Administratorinstallation durchzuführen, schließen Sie ACTION=ADMIN in *propertyValues ein.* Weitere Informationen finden Sie in der [**ACTION-Eigenschaft.**](action.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um ein Produkt vollständig zu entfernen, legen Sie REMOVE=ALL in *propertyValues fest.* Weitere Informationen finden Sie unter [**REMOVE-Eigenschaft.**](remove.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



 

 




