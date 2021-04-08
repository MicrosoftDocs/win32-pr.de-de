---
title: Steuern eines Geräts
description: Nachdem Sie Geräte ermittelt haben, können Sie diese Steuern.
ms.assetid: 6d0efb80-d6f5-4b36-a184-19f06afeb2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ff91339c67b67de5d3e90eda0ce64ebcc68b9e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856784"
---
# <a name="controlling-a-device"></a><span data-ttu-id="ea075-103">Steuern eines Geräts</span><span class="sxs-lookup"><span data-stu-id="ea075-103">Controlling a Device</span></span>

<span data-ttu-id="ea075-104">Nachdem Sie Geräte ermittelt haben, können Sie diese Steuern.</span><span class="sxs-lookup"><span data-stu-id="ea075-104">Once you have discovered devices, you can control them.</span></span>

<span data-ttu-id="ea075-105">**So zeigen Sie die Geräteeigenschaften an**</span><span class="sxs-lookup"><span data-stu-id="ea075-105">**To view device properties**</span></span>

1.  <span data-ttu-id="ea075-106">Wählen Sie in der Liste **gefundene Geräte** ein Gerät aus.</span><span class="sxs-lookup"><span data-stu-id="ea075-106">Select a device from the **Devices Found** list.</span></span>
2.  <span data-ttu-id="ea075-107">Klicken Sie auf **Geräteeigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="ea075-107">Click **Device Properties**.</span></span> <span data-ttu-id="ea075-108">Das Fenster **Geräteeigenschaften** wird mit den angeforderten Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ea075-108">The **Device Properties** window appears with the requested information.</span></span>

> [!Note]  
> <span data-ttu-id="ea075-109">Die **View Presentation** -Funktionalität ist im C++-Beispielcode nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ea075-109">The **View Presentation** functionality is not available in the C++ sample code.</span></span>

 

<span data-ttu-id="ea075-110">**So zeigen Sie die Präsentationsseite eines Geräts an**</span><span class="sxs-lookup"><span data-stu-id="ea075-110">**To view a device's presentation page**</span></span>

1.  <span data-ttu-id="ea075-111">Wählen Sie in der Liste **gefundene Geräte** ein Gerät aus.</span><span class="sxs-lookup"><span data-stu-id="ea075-111">Select a device from the **Devices Found** list.</span></span>
2.  <span data-ttu-id="ea075-112">Klicken Sie auf **Präsentation anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="ea075-112">Click **View Presentation**.</span></span> <span data-ttu-id="ea075-113">Ein Internet Explorer-Fenster wird mit der angeforderten Präsentationsseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ea075-113">An Internet Explorer window appears with the requested presentation page.</span></span>

> [!Note]  
> <span data-ttu-id="ea075-114">Die Funktion " **View Service DESC.** " ist im C++-Beispielcode nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ea075-114">The **View Service Desc.** functionality is not available in the C++ sample code.</span></span>

 

<span data-ttu-id="ea075-115">**So zeigen Sie eine Dienst Beschreibung an**</span><span class="sxs-lookup"><span data-stu-id="ea075-115">**To view a service description**</span></span>

1.  <span data-ttu-id="ea075-116">Sie können die URL für die Dienst Beschreibung im **Dienst DESC eingeben. URL** -Feld.</span><span class="sxs-lookup"><span data-stu-id="ea075-116">You can enter the URL to the service description in the **Service Desc. URL** field.</span></span>

    ![Dienst Beschreibungs-URL](images/ucp-url.png)

