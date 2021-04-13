---
title: Eigenschaften und Eigenschaften Sätze
description: Während die Arten von Lauf Zeiteigenschaften, die Automation-und Microsoft ActiveX-Steuerelemente bieten, wichtig sind, werden Sie nicht direkt darauf achten, Informationen mit Objekten zu speichern, die permanent im Dateisystem gespeichert sind.
ms.assetid: 350cfb84-2f8e-46e7-a70d-09beb14a8eee
keywords:
- Strukturierte Speicherung, Grundlagen, Eigenschaften und Eigenschafts Sätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fdafcbef0e92479aa628ab119b6d961abb74d82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388801"
---
# <a name="properties-and-property-sets"></a>Eigenschaften und Eigenschaften Sätze

Während die Arten von Lauf Zeiteigenschaften, die Automation-und Microsoft ActiveX-Steuerelemente bieten, wichtig sind, werden Sie nicht direkt darauf achten, Informationen mit Objekten zu speichern, die permanent im Dateisystem gespeichert sind. Diese Entitäten können Dateien (strukturiert, Verbund usw.), Verzeichnisse und Zusammenfassungs Kataloge enthalten. COM bietet sowohl ein serialisiertes Standardformat für diese permanenten Eigenschaften als auch einen Satz von Schnittstellen und Funktionen, mit denen Sie die Eigenschaften Sätze und deren Eigenschaften erstellen und bearbeiten können.

Persistente Eigenschaften werden als Sätze gespeichert, und mindestens ein Satz kann einer Dateisystem Entität zugeordnet werden. Diese persistenten Eigenschaften Sätze sollen zum Speichern von Daten verwendet werden, die für die Darstellung als Auflistung differenzierter Werte geeignet sind. Sie sind nicht für die Verwendung als große Daten Bank Basis vorgesehen. Sie können verwendet werden, um zusammenfassende Informationen zu einem Objekt auf dem System zu speichern, auf das von jedem anderen Objekt zugegriffen werden kann, das die Interpretation dieses Eigenschaften Satzes versteht.

Frühere Versionen von com haben in Bezug auf Eigenschaften und deren Verwendung sehr wenig angegeben, aber es wurde ein serialisiertes Format definiert, das Entwicklern das Speichern von Eigenschaften und Eigenschafts Sätzen in einer [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Instanz ermöglichte. Die Eigenschaften Bezeichner und die Semantik eines einzelnen Eigenschaften Satzes, die für Zusammenfassungs Informationen zu einem Dokument verwendet werden, wurden ebenfalls definiert. Zu diesem Zeitpunkt war es erforderlich, diese Struktur direkt als Datenstrom zu erstellen und zu bearbeiten. Siehe [strukturiertes Eigenschaften Satz Format für strukturierte Speicherung](structured-storage-serialized-property-set-format.md).

Nun definiert com jedoch zwei primäre Schnittstellen für die Verwaltung von Eigenschaften Sätzen:

-   [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
-   [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

Es ist nicht mehr erforderlich, direkt mit dem serialisierten Format umzugehen, wenn diese Schnittstellen für ein Objekt implementiert werden, das die [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle unterstützt (z. b. Verbund Dateien). Durch das Schreiben von Eigenschaften über [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) und [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) werden Daten erstellt, die exakt dem com-Eigenschaften Satz Format entsprechen, wie durch **IStorage** -Methoden angezeigt. Umgekehrt ist auch true – Eigenschaften, die mithilfe von **IStorage** in das com-Eigenschaften Satz Format geschrieben werden, sind über **IPropertySetStorage** und **IPropertyStorage** sichtbar (Sie können jedoch nicht erwarten, dass Sie in [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) schreiben und die Eigenschaften über **IPropertyStorage** sofort verfügbar oder umgekehrt).

Die [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle definiert Methoden, mit denen Eigenschafts Sätze erstellt und verwaltet werden. Die [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle bearbeitet die Eigenschaften innerhalb eines Eigenschaften Satzes direkt. Durch Aufrufen der Methoden dieser Schnittstellen kann ein Anwendungsentwickler alle Eigenschaften Sätze verwalten, die für eine bestimmte Dateisystem Entität geeignet sind. Die Verwendung dieser Schnittstellen bietet eine optimierte Lese-und Schreib Implementierung für Eigenschaften, anstatt eine Implementierung in jeder Anwendung zu haben, bei der Leistungsengpässe wie das unaufhörliches suchen auftreten können. Sie können die Schnittstellen implementieren, um die Leistung zu verbessern, sodass Eigenschaften schneller gelesen und geschrieben werden können, z. b. ein effizienteres Zwischenspeichern. Darüber hinaus ermöglichen **IPropertyStorage** und **IPropertySetStorage** das Ändern von Eigenschaften für Entitäten, die [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)nicht unterstützen, aber im Allgemeinen werden die meisten Anwendungen dies nicht tun.

Dieser Abschnitt enthält die folgenden Themen:

-   [Der Eigenschaften Satz für Zusammenfassungs Informationen](the-summary-information-property-set.md)
-   [Vordefinierte Format Bezeichner für Eigenschaften Sätze](predefined-property-set-format-identifiers.md)
-   [Die documentsummaryinformation-und UserDefined-Eigenschaften Sätze](the-documentsummaryinformation-and-userdefined-property-sets.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften Satz Implementierungen in com](property-set-implementations-in-com.md)
</dt> <dt>

[Überlegungen zu Eigenschaften Gruppen](property-set-considerations.md)
</dt> <dt>

[Verwalten von Eigenschaften](managing-properties.md)
</dt> <dt>

[Verwalten von Eigenschafts Sätzen](managing-property-sets.md)
</dt> <dt>

[Speichern von Eigenschafts Sätzen](storing-property-sets.md)
</dt> <dt>

[Leistungsmerkmale](performance-characteristics.md)
</dt> </dl>

 

 




