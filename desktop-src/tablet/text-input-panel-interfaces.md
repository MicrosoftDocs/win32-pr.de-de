---
description: Dieser Abschnitt enthält Informationen zu den Schnittstellen, die verwendet werden, um die Darstellung und das Verhalten des Tablet PC-Eingabe Bereichs zu steuern.
ms.assetid: 58f49d5b-8b38-45e7-94e1-8a4434d6e13b
title: Schnittstellen für Text Eingabebereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 798dc60f34171ce7254bca74c27a51fa12eaba65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218352"
---
# <a name="text-input-panel-interfaces"></a><span data-ttu-id="c29c0-103">Schnittstellen für Text Eingabebereich</span><span class="sxs-lookup"><span data-stu-id="c29c0-103">Text Input Panel Interfaces</span></span>

<span data-ttu-id="c29c0-104">Dieser Abschnitt enthält Informationen zu den Schnittstellen, die verwendet werden, um die Darstellung und das Verhalten des Tablet PC-Eingabe Bereichs zu steuern.</span><span class="sxs-lookup"><span data-stu-id="c29c0-104">This section contains information about the interfaces used to control the appearance and behavior of the Tablet PC Input Panel.</span></span>

> [!Note]  
> <span data-ttu-id="c29c0-105">Die Schnittstellen für den Text Eingabebereich sind nicht Automation-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c29c0-105">The Text Input Panel interfaces are not Automation compliant.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="c29c0-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c29c0-106">In This Section</span></span>



| <span data-ttu-id="c29c0-107">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c29c0-107">Interface</span></span>                                                                | <span data-ttu-id="c29c0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c29c0-108">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c29c0-109">**Ihandwrite-textinsertion-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c29c0-109">**IHandWrittenTextInsertion Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) | <span data-ttu-id="c29c0-110">Wird vom benutzerdefinierten Texteingabe Code der Anwendung verwendet, um den Text in das Textfeld und den Text Dienste-Unterstützungs Speicher einzufügen.</span><span class="sxs-lookup"><span data-stu-id="c29c0-110">Used by the application's custom text entry code to insert the text into both the text field and the Text Services backing-store.</span></span><br/> |
| [<span data-ttu-id="c29c0-111">**Itextinputpanel-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c29c0-111">**ITextInputPanel Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)                     | <span data-ttu-id="c29c0-112">Bietet Kontrolle über den Tablet PC-Eingabebereich.</span><span class="sxs-lookup"><span data-stu-id="c29c0-112">Provides control over the Tablet PC Input Panel.</span></span><br/>                                                                                  |
| [<span data-ttu-id="c29c0-113">**Itextinputpaneleventsink-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c29c0-113">**ITextInputPanelEventSink Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink)   | <span data-ttu-id="c29c0-114">Definiert Methoden, die die [**itextinputpanel-Schnittstellen**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) Ereignisse behandeln.</span><span class="sxs-lookup"><span data-stu-id="c29c0-114">Defines methods that handle the [**ITextInputPanel Interface**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) events.</span></span><br/>                                      |
| [<span data-ttu-id="c29c0-115">**Itextinputpanelruninfo-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c29c0-115">**ITextInputPanelRunInfo Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanelruninfo)       | <span data-ttu-id="c29c0-116">Stellt eine Methode bereit, um zu bestimmen, ob der Text Eingabebereich gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c29c0-116">Provides a method to determine if the Text Input Panel is currently running.</span></span><br/>                                                      |
| [<span data-ttu-id="c29c0-117">**Itipauwebcompleteclient-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c29c0-117">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)       | <span data-ttu-id="c29c0-118">Ermöglicht dem Client, das Auto Vervollständigen-Anbieter Objekt der Anwendung für den Text Eingabebereich aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c29c0-118">Enables the client to call the application's Text Input Panel auto complete provider object.</span></span><br/>                                      |
| [<span data-ttu-id="c29c0-119">**Itipauescompleteprovider-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c29c0-119">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)   | <span data-ttu-id="c29c0-120">Verwaltet die Seite der Anwendung der automatischen vollständigen Integration des Text Eingabe Bereichs.</span><span class="sxs-lookup"><span data-stu-id="c29c0-120">Manages the application's side of the Text Input Panel auto complete integration.</span></span><br/>                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="c29c0-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c29c0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c29c0-122">Verweis auf Text Eingabe Panel</span><span class="sxs-lookup"><span data-stu-id="c29c0-122">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




