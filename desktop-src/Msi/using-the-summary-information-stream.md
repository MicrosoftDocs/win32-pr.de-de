---
description: In diesem Abschnitt wird beschrieben, welche Funktionen in der Windows Installer-API die Eigenschaften des Zusammenfassungs Informations Stroms abrufen können. Weitere Informationen zum Zusammenfassungs Informationsdaten Strom und zur Funktionsweise von Datenbanken finden Sie unter Informationen zum Datenstrom für Zusammenfassungs Informationen.
ms.assetid: 2c22fe52-52a9-4e3f-9482-b5e41b91b3ae
title: Verwenden des Zusammenfassungs Informationsdaten Stroms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de3ece9ad336b1a88d343b859fd3881b23246c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959798"
---
# <a name="using-the-summary-information-stream"></a>Verwenden des Zusammenfassungs Informationsdaten Stroms

In diesem Abschnitt wird beschrieben, welche Funktionen in der Windows Installer-API die Eigenschaften des Zusammenfassungs Informations Stroms abrufen können. Weitere Informationen zum Zusammenfassungs Informationsdaten Strom und zur Funktionsweise von Datenbanken finden Sie unter Informationen zum Daten [Strom für Zusammenfassungs Informationen](about-the-summary-information-stream.md).

-   Beachten Sie, dass das Installationsprogramm verschiedene Typen von Datenbanken enthält und einige Eigenschaften des Datenstroms für Zusammenfassungs Informationen unterschiedliche Bedeutungen mit unterschiedlichen Datenbanken aufweisen. Weitere Informationen finden Sie unter [Zusammenfassungs Eigenschafts Beschreibungen](summary-property-descriptions.md).
-   Wenn eine Datenbank als Ausgabe einer anderen Datenbank geöffnet wird, ist der Zusammenfassungs Datenstrom der Ausgabedatenbank tatsächlich eine schreibgeschützte Spiegelung der ursprünglichen Datenbank und kann daher nicht geändert werden. Außerdem wird Sie nicht in der Datenbank gespeichert. Um die zusammenfassenden Informationen für die Ausgabedatenbank zu erstellen oder zu ändern, muss sie geschlossen und erneut geöffnet werden.

In den folgenden Schritten wird die Verwendung der Datenstrom Funktionen für Zusammenfassungs Informationen beschrieben:

**So verwenden Sie die Eigenschaften des Zusammenfassungs Informations Stroms**

1.  Rufen Sie ein Handle für die Datenbank mit dem Zusammenfassungs Informationsdaten Strom ab, indem Sie die [**msigetsummaryinformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa) -Funktion aufrufen.
2.  Rufen Sie die [**msisummaryinfogetpropertycount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) -Funktion auf, um die Anzahl der vorhandenen Eigenschaften zu erhalten.
3.  Aufrufen der [**msisummaryinfogetproperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya) -Funktion, um eine einzelne Zusammenfassungs Informations Eigenschaft anzuzeigen.
4.  Aufrufen der [**msisummaryinfosetproperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya) -Funktion, um eine einzelne Eigenschaft festzulegen
5.  Um die Eigenschaft "Zusammenfassungs Informationen" zu speichern, können Sie die Funktion [**msisummaryinfopersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist) abrufen.
6.  Rufen Sie die [**msikreatetransformsummaryinfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) -Funktion auf, um die Zusammenfassungs Informationen für eine vorhandene Transformation zu erstellen.

[Orca.exe](orca-exe.md) und [Msiinfo.exe](msiinfo-exe.md) sind Tools, mit denen der Zusammenfassungs Informationsdaten Strom einer Datenbank bearbeitet oder angezeigt werden kann. Diese Tools sind nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

Auf den Zusammenfassungs Informationsdaten Strom kann auch mit den folgenden Methoden und Eigenschaften der Windows Installer [Automation-Schnittstelle](automation-interface.md)zugegriffen werden.

-   [**SummaryInfo. Property**](summaryinfo-summaryinfo.md)
-   [**SummaryInfo. PropertyCount**](summaryinfo-propertycount.md)
-   [**SummaryInfo. Persistenz**](summaryinfo-persist.md)
-   [**Installer. SummaryInformation**](installer-summaryinformation.md)
-   [**Database. SummaryInformation**](database-summaryinformation.md)
-   [**Database. kreatetransformsummaryinfo**](database-createtransformsummaryinfo.md)

Die VBScript-Datei WiSumInf.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispielskript kann verwendet werden, um den Zusammenfassungs Informationsdaten Strom eines Windows Installer Pakets zu verwalten. Weitere Informationen zu WiSumInf.vbs finden Sie unter [Verwalten von Zusammenfassungs Informationen](manage-summary-information.md).

 

 



