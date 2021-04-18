---
description: Die mergeex-Methode des Merge-Objekts entspricht der Merge-Funktion, mit der Ausnahme, dass Sie ein zusätzliches Argument annimmt.
ms.assetid: 83b6d62b-d176-42ac-b513-d1c2e562965c
title: Merge. mergeex-Methode (Mergemod. h)
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
ms.openlocfilehash: 12accfcbc87877300b803ae90d8c924802410e9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358320"
---
# <a name="mergemergeex-method"></a>Merge. mergeex-Methode

Die **mergeex** -Methode des [**Merge**](merge-object.md) -Objekts entspricht der [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) -Funktion, mit der Ausnahme, dass Sie ein zusätzliches Argument annimmt. Das *pconfiguration* -Argument ist eine vom Client implementierte Schnittstelle. Das Argument kann NULL sein. Das vorhanden sein dieses Arguments gibt an, dass der Client die Konfigurationsfunktionen unterstützen kann, aber den Client nicht zum Bereitstellen von Konfigurationsdaten für ein bestimmtes konfigurierbares Element löscht.

Die [**Merge**](merge-merge.md) -Methode führt einen Merge der aktuellen Datenbank und des aktuellen Moduls aus. Der Merge fügt die Komponenten im Modul an die Funktion an, die durch die *Funktion* identifiziert wird. Der Stamm der Verzeichnisstruktur des Moduls wird an den von *redirectdir* angegebenen Speicherort umgeleitet.

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

Der Name einer Funktion in der Datenbank.

</dd> <dt>

*Redirectdir* 
</dt> <dd>

Der Schlüssel eines Eintrags in der [Verzeichnis Tabelle](directory-table.md) der Datenbank. Dieser Parameter kann NULL oder eine leere Zeichenfolge sein.

</dd> <dt>

*pconfiguration* 
</dt> <dd>

Das *pconfiguration* -Argument ist eine vom Client implementierte Schnittstelle. Das Argument kann NULL sein. Das vorhanden sein dieses Arguments gibt an, dass der Client die Konfigurationsfunktionen unterstützen kann, aber den Client nicht zum Bereitstellen von Konfigurationsdaten für ein bestimmtes konfigurierbares Element löscht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Nachdem die Zusammenführung fertiggestellt wurde, werden die Komponenten im Modul an das von der *Funktion* identifizierte Feature angefügt. Diese Funktion wird nicht erstellt und muss ein vorhandenes Feature sein. Das Modul kann mit der [**Connect**](merge-connect.md) -Methode an zusätzliche Features angefügt werden.

Änderungen, die an der Datenbank vorgenommen werden, werden nur dann gespeichert, wenn die Methode [**CloseDatabase**](merge-closedatabase.md) aufgerufen wird und *bcommit* auf **true** festgelegt ist.

Wenn Mergekonflikte auftreten, einschließlich Ausschlüsse, werden Sie für den späteren Abruf in den Fehler Enumerator eingefügt, führen jedoch nicht zu einem Fehler bei der Zusammenführung. Fehler können mithilfe der [**Errors**](merge-errors.md) -Eigenschaft abgerufen werden. Fehler und Informationsmeldungen werden in der aktuellen Protokolldatei gepostet.

Wenn die Zusammenführung aufgrund einer falschen Modulkonfiguration fehlschlägt, gibt die [**mergeex**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) -Funktion E \_ Fail zurück. Dies schließt folgende msmerrortype-Fehler ein: **msmerrorbadnullsubstitution**, **msmerrorbadsubstitutiontype**, **msmerrorbadnullresponse**, **msmerrormissingconfigitem** und **msmerrordatarequestfailed**. Diese Fehler bewirken, dass die Zusammenführung sofort beendet wird, wenn der Fehler auftritt. Das Error-Objekt wird immer noch dem Enumerator hinzugefügt, wenn **mergeex** E Fail zurückgibt \_ . Weitere Informationen zu msmerrortype-Fehlern finden [**Sie unter Get \_ Type Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type). Alle anderen Fehler bewirken, dass **mergeex** den Wert "false" zurückgibt \_ und den Vorgang fortsetzen kann.

### <a name="c"></a>C++

Siehe [**mergeex**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) -Funktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
