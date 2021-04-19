---
description: Die extractfilesex-Methode des Merge-Objekts extrahiert die eingebettete CAB-Datei aus einem Modul und schreibt diese Dateien dann in das Zielverzeichnis.
ms.assetid: 8b063052-4f92-466a-9c52-bda26ed13d5c
title: Merge. extractfilesex-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFilesEx
- IMsmMerge.ExtractFilesEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: be6aa1001be0d3ecd6cbb9c4cd1d8c04b4649f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359803"
---
# <a name="mergeextractfilesex-method"></a>Merge. extractfilesex-Methode

Die **extractfilesex** -Methode des [**Merge**](merge-object.md) -Objekts extrahiert die eingebettete CAB-Datei aus einem Modul und schreibt diese Dateien dann in das Zielverzeichnis.

## <a name="syntax"></a>Syntax


```JScript
Merge.ExtractFilesEx(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfad* 
</dt> <dd>

Das voll qualifizierte Zielverzeichnis.

</dd> <dt>

*flongfile Ames* 
</dt> <dd>

Legen Sie fest, um die Verwendung von langen Dateinamen für Pfadsegmente und endgültige Dateinamen anzugeben.

</dd> <dt>

*pfilepath* 
</dt> <dd>

Dies ist eine Liste der voll qualifizierten Pfade für die Dateien, die erfolgreich extrahiert wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Alle Dateien im Zielverzeichnis mit demselben Namen werden überschrieben. Der Pfad wird erstellt, wenn er nicht bereits vorhanden ist.

### <a name="c"></a>C++

Siehe [**extractfilesex**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) -Funktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




