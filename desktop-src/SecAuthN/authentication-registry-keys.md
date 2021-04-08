---
description: Wenn ein Netzwerkanbieter installiert wird, sollte Ihre Anwendung die in diesem Thema beschriebenen Registrierungsschlüssel und-Werte erstellen.
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: Registrierungsschlüssel für die Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2e42febe7516060dd61a7b751a33dcf62cb9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959968"
---
# <a name="authentication-registry-keys"></a><span data-ttu-id="903b2-103">Registrierungsschlüssel für die Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="903b2-103">Authentication Registry Keys</span></span>

<span data-ttu-id="903b2-104">Wenn ein Netzwerkanbieter installiert wird, sollte Ihre Anwendung die in diesem Thema beschriebenen Registrierungsschlüssel und-Werte erstellen.</span><span class="sxs-lookup"><span data-stu-id="903b2-104">When it installs a network provider, your application should create the registry keys and values described in this topic.</span></span> <span data-ttu-id="903b2-105">Diese Schlüssel und Werte stellen dem MPR Informationen zu den Netzwerkanbietern bereit, die auf dem System installiert sind.</span><span class="sxs-lookup"><span data-stu-id="903b2-105">These keys and values provide information to the MPR about the network providers installed on the system.</span></span> <span data-ttu-id="903b2-106">Die MPR prüft diese Schlüssel beim Start und lädt die gefundenen DLLs für den Netzwerkanbieter.</span><span class="sxs-lookup"><span data-stu-id="903b2-106">The MPR checks these keys when it starts and loads the network provider DLLs that it finds.</span></span>

<span data-ttu-id="903b2-107">Bevor Sie eine Reihe von Schlüsseln erstellen, die Informationen über Ihren Netzwerkanbieter enthalten, sollten Sie den Namen Ihres Netzwerk Anbieters dem **Bestell** Schlüssel hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="903b2-107">Before you create a set of keys to hold information about your network provider, you should add the name of your network provider to the **order** key.</span></span> <span data-ttu-id="903b2-108">Dieser Schlüssel ist ein Unterschlüssel des folgenden Schlüssels:</span><span class="sxs-lookup"><span data-stu-id="903b2-108">This key is a subkey of the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

<span data-ttu-id="903b2-109">Der **Bestell** Schlüssel enthält einen einzelnen Wert, **ProviderOrder**, der die installierten Anbieter auflistet und die Reihenfolge angibt, in der Sie während des Vorgangs ausprobiert werden sollen, der die Anbieter durchläuft, bis ein akzeptier barer Anbieter gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="903b2-109">The **order** key contains a single value, **ProviderOrder**, which lists the installed providers and specifies the order in which they should be tried during operations that cycle through providers until an accepting provider is found.</span></span>

<span data-ttu-id="903b2-110">Der **ProviderOrder** -Wert enthält eine durch Trennzeichen getrennte Liste von Schlüsselnamen.</span><span class="sxs-lookup"><span data-stu-id="903b2-110">The **ProviderOrder** value contains a comma-separated list of key names.</span></span> <span data-ttu-id="903b2-111">Jeder Schlüssel Name in **ProviderOrder** identifiziert einen Netzwerkanbieter.</span><span class="sxs-lookup"><span data-stu-id="903b2-111">Each key name in **ProviderOrder** identifies a network provider.</span></span> <span data-ttu-id="903b2-112">Wenn MPR die Anbieter durchläuft, werden diese in der Reihenfolge aufgerufen, in der Sie in der Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="903b2-112">When MPR cycles through the providers, it calls them in the order in which they appear in this list.</span></span>

<span data-ttu-id="903b2-113">Der in **ProviderOrder** festgelegte Anbieter Name sollte auch als Name des Registrierungsschlüssels verwendet werden, der Informationen zu diesem Anbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="903b2-113">The provider name set in **ProviderOrder** should also be used as the name of the registry key that contains information about that provider.</span></span> <span data-ttu-id="903b2-114">Die anbieterspezifischen Registrierungsschlüssel werden als Unterschlüssel des folgenden Schlüssels erstellt:</span><span class="sxs-lookup"><span data-stu-id="903b2-114">The provider-specific registry keys are created as subkeys of the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

<span data-ttu-id="903b2-115">Anders ausgedrückt: die in **ProviderOrder** angegebenen Anbieter Namen sind der Pfad zur Registrierung der Netzwerkanbieter spezifischen Schlüssel relativ zum folgenden Pfad:</span><span class="sxs-lookup"><span data-stu-id="903b2-115">In other words, the provider names specified in **ProviderOrder** are the path to the registry of the network provider-specific keys, relative to the following path:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

