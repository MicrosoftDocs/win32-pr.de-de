---
description: Fehlerbehandlung in com+ CRM
ms.assetid: 9de31fb5-31e9-494a-b61f-87bcff0d5085
title: Fehlerbehandlung in com+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aba2b5c4541485433a85fe01fee7870c2e43f62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483451"
---
# <a name="error-handling-in-the-com-crm"></a><span data-ttu-id="45218-103">Fehlerbehandlung in com+ CRM</span><span class="sxs-lookup"><span data-stu-id="45218-103">Error Handling in the COM+ CRM</span></span>

<span data-ttu-id="45218-104">Com+-Server Anwendungen implementieren eine FailFast-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="45218-104">COM+ server applications implement a failfast policy.</span></span> <span data-ttu-id="45218-105">Wenn ein schwerwiegender interner Fehler erkannt wird, wird der Server Anwendungsprozess beendet und eine Fehlermeldung in das Windows-Ereignisprotokoll geschrieben.</span><span class="sxs-lookup"><span data-stu-id="45218-105">If a serious internal error is detected, the server application process exits and writes an error message to the Windows event log.</span></span> <span data-ttu-id="45218-106">Dies ermöglicht eine schnelle Erkennung von Problemen und ist aufgrund des Schutzes von Anwendungsdaten durch die Transaktionsverarbeitung möglich.</span><span class="sxs-lookup"><span data-stu-id="45218-106">This allows quick detection of problems and is possible due to the protection of application data by transaction processing.</span></span> <span data-ttu-id="45218-107">Überprüfen Sie im Windows-Ereignisprotokoll immer, ob während der Entwicklung oder während der letzten Bereitstellung Fehler aus dem CRM vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="45218-107">Always check the Windows event log for any errors from the CRM, either during development or during final deployment.</span></span>

<span data-ttu-id="45218-108">Grundlegende Fehler bei der Verwendung von CRM-Schnittstellen, wie z. b. ungültige Argumente oder Sequenz Fehler (z. b. das Schreiben eines Protokolldaten Satzes vor der Registrierung des CRM-Compensators), geben Fehlercodes zurück und sollten FailFast nicht lösen.</span><span class="sxs-lookup"><span data-stu-id="45218-108">Basic errors in using the CRM interfaces, such as invalid arguments or sequence errors (for example, trying to write a log record before registering the CRM Compensator), return error codes and should not trigger failfast.</span></span> <span data-ttu-id="45218-109">Bei der Entwicklung von CRM können Sie den Registrierungsschlüssel VTRACE1 festlegen (siehe [com+ CRM-Registrierungs Einstellungen](com--crm-registry-settings.md)), der bewirkt, dass im Debugger-Ausgabefenster für jeden Fehler eine Meldung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="45218-109">For CRM development, you may choose to set the VTRACE1 registry key (see [COM+ CRM Registry Settings](com--crm-registry-settings.md)), which causes a message to appear in the debugger output window for each error.</span></span>

<span data-ttu-id="45218-110">Vorübergehende Fehler können ebenfalls auftreten.</span><span class="sxs-lookup"><span data-stu-id="45218-110">Transient errors can also occur.</span></span> <span data-ttu-id="45218-111">Diese Fehler werden in der Regel durch Zeit Steuerungs Bedingungen verursacht und führen dazu, dass ein Fehlercode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="45218-111">These errors are typically caused by timing conditions and result in an error code being returned.</span></span> <span data-ttu-id="45218-112">Der CRM-Entwickler sollte sicherstellen, dass diese Fehlerbedingungen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="45218-112">The CRM developer should ensure that these error conditions are handled.</span></span> <span data-ttu-id="45218-113">Beim Schreiben eines Protokolldaten Satzes könnte die Transaktion z. b. aufgrund eines Timeouts abgebrochen werden. Die-Methode gibt dann einen Fehler zurück, den der Aufrufer entsprechend überprüfen und behandeln soll.</span><span class="sxs-lookup"><span data-stu-id="45218-113">For example, while writing a log record, the transaction could abort due to a time-out. The method then returns an error, which the caller should check for and handle appropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45218-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="45218-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45218-115">Kompensierende com+-Ressourcen-Manager Konzepte</span><span class="sxs-lookup"><span data-stu-id="45218-115">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



