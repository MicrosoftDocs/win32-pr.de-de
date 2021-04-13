---
title: WSMAN-Objekt (WSManDisp. h)
description: Stellt Methoden und Eigenschaften bereit, mit denen eine Sitzung erstellt wird, die durch ein Sitzungs Objekt dargestellt wird.
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- WSMAN-Objekt Windows-Remoteverwaltung
- WSMAN-Objekt Windows-Remoteverwaltung, beschrieben
topic_type:
- apiref
api_name:
- WSMan
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02cb92b2d72d657791d4a16bd1e999b77645a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391584"
---
# <a name="wsman-object"></a><span data-ttu-id="469ec-105">WSMAN-Objekt</span><span class="sxs-lookup"><span data-stu-id="469ec-105">WSMan object</span></span>

<span data-ttu-id="469ec-106">Stellt Methoden und Eigenschaften bereit, mit denen eine Sitzung erstellt wird, die durch ein [**Sitzungs**](session.md) Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="469ec-106">Provides methods and properties used to create a session, represented by a [**Session**](session.md) object.</span></span> <span data-ttu-id="469ec-107">Alle Windows-Remoteverwaltung Vorgänge erfordern das Erstellen einer [**Sitzung**](session.md) , die eine Verbindung mit einem Remote Computer, einem [*Base Management Controller*](windows-remote-management-glossary.md) (BMC) oder dem lokalen Computer herstellt.</span><span class="sxs-lookup"><span data-stu-id="469ec-107">Any Windows Remote Management operations require creation of a [**Session**](session.md) that connects to a remote computer, [*base management controller*](windows-remote-management-glossary.md) (BMC), or the local computer.</span></span> <span data-ttu-id="469ec-108">Zu den Vorgängen gehören das Erstellen, schreiben, Auflisten von Daten oder das Aufrufen von Methoden.</span><span class="sxs-lookup"><span data-stu-id="469ec-108">Operations include getting, writing, enumerating data, or invoking methods.</span></span>

## <a name="members"></a><span data-ttu-id="469ec-109">Member</span><span class="sxs-lookup"><span data-stu-id="469ec-109">Members</span></span>

<span data-ttu-id="469ec-110">Das **WSMAN** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="469ec-110">The **WSMan** object has these types of members:</span></span>