<span data-ttu-id="903b2-116">Wenn Ihr Netzwerkanbieter Dienst installiert ist, sollte die Installationsanwendung einen Schlüssel wie folgt hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="903b2-116">When your network provider service is installed, the installation application should add a key as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

<span data-ttu-id="903b2-117">Dabei steht *providerName* für den Namen des Netzwerk Anbieters, der im **ProviderOrder** -Wert des **Auftrags** Schlüssels angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="903b2-117">Where *ProviderName* is the name of the network provider as specified in the **ProviderOrder** value of the **order** key.</span></span> <span data-ttu-id="903b2-118">Der **Gruppen** Wert unter dem *providerName* -Schlüssel sollte auf "Network Provider" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="903b2-118">The **Group** value under the *ProviderName* key should be set to "NetworkProvider".</span></span> <span data-ttu-id="903b2-119">Dadurch wird der Dienst als in der Netzwerkanbieter Gruppe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="903b2-119">This identifies the service as being in the network provider group.</span></span>

<span data-ttu-id="903b2-120">Sie müssen auch einen Unterschlüssel von *providerName*, **Network Provider**, erstellen.</span><span class="sxs-lookup"><span data-stu-id="903b2-120">You must also create a subkey of *ProviderName*, **networkprovider**.</span></span> <span data-ttu-id="903b2-121">Dieser Schlüssel enthält die folgenden Werte, die den Netzwerkanbieter beschreiben.</span><span class="sxs-lookup"><span data-stu-id="903b2-121">This key contains the following values that describe the network provider.</span></span>



| <span data-ttu-id="903b2-122">Wert</span><span class="sxs-lookup"><span data-stu-id="903b2-122">Value</span></span>                       | <span data-ttu-id="903b2-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="903b2-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="903b2-124">**Name**</span><span class="sxs-lookup"><span data-stu-id="903b2-124">**Name**</span></span><br/>         | <span data-ttu-id="903b2-125">Enthält den Namen des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="903b2-125">Contains the name of the provider.</span></span> <span data-ttu-id="903b2-126">Dieser Name wird dem Benutzer als Name des Netzwerks in den Dialogfeldern zum Durchsuchen angezeigt und sollte mit dem Feld **lpprovider** , das in den Strukturen von " [**nettresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) " zurückgegeben wird, identisch sein.</span><span class="sxs-lookup"><span data-stu-id="903b2-126">This name is displayed to the user as the name of the network in the browse dialog boxes and should match the **lpProvider** field returned in [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structures.</span></span> <span data-ttu-id="903b2-127">Dieser Name muss eine Variation des Produkt namens sein, vorzugsweise mit einem Hinweis auf das Unternehmen, sodass er eindeutig und eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="903b2-127">This name should be some variation of the product name, preferably with some indication of the company as well, so that it is clear and unique.</span></span> <span data-ttu-id="903b2-128">"MS-LanMan" ist beispielsweise ein guter Name, während "the net" eine schlechte Wahl wäre.</span><span class="sxs-lookup"><span data-stu-id="903b2-128">"MS-LanMan" for example is a good name, whereas "The Net" would be a poor choice.</span></span><br/> |
| <span data-ttu-id="903b2-129">**ProviderPath**</span><span class="sxs-lookup"><span data-stu-id="903b2-129">**ProviderPath**</span></span><br/> | <span data-ttu-id="903b2-130">Enthält den vollständigen Pfad der dll, die den Netzwerkanbieter implementiert.</span><span class="sxs-lookup"><span data-stu-id="903b2-130">Contains the full path of the DLL that implements the network provider.</span></span> <span data-ttu-id="903b2-131">MPR ruft [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) auf diesem Pfad auf.</span><span class="sxs-lookup"><span data-stu-id="903b2-131">MPR calls [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) on this path.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="903b2-132">Die folgenden Werte werden nur von Netzwerkanbietern verwendet, die die Funktionen für die Verwaltung von Anmelde Informationen, [**nplogonnotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) und [**nppasswordchangenotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), unterstützen.</span><span class="sxs-lookup"><span data-stu-id="903b2-132">The following values are used only by network providers that support the credential management functions, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) and [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).</span></span>



