---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f84d56ba74325b6c65fb5c06ba2db9228c78d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343779"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span data-ttu-id="30321-103"><span id="WWAN_profile_v4.element_MBNProfileExt"></span>Mbnprofileext</span><span class="sxs-lookup"><span data-stu-id="30321-103"><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt</span></span>

<span data-ttu-id="30321-104">Das **mbnprofileext** -Element ist eine Erweiterung des früheren mbnprofile-Elements.</span><span class="sxs-lookup"><span data-stu-id="30321-104">The **MBNProfileExt** element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="30321-105">Es identifiziert ein mobiles Breitband Profil mit einem umfassenderen Satz von Optionen als das mbnprofile-Element.</span><span class="sxs-lookup"><span data-stu-id="30321-105">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span>

<span data-ttu-id="30321-106">Es kann mehr als ein mbnprofileext-Element in einem Profil geben, das Profileinstellungen für einen bestimmten Satz von Betriebszuständen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="30321-106">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="30321-107">Verwenden Sie das untergeordnete [**profileconditionedon**](element-profileconditionedon.md) -Element von **mbnprofileext** , um anzugeben, welche Betriebsbedingungen ein bestimmtes Profil zum aktiven Profil machen.</span><span class="sxs-lookup"><span data-stu-id="30321-107">Use the [**ProfileConditionedOn**](element-profileconditionedon.md) child element of **MBNProfileExt** to specify which operating conditions make a particular profile the active profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="30321-108">Elementhierarchie</span><span class="sxs-lookup"><span data-stu-id="30321-108">Element hierarchy</span></span>

**<MBNProfileExt>**

## <a name="syntax"></a><span data-ttu-id="30321-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="30321-109">Syntax</span></span>

``` syntax
<MBNProfileExt>

  <!-- Child elements -->
  Name,
  Description?,
  ICONFilePath?,
  IsDefault,
  ProfileCreationType?,
  SubscriberID?,
  SimIccID,
  HomeProviderName?,
  AutoConnectOnInternet?,
  ConnectionMode?,
  Context?,
  DataRoamingPartners?,
  PurposeGroups?,
  ProfileConditionedOn?,
  IsProvisioningProfile?,
  ApnID?,
  AdminEnable?,
  AdminRoamControl?,
  IsExclusiveToOther?,
  IsLongStandingAdditionalPdpContextProfile?,
  MmsConfiguration?,
  any element in a non-schema namespace*

</MBNProfileExt>
```

### <a name="key"></a><span data-ttu-id="30321-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="30321-110">Key</span></span>

<span data-ttu-id="30321-111">`?`   optional (0 (null) oder eins)</span><span class="sxs-lookup"><span data-stu-id="30321-111">`?`   optional (zero or one)</span></span>

