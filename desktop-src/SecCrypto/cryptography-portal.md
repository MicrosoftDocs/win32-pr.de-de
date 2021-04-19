---
description: Verwenden Sie Kryptografietechnologien für Verschlüsselung mit öffentlichem Schlüssel, Verschlüsselungsalgorithmen, RSA-Verschlüsselung und digitale Zertifikate.
ms.assetid: c53af815-ee3f-417a-8e62-3a3689715bc6
title: Kryptografie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852b7c2b38ca5b7d330a70e91a5b7a9dd5bb6557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350405"
---
# <a name="cryptography"></a><span data-ttu-id="103d0-103">Kryptografie</span><span class="sxs-lookup"><span data-stu-id="103d0-103">Cryptography</span></span>

## <a name="purpose"></a><span data-ttu-id="103d0-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="103d0-104">Purpose</span></span>

<span data-ttu-id="103d0-105">Kryptografie ist die Verwendung von Codes zum Konvertieren von Daten, sodass nur ein bestimmter Empfänger ihn mit einem Schlüssel lesen kann.</span><span class="sxs-lookup"><span data-stu-id="103d0-105">Cryptography is the use of codes to convert data so that only a specific recipient will be able to read it, using a key.</span></span>

<span data-ttu-id="103d0-106">Zu den Kryptografietechnologien von Microsoft gehören CryptoAPI, Kryptografiedienstanbieter (CSP), CryptoAPI-Tools, CAPICOM, wintrust, ausstellen und Verwalten von Zertifikaten und entwickeln anpassbarer Public Key-Infrastrukturen.</span><span class="sxs-lookup"><span data-stu-id="103d0-106">Microsoft cryptographic technologies include CryptoAPI, Cryptographic Service Providers (CSP), CryptoAPI Tools, CAPICOM, WinTrust, issuing and managing certificates, and developing customizable public key infrastructures.</span></span> <span data-ttu-id="103d0-107">Die Zertifikat-und Smartcard-Registrierung, Zertifikat Verwaltung und die Entwicklung benutzerdefinierter Module werden ebenfalls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="103d0-107">Certificate and smart card enrollment, certificate management, and custom module development are also described.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="103d0-108">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="103d0-108">Developer audience</span></span>

<span data-ttu-id="103d0-109">CryptoAPI ist für die Verwendung durch Entwickler von Windows-basierten Anwendungen gedacht, die es Benutzern ermöglichen, Dokumente und andere Daten in einer sicheren Umgebung zu erstellen und auszutauschen, insbesondere über nicht sichere Medien wie das Internet.</span><span class="sxs-lookup"><span data-stu-id="103d0-109">CryptoAPI is intended for use by developers of Windows-based applications that will enable users to create and exchange documents and other data in a secure environment, especially over nonsecure media such as the Internet.</span></span> <span data-ttu-id="103d0-110">Entwickler sollten mit den Programmiersprachen C und C++ und der Windows-Programmierumgebung vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="103d0-110">Developers should be familiar with the C and C++ programming languages and the Windows programming environment.</span></span> <span data-ttu-id="103d0-111">Es ist zwar nicht erforderlich, aber es wird empfohlen, Kryptografie-oder sicherheitsrelevante Themen zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="103d0-111">Although not required, an understanding of cryptography or security-related subjects is advised.</span></span>

<span data-ttu-id="103d0-112">CAPICOM ist eine nur-32-Bit-Komponente, die von Entwicklern verwendet werden kann, die Anwendungen mit Visual Basic Scripting Edition-Programmiersprache (VBScript) oder der Programmiersprache C++ erstellen.</span><span class="sxs-lookup"><span data-stu-id="103d0-112">CAPICOM is a 32-bit only component that is intended for use by developers who are creating applications using Visual Basic Scripting Edition (VBScript) programming language or the C++ programming language.</span></span> <span data-ttu-id="103d0-113">CAPICOM ist für die Verwendung in den Betriebssystemen verfügbar, die unter Run-Time Anforderungen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="103d0-113">CAPICOM is available for use in the operating systems specified in Run-Time Requirements.</span></span> <span data-ttu-id="103d0-114">Für eine zukünftige Entwicklung empfiehlt es sich, die .NET Framework zum Implementieren von Sicherheitsfeatures zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="103d0-114">For future development, we recommend that you use the .NET Framework to implement security features.</span></span> <span data-ttu-id="103d0-115">Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).</span><span class="sxs-lookup"><span data-stu-id="103d0-115">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="103d0-116">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="103d0-116">Run-time requirements</span></span>

