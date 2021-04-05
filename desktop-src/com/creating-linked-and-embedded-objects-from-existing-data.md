---
title: Erstellen von verknüpften und eingebetteten Objekten aus vorhandenen Daten
description: Erstellen von verknüpften und eingebetteten Objekten aus vorhandenen Daten
ms.assetid: 76848b7e-6068-4bac-9793-304f813096f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f60064516a4312a9de3ce511e00e49ce7276f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714267"
---
# <a name="creating-linked-and-embedded-objects-from-existing-data"></a>Erstellen von verknüpften und eingebetteten Objekten aus vorhandenen Daten

Ein Benutzer assembliert in der Regel ein Verbund Dokument, indem es entweder die Zwischenablage oder Drag & Drop verwendet, um ein Datenobjekt aus seiner Serveranwendung in die Containeranwendung des Benutzers zu kopieren. Bei Anwendungen, die OLE unterstützen, kann der Benutzer die Übertragung entweder vom Server oder vom Container initiieren. Der Server kann z. b. Daten in die Zwischenablage in der Serveranwendung kopieren, dann zur Containeranwendung wechseln und ein spezielles/eingebettetes Objekt einfügen oder einen entsprechenden Menübefehl Einfügen, um ein neues eingebettetes Objekt aus den ausgewählten Daten zu erstellen. Oder der Benutzer kann die Daten von einer Anwendung in die andere ziehen. Der Prozess ähnelt dem Erstellen eines verknüpften Objekts.

> [!Note]  
> Eine Anwendung, die sowohl als OLE-Server als auch als Container fungiert, kann eine Auswahl ihrer eigenen Daten verwenden, um ein eingebettetes oder verknüpftes Objekt an einem neuen Speicherort innerhalb desselben Dokuments zu erstellen.

 

Die Datenübertragung zwischen OLE-Server-und Container Anwendungen basiert auf einheitlicher Datenübertragung, wie in [Datenübertragung](data-transfer.md)beschrieben. OLE-Server und Objekt Handler implementieren [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , um Ihre Daten für Übertragungen über die Zwischenablage oder Drag & Drop verfügbar zu machen. OLE-Objekte unterstützen alle üblichen Zwischenablage Formate. Außerdem unterstützen Sie sechs Zwischenablage Formate, die die Erstellung von verknüpften und eingebetteten Objekten aus einem ausgewählten Datenobjekt unterstützen.

OLE-Zwischenablage Formate beschreiben Datenobjekte, die beim Ablegen oder Einfügen in OLE-Containern zu eingebetteten oder verknüpften Verbund Dokument Objekten werden. Das Datenobjekt stellt den Container Anwendungen diese Formate in der Reihenfolge ihrer Genauigkeit als Beschreibungen der Daten zur Folge. Anders ausgedrückt: das-Objekt stellt zuerst das Format dar, das es am besten darstellt, gefolgt vom nächst optimalen Format usw. Diese absichtliche Reihenfolge fördert eine Containeranwendung, um das bestmögliche Format zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbund Dokumente](compound-documents.md)
</dt> <dt>

[Datenübertragung](data-transfer.md)
</dt> </dl>

 

 




