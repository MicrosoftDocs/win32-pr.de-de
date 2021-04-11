---
description: Der Hersteller Wrapper dient dazu, die COM-Schnittstellen auf niedriger Ebene (die von den Smartcardherstellern bereitgestellt werden) für eine bestimmte Smartcard zu kapseln und zu verwenden. Diese Schnittstellen werden nicht von Microsoft bereitgestellt.
ms.assetid: 7bc26f7b-c355-448a-9f23-4ccfffea2fef
title: Anbieter-Wrapper Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b7d22fea8e450111e1611f2ec069697c229a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128905"
---
# <a name="vendor-wrapper-service-provider"></a><span data-ttu-id="a8506-104">Anbieter-Wrapper Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a8506-104">Vendor Wrapper Service Provider</span></span>

<span data-ttu-id="a8506-105">Der Hersteller Wrapper dient dazu, die COM-Schnittstellen auf niedriger Ebene (die von den Smartcardherstellern bereitgestellt werden) für eine bestimmte Smartcard zu kapseln und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a8506-105">The purpose of the vendor wrapper is to encapsulate and use the low-level COM interfaces (supplied by the smart card manufacturers) for a particular smart card.</span></span> <span data-ttu-id="a8506-106">Diese Schnittstellen werden nicht von Microsoft bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a8506-106">These interfaces are not supplied by Microsoft.</span></span>

![Hersteller Wrapper](images/scspart1.png)

<span data-ttu-id="a8506-108">Wie in Teil 6 der *Interoperabilitäts Spezifikation für ICCS und Personal Computer Systeme* (siehe Spezifikationen unter [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ) beschrieben, ist die Funktionalität, die von diesem Wrapper verfügbar gemacht wird, einfacher zu verwenden als die Funktionalität von vier separaten Dienstanbietern.</span><span class="sxs-lookup"><span data-stu-id="a8506-108">As described in part 6 of the *Interoperability Specification for ICCs and Personal Computer Systems* (see specifications at [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/)), the functionality exposed by this wrapper is easier to use than the functionality of four separate service providers.</span></span> <span data-ttu-id="a8506-109">Die Wrapper Funktion kann in vier Hauptbereiche unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="a8506-109">The wrapper's functionality can be divided into four main areas:</span></span>

-   <span data-ttu-id="a8506-110">Dienste für die Smartcard-Authentifizierung, z. b. Get Challenge und Card Authentication.</span><span class="sxs-lookup"><span data-stu-id="a8506-110">Smart card authentication services, such as get challenge and card authentication.</span></span>
-   <span data-ttu-id="a8506-111">Zugriff auf smartcarddateien oder Dateisystem Dienste, z. b. öffnen, schließen, lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="a8506-111">Smart card file access or file system services, such as open, close, read, and write.</span></span>
-   <span data-ttu-id="a8506-112">Smartcardverwaltung, z. b. Anfügen und trennen.</span><span class="sxs-lookup"><span data-stu-id="a8506-112">Smart card management, such as attach and detach.</span></span>
-   <span data-ttu-id="a8506-113">Smartcard-Überprüfungs Dienste, z. b. überprüfen und Ändern von Code.</span><span class="sxs-lookup"><span data-stu-id="a8506-113">Smart card verification services, such as verify and change code.</span></span>

> [!Note]  
> <span data-ttu-id="a8506-114">Diese Spezifikation ist möglicherweise in einigen Sprachen und Ländern oder Regionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a8506-114">This specification may not be available in some languages and countries or regions.</span></span>

 

<span data-ttu-id="a8506-115">Die Funktionalität ist spezifisch für den Typ der verwendeten Karte (die von der Karte unterstützten Funktionen, Protokolle usw.) und unterscheidet sich für jede Karte.</span><span class="sxs-lookup"><span data-stu-id="a8506-115">The functionality is specific to the type of card being used (which functions the card supports, protocols, and so on) and will be different for each card.</span></span>

<span data-ttu-id="a8506-116">Der Wrapper für den Microsoft scardcom-Beispiel verwendet die ATL-COM-Bibliothek, um einen einfachen Wrapper zu implementieren und eine Vorlage für andere Wrapper anzulegen.</span><span class="sxs-lookup"><span data-stu-id="a8506-116">The Microsoft SCardCOM example wrapper uses the ATL COM library to implement a simple wrapper and lay down a template for other wrappers.</span></span> <span data-ttu-id="a8506-117">Die folgenden Schnittstellen werden implementiert.</span><span class="sxs-lookup"><span data-stu-id="a8506-117">It implements the following interfaces.</span></span>



| <span data-ttu-id="a8506-118">Schnittstelle oder Objekt</span><span class="sxs-lookup"><span data-stu-id="a8506-118">Interface or object</span></span>                                     | <span data-ttu-id="a8506-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8506-119">Description</span></span>                         |
|---------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="a8506-120">**Iscardauth**</span><span class="sxs-lookup"><span data-stu-id="a8506-120">**ISCardAuth**</span></span>](iscardauth.md)<br/>             | <span data-ttu-id="a8506-121">Authentifizierungsdienste.</span><span class="sxs-lookup"><span data-stu-id="a8506-121">Authentication services.</span></span><br/> |
| [<span data-ttu-id="a8506-122">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="a8506-122">**ISCardFileAccess**</span></span>](iscardfileaccess.md)<br/> | <span data-ttu-id="a8506-123">Dateisystem Dienste.</span><span class="sxs-lookup"><span data-stu-id="a8506-123">File system services.</span></span><br/>    |
| [<span data-ttu-id="a8506-124">**Iscardmanage**</span><span class="sxs-lookup"><span data-stu-id="a8506-124">**ISCardManage**</span></span>](iscardmanage.md)<br/>         | <span data-ttu-id="a8506-125">Verwaltungsdienste.</span><span class="sxs-lookup"><span data-stu-id="a8506-125">Management services.</span></span><br/>     |
| [<span data-ttu-id="a8506-126">**Iscardverify**</span><span class="sxs-lookup"><span data-stu-id="a8506-126">**ISCardVerify**</span></span>](iscardverify.md)<br/>         | <span data-ttu-id="a8506-127">Überprüfungs Dienste.</span><span class="sxs-lookup"><span data-stu-id="a8506-127">Verification services.</span></span><br/>   |



 

