---
description: Glossarseite
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 08951f9f-d03d-4720-8f18-1413ba72e93d
title: Glossar (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74d707c828a9eeb5f07ebf3ec3c1ca92a9d2b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866228"
---
# <a name="glossary-winhttp"></a><span data-ttu-id="8c981-103">Glossar (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="8c981-103">Glossary (WinHTTP)</span></span>

<dl> <dt>

<span data-ttu-id="8c981-104"><span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**Authentifizierungsdaten**</span><span class="sxs-lookup"><span data-stu-id="8c981-104"><span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**authentication data**</span></span>
</dt> <dd>

<span data-ttu-id="8c981-105">Schema spezifischer Datenblock, der während der Authentifizierung zwischen dem Server und dem Client ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="8c981-105">Scheme-specific block of data that is exchanged between the server and client during authentication.</span></span> <span data-ttu-id="8c981-106">Zum Nachweisen der Identität werden einige oder alle dieser Daten vom Client mit einem Benutzernamen und einem Kennwort verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="8c981-106">To prove its identity, the client encrypts some or all of this data with a user name and password.</span></span> <span data-ttu-id="8c981-107">Der Client sendet die verschlüsselten Daten an den Server, der die Daten entschlüsselt und mit dem Original vergleicht.</span><span class="sxs-lookup"><span data-stu-id="8c981-107">The client sends the encrypted data to the server, which decrypts the data and compares it to the original.</span></span> <span data-ttu-id="8c981-108">Wenn die entschlüsselten Daten mit den ursprünglichen Daten übereinstimmen, wird der Client authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="8c981-108">If the decrypted data matches the original data, the client is authenticated.</span></span>

</dd> <dt>

<span data-ttu-id="8c981-109"><span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**Base64-Codierung**</span><span class="sxs-lookup"><span data-stu-id="8c981-109"><span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**base64 encoding**</span></span>
</dt> <dd>

<span data-ttu-id="8c981-110">Schema, das zum Übertragen von Binärdaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c981-110">Scheme used to transmit binary data.</span></span> <span data-ttu-id="8c981-111">Base64 verarbeitet Daten als 24-Bit-Gruppen und ordnet diese Daten vier codierten Zeichen zu.</span><span class="sxs-lookup"><span data-stu-id="8c981-111">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="8c981-112">Dies wird manchmal als 3-zu-4-Codierung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8c981-112">It is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="8c981-113">Jede 6 Bits der 24-Bit-Gruppe wird als Index in einer Mapping-Tabelle (dem Base64-Alphabet) zum Abrufen eines Zeichens für die codierten Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c981-113">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="8c981-114">Die Zeilenlängen der codierten Daten sind auf 76 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="8c981-114">The encoded data has line lengths limited to 76 characters.</span></span>

</dd> <dt>

<span data-ttu-id="8c981-115"><span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**Zertifikat Speicher**</span><span class="sxs-lookup"><span data-stu-id="8c981-115"><span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**certificate store**</span></span>
</dt> <dd>

<span data-ttu-id="8c981-116">In der Regel ist der permanente Speicher, in dem Zertifikate, Zertifikat Sperr Listen (CRL) und Zertifikat Vertrauens Listen (Certificate Trust Lists, CTL) gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="8c981-116">Typically, permanent storage where certificates, certificate revocation lists (CRL), and certificate trust lists (CTL) are stored.</span></span> <span data-ttu-id="8c981-117">Ein Zertifikat Speicher kann auch temporär sein, wenn Sie mit Sitzungs basierten Zertifikaten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="8c981-117">A certificate store can also be temporary when working with session-based certificates.</span></span>

</dd> <dt>

<span data-ttu-id="8c981-118"><span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**Cobranding**</span><span class="sxs-lookup"><span data-stu-id="8c981-118"><span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**cobranding**</span></span>
</dt> <dd>

<span data-ttu-id="8c981-119">Möglichkeit für eine Microsoft Passport Teilnehmer Website, eigene Branding-Elemente und-Erklärungen auf den Passport-Netzwerkdienst Seiten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8c981-119">Ability for a Microsoft Passport participant site to provide its own branding elements and explanations on the Passport network service pages.</span></span> <span data-ttu-id="8c981-120">Zu den Cobrandings gehört das Anpassen von Aussehen und Verhalten, spezifischer Text und bestimmtes Verhalten auf Passport-Netzwerkseiten.</span><span class="sxs-lookup"><span data-stu-id="8c981-120">Cobranding includes customizing the look and feel, specific text, and specific behavior on Passport network pages.</span></span>

</dd> <dt>

<span data-ttu-id="8c981-121"><span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**Codepage**</span><span class="sxs-lookup"><span data-stu-id="8c981-121"><span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**code page**</span></span>
</dt> <dd>

<span data-ttu-id="8c981-122">Tabelle, die die Binär Zeichen Codes, die von einem Programm verwendet werden, auf Tastatur oder die Darstellung von Zeichen auf dem Monitor in Beziehung gesetzt.</span><span class="sxs-lookup"><span data-stu-id="8c981-122">Table that relates the binary character codes used by a program to keys on the keyboard or to the appearance of characters on the monitor.</span></span> <span data-ttu-id="8c981-123">Die Verwendung von Codepages bietet die Möglichkeit, Zeichensätze und Tastaturlayouts in verschiedenen Ländern und Regionen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8c981-123">Using code pages is a way to provide support for character sets and keyboard layouts used in different countries and regions.</span></span> <span data-ttu-id="8c981-124">Sie können Geräte wie den Monitor und die Tastatur so konfigurieren, dass eine bestimmte Codepage verwendet und von einer Codepage (z. b. USA) auf eine andere Codepage (z. b. Portugal) auf der Anforderung des Benutzers gewechselt wird.</span><span class="sxs-lookup"><span data-stu-id="8c981-124">You can configure devices such as the monitor and the keyboard to use a specific code page and to switch from one code page (such as United States) to another (such as Portugal) at the user's request.</span></span>

</dd> <dt>

<span data-ttu-id="8c981-125"><span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**HTTP-Verb**</span><span class="sxs-lookup"><span data-stu-id="8c981-125"><span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**HTTP verb**</span></span>
</dt> <dd>

<span data-ttu-id="8c981-126">Das HTTP-Verb (oder http-Methode) ist eine Anweisung, die in einer Anforderungs Nachricht gesendet wird, die einen HTTP-Server über die Aktion benachrichtigt, die für die angegebene Ressource ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c981-126">The HTTP verb (or HTTP method) is an instruction sent in a request message that notifies an HTTP server of the action to perform on the specified resource.</span></span> <span data-ttu-id="8c981-127">"Get" gibt beispielsweise an, dass eine Ressource vom Server abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8c981-127">For example, "GET" specifies that a resource is being retrieved from the server.</span></span> <span data-ttu-id="8c981-128">Zu den allgemeinen Verben zählen "Get", "Post" und "Head".</span><span class="sxs-lookup"><span data-stu-id="8c981-128">Common verbs include "GET", "POST", and "HEAD".</span></span> <span data-ttu-id="8c981-129">Weitere Informationen und eine komplette Liste der standardmäßigen HTTP-Verben finden Sie in der HTTP/1.1-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="8c981-129">For more information and a complete list of standard HTTP verbs, see the HTTP/1.1 specification.</span></span>

</dd> <dt>

<span data-ttu-id="8c981-130"><span id="term_ticket"></span><span id="TERM_TICKET"></span>**Preis**</span><span class="sxs-lookup"><span data-stu-id="8c981-130"><span id="term_ticket"></span><span id="TERM_TICKET"></span>**ticket**</span></span>
</dt> <dd>

<span data-ttu-id="8c981-131">Cookie, das ein Benutzerprofil für die Passport-Authentifizierung enthält.</span><span class="sxs-lookup"><span data-stu-id="8c981-131">Cookie that contains a user profile for Passport authentication.</span></span> <span data-ttu-id="8c981-132">Jedes Ticket entspricht einer URL.</span><span class="sxs-lookup"><span data-stu-id="8c981-132">Each ticket corresponds to one URL.</span></span> <span data-ttu-id="8c981-133">Der Anmelde Server einer Passport-Domänen Zertifizierungsstelle stellt Tickets bereit, die der Client für die Authentifizierung an ein Passport-Mitglied sendet.</span><span class="sxs-lookup"><span data-stu-id="8c981-133">The logon server of a Passport Domain Authority provides tickets that the client sends to a Passport member for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="8c981-134"><span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**Benutzer-Agent**</span><span class="sxs-lookup"><span data-stu-id="8c981-134"><span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**user agent**</span></span>
</dt> <dd>

<span data-ttu-id="8c981-135">Der Benutzer-Agent ist die Client Anwendung, die ein Dokument von einem HTTP-Server anfordert.</span><span class="sxs-lookup"><span data-stu-id="8c981-135">The user agent is the client application that requests a document from an HTTP server.</span></span> <span data-ttu-id="8c981-136">Wenn der Client eine Anforderung an einen HTTP-Server sendet, sendet er in der Regel den Namen des Benutzer-Agents mit dem Anforderungs Header, damit der Server die Funktionen der Client Software bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="8c981-136">When the client sends a request to an HTTP server, typically it sends the name of the user agent with the request header so that the server can determine the capabilities of the client software.</span></span>

</dd> </dl>

 

 



