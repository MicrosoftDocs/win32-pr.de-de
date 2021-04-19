---
description: Wenn das Betriebssystem oder sogar eine Anwendung für die Verwendung einer bestimmten Sprache und eines bestimmten Gebiets Schemas festgelegt ist, sind viele Einstellungen betroffen.
ms.assetid: cec164d1-125f-483c-9d74-0e24b8215157
title: Gebiets Schema Einstellungen für Dokumente und Systeme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9408093a8583a4b17566b5fcd118b30439c0ebda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350393"
---
# <a name="document-and-system-locale-settings"></a><span data-ttu-id="18957-103">Gebiets Schema Einstellungen für Dokumente und Systeme</span><span class="sxs-lookup"><span data-stu-id="18957-103">Document and System Locale Settings</span></span>

<span data-ttu-id="18957-104">Wenn das Betriebssystem oder sogar eine Anwendung für die Verwendung einer bestimmten Sprache und eines bestimmten Gebiets Schemas festgelegt ist, sind viele Einstellungen betroffen.</span><span class="sxs-lookup"><span data-stu-id="18957-104">When the operating system, or even an application, is set to use a particular language and locale, many settings are affected.</span></span> <span data-ttu-id="18957-105">Diese Einstellungen umfassen das numerische Format, das Datumsformat, das Währungs Format, die Zuordnung von Groß-und Kleinbuchstaben, die Sortierreihenfolge für Wörterbücher, die Tokenisierung und andere.</span><span class="sxs-lookup"><span data-stu-id="18957-105">These settings include numeric format, date format, currency format, uppercase and lowercase mapping, dictionary sort ordering, tokenization, and others.</span></span> <span data-ttu-id="18957-106">Obwohl diese Einstellungen Windows Search helfen, eine hervorragende lokalisierte Unterstützung zu bieten, können unerwartete Ergebnisse auftreten, wenn Dokumente aus einem Gebiets Schema durchsucht werden, indem ein System verwendet wird, das auf ein anderes Gebiets Schema</span><span class="sxs-lookup"><span data-stu-id="18957-106">Although these settings help Windows Search provide excellent localized support, unexpected results can occur when documents from one locale are searched by using a system that is set to another locale.</span></span>

<span data-ttu-id="18957-107">Wenn das [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Objekt die Texteigenschaften und den Inhalt eines Dokuments verarbeitet, meldet es dem inhaltsindexer die Sprache des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="18957-107">When the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) object processes a document's text properties and content, it reports the language of that document to the content indexer.</span></span> <span data-ttu-id="18957-108">Mithilfe dieser Informationen kann Windows Search die entsprechende Wörter Trennung anwenden.</span><span class="sxs-lookup"><span data-stu-id="18957-108">Using this information, Windows Search can apply the appropriate word breaker.</span></span>

 

 
