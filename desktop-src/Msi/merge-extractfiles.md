---
description: Die ExtractFiles-Methode des Merge-Objekts extrahiert die eingebettete .cab aus einem Modul und schreibt diese Dateien dann in das Zielverzeichnis.
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: Merge.ExtractFiles-Methode (Advpub.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFiles
- IMsmMerge.ExtractFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: e56d6572526e2aecfc12dc5b2bb9a365be6d3c53b6fb1707fe197c056d05c377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926560"
---
# <a name="mergeextractfiles-method"></a>Merge.ExtractFiles-Methode

Die **ExtractFiles-Methode** des [**Merge-Objekts**](merge-object.md) extrahiert die eingebettete .cab aus einem Modul und schreibt diese Dateien dann in das Zielverzeichnis.

## <a name="syntax"></a>Syntax


```JScript
Merge.ExtractFiles(
  Path
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Path* 
</dt> <dd>

Das vollqualifizierte Zielverzeichnis.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Alle Dateien im Zielverzeichnis mit demselben Namen werden überschrieben. Der Pfad wird erstellt, wenn er noch nicht vorhanden ist.

**ExtractFiles extrahiert** Dateien immer mithilfe kurzer Dateinamen für den Pfad. Verwenden Sie die [**ExtractFilesEx-Methode,**](merge-extractfilesex.md)um lange Dateinamen für den Pfad zu verwenden.

### <a name="c"></a>C++

Siehe [**ExtractFiles-Funktion.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1.0 oder höher<br/>                                                                     |
| Header<br/>  | <dl> <dt>Advpub.h (include Mergemod.h)</dt> </dl> |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl>                  |



 

 
