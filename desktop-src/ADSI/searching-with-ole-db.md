---
title: Suchen mit OLE DB
description: Sowohl für Automation-Clients, die ActiveX Data Objects (ADO) verwenden, als auch für alle Nichtautomatisierungsclients stellt ADSI einen OLE DB-Anbieter bereit, der eine Teilmenge von OLE DB Abfrageschnittstellen unterstützt.
ms.assetid: f4e48b60-82dd-4c39-879b-0bc8f40747d2
ms.tgt_platform: multiple
keywords:
- Suchen mit OLE DB ADSI
- fragt ADSI ab und sucht mit OLE DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 969dd544600bdb88b2c01b6b932f101f0b9508d7f3f54cd5e6728fd3e4dd5f6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828370"
---
# <a name="searching-with-ole-db"></a>Suchen mit OLE DB

Sowohl für Automation-Clients, die ActiveX Data Objects (ADO) verwenden, als auch für alle Nichtautomatisierungsclients stellt ADSI einen OLE DB-Anbieter bereit, der eine Teilmenge von OLE DB Abfrageschnittstellen unterstützt. Clientcode, der bereits OLE DB Schnittstellen für Abfragen verwendet, kann die gleichen Schnittstellen verwenden, um Verzeichnisdienste abzufragen.

Unter der OLE DB Implementierung wird ein Verzeichnisdienst als Datenquellenobjekt verfügbar gemacht. Datenquellenobjekte sind Factorys für Sitzungsobjekte und unterstützen [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) zum Herstellen einer Verbindung mit dem Verzeichnis, [IDBCreateSession](/previous-versions/windows/desktop/ms724076(v=vs.85)) zum Erstellen des Sitzungsobjekts, [IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85)) zum Bereitstellen von Authentifizierungsdaten für den zugrunde liegenden Namespace und Bereitstellen des Abfragebefehls und [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist) zum Speichern der Daten, die zum Erstellen des Datenquellenobjekts im zugrunde liegenden Verzeichnisdienst erforderlich sind.

**So führen Sie eine Active Directory-Abfrage mit OLE DB**

