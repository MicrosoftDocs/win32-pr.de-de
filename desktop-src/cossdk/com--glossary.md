---
description: Glossarseite
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26a72de1-24bc-41e6-8d41-61d45f581e51
title: Com+-Glossar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b5a6cb30529cd8b97b8cf11316347d68003e32c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483158"
---
# <a name="com-glossary"></a><span data-ttu-id="1d824-103">Com+-Glossar</span><span class="sxs-lookup"><span data-stu-id="1d824-103">COM+ Glossary</span></span>

<dl> <dt>

<span data-ttu-id="1d824-104"><span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**Zugriffs Token**</span><span class="sxs-lookup"><span data-stu-id="1d824-104"><span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**access token**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-105">Ein-Objekt, das den Sicherheitskontext eines Prozesses oder Threads beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1d824-105">An object that describes the security context of a process or thread.</span></span> <span data-ttu-id="1d824-106">Die Informationen in einem Token enthalten die Identität und die Berechtigungen des dem Prozess oder Thread zugeordneten Benutzerkontos.</span><span class="sxs-lookup"><span data-stu-id="1d824-106">The information in a token includes the identity and privileges of the user account associated with the process or thread.</span></span> <span data-ttu-id="1d824-107">Wenn sich ein Benutzer anmeldet, überprüft das System das Kennwort des Benutzers, indem es mit in einer Sicherheitsdatenbank gespeicherten Informationen vergleicht.</span><span class="sxs-lookup"><span data-stu-id="1d824-107">When a user logs on, the system verifies the user's password by comparing it with information stored in a security database.</span></span> <span data-ttu-id="1d824-108">Wenn das Kennwort authentifiziert ist, erstellt das System ein Zugriffs Token.</span><span class="sxs-lookup"><span data-stu-id="1d824-108">If the password is authenticated, the system produces an access token.</span></span> <span data-ttu-id="1d824-109">Jeder Prozess, der für diesen Benutzer ausgeführt wird, verfügt über eine Kopie dieses Zugriffs Tokens.</span><span class="sxs-lookup"><span data-stu-id="1d824-109">Every process executed on behalf of this user has a copy of this access token.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-110"><span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**ACID-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="1d824-110"><span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**ACID properties**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-111">Ein Akronym, das von dem Transaktions Verarbeitungs Pionier für atomarisch, konsistent, isoliert und dauerhaft geprägt ist.</span><span class="sxs-lookup"><span data-stu-id="1d824-111">Acronym coined by transaction processing pioneers for atomic, consistent, isolated, and durable.</span></span> <span data-ttu-id="1d824-112">Diese Eigenschaften stellen ein vorhersagbares Verhalten sicher und verstärken die Rolle von Transaktionen als all-oder-None-Angebote, um konsistente und vorhersagbare Ergebnisse in einer verteilten Umgebung bereitzustellen, wenn unabhängige Fehler auftreten können.</span><span class="sxs-lookup"><span data-stu-id="1d824-112">These properties ensure predictable behavior, reinforcing the role of transactions as all-or-none propositions designed to provide consistent and predictable results in a distributed environment when independent failures can occur.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-113"><span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**Aktivierung**</span><span class="sxs-lookup"><span data-stu-id="1d824-113"><span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**activation**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-114">Die Kette der Ereignisse, die zur Erstellung eines COM-Objekts und zum Zurückgeben eines gültigen Zeigers auf eine Schnittstelle für dieses Objekt führt.</span><span class="sxs-lookup"><span data-stu-id="1d824-114">The chain of events that results in the creation of a COM object and the return of a valid pointer to an interface on that object.</span></span> <span data-ttu-id="1d824-115">In com+ wird ein Objekt entweder in einem eigenen Kontext oder in dessen Ersteller (ein Objekt, das das aktivierte Objekt angefordert hat) aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1d824-115">In COM+, an object gets activated either in its own context or in that of its creator (an object that has requested the object being activated).</span></span> <span data-ttu-id="1d824-116">Com+-Dienste basieren auf der geeigneten Aktivierung eines Objekts, das auf der Konfiguration des Objekts basiert.</span><span class="sxs-lookup"><span data-stu-id="1d824-116">COM+ services rely on appropriate activation of an object based on the object's configuration.</span></span> <span data-ttu-id="1d824-117">Im Verlauf der Aktivierung bestimmt das System den Kontext, in dem das Objekt ausgeführt wird, initialisiert die Kontexteigenschaften, überprüft Zugriffsberechtigungen und richtet eine Sicherheitsidentität ein.</span><span class="sxs-lookup"><span data-stu-id="1d824-117">In the course of activation, the system determines the context in which the object runs, initializes the context properties, checks access permissions, and establishes a security identity.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-118"><span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**Aktivierungs Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="1d824-118"><span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**activation security**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-119">Eine Form von Sicherheitsschutz, die bestimmt, wer einen Server starten kann.</span><span class="sxs-lookup"><span data-stu-id="1d824-119">A form of security protection that determines who can launch a server.</span></span> <span data-ttu-id="1d824-120">Die Aktivierungs Sicherheit wird automatisch durch den Dienststeuerungs-Manager (Service Control Manager, SCM) eines bestimmten Computers angewendet.</span><span class="sxs-lookup"><span data-stu-id="1d824-120">Activation security is automatically applied by the Service Control Manager (SCM) of a particular computer.</span></span> <span data-ttu-id="1d824-121">Beim Empfang einer Anforderung von einem Client zum Aktivieren eines Objekts prüft der SCM die Anforderung anhand der in der Registrierung gespeicherten Aktivierungs Sicherheitsinformationen.</span><span class="sxs-lookup"><span data-stu-id="1d824-121">Upon receipt of a request from a client to activate an object, the SCM checks the request against activation-security information stored within its registry.</span></span> <span data-ttu-id="1d824-122">Die Aktivierungs Sicherheit wird auch auf die gleichen Computer Aktivierungen geprüft.</span><span class="sxs-lookup"><span data-stu-id="1d824-122">Activation security is also checked for same-computer activations.</span></span> <span data-ttu-id="1d824-123">Wird auch als *Start Sicherheit* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1d824-123">Also called *launch security*.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-124"><span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**Aktivierungstyp**</span><span class="sxs-lookup"><span data-stu-id="1d824-124"><span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**activation type**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-125">Aktivierungs Kategorie für eine COM+-Anwendung, die angibt, ob die Anwendung im Prozessbereich des Clients (abhängig davon, ob es sich um eine Bibliothek oder eine Serveranwendung handelt) ausgeführt wird, und ob die Anwendung als Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d824-125">Activation category for a COM+ application that indicates whether the application runs in or out of its client's process space (depending on whether it's a library or server application, respectively) as well as whether the application runs as a service.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-126"><span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**aktiv**</span><span class="sxs-lookup"><span data-stu-id="1d824-126"><span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**activity**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-127">In com+ ein logischer Thread, der eine oder mehrere Transaktionen umfasst und eine Auflistung von Komponenten enthält, die in einer COM+-Anwendung gruppiert sind.</span><span class="sxs-lookup"><span data-stu-id="1d824-127">In COM+, a logical thread comprising one or more transactions and containing a collection of components that are grouped into a COM+ application.</span></span> <span data-ttu-id="1d824-128">Jedes COM-Objekt gehört zu einer Aktivität.</span><span class="sxs-lookup"><span data-stu-id="1d824-128">Every COM object belongs to one activity.</span></span> <span data-ttu-id="1d824-129">Die Zuordnung zwischen einem Objekt und einer Aktivität kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1d824-129">The association between an object and an activity cannot be changed.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-130"><span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**Apartment modellprozess**</span><span class="sxs-lookup"><span data-stu-id="1d824-130"><span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**apartment model process**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-131">Ein Prozess, der über mindestens zwei Single Thread-Apartments und keine Multithread-Apartments verfügt.</span><span class="sxs-lookup"><span data-stu-id="1d824-131">A process that has two or more single-threaded apartments and no multithreaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-132"><span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**Anwendungs Proxy**</span><span class="sxs-lookup"><span data-stu-id="1d824-132"><span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**application proxy**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-133">Ein Satz von Dateien, die Registrierungsinformationen enthalten, die einem Client den Remote Zugriff auf eine COM+-Serveranwendung ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="1d824-133">A set of files containing registration information that allows a client to remotely access a COM+ server application.</span></span> <span data-ttu-id="1d824-134">Bei der Installation auf einem Client Computer werden von der Anwendungs Proxy Dateiinformationen zur Serveranwendung auf den Client Computer geschrieben. der Client kann dann Remote auf die Serveranwendung zugreifen.</span><span class="sxs-lookup"><span data-stu-id="1d824-134">When installed on a client computer, an application proxy file writes information about the server application to the client computer; the client can then remotely access the server application.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-135"><span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**Genehmigung**</span><span class="sxs-lookup"><span data-stu-id="1d824-135"><span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**authentication**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-136">Der Sicherheitsprozess, bei dem festgestellt wird, dass der Aufrufer einer Anwendung tatsächlich besagt, dass es sich um die Gültigkeit eines Identitäts Anspruchs handelt –</span><span class="sxs-lookup"><span data-stu-id="1d824-136">The security process of determining that a caller of an application is actually who it says it is—verifying the authenticity of an identity claim.</span></span> <span data-ttu-id="1d824-137">Für COM+-Anwendungen kann die Authentifizierung auf administrativer Weise aktiviert und konfiguriert werden. danach funktioniert Sie transparent mit der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1d824-137">For COM+ applications, authentication can be turned on and configured administratively, after which it works transparently to the application.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-138"><span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**Autorisierungs**</span><span class="sxs-lookup"><span data-stu-id="1d824-138"><span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**authorization**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-139">Der Sicherheitsprozess, der bestimmt, ob ein Aufrufer einer Anwendung autorisiert ist, den Vorgang durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="1d824-139">The security process of determining whether a caller of an application is authorized to do what it is asking to do.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-140"><span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**Caching-Ressourcen-Manager**</span><span class="sxs-lookup"><span data-stu-id="1d824-140"><span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**caching resource manager**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-141">Ein Ressourcen-Manager, der als Front-End zu einem anderen Ressourcen-Manager fungiert und Informationen lokal zwischenspeichert, wodurch die Kosten für den Zugriff auf die zugrunde liegende Ressource gesenkt werden.</span><span class="sxs-lookup"><span data-stu-id="1d824-141">A resource manager that acts as a front-end to another resource manager and that caches information locally, reducing the cost of accessing the underlying resource.</span></span> <span data-ttu-id="1d824-142">Anders als bei einem konventionellen Ressourcen-Manager ist ein Cache Ressourcen-Manager nicht an der Wiederherstellung beteiligt, da er die zugrunde liegenden Daten niemals dauerhaft speichert.</span><span class="sxs-lookup"><span data-stu-id="1d824-142">Unlike a conventional resource manager, a caching resource manager does not participate in recovery because it never permanently stores the underlying data.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-143"><span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**Sicherheit anrufen**</span><span class="sxs-lookup"><span data-stu-id="1d824-143"><span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**call security**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-144">Eine Form von Sicherheitsschutz, mit der der Zugriff auf die Methoden eines Server Objekts nach dem Start eines Servers gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1d824-144">A form of security protection that helps control access to a server object's methods after a server has been launched.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-145"><span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**Klasse (com)**</span><span class="sxs-lookup"><span data-stu-id="1d824-145"><span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**class (COM)**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-146">Eine benannte, konkrete Implementierung von einer oder mehreren Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="1d824-146">A named, concrete implementation of one or more interfaces.</span></span> <span data-ttu-id="1d824-147">Eine COM-Klasse wird durch eine CLSID und manchmal durch eine ProgID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1d824-147">A COM class is identified by a CLSID and, sometimes, a ProgID.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-148"><span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**Cloaking**</span><span class="sxs-lookup"><span data-stu-id="1d824-148"><span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-149">Die Fähigkeit eines Servers, seine eigene Identität bei Aufrufen im Auftrag eines Clients zu maskieren.</span><span class="sxs-lookup"><span data-stu-id="1d824-149">A server's ability to mask its own identity when making calls on a client's behalf.</span></span> <span data-ttu-id="1d824-150">Wenn das Cloaking aktiviert ist, können Aufrufe von dem Server, der die Identität des Clients annimmt, unter der Identität des Clients vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="1d824-150">When cloaking is enabled, calls made by the server impersonating the client can be made under the client's identity.</span></span> <span data-ttu-id="1d824-151">Wenn das Cloaking deaktiviert ist, werden Aufrufe durch den Server unter der Identität des Servers vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="1d824-151">When cloaking is disabled, calls by the server will be made under the server's identity.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-152"><span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**Com+-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="1d824-152"><span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**COM+ application**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-153">Die primäre Verwaltungs-und Sicherheitseinheit für Komponenten Dienste.</span><span class="sxs-lookup"><span data-stu-id="1d824-153">The primary unit of administration and security for Component Services.</span></span> <span data-ttu-id="1d824-154">Eine COM+-Anwendung ist eine Gruppe von COM-Komponenten, die im allgemeinen verwandte Funktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d824-154">A COM+ application is a group of COM components that, generally, perform related functions.</span></span> <span data-ttu-id="1d824-155">Diese Komponenten bestehen weiter aus COM-Schnittstellen und-Methoden.</span><span class="sxs-lookup"><span data-stu-id="1d824-155">These components further consist of COM interfaces and methods.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-156"><span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**Com+-Anwendungs Pooling**</span><span class="sxs-lookup"><span data-stu-id="1d824-156"><span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**COM+ Application Pooling**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-157">Ein Komponenten Dienst Feature, mit dem Single Thread-Prozesse skaliert werden können. Außerdem können Sie Sie bei Fehlern in einzelnen Prozessen wiederherstellen, indem Sie andere laufende Prozesse zur Behandlung von Aktivierungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1d824-157">A Component Services feature that allows single-threaded processes to scale and can also help you recover from failures in single processes by providing other running processes able to handle activations.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-158"><span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**Com+-Anwendungs Wiederverwendung**</span><span class="sxs-lookup"><span data-stu-id="1d824-158"><span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**COM+ Application Recycling**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-159">Ein Komponenten Dienst Feature, das die Gesamtstabilität Ihrer Anwendungen erheblich erhöht, indem es Ihnen ermöglicht, einen Prozess, der einer Anwendung zugeordnet ist, ordnungsgemäß herunterzufahren und neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="1d824-159">A Component Services feature that significantly increases the overall stability of your applications by allowing you to gracefully shut down a process associated with an application and restart it.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-160"><span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**Com+-Katalog**</span><span class="sxs-lookup"><span data-stu-id="1d824-160"><span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**COM+ catalog**</span></span> 
</dt> <dd>

