---
description: Es gibt drei Klassen, die von der COMAdmin Library (comadmin.dll) bereitgestellt werden, von denen jede eine com-Dual Schnittstelle implementiert.
ms.assetid: 5a20199f-9d46-4dbe-8e30-2c7ddbde8795
title: Zusammenfassungs Beschreibung der COMAdmin-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a2f54f21f89e9bca644006d50f4eec544565c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343596"
---
# <a name="summary-description-of-the-comadmin-classes"></a>Zusammenfassungs Beschreibung der COMAdmin-Klassen

Es gibt drei Klassen, die von der COMAdmin Library (comadmin.dll) bereitgestellt werden, von denen jede eine com-Dual Schnittstelle implementiert. Mithilfe von Objekten, die aus diesen Klassen erstellt werden, erhalten Sie Zugriff auf den Katalog, um Auflistungen im Katalog darzustellen und die in Auflistungen enthaltenen Elemente darzustellen.

## <a name="comadmincatalog"></a>Comadmincatalog

Die [**comadmincatalog**](comadmincatalog.md) -Klasse stellt den Katalog selbst dar. Ein aus **comadmincatalog** erstelltes Objekt ist das grundlegende Objekt, das Sie in der programmgesteuerten Verwaltung verwenden. Neben dem Einrichten der grundlegenden Verbindung mit dem Katalogserver, wenn Sie ihn instanziieren, stellt **comadmincatalog** Methoden bereit, mit denen Sie die folgenden Aufgaben ausführen können:

-   Sammlungen im Katalog erhalten.
-   Stellen Sie eine Verbindung mit dem Katalogserver auf einem Remote Computer her.
-   Installieren, exportieren, starten, Herunterfahren und Abrufen von Informationen zu com+-Anwendungen.
-   Installieren von Komponenten in com+-Anwendungen und Abrufen von Informationen zu Komponenten.
-   Starten, Abbrechen oder Aktualisieren von Diensten, die auf dem Computer ausgeführt werden.
-   Aktualisieren, wiederherstellen oder Sichern von Katalog Informationen.

In com+ 1,0 implementiert die [**comadmincatalog**](comadmincatalog.md) -Klasse die [**icomadmincatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) -Schnittstelle. In com+ 1,5 implementiert die **comadmincatalog** -Klasse [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) als Standardschnittstelle.

## <a name="comadmincatalogcollection"></a>Comadmincatalogcollection

Die [**comadmincatalogcollection**](comadmincatalogcollection.md) -Klasse stellt eine beliebige Auflistung im Katalog dar, indem eine Zeichenfolge bereitgestellt wird, die die jeweilige Auflistung bei der Objekt Instanziierung benennt. (Verfügbare Katalog Sammlungen werden in der Tabelle unter [com+-Verwaltungs Sammlungen](com--administration-collections.md)benannt.) Objekte werden aus dieser Klasse erstellt, wenn eine Auflistung der obersten Ebene abgerufen wird, indem die [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) -Methode des [**comadmincatalog**](comadmincatalog.md) -Objekts aufgerufen wird. Diese Objekte werden auch erstellt, wenn eine untergeordnete Auflistung abgerufen wird, indem die **GetCollection** -Methode des übergeordneten Auflistungs Objekts aufgerufen wird. Mit **comadmincatalogcollection** -Objekten können Sie folgende Aufgaben ausführen:

-   Listet die Elemente auf, die in der Auflistung enthalten sind.
-   Ruft ein Element aus der Auflistung ab.
-   Hinzufügen oder Entfernen von Elementen zu oder aus der Auflistung.
-   Speichern oder verwerfen Sie alle ausstehenden Änderungen an der Sammlung oder an den darin enthaltenen Elementen.
-   Sie erhalten eine andere Sammlung im Katalog.

Die [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse implementiert die [**icatalogcollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) -Schnittstelle.

## <a name="comadmincatalogobject"></a>COMAdminCatalogObject

Die [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse stellt ein beliebiges Element dar, das in einer Auflistung enthalten ist. Objekte werden aus dieser Klasse erstellt, wenn ein Element durch die [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) -Eigenschaft eines Katalog Sammlungs Objekts erhalten wird. Mithilfe von Objekten, die aus der **COMAdminCatalogObject** -Klasse erstellt wurden, können Sie folgende Aufgaben ausführen:

-   Dient zum Festlegen oder Festlegen von Eigenschaften, die von dem Element unterstützt werden, mit dem das Objekt dargestellt wird.
-   Abrufen von Informationen über das Element und seine Eigenschaften.

Die [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse implementiert die [**icatalogobject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) -Schnittstelle.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf den com+-Katalog](accessing-the-com--catalog.md)
</dt> <dt>

[Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
</dt> </dl>

 

 



