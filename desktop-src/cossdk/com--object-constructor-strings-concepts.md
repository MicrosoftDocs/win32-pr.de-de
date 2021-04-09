---
description: Com+-objektkonstruktorzeichenfolgen sind Initialisierungs Zeichenfolgen, die für eine Komponente administrativ angegeben werden.
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: Konzepte der com+-objektkonstruktorzeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32bffd35ad230efe1f22b52da10e1b4910d71da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958276"
---
# <a name="com-object-constructor-strings-concepts"></a>Konzepte der com+-objektkonstruktorzeichenfolgen

Com+-objektkonstruktorzeichenfolgen sind Initialisierungs Zeichenfolgen, die für eine Komponente administrativ angegeben werden. Sie können objektkonstruktorzeichenfolgen verwenden, um eine einzelne Komponente mit einem gewissen Grad an Generalität zu schreiben, der es Ihnen ermöglicht, später für eine bestimmte Aufgabe angepasst zu werden. Das heißt, Sie können die parametrisierte Objekt Erstellung durchführen.

Beispielsweise können Sie diese Funktion verwenden, um eine Komponente zu schreiben, die eine generische ODBC-Verbindung enthält, und später einen exakten DSN für die Komponente in administrativer Weise angeben. Wenn sich die Systemkonfiguration ändert, können Sie die Konstruktorzeichenfolge entsprechend ändern.

> [!Note]  
> Objektkonstruktorzeichenfolgen sollten nicht verwendet werden, um sicherheitsrelevante Informationen zu speichern.

 

Objektkonstruktorzeichenfolgen können in Verbindung mit dem [Objekt Pooling](com--object-pooling.md) verwendet werden, um einen höheren Grad an Granularität beim zusammenfassen und wieder verwenden von Ressourcen zu erzielen. Beispielsweise können Sie mehrere unterschiedliche Komponenten erstellen, die mit Ausnahme der Konstruktorzeichenfolgen und CLSIDs identisch sind, um unterschiedliche Pools von Objekten zu verwalten, die Verbindungen von unterschiedlichen Client Gruppen verwendet. Dies wäre nützlich, wenn Verbindungen so geöffnet werden, dass Sie an bestimmte Sicherheitsrollen gebunden werden – z. b. wenn die Verbindungen mit einer bestimmten Authentifizierung in der Datenbank geöffnet werden – wenn Sie in der Regel nicht wiederverwendbar sind.

Zu diesem Zweck können Sie eine einzelne generische Komponente schreiben, die mithilfe von [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct)auf objektkonstruktorzeichenfolgen basiert, und Sie neu kompilieren, um verschiedene anpassbare Komponenten zu erstellen, die jeweils über eine eindeutige CLSID verfügen. Anschließend können Sie jede Komponente administrativ so anpassen, dass Sie eine geeignete Verbindung mit einer Konstruktorzeichenfolge öffnet, Sie für die Zusammenstellung konfigurieren und in unterschiedlichen Pools pro CLSID verwaltet werden.

Sie können eine Konstruktorzeichenfolge angeben, wenn eine Komponente speziell zum Erkennen der von Ihnen eingegebenen Zeichenfolge geschrieben wurde. Komponenten können mithilfe von [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct)Programm gesteuert auf diese Zeichen folgen zugreifen.

Konstruktorzeichenfolgen werden zur Objekt Erstellungszeit nur übergeben, wenn die Objektkonstruktion administrativ aktiviert ist. Com+ Ruft die [**IObjectConstruct:: Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) -Methode auf, die implementiert wird. In dieser Methode können Sie auf die Konstruktorzeichenfolge mithilfe von [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring)zugreifen. Leere Zeichen folgen können gültige Einträge sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Objekt Pooling](com--object-pooling.md)
</dt> <dt>

[Angeben einer Objektkonstruktorzeichenfolge für eine Komponente](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[Verwenden einer Objektkonstruktorzeichenfolge zum Erstellen einer Komponente](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