2.  <span data-ttu-id="ea075-118">Klicken Sie auf **Dienst DESC anzeigen.** Das Fenster **Dienst Beschreibungs-Viewer** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ea075-118">Click **View Service Desc.** The **Service Description Viewer** window is displayed.</span></span> <span data-ttu-id="ea075-119">Anschließend können Sie die Dienst Beschreibung mithilfe der Strukturansicht durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="ea075-119">You can then browse the service description using the tree view.</span></span> <span data-ttu-id="ea075-120">Diese Funktion ist im C++-Beispielcode nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ea075-120">This functionality is not available in the C++ sample code.</span></span>

    ![Dienst Beschreibungs-Viewer-Fenster](images/ucp-serv.png)

    <span data-ttu-id="ea075-122">Es gibt fünf Befehle, die Sie im Dienst Beschreibungs-Viewer-Fenster verwenden können.</span><span class="sxs-lookup"><span data-stu-id="ea075-122">There are five commands you can use in the Service Description Viewer window.</span></span>



| <span data-ttu-id="ea075-123">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="ea075-123">Button</span></span>                 | <span data-ttu-id="ea075-124">Ausgeführte Aktion</span><span class="sxs-lookup"><span data-stu-id="ea075-124">Action Performed</span></span>                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea075-125">Go</span><span class="sxs-lookup"><span data-stu-id="ea075-125">Go</span></span>                     | <span data-ttu-id="ea075-126">Lädt die Datei, die im **Dienst DESC angezeigt wird. URL** -Feld.</span><span class="sxs-lookup"><span data-stu-id="ea075-126">Loads the file shown in the **Service Desc. URL** field.</span></span>                                                                                                                              |
| <span data-ttu-id="ea075-127">Aktion festlegen</span><span class="sxs-lookup"><span data-stu-id="ea075-127">Set Action</span></span>             | <span data-ttu-id="ea075-128">Wählen Sie in der Struktur der Dienst Beschreibung einen Aktions Namen aus, und klicken Sie auf **Aktion festlegen**.</span><span class="sxs-lookup"><span data-stu-id="ea075-128">Select an action name in the service description tree and click **Set Action**.</span></span> <span data-ttu-id="ea075-129">Der Aktionsname wird in das Feld **Aufruf Aktion** des **generischen Haupt-UCP** -Fensters eingegeben.</span><span class="sxs-lookup"><span data-stu-id="ea075-129">The action name is entered into the **Invoke Action** field of the main **Generic UCP** window.</span></span>       |
| <span data-ttu-id="ea075-130">Variable festlegen</span><span class="sxs-lookup"><span data-stu-id="ea075-130">Set Variable</span></span>           | <span data-ttu-id="ea075-131">Wählen Sie einen Variablennamen in der Dienst Beschreibungs Struktur aus, und klicken Sie auf **Variable festlegen**.</span><span class="sxs-lookup"><span data-stu-id="ea075-131">Select a variable name in the service description tree and click **Set Variable**.</span></span> <span data-ttu-id="ea075-132">Der Variablenname wird in das Feld **Abfrage Variable** des **generischen Haupt-UCP** -Fensters eingegeben.</span><span class="sxs-lookup"><span data-stu-id="ea075-132">The variable name is entered into the **Query Variable** field of the main **Generic UCP** window.</span></span> |
| <span data-ttu-id="ea075-133">Variablen Liste auffüllen</span><span class="sxs-lookup"><span data-stu-id="ea075-133">Populate Variable List</span></span> | <span data-ttu-id="ea075-134">Lädt alle Variablennamen aller Dienste in die **Abfrage Variablen** Liste des **generischen Haupt-UCP** -Fensters.</span><span class="sxs-lookup"><span data-stu-id="ea075-134">Loads all the service's variable names into the **Query Variable** list of the main **Generic UCP** window.</span></span>                                                                           |
| <span data-ttu-id="ea075-135">Aktionsliste Auffüllen</span><span class="sxs-lookup"><span data-stu-id="ea075-135">Populate Action List</span></span>   | <span data-ttu-id="ea075-136">Lädt alle Aktions Namen aller Dienste in die **Aufruf Aktions** Liste des **generischen Haupt-UCP** -Fensters.</span><span class="sxs-lookup"><span data-stu-id="ea075-136">Loads all the service's action names into the **Invoke Action** list of the main **Generic UCP** window.</span></span>                                                                              |



 

