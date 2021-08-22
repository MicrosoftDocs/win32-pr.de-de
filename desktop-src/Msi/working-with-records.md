---
description: Das Installationsprogramm stellt Funktionen zur Verfügung, die die Datensätze in einer Installationsdatenbank bearbeiten. Diese Funktionen können in Verbindung mit den Unter Arbeiten mit Abfragen beschriebenen Funktionen verwendet werden, um tatsächliche Änderungen in einer Datenbank vorzunehmen.
ms.assetid: 5ea3fb1d-ddcb-4013-84dc-dd6f90c5751a
title: Arbeiten mit Datensätzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f83159688ec106b8e3cea3021e4352c851620d0e2f89661cee823c1439c120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498380"
---
# <a name="working-with-records"></a>Arbeiten mit Datensätzen

Das Installationsprogramm stellt Funktionen zur Verfügung, die die Datensätze in einer Installationsdatenbank bearbeiten. Diese Funktionen können in Verbindung mit den Unter Arbeiten mit Abfragen beschriebenen Funktionen verwendet werden, [um](working-with-queries.md) tatsächliche Änderungen in einer Datenbank vorzunehmen.

Die folgenden Funktionen erstellen oder entfernen Datensätze:

-   Um einen neuen Datensatz für eine Datenbank zu erstellen, rufen Sie die [**MsiCreateRecord-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) auf.
-   Um Daten aus einem Datensatz zu löschen, legen Sie jedes Feld auf NULL fest, indem Sie die [**MsiRecordClearData-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) aufrufen.

Die folgenden Funktionen füllen die angegebenen Felder von Datensätzen aus:

-   Um einen Datensatz auf eine ganze Zahl zu setzen, rufen Sie die [**MsiRecordSetInteger-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) auf.
-   Um einen Datensatz auf eine Zeichenfolge zu setzen, rufen Sie die [**MsiRecordSetString-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) auf.
-   Rufen Sie die [**MsiRecordSetStream-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) auf, um eine gesamte Datei in ein Streamfeld einfügungen.

Die folgenden Funktionen lesen Werte aus angegebenen Feldern von Datensätzen:

-   Um einen ganzzahligen Wert aus einem Feld zu lesen, rufen Sie die [**MsiRecordGetInteger-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) auf.
-   Rufen Sie zum Abrufen eines Zeichenfolgenwerts die [**MsiRecordGetString-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) auf.
-   Um einen Stream zu erhalten, rufen Sie die [**MsiRecordReadStream-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) auf.
-   Um zu bestimmen, ob ein bestimmtes Feld eines Datensatzes NULL ist, rufen Sie die [**MsiRecordIsNull-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) auf.

Die folgenden Funktionen sind Informationsdatensatzfunktionen:

-   Um die Anzahl der Felder zu erhalten, die ein Datensatz enthält, rufen Sie die [**MsiRecordGetFieldCount-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) auf.
-   Rufen Sie die [**MsiRecordDataSize-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) auf, um die Größe eines Felds zu erhalten. Der Rückgabewert von **MsiRecordDataSize** ist für den Feldtyp vertraulich.

 

 



