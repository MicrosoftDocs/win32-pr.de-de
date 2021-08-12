---
description: Die CreateRecord-Methode des Installer-Objekts gibt ein neues Record-Objekt mit der angeforderten Anzahl von Feldern zurück.
ms.assetid: 7f9adb28-87da-48dd-ab5c-e138b356b133
title: Installer.CreateRecord-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: da9c6132b79706cca2135ffcea1bff09040e15a90af5b8b3b1b7175a41229dc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631911"
---
# <a name="installercreaterecord-method"></a>Installer.CreateRecord-Methode

Die **CreateRecord-Methode** des [**Installer-Objekts**](installer-object.md) gibt ein neues [**Record-Objekt**](record-object.md) mit der angeforderten Anzahl von Feldern zurück.

## <a name="syntax"></a>Syntax


```JScript
Installer.CreateRecord(
  count
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*count* 
</dt> <dd>

Erforderliche Anzahl von Feldern, die 0 sein können. Die maximale Anzahl von Feldern in einem Datensatz ist auf 65535 beschränkt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Feld 0, keins der Felder in *count,* wird normalerweise für datensatzorientierte Elemente wie Formatzeichenfolgen oder Ausführungs-Op-Codes verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



 

 




