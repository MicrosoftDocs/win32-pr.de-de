---
title: Standardbildobjekt
description: Standardbildobjekt
ms.assetid: 2df9e0a7-444b-454c-983a-82e82b9ed9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4b74daa4f62791c12927eba3fd0472ed2a956d4b84c03e3cc373c44e12ce25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129762"
---
# <a name="standard-picture-object"></a>Standardbildobjekt

Das Standardbildobjekt stellt eine sprachneutrale Abstraktion für GDI-Bilder bereit: Bitmaps, Symbole, Metadateien und erweiterte Metadateien. Wie beim Standardschriftartobjekt stellt das System eine Standardimplementierung dieses Objekts bereit. Die primären Schnittstellen sind [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) und [**IPictureDisp.**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp)Letztere werden von **IDispatch** abgeleitet, um den Zugriff auf die Eigenschaften des Bilds durch OLE-Automatisierung zu ermöglichen. Ein Bildobjekt wird neu mit [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)erstellt.

Das Bildobjekt unterstützt auch die ausgehende Schnittstelle [**IPropertyNotifySink, sodass**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) ein Client bestimmen kann, wann sich Bildeigenschaften ändern. Entsprechend unterstützt das Bildobjekt auch [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) und einen Verbindungspunkt für **IPropertyNotifySink.**

Das Bildobjekt unterstützt auch [**IPersistStream,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) sodass es sich selbst in einer Instanz von [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)speichern und laden kann. Ein Objekt, das intern ein Bildobjekt verwendet, würde normalerweise das Bild im Rahmen der eigenen Persistenzbehandlung des Objekts speichern und laden. Die [**OleLoadPicture-Funktion**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) vereinfacht die Erstellung eines Bildobjekts basierend auf Streaminhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementeigenschaften](control-properties.md)
</dt> </dl>

 

 