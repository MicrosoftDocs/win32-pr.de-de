---
title: Registrierungs Werte der EAP-Peer Methode
description: Erfahren Sie mehr über die spezifischen Registrierungs Werte, die für EAP-Peer Methoden erforderlich sind. Hier finden Sie eine Liste der Registrierungs Werte und weitere verfügbare Ressourcen.
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796260a25f824ffe52ada7cdfadfb7a25f05d491
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316491"
---
# <a name="eap-peer-method-registry-values"></a><span data-ttu-id="2b1f4-104">Registrierungs Werte der EAP-Peer Methode</span><span class="sxs-lookup"><span data-stu-id="2b1f4-104">EAP Peer Method Registry Values</span></span>

<span data-ttu-id="2b1f4-105">Bestimmte Registrierungs Werte sind für EAP-Peer Methoden erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-105">Specific registry values are required for EAP peer methods.</span></span>

## <a name="eap-peer-method-dll-paths"></a><span data-ttu-id="2b1f4-106">DLL-Pfade der EAP-Peer Methode</span><span class="sxs-lookup"><span data-stu-id="2b1f4-106">EAP Peer Method DLL Paths</span></span>

<span data-ttu-id="2b1f4-107">Der folgende Pfad gibt den Registrierungs Speicherort für reguläre DLLs der EAP-Peer Methode an.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-107">The following path specifies the registry location for regular EAP peer method DLLs.</span></span>

<span data-ttu-id="2b1f4-108">**HKLM \\ System \\ CCS \\ \\ -Dienste EAPHost- \\ Methoden \\ *&lt; AutorID &gt;* \\ \* &lt; eaptypeid&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="2b1f4-108">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="2b1f4-109">Beispielsweise wird ein Registrierungs Pfad für die EAP-Methoden Installation angegeben, der eine **autoriid** von "311" (die besagt, dass "Microsoft" der Autor ist) und die **eaptypeid** "40" erhalten.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-109">For example, an EAP method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author) and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="2b1f4-110">**HKLM \\ System \\ CCS- \\ Dienste \\ EAPHost- \\ Methoden \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="2b1f4-110">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\40**</span></span>

<span data-ttu-id="2b1f4-111">Der folgende Pfad gibt den Registrierungs Speicherort für erweiterte EAP-Methoden-DLLs an.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-111">The following path specifies the registry location for extended EAP method DLLs.</span></span>

> [!Note]  
> <span data-ttu-id="2b1f4-112">Erweiterte EAP-Methoden-DLLs werden in Windows Vista mit Service Pack 1 (SP1) oder höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-112">Extended EAP method DLLs are supported in Windows Vista with Service Pack 1 (SP1) or later.</span></span>

 

<span data-ttu-id="2b1f4-113">**HKLM \\ System \\ CCS- \\ Dienste \\ EAPHost- \\ Methoden \\ *&lt; AutorID &gt;* \\ 254 \\ *&lt; VendorID &gt;* \\ \* &lt; eaptypeid&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="2b1f4-113">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\254\\*&lt;VendorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="2b1f4-114">Beispielsweise wird ein Registrierungs Pfad der EAP-Methoden Installation mit der **Autorisierung** "311" (die besagt, dass "Microsoft" der Autor ist), der **VendorID** "311" und der **eaptypeid** "40" wie folgt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-114">For example, an EAP method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author), a **VendorId** of "311", and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="2b1f4-115">**HKLM \\ System \\ CCS- \\ Dienste \\ EAPHost- \\ Methoden \\ 311 \\ 254 \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="2b1f4-115">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\254\\311\\40**</span></span>

