---
description: Die Größe einer digestzugriffschallenge muss kleiner als 2048 Byte sein.
ms.assetid: 16c6728a-966b-436f-902d-3e12368986b6
title: Inhalt einer Digestherausforderung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f90dd78ae28536f6e2d07882f69335975df14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128316"
---
# <a name="contents-of-a-digest-challenge"></a><span data-ttu-id="228dd-103">Inhalt einer Digestherausforderung</span><span class="sxs-lookup"><span data-stu-id="228dd-103">Contents of a Digest Challenge</span></span>

<span data-ttu-id="228dd-104">Die Größe einer digestzugriffschallenge muss kleiner als 2048 Byte sein.</span><span class="sxs-lookup"><span data-stu-id="228dd-104">The size of a Digest Access challenge must be less than 2048 bytes.</span></span> <span data-ttu-id="228dd-105">Das folgende Beispiel zeigt eine Anforderung, die der Zeichenfolge szchallenge zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="228dd-105">The following example shows a challenge assigned to the character string szChallenge.</span></span>


```C++
szChallenge = "realm=\"Microsoft_Example_Forest\",";
algorithm = "MD5-sess\", qop=\"auth\", nonce=\"0123456789abcdef\"";
```



> [!Note]  
> <span data-ttu-id="228dd-106">Die Abfrage Zeichenfolge wird in doppelte Anführungszeichen eingeschlossen und enthält eingebettete doppelte Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="228dd-106">The challenge string is enclosed in double quotes and contains embedded double quotes.</span></span> <span data-ttu-id="228dd-107">Eingebetteten doppelten Anführungszeichen muss ein umgekehrter Schrägstrich () vorangestellt werden \\ .</span><span class="sxs-lookup"><span data-stu-id="228dd-107">Embedded double quotes must be preceded (escaped) with a backslash (\\).</span></span>

 

<span data-ttu-id="228dd-108">Eine Digestherausforderung kann die folgenden Direktiven enthalten.</span><span class="sxs-lookup"><span data-stu-id="228dd-108">A Digest challenge can contain the following directives.</span></span>



| <span data-ttu-id="228dd-109">Anweisung</span><span class="sxs-lookup"><span data-stu-id="228dd-109">Directive</span></span>         | <span data-ttu-id="228dd-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="228dd-110">Description</span></span>                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="228dd-111">realm</span><span class="sxs-lookup"><span data-stu-id="228dd-111">realm</span></span>             | <span data-ttu-id="228dd-112">Ein von der Implementierung definierter Hinweis für den Client, welche [*Anmelde*](/windows/desktop/SecGloss/c-gly) Informationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="228dd-112">An implementation-defined hint to the client about which [*credentials*](/windows/desktop/SecGloss/c-gly) are required.</span></span> <span data-ttu-id="228dd-113">Der Client sollte diese Informationen für den Benutzer anzeigen, wenn er zur Eingabe von Anmelde Informationen aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="228dd-113">The client should display this information to the user if it is prompting for credentials.</span></span>                                                  |
| <span data-ttu-id="228dd-114">Algorithmus</span><span class="sxs-lookup"><span data-stu-id="228dd-114">algorithm</span></span>         | <span data-ttu-id="228dd-115">Microsoft Digest unterstützt MD5 und MD5-sess.</span><span class="sxs-lookup"><span data-stu-id="228dd-115">Microsoft Digest supports MD5 and MD5-Sess.</span></span> <span data-ttu-id="228dd-116">Verwenden Sie für eine optimale Leistung MD5-sess.</span><span class="sxs-lookup"><span data-stu-id="228dd-116">For optimal performance, use MD5-Sess.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="228dd-117">QoP</span><span class="sxs-lookup"><span data-stu-id="228dd-117">qop</span></span>               | <span data-ttu-id="228dd-118">Diese Direktive kann auf "auth", "auth-int" oder "auth-conf" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="228dd-118">This directive can be set to auth, auth-int, or auth-conf.</span></span> <span data-ttu-id="228dd-119">Weitere Informationen finden Sie unter [Qualität von Schutz und Chiffren](quality-of-protection-and-ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="228dd-119">For more information, see [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).</span></span>                                                                                                                                       |
| <span data-ttu-id="228dd-120">nonce</span><span class="sxs-lookup"><span data-stu-id="228dd-120">nonce</span></span>             | <span data-ttu-id="228dd-121">Ein eindeutiger codierter Wert, der vom Server für jede Abfrage generiert wird.</span><span class="sxs-lookup"><span data-stu-id="228dd-121">A unique encoded value generated by the server for each challenge.</span></span> <span data-ttu-id="228dd-122">Dieser Wert darf nicht vom Client geändert werden.</span><span class="sxs-lookup"><span data-stu-id="228dd-122">This value must not be altered by the client.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="228dd-123">lässige</span><span class="sxs-lookup"><span data-stu-id="228dd-123">opaque</span></span>            | <span data-ttu-id="228dd-124">Enthält einen Verweis für den [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) , der festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="228dd-124">Contains a reference for the [*security context*](/windows/desktop/SecGloss/s-gly) that is being established.</span></span> <span data-ttu-id="228dd-125">Weitere Informationen finden Sie unter Verwalten [des Sicherheits Kontexts zwischen Verbindungen](maintaining-the-security-context-between-connections.md).</span><span class="sxs-lookup"><span data-stu-id="228dd-125">For more information, see [Maintaining the Security Context Between Connections](maintaining-the-security-context-between-connections.md).</span></span> |
| <span data-ttu-id="228dd-126">Chiffre (nur SASL)</span><span class="sxs-lookup"><span data-stu-id="228dd-126">cipher(SASL only)</span></span> | <span data-ttu-id="228dd-127">Die Liste der Chiffren, die der Server unterstützt.</span><span class="sxs-lookup"><span data-stu-id="228dd-127">The list of ciphers that the server supports.</span></span> <span data-ttu-id="228dd-128">Dieses Element kann in einer Digest-SASL-Abfrage nur vorhanden sein, wenn die QoP-Direktive auth-conf angibt.</span><span class="sxs-lookup"><span data-stu-id="228dd-128">This element can be present in a Digest SASL challenge only if the qop directive specifies auth-conf.</span></span> <span data-ttu-id="228dd-129">Weitere Informationen finden Sie unter [Qualität von Schutz und Chiffren](quality-of-protection-and-ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="228dd-129">For more information, see [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).</span></span>                                              |
| <span data-ttu-id="228dd-130">charset</span><span class="sxs-lookup"><span data-stu-id="228dd-130">charset</span></span>           | <span data-ttu-id="228dd-131">Diese Direktive kann auf UTF-8 festgelegt werden, wenn der Server UTF-8 – codierte Benutzernamen und Bereiche verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="228dd-131">This directive can be set to utf-8 if the server can process UTF-8–encoded user names and realms.</span></span> <span data-ttu-id="228dd-132">Wenn der Client die charset-Direktive versteht, kann er mithilfe von UTF-8 – codierten Werten Antworten.</span><span class="sxs-lookup"><span data-stu-id="228dd-132">If the client understands the charset directive, it can respond by using UTF-8–encoded values.</span></span>                                                                                                       |



 

<span data-ttu-id="228dd-133">Microsoft Digest generiert die digestaufforderungs-Zeichenfolge für Server Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="228dd-133">Microsoft Digest generates the Digest challenge string for server applications.</span></span> <span data-ttu-id="228dd-134">Weitere Informationen finden Sie unter [Erstellen der Digest-Herausforderung](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="228dd-134">For details, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

 

 
