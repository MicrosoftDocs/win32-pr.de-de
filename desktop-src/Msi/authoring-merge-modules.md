---
description: Im folgenden Verfahren werden die allgemeinen Schritte zum Erstellen von Mergemodulen beschrieben.
ms.assetid: 4b3871c0-f452-4935-9ee3-78b0ac847e67
title: Erstellen von Mergemodulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ece67151872a8d065d321c6adaae660be643ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215711"
---
# <a name="authoring-merge-modules"></a>Erstellen von Mergemodulen

Im folgenden Verfahren werden die allgemeinen Schritte zum Erstellen von Mergemodulen beschrieben.

**So erstellen Sie ein neues Mergemodul**

1.  Beziehen Sie ein Software Tool, das Sie zum Bearbeiten der mergemoduldatenbank verwenden können.
2.  Abrufen einer leeren mergemoduldatenbank.
3.  Generieren Sie eine [GUID](guid.md) für das Mergemodul. Sie müssen diese GUID verwenden, wenn Sie die Primärschlüssel von Datenbanktabellen im Mergemodul erstellen.
4.  Fügen Sie der [Komponenten Tabelle](component-table.md) für jede von der Zusammenführung gelieferte Komponente einen Datensatz hinzu. Eine Komponenten Tabelle ist in jedem Mergemodul erforderlich. Beachten Sie, dass Mergemodule mit-Komponenten arbeiten und nicht mit-Funktionen. In bestimmten Fällen muss ein Datenbanktabellen Eintrag jedoch möglicherweise auf eine Funktion verweisen. Weitere Informationen finden Sie unter [verweisen auf Features in Mergemodulen](referencing-features-in-merge-modules.md).
5.  Fügen Sie dem Mergemodul eine [Verzeichnis Tabelle](directory-table.md) hinzu, die das Layout der Verzeichnisse angibt, die das Mergemodul der Zieldatenbank hinzufügt. Eine Verzeichnis Tabelle ist in jedem Mergemodul erforderlich.
6.  Importieren Sie eine leere [FeatureComponents-Tabelle](featurecomponents-table.md) in die mergemoduldatenbank. Diese leere Tabelle stellt eine Richtlinie für das Mergetool in Fällen bereit, in denen die MSI-Datei keine eigene FeatureComponents-Tabelle enthält.
7.  Sammeln Sie alle von diesem Mergemodul gelieferten Dateien, und erstellen Sie die [MergeModule.CABinet](mergemodule-cabinet.md) -CAB-Datei. Fügen Sie die CAB-Datei dem Mergemodul als Stream in der MSM-Datei hinzu.
8.  Fügen Sie der Dateitabelle einen Datensatz für jede Datei hinzu, die in MergeModule.CABinet gespeichert ist.
9.  Fügen Sie die erforderlichen Informationen hinzu, um das Mergemodul in der [ModuleSignature-Tabelle](modulesignature-table.md)zu identifizieren. Jedes Mergemodul erfordert eine ModuleSignature-Tabelle.
10. Listet die Komponenten im Mergemodul in der [modulecomponents-Tabelle](modulecomponents-table.md)auf. Jedes Mergemodul erfordert eine modulecomponents-Tabelle.
11. Fügen Sie der MSM-Datei Mergemodul-Sequenz Tabellen nur dann hinzu, wenn das Mergemodul die [*Sequenz Tabellen*](s-gly.md) der Ziel Installations Datenbank ändern muss.
12. Fügen Sie \_ dem Mergemodul eine Validierungs Tabelle hinzu. Ein Mergemodul benötigt eine \_ Validierungs Tabelle, um die Überprüfung zu übergeben.
13. Mergemodule erfordern nur in seltenen Fällen eine Benutzeroberfläche. Das Einschließen einer Benutzeroberfläche mit einem Mergemodul ist nicht empfehlenswert. In Fällen, in denen eine Benutzeroberfläche erforderlich ist, können die UI-Tabellen wie andere Tabellen in der MSI-Datei zusammengeführt werden.
14. Fügen Sie Registrierungsinformationen zu den entsprechenden Registrierungs Tabellen in der mergemoduldatenbank hinzu. Fügen Sie Registrierungsinformationen für Typbibliotheken, Klassen, Erweiterungen und Verben in die Tabellen [typelib](typelib-table.md), [Klasse](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md)oder [MIME](mime-table.md) ein. Alle anderen Registrierungsinformationen können in der [Registrierungs Tabelle](registry-table.md)angezeigt werden. Die Verwendung der Tabelle "selfreg" wird nicht empfohlen.
15. Fügen Sie die Zusammenfassungs Informationen zum [Zusammenfassungs Informationsdaten Strom für Zusammenfassungs Module](merge-module-summary-information-stream-reference.md)hinzu.
16. Führen Sie die Überprüfung für alle Mergemodule aus, bevor Sie versuchen,

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abrufen von leeren mergemoduldatenbanken](obtaining-blank-merge-module-databases.md)
</dt> <dt>

[Abrufen von mergemodulauthoring-Tools](obtaining-merge-module-authoring-tools.md)
</dt> <dt>

[Benennen von primär Schlüsseln in mergemoduldatenbanken](naming-primary-keys-in-merge-module-databases.md)
</dt> <dt>

[Erstellen von Komponenten Tabellen für Mergemodule](authoring-merge-module-component-tables.md)
</dt> <dt>

[Erstellen von mergemodulverzeichnistabellen](authoring-merge-module-directory-tables.md)
</dt> <dt>

[Erstellen von FeatureComponents-Tabellen für Mergemodule](authoring-merge-module-featurecomponents-tables.md)
</dt> <dt>

[Erstellen von MergeModule.CABinet-CAB-Dateien](generating-mergemodule-cabinet-cabinet-files.md)
</dt> <dt>

[Erstellen von Mergemodul-Datei Tabellen](authoring-merge-module-file-tables.md)
</dt> <dt>

[Erstellen von ModuleSignature-Tabellen](authoring-modulesignature-tables.md)
</dt> <dt>

[Erstellen von modulecomponents-Tabellen](authoring-modulecomponents-tables.md)
</dt> <dt>

[Erstellen von Mergemodul-Sequenz Tabellen](authoring-merge-module-sequence-tables.md)
</dt> <dt>

[Validieren von Mergemodulen](validating-merge-modules.md)
</dt> <dt>

[Erstellen von Benutzeroberflächen in Mergemodulen](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[Erstellen von Mergemodul-Registrierungs Tabellen](authoring-merge-module-registry-tables.md)
</dt> <dt>

[Erstellen von Zusammenfassungs Datenströmen für Zusammenfassungs Module](authoring-merge-module-summary-information-streams.md)
</dt> <dt>

[Zusammenfassungs Informationsdaten Strom Referenz für Zusammenfassungs Modul](merge-module-summary-information-stream-reference.md)
</dt> <dt>

Validieren von Mergemodulen
</dt> <dt>

[Verwenden von 64-Bit-Mergemodulen](using-64-bit-merge-modules.md)
</dt> </dl>

 

 