<span data-ttu-id="1d824-161">Der Datenspeicher, der com+-Konfigurationsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="1d824-161">The data store that holds COM+ configuration data.</span></span> <span data-ttu-id="1d824-162">Die Leistung von com+-Verwaltungs Tasks erfordert das Lesen und Schreiben von Daten, die im Katalog gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="1d824-162">Performance of COM+ administration tasks requires reading and writing data stored in the catalog.</span></span> <span data-ttu-id="1d824-163">Der Zugriff auf den Katalog ist nur über das Verwaltungs Programmkomponenten Dienste oder über die COMAdmin-Bibliothek möglich.</span><span class="sxs-lookup"><span data-stu-id="1d824-163">The catalog can be accessed only through the Component Services administrative tool or through the COMAdmin library.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-164"><span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**Com+-Ereignisse**</span><span class="sxs-lookup"><span data-stu-id="1d824-164"><span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**COM+ Events**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-165">Com+-Ereignisse stimmen mit einem locker gekoppelten Ereignis System überein und verbinden Verleger und Abonnenten.</span><span class="sxs-lookup"><span data-stu-id="1d824-165">COM+ Events matches and connects publishers and subscribers through a loosely coupled events system.</span></span> <span data-ttu-id="1d824-166">Ein Verleger führt den Methodenaufruf aus, um ein Ereignis zu initiieren, und ein Abonnent empfängt diese Aufrufe nicht direkt vom Verleger, sondern über das Ereignis System.</span><span class="sxs-lookup"><span data-stu-id="1d824-166">A publisher makes the method call to initiate an event, and a subscriber receives these calls through the event system rather than directly from the publisher.</span></span> <span data-ttu-id="1d824-167">Der com+-Ereignis Dienst verwaltet die Liste der Abonnenten, die die Anrufe erhalten, und leitet diese Anrufe weiter, ohne dass die Kenntnisse des Verlegers erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1d824-167">The COM+ Events service maintains the list of interested subscribers who receive the calls and directs those calls without requiring the knowledge of the publisher.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-168"><span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**Com+-Bibliotheks Anwendung**</span><span class="sxs-lookup"><span data-stu-id="1d824-168"><span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**COM+ library application**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-169">Eine COM+-Anwendung, die im Prozess des Clients ausgeführt wird, von dem Sie erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1d824-169">A COM+ application that runs in the process of the client that creates it.</span></span> <span data-ttu-id="1d824-170">Bibliotheksanwendungen können rollenbasierte Sicherheit verwenden, aber keinen Remote Zugriff oder in die Warteschlange eingereihten Komponenten unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1d824-170">Library applications can use role-based security but do not support remote access or queued components.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-171"><span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**Com+-Objekt Pooling**</span><span class="sxs-lookup"><span data-stu-id="1d824-171"><span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**COM+ Object Pooling**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-172">Ein von com+ bereitgestellter automatischer Dienst, mit dem Sie eine-Komponente so konfigurieren können, dass Instanzen von selbst in einem Pool aktiv gehalten werden und von jedem Client verwendet werden können, der die Komponente anfordert.</span><span class="sxs-lookup"><span data-stu-id="1d824-172">An automatic service provided by COM+ that enables you to configure a component to have instances of itself kept active in a pool, ready to be used by any client that requests the component.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-173"><span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**Com+-Partitionen**</span><span class="sxs-lookup"><span data-stu-id="1d824-173"><span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**COM+ Partitions**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-174">Ein com+-Dienst, der auf einem einzelnen Computer die Erstellung separater Ausführungs Räume für Anwendungen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="1d824-174">A COM+ service that enables, on a single computer, the creation of separate execution spaces for applications.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-175"><span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**Com+-Partitions Sätze**</span><span class="sxs-lookup"><span data-stu-id="1d824-175"><span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**COM+ partition sets**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-176">Eine Gruppe von COM+-Partitionen, die einer bestimmten Benutzer-ID in Active Directory zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1d824-176">A group of COM+ partitions that is mapped to a particular user ID in Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-177"><span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**Com+-Komponenten in der Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="1d824-177"><span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**COM+ Queued Components**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-178">Ein com+-Dienst, der auf Microsoft Message Queuing basiert und eine einfache Möglichkeit zum asynchronen Aufrufen und Ausführen von Komponenten bietet.</span><span class="sxs-lookup"><span data-stu-id="1d824-178">A COM+ service, based on Microsoft Message Queuing, that provides an easy way to invoke and execute components asynchronously.</span></span> <span data-ttu-id="1d824-179">Die Nachrichtenverarbeitung kann ohne Rücksicht auf die Verfügbarkeit oder den Zugriff des Absenders oder des Empfängers erfolgen.</span><span class="sxs-lookup"><span data-stu-id="1d824-179">Message processing can occur without regard to the availability or accessibility of either the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-180"><span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**COM+-Serveranwendung**</span><span class="sxs-lookup"><span data-stu-id="1d824-180"><span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**COM+ server application**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-181">Eine COM+-Anwendung, die in einem eigenen Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d824-181">A COM+ application that runs in its own process.</span></span> <span data-ttu-id="1d824-182">Server Anwendungen können alle com+-Dienste unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1d824-182">Server applications can support all COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-183"><span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**com+-SOAP**</span><span class="sxs-lookup"><span data-stu-id="1d824-183"><span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**COM+ SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-184">Ein Komponenten Dienst Feature, mit dem Sie eine COM+-Anwendung als XML-Webdienst verfügbar machen können.</span><span class="sxs-lookup"><span data-stu-id="1d824-184">A Component Services feature that allows you to expose a COM+ application as an XML web service.</span></span> <span data-ttu-id="1d824-185">Mit com+ SOAP können Sie auch einen XML-Webdienst als COM-Komponente verwenden.</span><span class="sxs-lookup"><span data-stu-id="1d824-185">COM+ SOAP also enables you to use an XML web service as a COM component.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-186"><span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**COM-Komponente**</span><span class="sxs-lookup"><span data-stu-id="1d824-186"><span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**COM component**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-187">Eine binäre Einheit von Code, die Paket-und Registrierungscode umfasst und COM-Objekte erstellt.</span><span class="sxs-lookup"><span data-stu-id="1d824-187">A binary unit of code that includes packaging and registration code and that creates COM objects.</span></span> <span data-ttu-id="1d824-188">Alle com+-Anwendungen bestehen aus einer oder mehreren COM-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="1d824-188">All COM+ applications consist of one or more COM components.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-189"><span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**Commit-Struktur**</span><span class="sxs-lookup"><span data-stu-id="1d824-189"><span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**commit tree**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-190">In einem verteilten Transaktionssystem die konzeptionelle Darstellung einer Transaktion als Grundlage der hierarchischen Beziehungen zwischen einzelnen Transaktions-Managern, die an einer verteilten Transaktion teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="1d824-190">In a distributed transaction system, the conceptual representation of a transaction as based on the hierarchical relationships between individual transaction managers participating in a distributed transaction.</span></span> <span data-ttu-id="1d824-191">In dieser Hierarchie sind die eingetragenen Ressourcen-Manager enthalten, die den Transaktions-Managern zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1d824-191">Included in that hierarchy are the enlisted resource managers associated with the transaction managers.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-192"><span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**COM-Objekt**</span><span class="sxs-lookup"><span data-stu-id="1d824-192"><span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**COM object**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-193">Im COM-Programmiermodell ist eine Programmier Struktur, die sowohl Daten als auch Funktionen kapselt, die als einzelne Einheit definiert und zugeordnet sind und für die der einzige öffentliche Zugriff über die Schnittstellen der Programmier Struktur erfolgt.</span><span class="sxs-lookup"><span data-stu-id="1d824-193">In the COM programming model, a programming structure encapsulating both data and functionality, which are defined and allocated as a single unit and for which the only public access is through the programming structure's interfaces.</span></span> <span data-ttu-id="1d824-194">Ein COM-Objekt muss mindestens die [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle unterstützen, die das vorhanden sein des Objekts während der Verwendung beibehält und Zugriff auf die anderen Schnittstellen des Objekts bietet.</span><span class="sxs-lookup"><span data-stu-id="1d824-194">A COM object must support, at a minimum, the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface, which maintains the object's existence while it is being used and provides access to the object's other interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-195"><span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Kompensierende Ressourcen-Manager (CRM)**</span><span class="sxs-lookup"><span data-stu-id="1d824-195"><span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Compensating Resource Manager (CRM)**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-196">Ein com+-Feature, mit dem nicht transaktionale Ressourcen an einer Zweiphasencommit-Transaktion mit dem Microsoft Distributed Transaction Coordinator (DTC) teilnehmen können.</span><span class="sxs-lookup"><span data-stu-id="1d824-196">A COM+ feature that enables non-transactional resources to participate in a two-phase commit transaction with the Microsoft Distributed Transaction Coordinator (DTC).</span></span> <span data-ttu-id="1d824-197">In der Regel bieten CRMs nicht die Isolations Funktionen von vollständigen Ressourcen-Managern, aber Sie bieten transaktionale Atomizität und Dauerhaftigkeit durch Schreiben in ein Protokoll.</span><span class="sxs-lookup"><span data-stu-id="1d824-197">Typically, CRMs do not provide the isolation capabilities of full resource managers, but they do provide transactional atomicity and durability by writing to a log.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-198"><span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Verwaltungs Tool für Komponenten Dienste**</span><span class="sxs-lookup"><span data-stu-id="1d824-198"><span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Component Services administrative tool**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-199">Ein Benutzeroberflächen-Snap-in, über das Administratoren und Entwickler com+-Anwendungen erstellen, konfigurieren und warten sowie verteilte Transaktionen und Speicher residente Datenbanken verwalten können.</span><span class="sxs-lookup"><span data-stu-id="1d824-199">A user-interface snap-in through which administrators and developers can create, configure, and maintain COM+ applications, as well as administer distributed transactions and memory-resident databases.</span></span> <span data-ttu-id="1d824-200">Mit dem Verwaltungs Programmkomponenten Dienste können auch Systemereignisse angezeigt und Systemdienste lokal auf dem Computer verwaltet werden, auf dem das Tool installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1d824-200">The Component Services administrative tool can also be used to view system events and manage system services local to the computer on which the tool is installed.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-201"><span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**konzeptionelles Modell**</span><span class="sxs-lookup"><span data-stu-id="1d824-201"><span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**conceptual model**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-202">Der erste Schritt in der com+-Anwendungs Entwurfsphase, in der der Entwickler die zu lösenden Geschäftsprobleme definiert und entscheidet, welche Komponenten und Dienste erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1d824-202">The first step in the COM+ application design phase, where the developer defines the business problems to be solved and decides what components and services are required.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-203"><span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**Concurrency**</span><span class="sxs-lookup"><span data-stu-id="1d824-203"><span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**concurrency**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-204">Die Fähigkeit von mehr als einer Transaktion oder einem Prozess, gleichzeitig auf dieselben Daten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="1d824-204">The ability of more than one transaction or process to access the same data at the same time.</span></span> <span data-ttu-id="1d824-205">Com+ verwaltet die Parallelität im Allgemeinen durch Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="1d824-205">COM+ generally manages concurrency through synchronization.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-206"><span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**konfigurierte Komponente**</span><span class="sxs-lookup"><span data-stu-id="1d824-206"><span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**configured component**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-207">Eine COM-Komponente, die in einer COM+-Anwendung installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1d824-207">A COM component that has been installed into a COM+ application.</span></span> <span data-ttu-id="1d824-208">Nach der Installation wird die Komponente im com+-Katalog konfiguriert, um die verfügbaren com+-Dienste nutzen zu können.</span><span class="sxs-lookup"><span data-stu-id="1d824-208">After it is installed, the component is configured within the COM+ catalog to make use of the available COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-209"><span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**Kontext**</span><span class="sxs-lookup"><span data-stu-id="1d824-209"><span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-210">Ein Satz von Lauf Zeiteigenschaften, die einem oder mehreren COM-Objekten zugeordnet sind und zum Bereitstellen von Diensten für diese Objekte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d824-210">A set of run-time properties associated with one or more COM objects that are used to provide services for those objects.</span></span> <span data-ttu-id="1d824-211">Jedes COM-Objekt wird in einem einzigen Kontext von der Aktivierung bis zur Deaktivierung ausgeführt (immer innerhalb desselben Apartment).</span><span class="sxs-lookup"><span data-stu-id="1d824-211">Every COM object runs in a single context from activation to deactivation (always within the same apartment).</span></span> <span data-ttu-id="1d824-212">Wird initialisiert, wenn ein Objekt aktiviert wird. Kontexteigenschaften, wie z. b. Sicherheitskontext Eigenschaften, stellen die Lauf Zeitanforderungen eines Objekts dar.</span><span class="sxs-lookup"><span data-stu-id="1d824-212">Initialized when an object is activated, context properties, such as security context properties, represent the run-time needs of an object.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-213"><span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**Datenebene**</span><span class="sxs-lookup"><span data-stu-id="1d824-213"><span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**data tier**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-214">Das dreistufige Architekturmodell für Geschäftsanwendungen, die DBMS-Zugriffsebene, auf die über die mittlere Ebene, über die Business Services-Ebene und gelegentlich über die Präsentationsebene oder über die Benutzer Dienst Ebene zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="1d824-214">In the three-tier architecture model for business applications, the DBMS access layer, which can be accessed through the middle tier, or business services layer, and on occasion through the presentation tier, or user services layer.</span></span> <span data-ttu-id="1d824-215">Die Datenebene besteht aus Datenzugriffs Komponenten (anstelle von unformatierten DBMS-Verbindungen), um die Ressourcen Freigabe zu unterstützen und Clients zu ermöglichen, ohne die DBMS-Bibliotheken und ODBC-Treiber auf jedem Client zu installieren.</span><span class="sxs-lookup"><span data-stu-id="1d824-215">The data tier consists of data access components (rather than raw DBMS connections) to aid in resource sharing and to allow clients to be configured without installing the DBMS libraries and ODBC drivers on each client.</span></span> <span data-ttu-id="1d824-216">Wird auch als *Data Services-Ebene* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1d824-216">Also called *data services layer*.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-217"><span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**Sackgasse**</span><span class="sxs-lookup"><span data-stu-id="1d824-217"><span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**deadlock**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-218">Bei Multithreadanwendungen ein Threading Problem, das auftritt, wenn jedes Mitglied einer Gruppe von Threads auf einen anderen Member des Satzes wartet.</span><span class="sxs-lookup"><span data-stu-id="1d824-218">In multithreaded applications, a threading problem that occurs when each member of a set of threads is waiting for another member of the set.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-219"><span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**Delegations**</span><span class="sxs-lookup"><span data-stu-id="1d824-219"><span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**delegation**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-220">Eine Form des Identitäts Wechsels, die einen Server autorisiert, auf den Namen eines Clients zu reagieren. Dadurch kann der Server die Identität des Clients über das Netzwerk annehmen.</span><span class="sxs-lookup"><span data-stu-id="1d824-220">A form of impersonation that authorizes a server to act on a client's behalf, giving the server the ability to impersonate clients over the network.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-221"><span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**verteilte Transaktion**</span><span class="sxs-lookup"><span data-stu-id="1d824-221"><span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**distributed transaction**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-222">Eine Transaktion, die mehrere Ressourcen-Manager umfasst, die sich auf demselben Computer oder auf unterschiedlichen Computern befinden können.</span><span class="sxs-lookup"><span data-stu-id="1d824-222">A transaction that involves multiple resource managers, which can be on the same or different computers.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-223"><span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Distributed Transaction Coordinator (DTC)**</span><span class="sxs-lookup"><span data-stu-id="1d824-223"><span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Distributed Transaction Coordinator (DTC)**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-224">Ein-Systemdienst, der Transaktionen und transaktionsbezogene Kommunikationen verwaltet, die auf einem oder mehreren Systemen auf zwei oder mehr Ressourcen-Manager verteilt werden, um korrekte ACID-Transaktionen sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="1d824-224">A system service that manages transactions and transaction-related communications that are distributed across two or more resource managers on one or more systems to ensure correct ACID transactions.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-225"><span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**Dynamisches Cloaking**</span><span class="sxs-lookup"><span data-stu-id="1d824-225"><span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**dynamic cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-226">Eine Art von Verstopfungen, bei der die ursprüngliche Client Identität bei jedem Methodenaufrufe des Downstreamservers als Server Thread-Zugriffs Token erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="1d824-226">A form of cloaking where the original client identity is discovered as the server thread access token on each method call to the downstream server.</span></span> <span data-ttu-id="1d824-227">Obwohl die angegebene Identität dynamisch bestimmt werden kann, kann der Aufwand, der dazu erforderlich ist, erheblich teurer werden.</span><span class="sxs-lookup"><span data-stu-id="1d824-227">Although the identity that is presented can be determined dynamically, the overhead required to do this can be considerably more expensive.</span></span> <span data-ttu-id="1d824-228">Für COM+-Anwendungen ist die Standardkonfiguration für die Funktion für dynamisches abgleichen vorgesehen, da Sie die Flexibilität bereitstellt, die normalerweise von Umständen benötigt wird, die die Verwendung des Identitäts Wechsels an erster Stelle erfordern.</span><span class="sxs-lookup"><span data-stu-id="1d824-228">For COM+ applications, the default configuration is for dynamic cloaking capability because it provides the flexibility that is usually required by circumstances that necessitate using impersonation in the first place.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-229"><span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**Enumeratorobjekt**</span><span class="sxs-lookup"><span data-stu-id="1d824-229"><span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**enumerator object**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-230">Ermöglicht das Aufzählen der Elemente in einer Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1d824-230">Enables enumeration of items in a collection.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-231"><span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**Veranstalter**</span><span class="sxs-lookup"><span data-stu-id="1d824-231"><span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**event**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-232">Eine Aktion, die von einem Objekt erkannt wird, z. b. das Klicken auf die Maus oder das Drücken einer Taste, und für das Sie Code schreiben können, der antwortet.</span><span class="sxs-lookup"><span data-stu-id="1d824-232">An action recognized by an object, such as clicking the mouse or pressing a key, and for which you can write code to respond.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-233"><span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**Event Class-Objekt**</span><span class="sxs-lookup"><span data-stu-id="1d824-233"><span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**event class object**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-234">Eine konfigurierte Komponente, die einen persistenten Datensatz im com+-Ereignis System bereitstellt, um die Herausgeber und die auslösenden Schnittstellen zu beschreiben</span><span class="sxs-lookup"><span data-stu-id="1d824-234">A configured component that provides a persistent record in the COM+ event system to describe the publishers and the firing interfaces associated with those publishers.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-235"><span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**Ereignismethode**</span><span class="sxs-lookup"><span data-stu-id="1d824-235"><span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**event method**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-236">Eine Methode in einer COM+-Schnittstelle, die ein com+-Ereignis identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1d824-236">A method in a COM+ interface that identifies a COM+ event.</span></span> <span data-ttu-id="1d824-237">Ereignis Methoden müssen eindeutig benannt werden und dürfen nur Eingabeparameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="1d824-237">Event methods must be uniquely named and can contain only input parameters.</span></span> <span data-ttu-id="1d824-238">Der Rückgabewert muss ein **HRESULT** sein.</span><span class="sxs-lookup"><span data-stu-id="1d824-238">The return value must be an **HRESULT**.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-239"><span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**Ereignis Objekt**</span><span class="sxs-lookup"><span data-stu-id="1d824-239"><span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**event object**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-240">Ein COM-Objekt, das einem oder mehreren Threads signalisieren kann, dass ein Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1d824-240">A COM object that can signal one or more threads that an event has occurred.</span></span> <span data-ttu-id="1d824-241">Jeder Thread in einem Prozess kann ein Ereignis Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="1d824-241">Any thread within a process can create an event object.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-242"><span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**distanzieren**</span><span class="sxs-lookup"><span data-stu-id="1d824-242"><span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**exception**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-243">Eine ungewöhnliche Bedingung oder ein Fehler, die während der Ausführung eines Programms auftritt und die Ausführung von Software außerhalb der normalen Ablauf Steuerung erfordert.</span><span class="sxs-lookup"><span data-stu-id="1d824-243">An abnormal condition or error that occurs during the execution of a program and that requires the execution of software outside the normal flow of control.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-244"><span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**Failover**</span><span class="sxs-lookup"><span data-stu-id="1d824-244"><span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**failover**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-245">In einem Cluster Netzwerksystem der Prozess, bei dem ein überladener oder fehlerhafter Ressourcen – wie z. b. ein Server, ein Laufwerk oder ein Netzwerk – zu seiner Sicherungs Komponente verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="1d824-245">In a cluster network system, the process of relocating an overloaded or failed resource—such as a server, a disk drive, or a network—to its backup component.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-246"><span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**frei Thread Prozess**</span><span class="sxs-lookup"><span data-stu-id="1d824-246"><span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**free-threaded process**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-247">Ein Prozess, der über ein Multithread-Apartment und keine Single Thread-Apartments verfügt.</span><span class="sxs-lookup"><span data-stu-id="1d824-247">A process that has a multithreaded apartment and no single-threaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-248"><span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**globaler Commit-Koordinator**</span><span class="sxs-lookup"><span data-stu-id="1d824-248"><span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**global commit coordinator**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-249">Der Stamm Transaktions-Manager der commitstruktur auf einem Microsoft Windows – basierten verteilten Transaktionssystem.</span><span class="sxs-lookup"><span data-stu-id="1d824-249">On a Microsoft Windows–based distributed transaction system, the root transaction manager of the commit tree.</span></span> <span data-ttu-id="1d824-250">Dieser Koordinator trifft die Entscheidung, eine bestimmte Transaktion entweder zu commitden oder abzubrechen und ist nie unsicher.</span><span class="sxs-lookup"><span data-stu-id="1d824-250">This coordinator makes the decision to either commit or abort a given transaction and is never in doubt.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-251"><span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**Identitätswechsel**</span><span class="sxs-lookup"><span data-stu-id="1d824-251"><span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**impersonation**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-252">Die Fähigkeit eines Threads, in einem Sicherheitskontext auszuführen, der sich von dem Prozess unterscheidet, der den Thread besitzt.</span><span class="sxs-lookup"><span data-stu-id="1d824-252">The ability of a thread to execute in a security context different from that of the process owning the thread.</span></span> <span data-ttu-id="1d824-253">Der Server Thread verwendet ein Zugriffs Token, das die Anmelde Informationen des Clients darstellt, und damit kann er auf Ressourcen zugreifen, auf die der Client zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="1d824-253">The server thread uses an access token representing the client's credentials, and with this, it can access resources that the client can access.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-254"><span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**Identitätswechsel Ebene**</span><span class="sxs-lookup"><span data-stu-id="1d824-254"><span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**impersonation level**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-255">Die Einstellung, die vom Client verwendet wird, um dem Server eine bestimmte Berechtigungsebene zum Ausführen von Aktionen im Auftrag des Clients zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="1d824-255">The setting used by the client to grant the server a particular level of authority to carry out actions on the client's behalf.</span></span> <span data-ttu-id="1d824-256">In com+ kann dies nur für com+-Server Anwendungen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1d824-256">In COM+, this can be set only for COM+ server applications.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-257"><span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**geschützt**</span><span class="sxs-lookup"><span data-stu-id="1d824-257"><span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**interception**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-258">Für ein Objekt, das in einem bestimmten Kontext aktiviert ist, der Prozess der Verarbeitung von Aufrufen an dieses Objekt über die Kontext Grenze hinweg.</span><span class="sxs-lookup"><span data-stu-id="1d824-258">For an object activated in a given context, the process of handling calls to that object from across the context boundary.</span></span> <span data-ttu-id="1d824-259">Aufrufe über den Kontext werden mithilfe von Lightweight-Schnittstellen Proxys verarbeitet, die alle erforderlichen Vermittlungsarbeiten zur Anpassung der Laufzeitumgebung von einem verwenden, der den Aufrufer für den aufgerufener verwendet.</span><span class="sxs-lookup"><span data-stu-id="1d824-259">Calls across context are handled with lightweight interface proxies that will handle whatever mediation is required to adjust the run-time environment from one that accommodates the caller to one that accommodates the callee.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-260"><span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**berfläche**</span><span class="sxs-lookup"><span data-stu-id="1d824-260"><span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**interface**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-261">Bei der com-basierten Programmierung eine Auflistung von zugehörigen öffentlichen Funktionen, die Zugriff auf ein COM-Objekt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1d824-261">In COM-based programming, a collection of related public functions that provide access to a COM object.</span></span> <span data-ttu-id="1d824-262">Der Satz von Schnittstellen für ein COM-Objekt besteht aus einem Vertrag, der angibt, wie Programme und andere Objekte mit dem COM-Objekt interagieren können.</span><span class="sxs-lookup"><span data-stu-id="1d824-262">The set of interfaces on a COM object composes a contract that specifies how programs and other objects can interact with the COM object.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-263"><span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**Schnittstellen Proxy**</span><span class="sxs-lookup"><span data-stu-id="1d824-263"><span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**interface proxy**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-264">Ein Schnittstellen spezifisches Objekt, das die Parameter für diese Schnittstelle für die Vorbereitung eines Remote Methoden Aufrufes verpackt und die Rückgabewerte aus dem schnittstellenstub entpackt (marshunkt).</span><span class="sxs-lookup"><span data-stu-id="1d824-264">An interface-specific object that packages (marshals) parameters for that interface in preparation for a remote method call and unpackages (unmarshals) the return values from the interface stub.</span></span> <span data-ttu-id="1d824-265">Ein Proxy wird im Adressraum des Absenders ausgeführt und kommuniziert mit einem entsprechenden Stub im Adressraum des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="1d824-265">A proxy runs in the address space of the sender and communicates with a corresponding stub in the receiver's address space.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-266"><span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**schnittstellenstub**</span><span class="sxs-lookup"><span data-stu-id="1d824-266"><span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**interface stub**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-267">Ein Schnittstellen spezifisches Objekt, das gemarshallte Parameter entpackt, die erforderliche Methode aufruft und Pakete (Marshaller) Werte von der aufgerufenen Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1d824-267">An interface-specific object that unpackages marshaled parameters, calls the required method, and packages (marshals) return values from the called method.</span></span> <span data-ttu-id="1d824-268">Der Stub wird im Adressraum des Empfängers ausgeführt und kommuniziert mit einem entsprechenden Schnittstellen Proxy im Adressbereich des Absenders.</span><span class="sxs-lookup"><span data-stu-id="1d824-268">The stub runs in the receiver's address space and communicates with a corresponding interface proxy in the sender's address space.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-269"><span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**Inneres Objekt**</span><span class="sxs-lookup"><span data-stu-id="1d824-269"><span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**interior object**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-270">In einer transaktionalen Hierarchie ein beliebiges Objekt unter dem Stamm Objekt.</span><span class="sxs-lookup"><span data-stu-id="1d824-270">In a transactional hierarchy, any object under the root object.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-271"><span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**Just-in-time (JIT)-Aktivierung**</span><span class="sxs-lookup"><span data-stu-id="1d824-271"><span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**just-in-time (JIT) activation**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-272">Ein von com+ bereitgestellter automatischer Dienst, mit dem Server Ressourcen im Leerlauf produktiver verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1d824-272">An automatic service provided by COM+ that allows idle server resources to be used more productively.</span></span> <span data-ttu-id="1d824-273">Wenn eine Komponente als JIT aktiviert konfiguriert ist, kann com+ eine Instanz davon deaktivieren, während ein Client weiterhin einen aktiven Verweis auf das Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="1d824-273">When a component is configured as JIT activated, COM+ can deactivate an instance of it while a client still holds an active reference to the object.</span></span> <span data-ttu-id="1d824-274">Wenn der Client das nächste Mal eine Methode für das Objekt aufruft, aktiviert com+ das Objekt auf die gleiche Weise transparent auf dem Client, Just-in-Time.</span><span class="sxs-lookup"><span data-stu-id="1d824-274">The next time the client calls a method on the object, COM+ will reactivate the object transparently to the client, just in time.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-275"><span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**Legacy Komponente**</span><span class="sxs-lookup"><span data-stu-id="1d824-275"><span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**legacy component**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-276">Eine nicht konfigurierte Komponente, die in einer COM+-Anwendung installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1d824-276">An unconfigured component that has been installed into a COM+ application.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-277"><span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**empfunden**</span><span class="sxs-lookup"><span data-stu-id="1d824-277"><span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**listener**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-278">Ein Architecture-Element des com+-Dienstanbieter in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="1d824-278">An architectural element of the COM+ Queued Components service.</span></span> <span data-ttu-id="1d824-279">Der Listener ist ein COM-Objekt, das die der Host Anwendung zugeordnete Meldungs Warteschlange öffnet und darauf wartet, dass Nachrichten eintreffen.</span><span class="sxs-lookup"><span data-stu-id="1d824-279">The listener is a COM object that opens the message queue associated with its host application and waits for messages to arrive.</span></span> <span data-ttu-id="1d824-280">Beim Eintreffen von Nachrichten sendet der Listener Threads, die Nachrichten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1d824-280">As messages arrive, the listener dispatches threads that process messages.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-281"><span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**logisches Modell**</span><span class="sxs-lookup"><span data-stu-id="1d824-281"><span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**logical model**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-282">Der zweite Schritt in einem com+-Anwendungs Entwurfsprozess, bei dem das konzeptionelle Modell wie folgt in die logischen Ebenen der dreistufigen Architektur aufgeteilt wird: die Präsentationsebene oder die Benutzerdienste. die mittlere Ebene oder Unternehmens Dienste; und die Datenebene oder Datendienste.</span><span class="sxs-lookup"><span data-stu-id="1d824-282">The second step in a COM+ application design process, where the conceptual model is broken out into the logical tiers of the three-tier architecture, as follows: the presentation tier, or user services; the middle tier, or business services; and the data tier, or data services.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-283"><span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**lose gekoppelter Ereignis**</span><span class="sxs-lookup"><span data-stu-id="1d824-283"><span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**loosely coupled event**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-284">Ein Ereignis, dessen Absender (Verleger) und Empfänger (Abonnent) nicht eng gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="1d824-284">An event whose sender (publisher) and receiver (subscriber) are not closely bound.</span></span> <span data-ttu-id="1d824-285">In einem locker gekoppelten Ereignis System, z. b. com+-Ereignisse, werden Ereignis Informationen von verschiedenen Verlegern in einem Ereignisspeicher persistent gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1d824-285">In a loosely coupled event system, such as COM+ Events, event information from different publishers is persisted in an event store.</span></span> <span data-ttu-id="1d824-286">Abonnenten Fragen diesen Speicher ab und wählen die Ereignisse aus, die Sie empfangen möchten.</span><span class="sxs-lookup"><span data-stu-id="1d824-286">Subscribers query this store and select the events that they want to receive.</span></span> <span data-ttu-id="1d824-287">Durch die Auswahl von Ereignis Informationen aus dem Ereignisspeicher wird ein Abonnement erstellt.</span><span class="sxs-lookup"><span data-stu-id="1d824-287">Selecting event information from the event store creates a subscription.</span></span> <span data-ttu-id="1d824-288">Wenn ein Ereignis auftritt, sucht das Ereignis System in dieser Datenbank nach den interessierten Abonnenten, erstellt ein neues Objekt für jede interessierte Klasse und ruft eine Methode für dieses Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="1d824-288">When an event occurs, the event system looks in this database and finds the interested subscribers, creates a new object of each interested class, and calls a method on that object.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-289"><span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**Marshalling**</span><span class="sxs-lookup"><span data-stu-id="1d824-289"><span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**marshaling**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-290">Der Prozess, bei dem Schnittstellen Methoden Parameter über Thread-oder Prozess Grenzen hinweg verpackt und entpacken werden, sodass ein Remote Prozedur Rückruf stattfinden kann.</span><span class="sxs-lookup"><span data-stu-id="1d824-290">The process of packaging and unpackaging interface method parameters across thread or process boundaries so that a remote procedure call can take place.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-291"><span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**Nachrichten Verschiebe Vorgang**</span><span class="sxs-lookup"><span data-stu-id="1d824-291"><span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**message mover**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-292">Das Architecture-Element des com+-Dienstanbieter für die Warteschlange, der fehlerhafte Nachrichten zurück in die Eingabe Warteschlange verschiebt, damit Sie wiederholt werden können.</span><span class="sxs-lookup"><span data-stu-id="1d824-292">The architectural element of the COM+ Queued Components service that moves failed messages back to their input queue so that they can be retried.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-293"><span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**Meta-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="1d824-293"><span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**meta-event**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-294">Ein Ereignistyp, der vom com+-Ereignis System verwendet wird, um interessierte Abonnenten zu benachrichtigen, wenn Ereignis Klassen Objekte oder-Abonnements erstellt, geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1d824-294">A type of event used by the COM+ Events system to notify interested subscribers whenever event class objects or subscriptions are created, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-295"><span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**anzuwenden**</span><span class="sxs-lookup"><span data-stu-id="1d824-295"><span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**method**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-296">Bei der com-basierten Programmierung ein Prozess, der von einem COM-Objekt ausgeführt wird, wenn eine Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="1d824-296">In COM-based programming, a process performed by a COM object when it receives a message.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-297"><span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**mittlere Ebene**</span><span class="sxs-lookup"><span data-stu-id="1d824-297"><span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**middle tier**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-298">Im dreistufigen Architekturmodell für Geschäftsanwendungen die Ebene, die die Geschäftslogik und die Daten Regeln umfasst.</span><span class="sxs-lookup"><span data-stu-id="1d824-298">In the three-tier architecture model for business applications, the layer comprising the business logic and data rules.</span></span> <span data-ttu-id="1d824-299">Die Komponenten, aus denen die mittlere Ebene besteht, können verwendet werden, um Geschäftsregeln zu erzwingen, z. b. Geschäfts Algorithmen, gesetzliche oder behördliche Vorschriften und Daten Regeln, die so entworfen wurden, dass die Datenstrukturen innerhalb bestimmter oder mehrerer Datenbanken konsistent bleiben.</span><span class="sxs-lookup"><span data-stu-id="1d824-299">The components that make up the middle tier can be used to enforce business rules, such as business algorithms, legal or governmental regulations, and data rules, which are designed to keep the data structures consistent within either specific or multiple databases.</span></span> <span data-ttu-id="1d824-300">Da diese Komponenten der mittleren Ebene nicht an einen bestimmten Client gebunden sind, können Sie von allen Anwendungen verwendet werden und können als Antwortzeit und andere Regeln an verschiedene Speicherorte verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="1d824-300">Because these middle-tier components are not tied to a specific client, they can be used by all applications and can be moved to different locations as response time and other rules require.</span></span> <span data-ttu-id="1d824-301">Wird auch als *Geschäfts Dienst Ebene* oder *Geschäftslogik Ebene* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1d824-301">Also called *business services layer* or *business logic tier*.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-302"><span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**Gemischter modellprozess**</span><span class="sxs-lookup"><span data-stu-id="1d824-302"><span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**mixed model process**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-303">Ein Prozess, der über ein Multithread-Apartment und eine oder mehrere Single Thread-Apartments verfügt.</span><span class="sxs-lookup"><span data-stu-id="1d824-303">A process that has a multithreaded apartment and one or more single-threaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-304"><span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**Moniker**</span><span class="sxs-lookup"><span data-stu-id="1d824-304"><span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**moniker**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-305">Ein Name, der ein COM-Objekt eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1d824-305">A name that uniquely identifies a COM object.</span></span> <span data-ttu-id="1d824-306">Auf dieselbe Weise, wie ein Pfad eine Datei im Dateisystem identifiziert, identifiziert ein Moniker ein COM-Objekt im Verzeichnis Namespace.</span><span class="sxs-lookup"><span data-stu-id="1d824-306">In the same way that a path identifies a file in the file system, a moniker identifies a COM object in the directory namespace.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-307"><span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**MSI-Datei**</span><span class="sxs-lookup"><span data-stu-id="1d824-307"><span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**.msi file**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-308">Eine Datei, die vom Verwaltungs Programmkomponenten Dienste beim Exportieren einer COM+-Anwendung oder eines Anwendungs Proxys für die Installation auf einem anderen Computer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1d824-308">A file created by the Component Services administrative tool when you export a COM+ application or application proxy for installation on another computer.</span></span> <span data-ttu-id="1d824-309">Die MSI-Datei kann auf jedem Windows-basierten Client mithilfe Windows Installer installiert werden.</span><span class="sxs-lookup"><span data-stu-id="1d824-309">The .msi file can be installed on any Windows-based client using Windows Installer.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-310"><span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**Multithread-Apartment Modell**</span><span class="sxs-lookup"><span data-stu-id="1d824-310"><span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**multithreaded apartment model**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-311">Ein Apartment Modell, in dem alle Threads im Prozess, die als "frei Thread" initialisiert wurden, sich in einem einzigen Apartment befinden.</span><span class="sxs-lookup"><span data-stu-id="1d824-311">An apartment model in which all the threads in the process that have been initialized as free-threaded reside in a single apartment.</span></span> <span data-ttu-id="1d824-312">Daher ist es nicht erforderlich, zwischen Threads zu Mars Hallen.</span><span class="sxs-lookup"><span data-stu-id="1d824-312">Therefore, there is no need to marshal between threads.</span></span> <span data-ttu-id="1d824-313">Die Threads müssen keine Nachrichten abrufen und verteilen, weil com in diesem Modell keine Fenster Meldungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="1d824-313">The threads need not retrieve and dispatch messages because COM does not use window messages in this model.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-314"><span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**eine Transaktion**</span><span class="sxs-lookup"><span data-stu-id="1d824-314"><span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**nested transaction**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-315">Eine sekundäre Transaktion, die von innerhalb einer vorhandenen primären oder übergeordneten Transaktionsgrenze initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1d824-315">A secondary transaction initiated from within an existing primary or parent transaction boundary.</span></span> <span data-ttu-id="1d824-316">Der Commit der primären Transaktion wird erst durchführt, wenn alle untergeordneten oder nicht untergeordneten Transaktionen committet wurden.</span><span class="sxs-lookup"><span data-stu-id="1d824-316">The primary transaction does not commit until all of its subordinate, or nested, transactions commit.</span></span> <span data-ttu-id="1d824-317">Com+ unterstützt keine netsted Transactions.</span><span class="sxs-lookup"><span data-stu-id="1d824-317">COM+ does not support nested transactions.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-318"><span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**neutrales Apartment Modell**</span><span class="sxs-lookup"><span data-stu-id="1d824-318"><span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**neutral apartment model**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-319">Ein Threading Modell, in dem Objekte den Richtlinien für multithreadwohnungen entsprechen, aber in jeder Art von Thread ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="1d824-319">A threading model in which objects follow the guidelines for multithreaded apartments but can execute on any kind of thread.</span></span> <span data-ttu-id="1d824-320">Das neutrale Apartment Modell ist das empfohlene Threading Modell für COM-Komponenten und com+-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="1d824-320">The neutral apartment model is the recommended threading model for COM components and COM+ applications.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-321"><span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**persistentes Objekt**</span><span class="sxs-lookup"><span data-stu-id="1d824-321"><span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**persistent object**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-322">Ein COM-Objekt, das seinen internen Zustand speichern kann, wenn es von einem Client dazu aufgefordert wird und com-definierte Standards entspricht, über die Clients das Initialisieren, laden und Speichern von Objekten in einem Datenspeicher anfordern können (z. b. Flatfile, strukturierter Speicher oder Arbeitsspeicher).</span><span class="sxs-lookup"><span data-stu-id="1d824-322">A COM object that can save its internal state when asked to do so by a client and that conforms to COM-defined standards through which clients can request objects to be initialized, loaded, and saved to and from a data store (for example, flat file, structured storage, or memory).</span></span> <span data-ttu-id="1d824-323">Der Client ist dafür verantwortlich, den Speicherort zu verwalten, an dem die persistenten Daten des Objekts gespeichert werden, aber nicht das Format der Daten.</span><span class="sxs-lookup"><span data-stu-id="1d824-323">It is the client's responsibility to manage the location where the object's persistent data is stored but not the format of the data.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-324"><span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**persistente Objektschnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1d824-324"><span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**persistent object interface**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-325">Eine COM-Schnittstelle, die von einem permanenten Objekt implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="1d824-325">A COM interface implemented by a persistent object.</span></span> <span data-ttu-id="1d824-326">Clients verwenden persistente Objekt Schnittstellen, um den persistenten Objekten mitzuteilen, wann und wo ihr Zustand gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d824-326">Clients use persistent object interfaces to tell those persistent objects when and where to store their state.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-327"><span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**Benachrichtigungs Schnittstelle für Phase Zero**</span><span class="sxs-lookup"><span data-stu-id="1d824-327"><span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**phase zero notification interface**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-328">Com+-Schnittstelle, die es Anwendungen ermöglicht, zu erkennen, wann eine Transaktion mit einem Zweiphasencommit-Protokoll fortgesetzt werden kann, um die erforderlichen Benachrichtigungs Vorgänge auszuführen und mit dem Transaktions-Manager zu kommunizieren, wenn die Vorgänge abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="1d824-328">COM+ interface that allows applications to detect when a transaction is ready to proceed with a two-phase commit protocol so that it can perform the necessary notification operations and communicate to the transaction manager when the operations have been completed.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-329"><span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**physisches Modell**</span><span class="sxs-lookup"><span data-stu-id="1d824-329"><span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**physical model**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-330">Der dritte und letzte Schritt im com+-Anwendungs Entwurfsprozess, bei dem der Entwickler bestimmt, wo sich die Komponenten physisch befinden und wie Sie codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1d824-330">The third and final step in the COM+ application design process, where the developer determines where the components reside physically and how they are to be coded.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-331"><span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**Feldspieler**</span><span class="sxs-lookup"><span data-stu-id="1d824-331"><span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**player**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-332">Das Architecture-Element des com+-Dienstanbieter für die Warteschlange, der die Nachricht aus einer Warteschlange abruft und dann das Server Objekt und die standardschnittstellenstubvorgänge lädt, um Daten zu entfernen und Server Methoden aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1d824-332">The architectural element of the COM+ Queued Components service that retrieves the message from a queue and then loads the server object and the standard interface stubs to unmarshal data and invoke server methods.</span></span> <span data-ttu-id="1d824-333">Der Player gibt den Sicherheitskontext des Clients auf der Serverseite aus und ruft dann die Serverkomponente auf und führt die gleichen Methodenaufrufe aus.</span><span class="sxs-lookup"><span data-stu-id="1d824-333">The player unmarshals the client's security context at the server side and then invokes the server component and makes the same method calls.</span></span> <span data-ttu-id="1d824-334">Die Methodenaufrufe werden vom Player nicht wiedergegeben, bis die Client Komponente abgeschlossen ist, und die Transaktion, die die Methode aufgezeichnet hat, führt Commits aus.</span><span class="sxs-lookup"><span data-stu-id="1d824-334">The method calls are not played back by the player until the client component completes and the transaction that recorded the method calls commits.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-335"><span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**Präsentationsebene**</span><span class="sxs-lookup"><span data-stu-id="1d824-335"><span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**presentation tier**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-336">In den dreistufigen Architekturmodellen für Geschäftsanwendungen die Ebene, die Daten für den Benutzer darstellt und optional Datenbearbeitung und Dateneingabe zulässt.</span><span class="sxs-lookup"><span data-stu-id="1d824-336">In the three-tier architecture model for business applications, the layer that presents data to the user and optionally permits data manipulation and data entry.</span></span> <span data-ttu-id="1d824-337">Die zwei Haupttypen von Benutzeroberflächen für die Präsentationsebene sind die herkömmliche Anwendung und die webbasierte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1d824-337">The two main types of user interface for the presentation tier are the traditional application and the Web-based application.</span></span> <span data-ttu-id="1d824-338">Wird auch als *Benutzer Dienst Ebene* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1d824-338">Also called *user services layer*.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-339"><span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**primäres Zugriffs Token**</span><span class="sxs-lookup"><span data-stu-id="1d824-339"><span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**primary access token**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-340">Beschreibt den Sicherheitskontext des Benutzerkontos, das einem Prozess zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1d824-340">Describes the security context of the user account associated with a process.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-341"><span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**Proxy-Manager**</span><span class="sxs-lookup"><span data-stu-id="1d824-341"><span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**proxy manager**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-342">Beim Standardmarshalling eine Komponente, die alle Schnittstellen Proxys für ein einzelnes Objekt verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1d824-342">In standard marshaling, a component that manages all the interface proxies for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-343"><span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**Pseudo Objekt**</span><span class="sxs-lookup"><span data-stu-id="1d824-343"><span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**pseudo-object**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-344">Ein Typ eines enthaltenen Objekts, z. b. eine Benutzer Auswahl in einem Dokument, ein Bereich von Zellen in einer Kalkulations Tabelle oder ein Zeichenbereich in einem Textdokument.</span><span class="sxs-lookup"><span data-stu-id="1d824-344">A type of contained object, such as a user selection in a document, a range of cells in a spreadsheet, or a range of characters in a text document.</span></span> <span data-ttu-id="1d824-345">Dieser Objekttyp wird als Pseudo Objekt bezeichnet, da es nicht als eindeutiges Objekt behandelt wird, bis ein Benutzer die Auswahl markiert.</span><span class="sxs-lookup"><span data-stu-id="1d824-345">This type of object is called a pseudo-object because it isn't treated as a distinct object until a user marks the selection.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-346"><span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**Gebers**</span><span class="sxs-lookup"><span data-stu-id="1d824-346"><span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**publisher**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-347">Der Absender eines Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="1d824-347">The sender of an event.</span></span> <span data-ttu-id="1d824-348">In der Architektur der com+-Ereignisse führt der Herausgeber den Methoden aufzurufen, um ein Ereignis zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="1d824-348">In the COM+ Events architecture, the publisher makes the method call to initiate an event.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-349"><span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**Warteschlangen-Moniker**</span><span class="sxs-lookup"><span data-stu-id="1d824-349"><span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**queue moniker**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-350">Der Moniker, mit dem eine in der Warteschlange befindliche Komponente aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="1d824-350">The moniker used to activate a queued component.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-351"><span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**Racebedingung**</span><span class="sxs-lookup"><span data-stu-id="1d824-351"><span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**race condition**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-352">Eine Bedingung in einer Multithreadanwendung, die auftritt, wenn mehrere Threads auf ein Datenelement ohne Koordination zugreifen und möglicherweise inkonsistente Ergebnisse verursachen, je nachdem, welcher Thread zuerst das Datenelement erreicht.</span><span class="sxs-lookup"><span data-stu-id="1d824-352">In a multithreaded application, a condition that occurs when multiple threads access a data item without coordination, possibly causing inconsistent results, depending on which thread reaches the data item first.</span></span> <span data-ttu-id="1d824-353">COM bietet einige Funktionen, die speziell entwickelt wurden, um Racebedingungen in Prozess externen Servern zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="1d824-353">COM supplies some functions specifically designed to help avoid race conditions in out-of-process servers.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-354"><span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**aufzunehmen**</span><span class="sxs-lookup"><span data-stu-id="1d824-354"><span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**recorder**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-355">Das Architecture-Element des com+-Diensts für Warteschlangen Komponenten, der den Sicherheitskontext des Clients in eine Nachricht marshallt und alle Methodenaufrufe für ein Objekt aufzeichnet.</span><span class="sxs-lookup"><span data-stu-id="1d824-355">The architectural element of the COM+ Queued Components service that marshals the client's security context into a message and records all of the method calls for an object.</span></span> <span data-ttu-id="1d824-356">Der Recorder ist ein vom System bereitgestellter Proxy Manager, der Schnittstellen aus den Warteschlangen fähigen Schnittstellen im com+-Katalog auswählt.</span><span class="sxs-lookup"><span data-stu-id="1d824-356">The recorder is a system-provided proxy manager that selects interfaces from the queuable interfaces in the COM+ catalog.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-357"><span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**Ressourcen Verteiler**</span><span class="sxs-lookup"><span data-stu-id="1d824-357"><span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**resource dispenser**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-358">Eine Komponente im COM+-Programmiermodell, die den nicht permanenten Freigabe Zustand im Namen der Anwendungskomponenten innerhalb eines Prozesses verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1d824-358">In the COM+ programming model, a component that manages nondurable shared state on behalf of the application components within a process.</span></span> <span data-ttu-id="1d824-359">Ressourcen Spender ähneln Ressourcen-Managern, ohne dass die Dauerhaftigkeit gewährleistet ist.</span><span class="sxs-lookup"><span data-stu-id="1d824-359">Resource dispensers are similar to resource managers but without the guarantee of durability.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-360"><span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**Ressourcen-Manager**</span><span class="sxs-lookup"><span data-stu-id="1d824-360"><span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**resource manager**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-361">Ein Dienst, der persistente oder dauerhafte Daten in Datenbanken, permanenten Nachrichten Warteschlangen oder transaktionalen Dateisystemen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1d824-361">A service that manages persistent or durable data in databases, durable message queues, or transactional file systems.</span></span> <span data-ttu-id="1d824-362">Es ist der Ressourcen-Manager, der weiß, wie Daten gespeichert und eine Notfall Wiederherstellung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1d824-362">It is the resource manager that knows how to store data and perform disaster recovery.</span></span> <span data-ttu-id="1d824-363">Com+-Server Anwendungen verwenden Ressourcen-Manager, um den dauerhaften Status einer Anwendung aufrechtzuerhalten, z. b. den Datensatz des Bestands, ausstehende Bestellungen und Konten, die Sie empfangen können.</span><span class="sxs-lookup"><span data-stu-id="1d824-363">COM+ server applications use resource managers to maintain the durable state of an application, such as the record of inventory on hand, pending orders, and accounts receivable.</span></span> <span data-ttu-id="1d824-364">Ressourcen-Manager arbeiten in Zusammenarbeit mit dem Microsoft Distributed Transaction Coordinator (DTC) zusammen, um die Unteilbarkeit und Isolation von Anwendungen zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="1d824-364">Resource managers work in cooperation with the Microsoft Distributed Transaction Coordinator (DTC) to guarantee atomicity and isolation to an application.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-365"><span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**Rollenbasierte Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="1d824-365"><span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**role-based security**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-366">Ein com+-Sicherheitsdienst für COM+-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="1d824-366">A COM+ security service provided for COM+ applications.</span></span> <span data-ttu-id="1d824-367">Eine Rolle stellt eine Kategorie von Benutzern dar, die für eine COM+-Anwendung definiert sind, um die Zugriffsberechtigungen für die Ressourcen der Anwendung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="1d824-367">A role represents a category of users defined for a COM+ application for the purpose of determining access permissions to the application's resources.</span></span> <span data-ttu-id="1d824-368">Rollen werden von einem Entwickler Komponenten, Schnittstellen und Methoden zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1d824-368">Roles are assigned by a developer to components, interfaces, and methods.</span></span> <span data-ttu-id="1d824-369">Benutzer werden von einem Administrator den entsprechenden Rollen zugewiesen, sodass ein Benutzer in einer bestimmten Rolle auf alle Ressourcen zugreifen kann, denen diese Rolle zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1d824-369">Users are assigned by an administrator to appropriate roles, enabling a user within a given role to access any resources to which that role is assigned.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-370"><span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**Root-Objekt**</span><span class="sxs-lookup"><span data-stu-id="1d824-370"><span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**root object**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-371">Das erste Objekt einer Transaktion, das als Stamm der Transaktion bezeichnet wird und immer in einer neuen Transaktionsgrenze platziert wird.</span><span class="sxs-lookup"><span data-stu-id="1d824-371">The first object of a transaction, called the root of the transaction, and always placed in a new transactional boundary.</span></span> <span data-ttu-id="1d824-372">Es darf nur ein Stamm Objekt in einer Transaktion vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="1d824-372">There can be only one root object in a transaction.</span></span> <span data-ttu-id="1d824-373">Alle anderen Objekte in der transaktionalen Hierarchie unter dem Root-Objekt werden als innere Objekte bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1d824-373">All other objects in the transactional hierarchy under the root object are called interior objects.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-374"><span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**stammtransaktions-Manager**</span><span class="sxs-lookup"><span data-stu-id="1d824-374"><span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**root transaction manager**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-375">Der Transaktions-Manager auf dem System, der eine Transaktion initiiert.</span><span class="sxs-lookup"><span data-stu-id="1d824-375">The transaction manager on the system that initiates a transaction.</span></span> <span data-ttu-id="1d824-376">Die Transaktion wird erst beendet, wenn der Stamm Transaktions-Manager den Status der Transaktion ermittelt hat (entweder zugesichert oder abgebrochen).</span><span class="sxs-lookup"><span data-stu-id="1d824-376">The transaction is not finalized until the root transaction manager determines the transaction's status (either committed or aborted).</span></span>

