---
title: Komplexer channelType-Typ
description: Definiert einen Kanal, zu dem Anbieter Ereignisse protokollieren können.
ms.assetid: 882506e5-222b-45c8-af4b-59db8baa1dae
keywords:
- "\"ChannelType\", komplexer Typ, Ereignisprotokoll"
topic_type:
- apiref
api_name:
- ChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81158306285631748830d8aaaaf9cf329d7c0af1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478144"
---
# <a name="channeltype-complex-type"></a><span data-ttu-id="cf49c-104">Komplexer channelType-Typ</span><span class="sxs-lookup"><span data-stu-id="cf49c-104">ChannelType Complex Type</span></span>

<span data-ttu-id="cf49c-105">Definiert einen Kanal, zu dem Anbieter Ereignisse protokollieren können.</span><span class="sxs-lookup"><span data-stu-id="cf49c-105">Defines a channel to which providers can log events.</span></span>

``` syntax
<xs:complexType name="ChannelType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="logging"
            type="ChannelLoggingType"
            minOccurs="0"
         />
        <xs:element name="publishing"
            type="ChannelPublishingType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="chid"
        type="token"
        use="optional"
     />
    <xs:attribute name="type"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="access"
        type="string"
        use="optional"
     />
    <xs:attribute name="isolation"
        type="string"
        use="optional"
     />
    <xs:attribute name="enabled"
        type="boolean"
        default="false"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt8Type"
        use="optional"
     />
    <xs:attribute name="message"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="cf49c-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cf49c-106">Child elements</span></span>



| <span data-ttu-id="cf49c-107">Element</span><span class="sxs-lookup"><span data-stu-id="cf49c-107">Element</span></span>                                                                  | <span data-ttu-id="cf49c-108">type</span><span class="sxs-lookup"><span data-stu-id="cf49c-108">Type</span></span>                                                                                   | <span data-ttu-id="cf49c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf49c-109">Description</span></span>                                                                                                                                                                                                |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf49c-110">**Schlags**</span><span class="sxs-lookup"><span data-stu-id="cf49c-110">**logging**</span></span>](eventmanifestschema-logging-channeltype-element.md)       | [<span data-ttu-id="cf49c-111">**Channelloggingtype**</span><span class="sxs-lookup"><span data-stu-id="cf49c-111">**ChannelLoggingType**</span></span>](eventmanifestschema-channelloggingtype-complextype.md)       | <span data-ttu-id="cf49c-112">Definiert die Eigenschaften der Protokolldatei, die den Kanal sichert, z. b. die Kapazität und ob die Protokolldatei sequenziell oder zirkulär ist.</span><span class="sxs-lookup"><span data-stu-id="cf49c-112">Defines the properties of the log file that backs the channel, such as its capacity and whether the log file is sequential or circular.</span></span><br/>                                                         |
| [<span data-ttu-id="cf49c-113">**liche**</span><span class="sxs-lookup"><span data-stu-id="cf49c-113">**publishing**</span></span>](eventmanifestschema-publishing-channeltype-element.md) | [<span data-ttu-id="cf49c-114">**Channelpublishingtype**</span><span class="sxs-lookup"><span data-stu-id="cf49c-114">**ChannelPublishingType**</span></span>](eventmanifestschema-channelpublishingtype-complextype.md) | <span data-ttu-id="cf49c-115">Definiert die Protokollierungs Eigenschaften für die Sitzung, die vom Kanal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf49c-115">Defines the logging properties for the session that the channel uses.</span></span> <span data-ttu-id="cf49c-116">Nur Debug-und analytische Kanäle und Kanäle, die benutzerdefinierte Isolation verwenden, können Protokollierungs Eigenschaften für Ihre Sitzung angeben.</span><span class="sxs-lookup"><span data-stu-id="cf49c-116">Only Debug and Analytic channels and channels that use Custom isolation can specify logging properties for their session.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="cf49c-117">Attributes</span><span class="sxs-lookup"><span data-stu-id="cf49c-117">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf49c-118">Name</span><span class="sxs-lookup"><span data-stu-id="cf49c-118">Name</span></span></th>
<th><span data-ttu-id="cf49c-119">type</span><span class="sxs-lookup"><span data-stu-id="cf49c-119">Type</span></span></th>
<th><span data-ttu-id="cf49c-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf49c-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf49c-121">access</span><span class="sxs-lookup"><span data-stu-id="cf49c-121">access</span></span></td>
<td><span data-ttu-id="cf49c-122">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cf49c-122">string</span></span></td>
<td><span data-ttu-id="cf49c-123">Ein SDDL-Zugriffs Deskriptor ( <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Deskriptor Definition Language</a> ), der den Zugriff auf die Protokolldatei steuert, die den Kanal sichert.</span><span class="sxs-lookup"><span data-stu-id="cf49c-123">A <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> (SDDL) access descriptor that controls access to the log file that backs the channel.</span></span> <span data-ttu-id="cf49c-124">Wenn das <strong>Isolations</strong> Attribut auf "Application" oder "System" festgelegt ist, steuert der Zugriffs Deskriptor den Lesezugriff auf die Datei (die Schreibberechtigungen werden ignoriert).</span><span class="sxs-lookup"><span data-stu-id="cf49c-124">If the <strong>isolation</strong> attribute is set to Application or System, the access descriptor controls read access to the file (the write permissions are ignored).</span></span> <span data-ttu-id="cf49c-125">Wenn das <strong>Isolations</strong> Attribut auf Custom festgelegt ist, steuert der Zugriffs Deskriptor den Schreibzugriff auf den Kanal und den Lesezugriff auf die Datei.</span><span class="sxs-lookup"><span data-stu-id="cf49c-125">If the <strong>isolation</strong> attribute is set to Custom, the access descriptor controls write access to the channel and read access to the file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf49c-126">Chid</span><span class="sxs-lookup"><span data-stu-id="cf49c-126">chid</span></span></td>
<td><span data-ttu-id="cf49c-127">token</span><span class="sxs-lookup"><span data-stu-id="cf49c-127">token</span></span></td>
<td><span data-ttu-id="cf49c-128">Ein Bezeichner, der den Kanal in der Liste der vom Anbieter definierten oder importierten Kanäle eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cf49c-128">An identifier that uniquely identifies the channel in the list of channels that the provider defines or imports.</span></span> <span data-ttu-id="cf49c-129">Verwenden Sie diesen Wert, wenn Sie in einem Ereignis auf den Kanal verweisen.</span><span class="sxs-lookup"><span data-stu-id="cf49c-129">Use this value when referencing the channel in an event.</span></span> <span data-ttu-id="cf49c-130">Wenn Sie keinen channelbezeichner angeben, verwenden Sie den Namen des Kanals, um auf diesen Kanal in einer Ereignis Definition zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="cf49c-130">If you do not specify a channel identifier, use the channel's name to reference this channel in an event definition.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf49c-131">enabled</span><span class="sxs-lookup"><span data-stu-id="cf49c-131">enabled</span></span></td>
<td><span data-ttu-id="cf49c-132">boolean</span><span class="sxs-lookup"><span data-stu-id="cf49c-132">boolean</span></span></td>
<td><span data-ttu-id="cf49c-133">Bestimmt, ob der Kanal aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cf49c-133">Determines whether the channel is enabled.</span></span> <span data-ttu-id="cf49c-134">Auf " <strong>true</strong> " festlegen, um die Protokollierung auf dem Kanal zuzulassen. andernfalls <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf49c-134">Set to <strong>true</strong> to allow logging to the channel; otherwise, <strong>false</strong>.</span></span> <span data-ttu-id="cf49c-135">Der Standardwert ist <strong>false</strong> (die Protokollierung ist deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="cf49c-135">The default is <strong>false</strong> (logging is disabled).</span></span><br/> <span data-ttu-id="cf49c-136">Da es sich bei Debug-und analytischen Kanaltypen um Kanäle mit hohem Volumen handelt, sollten Sie den Kanal nur aktivieren, wenn Sie ein Problem mit einer Komponente untersuchen, die in diesen Kanal schreibt. Andernfalls sollte der Kanal deaktiviert bleiben.</span><span class="sxs-lookup"><span data-stu-id="cf49c-136">Because Debug and Analytic channel types are high volume channels, you should enable the channel only when investigating an issue with a component that writes to that channel; otherwise, the channel should remain disabled.</span></span><br/> <span data-ttu-id="cf49c-137">Jedes Mal, wenn Sie einen Debug-und analysekanal aktivieren, löscht der Dienst die Ereignisse aus dem Kanal.</span><span class="sxs-lookup"><span data-stu-id="cf49c-137">Each time you enable a Debug and Analytic channel, the service clears the events from the channel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf49c-138">Isolierung</span><span class="sxs-lookup"><span data-stu-id="cf49c-138">isolation</span></span></td>
<td><span data-ttu-id="cf49c-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cf49c-139">string</span></span></td>
<td><span data-ttu-id="cf49c-140">Der Isolations Wert definiert die Standard Zugriffsberechtigungen für den Kanal.</span><span class="sxs-lookup"><span data-stu-id="cf49c-140">The isolation value defines the default access permissions for the channel.</span></span> <span data-ttu-id="cf49c-141">Sie können einen der folgenden Werte angeben:</span><span class="sxs-lookup"><span data-stu-id="cf49c-141">You can specify one of the following values:</span></span>
<ul>
<li><span data-ttu-id="cf49c-142"><strong>Anwendung</strong></span><span class="sxs-lookup"><span data-stu-id="cf49c-142"><strong>Application</strong></span></span></li>
<li><span data-ttu-id="cf49c-143"><strong>System</strong></span><span class="sxs-lookup"><span data-stu-id="cf49c-143"><strong>System</strong></span></span></li>
<li><span data-ttu-id="cf49c-144"><strong>Benutzerdefiniert</strong></span><span class="sxs-lookup"><span data-stu-id="cf49c-144"><strong>Custom</strong></span></span></li>
</ul>
<span data-ttu-id="cf49c-145">Die Standard Isolation ist die <strong>Anwendung</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf49c-145">The default isolation is <strong>Application</strong>.</span></span> <span data-ttu-id="cf49c-146">Die Standard Berechtigungen für die <strong>Anwendung</strong> werden (mit SDDL angezeigt):</span><span class="sxs-lookup"><span data-stu-id="cf49c-146">The default permissions for <strong>Application</strong> are (shown using SDDL):</span></span> <br/> <span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf49c-147">Text</span><span class="sxs-lookup"><span data-stu-id="cf49c-147">Text</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="cf49c-148">Die Standard Berechtigungen für <strong>System</strong> lauten (mit SDDL angezeigt):</span><span class="sxs-lookup"><span data-stu-id="cf49c-148">The default permissions for <strong>System</strong> are (shown using SDDL):</span></span></p>
<div class="code">
<span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf49c-149">Text</span><span class="sxs-lookup"><span data-stu-id="cf49c-149">Text</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system             (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins          (read, write, clear)
            L&quot;(A;;0x3;;;BO)&quot;                    // backup operators         (read, write)
            L&quot;(A;;0x5;;;SO)&quot;                    // server operators         (read, clear) 
            L&quot;(A;;0x1;;;IU)&quot;                    // INTERACTIVE LOGON        (read)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON           (read, write)
            L&quot;(A;;0x1;;;S-1-5-3)&quot;               // BATCH LOGON              (read)
            L&quot;(A;;0x2;;;S-1-5-33)&quot;              // write restricted service (write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers        (read)</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="cf49c-150">Die Standard Berechtigungen für die <strong>benutzerdefinierte</strong> Isolation sind identisch mit der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="cf49c-150">The default permissions for <strong>Custom</strong> isolation is the same as Application.</span></span></p>
<p><span data-ttu-id="cf49c-151">Kanäle, die die <strong>Anwendungs</strong> Isolation angeben, verwenden dieselbe ETW-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="cf49c-151">Channels that specify <strong>Application</strong> isolation use the same ETW session.</span></span> <span data-ttu-id="cf49c-152">Das gleiche gilt für die <strong>System</strong> Isolation.</span><span class="sxs-lookup"><span data-stu-id="cf49c-152">The same is true for <strong>System</strong> isolation.</span></span> <span data-ttu-id="cf49c-153">Wenn Sie jedoch eine <strong>benutzerdefinierte</strong> Isolation angeben, erstellt der Dienst eine separate ETW-Sitzung für den Kanal.</span><span class="sxs-lookup"><span data-stu-id="cf49c-153">However, if you specify <strong>Custom</strong> isolation, the service creates a separate ETW session for the channel.</span></span> <span data-ttu-id="cf49c-154">Wenn Sie die <strong>benutzerdefinierte</strong> Isolation verwenden, können Sie die Zugriffsberechtigungen für den Kanal und die Sicherungsdatei steuern.</span><span class="sxs-lookup"><span data-stu-id="cf49c-154">Using <strong>Custom</strong> isolation lets you control the access permissions for the channel and backing file.</span></span> <span data-ttu-id="cf49c-155">Da nur 64 ETW-Sitzungen verfügbar sind, sollten Sie die Verwendung der <strong>benutzerdefinierten</strong> Isolierung einschränken.</span><span class="sxs-lookup"><span data-stu-id="cf49c-155">Because there are only 64 ETW sessions available, you should limit your use of <strong>Custom</strong> isolation.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf49c-156">message</span><span class="sxs-lookup"><span data-stu-id="cf49c-156">message</span></span></td>
<td><span data-ttu-id="cf49c-157">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cf49c-157">string</span></span></td>
<td><p><span data-ttu-id="cf49c-158">Der lokalisierte Anzeige Name für den Kanal.</span><span class="sxs-lookup"><span data-stu-id="cf49c-158">The localized display name for the channel.</span></span> <span data-ttu-id="cf49c-159">Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im <a href="eventmanifestschema-stringtable-resources-element.md"><strong>STRINGTABLE</strong></a> -Abschnitt des Manifests.</span><span class="sxs-lookup"><span data-stu-id="cf49c-159">The message string references a localized string in the <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> section of the manifest.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf49c-160">name</span><span class="sxs-lookup"><span data-stu-id="cf49c-160">name</span></span></td>
<td><span data-ttu-id="cf49c-161">anyURI</span><span class="sxs-lookup"><span data-stu-id="cf49c-161">anyURI</span></span></td>
<td><p><span data-ttu-id="cf49c-162">Der Name des Channels.</span><span class="sxs-lookup"><span data-stu-id="cf49c-162">The name of the channel.</span></span> <span data-ttu-id="cf49c-163">Der Name muss innerhalb der Liste der vom Anbieter verwendeten Kanäle eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="cf49c-163">The name must be unique within the list of channels that the provider uses.</span></span> <span data-ttu-id="cf49c-164">Die Konvention für Benennungs Kanäle besteht darin, den Kanaltyp an den Namen des Anbieters anzufügen.</span><span class="sxs-lookup"><span data-stu-id="cf49c-164">The convention for naming channels is to append the channel type to the provider's name.</span></span> <span data-ttu-id="cf49c-165">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="cf49c-165">For example.</span></span> <span data-ttu-id="cf49c-166">Wenn der Name des Anbieters Company-Product-Component lautet und Sie einen Betriebskanal definieren, lautet der Name Company-Product-Component/Operational.</span><span class="sxs-lookup"><span data-stu-id="cf49c-166">if the provider's name is Company-Product-Component and you are defining an operational channel, the name would be Company-Product-Component/Operational.</span></span></p>
<p><span data-ttu-id="cf49c-167">Channelnamen müssen weniger als 255 Zeichen umfassen und dürfen die folgenden Zeichen nicht enthalten: ">", "</span><span class="sxs-lookup"><span data-stu-id="cf49c-167">Channel names must be less that 255 characters and cannot contain the following characters: '>', '</span></span><', '&', '&quot;', '|', '\', ':', '`', '?', '*', or characters with codes less than 31.</p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf49c-168">Symbol</span><span class="sxs-lookup"><span data-stu-id="cf49c-168">symbol</span></span></td>
<td><span data-ttu-id="cf49c-169"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>Csymboltype</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf49c-169"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span></span></td>
<td><p><span data-ttu-id="cf49c-170">Das Symbol, das für den Verweis auf den Kanal in Ihrer Anwendung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf49c-170">The symbol to use to reference the channel in your application.</span></span> <span data-ttu-id="cf49c-171">Der <a href="message-compiler--mc-exe-.md"><strong>Nachrichten Compiler (MC.exe)</strong></a> verwendet das Symbol, um eine Konstante für den Kanal in der vom Compiler generierten Header Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cf49c-171">The <a href="message-compiler--mc-exe-.md"><strong>Message Compiler (MC.exe)</strong></a> uses the symbol to create a constant for the channel in the header file that the compiler generates.</span></span> <span data-ttu-id="cf49c-172">Wenn Sie kein Symbol angeben, generiert der Compiler den Namen für Sie.</span><span class="sxs-lookup"><span data-stu-id="cf49c-172">If you do not specify a symbol, the compiler generates the name for you.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf49c-173">type</span><span class="sxs-lookup"><span data-stu-id="cf49c-173">type</span></span></td>
<td><span data-ttu-id="cf49c-174">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cf49c-174">string</span></span></td>
<td><p><span data-ttu-id="cf49c-175">Identifiziert den Typ des Kanals.</span><span class="sxs-lookup"><span data-stu-id="cf49c-175">Identifies the channel's type.</span></span> <span data-ttu-id="cf49c-176">Sie können einen der folgenden Typen angeben:</span><span class="sxs-lookup"><span data-stu-id="cf49c-176">You can specify one of the following types:</span></span></p>
<ul>
<li><span data-ttu-id="cf49c-177"><strong>Administrator</strong></span><span class="sxs-lookup"><span data-stu-id="cf49c-177"><strong>Admin</strong></span></span></li>
<li><span data-ttu-id="cf49c-178"><strong>Bei Betrieb</strong></span><span class="sxs-lookup"><span data-stu-id="cf49c-178"><strong>Operational</strong></span></span></li>
<li><span data-ttu-id="cf49c-179"><strong>Analytic</strong></span><span class="sxs-lookup"><span data-stu-id="cf49c-179"><strong>Analytic</strong></span></span></li>
<li><span data-ttu-id="cf49c-180"><strong>Debuggen</strong></span><span class="sxs-lookup"><span data-stu-id="cf49c-180"><strong>Debug</strong></span></span></li>
</ul>
<p><span data-ttu-id="cf49c-181">Admin-typkanäle unterstützen Ereignisse, die Endbenutzern, Administratoren und Supportmitarbeitern als Ziel haben.</span><span class="sxs-lookup"><span data-stu-id="cf49c-181">Admin type channels support events that target end users, administrators, and support personnel.</span></span> <span data-ttu-id="cf49c-182">Ereignisse, die in die admin-Kanäle geschrieben werden, sollten über eine klar definierte Lösung verfügen, auf der der Administrator agieren kann. Ein Beispiel für ein Admin-Ereignis ist ein Ereignis, das auftritt, wenn eine Anwendung keine Verbindung zu einem Drucker herstellt.</span><span class="sxs-lookup"><span data-stu-id="cf49c-182">Events written to the Admin channels should have a well-defined solution on which the administrator can act. An example of an admin event is an event that occurs when an application fails to connect to a printer.</span></span> <span data-ttu-id="cf49c-183">Diese Ereignisse sind entweder gut dokumentiert oder verfügen über eine Nachricht, die dem Reader direkt Anweisungen zur Behebung des Problems liefert.</span><span class="sxs-lookup"><span data-stu-id="cf49c-183">These events are either well-documented or have a message associated with them that gives the reader direct instructions of what must be done to rectify the problem.</span></span></p>
<p><span data-ttu-id="cf49c-184">Operational Type Channels unterstützen Ereignisse, die zum Analysieren und Diagnostizieren eines Problems oder eines Vorkommens verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf49c-184">Operational type channels support events that are used for analyzing and diagnosing a problem or occurrence.</span></span> <span data-ttu-id="cf49c-185">Sie können zum Auslösen von Tools oder Aufgaben anhand des Problems oder des Vorkommens verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf49c-185">They can be used to trigger tools or tasks based on the problem or occurrence.</span></span> <span data-ttu-id="cf49c-186">Beispielsweise handelt es sich um ein Vorgangsereignis, wenn ein Drucker einem System hinzugefügt oder daraus entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="cf49c-186">An example of an operational event is an event that occurs when a printer is added or removed from a system.</span></span></p>
<p><span data-ttu-id="cf49c-187">Analytische typkanäle unterstützen Ereignisse, die in hohem Umfang veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="cf49c-187">Analytic type channels support events that are published in high volume.</span></span> <span data-ttu-id="cf49c-188">Sie beschreiben Programmvorgänge und geben Probleme an, die nicht durch Benutzereingriffe behoben werden können.</span><span class="sxs-lookup"><span data-stu-id="cf49c-188">They describe program operation and indicate problems that cannot be handled by user intervention.</span></span></p>
<p><span data-ttu-id="cf49c-189">Debug-typkanäle unterstützen Ereignisse, die ausschließlich von Entwicklern zum Diagnostizieren eines Problems beim Debuggen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf49c-189">Debug type channels support events that are used solely by developers to diagnose a problem for debugging.</span></span></p>
<p><span data-ttu-id="cf49c-190">Analytische und Debugkanäle sind standardmäßig deaktiviert und sollten nur aktiviert werden, um die Ursache eines Problems zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="cf49c-190">Analytic and debug channels are disabled by default and should only enabled to determine the cause of an issue.</span></span> <span data-ttu-id="cf49c-191">Beispielsweise können Sie den Channel aktivieren, das Szenario ausführen, das das Problem verursacht, den Kanal deaktivieren und dann die Ereignisse Abfragen.</span><span class="sxs-lookup"><span data-stu-id="cf49c-191">For example, you would enable the channel, run the scenario that is causing the issue, disable the channel, and then query the events.</span></span> <span data-ttu-id="cf49c-192">Beachten Sie, dass durch Aktivieren des Kanals der Kanal vorhandener Ereignisse gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="cf49c-192">Note that enabling the channel clears the channel of existing events.</span></span> <span data-ttu-id="cf49c-193">Wenn für den Analyse-und Debugkanal eine zirkuläre Unterstützungs Datei verwendet wird, müssen Sie den Kanal deaktivieren, um seine Ereignisse abzufragen.</span><span class="sxs-lookup"><span data-stu-id="cf49c-193">If the analytic and debug channel uses a circular backing file, you must disable the channel to query its events.</span></span></p>
<p><span data-ttu-id="cf49c-194">Alle Administrator Kanäle verwenden dieselbe ETW-Sitzung. das gleiche gilt für Betriebs Kanäle.</span><span class="sxs-lookup"><span data-stu-id="cf49c-194">All Admin channels use the same ETW session; the same is true for Operational channels.</span></span> <span data-ttu-id="cf49c-195">Allerdings wird für jeden Analyse-und Debugkanal eine separate ETW-Sitzung verwendet. Dies ist ein weiterer Grund, bei Bedarf nur diese Kanaltypen zu aktivieren (es ist eine begrenzte Anzahl von ETW-Sitzungen verfügbar).</span><span class="sxs-lookup"><span data-stu-id="cf49c-195">However, each Analytic and Debug channel uses a separate ETW session, which is another reason to only enable these channel types when needed (there is a limited number of ETW sessions available).</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf49c-196">value</span><span class="sxs-lookup"><span data-stu-id="cf49c-196">value</span></span></td>
<td><span data-ttu-id="cf49c-197"><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf49c-197"><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></span></span></td>
<td><p><span data-ttu-id="cf49c-198">Ein numerischer Bezeichner, der den Kanal innerhalb der Liste der vom Anbieter definierten Kanäle eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cf49c-198">A numeric identifier that uniquely identifies the channel within the list of channels that the provider defines.</span></span> <span data-ttu-id="cf49c-199">Der Nachrichten Compiler weist den Wert zu, wenn er nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cf49c-199">The message compiler assigns the value if not specified.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="cf49c-200">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf49c-200">Remarks</span></span>

