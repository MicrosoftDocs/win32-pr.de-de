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
# <a name="standard-picture-object"></a><span data-ttu-id="37e52-103">Standard Bild Objekt</span><span class="sxs-lookup"><span data-stu-id="37e52-103">Standard Picture Object</span></span>

<span data-ttu-id="37e52-104">Das Standardbild Objekt stellt eine sprachneutrale Abstraktion für GDI-Images bereit: Bitmaps, Symbole, Metadateien und Erweiterte Metadateien.</span><span class="sxs-lookup"><span data-stu-id="37e52-104">The standard picture object provides a language-neutral abstraction for GDI images: bitmaps, icons, metafiles, and enhanced metafiles.</span></span> <span data-ttu-id="37e52-105">Wie beim Standard Schriftart Objekt stellt das System eine Standard Implementierung dieses Objekts bereit.</span><span class="sxs-lookup"><span data-stu-id="37e52-105">As with the standard font object, the system provides a standard implementation of this object.</span></span> <span data-ttu-id="37e52-106">Die primären Schnittstellen sind [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) und [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp). Letztere werden von **IDispatch** abgeleitet, um den Zugriff auf die Eigenschaften des Bilds durch OLE-Automatisierung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="37e52-106">Its primary interfaces are [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) and [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), the latter being derived from **IDispatch** to provide access to the picture's properties through OLE automation.</span></span> <span data-ttu-id="37e52-107">Ein Bild Objekt wird mit [**olecreatepictureindirekte**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="37e52-107">A picture object is created new with [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span></span>

<span data-ttu-id="37e52-108">Das Bild Objekt unterstützt auch die ausgehende Schnittstelle [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) , damit ein Client ermitteln kann, wann die Bildeigenschaften geändert werden.</span><span class="sxs-lookup"><span data-stu-id="37e52-108">The picture object also supports the outgoing interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) so that a client can determine when picture properties change.</span></span> <span data-ttu-id="37e52-109">Dementsprechend unterstützt das Bild Objekt auch [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) und einen Verbindungspunkt für **IPropertyNotifySink**.</span><span class="sxs-lookup"><span data-stu-id="37e52-109">Accordingly, the picture object also supports [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) and one connection point for **IPropertyNotifySink**.</span></span>

<span data-ttu-id="37e52-110">Das Bild Objekt unterstützt [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) auch so, dass es sich selbst speichern und aus einer Instanz von [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)laden kann.</span><span class="sxs-lookup"><span data-stu-id="37e52-110">The picture object also supports [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) such that it can save and load itself from an instance of [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span> <span data-ttu-id="37e52-111">Ein Objekt, das ein Bild Objekt intern verwendet, speichert und lädt das Bild normalerweise als Teil der eigenen persistenzverarbeitung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="37e52-111">An object that uses a picture object internally would normally save and load the picture as part of the object's own persistence handling.</span></span> <span data-ttu-id="37e52-112">Die [**oleloadpicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) -Funktion vereinfacht die Erstellung eines Bildobjekts basierend auf dem Streaminhalt.</span><span class="sxs-lookup"><span data-stu-id="37e52-112">The [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) function simplifies the creation of a picture object based on stream contents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37e52-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="37e52-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37e52-114">Steuerelement Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37e52-114">Control Properties</span></span>](control-properties.md)
</dt> </dl>

 

 