---
title: Klassenmoniker
description: Obwohl Klassen in der Regel direkt mit CLSIDs für Funktionen wie CoCreateInstance oder CoGetClassObject identifiziert werden, können Klassen jetzt auch mit einem Moniker identifiziert werden, der als Klassenmoniker bezeichnet wird.
ms.assetid: 63f5d256-cb61-4673-b5d6-da5c1d89dfa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499a117372cd7364fc52b3503b30175a4be11afb9e28e3dd32adbf1007185f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048692"
---
# <a name="class-monikers"></a>Klassenmoniker

Obwohl Klassen in der Regel direkt mit CLSIDs für Funktionen wie [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)identifiziert werden, können Klassen jetzt auch mit einem Moniker identifiziert werden, der als Klassenmoniker bezeichnet *wird.* Klassenmoniker werden an das Klassenobjekt der Klasse gebunden, für die sie erstellt werden.

Die Fähigkeit, Klassen mit einem Moniker zu identifizieren, unterstützt nützliche Vorgänge, die andernfalls unhandlich sind. Dateimoniker unterstützten z. B. traditionell eine umfassende Bindung nur an die Klasse, die der Dateiklasse zugeordnet ist, auf die sie verwiesen haben. Ein Moniker an eine Excel-Datei würde an eine Instanz eines Excel-Objekts gebunden, und ein Moniker an ein GIF-Bild würde an eine Instanz des derzeit registrierten GIF-Handlers gebunden. Mit einem Klassenmoniker können Sie die Klasse angeben, die Sie verwenden möchten, um eine Datei durch Komposition mit einem Dateimoniker zu bearbeiten. Ein Klassenmoniker für eine 3D-Diagrammklasse, der mit einem Moniker zu einer Excel-Datei zusammengesetzt ist, ergibt einen Moniker, der an eine Instanz des 3D-Diagrammobjekts gebunden ist und das Objekt mit dem Inhalt der Excel-Datei initialisiert.

Klassenmoniker sind daher am nützlichsten bei der Komposition mit anderen Typen von Monikern, z. B. Dateimonikern oder Elementmonikern.

Klassenmoniker können auch rechts von Monikern zusammengesetzt werden, die die Bindung an die [**IClassActivator-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) unterstützen. Auf diese Weise ermöglicht **IClassActivator** einfach den Zugriff auf das Klassenobjekt und die Instanzen der -Klasse über [**IClassActivator::GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject). Klassenmoniker können über [**IMoniker::IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker)identifiziert werden, der MKSYS \_ CLASSMONIKER in *pdwMksys zurückgibt.*

Programmierer erstellen klassenmoniker in der Regel mithilfe der [**CreateClassMoniker-Funktion**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) oder [**über MkParseDisplayName.**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname) (Weitere Informationen finden Sie unter [**IMoniker::P arseDisplayName.)**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Antimoniker](anti-monikers.md)
</dt> <dt>

[Zusammengesetzte Moniker](composite-monikers.md)
</dt> <dt>

[Dateimoniker](file-monikers.md)
</dt> <dt>

[Elementmoniker](item-monikers.md)
</dt> <dt>

[Zeigermoniker](pointer-monikers.md)
</dt> </dl>

 

 




