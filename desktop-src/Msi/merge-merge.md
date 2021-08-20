---
description: Die Merge-Methode des Merge-Objekts führt eine Zusammenführung der aktuellen Datenbank und des aktuellen Moduls aus.
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: Merge.Merge-Methode (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Merge
- IMsmMerge.Merge
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 43644f8ef19b81331f9f2d88d4dac03d654379d51174a50e994d3642cb86eabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804730"
---
# <a name="mergemerge-method"></a>Merge.Merge-Methode

Die **Merge-Methode** des [**Merge-Objekts**](merge-object.md) führt eine Zusammenführung der aktuellen Datenbank und des aktuellen Moduls aus. Die Zusammenführung verbindet die Komponenten im Modul mit dem feature identifizierten *Feature.* Der Stamm der Verzeichnisstruktur des Moduls wird an den Von *RedirectDir angegebenen Speicherort umgeleitet.*

Die **Merge-Methode** kann nur einmal aufgerufen werden, um eine bestimmte Kombination aus .msi msm-Dateien zusammenführungen.

## <a name="syntax"></a>Syntax


```JScript
Merge.Merge(
  Feature,
  RedirectDir
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Feature* 
</dt> <dd>

Der Name eines Features in der Datenbank.

</dd> <dt>

*RedirectDir* 
</dt> <dd>

Der Schlüssel eines Eintrags in der [Directory-Tabelle](directory-table.md) der Datenbank. Dieser Parameter kann NULL oder eine leere Zeichenfolge sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Sobald der Merge abgeschlossen ist, werden Komponenten im Modul an das Feature angefügt, das durch Feature *identifiziert wird.* Dieses Feature wird nicht erstellt und muss bereits vorhanden sein. Beachten Sie, dass die **Merge-Methode** alle Funktionsverweise im Modul ruft und den Funktionsverweis für alle Vorkommen der NULL-GUID in der Moduldatenbank ersetzt. Weitere Informationen finden Sie unter [Verweisen auf Funktionen in Mergemodule](referencing-features-in-merge-modules.md).

Das Modul kann mithilfe der -Methode an zusätzliche [**Verbinden**](merge-connect.md) angefügt werden. Beachten Sie, dass **Verbinden-Methode** nur Funktionskomponentenzuordnungen erstellt. Die Zeilen, die bereits mit der Datenbank zusammengeführt wurden, werden nicht geändert.

Änderungen an der Datenbank werden nur gespeichert, wenn die [**CloseDatabase-Methode**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) aufgerufen wird und *bCommit* auf **TRUE festgelegt ist.**

Wenn Mergekonflikte auftreten, einschließlich Ausschlüssen, werden sie zum späteren Abrufen in den Fehler-Enumerator platziert, führen jedoch nicht zu einem Fehler bei der Zusammenführung. Fehler können über die [**Errors-Eigenschaft abgerufen**](error-object.md) werden. Fehler und Informationsmeldungen werden an die aktuelle Protokolldatei gesendet.

### <a name="c"></a>C++

Weitere Informationen [**finden Sie unter Mergefunktion.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