<span data-ttu-id="103d0-117">Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" der Referenzseite für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="103d0-117">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

<span data-ttu-id="103d0-118">CAPICOM 2.1.0.2 wird für die folgenden Betriebssysteme und Versionen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="103d0-118">CAPICOM 2.1.0.2 is supported on the following operating systems and versions:</span></span>

-   <span data-ttu-id="103d0-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="103d0-119">Windows Server 2003</span></span>
-   <span data-ttu-id="103d0-120">Windows XP</span><span class="sxs-lookup"><span data-stu-id="103d0-120">Windows XP</span></span>

<span data-ttu-id="103d0-121">CAPICOM ist als verteilbare Datei verfügbar, die von [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281)heruntergeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="103d0-121">CAPICOM is available as a redistributable file that can be downloaded from [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).</span></span>

<span data-ttu-id="103d0-122">Die Zertifikat Dienste erfordern die folgenden Versionen dieser Betriebssysteme:</span><span class="sxs-lookup"><span data-stu-id="103d0-122">Certificate Services requires the following versions of these operating systems:</span></span>

-   <span data-ttu-id="103d0-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="103d0-123">Windows Server 2008 R2</span></span>
-   <span data-ttu-id="103d0-124">WindowsServer 2008</span><span class="sxs-lookup"><span data-stu-id="103d0-124">Windows Server 2008</span></span>
-   <span data-ttu-id="103d0-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="103d0-125">Windows Server 2003</span></span>

## <a name="in-this-section"></a><span data-ttu-id="103d0-126">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="103d0-126">In this section</span></span>



| <span data-ttu-id="103d0-127">Thema</span><span class="sxs-lookup"><span data-stu-id="103d0-127">Topic</span></span>                                                           | <span data-ttu-id="103d0-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="103d0-128">Description</span></span>                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="103d0-129">Informationen zur Kryptografie</span><span class="sxs-lookup"><span data-stu-id="103d0-129">About Cryptography</span></span>](about-cryptography.md)<br/>         | <span data-ttu-id="103d0-130">Wichtige kryptografiekonzepte und eine allgemeine Übersicht über die Kryptografietechnologien von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="103d0-130">Key cryptography concepts and a high-level view of Microsoft cryptography technologies.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="103d0-131">Verwenden der Kryptografie</span><span class="sxs-lookup"><span data-stu-id="103d0-131">Using Cryptography</span></span>](using-cryptography.md)<br/>         | <span data-ttu-id="103d0-132">Kryptografieprozesse, Prozeduren und Erweiterte Beispiele von C-und Visual Basic Programmen mithilfe von CryptoAPI-Funktionen und CAPICOM-Objekten.</span><span class="sxs-lookup"><span data-stu-id="103d0-132">Cryptography processes, procedures, and extended samples of C and Visual Basic programs using CryptoAPI functions and CAPICOM objects.</span></span><br/>                                                                            |
| [<span data-ttu-id="103d0-133">Kryptografiereferenz</span><span class="sxs-lookup"><span data-stu-id="103d0-133">Cryptography Reference</span></span>](cryptography-reference.md)<br/> | <span data-ttu-id="103d0-134">Ausführliche Beschreibungen der Kryptografiefunktionen, Schnittstellen, Objekte, Strukturen und anderen Programmier Elemente von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="103d0-134">Detailed descriptions of the Microsoft cryptography functions, interfaces, objects, structures, and other programming elements.</span></span> <span data-ttu-id="103d0-135">Enthält Referenz Beschreibungen der API für die Arbeit mit digitalen Zertifikaten.</span><span class="sxs-lookup"><span data-stu-id="103d0-135">Includes reference descriptions of the API for working with digital certificates.</span></span><br/> |



 

 

 




