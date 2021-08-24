---
description: Mit der CreateSourceImage-Methode des Merge-Objekts kann der Client die Dateien nach einem Merge aus einem Modul in ein Quellimage auf dem Datenträger extrahieren und dabei Änderungen am Modul berücksichtigen, die möglicherweise während der Modulkonfiguration vorgenommen wurden.
ms.assetid: c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9
title: Merge.CreateSourceImage-Methode (Mergemod.h)
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
ms.openlocfilehash: 3e50fca7adaeced7f6f2130aeb86cf1ee74db18ae505575c8ce37b1bb85a4010
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926640"
---
# <a name="mergecreatesourceimage-method"></a>Merge.CreateSourceImage-Methode

Mit der **CreateSourceImage-Methode** des [**Merge-Objekts**](merge-object.md) kann der Client die Dateien nach einem Merge aus einem Modul in ein Quellimage auf dem Datenträger extrahieren und dabei Änderungen am Modul berücksichtigen, die möglicherweise während der Modulkonfiguration vorgenommen wurden. Die Liste der zu extrahierenden Dateien wird während des Mergevorgangs aus der Dateitabelle des Moduls übernommen. Die Liste der Dateien besteht aus jeder Datei, die erfolgreich aus der Dateitabelle des Moduls in die Zieldatenbank kopiert wurde. Dateitabelleneinträge, die aufgrund von Primärschlüsselkonflikten mit vorhandenen Zeilen in der Datenbank nicht kopiert wurden, sind nicht Teil dieser Liste. Zum Zeitpunkt der Imageerstellung stammt das Verzeichnis für jede dieser Dateien aus der geöffneten Datenbank (nach dem Zusammenführen). Der im *Path-Parameter angegebene* Pfad ist der Stamm des Quellimages für die Installation. *fLongFileNames bestimmt,* ob lange Dateinamen sowohl für Pfadsegmente als auch für endgültige Dateinamen verwendet werden. Die Funktion schlägt fehl, wenn keine Datenbank geöffnet ist, kein Modul geöffnet ist oder keine Zusammenführung durchgeführt wurde.

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

*Path* 
</dt> <dd>

Der Pfad des Stamms des Quellimages für die Installation.

</dd> <dt>

*fLongFileNames* 
</dt> <dd>

*fLongFileNames bestimmt,* ob lange Dateinamen sowohl für Pfadsegmente als auch für endgültige Dateinamen verwendet werden.

</dd> <dt>

*pFilePaths* 
</dt> <dd>

Dies ist eine Liste vollqualifizierter Pfade für die Dateien, die erfolgreich extrahiert wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Alle Dateien im Zielverzeichnis mit demselben Namen werden überschrieben. Der Pfad wird erstellt, wenn er noch nicht vorhanden ist.

### <a name="c"></a>C++

Siehe [**CreateSourceImage-Funktion.**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




