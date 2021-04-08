---
title: Registrierungsschlüssel und-Einträge für einen Typ 2-Online Speicher
description: Registrierungsschlüssel und-Einträge für einen Typ 2-Online Speicher
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Windows Media Player Online Stores, Registrierung
- Online Stores, Registrierung
- Typ 2 Online Stores, Registrierung
- Registrierung, Typ 2 Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685a26514730e7c370c698cbc9c64c29366c35ee
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101334"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a><span data-ttu-id="b91bd-107">Registrierungsschlüssel und-Einträge für einen Typ 2-Online Speicher</span><span class="sxs-lookup"><span data-stu-id="b91bd-107">Registry Keys and Entries for a Type 2 Online Store</span></span>

> [!Note]  
> <span data-ttu-id="b91bd-108">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="b91bd-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b91bd-109">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b91bd-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b91bd-110">Um einen Onlinespeicher vom Typ 2 in Windows Media Player verfügbar zu machen, muss der Onlinespeicher Anbieter die folgenden Registrierungs Unterschlüssel und Einträge auf dem Computer des Benutzers erstellen.</span><span class="sxs-lookup"><span data-stu-id="b91bd-110">To make a type 2 online store available in Windows Media Player, the online store provider must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="Apartment"
```



<span data-ttu-id="b91bd-111">In der vorangehenden Registrierungs Syntax sind die Symbole in kursiv Platzhalter für Namen und Global Unique Identifier (GUIDs), die für den Online Store spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="b91bd-111">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the online store.</span></span> <span data-ttu-id="b91bd-112">In der folgenden Tabelle werden diese Platzhalter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b91bd-112">The following table describes those placeholders.</span></span>



| <span data-ttu-id="b91bd-113">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="b91bd-113">Placeholder</span></span>    | <span data-ttu-id="b91bd-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b91bd-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b91bd-115">*keyName*</span><span class="sxs-lookup"><span data-stu-id="b91bd-115">*keyName*</span></span>      | <span data-ttu-id="b91bd-116">Eine Zeichenfolge, die zwischen Microsoft und dem Online Store vereinbart wurde.</span><span class="sxs-lookup"><span data-stu-id="b91bd-116">A string agreed upon between Microsoft and the online store.</span></span> <span data-ttu-id="b91bd-117">Diese Zeichenfolge identifiziert den Online Store eindeutig. Beispiel: "Proseware"</span><span class="sxs-lookup"><span data-stu-id="b91bd-117">This string uniquely identifies the online store.Example: "Proseware"</span></span><br/>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="b91bd-118">*flags*</span><span class="sxs-lookup"><span data-stu-id="b91bd-118">*flags*</span></span>        | <span data-ttu-id="b91bd-119">Eine bitweise **or** -Funktion von mindestens einem Plug-in-funktionsflags diese Flags geben an, ob Windows-Media Player bestimmte Methoden von [iwmpabonneptionservice](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) und [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)aufruft.</span><span class="sxs-lookup"><span data-stu-id="b91bd-119">A bitwise **OR** of one or more plug-in capability flags These flags specify whether Windows Media Player should call particular methods of [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) and [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2).</span></span> <span data-ttu-id="b91bd-120">Weitere Informationen zu unterstützten Flags finden Sie in der Tabelle mit den Plug-in-funktionsflags, die dieser Tabelle folgt. Beispiel: 00000037</span><span class="sxs-lookup"><span data-stu-id="b91bd-120">For information about supported flags, see the table of plug-in capability flags that follows this table.Example: 00000037</span></span><br/> |
| <span data-ttu-id="b91bd-121">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="b91bd-121">*clsid*</span></span>        | <span data-ttu-id="b91bd-122">Eine GUID, bei der es sich um den Klassen Bezeichner (CLSID) für die Klasse handelt, die im Plug-in des Online Stores **iwmpabonnementservice** implementiert.</span><span class="sxs-lookup"><span data-stu-id="b91bd-122">A GUID that is the class identifier (CLSID) for the class that implements **IWMPSubscriptionService** in the online store's plug-in.</span></span> <span data-ttu-id="b91bd-123">Diese GUID muss das Registrierungs Format aufweisen und mit den geschweiften Klammern vervollständigt werden. Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="b91bd-123">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                                                                                    |
| <span data-ttu-id="b91bd-124">*FriendlyName*</span><span class="sxs-lookup"><span data-stu-id="b91bd-124">*friendlyname*</span></span> | <span data-ttu-id="b91bd-125">Ein Anzeige Name für den Online Shop. Beispiel: "Proseware Music Service"</span><span class="sxs-lookup"><span data-stu-id="b91bd-125">A friendly name for the online store.Example: "Proseware Music Service"</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="b91bd-126">*pluginName*</span><span class="sxs-lookup"><span data-stu-id="b91bd-126">*pluginName*</span></span>   | <span data-ttu-id="b91bd-127">Ein Name für das Plug-in des Online Stores. Beispiel: "Proxy Dienst-Plug-in"</span><span class="sxs-lookup"><span data-stu-id="b91bd-127">A name for the online store's plug-in.Example: "Proseware Service Plug-in"</span></span><br/>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b91bd-128">*className*</span><span class="sxs-lookup"><span data-stu-id="b91bd-128">*className*</span></span>    | <span data-ttu-id="b91bd-129">Der Name der Klasse, die im Plug-in des Online Stores **iwmpabonneptionservice** implementiert. Beispiel: "cprosewareservice"</span><span class="sxs-lookup"><span data-stu-id="b91bd-129">The name of the class that implements **IWMPSubscriptionService** in the online store's plug-in.Example: "CProsewareService"</span></span><br/>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="b91bd-130">*ModuleName*</span><span class="sxs-lookup"><span data-stu-id="b91bd-130">*moduleName*</span></span>   | <span data-ttu-id="b91bd-131">Der voll qualifizierte Pfad zu der dll, die das Plug-in des Online Stores implementiert. Beispiel: "C: \\ Program Files \\ proseware \\ProsewareService.dll"</span><span class="sxs-lookup"><span data-stu-id="b91bd-131">The fully qualified path to the DLL that implements the online store's plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareService.dll"</span></span><br/>                                                                                                                                                                                                                                                |



 

<span data-ttu-id="b91bd-132">In der folgenden Tabelle werden die Plug-in-funktionsflags beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b91bd-132">The following table describes the plug-in capability flags.</span></span>



| <span data-ttu-id="b91bd-133">Flag</span><span class="sxs-lookup"><span data-stu-id="b91bd-133">Flag</span></span>                                    | <span data-ttu-id="b91bd-134">Wert</span><span class="sxs-lookup"><span data-stu-id="b91bd-134">Value</span></span> | <span data-ttu-id="b91bd-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b91bd-135">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b91bd-136">Abonnement- \_ Cap \_ allowplay</span><span class="sxs-lookup"><span data-stu-id="b91bd-136">SUBSCRIPTION\_CAP\_ALLOWPLAY</span></span>            | <span data-ttu-id="b91bd-137">0X1</span><span class="sxs-lookup"><span data-stu-id="b91bd-137">0X1</span></span>   | <span data-ttu-id="b91bd-138">Der Windows-Media Player sollte [iwmpabonneptionservice:: allowplay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay)aufruft.</span><span class="sxs-lookup"><span data-stu-id="b91bd-138">Windows Media Player should call [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).</span></span>                                                                                                                      |
| <span data-ttu-id="b91bd-139">Abonnement \_ Grenze \_ allowcdburn</span><span class="sxs-lookup"><span data-stu-id="b91bd-139">SUBSCRIPTION\_CAP\_ALLOWCDBURN</span></span>          | <span data-ttu-id="b91bd-140">0X2</span><span class="sxs-lookup"><span data-stu-id="b91bd-140">0X2</span></span>   | <span data-ttu-id="b91bd-141">Windows Media Player sollte [iwmpabonneptionservice:: allowcdburn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn)aufruft.</span><span class="sxs-lookup"><span data-stu-id="b91bd-141">Windows Media Player should call [IWMPSubscriptionService::allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).</span></span>                                                                                                                  |
| <span data-ttu-id="b91bd-142">Abonnement- \_ Cap \_ allowpdatransfer</span><span class="sxs-lookup"><span data-stu-id="b91bd-142">SUBSCRIPTION\_CAP\_ALLOWPDATRANSFER</span></span>     | <span data-ttu-id="b91bd-143">0X4</span><span class="sxs-lookup"><span data-stu-id="b91bd-143">0X4</span></span>   | <span data-ttu-id="b91bd-144">Der Windows-Media Player sollte [iwmpabonneptionservice:: allowpdatransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer)aufruft.</span><span class="sxs-lookup"><span data-stu-id="b91bd-144">Windows Media Player should call [IWMPSubscriptionService::allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).</span></span>                                                                                                        |
| <span data-ttu-id="b91bd-145">\_ \_ backgroundprocessing für Abonnement Abdeckung</span><span class="sxs-lookup"><span data-stu-id="b91bd-145">SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING</span></span> | <span data-ttu-id="b91bd-146">0X8</span><span class="sxs-lookup"><span data-stu-id="b91bd-146">0X8</span></span>   | <span data-ttu-id="b91bd-147">Windows Media Player sollte [iwmpabonneptionservice:: startbackgroundprocessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b91bd-147">Windows Media Player should call [IWMPSubscriptionService::startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).</span></span>                                                                                      |
| <span data-ttu-id="b91bd-148">Abonnement \_ Abdeckung \_ deviceavailable</span><span class="sxs-lookup"><span data-stu-id="b91bd-148">SUBSCRIPTION\_CAP\_DEVICEAVAILABLE</span></span>      | <span data-ttu-id="b91bd-149">0X10</span><span class="sxs-lookup"><span data-stu-id="b91bd-149">0X10</span></span>  | <span data-ttu-id="b91bd-150">Windows Media Player muss [IWMPSubscriptionService2::d eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b91bd-150">Windows Media Player should call [IWMPSubscriptionService2::deviceAvailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).</span></span>                                                                                                        |
| <span data-ttu-id="b91bd-151">Abonnement- \_ Cap \_ prepareforsync</span><span class="sxs-lookup"><span data-stu-id="b91bd-151">SUBSCRIPTION\_CAP\_PREPAREFORSYNC</span></span>       | <span data-ttu-id="b91bd-152">0X20</span><span class="sxs-lookup"><span data-stu-id="b91bd-152">0X20</span></span>  | <span data-ttu-id="b91bd-153">Windows Media Player muss [IWMPSubscriptionService2::p Analyse forsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).</span><span class="sxs-lookup"><span data-stu-id="b91bd-153">Windows Media Player should call [IWMPSubscriptionService2::prepareForSync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).</span></span>                                                                                                          |
| <span data-ttu-id="b91bd-154">Abonnement \_ v1- \_ Caps</span><span class="sxs-lookup"><span data-stu-id="b91bd-154">SUBSCRIPTION\_V1\_CAPS</span></span>                  | <span data-ttu-id="b91bd-155">0XF</span><span class="sxs-lookup"><span data-stu-id="b91bd-155">0XF</span></span>   | <span data-ttu-id="b91bd-156">Standard.</span><span class="sxs-lookup"><span data-stu-id="b91bd-156">Default.</span></span> <span data-ttu-id="b91bd-157">Dieser Wert wird verwendet, wenn keine registriert ist.</span><span class="sxs-lookup"><span data-stu-id="b91bd-157">This value is used if none is registered.</span></span> <span data-ttu-id="b91bd-158">Dies entspricht der Kombination von Abonnement- \_ Cap \_ allowplay, Abonnement Abdeckung \_ \_ allowcdburn, Abonnement Abdeckung \_ \_ allowpdatransfer und Abonnement Abdeckung \_ \_ backgroundprocessing.</span><span class="sxs-lookup"><span data-stu-id="b91bd-158">This is equivalent to combining SUBSCRIPTION\_CAP\_ALLOWPLAY, SUBSCRIPTION\_CAP\_ALLOWCDBURN, SUBSCRIPTION\_CAP\_ALLOWPDATRANSFER, and SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING.</span></span> |



 

<span data-ttu-id="b91bd-159">**Registrierungseinträge für Entwicklung und Tests**</span><span class="sxs-lookup"><span data-stu-id="b91bd-159">**Registry Entries for Development and Testing**</span></span>

<span data-ttu-id="b91bd-160">Wenn Sie mit der Entwicklung Ihres Online Stores beginnen, bietet Microsoft Ihnen zwei Schlüssel: einen Testschlüssel und einen Produktions Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="b91bd-160">When you begin developing your online store, Microsoft provides you with two keys: a test key and a production key.</span></span> <span data-ttu-id="b91bd-161">Während der Entwicklungs-und Testphase wird der Online Shop in Windows Media Player nur angezeigt, wenn sich der Testschlüssel oder Ihr Produktions Schlüssel in der Registrierung auf dem Computer des Benutzers befindet.</span><span class="sxs-lookup"><span data-stu-id="b91bd-161">During the development and testing phase, your online store will appear in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="b91bd-162">Weitere Informationen zu den Test-und Produktions Schlüsseln finden Sie unter [Test-und Produktions Schlüssel für einen Online Store vom Typ 2](test-and-production-keys-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="b91bd-162">For more information about the test and production keys, see [Test and Production Keys for a Type 2 Online Store](test-and-production-keys-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="b91bd-163">Platzieren Sie den Test-oder Produktions Schlüssel an folgendem Speicherort in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="b91bd-163">Place your test or production key in the following location in the registry.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



<span data-ttu-id="b91bd-164">Beachten Sie, dass der Wert des Registrierungs Eintrags Testparameter mehrere Test-oder Produktions Schlüssel angeben kann.</span><span class="sxs-lookup"><span data-stu-id="b91bd-164">Note that the value of the TestParameter registry entry can specify multiple test or production keys.</span></span> <span data-ttu-id="b91bd-165">Nehmen wir beispielsweise an, dass Proseware einen Testschlüssel mit dem Wert "1234" hat und dass die Datei "" den Testschlüssel "2345" hat.</span><span class="sxs-lookup"><span data-stu-id="b91bd-165">For example, suppose that Proseware has a test key of "1234" and Contoso has a test key of "2345".</span></span> <span data-ttu-id="b91bd-166">Der folgende Registrierungs Eintrag gibt an, dass die Test Speicher für Proseware und Microsoft Configuration Manager in der Windows-Media Player angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b91bd-166">The following registry entry specifies that the test stores for Proseware and Contoso will appear in Windows Media Player.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



<span data-ttu-id="b91bd-167">**ActiveService-Registrierungs Eintrag**</span><span class="sxs-lookup"><span data-stu-id="b91bd-167">**ActiveService Registry Entry**</span></span>

<span data-ttu-id="b91bd-168">Wenn der Benutzer einen Online Shop aktiviert, schreibt Windows Media Player Informationen in die Registrierung, die den aktiven Online Store identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b91bd-168">When the user activates an online store, Windows Media Player writes information in the registry that identifies the active online store.</span></span> <span data-ttu-id="b91bd-169">In Windows Media Player werden die Informationen an folgendem Speicherort in der Registrierung auf dem Computer des Benutzers abgelegt.</span><span class="sxs-lookup"><span data-stu-id="b91bd-169">Windows Media Player places the information in the following location in the registry on the user's computer.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



<span data-ttu-id="b91bd-170">In der vorangehenden Registrierungs Syntax ist *serviceInfo* ein Platzhalter für eine Zeichenfolge, die beschreibende Informationen zum aktiven Online Store enthält.</span><span class="sxs-lookup"><span data-stu-id="b91bd-170">In the preceding registry syntax, *serviceInfo* is a placeholder for a string that contains descriptive information about the active online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b91bd-171">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b91bd-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b91bd-172">**Referenz für Typ 2-Onlineshops**</span><span class="sxs-lookup"><span data-stu-id="b91bd-172">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





