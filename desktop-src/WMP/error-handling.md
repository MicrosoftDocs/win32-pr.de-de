---
title: Fehlerbehandlung (Windows Media Player SDK)
description: Fehlerbehandlung
ms.assetid: f0567c77-a855-4b93-9fb7-a36cde63859f
keywords:
- Windows Media Player, Fehlerbehandlung
- Windows Media Player-Objektmodell, Fehlerbehandlung
- Objektmodell, Fehlerbehandlung
- Windows Media Player ActiveX-Steuerelement, Fehlerbehandlung
- ActiveX-Steuerelement, Fehlerbehandlung
- Windows Media Player Mobile ActiveX-Steuerelement, Fehlerbehandlung
- Windows Media Player Mobile, Fehlerbehandlung
- Migrations Handbuch, Fehlerbehandlung
- Fehlerbehandlung im Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3b96e04d24009ee4b7e5819fdb26dfd6effd63
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102626"
---
# <a name="error-handling-windows-media-player-sdk"></a><span data-ttu-id="c7356-112">Fehlerbehandlung (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="c7356-112">Error Handling (Windows Media Player SDK)</span></span>

<span data-ttu-id="c7356-113">Das ActiveX-Steuerelement von Windows Media Player 6,4 bietet eine standardmäßige Fehlerbehandlung, indem Fehlermeldungen in Dialogfeldern und in der Statusleiste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c7356-113">The Windows Media Player 6.4 ActiveX control provides default error handling by displaying error messages in dialog boxes and on the status bar.</span></span> <span data-ttu-id="c7356-114">Sie können auch eine benutzerdefinierte Fehlerbehandlung bereitstellen, indem Sie Fehler in Ihrem Skript verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c7356-114">You can also provide custom error handling by processing errors in your script.</span></span> <span data-ttu-id="c7356-115">Die Fehlerbehandlung erfolgt durch ereignisgesteuert. Dies bedeutet, dass Sie für jeden Fehler eine Benachrichtigung erhalten, und Sie müssen entscheiden, wie die einzelnen Fehlerereignisse behandelt werden sollen, wenn Sie auftreten.</span><span class="sxs-lookup"><span data-stu-id="c7356-115">Error handling is event driven, which means you receive a notification for each error, and must decide how to deal with each error event when it occurs.</span></span> <span data-ttu-id="c7356-116">Weitere Informationen zur Behandlung von Fehlern mit dem Objektmodell der Version 6,4 finden Sie im Abschnitt zur Fehlerbehandlung im Handbuch zu Version 6,4 Player-Objekt Modellen, der Teil des Windows Media Player SDK ist.</span><span class="sxs-lookup"><span data-stu-id="c7356-116">For more information about handling errors using the version 6.4 object model, see the Error Handling section of the Version 6.4 Player Object Model Guide, which is part of the Windows Media Player SDK.</span></span>

<span data-ttu-id="c7356-117">Das Objektmodell Windows Media Player 7 oder höher stellt das **Fehler** Objekt und das **ErrorItem** -Objekt bereit, um Fehler zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="c7356-117">The Windows Media Player 7 or later object model provides the **Error** object and the **ErrorItem** object to handle errors.</span></span> <span data-ttu-id="c7356-118">Diese beiden Objekte arbeiten zusammen, um Ihnen einen Fehler Behandlungs Mechanismus bereitzustellen, mit dem Sie den Fehler Behandlungsprozess vervollständigen und flexibel steuern können.</span><span class="sxs-lookup"><span data-stu-id="c7356-118">These two objects work together to provide you with an error handling mechanism that gives you complete and flexible control of the error handling process.</span></span> <span data-ttu-id="c7356-119">Das **Error** -Objekt ermöglicht den Zugriff auf eine Auflistung von **ErrorItem** -Objekten. Jedes **ErrorItem** -Objekt stellt Details zu einer einzelnen Fehlermeldung bereit.</span><span class="sxs-lookup"><span data-stu-id="c7356-119">The **Error** object provides access to a collection of **ErrorItem** objects; each **ErrorItem** object provides details about an individual error message.</span></span>

