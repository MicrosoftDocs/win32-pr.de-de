---
description: Ein Klassen Anbieter verwaltet eine Klasse oder eine Reihe von Klassen für WMI.
ms.assetid: 755f1fde-a0bf-43f6-a01d-2da7d4e6c10d
ms.tgt_platform: multiple
title: Schreiben eines Klassen Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1e20115c4f833ad828e8d181ca97782d233130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347410"
---
# <a name="writing-a-class-provider"></a><span data-ttu-id="b9847-103">Schreiben eines Klassen Anbieters</span><span class="sxs-lookup"><span data-stu-id="b9847-103">Writing a Class Provider</span></span>

<span data-ttu-id="b9847-104">Ein Klassen Anbieter verwaltet eine Klasse oder eine Reihe von Klassen für WMI.</span><span class="sxs-lookup"><span data-stu-id="b9847-104">A class provider manages a class or series of classes for WMI.</span></span> <span data-ttu-id="b9847-105">Ein Klassen Anbieter kann per Push oder Pull abgerufen werden. Das heißt, es kann entweder eigene Daten speichern oder WMI das Speichern von Daten im Windows-Verwaltungsdienst ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b9847-105">A class provider can either be push or pull; that is, it can either store its own data or allow WMI to store data for it in the Windows Management Service.</span></span> <span data-ttu-id="b9847-106">Obwohl ein Klassen Anbieter auf einem bestimmten Computer installiert ist, kann er die Klassendefinitionen über ein gesamtes Unternehmen hinweg ändern.</span><span class="sxs-lookup"><span data-stu-id="b9847-106">Although a class provider is installed on a specific machine, it can change the class definitions across an entire enterprise.</span></span> <span data-ttu-id="b9847-107">Daher erstellen die meisten Entwickler nicht häufig Klassen Anbieter.</span><span class="sxs-lookup"><span data-stu-id="b9847-107">Therefore, most developers do not often create class providers.</span></span>

<span data-ttu-id="b9847-108">Überprüfen Sie vor dem Erstellen eines Klassen Anbieters, ob die unterstützten Klassen wirklich dynamisch generiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b9847-108">Before constructing a class provider, verify that the supported classes truly must be generated dynamically.</span></span> <span data-ttu-id="b9847-109">In den meisten Fällen ist die Liste der Klassen langsam veränderlich und begrenzt.</span><span class="sxs-lookup"><span data-stu-id="b9847-109">In most cases, the list of classes is slow-changing and finite.</span></span> <span data-ttu-id="b9847-110">Wenn dies der Fall ist, sollten Sie keinen Klassen Anbieter erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="b9847-110">If this is the case, you should not have to create a class provider.</span></span> <span data-ttu-id="b9847-111">Stattdessen können Sie Ihre Klassendefinitionen mithilfe der WMI-API oder einer MOF-Datei im WMI-Repository platzieren.</span><span class="sxs-lookup"><span data-stu-id="b9847-111">Instead, you can place your class definitions in the WMI repository using the WMI API or a MOF file.</span></span>

<span data-ttu-id="b9847-112">Im folgenden Verfahren wird beschrieben, wie ein Klassen Anbieter implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="b9847-112">The following procedure describes how to implement a class provider.</span></span>

<span data-ttu-id="b9847-113">**So implementieren Sie einen Klassen Anbieter**</span><span class="sxs-lookup"><span data-stu-id="b9847-113">**To implement a class provider**</span></span>

