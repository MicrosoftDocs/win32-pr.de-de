---
description: Mit der Methode "toourceimage" des Merge-Objekts kann der Client nach einer Zusammenführung die Dateien aus einem Modul in ein Quell Abbild auf dem Datenträger extrahieren, wobei Änderungen an dem Modul berücksichtigt werden, die möglicherweise während der Modulkonfiguration vorgenommen wurden.
ms.assetid: c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9
title: Merge. kreatesourceimage-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CreateSourceImage
- IMsmMerge.CreateSourceImage
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: e8d9365a69ff6f33c2989e9102bac7c9c22166aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359358"
---
# <a name="mergecreatesourceimage-method"></a>Merge. kreatesourceimage-Methode

Mit der Methode " **toourceimage** " des [**Merge**](merge-object.md) -Objekts kann der Client nach einer Zusammenführung die Dateien aus einem Modul in ein Quell Abbild auf dem Datenträger extrahieren, wobei Änderungen an dem Modul berücksichtigt werden, die möglicherweise während der Modulkonfiguration vorgenommen wurden. Die Liste der zu extrahierenden Dateien wird während des Mergeprozesses aus der Dateitabelle des Moduls entnommen. Die Liste der Dateien besteht aus jeder Datei, die erfolgreich aus der Dateitabelle des Moduls in die Zieldatenbank kopiert wurde. Datei Tabelleneinträge, die aufgrund von Primärschlüssel Konflikten mit vorhandenen Zeilen in der Datenbank nicht kopiert wurden, sind nicht Teil dieser Liste. Zum Zeitpunkt des Erstellens des Bilds stammt das Verzeichnis für jede dieser Dateien aus der geöffneten Datenbank (postmerge). Der im *path* -Parameter angegebene Pfad ist der Stamm des Quell Bilds für die Installation. *flongfileames* bestimmt, ob lange Dateinamen sowohl für Pfadsegmente als auch für endgültige Dateinamen verwendet werden. Die Funktion schlägt fehl, wenn keine Datenbank geöffnet ist, kein Modul geöffnet ist oder kein Merge ausgeführt wurde.

## <a name="syntax"></a>Syntax


```JScript
Merge.CreateSourceImage(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfad* 
</dt> <dd>

Der Pfad des Stamms des Quell Bilds für die Installation.

</dd> <dt>

*flongfile Ames* 
</dt> <dd>

*flongfileames* bestimmt, ob lange Dateinamen sowohl für Pfadsegmente als auch für endgültige Dateinamen verwendet werden.

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

Siehe " [**kreatesourceimage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) "-Funktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




