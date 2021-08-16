---
description: Die OpenModule-Methode des Merge-Objekts öffnet ein Windows Installer-Mergemodul im schreibgeschützten Modus. Ein Modul muss geöffnet werden, bevor es mit einer Installationsdatenbank zusammengeführt werden kann.
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: Merge.OpenModule-Methode (Mergemod.h)
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
ms.openlocfilehash: 4659fbd2c96d883b04e653fc67c6aa3017f16135405f956bf9b4eb78101bb404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628726"
---
# <a name="mergeopenmodule-method"></a>Merge.OpenModule-Methode

Die **OpenModule-Methode** des [**Merge-Objekts**](merge-object.md) öffnet ein Windows Installer-Mergemodul im schreibgeschützten Modus. Ein Modul muss geöffnet werden, bevor es mit einer Installationsdatenbank zusammengeführt werden kann.

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

Vollqualifizierte Dateiname, der auf ein Mergemodul verweist.

</dd> <dt>

*Sprache* 
</dt> <dd>

Ein gültiger Sprachbezeichner (LANGID).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion öffnet das Mergemodul im schreibgeschützten Modus und schließt andere Programme vom Schreiben in das Mergemodul aus, bis die [**CloseModule-Methode**](merge-closemodule.md) aufgerufen wird.

Das Installationsprogramm versucht, das Modul in der *sprache* angegebenen Sprache oder einer allgemeineren Sprache zu öffnen. *Wenn* Language beispielsweise als 1033 angegeben ist, kann ein Modul mit der Standardsprache 1033, 9 oder 0 in der Standardsprache geöffnet werden. Der *Sprachwert* 9 öffnet Module mit einer Standardsprache von 9 oder 0. Wenn die Standardsprache des Moduls die angegebenen Anforderungen nicht erfüllt, wird versucht, das Modul in die angeforderte Sprache zu transformieren. Wenn dies fehlschlägt, wird das Modul in immer allgemeinere Sprachen bis hin zu sprachneutralen Sprachen transformiert. Wenn keine der Transformationen erfolgreich ist, kann das Modul nicht geöffnet werden. In diesem Fall wird der Fehlerliste vom Typ msmErrorLanguageUnsupported ein Fehler hinzugefügt. Wenn beim Transformieren des Moduls in die gewünschte Sprache ein Fehler auftritt, wird der Fehlerliste des Typs msmErrorLanguageFailed ein Fehler hinzugefügt. Weitere Informationen finden Sie in der [**Type-Eigenschaft**](error-type.md) des [**Error-Objekts.**](error-object.md) Beim Öffnen eines Mergemoduls werden alle Fehler gelöscht, die noch nicht abgerufen wurden.

### <a name="c"></a>C++

Siehe [**OpenModule-Funktion.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
