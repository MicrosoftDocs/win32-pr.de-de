---
description: Das Installationsprogramm stellt Funktionen bereit, die die Datensätze in einer Installations Datenbank bearbeiten. Diese Funktionen können in Verbindung mit den in Arbeiten mit Abfragen beschriebenen Funktionen verwendet werden, um tatsächliche Änderungen in einer Datenbank vorzunehmen.
ms.assetid: 5ea3fb1d-ddcb-4013-84dc-dd6f90c5751a
title: Arbeiten mit Datensätzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3252dc29bf755d08494dbdc2326bf45a4afb1c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349483"
---
# <a name="working-with-records"></a>Arbeiten mit Datensätzen

Das Installationsprogramm stellt Funktionen bereit, die die Datensätze in einer Installations Datenbank bearbeiten. Diese Funktionen können in Verbindung mit den in [Arbeiten mit Abfragen](working-with-queries.md) beschriebenen Funktionen verwendet werden, um tatsächliche Änderungen in einer Datenbank vorzunehmen.

Die folgenden Funktionen erstellen oder entfernen Datensätze:

-   Um einen neuen Datensatz für eine Datenbank zu erstellen, rufen Sie die [**msikreaterecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) -Funktion auf.
-   Wenn Sie Daten aus einem Datensatz löschen möchten, legen Sie jedes Feld durch Aufrufen der [**msirecordcleardata**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) -Funktion auf NULL fest.

Die folgenden Funktionen füllen bestimmte Felder der Datensätze aus:

-   Um einen Datensatz auf eine ganze Zahl festzulegen, müssen Sie die [**msirecordsetinteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) -Funktion aufrufen.
-   Um einen Datensatz auf eine Zeichenfolge festzulegen, müssen Sie die [**msirecordsetstring**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) -Funktion aufrufen.
-   Um eine vollständige Datei in ein Datenstrom Feld einzufügen, müssen Sie die [**msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) -Funktion aufrufen.

Die folgenden Funktionen lesen Werte aus angegebenen Feldern von Datensätzen:

-   Um einen ganzzahligen Wert aus einem Feld zu lesen, müssen Sie die [**msirecordgetinteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) -Funktion aufrufen.
-   Um einen Zeichen folgen Wert abzurufen, rufen Sie die [**msirecordgetstring**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) -Funktion auf.
-   Um einen Stream abzurufen, rufen Sie die [**msirecordlesstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) -Funktion auf.
-   Um zu ermitteln, ob ein bestimmtes Feld eines Datensatzes Null ist, müssen Sie die [**msirecordisnull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) -Funktion aufzurufen.

Die folgenden Funktionen sind Informationsdaten Satz Funktionen:

-   Um die Anzahl von Feldern zu erhalten, die ein Datensatz enthält, nennen Sie die [**msirecordgetfieldcount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) -Funktion.
-   Um die Größe eines Felds abzurufen, nennen Sie die [**msirecorddatasize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) -Funktion. Der Rückgabewert von " **msirecorddatasize** " ist für den Feldtyp sensibel.

 

 



