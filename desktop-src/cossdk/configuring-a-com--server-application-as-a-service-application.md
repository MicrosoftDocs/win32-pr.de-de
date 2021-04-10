---
description: Eine COM+-Serveranwendung kann als Dienst erstellt werden, um entweder automatisch während des Systemstarts oder manuell durch Aktivierungen gestartet zu werden.
ms.assetid: 56487746-328d-4435-af58-368aaa15b32a
title: Konfigurieren einer com+-Server Anwendung als Dienst Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b3bbf8b691221590d6588c48dbef5198772439
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860852"
---
# <a name="configuring-a-com-server-application-as-a-service-application"></a><span data-ttu-id="94184-103">Konfigurieren einer com+-Server Anwendung als Dienst Anwendung</span><span class="sxs-lookup"><span data-stu-id="94184-103">Configuring a COM+ Server Application as a Service Application</span></span>

<span data-ttu-id="94184-104">Eine COM+-Serveranwendung kann als Dienst erstellt werden, um entweder automatisch während des Systemstarts oder manuell durch Aktivierungen gestartet zu werden.</span><span class="sxs-lookup"><span data-stu-id="94184-104">A COM+ server application can be created as a service to start either automatically during the system startup or manually by activations.</span></span> <span data-ttu-id="94184-105">Wenn der Dienst nicht gestartet werden kann, gibt die Option für die Fehlerbehandlung den Schweregrad des Fehlers an und legt fest, welche Aktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="94184-105">If the service fails to start, the option for error handling specifies the severity of the error and determines the action to be taken.</span></span> <span data-ttu-id="94184-106">Die Option zum Konfigurieren eines Dienstanbieter, der als lokales Systemkonto ausgeführt werden soll, ist ebenfalls verfügbar, und die Option zum Zuweisen eines bestimmten Benutzerkontos, für das die COM+-Serveranwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94184-106">The option to configure a service to run as the local system account is also available, as well as the option to assign a specific user account for which the COM+ server application will run.</span></span> <span data-ttu-id="94184-107">Abhängigkeiten können auch in einer Liste der Dienste ausgewählt werden, die mithilfe von Komponenten Diensten auf dem Computer registriert sind.</span><span class="sxs-lookup"><span data-stu-id="94184-107">Dependencies can also be selected from a list of services registered on the computer using Component Services.</span></span> <span data-ttu-id="94184-108">Dadurch wird festgelegt, welche Dienste vor dem Start dieses Diensts ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="94184-108">This will determine which services must be executed before this service is started.</span></span>

<span data-ttu-id="94184-109">**So konfigurieren Sie eine COM+-Anwendung für die Durchführung als Dienst**</span><span class="sxs-lookup"><span data-stu-id="94184-109">**To configure a COM+ application to run as a service**</span></span>

1.  <span data-ttu-id="94184-110">Suchen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste die COM+-Serveranwendung, die Sie als Dienst ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="94184-110">In the console tree of the Component Services administrative tool, locate the COM+ server application you want to run as a service.</span></span>

2.  <span data-ttu-id="94184-111">Klicken Sie mit der rechten Maustaste auf die Anwendung com+ Server, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="94184-111">Right-click the COM+ server application, and then click **Properties**.</span></span>

3.  <span data-ttu-id="94184-112">Klicken Sie im Dialogfeld **Eigenschaften** auf die Registerkarte **Aktivierung** .</span><span class="sxs-lookup"><span data-stu-id="94184-112">In the **Properties** dialog box, click the **Activation** tab.</span></span>

4.  <span data-ttu-id="94184-113">Aktivieren Sie im Feld **Aktivierungstyp** das Kontrollkästchen **Anwendung als NT-Dienst ausführen** .</span><span class="sxs-lookup"><span data-stu-id="94184-113">In the **Activation type** box, check the **Run application as NT Service** check box.</span></span>

    > [!Note]  
    > <span data-ttu-id="94184-114">Das Kontrollkästchen **Anwendung als NT-Dienst ausführen** ist nur für Server Anwendungen aktiviert und für Bibliotheksanwendungen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="94184-114">The **Run application as NT Service** check box is enabled only for server applications and is disabled for library applications.</span></span>

     

5.  <span data-ttu-id="94184-115">Klicken Sie auf die Schaltfläche **neuen Dienst einrichten** .</span><span class="sxs-lookup"><span data-stu-id="94184-115">Click the **Setup New Service** button.</span></span>

6.  <span data-ttu-id="94184-116">Wählen Sie im Feld **Starttyp** im Dialogfeld **Dienst Name** die Option **automatisch** oder **manuell** aus.</span><span class="sxs-lookup"><span data-stu-id="94184-116">In the **Startup type** box in the **Service Name** dialog box, select **Automatic** or **Manual**.</span></span>