> [!Note]  
> <span data-ttu-id="a8506-128">Das Beispiel "scardcom" wird nur als Beispiel für das Implementieren der Wrapper Schnittstellen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a8506-128">The SCardCOM example is provided only as an example of implementing the wrapper interfaces.</span></span> <span data-ttu-id="a8506-129">Um einen DLL-namens Konflikt mit anderen Anbietern zu vermeiden, dürfen Sie SCardCOM.dll nicht als Namen von DLLs verwenden, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8506-129">To prevent DLL name collision with other vendors, you must not use SCardCOM.dll as the name of any DLLs you create.</span></span>

 

<span data-ttu-id="a8506-130">Im folgenden finden Sie eine typische Verwendung des Hersteller Wrappers.</span><span class="sxs-lookup"><span data-stu-id="a8506-130">Following is a typical use of the vendor wrapper.</span></span> <span data-ttu-id="a8506-131">In diesem Beispiel wird die [**iscardmanage**](iscardmanage.md) -Schnittstelle verwendet, um Instanzen der Schnittstellen zu erstellen, die in den Dienstanbieter und die [**iscardverify**](iscardverify.md) -Schnittstelle integriert werden, um Ihren Vorgang zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a8506-131">This example uses the [**ISCardManage**](iscardmanage.md) interface to create instances of the interfaces that will be wrapped into the service provider and the [**ISCardVerify**](iscardverify.md) interface to verify their operation.</span></span>

<span data-ttu-id="a8506-132">**So erstellen Sie einen Wrapper Dienstanbieter**</span><span class="sxs-lookup"><span data-stu-id="a8506-132">**To build a wrapper service provider**</span></span>

