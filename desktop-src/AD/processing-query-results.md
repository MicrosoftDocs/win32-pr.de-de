---
title: Verarbeiten der Suchergebnisse
description: Nach dem ersten Aufrufen von IDirectorySearch GetFirstRow oder IDirectorySearch GetNextRow werden entweder die \_ Zeilen "OK", "s" \_ oder "Fehler" \_ \_ zurückgegeben.
ms.assetid: 3a84f394-a256-4815-901c-eaaae3d54b75
ms.tgt_platform: multiple
keywords:
- Die Suchergebnisse werden verarbeitet.
- Active Directory, suchen, Verarbeiten von Suchergebnissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 732128438162f5ee8f6fe75bb4d2ce53e0d43070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106342335"
---
# <a name="processing-the-search-results"></a>Verarbeiten der Suchergebnisse

Nach dem ersten Aufrufen von [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow) oder [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow)werden entweder die **\_ \_ \_ Zeilen**" **\_ OK**", "s" oder "Fehler" zurückgegeben.

Wenn der Rückgabewert **S \_ ADS \_ nomore- \_ Zeilen** ist, wurden keine weiteren Objekte gefunden, die mit dem Filter übereinstimmen. Wenn ein Fehler Ergebnis zurückgegeben wird, ist die Abfrage fehlgeschlagen. In beiden Fällen ist es nicht erforderlich, die Zeilen im Ergebnis zu verarbeiten, da nichts zurückgegeben wurde.

Wenn **S \_ OK** zurückgegeben wird, wurde eine Zeile abgerufen. Sie können die Spalten nach Namen mithilfe von [**idirector ysearch:: GetColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn)analysieren. Der Name ist der **ldapDisplayName** des Attributs in der Spalte. Der Satz aller Spalten wurde durch den pattributenames-Parameter der [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) -Methode definiert. Wenn **null** angegeben wurde, ist der Satz aller Spalten die Vereinigung aller Eigenschaften, die für alle zurückgegebenen Objekte gefunden wurden. Um die gesamte Gruppe von Spalten zu lesen, die für ein Objekt zurückgegeben werden, verwenden Sie [**IDirectorySearch:: getnextcolumnname**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextcolumnname) , um die einzelnen Spalten zu durchlaufen, und verwenden Sie den zurückgegebenen Spaltennamen, um **IDirectorySearch:: GetColumn** aufzurufen.

Die [**IDirectorySearch:: GetColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn) -Methode gibt eine [**ADS- \_ Such \_ Spalten**](/windows/desktop/api/iads/ns-iads-ads_search_column) Struktur zurück, die den Attributnamen, den Typ des Attributs, die Anzahl der Werte und einen Zeiger auf ein Array von [**ADSVALUE**](/windows/desktop/api/iads/ns-iads-adsvalue) -Strukturen enthält, die die Werte enthalten. Sie können die **ADSVALUE** -Strukturen durchlaufen, um die Werte für die von der Spalte zurückgegebene Eigenschaft zu lesen. Sie müssen den entsprechenden Member der **ADSVALUE** -Struktur basierend auf dem vom **dwadstype** -Member der **ADS- \_ Such \_ Spalten** Struktur angegebenen [**adstype**](/windows/win32/api/iads/ne-iads-adstypeenum) lesen (oder dem **dwType** -Member der **ADSVALUE** -Struktur). Wenn **dwadstype** beispielsweise eine **adstype- \_ Ganzzahl** ist, würden Sie das **ganzzahlige** Element jeder **ADSVALUE** -Struktur lesen.

Weitere Informationen und ein Codebeispiel finden Sie unter [Beispielcode für die Suche nach Benutzern](example-code-for-searching-for-users.md).

 

 