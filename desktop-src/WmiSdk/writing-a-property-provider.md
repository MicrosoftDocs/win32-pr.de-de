---
description: Ein Eigenschaften Anbieter ruft einzelne Eigenschaftswerte für Instanzen einer bestimmten Klasse ab, die im WMI-Repository gespeichert sind, und ändert Sie.
ms.assetid: fe150157-cf9d-47da-8f94-b18eb0502bd8
ms.tgt_platform: multiple
title: Schreiben eines Eigenschaften Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bf22d927435b5c46f0ec8d8d2cf42ab872a0c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351724"
---
# <a name="writing-a-property-provider"></a><span data-ttu-id="24c96-103">Schreiben eines Eigenschaften Anbieters</span><span class="sxs-lookup"><span data-stu-id="24c96-103">Writing a Property Provider</span></span>

<span data-ttu-id="24c96-104">Ein Eigenschaften Anbieter ruft einzelne Eigenschaftswerte für Instanzen einer bestimmten Klasse ab, die im WMI-Repository gespeichert sind, und ändert Sie.</span><span class="sxs-lookup"><span data-stu-id="24c96-104">A property provider retrieves and modifies individual property values for instances of a given class that is stored in the WMI repository.</span></span>

<span data-ttu-id="24c96-105">Im folgenden Verfahren wird beschrieben, wie ein Eigenschaften Anbieter erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="24c96-105">The following procedure describes how to create a property provider.</span></span>

<span data-ttu-id="24c96-106">**So erstellen Sie einen Eigenschaften Anbieter**</span><span class="sxs-lookup"><span data-stu-id="24c96-106">**To create a property provider**</span></span>

1.  <span data-ttu-id="24c96-107">Entwerfen und registrieren Sie Ihren Anbieter bei WMI.</span><span class="sxs-lookup"><span data-stu-id="24c96-107">Design and register your provider with WMI.</span></span>

    <span data-ttu-id="24c96-108">Instanzanbieter registrieren sich bei WMI, indem Sie eine [**\_ \_ Win32Provider**](--win32provider.md) -Instanz und eine [**\_ \_ propertyproviderregistration**](--propertyproviderregistration.md) -Klasse erstellen.</span><span class="sxs-lookup"><span data-stu-id="24c96-108">Instance providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class.</span></span> <span data-ttu-id="24c96-109">Weitere Informationen finden Sie unter [Registrieren eines Eigenschaften Anbieters](registering-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="24c96-109">For more information, see [Registering a Property Provider](registering-a-property-provider.md).</span></span>

2.  <span data-ttu-id="24c96-110">Implementieren Sie die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle für Ihren Anbieter.</span><span class="sxs-lookup"><span data-stu-id="24c96-110">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="24c96-111">WMI verwendet [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) , um einen Anbieter zu laden und zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="24c96-111">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="24c96-112">Dies ist eine Aufgabe, die allen Anbietern gemeinsam ist.</span><span class="sxs-lookup"><span data-stu-id="24c96-112">This is a task common to all providers.</span></span> <span data-ttu-id="24c96-113">Weitere Informationen finden Sie unter [Initialisieren eines Anbieters](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="24c96-113">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="24c96-114">Eigenschafts Anbietern wird dringend empfohlen, das Multithreading-Modell "both" zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="24c96-114">Property providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="24c96-115">Implementieren Sie die [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) -Schnittstelle für Ihren Anbieter.</span><span class="sxs-lookup"><span data-stu-id="24c96-115">Implement the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interface for your provider.</span></span>

    <span data-ttu-id="24c96-116">Die [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) -Schnittstelle ist die primäre Schnittstelle für einen Eigenschaften Anbieter.</span><span class="sxs-lookup"><span data-stu-id="24c96-116">The [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interface is the primary interface for a property provider.</span></span> <span data-ttu-id="24c96-117">Die zwei Hauptmethoden sind [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) und [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty).</span><span class="sxs-lookup"><span data-stu-id="24c96-117">The two main methods are [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) and [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty).</span></span> <span data-ttu-id="24c96-118">Weitere Informationen finden Sie unter [Implementieren der primären Schnittstelle für einen Eigenschaften Anbieter](implementing-the-primary-interface-for-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="24c96-118">For more information, see [Implementing the Primary Interface for a Property Provider](implementing-the-primary-interface-for-a-property-provider.md).</span></span>

4.  <span data-ttu-id="24c96-119">Fügen Sie zusätzlichen Code hinzu, der für Ihren Anbieter erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="24c96-119">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="24c96-120">Wenn Sie Ihren Anbieter entwerfen, müssen Sie wahrscheinlich WMI-Schnittstellen abrufen.</span><span class="sxs-lookup"><span data-stu-id="24c96-120">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="24c96-121">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md) und Verwalten von [Sicherheitsstufen in einem Anbieter](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="24c96-121">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="24c96-122">Beim Abrufen von Informationen für einen Client müssen Sie möglicherweise auf die Sicherheitsebenen für diesen Client zugreifen.</span><span class="sxs-lookup"><span data-stu-id="24c96-122">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="24c96-123">Weitere Informationen finden Sie unter Annehmen der Identität [eines Clients](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="24c96-123">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="24c96-124">Ersetzen Sie den bereits vorhandenen Anbieter durch den neuen Code.</span><span class="sxs-lookup"><span data-stu-id="24c96-124">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="24c96-125">Sie müssen diesen Schritt nicht ausführen, wenn Sie nicht über einen vorhandenen Anbieter verfügen, der kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="24c96-125">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="24c96-126">Weitere Informationen finden Sie unter [Aktualisieren eines Anbieters](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="24c96-126">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



