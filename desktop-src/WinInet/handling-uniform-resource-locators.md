---
title: Behandeln von Uniform Resource Locators
description: Eine Uniform Resource Locator (URL) ist eine kompakte Darstellung der Standort-und Zugriffsmethode für eine Ressource, die sich im Internet befindet.
ms.assetid: bb59ada6-f49f-412c-a32c-4fb9495b1222
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08157738d99e78ff4d458a3bdd1b1e2e661ce538
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104551316"
---
# <a name="handling-uniform-resource-locators"></a><span data-ttu-id="6c5c5-103">Behandeln von Uniform Resource Locators</span><span class="sxs-lookup"><span data-stu-id="6c5c5-103">Handling Uniform Resource Locators</span></span>

<span data-ttu-id="6c5c5-104">Eine Uniform Resource Locator (URL) ist eine kompakte Darstellung der Standort-und Zugriffsmethode für eine Ressource, die sich im Internet befindet.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-104">A Uniform Resource Locator (URL) is a compact representation of the location and access method for a resource located on the Internet.</span></span> <span data-ttu-id="6c5c5-105">Jede URL besteht aus einem Schema (http, HTTPS oder FTP) und einer Schema spezifischen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-105">Each URL consists of a scheme (HTTP, HTTPS, or FTP) and a scheme-specific string.</span></span> <span data-ttu-id="6c5c5-106">Diese Zeichenfolge kann auch eine Kombination aus Verzeichnispfad, Such Zeichenfolge oder Name der Ressource enthalten.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-106">This string can also include a combination of a directory path, search string, or name of the resource.</span></span> <span data-ttu-id="6c5c5-107">Die WinInet-Funktionen bieten die Möglichkeit, URLs zu erstellen, zu kombinieren, aufzulösen und zu kanonisieren.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-107">The WinINet functions provide the ability to create, combine, break down, and canonicalize URLs.</span></span> <span data-ttu-id="6c5c5-108">Weitere Informationen zu URLs finden Sie unter [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) für URL (Uniform Resource Locators).</span><span class="sxs-lookup"><span data-stu-id="6c5c5-108">For more information on URLs, see [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) on Uniform Resource Locators (URL).</span></span>

<span data-ttu-id="6c5c5-109">Die URL-Funktionen arbeiten aufgabenorientiert.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-109">The URL functions operate in a task-oriented manner.</span></span> <span data-ttu-id="6c5c5-110">Der Inhalt und das Format der URL, die an die Funktion übergeben wird, werden nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-110">The content and format of the URL that is given to the function is not verified.</span></span> <span data-ttu-id="6c5c5-111">Die aufrufende Anwendung sollte die Verwendung dieser Funktionen nachverfolgen, um sicherzustellen, dass die Daten im vorgesehenen Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-111">The calling application should track the use of these functions to ensure that the data is in the intended format.</span></span> <span data-ttu-id="6c5c5-112">Beispielsweise würde die [**internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) -Funktion das Zeichen "%" in die Escapesequenz "%25" konvertieren, wenn keine Flags verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-112">For example, the [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) function would convert the character "%" into the escape sequence "%25" when using no flags.</span></span> <span data-ttu-id="6c5c5-113">Wenn [**internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) für die kanonisierte URL verwendet wird, wird die Escapesequenz "%25" in die Escapesequenz "%2525" konvertiert, was nicht ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-113">If [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) is used on the canonicalized URL, the escape sequence "%25" would be converted into the escape sequence "%2525", which would not work properly.</span></span>

