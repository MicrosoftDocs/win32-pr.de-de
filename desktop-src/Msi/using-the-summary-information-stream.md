---
description: In diesem Abschnitt wird beschrieben, welche Funktionen in der Windows Installer-API die Eigenschaften des Zusammenfassungsinformationsstreams aufrufen können. Weitere Informationen zum Zusammenfassungsinformationsstream und zur Funktionsweise mit Datenbanken finden Sie unter Informationen zum Zusammenfassungsinformationsstream.
ms.assetid: 2c22fe52-52a9-4e3f-9482-b5e41b91b3ae
title: Verwenden des Zusammenfassungsinformationsstreams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a90d6be9586ab6adc469f14fea71dc1325cb19107bd8ddc634a3d0b4463c490
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996040"
---
# <a name="using-the-summary-information-stream"></a>Verwenden des Zusammenfassungsinformationsstreams

In diesem Abschnitt wird beschrieben, welche Funktionen in der Windows Installer-API die Eigenschaften des Zusammenfassungsinformationsstreams aufrufen können. Weitere Informationen zum Zusammenfassungsinformationsstream und zur Funktionsweise mit Datenbanken finden Sie unter [Informationen zum Zusammenfassungsinformationsstream.](about-the-summary-information-stream.md)

-   Beachten Sie, dass das Installationsprogramm unterschiedliche Arten von Datenbanken enthält und einige Eigenschaften des Zusammenfassungsinformationsstreams unterschiedliche Bedeutungen für verschiedene Datenbanken haben. Weitere Informationen finden Sie unter [Zusammenfassungseigenschaftsbeschreibungen.](summary-property-descriptions.md)
-   Wenn eine Datenbank als Ausgabe einer anderen Datenbank geöffnet wird, ist der Zusammenfassungsinformationsstream der Ausgabedatenbank tatsächlich ein schreibgeschützter Spiegel der ursprünglichen Datenbank und kann daher nicht geändert werden. Darüber hinaus wird es nicht in der Datenbank beibehalten. Um die Zusammenfassungsinformationen für die Ausgabedatenbank zu erstellen oder zu ändern, muss sie geschlossen und erneut geöffnet werden.

In den folgenden Schritten wird beschrieben, wie sie die Funktionen des Zusammenfassungsinformationsstreams verwenden:

**So verwenden Sie die Eigenschaften des Zusammenfassungsinformationsstreams**

1.  Rufen Sie ein Handle für die Datenbank ab, das den Zusammenfassungsinformationsstream enthält, indem Sie die [**MsiGetSummaryInformation-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa) aufrufen.
2.  Rufen Sie die [**MsiSummaryInfoGetPropertyCount-Funktion auf,**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) um die Anzahl der vorhandenen Eigenschaften zu erhalten.
3.  Rufen Sie die [**MsiSummaryInfoGetProperty-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya) auf, um eine einzelne Zusammenfassungsinformationseigenschaft anzeigen zu können.
4.  Aufrufen der [**MsiSummaryInfoSetProperty-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya) zum Festlegen einer einzelnen Eigenschaft
5.  Rufen Sie die [**MsiSummaryInfoPersist-Funktion auf,**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist) um die Eigenschaft zusammenfassungsinformationen zu speichern.
6.  Rufen Sie die [**MsiCreateTransformSummaryInfo-Funktion auf,**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) um die Zusammenfassungsinformationen für eine vorhandene Transformation zu erstellen.

[Orca.exe](orca-exe.md) und [Msiinfo.exe](msiinfo-exe.md) Tools, die zum Bearbeiten oder Anzeigen des Zusammenfassungsinformationsstreams einer Datenbank verwendet werden können. Diese Tools sind nur in Windows [SDK-Komponenten für Windows Installer-Entwickler verfügbar.](platform-sdk-components-for-windows-installer-developers.md)

Auf den Zusammenfassungsinformationsstream kann auch mithilfe der folgenden Methoden und Eigenschaften des Windows Installer [Automation Interface zugegriffen werden.](automation-interface.md)

-   [**SummaryInfo.Property**](summaryinfo-summaryinfo.md)
-   [**SummaryInfo.PropertyCount**](summaryinfo-propertycount.md)
-   [**SummaryInfo.Persist**](summaryinfo-persist.md)
-   [**Installer.SummaryInformation**](installer-summaryinformation.md)
-   [**Database.SummaryInformation**](database-summaryinformation.md)
-   [**Database.CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md)

Die VBScript-WiSumInf.vbs wird in den Windows [SDK-Komponenten für Windows Installer-Entwickler bereitgestellt.](platform-sdk-components-for-windows-installer-developers.md) Dieses Beispielskript kann verwendet werden, um den Zusammenfassungsinformationsstream eines Pakets Windows Installer zu verwalten. Weitere Informationen zu WiSumInf.vbs finden Sie unter [Verwalten von Zusammenfassungsinformationen.](manage-summary-information.md)

 

 



