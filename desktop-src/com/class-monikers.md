---
title: Klassenmoniker
description: Obwohl Klassen normalerweise direkt mit CLSIDs für Funktionen wie cokreatanstance oder CoGetClassObject identifiziert werden, können Klassen jetzt auch mit einem Moniker identifiziert werden, der als klassenmoniker bezeichnet wird.
ms.assetid: 63f5d256-cb61-4673-b5d6-da5c1d89dfa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80886ce49ea25d2fb5acbf4dddf550c9d2c3ae29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311177"
---
# <a name="class-monikers"></a>Klassenmoniker

Obwohl Klassen normalerweise direkt mit CLSIDs für Funktionen wie [**cokreatanstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)identifiziert werden, können Klassen jetzt auch mit einem Moniker identifiziert werden, der als *klassenmoniker* bezeichnet wird. Klassenmoniker binden an das Klassenobjekt der Klasse, für die Sie erstellt werden.

Die Möglichkeit zum Identifizieren von Klassen mit einem Moniker unterstützt nützliche Vorgänge, die ansonsten unhandlich sind. Beispielsweise unterstützten dateimoniker in der Regel nur eine umfangreiche Bindung an die Klasse, die der Klasse der Datei zugeordnet ist, auf die Sie verweisen. ein Moniker für eine Excel-Datei würde eine Bindung an eine Instanz eines Excel-Objekts herstellen, und ein Moniker für ein GIF-Bild würde an eine Instanz des aktuell registrierten GIF-Handlers gebunden werden. Mit einem klassenmoniker können Sie die Klasse angeben, die Sie verwenden möchten, um eine Datei durch Komposition mit einem dateimoniker zu manipulieren. Ein klassenmoniker für eine 3D-Diagramm Klasse, die mit einem Moniker in einer Excel-Datei zusammengesetzt wird, erzeugt einen Moniker, der an eine Instanz des 3D-Diagramm Objekts gebunden ist, und initialisiert das Objekt mit dem Inhalt der Excel-Datei.

Klassenmoniker sind daher am nützlichsten bei der Komposition mit anderen Typen von Monikern, z. b. dateimonikern oder elementmoniker.

Klassenmoniker können auch rechts von Monikern zusammengesetzt werden, die die Bindung an die [**iclassactivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) -Schnittstelle unterstützen. Wenn Sie auf diese Weise zusammengesetzt wird, bietet **iclassactivator** einfach Zugriff auf das Klassenobjekt und Instanzen der Klasse über [**iclassactivator:: GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject). Klassenmoniker können über [**IMoniker:: IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker)identifiziert werden, der den MKSYS- \_ classmoniker in *pdwmksys* zurückgibt.

Programmierer erstellen üblicherweise klassenmoniker mithilfe der Funktion " [**deeclassmoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) " oder mithilfe von " [**mkparsetdisplayname**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname)". (Weitere Informationen finden Sie unter [**IMoniker::P armendisplayname**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) .)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anti-Moniker](anti-monikers.md)
</dt> <dt>

[Zusammengesetzte Moniker](composite-monikers.md)
</dt> <dt>

[Dateimoniker](file-monikers.md)
</dt> <dt>

[Elementmoniker](item-monikers.md)
</dt> <dt>

[Zeigermoniker](pointer-monikers.md)
</dt> </dl>

 

 