<span data-ttu-id="c7356-120">Wenn ein Fehler auftritt, werden die Fehlerinformationen an eine Fehler Warteschlange gesendet.</span><span class="sxs-lookup"><span data-stu-id="c7356-120">When an error occurs, the error information is posted to an error queue.</span></span> <span data-ttu-id="c7356-121">Die Warteschlange ist eine Sammlung von **ErrorItem** -Objekten.</span><span class="sxs-lookup"><span data-stu-id="c7356-121">The queue is a collection of **ErrorItem** objects.</span></span> <span data-ttu-id="c7356-122">Jeder Fehler, der der Warteschlange hinzugefügt wird, ist einer Indexnummer (beginnend mit null) zugeordnet, die zum Identifizieren des jeweiligen **ErrorItem** -Objekts verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7356-122">As each error is added to the queue, it is associated with an index number (beginning with zero) that can be used to identify the particular **ErrorItem** object.</span></span> <span data-ttu-id="c7356-123">Der *Fehler*. die **errorCount** -Eigenschaft ruft die Anzahl der Fehler in der Fehler Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="c7356-123">The *Error*.**errorCount** property retrieves the number of errors in the error queue.</span></span> <span data-ttu-id="c7356-124">Da die Indexnummern Null basiert sind, weist der letzte Fehler, der an die Warteschlange gesendet wird, immer einen Indexwert auf, der " *Error*" entspricht. **errorCount** minus 1.</span><span class="sxs-lookup"><span data-stu-id="c7356-124">Since the index numbers are zero-based, the most recent error posted to the queue will always have an index value equal to *Error*.**errorCount** minus one.</span></span>

<span data-ttu-id="c7356-125">Sie können einen Fehler Ereignishandler für Windows-Media Player mithilfe eines Skripts erstellen.</span><span class="sxs-lookup"><span data-stu-id="c7356-125">You can create an error event handler for Windows Media Player using script.</span></span> <span data-ttu-id="c7356-126">Im folgenden JScript-Beispiel wird gezeigt, wie das letzte Fehler Element aus der Fehler Warteschlange abgerufen und der Fehlercode und die Fehlerbeschreibung mithilfe des Objektmodells Windows Media Player 7 oder höher angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c7356-126">The following JScript example shows how to retrieve the most recent error item from the error queue and display the error code and error description using the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="c7356-127">Das **Player** -Objekt wurde mit ID = "WMP9" erstellt.</span><span class="sxs-lookup"><span data-stu-id="c7356-127">The **Player** object was created with ID = "WMP9".</span></span>


```C++
<!-- Create an error event handler for Windows Media Player 7 or later errors. -->
<SCRIPT  LANGUAGE = "JScript"  FOR = WMP9  EVENT = error()>

// Store the number of errors in the error queue.
var max = WMP9.error.errorCount;

// Retrieve most recent ErrorItem object.
var err = WMP9.error.item(max-1)

// Store the error code number.
var errNum = err.errorCode;

// Store the error description string.
var errDesc = err.errorDescription;

// Build a message string to notify the user.
var msg = "Error number: " + errNum + "\n";
msg += "Error description: " + errDesc;

// Display the message box.
alert(msg);

</SCRIPT>

```



<span data-ttu-id="c7356-128">Das **Error** -Objekt verfügt über zwei zusätzliche Methoden, die Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c7356-128">The **Error** object has two additional methods that you can use.</span></span> <span data-ttu-id="c7356-129">Der *Fehler*. mit der **clearerrorqueue** -Methode können Sie alle Fehler aus der Fehler Warteschlange entfernen und die Indexnummer auf Null zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="c7356-129">The *Error*.**clearErrorQueue** method allows you to remove all the errors from the error queue and reset the index number to zero.</span></span> <span data-ttu-id="c7356-130">Sie haben die komplette Kontrolle über diesen Prozess. Sie können Fehler in der Warteschlange so lange beibehalten, wie Sie verfügbar sein müssen, und dann die Warteschlange leeren, wenn Sie die Fehlerbehandlung abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="c7356-130">You have complete control over this process; you can keep errors in the queue for as long as you need them to be available, and then empty the queue when you're finished handling the errors.</span></span>

<span data-ttu-id="c7356-131">Der *Fehler*. die **WebHelp** -Methode bietet eine Möglichkeit, dem Benutzer die aktuellsten Fehlerinformationen über das Internet anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c7356-131">The *Error*.**webHelp** method provides a way to display the most current error information to the user by using the Internet.</span></span> <span data-ttu-id="c7356-132">Beim Aufrufen überträgt diese Methode alle relevanten Informationen zum ersten Fehler in der Warteschlange (der mit dem Index 0 (null)) an die Microsoft Windows Media Player-Webhilfe, die weitere Informationen über den Fehler im aktuellen Browserfenster anzeigt.</span><span class="sxs-lookup"><span data-stu-id="c7356-132">When called, this method transfers all relevant information about the first error in the queue (the one with index zero) to Microsoft Windows Media Player Web Help, which displays further information about the error in the current browser window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7356-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c7356-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7356-134">**Error-Objekt**</span><span class="sxs-lookup"><span data-stu-id="c7356-134">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="c7356-135">**ErrorItem-Objekt**</span><span class="sxs-lookup"><span data-stu-id="c7356-135">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="c7356-136">**Handbuch für die Migration des Objektmodells**</span><span class="sxs-lookup"><span data-stu-id="c7356-136">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