1.  <span data-ttu-id="b9847-114">Stellen Sie fest, ob es sich bei dem Anbieter um einen Push-oder Pull</span><span class="sxs-lookup"><span data-stu-id="b9847-114">Determine if your provider is a push or pull provider.</span></span>

    <span data-ttu-id="b9847-115">Ein Pull-Anbieter stellt Daten dynamisch als Reaktion auf eine Anwendungsanforderung bereit, während pushanbieter Ihre Daten im WMI-Repository einmal speichern.</span><span class="sxs-lookup"><span data-stu-id="b9847-115">A pull provider supplies data dynamically in response to an application request, whereas push providers store their data once in the WMI repository.</span></span> <span data-ttu-id="b9847-116">Weitere Informationen finden Sie unter [bestimmen des Push-oder Pull-Status](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="b9847-116">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

2.  <span data-ttu-id="b9847-117">Entwerfen und registrieren Sie den Klassen Anbieter bei WMI.</span><span class="sxs-lookup"><span data-stu-id="b9847-117">Design and register your class provider with WMI.</span></span>

    <span data-ttu-id="b9847-118">Klassen Anbieter registrieren sich bei WMI, indem Sie eine [**\_ \_ Win32Provider**](--win32provider.md) -Instanz und eine [**\_ \_ classproviderregistration**](--classproviderregistration.md) -Instanz erstellen.</span><span class="sxs-lookup"><span data-stu-id="b9847-118">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_ClassProviderRegistration**](--classproviderregistration.md) instance.</span></span> <span data-ttu-id="b9847-119">Weitere Informationen finden Sie unter [Registrieren eines Klassen Anbieters](registering-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b9847-119">For more information, see [Registering a Class Provider](registering-a-class-provider.md).</span></span>

3.  <span data-ttu-id="b9847-120">Implementieren Sie die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle für Ihren Anbieter.</span><span class="sxs-lookup"><span data-stu-id="b9847-120">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="b9847-121">WMI verwendet [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) , um einen Anbieter zu laden und zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b9847-121">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="b9847-122">Wenn Sie einen pushanbieter entwerfen, ist **iwbemproviderinit** die einzige Schnittstelle, die Sie implementieren werden.</span><span class="sxs-lookup"><span data-stu-id="b9847-122">If you are designing a push provider, **IWbemProviderInit** is the only interface you will implement.</span></span> <span data-ttu-id="b9847-123">Weitere Informationen finden Sie unter [Initialisieren eines Anbieters](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b9847-123">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="b9847-124">Klassen Anbietern wird dringend empfohlen, das Multithreading-Modell "both" zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9847-124">Class providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

4.  <span data-ttu-id="b9847-125">Fügen Sie zusätzlichen Code hinzu, der für Ihren Anbieter erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b9847-125">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="b9847-126">Wenn Sie Ihren Anbieter entwerfen, müssen Sie wahrscheinlich WMI-Schnittstellen abrufen.</span><span class="sxs-lookup"><span data-stu-id="b9847-126">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="b9847-127">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md) und Verwalten von [Sicherheitsstufen in einem Anbieter](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="b9847-127">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="b9847-128">Beim Abrufen von Informationen für einen Client müssen Sie möglicherweise auf die Sicherheitsebenen für diesen Client zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b9847-128">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="b9847-129">Weitere Informationen finden Sie unter Annehmen der Identität [eines Clients](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="b9847-129">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="b9847-130">Implementieren Sie die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle für Ihren Anbieter.</span><span class="sxs-lookup"><span data-stu-id="b9847-130">Implement the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface for your provider.</span></span>

    <span data-ttu-id="b9847-131">Die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle ist die primäre Schnittstelle für einen Pull-Klassen Anbieter.</span><span class="sxs-lookup"><span data-stu-id="b9847-131">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for a pull class provider.</span></span> <span data-ttu-id="b9847-132">Weitere Informationen finden Sie unter [Implementieren der primären Schnittstelle für einen Klassen Anbieter](implementing-the-primary-interface-for-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b9847-132">For more information, see [Implementing the Primary Interface for a Class Provider](implementing-the-primary-interface-for-a-class-provider.md).</span></span>

6.  <span data-ttu-id="b9847-133">Ersetzen Sie den bereits vorhandenen Anbieter durch den neuen Code.</span><span class="sxs-lookup"><span data-stu-id="b9847-133">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="b9847-134">Sie müssen diesen Schritt nicht ausführen, wenn Sie nicht über einen vorhandenen Anbieter verfügen, der kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9847-134">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="b9847-135">Weitere Informationen finden Sie unter [Aktualisieren eines Anbieters](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b9847-135">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