-   [<span data-ttu-id="469ec-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="469ec-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="469ec-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="469ec-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="469ec-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="469ec-113">Methods</span></span>

<span data-ttu-id="469ec-114">Das **WSMAN** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="469ec-114">The **WSMan** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="469ec-115">Methode</span><span class="sxs-lookup"><span data-stu-id="469ec-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="469ec-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="469ec-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="469ec-117"><a href="wsman-createconnectionoptions.md"><strong>"Kreateconnectionoptions"</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-117"><a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-118">Erstellt ein <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> -Objekt, das den Benutzernamen und das Kennwort angibt, die beim Erstellen einer Remote Sitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="469ec-118">Creates a <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> object that specifies the user name and password used when creating a remote session.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="469ec-119"><a href="wsman-createresourcelocator.md"><strong>"Kreateresourcelocator"</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-119"><a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-120">Erstellt ein <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> -Objekt, das Folgendes angeben kann:</span><span class="sxs-lookup"><span data-stu-id="469ec-120">Creates a <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> object that can specify:</span></span><br/>
<ul>
<li><span data-ttu-id="469ec-121">Der gesamte Pfad zu einer <a href="windows-remote-management-glossary.md"><em>Ressource</em></a> oder einem einzelnen Datenelement.</span><span class="sxs-lookup"><span data-stu-id="469ec-121">The complete path to a <a href="windows-remote-management-glossary.md"><em>resource</em></a> or a single piece of data.</span></span></li>
<li><span data-ttu-id="469ec-122">Eine <a href="windows-remote-management-glossary.md"><em>Auswahl</em></a> für eine bestimmte Instanz einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="469ec-122">A <a href="windows-remote-management-glossary.md"><em>selector</em></a> for a specific instance of a resource.</span></span></li>
<li><span data-ttu-id="469ec-123">Eine <a href="windows-remote-management-glossary.md"><em>Option</em></a> , die dem Ressourcenanbieter zusätzliche Daten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="469ec-123">An <a href="windows-remote-management-glossary.md"><em>option</em></a> that supplies additional data to the resource provider.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="469ec-124"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-124"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-125">Erstellt ein <a href="session.md"><strong>Sitzungs</strong></a> Objekt, das dann für nachfolgende Netzwerk Vorgänge verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="469ec-125">Creates a <a href="session.md"><strong>Session</strong></a> object that can then be used for subsequent network operations.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="469ec-126"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMAN. enumerationflaghierarchydeep</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-126"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan.EnumerationFlagHierarchyDeep</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-127">Gibt den Wert des <strong>Enumerationsflags enumerationflaghierarchydeep</strong> zur Verwendung im <em>Flags</em> -Parameter von <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>zurück.</span><span class="sxs-lookup"><span data-stu-id="469ec-127">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyDeep</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="469ec-128"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMAN. enumerationflaghierarchydeepbasepropsonly</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-128"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan.EnumerationFlagHierarchyDeepBasePropsOnly</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-129">Gibt den Wert des <strong>Enumerationsflags enumerationflaghierarchydeepbasepropsonly</strong> zur Verwendung im <em>Flags</em> -Parameter von <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>zurück.</span><span class="sxs-lookup"><span data-stu-id="469ec-129">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="469ec-130"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMAN. enumerationflaghierarchyflache</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-130"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan.EnumerationFlagHierarchyShallow</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-131">Gibt den Wert des <strong>Enumerationsflags enumerationflaghierarchyflache</strong> zurück, der im <em>Flags</em> -Parameter von <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="469ec-131">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyShallow</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="469ec-132"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMAN. enumerationflagnonxmltext</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-132"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan.EnumerationFlagNonXmlText</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-133">Gibt den Wert der Enumerationskonstante <strong>wsmanflagnonxmltext</strong> zurück, der im <em>Flags</em> -Parameter der <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a> -Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="469ec-133">Returns the value of the enumeration constant <strong>WSManFlagNonXmlText</strong> for use in the <em>flags</em> parameter of the <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a> method.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="469ec-134"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMAN. enumerationflagreturnetpr</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-134"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan.EnumerationFlagReturnEPR</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-135">Gibt den Wert des <strong>Enumerationsflags enumerationflagreturnetpr</strong> zur Verwendung im <em>Flags</em> -Parameter von <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>zurück.</span><span class="sxs-lookup"><span data-stu-id="469ec-135">Returns the value of the enumeration flag <strong>EnumerationFlagReturnEPR</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="469ec-136"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMAN. enumerationflagreturnobject</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-136"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan.EnumerationFlagReturnObject</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-137">Gibt den Wert des <strong>Enumerationsflags enumerationflagreturnobject</strong> zurück, das im <em>Flags</em> -Parameter von <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="469ec-137">Returns the value of the enumeration flag <strong>EnumerationFlagReturnObject</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="469ec-138"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMAN. enumerationflagreturnobjectandepr</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-138"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan.EnumerationFlagReturnObjectAndEPR</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-139">Gibt den Wert des <strong>Enumerationsflags enumerationflagreturnobjectandepr</strong> zurück, der im <em>Flags</em> -Parameter von <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="469ec-139">Returns the value of the enumeration flag <strong>EnumerationFlagReturnObjectAndEPR</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="469ec-140"><a href="wsman-geterrormessage.md"><strong>WSMAN. getErrorMessage</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-140"><a href="wsman-geterrormessage.md"><strong>WSMan.GetErrorMessage</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-141">Gibt eine formatierte Zeichenfolge zurück, die den Text einer Fehlernummer enthält.</span><span class="sxs-lookup"><span data-stu-id="469ec-141">Returns a formatted string containing the text of an error number.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="469ec-142"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMAN. sessionflagkredusernamepassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-142"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan.SessionFlagCredUsernamePassword</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-143">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagkredusernamepassword</strong> für die Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.</span><span class="sxs-lookup"><span data-stu-id="469ec-143">Returns the value of the authentication flag <strong>WSManFlagCredUsernamePassword</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="469ec-144"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMAN. sessionflagenablespnserverport</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-144"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan.SessionFlagEnableSPNServerPort</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-145">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagenablespnserverport</strong> für die Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.</span><span class="sxs-lookup"><span data-stu-id="469ec-145">Returns the value of the authentication flag <strong>WSManFlagEnableSPNServerPort</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="469ec-146"><a href="wsman-sessionflagnoencryption.md"><strong>WSMAN. sessionflagnoencryption</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-146"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan.SessionFlagNoEncryption</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-147">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagnoencryption</strong> zur Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.</span><span class="sxs-lookup"><span data-stu-id="469ec-147">Returns the value of the authentication flag <strong>WSManFlagNoEncryption</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="469ec-148"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMAN. sessionflagskipcacheck</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-148"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan.SessionFlagSkipCACheck</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-149">Gibt den Wert des <strong>wsmanflagskipcacheck</strong> -Authentifizierungsflags für die Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.</span><span class="sxs-lookup"><span data-stu-id="469ec-149">Returns the value of the <strong>WSManFlagSkipCACheck</strong> authentication flag for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="469ec-150"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMAN. sessionflagskipcncheck</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-150"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan.SessionFlagSkipCNCheck</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-151">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagskipcncheck</strong> zur Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.</span><span class="sxs-lookup"><span data-stu-id="469ec-151">Returns the value of the authentication flag <strong>WSManFlagSkipCNCheck</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="469ec-152"><a href="wsman-sessionflagusebasic.md"><strong>WSMAN. sessionflagusebasic</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-152"><a href="wsman-sessionflagusebasic.md"><strong>WSMan.SessionFlagUseBasic</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-153">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagusebasic</strong> für die Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.</span><span class="sxs-lookup"><span data-stu-id="469ec-153">Returns the value of the authentication flag <strong>WSManFlagUseBasic</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="469ec-154"><a href="wsman-sessionflagusedigest.md"><strong>WSMAN. sessionflagusedigest</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-154"><a href="wsman-sessionflagusedigest.md"><strong>WSMan.SessionFlagUseDigest</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-155">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagusedigest</strong> zur Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.</span><span class="sxs-lookup"><span data-stu-id="469ec-155">Returns the value of the authentication flag <strong>WSManFlagUseDigest</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="469ec-156"><a href="wsman-sessionflagusekerberos.md"><strong>WSMAN. sessionflagusekerberos</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-156"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan.SessionFlagUseKerberos</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-157">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagusekerberos</strong> für die Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.</span><span class="sxs-lookup"><span data-stu-id="469ec-157">Returns the value of the authentication flag <strong>WSManFlagUseKerberos</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="469ec-158"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMAN. sessionflagusenegotiate</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-158"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan.SessionFlagUseNegotiate</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-159">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagusenegotiate</strong> zur Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.</span><span class="sxs-lookup"><span data-stu-id="469ec-159">Returns the value of the authentication flag <strong>WSManFlagUseNegotiate</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="469ec-160"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMAN. sessionflagusenoauthentication</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-160"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan.SessionFlagUseNoAuthentication</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-161">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagusenoauthentication</strong> für die Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.</span><span class="sxs-lookup"><span data-stu-id="469ec-161">Returns the value of the authentication flag <strong>WSManFlagUseNoAuthentication</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="469ec-162"><a href="wsman-sessionflagutf8.md"><strong>WSMAN. SessionFlagUTF8</strong></a></span><span class="sxs-lookup"><span data-stu-id="469ec-162"><a href="wsman-sessionflagutf8.md"><strong>WSMan.SessionFlagUTF8</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="469ec-163">Gibt den Wert des Authentifizierungsflags <strong>WSManFlagUTF8</strong> für die Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.</span><span class="sxs-lookup"><span data-stu-id="469ec-163">Returns the value of the authentication flag <strong>WSManFlagUTF8</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="469ec-164">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="469ec-164">Properties</span></span>

<span data-ttu-id="469ec-165">Das **WSMAN** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="469ec-165">The **WSMan** object has these properties.</span></span>



| <span data-ttu-id="469ec-166">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="469ec-166">Property</span></span>                                            | <span data-ttu-id="469ec-167">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="469ec-167">Access type</span></span>          | <span data-ttu-id="469ec-168">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="469ec-168">Description</span></span>                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="469ec-169">**CommandLine**</span><span class="sxs-lookup"><span data-stu-id="469ec-169">**CommandLine**</span></span>](wsman-commandline.md)<br/> | <span data-ttu-id="469ec-170">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469ec-170">Read-only</span></span><br/> | <span data-ttu-id="469ec-171">Ruft die nicht verarbeitete Befehlszeile für den aktuellen Hostingprozess ab.</span><span class="sxs-lookup"><span data-stu-id="469ec-171">Gets the unprocessed command line for the current hosting process.</span></span><br/> |
| [<span data-ttu-id="469ec-172">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="469ec-172">**Error**</span></span>](wsman-error.md)<br/>             | <span data-ttu-id="469ec-173">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="469ec-173">Read-only</span></span><br/> | <span data-ttu-id="469ec-174">Ruft Fehlerinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="469ec-174">Gets error information.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="469ec-175">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="469ec-175">Remarks</span></span>

