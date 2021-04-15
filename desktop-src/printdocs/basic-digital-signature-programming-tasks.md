---
description: In diesem Abschnitt wird beschrieben, wie grundlegende Programmieraufgaben mit der XPS Digital Signature-API ausgeführt werden.
ms.assetid: a25a8d33-000a-4774-8beb-56d3bb39d5ae
title: Allgemeine Programmieraufgaben für digitale Signaturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 346b29c7768f4c4e972284afa697f97bb1da5f69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485803"
---
# <a name="common-digital-signature-programming-tasks"></a><span data-ttu-id="b491a-103">Allgemeine Programmieraufgaben für digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="b491a-103">Common Digital Signature Programming Tasks</span></span>

<span data-ttu-id="b491a-104">In diesem Abschnitt wird beschrieben, wie grundlegende Programmieraufgaben mit der XPS Digital Signature-API ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b491a-104">This section describes how to perform basic programming tasks with the XPS Digital Signature API.</span></span>

<span data-ttu-id="b491a-105">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="b491a-105">Tasks</span></span>

-   [<span data-ttu-id="b491a-106">Initialisieren des Signatur-Managers</span><span class="sxs-lookup"><span data-stu-id="b491a-106">Initialize the Signature Manager</span></span>](initialize-the-signature-manager.md)
-   [<span data-ttu-id="b491a-107">Signieren eines Dokuments</span><span class="sxs-lookup"><span data-stu-id="b491a-107">Sign a Document</span></span>](sign-a-document.md)
-   [<span data-ttu-id="b491a-108">Hinzufügen einer Signatur Anforderung zu einem XPS-Dokument</span><span class="sxs-lookup"><span data-stu-id="b491a-108">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
-   [<span data-ttu-id="b491a-109">Überprüfen von Dokument Signaturen</span><span class="sxs-lookup"><span data-stu-id="b491a-109">Verify Document Signatures</span></span>](verify-document-signatures.md)

## <a name="disclaimer"></a><span data-ttu-id="b491a-110">Haftungsausschluss</span><span class="sxs-lookup"><span data-stu-id="b491a-110">Disclaimer</span></span>

<span data-ttu-id="b491a-111">Code Beispiele sind nicht als komplett und funktionierende Programme gedacht.</span><span class="sxs-lookup"><span data-stu-id="b491a-111">Code examples are not intended to be complete and working programs.</span></span> <span data-ttu-id="b491a-112">Die Codebeispiele, auf die auf dieser Seite verwiesen wird, führen beispielsweise keine Parameter Überprüfung, Fehlerüberprüfung, vollständige Arbeitsspeicher-oder Ressourcenverwaltung oder Fehlerbehandlung aus.</span><span class="sxs-lookup"><span data-stu-id="b491a-112">The code examples that are referenced on this page, for example, do not perform parameter checking, error checking, complete memory or resource management, or error handling.</span></span> <span data-ttu-id="b491a-113">Verwenden Sie diese Beispiele als Ausgangspunkt, und fügen Sie dann den erforderlichen Code hinzu, um eine robuste Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b491a-113">Use these examples as a starting point, then add the necessary code to create a robust application.</span></span> <span data-ttu-id="b491a-114">Weitere Informationen zu den **HRESULT** -Rückgabe Werten und Fehlerbehandlungsstrategien finden Sie unter [Fehlerbehandlung in com](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="b491a-114">For more information about **HRESULT** return values and error handling strategies, see [Error Handling in COM](../com/error-handling-in-com.md).</span></span>

<span data-ttu-id="b491a-115">Aus Gründen der Übersichtlichkeit verwenden diese Codebeispiele sehr einfache XPS-Dokument-und-Signatur Szenarien, die für Ihre Anforderungen möglicherweise nicht ausreichend komplex sind.</span><span class="sxs-lookup"><span data-stu-id="b491a-115">For clarity, these code examples use very simple XPS document and signature scenarios, which might not be sufficiently complex to meet your needs.</span></span>

 

 
