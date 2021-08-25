---
description: Die MergeEx-Methode des Merge-Objekts entspricht der Merge-Funktion, außer dass sie ein zusätzliches Argument verwendet.
ms.assetid: 83b6d62b-d176-42ac-b513-d1c2e562965c
title: Merge.MergeEx-Methode (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.MergeEx
- IMsmMerge.MergeEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 7e683597d78e568e6bfec9b59241fe45f922c5346ef83f427598ad0a7c59dcac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926530"
---
# <a name="mergemergeex-method"></a>Merge.MergeEx-Methode

Die **MergeEx-Methode** des [**Merge-Objekts**](merge-object.md) entspricht der [**Merge-Funktion,**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) außer dass sie ein zusätzliches Argument verwendet. Das *pConfiguration-Argument* ist eine Schnittstelle, die vom Client implementiert wird. Das Argument kann NULL sein. Das Vorhandensein dieses Arguments gibt an, dass der Client in der Lage ist, die Konfigurationsfunktionalität zu unterstützen, aber der Client wird nicht gezwungen, Konfigurationsdaten für ein bestimmtes konfigurierbares Element bereitzustellen.

Die [**Merge-Methode**](merge-merge.md) führt eine Zusammenführung der aktuellen Datenbank und des aktuellen Moduls aus. Der Merge fügt die Komponenten im Modul an das *feature* identifizierte Feature an. Der Stamm der Verzeichnisstruktur des Moduls wird an den Von *RedirectDir* angegebenen Speicherort umgeleitet.

## <a name="syntax"></a>Syntax


```JScript
Merge.MergeEx(
  Feature,
  RedirectDir,
  pConfiguration
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

Der Schlüssel eines Eintrags in der [Verzeichnistabelle](directory-table.md) der Datenbank. Dieser Parameter kann NULL oder eine leere Zeichenfolge sein.

</dd> <dt>

*pConfiguration* 
</dt> <dd>

Das *pConfiguration-Argument* ist eine Schnittstelle, die vom Client implementiert wird. Das Argument kann NULL sein. Das Vorhandensein dieses Arguments gibt an, dass der Client in der Lage ist, die Konfigurationsfunktionalität zu unterstützen, aber der Client wird nicht gezwungen, Konfigurationsdaten für ein bestimmtes konfigurierbares Element bereitzustellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Sobald die Zusammenführung abgeschlossen ist, werden Komponenten im Modul an das Feature angefügt, das durch *Feature* identifiziert wird. Dieses Feature wird nicht erstellt und muss ein vorhandenes Feature sein. Das Modul kann mithilfe der [**Verbinden-Methode**](merge-connect.md) an zusätzliche Features angefügt werden.

An der Datenbank vorgenommene Änderungen werden nur gespeichert, wenn die [**CloseDatabase-Methode**](merge-closedatabase.md) aufgerufen wird und *bCommit* auf **TRUE** festgelegt ist.

Wenn Mergekonflikte auftreten, einschließlich Ausschlüssen, werden sie zum späteren Abrufen im Fehlerenumerator platziert, führen jedoch nicht dazu, dass die Zusammenführung fehlschlägt. Fehler können über die [**Errors-Eigenschaft**](merge-errors.md) abgerufen werden. Fehler und Informationsmeldungen werden an die aktuelle Protokolldatei gesendet.

Wenn die Zusammenführung aufgrund einer falschen Modulkonfiguration fehlschlägt, gibt die [**MergeEx-Funktion**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) E \_ FAIL zurück. Dies schließt die folgenden msmErrorType-Fehler ein: **msmErrorBadNullSubsune**, **msmErrorBadSubsuneType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem** und **msmErrorDataRequestFailed**. Diese Fehler bewirken, dass die Zusammenführung sofort beendet wird, wenn der Fehler auftritt. Das Fehlerobjekt wird dem Enumerator weiterhin hinzugefügt, wenn **MergeEx** E FAIL \_ zurückgibt. Weitere Informationen zu msmErrorType-Fehlern finden Sie unter [**get \_ Type Function (Error Object) .**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type) Alle anderen Fehler führen dazu, dass **MergeEx** S FALSE zurückgibt \_ und die Zusammenführung fortgesetzt wird.

### <a name="c"></a>C++

Weitere Informationen finden Sie unter [**MergeEx-Funktion.**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
