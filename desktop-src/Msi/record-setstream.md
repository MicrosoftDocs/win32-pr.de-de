---
description: Die SetStream-Methode des Record-Objekts kopiert den Inhalt der angegebenen Datei als Datenstromdaten in das angegebene Datensatzfeld. Streamdaten können nicht in temporäre Felder eingefügt werden.
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: Record.SetStream-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.SetStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: de443f2d6802fb74e4b0f05b90ca8d3b3f97e328991fde50ec05ff37c203943c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626970"
---
# <a name="recordsetstream-method"></a>Record.SetStream-Methode

Die **SetStream-Methode** des [**Record-Objekts**](record-object.md) kopiert den Inhalt der angegebenen Datei als Datenstromdaten in das angegebene Datensatzfeld. Streamdaten können nicht in temporäre Felder eingefügt werden.

## <a name="syntax"></a>Syntax


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Feld* 
</dt> <dd>

Erforderliche Feldnummer des Werts innerhalb des Datensatzes, 1-basiert.

</dd> <dt>

*Filepath* 
</dt> <dd>

Der Speicherort der zu kopierenden Datei. Es wird keine Übersetzung eines beliebigen Typs ausgeführt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn bei der Methode ein Fehler auftritt, können Sie erweiterte Fehlerinformationen mithilfe der [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord ist als 000C1093-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                              |



 

 




