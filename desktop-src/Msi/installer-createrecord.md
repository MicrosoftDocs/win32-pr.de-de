---
description: Die Methode "kreaterecord" des Installer-Objekts gibt ein neues Datensatz-Objekt mit der angeforderten Anzahl von Feldern zurück.
ms.assetid: 7f9adb28-87da-48dd-ab5c-e138b356b133
title: Installer. kreaterecord-Methode
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
ms.openlocfilehash: 8095e35a7e424a50448f1f0d948b9224bcdaa423
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365437"
---
# <a name="installercreaterecord-method"></a>Installer. kreaterecord-Methode

Die Methode " **kreaterecord** " des [**Installer**](installer-object.md) -Objekts gibt ein neues [**Datensatz**](record-object.md) -Objekt mit der angeforderten Anzahl von Feldern zurück.

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

Erforderliche Anzahl von Feldern, die möglicherweise 0 (null) ist. Die maximale Anzahl von Feldern in einem Datensatz ist auf 65535 beschränkt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Feld 0, nicht eines der Felder in *count*, wird normalerweise für Daten Satz orientierte Elemente verwendet, z. b. Format Zeichenfolgen oder Ausführungs-op-Codes.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




