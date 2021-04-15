---
title: Datenübertragung
description: Datenübertragung
ms.assetid: 26b16438-f940-4086-869e-74021ed00b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37dee268b99f205e0093288f6980c8425220a45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516065"
---
# <a name="data-transfer"></a>Datenübertragung

Der Component Object Model (com) stellt einen Standardmechanismus zum Übertragen von Daten zwischen Anwendungen bereit. Dieser Mechanismus ist das *Datenobjekt*, bei dem es sich einfach um beliebige com-Objekte handelt, die die [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Schnittstelle implementieren. Einige Datenobjekte, z. b. ein Text, der in die Zwischenablage kopiert wurde, haben **IDataObject** als einzige Schnittstelle. Andere, wie z. b. Verbund Dokument Objekte, machen mehrere Schnittstellen verfügbar, von denen **IDataObject** einfach eins ist. Datenobjekte sind für die Arbeit von Verbund Dokumenten von grundlegender Bedeutung, auch wenn Sie über eine weit verbreitete Anwendung außerhalb der OLE-Technologie verfügen.

Durch Austauschen von Zeigern auf ein Datenobjekt können Anbieter und Consumer von Daten Datenübertragungen auf einheitliche Weise verwalten, unabhängig vom Format der Daten, dem Medientyp, der zum Übertragen der Daten verwendet wird, oder dem Zielgerät, auf dem Sie gerendert werden soll. Sie können Unterstützung für grundlegende Übertragungen der Zwischenablage, Drag & Drop-Übertragungen und OLE-Verbund Dokument Übertragungen mit einer einzelnen Implementierung von [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)einschließen. Wenn dies der Fall ist, ist die Menge an Code, die für die besondere Semantik der einzelnen Protokolle erforderlich ist, minimal.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Datenübertragung Schnittstellen](data-transfer-interfaces.md)
-   [Datenformate und Übertragungsmedien](data-formats-and-transfer-media.md)
-   [Drag &amp; Drop](drag-and-drop.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbund Dokumente](compound-documents.md)
</dt> </dl>

 

 




