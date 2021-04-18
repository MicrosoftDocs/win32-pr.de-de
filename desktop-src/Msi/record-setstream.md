---
description: Mit der setStream-Methode des Datensatz-Objekts wird der Inhalt der angegebenen Datei als Streamdaten in das angegebene Daten Satz Feld kopiert. Streamdaten können nicht in temporäre Felder eingefügt werden.
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: Record. setStream-Methode
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
ms.openlocfilehash: 94ec3d63b3dcd75a13c2c0ff62b624b89979d641
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360961"
---
# <a name="recordsetstream-method"></a>Record. setStream-Methode

Mit der **setStream** -Methode des [**Datensatz**](record-object.md) -Objekts wird der Inhalt der angegebenen Datei als Streamdaten in das angegebene Daten Satz Feld kopiert. Streamdaten können nicht in temporäre Felder eingefügt werden.

## <a name="syntax"></a>Syntax


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flächen* 
</dt> <dd>

Erforderliche Feldnummer des Werts im Datensatz, 1-basiert.

</dd> <dt>

*FilePath* 
</dt> <dd>

Der Speicherort der zu kopierenden Datei. Es wird keine Übersetzung eines beliebigen Typs durchgeführt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iRecord ist definiert als 000c1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