1.  Rufen Sie die [IDBInitialize-Schnittstelle](/previous-versions/windows/desktop/ms713706(v=vs.85)) vom OLE DB-Anbieter ab. Verwenden Sie im Fall von Active Directory den Klassenbezeichner **CLSID \_ ADsDSOObject**.
2.  Erstellen Sie ein [DBPROP-Array](/previous-versions/windows/desktop/ms717970(v=vs.85)) mit Verbindungsdaten unter Angabe von Benutzername und Kennwort.
3.  Fragen Sie die [IDBInitialize-Schnittstelle](/previous-versions/windows/desktop/ms713706(v=vs.85)) ab, die in Schritt 1 für die [IDBProperties-Schnittstelle](/previous-versions/windows/desktop/ms719607(v=vs.85)) abgerufen wurde.
4.  Rufen Sie die [IDBProperties::SetProperties-Methode](/previous-versions/windows/desktop/ms723049(v=vs.85)) auf, indem Sie das in Schritt 2 erstellte [DBPROP-Array](/previous-versions/windows/desktop/ms717970(v=vs.85)) übergeben.
5.  Rufen Sie die [IDBInitialize::Initialize-Methode](/previous-versions/windows/desktop/ms718026(v=vs.85)) auf, um die Verbindung mit dem OLE DB Anbieter herzustellen. In diesem Fall ist dies der Active Directory-Anbieter.
6.  Fragen Sie die [IDBInitialize-Schnittstelle](/previous-versions/windows/desktop/ms713706(v=vs.85)) nach der [IDBCreateSession-Schnittstelle](/previous-versions/windows/desktop/ms724076(v=vs.85)) ab.
7.  Rufen Sie die [IDBCreateSession::CreateSession-Methode](/previous-versions/windows/desktop/ms714942(v=vs.85)) auf, um eine neue Schnittstelle vom Typ [IDBCreateCommand](/previous-versions/windows/desktop/ms711625(v=vs.85))anzufordern.
8.  Rufen Sie die [IDBCreateCommand::CreateCommand-Methode](/previous-versions/windows/desktop/ms709772(v=vs.85)) auf, um eine [ICommandText-Schnittstelle](/previous-versions/windows/desktop/ms714914(v=vs.85)) zu erstellen.
9.  Rufen Sie die [ICommandText::SetCommandText-Methode](/previous-versions/windows/desktop/ms709757(v=vs.85)) auf. Übergeben Sie den bevorzugten Dialekt und den tatsächlichen Abfragebefehlstext in diesem Dialekt. Entweder **DBGUID \_ LDAPDialect** oder **DBGUID \_ DBSQL** kann als Dialekt verwendet werden.
10. Aufrufen [von ICommand::Execute](/previous-versions/windows/desktop/ms718095(v=vs.85)); Eine [IRowset-Schnittstelle](/previous-versions/windows/desktop/ms720986(v=vs.85)) wird zurückgegeben, bei der es sich um die Schnittstelle für das Resultset handelt.
11. Fragen Sie die [IRowset-Schnittstelle](/previous-versions/windows/desktop/ms720986(v=vs.85)) nach der [IColumnsInfo-Schnittstelle](/previous-versions/windows/desktop/ms725401(v=vs.85)) ab.
12. Rufen Sie die [IColumnsInfo::GetColumnInfo-Methode](/previous-versions/windows/desktop/ms722704(v=vs.85)) auf, um Spaltendaten zum Resultset abzurufen.
13. Füllen Sie ein Array von [DBBINDING-Strukturen](/previous-versions/windows/desktop/ms716845(v=vs.85)) auf, und beschreiben Sie dem OLE DB Anbieter, wie die Datentypen spaltenweise für den Anwendungscode verfügbar gemacht werden. Mit diesem Schritt können Sie angeben, welcher TYPE-Typ in einer bestimmten Spalte enthalten ist. Auch die Offsets der Spalten relativ zur zurückgegebenen Zeile werden hier spaltenweise festgelegt.
14. Fragen Sie die [IRowset-Schnittstelle](/previous-versions/windows/desktop/ms720986(v=vs.85)) nach der [IAccessor-Schnittstelle](/previous-versions/windows/desktop/ms719672(v=vs.85)) ab.
15. Rufen Sie die [IAccessor::CreateAccessor-Methode](/previous-versions/windows/desktop/ms720969(v=vs.85)) auf, die ein Array von Accessorhandles zurückgibt. Dieses Array wird dann verwendet, um auf die Zeilen des Resultsets zuzugreifen.
16. Rufen Sie [IRowset::GetNextRows](/previous-versions/windows/desktop/ms709827(v=vs.85)) auf, indem Sie die Zeilenhandles und die Anzahl der abzurufenden Zeilen übergeben.
17. Rufen Sie [IRowset::GetData](/previous-versions/windows/desktop/ms716988(v=vs.85)) auf, indem Sie ein Zeilenhandle aus dem in Schritt 16 zurückgegebenen Satz übergeben. Ein roher Zeiger auf die Zeile wird zurückgegeben.

Weitere Informationen zur Suchfiltersyntax finden Sie unter [Suchfiltersyntax.](search-filter-syntax.md)

Verwenden Sie zum Lesen der zurückgegebenen nicht verarbeiteten Zeilendaten die in Schritt 13 erstellte [DBBINDING-Struktur,](/previous-versions/windows/desktop/ms716845(v=vs.85)) und berechnen Sie die Spaltenoffsets im in Schritt 17 zurückgegebenen nicht verarbeiteten Datenzeiger. Lesen Sie den Statusteil der Spalte für ein Abrufergebnis für diese Spalte.

Weitere Informationen und ein Codebeispiel, das zeigt, wie Active Directory mit dem ADSI-OLE DB-Anbieter durchsucht wird, finden Sie unter [Beispielcode für die Verwendung von OLE DB zum Suchen von Active Directory.](example-code-for-using-ole-db-to-search-active-directory.md)

 

 