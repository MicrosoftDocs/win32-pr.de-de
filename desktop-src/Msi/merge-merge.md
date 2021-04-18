---
description: Die Merge-Methode des Merge-Objekts führt einen Merge der aktuellen Datenbank und des aktuellen Moduls aus.
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: Merge. Merge-Methode (Mergemod. h)
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
ms.openlocfilehash: f33a0ba8218ae38d8fb31cefb6910f5b2c16484d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365634"
---
# <a name="mergemerge-method"></a>Merge. Merge-Methode

Die **Merge** -Methode des [**Merge**](merge-object.md) -Objekts führt einen Merge der aktuellen Datenbank und des aktuellen Moduls aus. Der Merge fügt die Komponenten im Modul an die Funktion an, die durch die *Funktion* identifiziert wird. Der Stamm der Verzeichnisstruktur des Moduls wird an den von *redirectdir* angegebenen Speicherort umgeleitet.

Die **Merge** -Methode kann nur einmal aufgerufen werden, um eine bestimmte Kombination aus MSI-und MSM-Dateien zusammenzuführen.

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

Der Name einer Funktion in der Datenbank.

</dd> <dt>

*Redirectdir* 
</dt> <dd>

Der Schlüssel eines Eintrags in der [Verzeichnis Tabelle](directory-table.md) der Datenbank. Dieser Parameter kann NULL oder eine leere Zeichenfolge sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Nachdem die Zusammenführung fertiggestellt wurde, werden die Komponenten im Modul an das von der *Funktion* identifizierte Feature angefügt. Diese Funktion wird nicht erstellt und muss ein vorhandenes Feature sein. Beachten Sie, dass die **Merge** -Methode alle Funktions Verweise im Modul abruft und die Funktionsreferenz für alle Vorkommen der NULL-GUID in der Modul Datenbank ersetzt. Weitere Informationen finden Sie unter [verweisen auf Features in Mergemodulen](referencing-features-in-merge-modules.md).

Das Modul kann mit der [**Connect**](merge-connect.md) -Methode an zusätzliche Features angefügt werden. Beachten Sie, dass durch den Aufruf der **Connect** -Methode nur Funktionskomponenten Zuordnungen erstellt werden. Die Zeilen, die bereits in der Datenbank zusammengeführt wurden, werden nicht geändert.

Änderungen, die an der Datenbank vorgenommen werden, werden nur dann gespeichert, wenn die Methode [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) aufgerufen wird und *bcommit* auf **true** festgelegt ist.

Wenn Mergekonflikte auftreten, einschließlich Ausschlüsse, werden Sie für den späteren Abruf in den Fehler Enumerator eingefügt, führen jedoch nicht zu einem Fehler bei der Zusammenführung. Fehler können mithilfe der [**Errors**](error-object.md) -Eigenschaft abgerufen werden. Fehler und Informationsmeldungen werden in der aktuellen Protokolldatei gepostet.

### <a name="c"></a>C++

Siehe [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) -Funktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
