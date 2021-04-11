---
title: Standard Bild Objekt
description: Standard Bild Objekt
ms.assetid: 2df9e0a7-444b-454c-983a-82e82b9ed9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8a711fc0c33cf5e99b0db6e90941dbe855289b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949144"
---
# <a name="standard-picture-object"></a>Standard Bild Objekt

Das Standardbild Objekt stellt eine sprachneutrale Abstraktion für GDI-Images bereit: Bitmaps, Symbole, Metadateien und Erweiterte Metadateien. Wie beim Standard Schriftart Objekt stellt das System eine Standard Implementierung dieses Objekts bereit. Die primären Schnittstellen sind [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) und [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp). Letztere werden von **IDispatch** abgeleitet, um den Zugriff auf die Eigenschaften des Bilds durch OLE-Automatisierung zu ermöglichen. Ein Bild Objekt wird mit [**olecreatepictureindirekte**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)neu erstellt.

Das Bild Objekt unterstützt auch die ausgehende Schnittstelle [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) , damit ein Client ermitteln kann, wann die Bildeigenschaften geändert werden. Dementsprechend unterstützt das Bild Objekt auch [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) und einen Verbindungspunkt für **IPropertyNotifySink**.

Das Bild Objekt unterstützt [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) auch so, dass es sich selbst speichern und aus einer Instanz von [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)laden kann. Ein Objekt, das ein Bild Objekt intern verwendet, speichert und lädt das Bild normalerweise als Teil der eigenen persistenzverarbeitung des Objekts. Die [**oleloadpicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) -Funktion vereinfacht die Erstellung eines Bildobjekts basierend auf dem Streaminhalt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Eigenschaften](control-properties.md)
</dt> </dl>

 

 