</dd> <dt>

<span data-ttu-id="1d824-377"><span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**Semaphor**</span><span class="sxs-lookup"><span data-stu-id="1d824-377"><span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**semaphore**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-378">Ein Kernel Objekt, das verwendet wird, um den Zugriff auf eine freigegebene Ressource zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="1d824-378">A kernel object used to arbitrate access to a shared resource.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-379"><span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**Dienststeuerungs-Manager (SCM)**</span><span class="sxs-lookup"><span data-stu-id="1d824-379"><span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**service control manager (SCM)**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-380">Ein Microsoft Windows Server-Prozess, mit dem alle Dienste in der Windows-Registrierung verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="1d824-380">A Microsoft Windows server process that manages all the services in the Windows registry.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-381"><span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**frei gegebener Eigenschaften-Manager (SPM)**</span><span class="sxs-lookup"><span data-stu-id="1d824-381"><span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**shared property manager (SPM)**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-382">In com+ ein Ressourcen Verteiler, den Sie verwenden können, um einen nicht persistenten Status für mehrere Objekte innerhalb eines Server Prozesses freizugeben.</span><span class="sxs-lookup"><span data-stu-id="1d824-382">In Com+, a resource dispenser that you can use to share nonpersistent state among multiple objects within a server process.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-383"><span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**Single Thread-Prozess**</span><span class="sxs-lookup"><span data-stu-id="1d824-383"><span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**single-threaded process**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-384">Ein Prozess, der aus nur einem Single Thread-Apartment besteht, das wiederum genau einen Thread umfasst.</span><span class="sxs-lookup"><span data-stu-id="1d824-384">A process that consists of just one single-threaded apartment, which in turn consists of exactly one thread.</span></span> <span data-ttu-id="1d824-385">Alle COM-Objekte, die in einem Single Thread-Apartment Leben, können Methodenaufrufe von nur einem Thread empfangen, der zu diesem Apartment gehört.</span><span class="sxs-lookup"><span data-stu-id="1d824-385">All COM objects that live in a single-threaded apartment can receive method calls from only the one thread that belongs to that apartment.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-386"><span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**Soester**</span><span class="sxs-lookup"><span data-stu-id="1d824-386"><span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-387">Ein einfaches XML-basiertes Protokoll zum Austauschen strukturierter und Typinformationen im Web.</span><span class="sxs-lookup"><span data-stu-id="1d824-387">A simple, XML-based protocol for exchanging structured and type information on the Web.</span></span> <span data-ttu-id="1d824-388">Das Protokoll enthält keine Anwendungs-oder Transport Semantik, wodurch es stark modular und erweiterbar ist.</span><span class="sxs-lookup"><span data-stu-id="1d824-388">The protocol contains no application or transport semantics, which makes it highly modular and extensible.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-389"><span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**geteilte Registrierung**</span><span class="sxs-lookup"><span data-stu-id="1d824-389"><span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**split registration**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-390">Für Komponenten, die bereits vorhandene COM-Komponenten sind und in der com+-Dienst Umgebung verwendet werden, wird die Registrierungs Anordnung, bei der der grundlegende com-Aspekt der Registrierung in der Windows-Registrierung gespeichert ist, und neue COM+-Dienste und-Attribute (z. b. in der Warteschlange befindliche Komponenten) in der COM+-Registrierungsdatenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1d824-390">For components that are already existing COM components and are used in the COM+ services environment, the registration arrangement in which the basic COM aspect of the registration is stored in the Windows registry and new COM+ services and attributes (for example, Queued Components) are stored in the COM+ Registration Database.</span></span> <span data-ttu-id="1d824-391">Die einzelnen Komponenten Attribute werden entweder in der Windows-Registrierung oder in der COM+-Registrierungsdatenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1d824-391">Each component attribute is stored in either the Windows registry or the COM+ Registration Database.</span></span> <span data-ttu-id="1d824-392">Neue COM-Komponenten werden ausschließlich in der COM+-Registrierungsdatenbank registriert, wobei eine Duplizierung in der Windows-Registrierung möglich ist, damit vorhandene Tools Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="1d824-392">New COM components are registered exclusively in the COM+ Registration Database, with some duplication in the Windows registry so that existing tools can use them.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-393"><span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**Zustands behafteten**</span><span class="sxs-lookup"><span data-stu-id="1d824-393"><span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**stateful**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-394">Von oder im Zusammenhang mit einem System oder Prozess, das alle Details des Zustands einer Aktivität überwacht, an der es beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="1d824-394">Of or pertaining to a system or process that monitors all details of the state of an activity in which it participates.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-395"><span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**Zustands losen**</span><span class="sxs-lookup"><span data-stu-id="1d824-395"><span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**stateless**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-396">Von oder im Zusammenhang mit einem System oder Prozess, der an Aktivitäten teilnimmt, ohne alle Details seines Zustands zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="1d824-396">Of or pertaining to a system or process that participates in activity without monitoring all details of its state.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-397"><span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**statischer Cloaking**</span><span class="sxs-lookup"><span data-stu-id="1d824-397"><span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**static cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-398">Eine Art von Verstopfungen, bei der die ursprüngliche Client Identität einmal an einen Downstreamserver präsentiert werden kann, wobei die ursprüngliche Client Identität einmal auf dem Proxy festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1d824-398">A form of cloaking where the original client identity can be presented once to a downstream server, setting the original client identity once on the proxy.</span></span> <span data-ttu-id="1d824-399">Diese Client Identität wird als Server Thread Token dargestellt, das bei nachfolgenden Methoden aufrufen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d824-399">This client identity is presented as a server thread token that will be used on subsequent method calls.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-400"><span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**Abonnenten**</span><span class="sxs-lookup"><span data-stu-id="1d824-400"><span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**subscriber**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-401">Der Empfänger eines Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="1d824-401">The receiver of an event.</span></span> <span data-ttu-id="1d824-402">In der Architektur der com+-Ereignisse empfängt der Abonnent die vom Verleger ausgeführten Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="1d824-402">In the COM+ Events architecture, the subscriber receives the calls made by the publisher.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-403"><span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**Abonnement Objekt**</span><span class="sxs-lookup"><span data-stu-id="1d824-403"><span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**subscription object**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-404">Ein Objekt im com+-Ereignis System, das von einem Abonnenten erstellt wurde, um die Übermittlung von Ereignissen anzufordern und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="1d824-404">In the COM+ Events system, an object created by a subscriber to request and manage the delivery of events.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-405"><span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**synchron**</span><span class="sxs-lookup"><span data-stu-id="1d824-405"><span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**synchronization**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-406">In com+ ein Dienst, der von Komponente zu Komponente fließt und verhindert, dass mehr als ein Aufrufer zu einem bestimmten Zeitpunkt in die Komponente wechselt.</span><span class="sxs-lookup"><span data-stu-id="1d824-406">In COM+, a service that flows from component to component and prohibits more than one caller from entering the component at any given time.</span></span> <span data-ttu-id="1d824-407">Die Synchronisierung bestimmt, wann Threads Aufrufe an ein-Objekt senden können.</span><span class="sxs-lookup"><span data-stu-id="1d824-407">Synchronization determines when threads can dispatch calls to an object.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-408"><span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**dreistufiges Architekturmodell**</span><span class="sxs-lookup"><span data-stu-id="1d824-408"><span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**three-tier architectural model**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-409">Das grundlegende Framework für das logische Entwurfs Modell segmentiert die Komponenten einer Anwendung wie folgt in drei Dienst Ebenen: die Präsentationsebene oder die Benutzerdienste. die mittlere Ebene oder Unternehmens Dienste; und die Datenebene oder Datendienste.</span><span class="sxs-lookup"><span data-stu-id="1d824-409">The fundamental framework for the logical design model, segments an application's components into three tiers of services as follows: the presentation tier, or user services; the middle tier, or business services; and the data tier, or data services.</span></span> <span data-ttu-id="1d824-410">Diese Ebenen entsprechen nicht notwendigerweise physischen Standorten auf verschiedenen Computern in einem Netzwerk, sondern eher auf logischen Ebenen der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1d824-410">These tiers do not necessarily correspond to physical locations on various computers on a network, but rather to logical layers of the application.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-411"><span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**eng verbundenes Ereignis**</span><span class="sxs-lookup"><span data-stu-id="1d824-411"><span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**tightly coupled event**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-412">Ein Ereignis, dessen Absender (Verleger) und Empfänger (Abonnent) eng gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="1d824-412">An event whose sender (publisher) and receiver (subscriber) are closely bound.</span></span> <span data-ttu-id="1d824-413">In einem eng gekoppelten Ereignis System wird dem Verleger eine Schnittstelle zur Verfügung gestellt, auf der eine Methode aufgerufen werden soll, wenn eine Änderung auftritt.</span><span class="sxs-lookup"><span data-stu-id="1d824-413">In a tightly coupled event system, the publisher is provided with an interface on which to call a method when a change occurs.</span></span> <span data-ttu-id="1d824-414">Der Abonnent weiß, von welchem Verleger eine Benachrichtigung angefordert werden soll, und die verfügbaren Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="1d824-414">The subscriber knows which publisher to request notification from and the interfaces that are exposed.</span></span> <span data-ttu-id="1d824-415">Ein eng gekoppeltes Ereignis System erfordert, dass sowohl der Verleger als auch der Abonnent jederzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1d824-415">A tightly coupled event system requires that both the publisher and the subscriber are running at all times.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-416"><span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**Ablauf Verfolgungs Protokoll**</span><span class="sxs-lookup"><span data-stu-id="1d824-416"><span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**trace log**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-417">Eine Protokolldatei, die automatisch vom Microsoft-Distributed Transaction Coordinator generiert wird und Daten enthält, die mit einer oder mehreren verteilten Transaktionen verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="1d824-417">A log file automatically generated by the Microsoft Distributed Transaction Coordinator that shows data related to one or more distributed transactions.</span></span> <span data-ttu-id="1d824-418">Beispiele für Daten in einem Ablauf Verfolgungs Protokoll sind Transaktions-ID, Transaktionszeit und Nachrichten, die das Transaktions Ergebnis angeben.</span><span class="sxs-lookup"><span data-stu-id="1d824-418">Examples of data in a trace log are transaction ID, transaction time, and messages indicating the transaction outcome.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-419"><span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**Geschäfte**</span><span class="sxs-lookup"><span data-stu-id="1d824-419"><span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**transaction**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-420">Eine Arbeitseinheit, bei der während eines Anwendungsprozesses eine Reihe verwandter Vorgänge stattfindet.</span><span class="sxs-lookup"><span data-stu-id="1d824-420">A unit of work in which a series of related operations occur during an application process.</span></span> <span data-ttu-id="1d824-421">Eine Transaktion wird genau einmal ausgeführt und ist atomarisch – entweder ist entweder die gesamte Arbeit abgeschlossen, oder es ist kein Wert.</span><span class="sxs-lookup"><span data-stu-id="1d824-421">A transaction executes exactly once and is atomic—either all of the work is done or none of it is.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-422"><span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Transaction Internet Protocol (Tipp)**</span><span class="sxs-lookup"><span data-stu-id="1d824-422"><span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Transaction Internet Protocol (TIP)**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-423">Das Internetprotokoll der Transaktion ist ein Standardmäßiges Zweiphasencommit-Protokoll, das heterogenen Transaktions-Managern ermöglicht, verteilte Transaktionen zu koordinieren, insbesondere über das Internet.</span><span class="sxs-lookup"><span data-stu-id="1d824-423">Transaction Internet Protocol is a standard two-phase commit protocol that enables heterogeneous transaction managers to coordinate distributed transactions, especially over the Internet.</span></span> <span data-ttu-id="1d824-424">Das Zweiphasencommit-Protokoll von Tip ist einfach zu implementieren und ist unabhängig vom Anwendungs-zu-Anwendungs-Kommunikationsprotokoll, sodass es mit jedem beliebigen Anwendungsprotokoll, jedoch insbesondere mit http, verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1d824-424">The TIP two-phase commit protocol is simple to implement and is independent of the application-to-application communications protocol, such that it may be used with any application protocol but especially HTTP.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-425"><span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**Transaktions-Manager**</span><span class="sxs-lookup"><span data-stu-id="1d824-425"><span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**transaction manager**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-426">Der Teil des Microsoft Distributed Transaction Coordinator (DTC), der auf allen Computern ausgeführt wird, die an einer verteilten Transaktion teilnehmen und die Aktivitäten im Zusammenhang mit dem Commit oder Abbruch dieses Teils der Transaktion verwalten.</span><span class="sxs-lookup"><span data-stu-id="1d824-426">The part of the Microsoft Distributed Transaction Coordinator (DTC) that executes on each computer participating in a distributed transaction and manages the activities related to committing or aborting that part of the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-427"><span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**Transaktions Verarbeitungs Anwendung**</span><span class="sxs-lookup"><span data-stu-id="1d824-427"><span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**transaction processing application**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-428">Eine Auflistung von Transaktions Vorgängen, die eine bestimmte Geschäftsaufgabe automatisieren.</span><span class="sxs-lookup"><span data-stu-id="1d824-428">A collection of transaction operations that automate a given business task.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-429"><span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**Transaktions Verarbeitungssystem**</span><span class="sxs-lookup"><span data-stu-id="1d824-429"><span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**transaction processing system**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-430">Ein vollständiges System, das sowohl Computer Hardware als auch Software umfasst, das eine Transaktions Verarbeitungs Anwendung hostet, um routinemäßige Transaktionen auszuführen, die für das Durchführen von Geschäfts</span><span class="sxs-lookup"><span data-stu-id="1d824-430">A complete system, comprising both computer hardware and software, that hosts a transaction processing application to perform routine transactions necessary to conduct business.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-431"><span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**Zweiphasencommit-Protokoll**</span><span class="sxs-lookup"><span data-stu-id="1d824-431"><span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**two-phase commit protocol**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-432">Ein Protokoll, das nur in verteilten Transaktionen verwendet wird, stellt sicher, dass das Ergebnis einer Transaktion über alle Transaktions-Manager hinweg konsistent ist, die an der Transaktion beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="1d824-432">A protocol used only in distributed transactions, ensures that the outcome of a transaction is consistent across all transaction managers participating in the transaction.</span></span> <span data-ttu-id="1d824-433">Das Protokoll arbeitet in zwei unterschiedlichen Phasen, um letztendlich einen Commit oder Abbruch einer Transaktion durchzusetzen: Phase 1 wertet die Bedingung der einzelnen Ressourcen-Manager aus, und Phase 2 schließt die Transaktion ab.</span><span class="sxs-lookup"><span data-stu-id="1d824-433">The protocol operates in two distinct phases to ultimately commit or abort a transaction: phase one evaluates the condition of each resource manager, and phase two completes the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-434"><span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**nicht konfigurierte Komponente**</span><span class="sxs-lookup"><span data-stu-id="1d824-434"><span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**unconfigured component**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-435">Eine COM-Komponente, die nicht im com+-Katalog konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="1d824-435">A COM component that has not been configured within the COM+ catalog.</span></span> <span data-ttu-id="1d824-436">Nicht konfigurierte Komponenten können die com+-Dienste nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="1d824-436">Unconfigured components cannot make use of COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-437"><span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**Positions**</span><span class="sxs-lookup"><span data-stu-id="1d824-437"><span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**whereabouts**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-438">Für DTC-Transaktionen eine nicht transparente Datenstruktur, die die Adresse des Transaktions-Managers des Ressourcen-Managers darstellt.</span><span class="sxs-lookup"><span data-stu-id="1d824-438">For DTC transactions, an opaque data structure that represents the address of the resource manager's transaction manager.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-439"><span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**XA-Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="1d824-439"><span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**XA interfaces**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-440">Ein Standardsatz von Programmierschnittstellen, die com+-Anwendungsentwicklern ermöglichen, auf XA-kompatible Datenbanken zuzugreifen und Ressourcen-Manager zu erstellen, die mit relationalen Datenbanken, Message Queueing, Transaktions Dateien und objektorientierten Datenbanken arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1d824-440">A standard set of programming interfaces that allow COM+ application developers to access XA-compliant databases and create resource managers that operate with relational databases, message queuing, transactional files, and object-oriented databases.</span></span> <span data-ttu-id="1d824-441">Obwohl Microsoft das XA-Protokoll nicht direkt unterstützt, unterstützt Microsoft Übersetzungsfunktionen zwischen OLE-Transaktionen und XA.</span><span class="sxs-lookup"><span data-stu-id="1d824-441">Although Microsoft does not directly support the XA protocol, Microsoft does support translation facilities between OLE transactions and XA.</span></span>

</dd> <dt>

<span data-ttu-id="1d824-442"><span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**XML-Webdienste**</span><span class="sxs-lookup"><span data-stu-id="1d824-442"><span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**XML web services**</span></span>
</dt> <dd>

<span data-ttu-id="1d824-443">Einheiten der Anwendungslogik, die Daten und Dienste für andere Anwendungen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="1d824-443">Units of application logic providing data and services to other applications.</span></span> <span data-ttu-id="1d824-444">Anwendungen greifen mithilfe standardmäßiger Webprotokolle wie SOAP auf XML-Webdienste zu.</span><span class="sxs-lookup"><span data-stu-id="1d824-444">Applications access XML web services through standard Web protocols, such as SOAP.</span></span>

</dd> </dl>

 

 