<span data-ttu-id="cf49c-201">Wenn der Name des Kanals der channelbenennungs Konvention folgt, listet der Windows-Ereignisanzeige den Kanal mithilfe der Zeichenfolge auf, die dem umgekehrten Schrägstrich folgt.</span><span class="sxs-lookup"><span data-stu-id="cf49c-201">If the channel's name follows the channel naming convention, the Windows Event Viewer will list the channel using the string that follows the backslash.</span></span> <span data-ttu-id="cf49c-202">Wenn der ChannelName beispielsweise Company-Product-Component/Operational ist, wird der Kanal vom Ereignisanzeige als betriebsbereit mit dem Anbieter Company-Product-Component aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="cf49c-202">For example, if the channel name is Company-Product-Component/Operational, then the Event Viewer will list the channel as Operational under the Company-Product-Component provider.</span></span> <span data-ttu-id="cf49c-203">Andernfalls wird der gesamte Kanalname unter dem Anbieter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cf49c-203">Otherwise, the entire channel name is shown under the provider.</span></span> <span data-ttu-id="cf49c-204">Wenn angegeben, wird der lokalisierte Anzeige Name verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf49c-204">The localized display name is used if provided.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf49c-205">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf49c-205">Requirements</span></span>



| <span data-ttu-id="cf49c-206">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf49c-206">Requirement</span></span> | <span data-ttu-id="cf49c-207">Wert</span><span class="sxs-lookup"><span data-stu-id="cf49c-207">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cf49c-208">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf49c-208">Minimum supported client</span></span><br/> | <span data-ttu-id="cf49c-209">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf49c-209">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cf49c-210">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf49c-210">Minimum supported server</span></span><br/> | <span data-ttu-id="cf49c-211">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf49c-211">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




`