<span data-ttu-id="469ec-176">Das **WSMAN** -Objekt entspricht den [**iwsman**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) -und [**iwsmanex**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="469ec-176">The **WSMan** object corresponds to the [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) and [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) interfaces.</span></span> <span data-ttu-id="469ec-177">**WSMAN** ist das einzige Objekt, das [direkt mithilfe von](/previous-versions//xzysf6hc(v=vs.85))"" erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="469ec-177">**WSMan** is the only object that can be created directly using [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span>

## <a name="examples"></a><span data-ttu-id="469ec-178">Beispiele</span><span class="sxs-lookup"><span data-stu-id="469ec-178">Examples</span></span>

<span data-ttu-id="469ec-179">Im folgenden Codebeispiel wird gezeigt, wie ein **WSMAN** -Objekt instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="469ec-179">The following code example shows how to instantiate a **WSMan** object.</span></span>


```VB
Dim objWsman
Dim Session, Resource 
Set objWsman = CreateObject( "WSMAN.Automation" )
Set Session = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/Root/CIMv2/Win32_OperatingSystem"
```



## <a name="requirements"></a><span data-ttu-id="469ec-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="469ec-180">Requirements</span></span>



| <span data-ttu-id="469ec-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="469ec-181">Requirement</span></span> | <span data-ttu-id="469ec-182">Wert</span><span class="sxs-lookup"><span data-stu-id="469ec-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="469ec-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="469ec-183">Minimum supported client</span></span><br/> | <span data-ttu-id="469ec-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="469ec-184">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="469ec-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="469ec-185">Minimum supported server</span></span><br/> | <span data-ttu-id="469ec-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="469ec-186">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="469ec-187">Header</span><span class="sxs-lookup"><span data-stu-id="469ec-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="469ec-188"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="469ec-188"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="469ec-189">IDL</span><span class="sxs-lookup"><span data-stu-id="469ec-189">IDL</span></span><br/>                      | <dl> <span data-ttu-id="469ec-190"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="469ec-190"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="469ec-191">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="469ec-191">Library</span></span><br/>                  | <dl> <span data-ttu-id="469ec-192"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="469ec-192"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="469ec-193">DLL</span><span class="sxs-lookup"><span data-stu-id="469ec-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="469ec-194"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="469ec-194"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="469ec-195">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="469ec-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="469ec-196">WinRM-Skript-API</span><span class="sxs-lookup"><span data-stu-id="469ec-196">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="469ec-197">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="469ec-197">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="469ec-198">Verwenden von Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="469ec-198">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="469ec-199">Skripterstellung in Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="469ec-199">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="469ec-200">Abrufen von Daten vom lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="469ec-200">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="469ec-201">Abrufen von Daten von einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="469ec-201">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