<span data-ttu-id="ea075-137">**So steuern Sie ein Gerät**</span><span class="sxs-lookup"><span data-stu-id="ea075-137">**To control a device**</span></span>

1.  <span data-ttu-id="ea075-138">Wählen Sie in der Liste **gefundene Geräte** das Gerät aus, das Sie steuern möchten.</span><span class="sxs-lookup"><span data-stu-id="ea075-138">From the **Devices Found** list, select the device you want to control.</span></span>
2.  <span data-ttu-id="ea075-139">Wählen Sie in der Liste **Dienst auswählen** den Dienst aus, den Sie aufrufen möchten, oder wählen Sie die Zustands Variable aus, die Sie Abfragen möchten.</span><span class="sxs-lookup"><span data-stu-id="ea075-139">From the **Choose Service** list, select the service you want to invoke or state variable you want to query.</span></span>

    ![Fenster "Geräte steuern"](images/ucp-contr.png)

    > [!Note]  
    > <span data-ttu-id="ea075-141">Der Inhalt der **Dienst Liste** basiert auf dem Gerät, das in der Liste **gefundene Geräte** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="ea075-141">The contents of the **Service List** is based on the device selected in the **Devices Found** list.</span></span>

     

3.  <span data-ttu-id="ea075-142">Wenn Sie den Wert einer Zustandsvariablen für den ausgewählten Dienst ermitteln möchten, geben Sie den Variablennamen in das Feld **Abfrage Variable** für Dienst ein.</span><span class="sxs-lookup"><span data-stu-id="ea075-142">If you want to find out the value of a state variable for the selected service, enter the variable name in the **Query Variable** field for service.</span></span> <span data-ttu-id="ea075-143">Klicken Sie auf **Abfragen**.</span><span class="sxs-lookup"><span data-stu-id="ea075-143">Click **Query**.</span></span> <span data-ttu-id="ea075-144">Die Ergebnisse werden im Feld **Abfrage Zustandswert/Aktions Ausgabe Argumente** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ea075-144">The results are shown in the **Query State Value/Action Out Arguments** field.</span></span>
4.  <span data-ttu-id="ea075-145">Wenn Sie eine Aktion für einen Dienst aufrufen möchten, geben Sie den Namen der Aktion im Feld **Aufruf Aktion** und alle Argumente im Feld **Aktions Argumente** ein.</span><span class="sxs-lookup"><span data-stu-id="ea075-145">If you want to invoke an action for a service, enter the action name in the **Invoke Action** field, and any arguments in the **Action Arguments** field.</span></span> <span data-ttu-id="ea075-146">Klicken Sie auf **aufrufen**.</span><span class="sxs-lookup"><span data-stu-id="ea075-146">Click **Invoke**.</span></span> <span data-ttu-id="ea075-147">Die Ergebnisse werden ggf. im Feld **Abfrage Zustandswert/Aktions Ausgabe Argumente** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ea075-147">The results are shown in the **Query State Value/Action Out Arguments** field, if any.</span></span>

    <span data-ttu-id="ea075-148">Der Rückgabewert ist, falls vorhanden, im ersten out-Argument enthalten.</span><span class="sxs-lookup"><span data-stu-id="ea075-148">The return value, if any, is contained in the first out argument.</span></span>

    > [!Note]  
    > <span data-ttu-id="ea075-149">Wenn mehrere Argumente für eine Aktion vorhanden sind, trennen Sie diese durch Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="ea075-149">If there are multiple arguments for an action, separate them with spaces.</span></span>

     

5.  <span data-ttu-id="ea075-150">Anzeigen von Ereignis Informationen im Feld " **Ereignisse** " für den ausgewählten Dienst.</span><span class="sxs-lookup"><span data-stu-id="ea075-150">View eventing information in the **Events** field for the selected service.</span></span>

 

 




