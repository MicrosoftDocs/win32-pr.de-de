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
# <a name="data-transfer"></a><span data-ttu-id="420d7-103">Datenübertragung</span><span class="sxs-lookup"><span data-stu-id="420d7-103">Data Transfer</span></span>

<span data-ttu-id="420d7-104">Der Component Object Model (com) stellt einen Standardmechanismus zum Übertragen von Daten zwischen Anwendungen bereit.</span><span class="sxs-lookup"><span data-stu-id="420d7-104">The Component Object Model (COM) provides a standard mechanism for transferring data between applications.</span></span> <span data-ttu-id="420d7-105">Dieser Mechanismus ist das *Datenobjekt*, bei dem es sich einfach um beliebige com-Objekte handelt, die die [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="420d7-105">This mechanism is the *data object*, which is simply any COM object that implements the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="420d7-106">Einige Datenobjekte, z. b. ein Text, der in die Zwischenablage kopiert wurde, haben **IDataObject** als einzige Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="420d7-106">Some data objects, such as a piece of text copied to the clipboard, have **IDataObject** as their sole interface.</span></span> <span data-ttu-id="420d7-107">Andere, wie z. b. Verbund Dokument Objekte, machen mehrere Schnittstellen verfügbar, von denen **IDataObject** einfach eins ist.</span><span class="sxs-lookup"><span data-stu-id="420d7-107">Others, such as compound document objects, expose several interfaces, of which **IDataObject** is simply one.</span></span> <span data-ttu-id="420d7-108">Datenobjekte sind für die Arbeit von Verbund Dokumenten von grundlegender Bedeutung, auch wenn Sie über eine weit verbreitete Anwendung außerhalb der OLE-Technologie verfügen.</span><span class="sxs-lookup"><span data-stu-id="420d7-108">Data objects are fundamental to the working of compound documents, although they also have widespread application outside that OLE technology.</span></span>

<span data-ttu-id="420d7-109">Durch Austauschen von Zeigern auf ein Datenobjekt können Anbieter und Consumer von Daten Datenübertragungen auf einheitliche Weise verwalten, unabhängig vom Format der Daten, dem Medientyp, der zum Übertragen der Daten verwendet wird, oder dem Zielgerät, auf dem Sie gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="420d7-109">By exchanging pointers to a data object, providers and consumers of data can manage data transfers in a uniform manner, regardless of the format of the data, the type of medium used to transfer the data, or the target device on which it is to be rendered.</span></span> <span data-ttu-id="420d7-110">Sie können Unterstützung für grundlegende Übertragungen der Zwischenablage, Drag & Drop-Übertragungen und OLE-Verbund Dokument Übertragungen mit einer einzelnen Implementierung von [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)einschließen.</span><span class="sxs-lookup"><span data-stu-id="420d7-110">You can include support in your application for basic clipboard transfers, drag and drop transfers, and OLE compound document transfers with a single implementation of [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject).</span></span> <span data-ttu-id="420d7-111">Wenn dies der Fall ist, ist die Menge an Code, die für die besondere Semantik der einzelnen Protokolle erforderlich ist, minimal.</span><span class="sxs-lookup"><span data-stu-id="420d7-111">Having done that, the amount of code required to accommodate the special semantics of each protocol is minimal.</span></span>

<span data-ttu-id="420d7-112">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="420d7-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="420d7-113">Datenübertragung Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="420d7-113">Data Transfer Interfaces</span></span>](data-transfer-interfaces.md)
-   [<span data-ttu-id="420d7-114">Datenformate und Übertragungsmedien</span><span class="sxs-lookup"><span data-stu-id="420d7-114">Data Formats and Transfer Media</span></span>](data-formats-and-transfer-media.md)
-   [<span data-ttu-id="420d7-115">Drag &amp; Drop</span><span class="sxs-lookup"><span data-stu-id="420d7-115">Drag and Drop</span></span>](drag-and-drop.md)

## <a name="related-topics"></a><span data-ttu-id="420d7-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="420d7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="420d7-117">Verbund Dokumente</span><span class="sxs-lookup"><span data-stu-id="420d7-117">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




