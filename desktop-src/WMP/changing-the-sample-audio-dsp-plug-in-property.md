---
title: Ändern der Sample audiodsp-Plug-in-Eigenschaft
description: Ändern der Sample audiodsp-Plug-in-Eigenschaft
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Windows Media Player-Plug-ins, audiodsp
- Plug-ins, audiodsp
- Plug-Ins für die digitale Signalverarbeitung, Audioeigenschaften
- DSP-Plug-ins, Audioeigenschaften
- audiodsp-Plug-ins, Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc27f58fa8c8903b54f9903797dcc32a7795841
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712185"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a><span data-ttu-id="d8250-108">Ändern der Sample audiodsp-Plug-in-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d8250-108">Changing the Sample Audio DSP Plug-in Property</span></span>

<span data-ttu-id="d8250-109">Sie möchten wahrscheinlich die Eigenschaft ändern, die der Assistent für den Windows Media Player-Plug-in standardmäßig erstellt.</span><span class="sxs-lookup"><span data-stu-id="d8250-109">You will probably want to change the property that the Windows Media Player Plug-in Wizard creates by default.</span></span> <span data-ttu-id="d8250-110">In der folgenden Liste sind die Elemente aufgeführt, die möglicherweise geändert werden müssen:</span><span class="sxs-lookup"><span data-stu-id="d8250-110">The following list details the items that might require changing:</span></span>

-   <span data-ttu-id="d8250-111">**Die Dialogfeld Ressource.**</span><span class="sxs-lookup"><span data-stu-id="d8250-111">**The dialog resource.**</span></span> <span data-ttu-id="d8250-112">Klicken Sie im Fenster Arbeitsbereich des Projekts auf die Registerkarte **resourceview** .</span><span class="sxs-lookup"><span data-stu-id="d8250-112">Click the **ResourceView** tab in the Project Workspace window.</span></span> <span data-ttu-id="d8250-113">Erweitern Sie die Ordnerliste, um den Dialog Ordner zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d8250-113">Expand the folder list to open the Dialog folder.</span></span> <span data-ttu-id="d8250-114">Doppelklicken Sie auf die Dialogfeld Ressource, um den Ressourcen-Editor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d8250-114">Double-click the dialog resource to open the resource editor.</span></span> <span data-ttu-id="d8250-115">Sie können Änderungen am Eigenschaften Seiten Dialogfeld vornehmen, um Ihre Anforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="d8250-115">You can make changes to the property page dialog to fulfill your needs.</span></span> <span data-ttu-id="d8250-116">Beispielsweise können Sie den Text in der Bezeichnung ändern oder das Bearbeitungs Steuerelement durch ein Kontrollkästchen ersetzen.</span><span class="sxs-lookup"><span data-stu-id="d8250-116">For instance, you could change the text in the label or replace the edit control with a checkbox.</span></span>
-   <span data-ttu-id="d8250-117">**Der Objektcode der Eigenschaften Seite.**</span><span class="sxs-lookup"><span data-stu-id="d8250-117">**The property page object code.**</span></span> <span data-ttu-id="d8250-118">Die Standard Implementierung verwendet eine Variable vom Typ Double, um den Skalierungsfaktor zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d8250-118">The default implementation uses a variable of type double to store the scale factor.</span></span> <span data-ttu-id="d8250-119">Möglicherweise benötigen Sie einen anderen Datentyp.</span><span class="sxs-lookup"><span data-stu-id="d8250-119">You might require a different type of data.</span></span> <span data-ttu-id="d8250-120">Dies erfordert auch, dass Sie den Code, der die Daten persistent speichert, in die Registrierung ändern und die Daten aus der Registrierung lesen (einschließlich des Codes, der aus der Registrierung in *cprojectname*::**FinalConstruct** liest).</span><span class="sxs-lookup"><span data-stu-id="d8250-120">This would also require you to change the code that persists the data to the registry and reads the data from the registry (including the code that reads from the registry in *CProjectName*::**FinalConstruct**).</span></span>
-   <span data-ttu-id="d8250-121">**Die Element Variable, die den Eigenschafts Wert speichert.**</span><span class="sxs-lookup"><span data-stu-id="d8250-121">**The member variable that stores the property value.**</span></span> <span data-ttu-id="d8250-122">Diese Variable hat den Namen "m \_ f/alefactor" und ist als Typ "Double" deklariert.</span><span class="sxs-lookup"><span data-stu-id="d8250-122">This variable is named "m\_fScaleFactor" and is declared as type double.</span></span> <span data-ttu-id="d8250-123">Möglicherweise möchten Sie den Namen und den Typ dieser Variablen im gesamten Projekt ändern.</span><span class="sxs-lookup"><span data-stu-id="d8250-123">You may want to change the name and type of this variable throughout the project.</span></span>
-   <span data-ttu-id="d8250-124">**Die Get-und Property Put-Methode der Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="d8250-124">**The property get and property put methods.**</span></span> <span data-ttu-id="d8250-125">Möglicherweise möchten Sie die Namen, Parameter und Implementierungen dieser Methoden ändern.</span><span class="sxs-lookup"><span data-stu-id="d8250-125">You might want to change the names, parameters, and implementations of these methods.</span></span> <span data-ttu-id="d8250-126">Vergessen Sie nicht, diese Änderungen auch an anderer Stelle im Projekt widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="d8250-126">Don't forget to also reflect those changes elsewhere in the project.</span></span> <span data-ttu-id="d8250-127">Beispielsweise ruft die Methode zum **anwenden** der Eigenschaften Seite " *cprojectname*::**Put \_ Scale**" auf.</span><span class="sxs-lookup"><span data-stu-id="d8250-127">For instance, the property page **Apply** method calls *CProjectName*::**put\_scale**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8250-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8250-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8250-129">**Implementieren eines audiodsp-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="d8250-129">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




