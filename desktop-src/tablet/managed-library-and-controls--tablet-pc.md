---
description: Zum Erstellen von Tablet PC-Anwendungen in C \# und Visual Basic .NET muss Ihr Projekt in Microsoft Visual Studio .net einen Verweis auf die von Tablet PC verwalteten Bibliotheksassemblys enthalten. Dies ermöglicht den Zugriff auf das verwaltete Objektmodell und die Steuerelemente.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Verwaltete Bibliothek und Steuerelemente (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7299a1df0cc1b64d650ec748eb2de01ad4b776f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366117"
---
# <a name="managed-library-and-controls-tablet-pc"></a><span data-ttu-id="8a187-104">Verwaltete Bibliothek und Steuerelemente (Tablet PC)</span><span class="sxs-lookup"><span data-stu-id="8a187-104">Managed Library and Controls (Tablet PC)</span></span>

<span data-ttu-id="8a187-105">Zum Erstellen von Tablet PC-Anwendungen in C \# und Visual Basic .NET muss Ihr Projekt in Microsoft Visual Studio .net einen Verweis auf die von Tablet PC verwalteten Bibliotheksassemblys enthalten.</span><span class="sxs-lookup"><span data-stu-id="8a187-105">To build Tablet PC applications in C\# and Visual Basic .NET, your project in Microsoft Visual Studio .NET must include a reference to the Tablet PC managed library assemblies.</span></span> <span data-ttu-id="8a187-106">Dies ermöglicht den Zugriff auf das verwaltete Objektmodell und die Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="8a187-106">This provides access to the managed object model and controls.</span></span>

## <a name="microsoft-visual-c-and-visual-basicnet"></a><span data-ttu-id="8a187-107">Microsoft Visual C \# und Visual Basic.net</span><span class="sxs-lookup"><span data-stu-id="8a187-107">Microsoft Visual C\# and Visual Basic.NET</span></span>

<span data-ttu-id="8a187-108">In Windows Vista werden die von Tablet PC verwalteten Bibliotheksassemblys standardmäßig in zwei Verzeichnissen installiert:</span><span class="sxs-lookup"><span data-stu-id="8a187-108">In Windows Vista, the Tablet PC managed library assemblies are installed by default in two directories:</span></span>

-   <span data-ttu-id="8a187-109"><systemdrive>: \\ Programmdateien \\ Allgemeine Dateien \\ Microsoft Shared \\ Ink Directory</span><span class="sxs-lookup"><span data-stu-id="8a187-109"><systemdrive>:\\Program Files\\Common Files\\Microsoft Shared\\Ink directory</span></span>
-   <span data-ttu-id="8a187-110"><systemdrive>: \\ Programme \\ Microsoft sdert \\ Windows \\ v 6.0 \\ bin</span><span class="sxs-lookup"><span data-stu-id="8a187-110"><systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Bin</span></span>

<span data-ttu-id="8a187-111">So fügen Sie einen Verweis auf die von Tablet PC Platform verwalteten Bibliotheken in Microsoft Visual Studio .net hinzu:</span><span class="sxs-lookup"><span data-stu-id="8a187-111">To add a reference to the Tablet PC platform managed libraries in Microsoft Visual Studio .NET:</span></span>

1.  <span data-ttu-id="8a187-112">Öffnen Sie das Visual Studio .net-Projekt.</span><span class="sxs-lookup"><span data-stu-id="8a187-112">Open your Visual Studio .NET project.</span></span>
2.  <span data-ttu-id="8a187-113">Klicken Sie im Menü **Projekt** auf **Verweis hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="8a187-113">On the **Project** menu, click **Add Reference**.</span></span>
3.  <span data-ttu-id="8a187-114">Wählen Sie auf der Registerkarte **.net** im Dialogfeld **Verweis hinzufügen** in der Liste Komponenten die Option **Microsoft Tablet PC-API** aus.</span><span class="sxs-lookup"><span data-stu-id="8a187-114">On the **.NET** tab in the **Add Reference** dialog box, on the components list, select **Microsoft Tablet PC API**.</span></span>
4.  <span data-ttu-id="8a187-115">Klicken Sie auf **auswählen**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a187-115">Click **Select**, and then click **OK**.</span></span>

<span data-ttu-id="8a187-116">So fügen Sie einen Verweis auf die APIs für die frei Hand Analyse in Visual Studio .net hinzu:</span><span class="sxs-lookup"><span data-stu-id="8a187-116">To add a reference to the ink analysis APIs in Visual Studio .NET:</span></span>

1.  <span data-ttu-id="8a187-117">Öffnen Sie das Microsoft Visual Studio .net-Projekt.</span><span class="sxs-lookup"><span data-stu-id="8a187-117">Open your Microsoft Visual Studio .NET project.</span></span>
2.  <span data-ttu-id="8a187-118">Klicken Sie im Menü **Projekt** auf **Verweis hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="8a187-118">On the **Project** menu, click **Add Reference**.</span></span>
3.  <span data-ttu-id="8a187-119">Wählen Sie auf der Registerkarte **.net** im Dialogfeld **Verweis hinzufügen** in der Liste Komponenten die Option **Microsoft Tablet PC Ink Analysis verwaltete Bibliothek** aus.</span><span class="sxs-lookup"><span data-stu-id="8a187-119">On the **.NET** tab in the **Add Reference** dialog box, on the components list, select **Microsoft Tablet PC Ink Analysis Managed Library**.</span></span>
4.  <span data-ttu-id="8a187-120">Klicken Sie auf **auswählen**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a187-120">Click **Select**, and then click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="8a187-121">Wenn Sie Anwendungen kompilieren, die Microsoft. Ink in Visual Studio 2005 verwenden, müssen Sie **Project**, Select **Properties**, **Build** und Set Platform Target = x86 auswählen.</span><span class="sxs-lookup"><span data-stu-id="8a187-121">When compiling applications that use Microsoft.Ink on Visual Studio 2005, you must select **Project**, select **Properties**, select **Build** and set Platform target=x86.</span></span> <span data-ttu-id="8a187-122">Diese Option ist in Microsoft Visual Studio Express Produkte nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8a187-122">This option is not available in Microsoft Visual Studio Express products.</span></span>

 

 

 



