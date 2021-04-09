---
title: Registrierungs Werte der EAP-Authenticator-Methode
description: Weitere Informationen zu den Registrierungs Werten der EAP Authenticator-Methode. Diese spezifischen Registrierungs Werte sind für EAP Authenticator-Methoden erforderlich.
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a710ca6f09914c8d111c42a8323a9c39c51f898
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949127"
---
# <a name="eap-authenticator-method-registry-values"></a><span data-ttu-id="08dfc-104">Registrierungs Werte der EAP-Authenticator-Methode</span><span class="sxs-lookup"><span data-stu-id="08dfc-104">EAP Authenticator Method Registry Values</span></span>

<span data-ttu-id="08dfc-105">Bestimmte Registrierungs Werte sind für EAP Authenticator-Methoden erforderlich.</span><span class="sxs-lookup"><span data-stu-id="08dfc-105">Specific registry values are required for EAP authenticator methods.</span></span>

## <a name="eap-authenticator-method-dll-paths"></a><span data-ttu-id="08dfc-106">DLL-Pfade der EAP-Authenticator-Methode</span><span class="sxs-lookup"><span data-stu-id="08dfc-106">EAP Authenticator Method DLL Paths</span></span>

<span data-ttu-id="08dfc-107">Der folgende Pfad gibt den Registrierungs Speicherort für reguläre EAP Authenticator-Methoden-DLLs an.</span><span class="sxs-lookup"><span data-stu-id="08dfc-107">The following path specifies the registry location for regular EAP authenticator method DLLs.</span></span>

<span data-ttu-id="08dfc-108">**HKLM \\ System \\ CCS \\ \\ -Dienste EAPHost- \\ Methoden \\ *&lt; AutorID &gt;* \\ \* &lt; eaptypeid&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="08dfc-108">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="08dfc-109">Beispielsweise wird ein Installationspfad der EAP Authenticator-Methode, der eine **AutorID** von "311" (gibt an, dass "Microsoft" der Autor ist) und die **eaptypeid** "40" angezeigt, wie folgt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="08dfc-109">For example, an EAP authenticator method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author) and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="08dfc-110">**HKLM \\ System \\ CCS- \\ Dienste \\ EAPHost- \\ Methoden \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="08dfc-110">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\40**</span></span>

<span data-ttu-id="08dfc-111">Der folgende Pfad gibt den Registrierungs Speicherort für erweiterte EAP Authenticator-Methoden-DLLs an.</span><span class="sxs-lookup"><span data-stu-id="08dfc-111">The following path specifies the registry location for extended EAP authenticator method DLLs.</span></span>

<span data-ttu-id="08dfc-112">**HKLM \\ System \\ CCS- \\ Dienste \\ EAPHost- \\ Methoden \\ *&lt; AutorID &gt;* \\ 254 \\ *&lt; VendorID &gt;* \\ \* &lt; vendortype&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="08dfc-112">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\254\\*&lt;VendorId&gt;*\\*&lt;VendorType&gt;**\*</span></span>

<span data-ttu-id="08dfc-113">Beispielsweise wird ein Installationspfad der EAP Authenticator-Methode für die **Autorisierung mit der Autorisierung** "311" (die besagt, dass "Microsoft" der Autor ist), der **VendorID** "311" und der **eaptypeid** "40" wie folgt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="08dfc-113">For example, an EAP authenticator method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author), a **VendorId** of "311", and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="08dfc-114">**HKLM \\ System \\ CCS- \\ Dienste \\ EAPHost- \\ Methoden \\ 311 \\ 254 \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="08dfc-114">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\254\\311\\40**</span></span>

