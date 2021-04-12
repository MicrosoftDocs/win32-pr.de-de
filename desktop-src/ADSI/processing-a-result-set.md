---
title: Verarbeiten eines Resultsets
description: Ein Resultset wird als eine Reihe von Zeilen zurückgegeben.
ms.assetid: e0949c1c-a31a-440a-ae10-2934ffeb7128
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ad422494fd2d384b612989e9e36cec7110e021
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316449"
---
# <a name="processing-a-result-set"></a>Verarbeiten eines Resultsets

Ein Resultset wird als eine Reihe von Zeilen zurückgegeben. Jede Zeile kann ein bestimmtes Attribut enthalten. Mit dem OLE DB-Anbieter wird das Resultset ähnlich wie ein normales SQL-Resultset angezeigt. Wenn Sie ADO für die Abfrage verwenden, [ADODB. Das Recordset](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) -Objekt wird zum Durchlaufen des Resultsets verwendet. [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (nur in Sprachen verfügbar, die Vtable-Bindungen unterstützen) enthält Elemente zum Verschieben des Zeilen Cursors und Überprüfen von Eigenschafts Werten in einer bestimmten Zeile. Alternativ können Sie [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) verwenden, um Eigenschaften zu erhalten und festzulegen.

 

 