| <span data-ttu-id="903b2-133">Wert</span><span class="sxs-lookup"><span data-stu-id="903b2-133">Value</span></span>                              | <span data-ttu-id="903b2-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="903b2-134">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="903b2-135">**Klasse**</span><span class="sxs-lookup"><span data-stu-id="903b2-135">**Class**</span></span><br/>               | <span data-ttu-id="903b2-136">Ein **DWORD** , das die Klasse oder den Typ der Anbieter Funktionalität identifiziert, die dieser Anbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="903b2-136">A **DWORD** that identifies the class, or type, of provider functionality that this provider supports.</span></span> <span data-ttu-id="903b2-137">Werte können ggf. durch den **or** -Operator verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="903b2-137">Values may be joined by the **OR** operator when appropriate.</span></span> <span data-ttu-id="903b2-138">Gültige Werte hierfür sind "WN \_ Network \_ Class", "WN \_ Credential \_ Class", "WN \_ Primary \_ Authent \_ Class" und "WN \_ Service Class" \_ .</span><span class="sxs-lookup"><span data-stu-id="903b2-138">Valid values for this are WN\_NETWORK\_CLASS, WN\_CREDENTIAL\_CLASS, WN\_PRIMARY\_AUTHENT\_CLASS, and WN\_SERVICE\_CLASS.</span></span><br/> <span data-ttu-id="903b2-139">Obwohl ein Anbieter möglicherweise die primäre Authenticator-Funktionalität unterstützt, wird ein weiterer Mittelwert verwendet, um zu bestimmen, welcher Authentifikator primär ist.</span><span class="sxs-lookup"><span data-stu-id="903b2-139">Although a provider may support primary authenticator functionality, another means will be used to determine which authenticator is primary.</span></span><br/> <span data-ttu-id="903b2-140">**Windows XP/2000:** Das wechseln primärer Authentifikatoren wird nicht unterstützt, daher wird dieser Wert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="903b2-140">**Windows XP/2000:** Switching primary authenticators is not supported, so this value is ignored.</span></span> <br/> |
| <span data-ttu-id="903b2-141">**Authentproviderpath**</span><span class="sxs-lookup"><span data-stu-id="903b2-141">**AuthentProviderPath**</span></span><br/> | <span data-ttu-id="903b2-142">Dies ist der voll qualifizierte Dateiname für die dll, von der die Funktionen zur Verwaltung von Anmelde Informationen exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="903b2-142">This is the fully qualified file name for the DLL that exports the Credential Management Functions.</span></span> <span data-ttu-id="903b2-143">Dieser Wert ist nur nützlich (aber nicht erforderlich), wenn der Anbieter als Anmelde Informations \_ Klasse oder primärer \_ Authent- \_ Klassen Anbieter identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="903b2-143">This value is useful (but not required) only when the provider is identified as being a CREDENTIAL\_CLASS or PRIMARY\_AUTHENT\_CLASS provider.</span></span> <span data-ttu-id="903b2-144">Wenn dieser Wert für einen Anbieter dieser Klasse nicht vorhanden ist, wird erwartet, dass die Anmelde Informations Verwaltungsfunktionen aus der durch den ProviderPath-Wert identifizierten dll exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="903b2-144">If this value is not present for a provider of this class, the credential management functions are expected to be exported from the DLL identified by the ProviderPath value.</span></span> <span data-ttu-id="903b2-145">Dieser Wert wird nur verwendet, wenn es wünschenswert ist, die Netzwerkfunktionen und die Funktionen der Anmelde Informationsverwaltung in separaten DLLs zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="903b2-145">This value is used only if it is desirable to package the network functions and the credential manager functions in separate DLLs.</span></span><br/>  |



 

<span data-ttu-id="903b2-146">Zusätzlich zu den Werten, die zum Registrieren von Netzwerkanbietern und Anmelde Informations Managern verwendet werden, können Sie der Registrierung einen Wert hinzufügen, um eine DLL für den Empfang von Verbindungs Benachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="903b2-146">In addition to the values used to register network providers and credential managers, you can add a value to the registry to register a DLL to receive connection notifications.</span></span> <span data-ttu-id="903b2-147">Erstellen Sie hierzu \_ \_ den Wert reg Expand SZ unter folgendem Schlüssel:</span><span class="sxs-lookup"><span data-stu-id="903b2-147">To do so, create a REG\_EXPAND\_SZ value under the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

