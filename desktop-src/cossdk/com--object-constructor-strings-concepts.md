---
description: COM+-Objektkonstruktorzeichenfolgen sind Initialisierungszeichenfolgen, die für eine Komponente administrativ angegeben werden.
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: Konzepte für COM+-Objektkonstruktorzeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9baef62780950e93043a48c2ccf13910faf7c692dc534f984ffd028e0b342dcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029520"
---
# <a name="com-object-constructor-strings-concepts"></a>Konzepte für COM+-Objektkonstruktorzeichenfolgen

COM+-Objektkonstruktorzeichenfolgen sind Initialisierungszeichenfolgen, die für eine Komponente administrativ angegeben werden. Sie können Objektkonstruktorzeichenfolgen verwenden, um eine einzelne Komponente mit einem gewissen Grad an Allgemeinkeit zu schreiben, sodass sie später für eine bestimmte Aufgabe angepasst werden kann. Das heißt, Sie können parametrisierte Objektkonstruktionen ausführen.

Beispielsweise können Sie dieses Feature verwenden, um eine Komponente zu schreiben, die eine generische ODBC-Verbindung enthält, und später einen genauen DSN für die Komponente administrativer Art angeben. Wenn sich die Systemkonfiguration ändert, können Sie die Konstruktorzeichenfolge entsprechend ändern.

> [!Note]  
> Objektkonstruktorzeichenfolgen dürfen nicht zum Speichern von sicherheitsrelevanten Informationen verwendet werden.

 

Sie können Objektkonstruktorzeichenfolgen in Verbindung mit [dem Objektpooling](com--object-pooling.md) verwenden, um ein höheres Maß an Granularität beim Poolen und Wiederverwenden von Ressourcen zu erreichen. Beispielsweise können Sie mehrere unterschiedliche Komponenten erstellen, die mit Ausnahme von Konstruktorzeichenfolgen und CLSIDs identisch sind, um unterschiedliche Pools von Objekten zu verwalten, die Verbindungen enthalten, die von unterschiedlichen Gruppen von Clients verwendet werden können. Dies wäre nützlich, wenn Verbindungen auf eine Weise geöffnet werden, die sie an bestimmte Sicherheitsrollen bindet , z. B. wenn die Verbindungen mit einer bestimmten Authentifizierung in der Datenbank geöffnet werden, sodass sie im Allgemeinen nicht wiederverwendbar werden.

Zu diesem Zweck können Sie mithilfe von [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct)eine einzelne generische Komponente schreiben, die auf Objektkonstruktorzeichenfolgen basiert, und sie neu kompilieren, um mehrere anpassbare Komponenten mit jeweils einer eindeutigen CLSID zu erstellen. Anschließend können Sie jede Komponente administrativ anpassen, um eine geeignete Verbindung mit einer Konstruktorzeichenfolge zu öffnen, sie für den Pool zu konfigurieren und sie in unterschiedlichen Pools pro CLSID zu verwalten.

Sie können eine Konstruktorzeichenfolge angeben, wenn eine Komponente speziell geschrieben wurde, um die eingegebene Zeichenfolge zu erkennen. Komponenten können programmgesteuert mithilfe von [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct)auf diese Zeichenfolgen zugreifen.

Konstruktorzeichenfolgen werden nur zum Zeitpunkt der Objekterstellung übergeben, wenn die Objekterstellung administratorisch aktiviert ist. COM+ ruft die [**IObjectConstruct::Construct-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) auf, die implementiert wird. Innerhalb dieser Methode können Sie mit [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring)auf die Konstruktorzeichenfolge zugreifen. Leere Zeichenfolgen können gültige Einträge sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Objektpooling](com--object-pooling.md)
</dt> <dt>

[Angeben einer Objektkonstruktorzeichenfolge für eine Komponente](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[Verwenden einer Objektkonstruktorzeichenfolge zum Erstellen einer Komponente](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



