---
description: Die FileVersion-Methode des Installer-Objekts gibt die Versionszeichenfolge oder Sprachzeichenfolge des in Path angegebenen Pfads zurück. Dabei wird das Format verwendet, in dem das Installationsprogramm erwartet, dass sie in der Datenbank zu finden sind.
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: Installer.FileVersion-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileVersion
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 492ebb0c7678b7819f3abc423517dcf77d071b81009c3b12017b1b627bb84057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630582"
---
# <a name="installerfileversion-method"></a>Installer.FileVersion-Methode

Die **FileVersion-Methode** des [**Installer-Objekts**](installer-object.md) gibt die Versionszeichenfolge oder Sprachzeichenfolge des in *Path* angegebenen Pfads zurück. Dabei wird das Format verwendet, in dem das Installationsprogramm erwartet, dass sie in der Datenbank zu finden sind. Bei Versionen ist dies eine Zeichenfolge im \# Format " . . . \# \# \# ". Für die Sprache ist dies die ID der Dezimalsprache.

## <a name="syntax"></a>Syntax


```JScript
Installer.FileVersion(
  Path,
  Language
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Path* 
</dt> <dd>

Erforderliche Zeichenfolge, die den Pfad zur Datei enthält.

</dd> <dt>

*Sprache* 
</dt> <dd>

Flag zum Angeben, ob der zurückgegebene Wert eine Sprach-ID oder Versionszeichenfolge ist. TRUE gibt die Sprache zurück, FALSE gibt die Version zurück. Dieser Parameter ist optional und hat den Standardwert FALSE.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



 

 




