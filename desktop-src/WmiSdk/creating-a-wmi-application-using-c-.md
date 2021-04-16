---
description: 'So erstellen Sie eine Anwendung für WMI mithilfe von C++: Sie müssen com initialisieren, auf WMI-Protokolle zugreifen und diese festlegen und eine manuelle Bereinigung durchführen.'
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: Erstellen einer WMI-Anwendung mithilfe von C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baaa4f7e79828b2cb6cb496254d906182ff611ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348408"
---
# <a name="creating-a-wmi-application-using-c"></a><span data-ttu-id="7d96c-103">Erstellen einer WMI-Anwendung mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="7d96c-103">Creating a WMI Application Using C++</span></span>

<span data-ttu-id="7d96c-104">So erstellen Sie eine Anwendung für WMI mithilfe von C++: Sie müssen com initialisieren, auf WMI-Protokolle zugreifen und diese festlegen und eine manuelle Bereinigung durchführen.</span><span class="sxs-lookup"><span data-stu-id="7d96c-104">To create an application for WMI using C++: you must initialize COM, access and set WMI protocols, and perform a manual cleanup.</span></span> <span data-ttu-id="7d96c-105">C++ bietet jedoch den Vorteil von Flexibilität und Leistung.</span><span class="sxs-lookup"><span data-stu-id="7d96c-105">However, C++ does have the advantage of flexibility and power.</span></span> <span data-ttu-id="7d96c-106">Obwohl Sie in der Verwendung von Visual Basic Scripting Edition (VBScript) oder Windows PowerShell für einfache Prozesse besser tätig sind, funktioniert C++ besser für anspruchsvollere Anwendungen und ist für das Schreiben von [Anbietern](providing-data-to-wmi.md)erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7d96c-106">Therefore, while you are better served in using Visual Basic Scripting Edition (VBScript) or Windows PowerShell for simple processes, C++ works better for more sophisticated applications and is required for writing [providers](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="7d96c-107">Im folgenden Verfahren wird beschrieben, wie eine WMI-Anwendung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7d96c-107">The following procedure describes how to create a WMI application.</span></span>

<span data-ttu-id="7d96c-108">**So erstellen Sie eine WMI-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="7d96c-108">**To create a WMI application**</span></span>

1.  <span data-ttu-id="7d96c-109">[Initialisieren von com](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="7d96c-109">[Initialize COM](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="7d96c-110">Da WMI auf der com-Technologie basiert, müssen Sie Aufrufe an die Funktionen [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ausführen, um auf WMI zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="7d96c-110">Because WMI is based on COM technology, you must perform calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions to access WMI.</span></span>

2.  <span data-ttu-id="7d96c-111">[Erstellen Sie eine Verbindung mit einem WMI-Namespace](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="7d96c-111">[Create a connection to a WMI namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

    <span data-ttu-id="7d96c-112">Definitionsgemäß wird WMI in einem anderen Prozess ausgeführt als die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7d96c-112">By definition, WMI runs in a different process than your application.</span></span> <span data-ttu-id="7d96c-113">Daher müssen Sie eine Verbindung zwischen Ihrer Anwendung und WMI herstellen.</span><span class="sxs-lookup"><span data-stu-id="7d96c-113">Therefore, you must create a connection between your application and WMI.</span></span>

3.  <span data-ttu-id="7d96c-114">[Legen Sie die Sicherheitsstufen für die WMI-Verbindung fest](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7d96c-114">[Set the security levels on the WMI connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

    <span data-ttu-id="7d96c-115">Um die Verbindung zu verwenden, die Sie mit WMI erstellt haben, müssen Sie die Identitätswechsel-und Authentifizierungs Ebenen für die Anwendung festlegen.</span><span class="sxs-lookup"><span data-stu-id="7d96c-115">To use the connection you create to WMI, you must set the impersonation and authentication levels for your application.</span></span>

4.  <span data-ttu-id="7d96c-116">Implementieren Sie den Zweck Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7d96c-116">Implement the purpose of your application.</span></span>

    <span data-ttu-id="7d96c-117">WMI macht eine Vielzahl von COM-Schnittstellen verfügbar, die für den Zugriff und die Bearbeitung von Daten im gesamten Unternehmen</span><span class="sxs-lookup"><span data-stu-id="7d96c-117">WMI exposes a variety of COM interfaces use to access and manipulate data across your enterprise.</span></span> <span data-ttu-id="7d96c-118">Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md), [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md)und [com-API für WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="7d96c-118">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Receiving a WMI Event](receiving-a-wmi-event.md), and [COM API for WMI](com-api-for-wmi.md).</span></span>

    <span data-ttu-id="7d96c-119">An dieser Stelle sollte der Großteil der WMI-Client Anwendung vorhanden sein, z. b. der Zugriff auf WMI-Objekte oder die Datenbearbeitung.</span><span class="sxs-lookup"><span data-stu-id="7d96c-119">This is where the bulk of your WMI client application should exist, such as accessing WMI objects or manipulating data.</span></span>

5.  <span data-ttu-id="7d96c-120">[Bereinigen Sie Ihre Anwendung, und](cleaning-up-and-shutting-down-a-wmi-application.md)fahren Sie Sie herunter.</span><span class="sxs-lookup"><span data-stu-id="7d96c-120">[Cleanup and shut down your application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

    <span data-ttu-id="7d96c-121">Nachdem Sie die WMI-Abfragen durchgeführt haben, sollten Sie alle com-Zeiger zerstören und die Anwendung ordnungsgemäß herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="7d96c-121">After you complete your queries to WMI, you should destroy all COM pointers and shut down your application correctly.</span></span>

<span data-ttu-id="7d96c-122">Weitere Informationen und ein Codebeispiel zum Erstellen einer WMI-Anwendung finden Sie unter [Beispiel: Erstellen einer WMI-Anwendung](example-creating-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="7d96c-122">For more information and a code example about how to create a WMI application, see [Example: Creating a WMI Application](example-creating-a-wmi-application.md).</span></span>

 

 