-   [<span data-ttu-id="6c5c5-114">Was ist eine kanonisierte URL?</span><span class="sxs-lookup"><span data-stu-id="6c5c5-114">What Is a Canonicalized URL?</span></span>](#what-is-a-canonicalized-url)
-   [<span data-ttu-id="6c5c5-115">Verwenden der WinInet-Funktionen zum Verarbeiten von URLs</span><span class="sxs-lookup"><span data-stu-id="6c5c5-115">Using the WinINet Functions to Handle URLs</span></span>](#using-the-wininet-functions-to-handle-urls)
-   [<span data-ttu-id="6c5c5-116">Kanonisierende URLs</span><span class="sxs-lookup"><span data-stu-id="6c5c5-116">Canonicalizing URLs</span></span>](#what-is-a-canonicalized-url)
-   [<span data-ttu-id="6c5c5-117">Kombinieren von Basis-und relativen URLs</span><span class="sxs-lookup"><span data-stu-id="6c5c5-117">Combining Base and Relative URLs</span></span>](#combining-base-and-relative-urls)
-   [<span data-ttu-id="6c5c5-118">Knacken von URLs</span><span class="sxs-lookup"><span data-stu-id="6c5c5-118">Cracking URLs</span></span>](#cracking-urls)
-   [<span data-ttu-id="6c5c5-119">Erstellen von URLs</span><span class="sxs-lookup"><span data-stu-id="6c5c5-119">Creating URLs</span></span>](#creating-urls)
-   [<span data-ttu-id="6c5c5-120">Direktes Aufrufen von URLs</span><span class="sxs-lookup"><span data-stu-id="6c5c5-120">Accessing URLs Directly</span></span>](#accessing-urls-directly)

## <a name="what-is-a-canonicalized-url"></a><span data-ttu-id="6c5c5-121">Was ist eine kanonisierte URL?</span><span class="sxs-lookup"><span data-stu-id="6c5c5-121">What Is a Canonicalized URL?</span></span>

<span data-ttu-id="6c5c5-122">Das Format aller URLs muss der akzeptierten Syntax und Semantik entsprechen, damit Sie über das Internet auf Ressourcen zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-122">The format of all URLs must follow the accepted syntax and semantics in order to access resources through the Internet.</span></span> <span data-ttu-id="6c5c5-123">Kanonisierung ist der Prozess, bei dem eine URL formatiert wird, um diese akzeptierte Syntax und Semantik zu befolgen.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-123">Canonicalization is the process of formatting a URL to follow this accepted syntax and semantics.</span></span>

<span data-ttu-id="6c5c5-124">Zeichen, die codiert werden müssen, enthalten alle Zeichen, die kein entsprechendes Grafikzeichen im US-ASCII-codierten Zeichensatz aufweisen (hexadezimal 80-FF, die nicht im codierten US-ASCII-Zeichensatz verwendet werden, und hexadezimale 00-1f und 7F, die Steuerzeichen sind, Leerzeichen, "%" (zum Codieren anderer Zeichen verwendet) und unsichere Zeichen (<, >, ", \# , {,}, \| , \\ , ^, ~, \[ , \] und ').</span><span class="sxs-lookup"><span data-stu-id="6c5c5-124">Characters that must be encoded include any characters that have no corresponding graphic character in the US-ASCII coded character set (hexadecimal 80-FF, which are not used in the US-ASCII coded character set, and hexadecimal 00-1F and 7F, which are control characters), blank spaces, "%" (which is used to encode other characters), and unsafe characters (<, >, ", \#, {, }, \|, \\, ^, ~, \[, \], and ').</span></span>

## <a name="using-the-wininet-functions-to-handle-urls"></a><span data-ttu-id="6c5c5-125">Verwenden der WinInet-Funktionen zum Verarbeiten von URLs</span><span class="sxs-lookup"><span data-stu-id="6c5c5-125">Using the WinINet Functions to Handle URLs</span></span>

<span data-ttu-id="6c5c5-126">In der folgenden Tabelle werden die URL-Funktionen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-126">The following table summarizes the URL functions.</span></span>



| <span data-ttu-id="6c5c5-127">Funktion</span><span class="sxs-lookup"><span data-stu-id="6c5c5-127">Function</span></span>                                                   | <span data-ttu-id="6c5c5-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c5c5-128">Description</span></span>                                        |
|------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="6c5c5-129">**Internetcanonicalizeurl**</span><span class="sxs-lookup"><span data-stu-id="6c5c5-129">**InternetCanonicalizeUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) | <span data-ttu-id="6c5c5-130">Kanonisiert die URL.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-130">Canonicalizes the URL.</span></span>                             |
| [<span data-ttu-id="6c5c5-131">**Internetcombineurl**</span><span class="sxs-lookup"><span data-stu-id="6c5c5-131">**InternetCombineUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla)           | <span data-ttu-id="6c5c5-132">Kombiniert Basis-und relative URLs.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-132">Combines base and relative URLs.</span></span>                   |
| [<span data-ttu-id="6c5c5-133">**Internetcrackurl**</span><span class="sxs-lookup"><span data-stu-id="6c5c5-133">**InternetCrackUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)               | <span data-ttu-id="6c5c5-134">Analysiert eine URL-Zeichenfolge in-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-134">Parses a URL string into components.</span></span>               |
| [<span data-ttu-id="6c5c5-135">**Internetkreateurl**</span><span class="sxs-lookup"><span data-stu-id="6c5c5-135">**InternetCreateUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)             | <span data-ttu-id="6c5c5-136">Erstellt eine URL-Zeichenfolge aus-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-136">Creates a URL string from components.</span></span>              |
| [<span data-ttu-id="6c5c5-137">**InternetOpenURL**</span><span class="sxs-lookup"><span data-stu-id="6c5c5-137">**InternetOpenUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                 | <span data-ttu-id="6c5c5-138">Startet das Abrufen einer FTP-, http-oder HTTPS-Ressource.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-138">Begins retrieving an FTP, HTTP, or HTTPS resource.</span></span> |



 

## <a name="canonicalizing-urls"></a><span data-ttu-id="6c5c5-139">Kanonisierende URLs</span><span class="sxs-lookup"><span data-stu-id="6c5c5-139">Canonicalizing URLs</span></span>

<span data-ttu-id="6c5c5-140">Die kanonialisierung einer URL ist der Prozess, bei dem eine URL, die möglicherweise unsichere Zeichen (z. b. Leerzeichen, reservierte Zeichen usw.) enthält, in ein akzeptiertes Format konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-140">Canonicalizing a URL is the process that converts a URL, which might contain unsafe characters such as blank spaces, reserved characters, and so on, into an accepted format.</span></span>

<span data-ttu-id="6c5c5-141">Die [**internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) -Funktion kann zum kanonisieren von URLs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-141">The [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) function can be used to canonicalize URLs.</span></span> <span data-ttu-id="6c5c5-142">Diese Funktion ist sehr aufgabenorientiert, sodass die Anwendung die Verwendung sorgfältig verfolgen sollte.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-142">This function is very task-oriented, so the application should track its use carefully.</span></span> <span data-ttu-id="6c5c5-143">[**Internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) überprüft nicht, ob die an Sie übergebenen URL bereits kanonisiert ist und ob die zurückgegebene URL gültig ist.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-143">[**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) does not verify that the URL passed to it is already canonicalized and that the URL that it returns is valid.</span></span>

<span data-ttu-id="6c5c5-144">Die folgenden fünf Flags steuern, wie [**internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) eine bestimmte URL behandelt.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-144">The following five flags control how [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) handles a particular URL.</span></span> <span data-ttu-id="6c5c5-145">Die Flags können in Kombination verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-145">The flags can be used in combination.</span></span> <span data-ttu-id="6c5c5-146">Wenn keine Flags verwendet werden, codiert die Funktion die URL standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-146">If no flags are used, the function encodes the URL by default.</span></span>



| <span data-ttu-id="6c5c5-147">Wert</span><span class="sxs-lookup"><span data-stu-id="6c5c5-147">Value</span></span>                     | <span data-ttu-id="6c5c5-148">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6c5c5-148">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5c5-149">ICU- \_ Browser \_ Modus</span><span class="sxs-lookup"><span data-stu-id="6c5c5-149">ICU\_BROWSER\_MODE</span></span>        | <span data-ttu-id="6c5c5-150">Codieren oder Decodieren Sie keine Zeichen nach " \# " oder "?", und entfernen Sie nachfolgende Leerzeichen nicht nach "?".</span><span class="sxs-lookup"><span data-stu-id="6c5c5-150">Do not encode or decode characters after "\#" or "?", and do not remove trailing white space after "?".</span></span> <span data-ttu-id="6c5c5-151">Wenn dieser Wert nicht angegeben wird, wird die gesamte URL codiert, und nachfolgende Leerzeichen werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-151">If this value is not specified, the entire URL is encoded, and trailing white space is removed.</span></span> |
| <span data-ttu-id="6c5c5-152">ICU- \_ Decodierung</span><span class="sxs-lookup"><span data-stu-id="6c5c5-152">ICU\_DECODE</span></span>               | <span data-ttu-id="6c5c5-153">Konvertieren Sie alle% XX-Sequenzen in Zeichen, einschließlich Escapesequenzen, bevor die URL analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-153">Convert all %XX sequences to characters, including escape sequences, before the URL is parsed.</span></span>                                                                                                          |
| <span data-ttu-id="6c5c5-154">nur in ICU codierende \_ \_ Leerzeichen \_</span><span class="sxs-lookup"><span data-stu-id="6c5c5-154">ICU\_ENCODE\_SPACES\_ONLY</span></span> | <span data-ttu-id="6c5c5-155">Nur Leerzeichen codieren.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-155">Encode spaces only.</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="6c5c5-156">ICU \_ nicht \_ Codieren</span><span class="sxs-lookup"><span data-stu-id="6c5c5-156">ICU\_NO\_ENCODE</span></span>           | <span data-ttu-id="6c5c5-157">Nicht unsichere Zeichen in Escapesequenzen konvertieren.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-157">Do not convert unsafe characters to escape sequences.</span></span>                                                                                                                                                   |
| <span data-ttu-id="6c5c5-158">ICU \_ No \_ Meta</span><span class="sxs-lookup"><span data-stu-id="6c5c5-158">ICU\_NO\_META</span></span>             | <span data-ttu-id="6c5c5-159">Entfernen Sie keine Metasequenzen (z. b. "." und "..") aus der URL.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-159">Do not remove meta sequences (such as "." and "..") from the URL.</span></span>                                                                                                                                       |



 

<span data-ttu-id="6c5c5-160">Das Flag für die ICU- \_ Decodierung sollte nur für kanonisierte URLs verwendet werden, da davon ausgegangen wird, dass es sich bei allen% XX-Sequenzen um Escapecodes handelt, die in die durch den Code aufgeführten Zeichen konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-160">The ICU\_DECODE flag should be used only on canonicalized URLs, because it assumes that all %XX sequences are escape codes and converts them into the characters indicated by the code.</span></span> <span data-ttu-id="6c5c5-161">Wenn die URL das Symbol "%" enthält, das nicht Teil eines Escapecodes ist, behandelt die ICU- \_ Decodierung Sie weiterhin als eins.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-161">If the URL has a "%" symbol in it that is not part of an escape code, ICU\_DECODE still treats it as one.</span></span> <span data-ttu-id="6c5c5-162">Dieses Merkmal kann dazu führen, dass [**internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) eine ungültige URL erstellt.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-162">This characteristic might cause [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) to create an invalid URL.</span></span>

<span data-ttu-id="6c5c5-163">Um [**internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) zum Zurückgeben einer vollständig decodierten URL verwenden zu können, müssen die ICU \_ -decodierungsflags und die ICU-Kennung nicht codiert \_ \_ werden.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-163">To use [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) to return a completely decoded URL, the ICU\_DECODE and ICU\_NO\_ENCODE flags must be specified.</span></span> <span data-ttu-id="6c5c5-164">Dieses Setup geht davon aus, dass die an [**internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) übergebenen URL zuvor kanonisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-164">This setup assumes that the URL being passed to [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) has been previously canonicalized.</span></span>

## <a name="combining-base-and-relative-urls"></a><span data-ttu-id="6c5c5-165">Kombinieren von Basis-und relativen URLs</span><span class="sxs-lookup"><span data-stu-id="6c5c5-165">Combining Base and Relative URLs</span></span>

<span data-ttu-id="6c5c5-166">Ein relative URL ist eine kompakte Darstellung des Speicher Orts einer Ressource in Relation zu einer absoluten Basis-URL.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-166">A relative URL is a compact representation of the location of a resource relative to an absolute base URL.</span></span> <span data-ttu-id="6c5c5-167">Die Basis-URL muss dem Parser bekannt sein und umfasst in der Regel das Schema, den Netzwerk Speicherort und Teile des URL-Pfads.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-167">The base URL must be known to the parser and usually includes the scheme, network location, and parts of the URL path.</span></span> <span data-ttu-id="6c5c5-168">Eine Anwendung kann [**internetcombineurl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) aufgerufen werden, um die relative URL mit ihrer Basis-URL zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-168">An application can call [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) to combine the relative URL with its base URL.</span></span> <span data-ttu-id="6c5c5-169">[**Internetcombineurl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) wird die resultierende URL auch kanonisiert.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-169">[**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) also canonicalizes the resultant URL.</span></span>

## <a name="cracking-urls"></a><span data-ttu-id="6c5c5-170">Knacken von URLs</span><span class="sxs-lookup"><span data-stu-id="6c5c5-170">Cracking URLs</span></span>

<span data-ttu-id="6c5c5-171">Die Funktion [**internetknackurl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) trennt eine URL in Ihre Komponenten Teile und gibt die von der URL- [**\_ Komponenten**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) Struktur, die an die Funktion übermittelt wird, aufgeführten Komponenten zurück.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-171">The [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) function separates a URL into its component parts and returns the components indicated by the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure that is passed to the function.</span></span>

<span data-ttu-id="6c5c5-172">Die Komponenten, die die [**URL- \_ Komponenten**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) Struktur bilden, sind die Schema Nummer, der Hostname, die Portnummer, der Benutzername, das Kennwort, der URL-Pfad und zusätzliche Informationen (z. b. Suchparameter).</span><span class="sxs-lookup"><span data-stu-id="6c5c5-172">The components that make up the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure are the scheme number, host name, port number, user name, password, URL path, and additional information (such as search parameters).</span></span> <span data-ttu-id="6c5c5-173">Jede Komponente, außer dem Schema und den Portnummern, verfügt über einen Zeichen folgen Member, der die Informationen enthält, und einen Member, der die Länge des Zeichen folgen Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-173">Each component, except the scheme and port numbers, has a string member that holds the information, and a member that holds the length of the string member.</span></span> <span data-ttu-id="6c5c5-174">Das Schema und die Portnummern verfügen nur über einen Member, der den entsprechenden Wert speichert. Beide werden bei allen erfolgreichen Aufrufen von [**internetcrackurl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-174">The scheme and port numbers have only a member that stores the corresponding value; they are both returned on all successful calls to [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla).</span></span>

<span data-ttu-id="6c5c5-175">Um den Wert einer bestimmten Komponente in der Struktur der [**URL- \_ Komponenten**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) zu erhalten, muss der Member, der die Zeichen folgen Länge dieser Komponente speichert, auf einen Wert ungleich 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-175">To get the value of a particular component in the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure, the member that stores the string length of that component must be set to a nonzero value.</span></span> <span data-ttu-id="6c5c5-176">Der Zeichen folgen Member kann entweder die Adresse eines Puffers oder **null** sein.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-176">The string member can be either the address of a buffer or **NULL**.</span></span>

<span data-ttu-id="6c5c5-177">Wenn das Zeigermember die Adresse eines Puffers enthält, muss das Zeichen folgen Längen Element die Größe dieses Puffers enthalten.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-177">If the pointer member contains the address of a buffer, the string length member must contain the size of that buffer.</span></span> <span data-ttu-id="6c5c5-178">[**Internetcrackurl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) gibt die Komponenten Informationen als Zeichenfolge im Puffer zurück und speichert die Länge der Zeichenfolge im Zeichen folgen Längen Element.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-178">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) returns the component information as a string in the buffer and stores the string length in the string length member.</span></span>

<span data-ttu-id="6c5c5-179">Wenn das Zeigermember **null** ist, kann das Zeichen folgen Längen Element auf einen Wert ungleich 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-179">If the pointer member is **NULL**, the string length member can be set to any nonzero value.</span></span> <span data-ttu-id="6c5c5-180">[**Internetcrackurl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) speichert die Adresse des ersten Zeichens der URL-Zeichenfolge, die die Komponenten Informationen enthält, und legt die Zeichen folgen Länge auf die Anzahl der Zeichen im verbleibenden Teil der URL-Zeichenfolge fest, die sich auf die Komponente bezieht.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-180">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) stores the address of the first character of the URL string that contains the component information and sets the string length to the number of characters in the remaining part of the URL string that pertains to the component.</span></span>

<span data-ttu-id="6c5c5-181">Alle Zeiger Elemente, die auf **null** festgelegt sind, mit einem Element, das nicht NULL ist, zeigen auf den entsprechenden Startpunkt in der URL-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6c5c5-181">All pointer members set to **NULL** with a nonzero length member point to the appropriate starting point in the URL string.</span></span> <span data-ttu-id="6c5c5-182">Die im Längen Element gespeicherte Länge muss verwendet werden, um das Ende der Informationen der einzelnen Komponente zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-182">The length stored in the length member must be used to determine the end of the individual component's information.</span></span>

<span data-ttu-id="6c5c5-183">Damit die Struktur der [**URL- \_ Komponenten**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) ordnungsgemäß initialisiert wird, muss der **dwstructsize** -Member auf die Größe der [**URL- \_ Komponenten**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) Struktur in Bytes festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-183">To finish initializing the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure properly, the **dwStructSize** member must be set to the size of the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure, in bytes.</span></span>

<span data-ttu-id="6c5c5-184">Im folgenden Beispiel werden die Komponenten der URL im Bearbeitungsfeld, IDC \_ PreOpen1, zurückgegeben, und die Komponenten werden an das Listenfeld IDC \_ preopenlist zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-184">The following example returns the components of the URL in the edit box, IDC\_PreOpen1, and returns the components to the list box, IDC\_PreOpenList.</span></span> <span data-ttu-id="6c5c5-185">Wenn Sie nur die Informationen für eine einzelne Komponente anzeigen möchten, kopiert diese Funktion das Zeichen direkt nach den Informationen der Komponente in der Zeichenfolge und ersetzt diese temporär durch **null**.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-185">To display only the information for an individual component, this function copies the character immediately after the component's information in the string and temporarily replaces it with a **NULL**.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>
#include <wininet.h>
#include <stdlib.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  CRACKER_BUFFER_SIZE           MAX_PATH

// For sample source code implementing the InternetErrorOut( ) 
// function referenced below, see the "Handling Errors" topic  
// under "Using WinInet"
extern BOOL WINAPI InternetErrorOut( HWND hWnd, DWORD dwError,
                                     LPCTSTR szFailingFunctionName );

// Forward declaration of listUrlPart helper functions:
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength );
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, int partValue );

// Static list describing the URL Scheme types 
// enumerated in INTERNET_SCHEME:
TCHAR* schemeType[] =
{
  TEXT( "[Partial URL]" ),                //  0
  TEXT( "[Unknown scheme]" ),             //  1
  TEXT( "[Default scheme]" ),             //  2
  TEXT( "FTP" ),                          //  3
  TEXT( "Gopher" ),                       //  4
  TEXT( "HTTP" ),                         //  5
  TEXT( "HTTPS" ),                        //  6
  TEXT( "File" ),                         //  7
  TEXT( "News" ),                         //  8
  TEXT( "MailTo" ),                       //  9
  TEXT( "Socks" ),                        // 10
  TEXT( "JavaScript" ),                   // 11
  TEXT( "VBScript" )                      // 12
};
#define  CRACKER_SCHEME_TYPE_ARRAY_SIZE      13

BOOL WINAPI Cracker( HWND hDlg, int nURLtextBoxId, int nListBoxId )
{
   int i, j;
   TCHAR* failedFunctionName;
   TCHAR URL_buffer[CRACKER_BUFFER_SIZE];

   URL_COMPONENTS URLparts;

   URLparts.dwStructSize = sizeof( URLparts );

   // The following elements determine which components are displayed
   URLparts.dwSchemeLength    = 1;
   URLparts.dwHostNameLength  = 1;
   URLparts.dwUserNameLength  = 1;
   URLparts.dwPasswordLength  = 1;
   URLparts.dwUrlPathLength   = 1;
   URLparts.dwExtraInfoLength = 1;

   URLparts.lpszScheme     = NULL;
   URLparts.lpszHostName   = NULL;
   URLparts.lpszUserName   = NULL;
   URLparts.lpszPassword   = NULL;
   URLparts.lpszUrlPath    = NULL;
   URLparts.lpszExtraInfo  = NULL;

   SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
   if( !GetDlgItemText( hDlg, nURLtextBoxId, 
                        URL_buffer, CRACKER_BUFFER_SIZE ) )
   {
       failedFunctionName = TEXT( "GetDlgItemText" );
       goto CrackerError_01;
   }

   if( FAILED( StringCchLength( URL_buffer, CRACKER_BUFFER_SIZE, 
                                (size_t*) &i ) ) )
   {
       failedFunctionName = TEXT( "StringCchLength" );
       goto CrackerError_01;
   }

   if( !InternetCrackUrl( URL_buffer, (DWORD)_tcslen( URL_buffer ), 0, 
                          &URLparts ) )
   {
       failedFunctionName = TEXT( "InternetCrackUrl" );
       goto CrackerError_01;
   }

   failedFunctionName = TEXT( "listURLpart" );

   i = URLparts.nScheme + 2;
   if( ( i >= 0 ) && ( i < CRACKER_SCHEME_TYPE_ARRAY_SIZE ) )
   {
       StringCchLength( schemeType[i], 
                        CRACKER_BUFFER_SIZE, 
                        (size_t*) &j );
       if( !listURLpart( hDlg, nListBoxId, 
                         TEXT("Scheme type"), 
                         schemeType[i], j ))
           goto CrackerError_01;
   }

   if( !listURLpart( hDlg, nListBoxId, TEXT( "Scheme text" ), 
                     URLparts.lpszScheme, 
                     URLparts.dwSchemeLength ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Host name" ), 
                     URLparts.lpszHostName, 
                     URLparts.dwHostNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Port number" ), 
                     (int) URLparts.nPort ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "User name" ), 
                     URLparts.lpszUserName, 
                     URLparts.dwUserNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Password" ), 
                     URLparts.lpszPassword, 
                     URLparts.dwPasswordLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Path" ), 
                     URLparts.lpszUrlPath, 
                     URLparts.dwUrlPathLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Extra information"), 
                     URLparts.lpszExtraInfo, 
                     URLparts.dwExtraInfoLength))
           goto CrackerError_01;

   return( TRUE );

CrackerError_01:
// For sample source code of the InternetErrorOut( ) function 
// referenced below, see the "Handling Errors" 
// topic under "Using WinInet"
   InternetErrorOut( hDlg, GetLastError( ), failedFunctionName );
   return FALSE;
}

// listURLpart( ) helper function for string parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];
  LPTSTR nextStart;
  size_t nextSize;

  if( partLength == 0 )  // Just skip empty ones
    return( TRUE );

  if( FAILED( StringCchCopyEx( outputBuffer, 
                              (size_t) CRACKER_BUFFER_SIZE,
                               szPartName, &nextStart, 
                               &nextSize, 0 ) ) ||
      FAILED( StringCchCopyEx( nextStart, nextSize, TEXT( ": " ), 
                               &nextStart, &nextSize, 0 ) ) ||
      FAILED( StringCchCopyNEx( nextStart, nextSize, part, 
                                (size_t) partLength,
                                &nextStart, &nextSize, 0 ) ) )
    return( FALSE );

  *nextStart = 0;
  if( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                          (LPARAM)outputBuffer ) < 0 )
    return( FALSE );
  return( TRUE );
}

// listURLpart( ) helper function for numeric parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, int partValue )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];

  if( FAILED( StringCchPrintf( outputBuffer, 
                               (size_t) CRACKER_BUFFER_SIZE,
                               TEXT( "%s: %d" ), szPartName, 
                               partValue ) ) ||
      ( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                            (LPARAM)outputBuffer ) < 0 ) )
    return( FALSE );
  return( TRUE );
}
```



## <a name="creating-urls"></a><span data-ttu-id="6c5c5-186">Erstellen von URLs</span><span class="sxs-lookup"><span data-stu-id="6c5c5-186">Creating URLs</span></span>

<span data-ttu-id="6c5c5-187">Die [**internetkreateurl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) -Funktion verwendet die Informationen in der Struktur der [**URL- \_ Komponenten**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , um eine Uniform Resource Locator zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-187">The [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) function uses the information in the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure to create a Uniform Resource Locator.</span></span>

<span data-ttu-id="6c5c5-188">Die Komponenten, aus denen die [**URL- \_ Komponenten**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) Struktur besteht, sind das Schema, der Hostname, die Portnummer, der Benutzername, das Kennwort, der URL-Pfad und zusätzliche Informationen (z. b. Suchparameter).</span><span class="sxs-lookup"><span data-stu-id="6c5c5-188">The components that make up the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure are the scheme, host name, port number, user name, password, URL path, and additional information (such as search parameters).</span></span> <span data-ttu-id="6c5c5-189">Jede Komponente, außer der Portnummer, verfügt über einen Zeichen folgen Member, der die Informationen enthält, und einen Member, der die Länge des Zeichen folgen Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-189">Each component, except the port number, has a string member that holds the information, and a member that holds the length of the string member.</span></span>

<span data-ttu-id="6c5c5-190">Für jede erforderliche Komponente sollte das Zeigermember die Adresse des Puffers enthalten, der die Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-190">For each required component, the pointer member should contain the address of the buffer holding the information.</span></span> <span data-ttu-id="6c5c5-191">Das Längen Element muss auf 0 (null) festgelegt werden, wenn das Zeigermember die Adresse einer null-terminierten Zeichenfolge enthält. Das Längen Element muss auf die Länge der Zeichenfolge festgelegt werden, wenn das Zeigermember die Adresse einer Zeichenfolge enthält, die nicht mit 0 (null) beendet wird.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-191">The length member should be set to zero if the pointer member contains the address of a zero-terminated string; the length member should be set to the string length if the pointer member contains the address of a string that is not zero-terminated.</span></span> <span data-ttu-id="6c5c5-192">Das Zeiger Element von Komponenten, die nicht erforderlich sind, muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-192">The pointer member of any components that are not required must be **NULL**.</span></span>

## <a name="accessing-urls-directly"></a><span data-ttu-id="6c5c5-193">Direktes Aufrufen von URLs</span><span class="sxs-lookup"><span data-stu-id="6c5c5-193">Accessing URLs Directly</span></span>

<span data-ttu-id="6c5c5-194">Auf FTP-und http-Ressourcen im Internet kann direkt mithilfe der Funktionen [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)und [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-194">FTP, and HTTP resources on the Internet can be accessed directly by using the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), and [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) functions.</span></span> <span data-ttu-id="6c5c5-195">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) öffnet eine Verbindung mit der Ressource an der URL, die an die Funktion übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-195">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) opens a connection to the resource at the URL passed to the function.</span></span> <span data-ttu-id="6c5c5-196">Wenn diese Verbindung hergestellt wird, können zwei Schritte ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-196">When this connection is made, there are two possible steps.</span></span> <span data-ttu-id="6c5c5-197">Wenn es sich bei der Ressource um eine Datei handelt, kann Sie von " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) " heruntergeladen werden. Zweitens: Wenn es sich bei der Ressource um ein Verzeichnis handelt, kann [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) die Dateien im Verzeichnis auflisten (außer bei Verwendung von CERN-Proxys).</span><span class="sxs-lookup"><span data-stu-id="6c5c5-197">First, if the resource is a file, [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) can download it; second, if the resource is a directory, [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) can enumerate the files within the directory (except when using CERN proxies).</span></span> <span data-ttu-id="6c5c5-198">Weitere Informationen zu " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)" finden Sie unter [Lesen von Dateien](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6c5c5-198">For more information on [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), see [Reading Files](common-functions.md).</span></span> <span data-ttu-id="6c5c5-199">Weitere Informationen zu [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)finden Sie untersuchen [der nächsten Datei](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6c5c5-199">For more information on [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), see [Finding the Next File](common-functions.md).</span></span>

<span data-ttu-id="6c5c5-200">Für Anwendungen, die über einen CERN-Proxy ausgeführt werden müssen, kann [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) für den Zugriff auf FTP-Verzeichnisse und-Dateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-200">For applications that need to operate through a CERN proxy, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) can be used to access FTP directories and files.</span></span> <span data-ttu-id="6c5c5-201">Die FTP-Anforderungen werden verpackt, damit Sie wie eine HTTP-Anforderung angezeigt werden, die der CERN-Proxy akzeptieren würde.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-201">The FTP requests are packaged to appear like an HTTP request, which the CERN proxy would accept.</span></span>

<span data-ttu-id="6c5c5-202">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) verwendet das [**hinternethandle**](appendix-a-hinternet-handles.md) , das von der [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) -Funktion erstellt wurde, und die URL der Ressource.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-202">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) uses the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function and the URL of the resource.</span></span> <span data-ttu-id="6c5c5-203">Die URL muss das Schema (http:, FTP:, file: \[ für eine lokale Datei \] oder https: für ein \[ Hypertext-Protokoll sicher \] ) und einen Netzwerk Speicherort (z `www.microsoft.com` . b.) enthalten.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-203">The URL must include the scheme (http:, ftp:, file: \[for a local file\], or https: \[for hypertext protocol secure\]) and network location (such as `www.microsoft.com`).</span></span> <span data-ttu-id="6c5c5-204">Die URL kann auch einen Pfad enthalten (z. b./isapi/gomscom.ASP? Target =/Windows/Feature/) und Ressourcen Name (z. b. default.htm).</span><span class="sxs-lookup"><span data-stu-id="6c5c5-204">The URL can also include a path (for example, /isapi/gomscom.asp?TARGET=/windows/feature/) and resource name (for example, default.htm).</span></span> <span data-ttu-id="6c5c5-205">Für http-oder HTTPS-Anforderungen können zusätzliche Header eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-205">For HTTP or HTTPS requests, additional headers can be included.</span></span>

<span data-ttu-id="6c5c5-206">[**Internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)und [**internetsetfilepointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (nur http-oder HTTPS-URLs) können das Handle verwenden, das von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) zum Herunterladen der Ressource erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-206">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP or HTTPS URLs only) can use the handle that is created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) to download the resource.</span></span>

<span data-ttu-id="6c5c5-207">Im folgenden Diagramm wird veranschaulicht, welche Handles für die einzelnen Funktionen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-207">The following diagram illustrates which handles to use with each function.</span></span>

![mit Functions zu verwendende Handles](images/ax-wnt02.png)

<span data-ttu-id="6c5c5-209">Das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) erstellte Stamm- [**HINTERNET**](appendix-a-hinternet-handles.md) Handle wird von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-209">The root [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) is used by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span> <span data-ttu-id="6c5c5-210">Das **hinternethandle** , das von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) erstellt wurde, kann von [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (hier nicht gezeigt) und [**internetsetfilepointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (nur http-oder HTTPS-URLs) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-210">The **HINTERNET** handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) can be used by [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (not shown here), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP or HTTPS URLs only).</span></span>

<span data-ttu-id="6c5c5-211">Weitere Informationen finden Sie unter [**HINTERNET Handles**](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="6c5c5-211">For more information, see [**HINTERNET Handles**](appendix-a-hinternet-handles.md).</span></span>

> [!Note]  
> <span data-ttu-id="6c5c5-212">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-212">WinINet does not support server implementations.</span></span> <span data-ttu-id="6c5c5-213">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c5c5-213">In addition, it should not be used from a service.</span></span> <span data-ttu-id="6c5c5-214">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="6c5c5-214">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 