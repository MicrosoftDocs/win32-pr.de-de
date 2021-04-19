---
description: Ein Methoden Anbieter ermöglicht dem WMI-Zugriff auf die Methoden einer Klasse. Beispielsweise kann eine-Klasse, die eine Anwendung darstellt, über eine-Methode verfügen, die die Anwendung beendet.
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: Schreiben eines Methoden Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8626e2e16fe5424a0b05df81e2444a72ecb8841f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345270"
---
# <a name="writing-a-method-provider"></a><span data-ttu-id="c4a40-104">Schreiben eines Methoden Anbieters</span><span class="sxs-lookup"><span data-stu-id="c4a40-104">Writing a Method Provider</span></span>

<span data-ttu-id="c4a40-105">Ein Methoden Anbieter ermöglicht dem WMI-Zugriff auf die Methoden einer Klasse.</span><span class="sxs-lookup"><span data-stu-id="c4a40-105">A method provider allows WMI access to the methods of a class.</span></span> <span data-ttu-id="c4a40-106">Beispielsweise kann eine-Klasse, die eine Anwendung darstellt, über eine-Methode verfügen, die die Anwendung beendet.</span><span class="sxs-lookup"><span data-stu-id="c4a40-106">For example, a class that represents an application may have a method that terminates the application.</span></span>

<span data-ttu-id="c4a40-107">Das Ändern der Reihenfolge der Eingabe-und Ausgabeparameter der Methode beim Aktualisieren eines vorhandenen Methoden Anbieters kann zu Fehlern bei Anwendungen führen, die die-Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="c4a40-107">Changing the order of method input and output parameters when updating an existing method provider can cause failure for applications that call the method.</span></span> <span data-ttu-id="c4a40-108">Die Reihenfolge der Eingabe-oder Ausgabeparameter wird durch den Wert des [**ID**](standard-wmi-qualifiers.md) -Qualifizierers für jeden Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c4a40-108">The order of the input or output parameters is established by the value of the [**ID**](standard-wmi-qualifiers.md) qualifier on each parameter.</span></span> <span data-ttu-id="c4a40-109">Der erste Parameter hat den **ID** -Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c4a40-109">The first parameter has an **ID** value of zero.</span></span> <span data-ttu-id="c4a40-110">Fügen Sie am Ende der vorhandenen Parameter neue Eingabeparameter hinzu, anstatt Sie in die bereits festgelegte Sequenz einzufügen.</span><span class="sxs-lookup"><span data-stu-id="c4a40-110">Add new input parameters at the end of the existing parameters rather than inserting them in the already established sequence.</span></span>

<span data-ttu-id="c4a40-111">Im folgenden Verfahren wird beschrieben, wie ein Methoden Anbieter implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="c4a40-111">The following procedure describes how to implement a method provider.</span></span>

<span data-ttu-id="c4a40-112">**So implementieren Sie einen Methoden Anbieter**</span><span class="sxs-lookup"><span data-stu-id="c4a40-112">**To implement a method provider**</span></span>

1.  <span data-ttu-id="c4a40-113">Entwerfen und registrieren Sie den Klassen Anbieter bei WMI.</span><span class="sxs-lookup"><span data-stu-id="c4a40-113">Design and register your class provider with WMI.</span></span>

    <span data-ttu-id="c4a40-114">Klassen Anbieter werden bei WMI registriert, indem eine [**\_ \_ Win32Provider**](--win32provider.md) -Instanz und eine [**\_ \_ methodproviderregistration**](--methodproviderregistration.md) -Klasse erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c4a40-114">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class.</span></span> <span data-ttu-id="c4a40-115">Weitere Informationen finden Sie unter [Registrieren eines Methoden Anbieters](registering-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c4a40-115">For more information, see [Registering a Method Provider](registering-a-method-provider.md).</span></span>

2.  <span data-ttu-id="c4a40-116">Implementieren Sie die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle für Ihren Anbieter.</span><span class="sxs-lookup"><span data-stu-id="c4a40-116">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    > [!Note]  
    > <span data-ttu-id="c4a40-117">Methoden Anbietern wird dringend empfohlen, das Multithreading-Modell "both" zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4a40-117">Method providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="c4a40-118">Implementieren Sie die [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) -Methode für Ihren Anbieter.</span><span class="sxs-lookup"><span data-stu-id="c4a40-118">Implement the [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) method for your provider.</span></span>

    <span data-ttu-id="c4a40-119">Die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle ist die primäre Schnittstelle für einen Methoden Anbieter.</span><span class="sxs-lookup"><span data-stu-id="c4a40-119">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for a method provider.</span></span> <span data-ttu-id="c4a40-120">Weitere Informationen finden Sie unter [Implementieren der primären Schnittstelle für einen Methoden Anbieter](implementing-the-primary-interface-for-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c4a40-120">For more information, see [Implementing the Primary Interface for a Method Provider](implementing-the-primary-interface-for-a-method-provider.md).</span></span>

4.  <span data-ttu-id="c4a40-121">Fügen Sie zusätzlichen Code hinzu, der für Ihren Anbieter erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c4a40-121">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="c4a40-122">Wenn Sie Ihren Anbieter entwerfen, müssen Sie wahrscheinlich WMI-Schnittstellen abrufen.</span><span class="sxs-lookup"><span data-stu-id="c4a40-122">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="c4a40-123">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md) und Verwalten von [Sicherheitsstufen in einem Anbieter](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="c4a40-123">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="c4a40-124">Beim Abrufen von Informationen für einen Client müssen Sie möglicherweise auf die Sicherheitsebenen für diesen Client zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c4a40-124">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="c4a40-125">Weitere Informationen finden Sie unter Annehmen der Identität [eines Clients](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="c4a40-125">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="c4a40-126">Ersetzen Sie den bereits vorhandenen Anbieter durch den neuen Code.</span><span class="sxs-lookup"><span data-stu-id="c4a40-126">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="c4a40-127">Sie müssen diesen Schritt nicht ausführen, wenn Sie nicht über einen vorhandenen Anbieter verfügen, der kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4a40-127">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="c4a40-128">Weitere Informationen finden Sie unter [Aktualisieren eines Anbieters](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c4a40-128">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



