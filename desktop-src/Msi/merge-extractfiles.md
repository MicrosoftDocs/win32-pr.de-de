---
description: Die ExtractFiles-Methode des Merge-Objekts extrahiert die eingebettete CAB-Datei aus einem Modul und schreibt diese Dateien dann in das Zielverzeichnis.
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: Merge. ExtractFiles-Methode (advpub. h)
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
ms.openlocfilehash: 3869dc37b841d386891eb70940054bd78805bf94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360427"
---
# <a name="mergeextractfiles-method"></a>Merge. ExtractFiles-Methode

Die **ExtractFiles** -Methode des [**Merge**](merge-object.md) -Objekts extrahiert die eingebettete CAB-Datei aus einem Modul und schreibt diese Dateien dann in das Zielverzeichnis.

## <a name="syntax"></a>Syntax


```JScript
Merge.ExtractFiles(
  Path
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfad* 
</dt> <dd>

Das voll qualifizierte Zielverzeichnis.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Alle Dateien im Zielverzeichnis mit demselben Namen werden überschrieben. Der Pfad wird erstellt, wenn er nicht bereits vorhanden ist.

**ExtractFiles** extrahiert Dateien immer mit kurzen Dateinamen für den Pfad. Verwenden Sie die [**extractfilesex-Methode**](merge-extractfilesex.md), um lange Dateinamen für den Pfad zu verwenden.

### <a name="c"></a>C++

Siehe [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) -Funktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                                     |
| Header<br/>  | <dl> <dt>Advpub. h (Include Mergemod. h)</dt> </dl> |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl>                  |



 

 
