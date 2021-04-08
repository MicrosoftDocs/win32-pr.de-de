---
title: Suchen mit OLE DB
description: Für Automatisierungs Clients, die ActiveX Data Objects (ADO) und alle nicht-Automatisierungs Clients verwenden, liefert ADSI einen OLE DB-Anbieter, der eine Teilmenge von OLE DB Abfrageschnittstellen unterstützt.
ms.assetid: f4e48b60-82dd-4c39-879b-0bc8f40747d2
ms.tgt_platform: multiple
keywords:
- Suchen mit OLE DB ADSI
- fragt ADSI ab und sucht mit OLE DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b6b0c056a63174233271b9b059ebffa9d4d841
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730321"
---
# <a name="searching-with-ole-db"></a>Suchen mit OLE DB

Für Automatisierungs Clients, die ActiveX Data Objects (ADO) und alle nicht-Automatisierungs Clients verwenden, liefert ADSI einen OLE DB-Anbieter, der eine Teilmenge von OLE DB Abfrageschnittstellen unterstützt. Client Code, der bereits OLE DB-Schnittstellen für Abfragen verwendet, kann die gleichen Schnittstellen verwenden, um Verzeichnisdienste abzufragen.

Unter der OLE DB-Implementierung wird ein Verzeichnisdienst als Datenquellen Objekt verfügbar gemacht. Datenquellen Objekte sind Factorys für Sitzungs Objekte und unterstützen [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) zum Herstellen einer Verbindung mit dem Verzeichnis, [idbkreatesession](/previous-versions/windows/desktop/ms724076(v=vs.85)) zum Erstellen des Sitzungs Objekts, [IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85)) zum Bereitstellen von Authentifizierungsdaten für den zugrunde liegenden Namespace und Bereitstellen des Abfrage Befehls und des [**ipersistent**](/windows/win32/api/objidl/nn-objidl-ipersist) zum Speichern der zum Erstellen des Datenquellen Objekts im zugrunde liegenden Verzeichnisdienst erforderlichen Daten.

**So führen Sie eine Active Directory Abfrage mithilfe von aus OLE DB**

1.  Rufen Sie die [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) -Schnittstelle vom OLE DB-Anbieter ab. Verwenden Sie im Fall von Active Directory den Klassen Bezeichner **CLSID \_ ADSDSOObject**.
2.  Erstellen eines [DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) -Arrays mit Verbindungsdaten, die den Benutzernamen und das Kennwort angeben.
3.  Abfragen der [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) -Schnittstelle, die in Schritt 1 für die [IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85)) -Schnittstelle abgerufen wurde.
4.  Nennen Sie die [IDBProperties:: SetProperties](/previous-versions/windows/desktop/ms723049(v=vs.85)) -Methode, und übergeben Sie das in Schritt 2 erstellte [DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) -Array.
5.  Wenden Sie die [IDBInitialize:: Initialize](/previous-versions/windows/desktop/ms718026(v=vs.85)) -Methode an, um die Verbindung mit dem OLE DB-Anbieter herzustellen. Dabei handelt es sich um den Active Directory Anbieter, in diesem Fall.
6.  Fragen Sie die [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) -Schnittstelle für die [idbkreatesession](/previous-versions/windows/desktop/ms724076(v=vs.85)) -Schnittstelle ab.
7.  Aufrufen der [idbkreatesession:: | atesession](/previous-versions/windows/desktop/ms714942(v=vs.85)) -Methode, die eine neue Schnittstelle des Typs [idbkreatecommand](/previous-versions/windows/desktop/ms711625(v=vs.85))anfordert.
8.  Rufen Sie die [idbkreatecommand:: kreatecommand](/previous-versions/windows/desktop/ms709772(v=vs.85)) -Methode auf, um eine [ICommandText](/previous-versions/windows/desktop/ms714914(v=vs.85)) -Schnittstelle zu erstellen.
9.  Aufrufen der [ICommandText:: SetCommandText](/previous-versions/windows/desktop/ms709757(v=vs.85)) -Methode. Übergeben Sie den bevorzugten Dialekt und den eigentlichen Abfrage Befehls Text in diesem Dialekt. **DBGUID \_ ldapdialekt** oder **DBGUID \_ dbsql** kann als Dialekt verwendet werden.
10. [Callicommand:: Execute](/previous-versions/windows/desktop/ms718095(v=vs.85)); eine [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) -Schnittstelle wird zurückgegeben, die die Schnittstelle zum Resultset ist.
11. Fragen Sie die [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) -Schnittstelle für die [IColumnsInfo](/previous-versions/windows/desktop/ms725401(v=vs.85)) -Schnittstelle ab.
12. Rufen Sie die [IColumnsInfo:: GetColumnInfo](/previous-versions/windows/desktop/ms722704(v=vs.85)) -Methode auf, um Spaltendaten zum Resultset abzurufen.
13. Auffüllen eines Arrays von [DBBINDING](/previous-versions/windows/desktop/ms716845(v=vs.85)) -Strukturen, das dem OLE DB-Anbieter beschreibt, wie die Datentypen pro Spalte für den Anwendungscode verfügbar gemacht werden. In diesem Schritt können Sie angeben, welcher Typ in einer bestimmten Spalte enthalten ist. Außerdem werden die Offsets der Spalten relativ zur zurückgegebenen Zeile für spaltenweise festgelegt.
14. Fragen Sie die [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) -Schnittstelle für die [IAccessor](/previous-versions/windows/desktop/ms719672(v=vs.85)) -Schnittstelle ab.
15. Aufrufen der [IAccessor:: deateaccessor](/previous-versions/windows/desktop/ms720969(v=vs.85)) -Methode, die ein Array von Accessorhandles zurückgibt. Dieses Array wird dann verwendet, um auf die Zeilen des Resultsets zuzugreifen.
16. Wenden Sie [IRowset:: GetNextRows](/previous-versions/windows/desktop/ms709827(v=vs.85)) an, und übergeben Sie die Zeilen Handles und die Anzahl der abzurufenden Zeilen.
17. Aufrufen von [IRowset:: GetData](/previous-versions/windows/desktop/ms716988(v=vs.85)) , das ein Zeilen handle übergibt, aus dem in Schritt 16 zurückgegebenen Satz. Ein Rohdaten Zeiger auf die Zeile wird zurückgegeben.

Weitere Informationen zur Suchfilter Syntax finden Sie unter [Syntax für Suchfilter](search-filter-syntax.md).

Um die zurückgegebenen Daten der nicht verarbeiteten Zeilen zu lesen, verwenden Sie die in Schritt 13 erstellte [DBBINDING](/previous-versions/windows/desktop/ms716845(v=vs.85)) -Struktur, um die Spalten Offsets in dem nicht verarbeiteten Datenzeiger zu berechnen, der in Schritt 17 zurückgegeben wurde. Lesen Sie den Status Teil der Spalte, um ein Abruf Ergebnis für diese Spalte zu erhalten.

Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie Active Directory mithilfe des ADSI OLE DB-Anbieters suchen, finden Sie unter [Beispielcode für die Verwendung OLE DB zum Durchsuchen von Active Directory](example-code-for-using-ole-db-to-search-active-directory.md).

 

 