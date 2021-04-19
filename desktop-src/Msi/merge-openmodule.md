---
description: Die OpenModule-Methode des Merge-Objekts öffnet ein Windows Installer Mergemodul im schreibgeschützten Modus. Ein Modul muss geöffnet werden, bevor es mit einer Installations Datenbank zusammengeführt werden kann.
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: Merge. OpenModule-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenModule
- IMsmMerge.OpenModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9d83a9331c91817f70c49ecf74c7171c5e627be6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372521"
---
# <a name="mergeopenmodule-method"></a>Merge. OpenModule-Methode

Die **OpenModule** -Methode des [**Merge**](merge-object.md) -Objekts öffnet ein Windows Installer Mergemodul im schreibgeschützten Modus. Ein Modul muss geöffnet werden, bevor es mit einer Installations Datenbank zusammengeführt werden kann.

## <a name="syntax"></a>Syntax


```JScript
Merge.OpenModule(
  FileName,
  Language
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FileName* 
</dt> <dd>

Voll qualifizierter Dateiname, der auf ein Mergemodul verweist.

</dd> <dt>

*Sprache* 
</dt> <dd>

Ein gültiger sprach Bezeichner (langid).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion öffnet das Mergemodul im schreibgeschützten Modus und schließt andere Programme vom Schreiben in das Mergemodul aus, bis die [**closemodule**](merge-closemodule.md) -Methode aufgerufen wird.

Das Installationsprogramm versucht, das Modul in der Sprache zu öffnen, die in der *Sprache* angegeben ist, oder eine allgemeinere Sprache. Wenn *Language* beispielsweise als 1033 angegeben wird, kann ein Modul mit der Standardsprache 1033, 9 oder 0 in der Standardsprache geöffnet werden. Der *sprach* Wert 9 öffnet Module mit der Standardsprache 9 oder 0. Wenn die Standardsprache des Moduls nicht den angegebenen Anforderungen entspricht, wird versucht, das Modul in die angeforderte Sprache umzuwandeln. Wenn dies nicht möglich ist, wird das Modul in immer mehr allgemeine Sprachen transformiert, und zwar bis zu sprachneutral. Wenn keine der Transformationen erfolgreich ist, kann das Modul nicht geöffnet werden. In diesem Fall wird der Fehlerliste des Typs msmerrorlanguageunsupported ein Fehler hinzugefügt. Wenn beim Transformieren des Moduls in die gewünschte Sprache ein Fehler auftritt, wird der Fehlerliste des Typs msmerrorlanguagefailed ein Fehler hinzugefügt. Weitere Informationen finden Sie unter der [**Type**](error-type.md) -Eigenschaft des [**Error**](error-object.md) -Objekts. Durch das Öffnen eines Mergemoduls werden alle Fehler gelöscht, die noch nicht abgerufen wurden.

### <a name="c"></a>C++

Siehe [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) -Funktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
