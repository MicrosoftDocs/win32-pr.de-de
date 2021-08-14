---
title: Verarbeiten der Suchergebnisse
description: Nach dem ersten Aufruf von IDirectorySearch GetFirstRow oder IDirectorySearch GetNextRow wird entweder S OK, S ADS NOMORE ROWS oder ein Fehlerergebnis \_ \_ \_ \_ zurückgegeben.
ms.assetid: 3a84f394-a256-4815-901c-eaaae3d54b75
ms.tgt_platform: multiple
keywords:
- Verarbeiten von Suchergebnissen (AD)
- Active Directory, Suchen, Verarbeiten von Suchergebnissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0a3ba7d3dac59e5d887dc7897eb6722295842f08cb4167d5292aaace0d115c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185204"
---
# <a name="processing-the-search-results"></a>Verarbeiten der Suchergebnisse

Nach dem ersten Aufruf von [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow) oder [**IDirectorySearch::GetNextRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow)wird entweder **S \_ OK**, **S ADS \_ \_ NOMORE \_ ROWS** oder ein Fehlerergebnis zurückgegeben.

Wenn der Rückgabewert **S \_ ADS \_ NOMORE \_ ROWS** ist, wurden keine objekte gefunden, die mit dem Filter übereinstimmen. Wenn ein Fehlerergebnis zurückgegeben wird, ist die Abfrage fehlgeschlagen. In beiden Fällen müssen Sie die Zeilen im Ergebnis nicht verarbeiten, da nichts zurückgegeben wurde.

Wenn **S \_ OK** zurückgegeben wird, wurde eine Zeile abgerufen. Sie können die Spalten anhand des Namens analysieren, indem [**Sie IDirectorySearch::GetColumn verwenden.**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn) Der Name ist der **lDAPDisplayName** des Attributs in der Spalte. Der Satz aller Spalten wurde durch den pAttributeNames-Parameter der [**IDirectorySearch::ExecuteSearch-Methode**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) definiert. Wenn **NULL** angegeben wurde, ist der Satz aller Spalten die Vereinigung aller Eigenschaften, die für alle zurückgegebenen Objekte gefunden wurden. Um den gesamten Satz von Spalten zu lesen, die für ein Objekt zurückgegeben werden, verwenden Sie [**IDirectorySearch::GetNextColumnName,**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextcolumnname) um jede Spalte zu iterieren, und verwenden Sie den zurückgegebenen Spaltennamen zum Aufrufen von **IDirectorySearch::GetColumn**.

Die [**IDirectorySearch::GetColumn-Methode**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn) gibt eine [**ADS SEARCH \_ \_ COLUMN-Struktur**](/windows/desktop/api/iads/ns-iads-ads_search_column) zurück, die den Attributnamen, den Typ des Attributs, die Anzahl der Werte und einen Zeiger auf ein Array von [**ADSVALUE-Strukturen**](/windows/desktop/api/iads/ns-iads-adsvalue) enthält, die die Werte enthalten. Sie können die **ADSVALUE-Strukturen in** einer Schleife durchlesen, um die Werte für die von der Spalte zurückgegebene Eigenschaft zu lesen. Sie müssen den entsprechenden Member der **ADSVALUE-Struktur** basierend auf dem [**ADSTYPE**](/windows/win32/api/iads/ne-iads-adstypeenum) lesen, der vom **dwADsType-Member** der **ADS SEARCH \_ \_ COLUMN-Struktur** (oder dem **dwType-Member** der **ADSVALUE-Struktur)** angegeben wird. Wenn **dwADsType beispielsweise** **ADSTYPE \_ INTEGER** lautet, würden Sie den **Integer-Member** jeder **ADSVALUE-Struktur** lesen.

Weitere Informationen und ein Codebeispiel finden Sie unter [Beispielcode für die Suche nach Benutzern.](example-code-for-searching-for-users.md)

 

 