7.  <span data-ttu-id="94184-117">Optionale Um die Aktion anzugeben, die für einen bestimmten Fehler ausgeführt werden soll, wählen Sie im Feld **Fehlerbehandlung** die Option **ignorieren**, **Normal**, **schwerwiegend** oder **kritisch** aus.</span><span class="sxs-lookup"><span data-stu-id="94184-117">(Optional) To specify the action to be taken for a particular error, select **Ignore**, **Normal**, **Severe**, or **Critical** in the **Error Handling** box.</span></span> <span data-ttu-id="94184-118">Die einzelnen Optionen zugeordneten Verhalten lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="94184-118">The behavior associated with each option is as follows:</span></span>

    1.  <span data-ttu-id="94184-119">**Ignore** (Ignorieren):</span><span class="sxs-lookup"><span data-stu-id="94184-119">**Ignore**.</span></span> <span data-ttu-id="94184-120">Der Fehler wird vom Start Programm protokolliert, aber der Startvorgang wird fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="94184-120">The startup program logs the error but continues the startup operation.</span></span>
    2.  <span data-ttu-id="94184-121">**Normal**.</span><span class="sxs-lookup"><span data-stu-id="94184-121">**Normal**.</span></span> <span data-ttu-id="94184-122">Der Fehler wird protokolliert, ein Meldungs Feld wird angezeigt, und der Startvorgang wird vom Start Programm fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="94184-122">The error is logged, a message box is displayed, and the startup program continues the startup operation.</span></span>
    3.  <span data-ttu-id="94184-123">**Schwerwiegend**.</span><span class="sxs-lookup"><span data-stu-id="94184-123">**Severe**.</span></span> <span data-ttu-id="94184-124">Der Fehler wird protokolliert, und das System wird mit der letzten als funktionierend bekannten Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="94184-124">The error is logged, and the system is restarted with the last known good configuration.</span></span> <span data-ttu-id="94184-125">Wenn es sich um die letzte bekannte, gute Konfiguration handelt, die beim Protokollieren des Fehlers gestartet wird, wird der Startvorgang fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="94184-125">If it is the last known good configuration that is being started when the error is logged, the startup operation continues.</span></span>
    4.  <span data-ttu-id="94184-126">**Kritisch**.</span><span class="sxs-lookup"><span data-stu-id="94184-126">**Critical**.</span></span> <span data-ttu-id="94184-127">Der Fehler wird protokolliert, und das System wird mit der letzten als funktionierend bekannten Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="94184-127">The error is logged, and the system is restarted with the last known good configuration.</span></span> <span data-ttu-id="94184-128">Wenn es sich um die letzte als funktionierend bekannte Konfiguration handelt, die beim Protokollieren des Fehlers gestartet wird, tritt beim Startvorgang ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="94184-128">If it is the last known good configuration that is being started when the error is logged, the startup operation fails.</span></span>

8.  <span data-ttu-id="94184-129">Optionale Um andere Dienste als abhängig festzulegen, wählen Sie die abhängigen Dienste aus der Liste im Feld **Abhängigkeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="94184-129">(Optional) To set other services as dependent, select the dependent services from the list in the **Dependencies** box.</span></span>

9.  <span data-ttu-id="94184-130">Optionale Aktivieren Sie das Kontrollkästchen **Dienst für die Interaktion mit dem Desktop zulassen** , um anzugeben, dass der Dienst mit dem Desktop interagieren darf.</span><span class="sxs-lookup"><span data-stu-id="94184-130">(Optional) To indicate that the service should be allowed to interact with the desktop, check the **Allow service to interact with desktop** check box.</span></span>

10. <span data-ttu-id="94184-131">Klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="94184-131">Click **Create**.</span></span>

11. <span data-ttu-id="94184-132">Optionale So weisen Sie den Dienst einem Benutzerkonto zu:</span><span class="sxs-lookup"><span data-stu-id="94184-132">(Optional) To assign the service to a user account:</span></span>

    1.  <span data-ttu-id="94184-133">Wählen Sie auf der Registerkarte **Identität** den **Benutzer** aus.</span><span class="sxs-lookup"><span data-stu-id="94184-133">In the **Identity** tab, select **This user**.</span></span>
    2.  <span data-ttu-id="94184-134">Geben Sie den Benutzernamen in das Feld **Benutzer** ein, oder klicken Sie auf die Schaltfläche **Durchsuchen** , um den Benutzer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="94184-134">To select the user, enter the user name in the **User** box or click the **Browse** button.</span></span>
    3.  <span data-ttu-id="94184-135">Geben Sie im Feld **Kennwort** das Kennwort für das Benutzerkonto ein.</span><span class="sxs-lookup"><span data-stu-id="94184-135">Enter the password for the user account in the **Password** box.</span></span>
    4.  <span data-ttu-id="94184-136">Geben Sie das gleiche Kennwort in das Feld **Kennwort bestätigen** ein.</span><span class="sxs-lookup"><span data-stu-id="94184-136">Enter the same password in the **Confirm Password** box.</span></span>

 

 