1.  <span data-ttu-id="a8506-133">Erstellen Sie eine Instanz der [**iscardmanage**](iscardmanage.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a8506-133">Create an instance of the [**ISCardManage**](iscardmanage.md) interface.</span></span> <span data-ttu-id="a8506-134">Verwenden Sie diese Schnittstelle, um eine Instanz der erforderlichen Schnittstellen (z. b. [**iscardfileaccess**](iscardfileaccess.md) oder [**iscardverify**](iscardverify.md)) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8506-134">Use this interface to create an instance of required interfaces (for example, [**ISCardFileAccess**](iscardfileaccess.md) or [**ISCardVerify**](iscardverify.md)).</span></span> <span data-ttu-id="a8506-135">Wenn diese Schnittstellen erstellt werden, werden auch alle entsprechenden COM-Schnittstellen auf niedriger Ebene erstellt.</span><span class="sxs-lookup"><span data-stu-id="a8506-135">When creating these interfaces, any corresponding low-level COM interfaces would also be created.</span></span>
2.  <span data-ttu-id="a8506-136">Fügen Sie eine Karte mithilfe der entsprechenden [**iscardmanage**](iscardmanage.md) -Methode an/Stellen Sie eine Verbindung her.</span><span class="sxs-lookup"><span data-stu-id="a8506-136">Attach/connect to a card through the appropriate [**ISCardManage**](iscardmanage.md) method.</span></span>
3.  <span data-ttu-id="a8506-137">Führen Sie erforderliche Vorgänge über die entsprechende [**iscardverify**](iscardverify.md) -Methode aus (die möglicherweise mehrere COM-Schnittstellen auf niedriger Ebene aufruft, und Methoden zum Abschluss).</span><span class="sxs-lookup"><span data-stu-id="a8506-137">Perform required operations through the appropriate [**ISCardVerify**](iscardverify.md) method (which may call multiple low-level COM interfaces and methods to complete).</span></span>
4.  <span data-ttu-id="a8506-138">Wiederholen Sie dies für andere Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="a8506-138">Repeat for other operations.</span></span>
5.  <span data-ttu-id="a8506-139">Release nach Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="a8506-139">Release when complete.</span></span>

<span data-ttu-id="a8506-140">Der Name und der Schnittstellen Bezeichner (GUID) der COM-Schnittstelle dürfen sich nicht von den im Code-oder Beispiel Wrapper verwendeten Änderungen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="a8506-140">The COM interface name and interface identifier (GUID) should not change from those used in the code or example wrapper.</span></span> <span data-ttu-id="a8506-141">Allerdings muss die Klassen-GUID (d. h., in der sich eine tatsächliche Implementierung einer Schnittstelle befindet) von den verwendeten geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a8506-141">However, the class GUID (that is, where an actual implementation of an interface resides) must be changed from those used.</span></span> <span data-ttu-id="a8506-142">Dies ist besonders wichtig, wenn ein Hersteller Wrapper implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="a8506-142">This is especially important when implementing a vendor wrapper.</span></span> <span data-ttu-id="a8506-143">Ein Beispiel wäre die Verwendung mehrerer Hersteller-Wrapper auf einem bestimmten Computer.</span><span class="sxs-lookup"><span data-stu-id="a8506-143">One example would be using multiple vendor wrappers on a particular computer.</span></span> <span data-ttu-id="a8506-144">Diese Wrapper sollten die gleichen com-Schnittstellen implementieren, verwenden jedoch immer verschiedene Implementierungs Strategien.</span><span class="sxs-lookup"><span data-stu-id="a8506-144">These wrappers should implement the same COM interfaces, but will always use different implementation strategies.</span></span> <span data-ttu-id="a8506-145">Daher sind verschiedene Klassen (und Klassen-IDs) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a8506-145">Therefore, different classes (and class IDs) are required.</span></span>

 

 




