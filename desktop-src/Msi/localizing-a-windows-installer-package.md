---
description: Allgemeine Informationen zur Lokalisierung finden Sie unter Globalisierungs Dienste.
ms.assetid: 734961f6-de0a-4c54-9866-ade994c41c7e
title: Lokalisieren eines Windows Installer Pakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b325b211302fba632f454f30eefbcb688f30d819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129681"
---
# <a name="localizing-a-windows-installer-package"></a>Lokalisieren eines Windows Installer Pakets

Allgemeine Informationen zur Lokalisierung finden Sie unter [Globalisierungs Dienste](../intl/globalization-services.md). Zum Lokalisieren eines Windows Installer Pakets müssen die von der Benutzeroberfläche angezeigten Zeichen folgen geändert werden, und es müssen möglicherweise auch Produkt Ressourcen hinzugefügt oder geändert werden. Beispielsweise kann die Lokalisierung das Hinzufügen von internationalen DLLs und lokalisierten Dateien zum Produkt einschließen.

**So lokalisieren Sie ein Windows Installer Paket**

1.  Vorbereiten der Lokalisierung bei der Erstellung des ursprünglichen Installationspakets. Entwerfen Sie das Layout lokalisierter Dateien so, dass verschiedene Sprachversionen sicher nebeneinander vorhanden sein können, wenn Sie auf dem Computer des Benutzers installiert werden. Organisieren Sie Dateien, die eine Lokalisierung in separate Komponenten erfordern, und installieren Sie diese Dateien in separaten Verzeichnissen. Erstellen Sie eine Basis Installations Datenbank, die über eine neutrale Steuerungs Seite verfügt. Siehe [Vorbereiten eines Windows Installer Pakets für die Lokalisierung](preparing-a-windows-installer-package-for-localization.md).
2.  Legen Sie immer die Codepage der Datenbank fest, die lokalisiert wird, bevor Sie lokalisierte Daten hinzufügen. Wenn die Codepage der zu lokalisierenden Datenbank neutral ist, finden Sie weitere Informationen unter [Festlegen der Codepage einer Datenbank](setting-the-code-page-of-a-database.md). Informationen zum Bestimmen der Codepage finden Sie unter [bestimmen der Codepage einer Installations Datenbank](determining-an-installation-database-s-code-page.md).
3.  Importieren Sie eine lokalisierte [Fehler Tabelle](error-table.md) und eine [Aktions Text Tabelle](actiontext-table.md) in die-Datenbank. Weitere Informationen finden Sie unter [lokalisieren der Fehler-und Aktions Text Tabellen](localizing-the-error-and-actiontext-tables.md) für eine Liste der Sprachen, die vom Microsoft Windows Software Development Kit (SDK) unterstützt werden. Sie können diese Tabellen mithilfe von Msidb.exe oder [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)importieren.
4.  Ändern Sie die anderen lokalisierbaren Spalten in der Datenbank mithilfe eines Tabellen-Editors oder von SQL-Abfragen. Informationen zu den SQL-Zugriffs Funktionen finden Sie unter [Arbeiten mit Abfragen](working-with-queries.md). Die Themen für die Datenbanktabellen bestimmen, welche Daten Bank Spalten lokalisiert werden können. Weitere Informationen finden Sie in der Liste der Tabellen in [Datenbanktabellen](database-tables.md).
5.  Legen Sie die [**productlanguage**](productlanguage.md) -Eigenschaft in der [Eigenschaften Tabelle](property-table.md) auf die langid der Datenbank fest. Wenn Sie ein Paket als sprachneutral erstellen, legen Sie die productlanguage-Eigenschaft auf 0 fest, und verwenden Sie die Schriftart der MS Shell Dlg als Textstil für alle erstellten Dialogfelder. Da einige Schriftarten nicht alle Zeichensätze unterstützen, können Sie sicherstellen, dass der Text auf allen lokalisierten Versionen des Betriebssystems mit dieser Schriftart ordnungsgemäß angezeigt wird.
6.  Legen Sie das Sprachfeld der [**Template Summary**](template-summary.md) -Eigenschaft auf die langid der Datenbank fest.
7.  Wenn die Text Zeichenfolgen im [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) lokalisiert werden, legen Sie die [**Codepage-Zusammenfassungs**](codepage-summary.md) Eigenschaft auf die Codepage fest.
8.  Legen Sie die Eigenschaft [**ProductCode**](productcode.md) in der [Eigenschaften Tabelle](property-table.md) fest, und legen Sie den Paketcode in der [**Zusammenfassungs Eigenschaft Revisionsnummer**](revision-number-summary.md) auf einen neuen Paketcode fest. Ein lokalisiertes Produkt gilt als ein anderes Produkt. Beispielsweise werden die deutsche und die englische Version einer Anwendung als zwei verschiedene Produkte betrachtet und müssen über unterschiedliche Produktcodes verfügen.
9.  Die Lokalisierung erfordert möglicherweise das Ändern von Ressourcen, die bereits vorhanden sind, oder das Hinzufügen neuer Ressourcen wie Dateien oder Registrierungsschlüssel. Stellen Sie sicher, dass der Komponenten Code für jede vorhandene Komponente geändert wird, der eine neue Ressource hinzugefügt wurde. Andere Änderungen erfordern möglicherweise auch Änderungen am Code einer Komponente. Weitere Informationen finden Sie [unter Ändern des Komponenten Codes](changing-the-component-code.md).
10. Achten Sie darauf, die Lokalisierung und andere Änderungen an der Datenbank zu speichern, indem Sie das Paket mit dem Bearbeitungs Tool speichern oder indem Sie [**msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)aufrufen.

Weitere Informationen finden Sie unter [Beispiel für eine Lokalisierung](a-localization-example.md).

 

 
