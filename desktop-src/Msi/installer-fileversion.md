---
description: Die fileversion-Methode des Installer-Objekts gibt die Versions Zeichenfolge oder die sprach Zeichenfolge des Pfads zurück, der im Pfad unter Verwendung des Formats angegeben ist, in dem das Installationsprogramm diese in der Datenbank finden soll
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: Installer. FileVersion-Methode
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
ms.openlocfilehash: a36a92b42815a1b2df913ba6bd9f687cdd1b609b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370519"
---
# <a name="installerfileversion-method"></a>Installer. FileVersion-Methode

Die **fileversion** -Methode des [**Installer**](installer-object.md) -Objekts gibt die Versions Zeichenfolge oder die sprach Zeichenfolge des Pfads zurück, der im *Pfad* unter Verwendung des Formats angegeben ist, in dem das Installationsprogramm diese in der Datenbank finden soll Bei Versionen ist dies eine Zeichenfolge im \# Format ". \# . \# . \# ". In der Sprache ist dies die dezimale Sprach-ID.

## <a name="syntax"></a>Syntax


```JScript
Installer.FileVersion(
  Path,
  Language
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfad* 
</dt> <dd>

Erforderliche Zeichenfolge, die den Pfad zur Datei enthält.

</dd> <dt>

*Sprache* 
</dt> <dd>

Flag zum Festlegen, ob der zurückgegebene Wert eine Sprach-ID oder eine Versions Zeichenfolge ist. TRUE gibt die Sprache zurück, false gibt die Version zurück. Dieser Parameter ist optional, und der Standardwert ist false.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