<span data-ttu-id="30321-112">`*`   optional (0 (null) oder mehr)</span><span class="sxs-lookup"><span data-stu-id="30321-112">`*`   optional (zero or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="30321-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="30321-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="30321-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="30321-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="30321-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="30321-115">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="30321-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="30321-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30321-117">Untergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="30321-117">Child Element</span></span></th>
<th><span data-ttu-id="30321-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30321-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30321-119"><a href="element-adminenable.md">Adminenable</a></span><span class="sxs-lookup"><span data-stu-id="30321-119"><a href="element-adminenable.md">AdminEnable</a></span></span></td>
<td><p><span data-ttu-id="30321-120">Gibt an, ob das Profil administrativ aktiviert ist. Dies ist ein neues Element für v4.</span><span class="sxs-lookup"><span data-stu-id="30321-120">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30321-121"><a href="element-adminroamcontrol.md">Adminroamcontrol</a></span><span class="sxs-lookup"><span data-stu-id="30321-121"><a href="element-adminroamcontrol.md">AdminRoamControl</a></span></span></td>
<td><p><span data-ttu-id="30321-122">Gibt an, ob das Profil administrativ durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="30321-122">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="30321-123">Dieses Element ist neu für v4.</span><span class="sxs-lookup"><span data-stu-id="30321-123">This element is new for v4.</span></span> <span data-ttu-id="30321-124">Der Wert dieses Elements ist ein <a href="simpletype-roamcontroltype.md"><strong>roamcontroltype</strong></a> -Wert.</span><span class="sxs-lookup"><span data-stu-id="30321-124">The value of this element is a <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> value.</span></span> <span data-ttu-id="30321-125">Dies ist ein optionales Element. Wenn kein Wert angegeben wird, ist <strong>allroamallowed</strong> der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="30321-125">This is an optional element; if no value is specified, then <strong>AllRoamAllowed</strong> is the default.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30321-126"><a href="element-apnid.md">Apnid</a></span><span class="sxs-lookup"><span data-stu-id="30321-126"><a href="element-apnid.md">ApnID</a></span></span></td>
<td><p><span data-ttu-id="30321-127">Eine APN-ID, die diesem Profil zugeordnet ist. Dieses Element ist neu in v4 und optional.</span><span class="sxs-lookup"><span data-stu-id="30321-127">An APN ID associated with this profile.This element is new in v4, and it is optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30321-128"><a href="element-autoconnectoninternet.md">Autoconnectoninternet</a></span><span class="sxs-lookup"><span data-stu-id="30321-128"><a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a></span></span></td>
<td><p><span data-ttu-id="30321-129">Hiermit wird angegeben, ob das mobile Breitband Gerät automatisch eine Verbindung mit einem Netzwerk herstellt.</span><span class="sxs-lookup"><span data-stu-id="30321-129">Specifies whether the Mobile Broadband device will automatically connect to a network.</span></span></p>
<p><span data-ttu-id="30321-130">Weitere Informationen finden Sie in der Dokumentation zum Element " <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>autoconnectoninternet</strong></a> " von v1.</span><span class="sxs-lookup"><span data-stu-id="30321-130">For more information, see the documentation for the v1 <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30321-131"><a href="element-connectionmode.md">ConnectionMode</a></span><span class="sxs-lookup"><span data-stu-id="30321-131"><a href="element-connectionmode.md">ConnectionMode</a></span></span></td>
<td><p><span data-ttu-id="30321-132">Gibt die Einstellung für die automatische Verbindung an, die für ein mobiles Breitband Gerät verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="30321-132">Specifies the auto connection setting to be used for a Mobile Broadband device.</span></span></p>
<p><span data-ttu-id="30321-133">Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> -Element.</span><span class="sxs-lookup"><span data-stu-id="30321-133">For more information, see the documentation for the v1 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30321-134"><a href="element-context.md">Context</a></span><span class="sxs-lookup"><span data-stu-id="30321-134"><a href="element-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="30321-135">Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="30321-135">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30321-136"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span><span class="sxs-lookup"><span data-stu-id="30321-136"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span></span></td>
<td><p><span data-ttu-id="30321-137">Gibt eine Liste der bevorzugten Netzwerkanbieter beim Roaming an.</span><span class="sxs-lookup"><span data-stu-id="30321-137">Specifies a list of preferred network providers when roaming.</span></span></p>
<p><span data-ttu-id="30321-138">Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>dataroamingpartners</strong></a> -Element.</span><span class="sxs-lookup"><span data-stu-id="30321-138">For details, see the documentation for the v1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30321-139"><a href="element-description.md">Beschreibung</a></span><span class="sxs-lookup"><span data-stu-id="30321-139"><a href="element-description.md">Description</a></span></span></td>
<td><p><span data-ttu-id="30321-140">Eine Beschreibung des Profils.</span><span class="sxs-lookup"><span data-stu-id="30321-140">A description of the profile.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30321-141"><a href="element-homeprovidername.md">HomeProviderName</a></span><span class="sxs-lookup"><span data-stu-id="30321-141"><a href="element-homeprovidername.md">HomeProviderName</a></span></span></td>
<td><p><span data-ttu-id="30321-142">Der Name des Basis Anbieters für das angegebene SIM/Gerät.</span><span class="sxs-lookup"><span data-stu-id="30321-142">The name of the home provider for the given SIM/Device.</span></span> <span data-ttu-id="30321-143">Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>homeprovidername</strong></a> -Element.</span><span class="sxs-lookup"><span data-stu-id="30321-143">For more information, see the documentation for the v1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30321-144"><a href="element-iconfilepath.md">Iconfilepath</a></span><span class="sxs-lookup"><span data-stu-id="30321-144"><a href="element-iconfilepath.md">ICONFilePath</a></span></span></td>
<td><p><span data-ttu-id="30321-145">Der Pfad zur Symbol Datei für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="30321-145">The path to the icon file for the connection.</span></span> <span data-ttu-id="30321-146">Die Benutzeroberfläche für die Betriebssystem Verbindung zeigt das Symbol an, wenn eine Verbindung mit diesem Profil hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="30321-146">The operating system connection user interface displays the icon when a connection is made using this profile.</span></span></p>
<p><span data-ttu-id="30321-147">Weitere Informationen zur Verwendung dieses Elements finden Sie in der v1-Dokumentation für <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>iconfilepath</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="30321-147">For more details on using this element, see the v1 documentation for <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30321-148"><a href="element-isdefault.md">IsDefault</a></span><span class="sxs-lookup"><span data-stu-id="30321-148"><a href="element-isdefault.md">IsDefault</a></span></span></td>
<td><p><span data-ttu-id="30321-149">Gibt an, ob dieses Profil das Standardprofil ist.</span><span class="sxs-lookup"><span data-stu-id="30321-149">Specifies whether this profile is the default profile.</span></span></p>
<p><span data-ttu-id="30321-150">Weitere Details zu diesem Element finden Sie in der v1-Dokumentation für <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="30321-150">For more detail on this element, see the v1 documentation for <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30321-151"><a href="element-isexclusivetoother.md">Isexclusivean other</a></span><span class="sxs-lookup"><span data-stu-id="30321-151"><a href="element-isexclusivetoother.md">IsExclusiveToOther</a></span></span></td>
<td><p><span data-ttu-id="30321-152">Gibt an, dass dieses Profil für andere Profile desselben Profil Satzes exklusiv ist. Dieses Element ist neu für v4.</span><span class="sxs-lookup"><span data-stu-id="30321-152">Specifies that this profile is exclusive to other profiles of the same profile set(s).This element is new for v4.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30321-153"><a href="element-islongstandingadditionalpdpcontextprofile.md">Islongstandingadditionalpdpcontextprofile</a></span><span class="sxs-lookup"><span data-stu-id="30321-153"><a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a></span></span></td>
<td><p><span data-ttu-id="30321-154">Gibt an, dass dieses Profil ein langjähriges zusätzliches PDP-Kontext Profil ist. Wenn der Wert dieses Elements " <strong>true</strong>" ist, muss <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>isadditionalpdpcontextprofile</strong></a> ebenfalls auf " <strong>true</strong>" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="30321-154">Specifies that this profile is a long-standing additional PDP context profile.If the value of this element is <strong>true</strong>, then <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must also be set to <strong>true</strong>.</span></span> <span data-ttu-id="30321-155">Dies ist ein neues Element für v4.</span><span class="sxs-lookup"><span data-stu-id="30321-155">This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30321-156"><a href="element-isprovisioningprofile.md">Isprovisioningprofile</a></span><span class="sxs-lookup"><span data-stu-id="30321-156"><a href="element-isprovisioningprofile.md">IsProvisioningProfile</a></span></span></td>
<td><p><span data-ttu-id="30321-157">Gibt an, dass dieses Profil nur für die Bereitstellung verwendet werden soll. Andernfalls ist das Profil nicht anwendbar und kann nicht verwendet werden, um einen PDP-Kontext (Packet Data Protocol) zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="30321-157">Specifies that this profile is to be used for provisioning only.Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="30321-158">Dieses Element ist neu für v4.</span><span class="sxs-lookup"><span data-stu-id="30321-158">This element is new for v4.</span></span></p>
<p><span data-ttu-id="30321-159">Wenn " <strong>isprovisioningprofile</strong> " auf "true" festgelegt ist, muss " <a href="element-isdefault.md"><strong>IsDefault</strong></a> " den Wert "false" und " <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> "</span><span class="sxs-lookup"><span data-stu-id="30321-159">If <strong>IsProvisioningProfile</strong> is true, <a href="element-isdefault.md"><strong>IsDefault</strong></a> must be false, and <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> must be manual.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30321-160"><a href="element-mmsconfiguration.md">MMSConfiguration</a></span><span class="sxs-lookup"><span data-stu-id="30321-160"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="30321-161">Konfigurationsinformationen für den Multimedia Messaging Service (MMS).</span><span class="sxs-lookup"><span data-stu-id="30321-161">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="30321-162">Zusätzlich zum Festlegen der Konfigurationselemente in diesem Element muss ein MMS-Profil über die folgenden Einstellungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="30321-162">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="30321-163">Das <a href="element-name.md"><strong>Name</strong></a> -Element muss einen systemweiten eindeutigen Namen enthalten.</span><span class="sxs-lookup"><span data-stu-id="30321-163">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="30321-164">Der <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>profilekreationtype</strong></a> muss auf " <strong>userprovisioned</strong>" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="30321-164">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="30321-165">Die <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>simiccid</strong></a> muss die ICCID der SIM enthalten, für die dieses Profil vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="30321-165">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="30321-166">Der <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> muss auf " <strong>Manual</strong>" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="30321-166">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="30321-167">Die zugehörige Ziel <a href="element-purposegroupguid.md"><strong>Gruppen-ID</strong></a> muss die GUID für die MMS-Zweck Gruppe enthalten.</span><span class="sxs-lookup"><span data-stu-id="30321-167">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="30321-168"><a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>Isadditionalpdpcontextprofile</strong></a> muss auf " <strong>true</strong>" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="30321-168">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30321-169"><a href="element-name.md">Name</a></span><span class="sxs-lookup"><span data-stu-id="30321-169"><a href="element-name.md">Name</a></span></span></td>
<td><p><span data-ttu-id="30321-170">Der Name des Profils.</span><span class="sxs-lookup"><span data-stu-id="30321-170">The name of the profile.</span></span> <span data-ttu-id="30321-171">Weitere Informationen finden Sie in der Dokumentation für das v1- <a href="../mbn/schema-name-mbnprofile-element.md"><strong>namens</strong></a> Element.</span><span class="sxs-lookup"><span data-stu-id="30321-171">For more information, see the documentation for the v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30321-172"><a href="element-profileconditionedon.md">Profileconditionedon</a></span><span class="sxs-lookup"><span data-stu-id="30321-172"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="30321-173">Gibt die Bedingungen an, die erfüllt sein müssen, damit ein Profil anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="30321-173">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="30321-174">Dieses Element ist neu für v4.</span><span class="sxs-lookup"><span data-stu-id="30321-174">This element is new for v4.</span></span> <span data-ttu-id="30321-175">Sie ermöglicht es Ihnen, mehrere Profile anzugeben, die unterschiedlichen Bedingungen gelten, und damit das richtige Profil automatisch verwendet wird, wenn es anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="30321-175">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="30321-176">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="30321-176">This element is optional.</span></span> <span data-ttu-id="30321-177">Wenn Sie ihn nicht angeben, gilt das Profil immer in Bezug auf die aufgeführten Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="30321-177">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30321-178"><a href="element-profilecreationtype.md">Profilekreationtype (in mbnprofileext)</a></span><span class="sxs-lookup"><span data-stu-id="30321-178"><a href="element-profilecreationtype.md">ProfileCreationType (in MBNProfileExt)</a></span></span></td>
<td><p><span data-ttu-id="30321-179">Gibt den Ersteller des Profils an.</span><span class="sxs-lookup"><span data-stu-id="30321-179">Specifies the creator of the profile.</span></span></p>
<p><span data-ttu-id="30321-180">Weitere Informationen zu diesem Element finden Sie in der Dokumentation für das v1 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>profilekreationtype</strong></a> -Element.</span><span class="sxs-lookup"><span data-stu-id="30321-180">For more information about this element, see the documentation for the v1 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30321-181"><a href="element-purposegroups.md">Zielstregruppen</a></span><span class="sxs-lookup"><span data-stu-id="30321-181"><a href="element-purposegroups.md">PurposeGroups</a></span></span></td>
<td><p><span data-ttu-id="30321-182">Eine optionale Liste der Gruppen von Profilen, wobei jede Gruppe Profile enthält, die für einen allgemeinen Zweck verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="30321-182">An optional list of groups of profiles, where each group includes profiles used for a common purpose.</span></span></p>
<p><span data-ttu-id="30321-183">Dieses Element ist neu für V4 des Schemas.</span><span class="sxs-lookup"><span data-stu-id="30321-183">This element is new for v4 of the schema.</span></span></p>
<p><span data-ttu-id="30321-184">Ein Profil kann in mehreren Gruppen aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="30321-184">One profile can be listed in multiple groups.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30321-185"><a href="element-simiccid.md">Simiccid</a></span><span class="sxs-lookup"><span data-stu-id="30321-185"><a href="element-simiccid.md">SimIccID</a></span></span></td>
<td><p><span data-ttu-id="30321-186">Die SIM-identikations Nummer für GSM-Geräte.</span><span class="sxs-lookup"><span data-stu-id="30321-186">The SIM Identifcation number for GSM devices.</span></span> <span data-ttu-id="30321-187">Weitere Informationen finden Sie in der Dokumentation für das v1 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>simiccid-</strong></a> Element.</span><span class="sxs-lookup"><span data-stu-id="30321-187">For more details , see the documentation for the v1 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30321-188"><a href="element-subscriberid.md">Abonnement-ID</a></span><span class="sxs-lookup"><span data-stu-id="30321-188"><a href="element-subscriberid.md">SubscriberID</a></span></span></td>
<td><p><span data-ttu-id="30321-189">Identifiziert den eindeutigen Bezeichner des Profils.</span><span class="sxs-lookup"><span data-stu-id="30321-189">Identifies the unique identifier of the profile.</span></span></p>
<p><span data-ttu-id="30321-190">Bei einem GSM-Netzwerk sollte dies die IMSI (International Mobile Subscriber Identity) der SIM und für CDMA-Geräte enthalten, die den minimalen (mobilen Identifikationsnummer) des Geräts enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="30321-190">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span></p>
<p><span data-ttu-id="30321-191">Weitere Informationen finden Sie in der Dokumentation zum <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>abonniert</strong></a> -Element von v1.</span><span class="sxs-lookup"><span data-stu-id="30321-191">For more information, see the documentation for the v1 <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>SubscriberID</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="30321-192"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="30321-192"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="30321-193">Dieses äußerste (Dokument-) Element darf nicht in anderen Elementen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="30321-193">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="30321-194">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30321-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30321-195">Namespace</span><span class="sxs-lookup"><span data-stu-id="30321-195">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