> [!Note]  
> <span data-ttu-id="2b1f4-116">Weitere Informationen zur Zuordnung von EAP-Methoden Typen finden Sie im Abschnitt 6,2 von [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span><span class="sxs-lookup"><span data-stu-id="2b1f4-116">For more information on the allocation of EAP method types, see section 6.2 of [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span></span>

 

## <a name="registry-values"></a><span data-ttu-id="2b1f4-117">Registrierungs Werte</span><span class="sxs-lookup"><span data-stu-id="2b1f4-117">Registry Values</span></span>

<span data-ttu-id="2b1f4-118">Die folgenden Registrierungs Werte für die EAPHost-Peer Methode sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-118">The following EAPHost peer method registry values are required.</span></span>

-   [<span data-ttu-id="2b1f4-119">Peerdllpath</span><span class="sxs-lookup"><span data-stu-id="2b1f4-119">PeerDllPath</span></span>](#peerdllpath)
-   [<span data-ttu-id="2b1f4-120">Peer FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2b1f4-120">PeerFriendlyName</span></span>](#peerfriendlyname)
-   [<span data-ttu-id="2b1f4-121">Peer invokepassworddialog</span><span class="sxs-lookup"><span data-stu-id="2b1f4-121">PeerInvokePasswordDialog</span></span>](#peerinvokepassworddialog)
-   [<span data-ttu-id="2b1f4-122">Peer invokeusernamedialog</span><span class="sxs-lookup"><span data-stu-id="2b1f4-122">PeerInvokeUsernameDialog</span></span>](#peerinvokeusernamedialog)

<span data-ttu-id="2b1f4-123">Die folgenden Registrierungs Werte für die AP-Peer Methode werden empfohlen.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-123">The following AP peer method registry values are recommended.</span></span>

-   [<span data-ttu-id="2b1f4-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2b1f4-124">Properties</span></span>](#properties)

<span data-ttu-id="2b1f4-125">Die folgenden Registrierungs Werte für die AP-Peer Methode sind optional.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-125">The following AP peer method registry values are optional.</span></span>

-   [<span data-ttu-id="2b1f4-126">Peerconfiguipath</span><span class="sxs-lookup"><span data-stu-id="2b1f4-126">PeerConfigUIPath</span></span>](#peerconfiguipath)
-   [<span data-ttu-id="2b1f4-127">Peeridentitypath</span><span class="sxs-lookup"><span data-stu-id="2b1f4-127">PeerIdentityPath</span></span>](#peeridentitypath)
-   [<span data-ttu-id="2b1f4-128">Peerinteractiveuipath</span><span class="sxs-lookup"><span data-stu-id="2b1f4-128">PeerInteractiveUIPath</span></span>](#peerinteractiveuipath)
-   [<span data-ttu-id="2b1f4-129">Peerrequirements configui</span><span class="sxs-lookup"><span data-stu-id="2b1f4-129">PeerRequireConfigUI</span></span>](#peerrequireconfigui)

### <a name="peerconfiguipath"></a><span data-ttu-id="2b1f4-130">Peerconfiguipath</span><span class="sxs-lookup"><span data-stu-id="2b1f4-130">PeerConfigUIPath</span></span>



| <span data-ttu-id="2b1f4-131">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="2b1f4-131">Constant Value</span></span> | <span data-ttu-id="2b1f4-132">Peerconfiguipath</span><span class="sxs-lookup"><span data-stu-id="2b1f4-132">PeerConfigUIPath</span></span>                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b1f4-133">type</span><span class="sxs-lookup"><span data-stu-id="2b1f4-133">Type</span></span>           | <span data-ttu-id="2b1f4-134">REG \_ Expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="2b1f4-134">REG\_EXPAND\_SZ</span></span>                                                                                                                                        |
| <span data-ttu-id="2b1f4-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b1f4-135">Description</span></span>    | <span data-ttu-id="2b1f4-136">Der Pfad zur dll, die die Implementierung des Dialog Felds für die Benutzerkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-136">The path to the DLL that contains the implementation of the user configuration dialog.</span></span> <span data-ttu-id="2b1f4-137">Beispiel:% systemroot% \\ system32 \\ &lt; Name \_ von \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-137">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerdllpath"></a><span data-ttu-id="2b1f4-138">Peerdllpath</span><span class="sxs-lookup"><span data-stu-id="2b1f4-138">PeerDllPath</span></span>



| <span data-ttu-id="2b1f4-139">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="2b1f4-139">Constant Value</span></span> | <span data-ttu-id="2b1f4-140">Peerdllpath</span><span class="sxs-lookup"><span data-stu-id="2b1f4-140">PeerDllPath</span></span>                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b1f4-141">type</span><span class="sxs-lookup"><span data-stu-id="2b1f4-141">Type</span></span>           | <span data-ttu-id="2b1f4-142">REG \_ Expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="2b1f4-142">REG\_EXPAND\_SZ</span></span>                                                                                 |
| <span data-ttu-id="2b1f4-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b1f4-143">Description</span></span>    | <span data-ttu-id="2b1f4-144">Der Pfad zur EAP-Methoden-dll.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-144">The path to the EAP method DLL.</span></span> <span data-ttu-id="2b1f4-145">Beispiel:% systemroot% \\ system32 \\ &lt; Name \_ von \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-145">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerfriendlyname"></a><span data-ttu-id="2b1f4-146">Peer FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2b1f4-146">PeerFriendlyName</span></span>



| <span data-ttu-id="2b1f4-147">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="2b1f4-147">Constant Value</span></span> | <span data-ttu-id="2b1f4-148">Peer FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2b1f4-148">PeerFriendlyName</span></span>                                                     |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="2b1f4-149">type</span><span class="sxs-lookup"><span data-stu-id="2b1f4-149">Type</span></span>           | <span data-ttu-id="2b1f4-150">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="2b1f4-150">REG\_SZ</span></span>                                                              |
| <span data-ttu-id="2b1f4-151">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b1f4-151">Description</span></span>    | <span data-ttu-id="2b1f4-152">Eine Zeichenfolge, die den anzeigen Amen für die EAP-Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-152">String that contains the friendly (display) name for the EAP method.</span></span> |



 

### <a name="peeridentitypath"></a><span data-ttu-id="2b1f4-153">Peeridentitypath</span><span class="sxs-lookup"><span data-stu-id="2b1f4-153">PeerIdentityPath</span></span>



| <span data-ttu-id="2b1f4-154">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="2b1f4-154">Constant Value</span></span> | <span data-ttu-id="2b1f4-155">Peeridentitypath</span><span class="sxs-lookup"><span data-stu-id="2b1f4-155">PeerIdentityPath</span></span>                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b1f4-156">type</span><span class="sxs-lookup"><span data-stu-id="2b1f4-156">Type</span></span>           | <span data-ttu-id="2b1f4-157">REG \_ Expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="2b1f4-157">REG\_EXPAND\_SZ</span></span>                                                                                                                                      |
| <span data-ttu-id="2b1f4-158">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b1f4-158">Description</span></span>    | <span data-ttu-id="2b1f4-159">Der Pfad zur dll, die die Implementierung der Benutzer Identitäts Funktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-159">The path to the DLL that contains the implementation of the user identity functions.</span></span> <span data-ttu-id="2b1f4-160">Beispiel:% systemroot% \\ system32 \\ &lt; Name \_ von \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-160">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerinteractiveuipath"></a><span data-ttu-id="2b1f4-161">Peerinteractiveuipath</span><span class="sxs-lookup"><span data-stu-id="2b1f4-161">PeerInteractiveUIPath</span></span>



| <span data-ttu-id="2b1f4-162">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="2b1f4-162">Constant Value</span></span> | <span data-ttu-id="2b1f4-163">Peerinteractiveuipath</span><span class="sxs-lookup"><span data-stu-id="2b1f4-163">PeerInteractiveUIPath</span></span>                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b1f4-164">type</span><span class="sxs-lookup"><span data-stu-id="2b1f4-164">Type</span></span>           | <span data-ttu-id="2b1f4-165">REG \_ Expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="2b1f4-165">REG\_EXPAND\_SZ</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="2b1f4-166">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b1f4-166">Description</span></span>    | <span data-ttu-id="2b1f4-167">Der Pfad zur dll, die die Implementierung der interaktiven Benutzeroberfläche enthält, die zum Abrufen von Benutzerinformationen während der Ausführung der EAP-Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-167">The path to the DLL that contains the implementation of the interactive user interface used to obtain user information during execution of the EAP method.</span></span> <span data-ttu-id="2b1f4-168">Beispiel:% systemroot% \\ system32 \\ &lt; Name \_ von \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-168">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerinvokepassworddialog"></a><span data-ttu-id="2b1f4-169">Peer invokepassworddialog</span><span class="sxs-lookup"><span data-stu-id="2b1f4-169">PeerInvokePasswordDialog</span></span>



| <span data-ttu-id="2b1f4-170">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="2b1f4-170">Constant Value</span></span> | <span data-ttu-id="2b1f4-171">Peer invokepassworddialog</span><span class="sxs-lookup"><span data-stu-id="2b1f4-171">PeerInvokePasswordDialog</span></span>                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b1f4-172">type</span><span class="sxs-lookup"><span data-stu-id="2b1f4-172">Type</span></span>           | <span data-ttu-id="2b1f4-173">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="2b1f4-173">REG\_DWORD</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="2b1f4-174">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b1f4-174">Description</span></span>    | <span data-ttu-id="2b1f4-175">1: um Anmelde Informationen mithilfe des generischen EAPHost-Kennworts und der Domäne zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-175">1- to get credentials using the generic EAPHost password and domain dialog box.</span></span> <span data-ttu-id="2b1f4-176">0-so verwenden Sie ein benutzerdefiniertes Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-176">0 - to use a custom dialog box.</span></span> <span data-ttu-id="2b1f4-177">Wenn das generische Dialogfeld verwendet wird, werden die Anmelde Informationen von der [**eappeersetanmelde**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) -Methode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-177">If the generic dialog box is used, credentials are set by the [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) method.</span></span> |



 

### <a name="peerinvokeusernamedialog"></a><span data-ttu-id="2b1f4-178">Peer invokeusernamedialog</span><span class="sxs-lookup"><span data-stu-id="2b1f4-178">PeerInvokeUsernameDialog</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2b1f4-179">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="2b1f4-179">Constant Value</span></span></th>
<th><span data-ttu-id="2b1f4-180">Peer invokeusernamedialog</span><span class="sxs-lookup"><span data-stu-id="2b1f4-180">PeerInvokeUsernameDialog</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b1f4-181">type</span><span class="sxs-lookup"><span data-stu-id="2b1f4-181">Type</span></span></td>
<td><span data-ttu-id="2b1f4-182">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2b1f4-182">REG_DWORD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b1f4-183">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b1f4-183">Description</span></span></td>
<td><ul>
<li><span data-ttu-id="2b1f4-184">1: zum erhalten von Anmelde Informationen im Dialogfeld "generischer EAPHost-Benutzername".</span><span class="sxs-lookup"><span data-stu-id="2b1f4-184">1 - to get credentials using the generic EAPHost user name dialog box.</span></span></li>
<li><span data-ttu-id="2b1f4-185">0-so verwenden Sie ein benutzerdefiniertes Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-185">0- to use a custom dialog box.</span></span></li>
</ul>
<span data-ttu-id="2b1f4-186">Wenn das generische Dialogfeld verwendet wird, werden die Anmelde Informationen von der [<strong>eappeersetanmelde</strong>Informationen] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeersetcredentials)-Methode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-186">If the generic dialog box is used, credentials are set by the [<strong>EapPeerSetCredentials</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) method.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="peerrequireconfigui"></a><span data-ttu-id="2b1f4-187">Peerrequirements configui</span><span class="sxs-lookup"><span data-stu-id="2b1f4-187">PeerRequireConfigUI</span></span>



| <span data-ttu-id="2b1f4-188">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="2b1f4-188">Constant Value</span></span> | <span data-ttu-id="2b1f4-189">Peerrequirements configui</span><span class="sxs-lookup"><span data-stu-id="2b1f4-189">PeerRequireConfigUI</span></span>                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b1f4-190">type</span><span class="sxs-lookup"><span data-stu-id="2b1f4-190">Type</span></span>           | <span data-ttu-id="2b1f4-191">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="2b1f4-191">REG\_DWORD</span></span>                                                                                 |
| <span data-ttu-id="2b1f4-192">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b1f4-192">Description</span></span>    | <span data-ttu-id="2b1f4-193">0, wenn für diese Methode ein Dialogfeld für die Konfigurations Benutzeroberfläche implementiert ist. 1, wenn dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-193">0 if a configuration user interface dialog is implemented for this method; 1 if it is not.</span></span> |



 

### <a name="properties"></a><span data-ttu-id="2b1f4-194">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2b1f4-194">Properties</span></span>



| <span data-ttu-id="2b1f4-195">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="2b1f4-195">Constant Value</span></span> | <span data-ttu-id="2b1f4-196">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2b1f4-196">Properties</span></span>                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b1f4-197">type</span><span class="sxs-lookup"><span data-stu-id="2b1f4-197">Type</span></span>           | <span data-ttu-id="2b1f4-198">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="2b1f4-198">REG\_DWORD</span></span>                                                                                                                                                  |
| <span data-ttu-id="2b1f4-199">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b1f4-199">Description</span></span>    | <span data-ttu-id="2b1f4-200">Bits in DWORD sind so festgelegt, dass die Unterstützung für die Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2b1f4-200">Bits in the DWORD are set to indicate support for the property.</span></span> <span data-ttu-id="2b1f4-201">Eine Liste der unterstützten Werte finden Sie unter [**Eigenschaften der EAP-Methode**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="2b1f4-201">For a list of supported values, see [**EAP Method Properties**](eap-method-properties.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2b1f4-202">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b1f4-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b1f4-203">Registrierungsschlüssel für die EAP-Authenticator-Methode</span><span class="sxs-lookup"><span data-stu-id="2b1f4-203">EAP Authenticator Method Registry Keys</span></span>](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="2b1f4-204">Registrierungs Konfiguration für erweiterte EAP-Typen</span><span class="sxs-lookup"><span data-stu-id="2b1f4-204">Registry Configuration for Expanded EAP Types</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="2b1f4-205">Verwenden von EAPHost</span><span class="sxs-lookup"><span data-stu-id="2b1f4-205">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="2b1f4-206">RFC 3748</span><span class="sxs-lookup"><span data-stu-id="2b1f4-206">RFC 3748</span></span>](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 