> [!Note]  
> <span data-ttu-id="08dfc-115">Weitere Informationen zur Zuordnung von EAP-Methoden Typen finden Sie im Abschnitt 6,2 von [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span><span class="sxs-lookup"><span data-stu-id="08dfc-115">For more information on the allocation of EAP method types, see section 6.2 of [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span></span>

 

## <a name="registry-values"></a><span data-ttu-id="08dfc-116">Registrierungs Werte</span><span class="sxs-lookup"><span data-stu-id="08dfc-116">Registry Values</span></span>

<span data-ttu-id="08dfc-117">Die folgenden Registrierungs Werte für die Authenticator-Methode sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="08dfc-117">The following authenticator method registry values are required.</span></span>

-   [<span data-ttu-id="08dfc-118">Authentierordllpath</span><span class="sxs-lookup"><span data-stu-id="08dfc-118">AuthenticatorDllPath</span></span>](#authenticatordllpath)
-   [<span data-ttu-id="08dfc-119">Authenti-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="08dfc-119">AuthenticatorFriendlyName</span></span>](#authenticatorfriendlyname)

<span data-ttu-id="08dfc-120">Neben den oben aufgeführten Registrierungs Werten wird der folgende Authentifikator-Methoden Registrierungs Wert empfohlen.</span><span class="sxs-lookup"><span data-stu-id="08dfc-120">Besides the above registry values, the following authenticator method registry value is recommended.</span></span>

-   [<span data-ttu-id="08dfc-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08dfc-121">Properties</span></span>](#properties)

<span data-ttu-id="08dfc-122">Die verbleibenden Registrierungs Werte der Authenticator-Methode sind optional.</span><span class="sxs-lookup"><span data-stu-id="08dfc-122">The remaining authenticator method registry values are optional.</span></span>

-   [<span data-ttu-id="08dfc-123">Configclsid</span><span class="sxs-lookup"><span data-stu-id="08dfc-123">ConfigCLSID</span></span>](#configclsid)
-   [<span data-ttu-id="08dfc-124">Standalonesupportiert</span><span class="sxs-lookup"><span data-stu-id="08dfc-124">StandaloneSupported</span></span>](#standalonesupported)

## <a name="authenticatordllpath"></a><span data-ttu-id="08dfc-125">Authentierordllpath</span><span class="sxs-lookup"><span data-stu-id="08dfc-125">AuthenticatorDllPath</span></span>



| <span data-ttu-id="08dfc-126">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="08dfc-126">Constant Value</span></span> | <span data-ttu-id="08dfc-127">Authentierordllpath</span><span class="sxs-lookup"><span data-stu-id="08dfc-127">AuthenticatorDllPath</span></span>                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08dfc-128">type</span><span class="sxs-lookup"><span data-stu-id="08dfc-128">Type</span></span>           | <span data-ttu-id="08dfc-129">REG \_ Expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="08dfc-129">REG\_EXPAND\_SZ</span></span>                                                                                               |
| <span data-ttu-id="08dfc-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08dfc-130">Description</span></span>    | <span data-ttu-id="08dfc-131">Der Pfad zur EAP Authenticator-Methoden-dll.</span><span class="sxs-lookup"><span data-stu-id="08dfc-131">The path to the EAP authenticator method DLL.</span></span> <span data-ttu-id="08dfc-132">Beispiel:% systemroot% \\ system32 \\ &lt; Name \_ von \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="08dfc-132">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

## <a name="authenticatorfriendlyname"></a><span data-ttu-id="08dfc-133">Authenti-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="08dfc-133">AuthenticatorFriendlyName</span></span>



| <span data-ttu-id="08dfc-134">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="08dfc-134">Constant Value</span></span> | <span data-ttu-id="08dfc-135">Authenti-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="08dfc-135">AuthenticatorFriendlyName</span></span>                                                          |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="08dfc-136">type</span><span class="sxs-lookup"><span data-stu-id="08dfc-136">Type</span></span>           | <span data-ttu-id="08dfc-137">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="08dfc-137">REG\_SZ</span></span>                                                                            |
| <span data-ttu-id="08dfc-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08dfc-138">Description</span></span>    | <span data-ttu-id="08dfc-139">Eine Zeichenfolge, die den anzeigen Amen für die EAP-Authenticator-Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="08dfc-139">String that contains the friendly (display) name for the EAP authenticator method.</span></span> |



 

## <a name="configclsid"></a><span data-ttu-id="08dfc-140">Configclsid</span><span class="sxs-lookup"><span data-stu-id="08dfc-140">ConfigCLSID</span></span>



| <span data-ttu-id="08dfc-141">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="08dfc-141">Constant Value</span></span> | <span data-ttu-id="08dfc-142">Configclsid</span><span class="sxs-lookup"><span data-stu-id="08dfc-142">ConfigCLSID</span></span>                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08dfc-143">type</span><span class="sxs-lookup"><span data-stu-id="08dfc-143">Type</span></span>           | <span data-ttu-id="08dfc-144">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="08dfc-144">REG\_SZ</span></span>                                                                                                                               |
| <span data-ttu-id="08dfc-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08dfc-145">Description</span></span>    | <span data-ttu-id="08dfc-146">Zeichenfolge, die die Konfigurations Klassen-GUID für diese Authenticator-Methode im Format {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} enthält.</span><span class="sxs-lookup"><span data-stu-id="08dfc-146">String that contains the configuration class GUID for this authenticator method, in the format {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span></span> |



 

## <a name="properties"></a><span data-ttu-id="08dfc-147">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08dfc-147">Properties</span></span>



| <span data-ttu-id="08dfc-148">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="08dfc-148">Constant Value</span></span> | <span data-ttu-id="08dfc-149">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08dfc-149">Properties</span></span>                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08dfc-150">type</span><span class="sxs-lookup"><span data-stu-id="08dfc-150">Type</span></span>           | <span data-ttu-id="08dfc-151">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="08dfc-151">REG\_DWORD</span></span>                                                                                                                                                  |
| <span data-ttu-id="08dfc-152">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08dfc-152">Description</span></span>    | <span data-ttu-id="08dfc-153">Bits in DWORD sind so festgelegt, dass die Unterstützung für die Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="08dfc-153">Bits in the DWORD are set to indicate support for the property.</span></span> <span data-ttu-id="08dfc-154">Eine Liste der unterstützten Werte finden Sie unter [**Eigenschaften der EAP-Methode**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="08dfc-154">For a list of supported values, see [**EAP Method Properties**](eap-method-properties.md).</span></span> |



 

## <a name="standalonesupported"></a><span data-ttu-id="08dfc-155">Standalonesupportiert</span><span class="sxs-lookup"><span data-stu-id="08dfc-155">StandaloneSupported</span></span>



| <span data-ttu-id="08dfc-156">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="08dfc-156">Constant Value</span></span> | <span data-ttu-id="08dfc-157">Standalonesupportiert</span><span class="sxs-lookup"><span data-stu-id="08dfc-157">StandaloneSupported</span></span>                                             |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="08dfc-158">type</span><span class="sxs-lookup"><span data-stu-id="08dfc-158">Type</span></span>           | <span data-ttu-id="08dfc-159">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="08dfc-159">REG\_DWORD</span></span>                                                      |
| <span data-ttu-id="08dfc-160">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08dfc-160">Description</span></span>    | <span data-ttu-id="08dfc-161">0, wenn es sich um eine eigenständige Authenticator-Methode handelt. 1, wenn dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="08dfc-161">0 if this is a standalone authenticator method; 1 if it is not.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="08dfc-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08dfc-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08dfc-163">Registrierungsschlüssel für die EAP-Peer Methode</span><span class="sxs-lookup"><span data-stu-id="08dfc-163">EAP Peer Method Registry Keys</span></span>](eap-peer-method-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="08dfc-164">Registrierungs Konfiguration für erweiterte EAP-Typen</span><span class="sxs-lookup"><span data-stu-id="08dfc-164">Registry Configuration for Expanded EAP Types</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="08dfc-165">Verwenden von EAPHost</span><span class="sxs-lookup"><span data-stu-id="08dfc-165">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="08dfc-166">RFC 3748</span><span class="sxs-lookup"><span data-stu-id="08dfc-166">RFC 3748</span></span>](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