<span data-ttu-id="903b2-148">Dieser Wert sollte den Pfad zu einer DLL angeben, die die [Verbindungs Benachrichtigungs-API](connection-notification-api.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="903b2-148">This value should specify the path to a DLL that implements the [Connection Notification API](connection-notification-api.md).</span></span> <span data-ttu-id="903b2-149">Der Name dieses Werts kann beliebig sein, solange er nicht mit bereits vorhandenen Wertnamen in Konflikt steht.</span><span class="sxs-lookup"><span data-stu-id="903b2-149">The name of this value can be anything you want, as long as it does not conflict with preexisting value names.</span></span>

## <a name="example"></a><span data-ttu-id="903b2-150">Beispiel</span><span class="sxs-lookup"><span data-stu-id="903b2-150">Example</span></span>

<span data-ttu-id="903b2-151">Das folgende Beispiel zeigt die Registrierungsschlüssel für ein System, das zwei Netzwerkanbieter installiert hat: "LanmanWorkstation" und "anothernetzvc".</span><span class="sxs-lookup"><span data-stu-id="903b2-151">The following example shows the registry keys for a system that has two network providers installed: LanmanWorkStation and AnotherNetSvc.</span></span> <span data-ttu-id="903b2-152">Anothernetzvc ist auch eine Anmelde Informationsverwaltung.</span><span class="sxs-lookup"><span data-stu-id="903b2-152">AnotherNetSvc is also a credential manager.</span></span> <span data-ttu-id="903b2-153">Im Beispiel sind die Schlüsselnamen fett formatiert, und Wertnamen sind kursiv formatiert.</span><span class="sxs-lookup"><span data-stu-id="903b2-153">In the example, key names are bold and value names are italic.</span></span>

<span data-ttu-id="903b2-154">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Network Provider** \\ **Order**</span><span class="sxs-lookup"><span data-stu-id="903b2-154">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**order**</span></span>

<span data-ttu-id="903b2-155">*ProviderOrder* = "LanmanWorkstation, anothernetzvc"</span><span class="sxs-lookup"><span data-stu-id="903b2-155">*ProviderOrder* = "LanmanWorkStation,AnotherNetSvc"</span></span>

<span data-ttu-id="903b2-156">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Network Provider** \\ **notififyees**</span><span class="sxs-lookup"><span data-stu-id="903b2-156">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**Notifyees**</span></span>

<span data-ttu-id="903b2-157">*Mynotifyapp* = "c: \\ Connect \\connect.dll"</span><span class="sxs-lookup"><span data-stu-id="903b2-157">*MyNotifyApp* = "c:\\connect\\connect.dll"</span></span>

<span data-ttu-id="903b2-158">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkstation**</span><span class="sxs-lookup"><span data-stu-id="903b2-158">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**LanmanWorkStation**</span></span>\\

<span data-ttu-id="903b2-159">*Group* = "Network Provider"</span><span class="sxs-lookup"><span data-stu-id="903b2-159">*Group* = "NetworkProvider"</span></span>

<span data-ttu-id="903b2-160">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkstation** \\ **Network Provider**</span><span class="sxs-lookup"><span data-stu-id="903b2-160">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**LanmanWorkStation**\\**NetworkProvider**</span></span>

<span data-ttu-id="903b2-161">*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"</span><span class="sxs-lookup"><span data-stu-id="903b2-161">*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"</span></span>

<span data-ttu-id="903b2-162">*Class* = 0x00000001 (WN- \_ Netzwerk \_ Klasse)</span><span class="sxs-lookup"><span data-stu-id="903b2-162">*Class* = 0x00000001 (WN\_NETWORK\_CLASS)</span></span>

<span data-ttu-id="903b2-163">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **anothernetzvc**</span><span class="sxs-lookup"><span data-stu-id="903b2-163">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**AnotherNetSvc**</span></span>\\

<span data-ttu-id="903b2-164">*Group* = "Network Provider"</span><span class="sxs-lookup"><span data-stu-id="903b2-164">*Group* = "NetworkProvider"</span></span>

<span data-ttu-id="903b2-165">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **anothernetzwerkvc** \\ **Network Provider**</span><span class="sxs-lookup"><span data-stu-id="903b2-165">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**AnotherNetSvc**\\**NetworkProvider**</span></span>

<span data-ttu-id="903b2-166">*Name* = "ein anderes Netzwerk"*ProviderPath* = "c: \\ andere \\anet.dll"</span><span class="sxs-lookup"><span data-stu-id="903b2-166">*Name* = "Another Network"*ProviderPath* = "c:\\another\\anet.dll"</span></span>

<span data-ttu-id="903b2-167">*Class* = 0x00000003 (WN- \_ Netzwerk \_ Klasse \| WN \_ Credential \_ Class)</span><span class="sxs-lookup"><span data-stu-id="903b2-167">*Class* = 0x00000003 (WN\_NETWORK\_CLASS \| WN\_CREDENTIAL\_CLASS)</span></span>

<span data-ttu-id="903b2-168">*Authentproviderpath* = "c: \\ andere \\anetCM.dll"</span><span class="sxs-lookup"><span data-stu-id="903b2-168">*AuthentProviderPath* = "c:\\another\\anetCM.dll"</span></span>

 

