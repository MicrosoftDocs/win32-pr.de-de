---
description: Im Netzwerkmonitor Frame-Viewer werden Analysierte Daten in drei Bereichen angezeigt.
ms.assetid: 72770b6f-1cec-4fa4-a91e-85367d531c7f
title: Anzeigen von analysierten Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0d1e82503d8ad78757e7c6cb1b8f02df8bc163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558312"
---
# <a name="viewing-parsed-information"></a><span data-ttu-id="b10e9-103">Anzeigen von analysierten Informationen</span><span class="sxs-lookup"><span data-stu-id="b10e9-103">Viewing Parsed Information</span></span>

<span data-ttu-id="b10e9-104">Im Netzwerkmonitor Frame-Viewer werden Analysierte Daten in drei Bereichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b10e9-104">The Network Monitor frame viewer displays parsed data in three panes.</span></span> <span data-ttu-id="b10e9-105">Im oberen Bereich wird eine Zusammenfassung des Frames angezeigt, in dem das identifizierte Protokoll enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b10e9-105">The upper pane displays a summary of the frame that includes the identified protocol.</span></span> <span data-ttu-id="b10e9-106">Im mittleren Bereich werden die Eigenschaften für formatierte Daten angezeigt, die hierarchisch als Teil der parseranzeige organisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="b10e9-106">The middle pane displays the formatted data properties that can be organized hierarchically as part of the parser display.</span></span> <span data-ttu-id="b10e9-107">Im unteren Bereich werden markierte Rohdaten angezeigt, die im mittleren Bereich ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="b10e9-107">The lower pane displays highlighted raw data that is selected from the middle pane.</span></span>

<span data-ttu-id="b10e9-108">Sie können angeben, wie die Informationen im Viewer angezeigt werden, wenn Sie einen eigenen Parser entwickeln.</span><span class="sxs-lookup"><span data-stu-id="b10e9-108">You can specify how the information in the viewer is displayed when you develop your own parser.</span></span> <span data-ttu-id="b10e9-109">Die folgende Abbildung zeigt, wie Informationen im Netzwerkmonitor Frame-Viewer angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="b10e9-109">The following illustration shows how information can be displayed in the Network Monitor frame viewer.</span></span>

![Netzwerkmonitor-Frame Viewer](images/parseui.png)

> [!Note]  
> <span data-ttu-id="b10e9-111">Parser zeigen keine Frames an.</span><span class="sxs-lookup"><span data-stu-id="b10e9-111">Parsers do not display frames.</span></span> <span data-ttu-id="b10e9-112">Parser erkennen Felder in den bereitgestellten Informationen und Benachrichtigen dann Netzwerkmonitor, den Frame anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b10e9-112">Parsers recognize fields in the information provided, and then notify Network Monitor to display the frame.</span></span> <span data-ttu-id="b10e9-113">Das Filtern ist ein Vorgang auf höherer Ebene, der es Filter Abfragen ermöglicht, Parser zu spannen.</span><span class="sxs-lookup"><span data-stu-id="b10e9-113">Filtering is a higher level operation that allows filter queries to span parsers.</span></span>

 

<span data-ttu-id="b10e9-114">Verwenden Sie in Ihrem Parser nur Funktionen, die in Microsoft Win32-Anwendungen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="b10e9-114">In your parser, use only functions that can run on Microsoft Win32 applications.</span></span> <span data-ttu-id="b10e9-115">Vor dem Anfügen von Eigenschaften an die Rohdaten muss ein Parser zunächst alle möglichen Eigenschaften mit dem Netzwerkmonitor Kernel registrieren.</span><span class="sxs-lookup"><span data-stu-id="b10e9-115">Before attaching properties to the raw data, a parser must first register all possible properties with the Network Monitor kernel.</span></span> <span data-ttu-id="b10e9-116">Der Parser sendet eine Nachricht an den Kernel, um eine Eigenschaften Datenbank zu erstellen, und füllt dann die Eigenschaften Datenbank mit jeder möglichen Eigenschaft für das zugehörige Protokoll aus.</span><span class="sxs-lookup"><span data-stu-id="b10e9-116">The parser sends a message to the kernel to create a property database, and then fills the property database with every possible property for its protocol.</span></span> <span data-ttu-id="b10e9-117">Jede Eigenschaft in der Eigenschaften Datenbank enthält Informationen, wie z. b. eine Textbeschreibung, einen Datentyp und einen Qualifizierer, die zum Formatieren der Rohdaten verwendet werden, und eine Formatierungs Routine, die zum Anzeigen der Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b10e9-117">Each property in the property database contains information such as a textual description, a data type and qualifier that are used to format the raw data, and a formatting routine that is used to display the data.</span></span>

 

 



