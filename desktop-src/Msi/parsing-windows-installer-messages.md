---
description: Ein externer Benutzeroberflächen Handler kann die Liste der vom dwmessagedfilter-Parameter der msisettexternalui-Funktion angegebenen Installationsprogramm Nachrichten verarbeiten.
ms.assetid: c4405803-9abd-40f4-9090-c075e7dcf293
title: Windows Installer Meldungen werden verarbeitet.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65cf96c85499b44accd0e01548ca184a030775d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215360"
---
# <a name="parsing-windows-installer-messages"></a><span data-ttu-id="44275-103">Windows Installer Meldungen werden verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="44275-103">Parsing Windows Installer Messages</span></span>

<span data-ttu-id="44275-104">Ein externer Benutzeroberflächen Handler kann die Liste der vom *dwmessagedfilter* -Parameter der [**msisettexternalui**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) -Funktion angegebenen Installationsprogramm Nachrichten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="44275-104">An external UI handler can process the list of installer messages specified by the *dwMessagedFilter* parameter of the [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) function.</span></span> <span data-ttu-id="44275-105">Einige dieser Nachrichten enthalten Zeichen folgen, die direkt verwendet werden können. andere Meldungen müssen möglicherweise analysiert und vom externen UI-Handler verarbeitet werden, damit Sie hilfreich sind.</span><span class="sxs-lookup"><span data-stu-id="44275-105">Some of these messages contain strings that can be used directly, and other messages may need to be parsed and processed by the external UI handler to be useful.</span></span> <span data-ttu-id="44275-106">Der externe Benutzeroberflächen Handler muss möglicherweise nur Windows Installer Nachrichten überwachen, ohne einen Vorgang auszuführen, der sich auf die Installation auswirkt.</span><span class="sxs-lookup"><span data-stu-id="44275-106">Your external UI handler may only need to monitor Windows Installer messages without performing any operation that affects the installation.</span></span>

<span data-ttu-id="44275-107">Die folgenden Windows Installer Meldungen enthalten Zeichen folgen, die von einem Dialogfeld angezeigt werden können und keine zusätzliche Verarbeitung erfordern.</span><span class="sxs-lookup"><span data-stu-id="44275-107">The following Windows Installer messages contain strings that can be displayed by a dialog box and need no additional processing.</span></span> <span data-ttu-id="44275-108">Diese Meldungen enthalten eine Liste von Schaltflächen und Symbolen, die von einem Dialogfeld angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="44275-108">These messages contain a list of buttons and icons that are to be displayed by a dialog box.</span></span> <span data-ttu-id="44275-109">Zum Angeben von Symbolen und Schaltflächen können Sie die Werte für die **\_ typemasken** "MB", "MB" und **"MB" \_** verwenden. **\_**</span><span class="sxs-lookup"><span data-stu-id="44275-109">You can use the **MB\_ICONMASK**, **MB\_DEFMASK**, and **MB\_TYPEMASK** values to specify icons and buttons.</span></span>

<dl> <dt>

<span data-ttu-id="44275-110"><span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**installmessage \_ fatalexit**</span><span class="sxs-lookup"><span data-stu-id="44275-110"><span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**INSTALLMESSAGE\_FATALEXIT**</span></span>
</dt> <dd>

<span data-ttu-id="44275-111">Eine vorzeitige Beendigung der Installation ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="44275-111">Premature termination of installation has occurred.</span></span>

</dd> <dt>

<span data-ttu-id="44275-112"><span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**installmessage- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="44275-112"><span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**INSTALLMESSAGE\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="44275-113">Formatierte Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="44275-113">Formatted error message.</span></span>

</dd> <dt>

<span data-ttu-id="44275-114"><span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**installmessage- \_ Warnung**</span><span class="sxs-lookup"><span data-stu-id="44275-114"><span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**INSTALLMESSAGE\_WARNING**</span></span>
</dt> <dd>

<span data-ttu-id="44275-115">Formatierte Warnmeldung.</span><span class="sxs-lookup"><span data-stu-id="44275-115">Formatted warning message.</span></span>

</dd> <dt>

<span data-ttu-id="44275-116"><span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**installmessage- \_ Info**</span><span class="sxs-lookup"><span data-stu-id="44275-116"><span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**INSTALLMESSAGE\_INFO**</span></span>
</dt> <dd>

<span data-ttu-id="44275-117">Formatierte Protokollmeldung.</span><span class="sxs-lookup"><span data-stu-id="44275-117">Formatted log message.</span></span>

</dd> <dt>

<span data-ttu-id="44275-118"><span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**installmessage- \_ Benutzer**</span><span class="sxs-lookup"><span data-stu-id="44275-118"><span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**INSTALLMESSAGE\_USER**</span></span>
</dt> <dd>

<span data-ttu-id="44275-119">Formatierte Benutzer Meldung.</span><span class="sxs-lookup"><span data-stu-id="44275-119">Formatted user message.</span></span>

</dd> <dt>

<span data-ttu-id="44275-120"><span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**installmessage \_ oudeatdiskspace**</span><span class="sxs-lookup"><span data-stu-id="44275-120"><span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**INSTALLMESSAGE\_OUTOFDISKSPACE**</span></span>
</dt> <dd>

<span data-ttu-id="44275-121">Formatierte Meldung, die auf eine nicht genügend Speicherplatz Bedingung hinweist</span><span class="sxs-lookup"><span data-stu-id="44275-121">Formatted message indicating an out of disk space condition</span></span>

</dd> </dl>

<span data-ttu-id="44275-122">Der externe Benutzer Handler kann die folgenden Windows Installer Nachrichten verwenden, um eine Sequenz der Windows Installer-Benutzeroberfläche zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="44275-122">The external user handler can use the following Windows Installer messages to monitor a sequence of the Windows Installer UI.</span></span> <span data-ttu-id="44275-123">Das Installationsprogramm sendet diese Nachrichten zu Beginn einer Windows Installer UI-Sequenz, wenn jedes Dialogfeld angezeigt wird, und am Ende der UI-Sequenz.</span><span class="sxs-lookup"><span data-stu-id="44275-123">The installer sends these messages at the start of a Windows Installer UI sequence, as each dialog box is displayed, and at the end of the UI sequence.</span></span> <span data-ttu-id="44275-124">Es ist keine Verarbeitung erforderlich, um diese Nachrichten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="44275-124">No processing is required to use these messages.</span></span>

<dl> <dt>

<span data-ttu-id="44275-125"><span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>installmessage \_ Beenden</span><span class="sxs-lookup"><span data-stu-id="44275-125"><span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>INSTALLMESSAGE\_TERMINATE</span></span>
</dt> <dd>

<span data-ttu-id="44275-126">Diese Meldung gibt das Ende der UI-Sequenz an.</span><span class="sxs-lookup"><span data-stu-id="44275-126">This message indicates the end of the UI sequence.</span></span> <span data-ttu-id="44275-127">Die Zeichenfolge ist eine NULL-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="44275-127">The string is a null string.</span></span>

</dd> <dt>

<span data-ttu-id="44275-128"><span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>installmessage \_ initialisieren</span><span class="sxs-lookup"><span data-stu-id="44275-128"><span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>INSTALLMESSAGE\_INITIALIZE</span></span>
</dt> <dd>

<span data-ttu-id="44275-129">Diese Meldung gibt an, dass die UI-Sequenz gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="44275-129">This message indicates that the UI sequence has started.</span></span> <span data-ttu-id="44275-130">Die Zeichenfolge ist eine NULL-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="44275-130">The string is a null string.</span></span>

</dd> <dt>

<span data-ttu-id="44275-131"><span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>installmessage \_ Show Dialog</span><span class="sxs-lookup"><span data-stu-id="44275-131"><span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE\_SHOWDIALOG</span></span>
</dt> <dd>

<span data-ttu-id="44275-132">Die Zeichenfolge enthält den Namen des aktuellen Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="44275-132">The string contains the name of the current dialog box.</span></span>

</dd> </dl>

<span data-ttu-id="44275-133">Die folgenden Windows Installer Meldungen erfordern eine zusätzliche Verarbeitung durch den externen UI-Handler.</span><span class="sxs-lookup"><span data-stu-id="44275-133">The following Windows Installer messages require additional processing by the external UI handler.</span></span>

<dl> <dt>

<span data-ttu-id="44275-134"><span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**installmessage \_ ResolveSource**</span><span class="sxs-lookup"><span data-stu-id="44275-134"><span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**INSTALLMESSAGE\_RESOLVESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="44275-135">Der externe Benutzeroberflächen Handler muss 0 (null) zurückgeben und es Windows Installer ermöglichen, die Nachricht zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="44275-135">The external user interface handler must return 0 and allow Windows Installer to handle the message.</span></span> <span data-ttu-id="44275-136">Der Handler für die externe Benutzeroberfläche kann diese Meldung überwachen, sollte jedoch keine Aktionen ausführen, die sich auf die Installation auswirken.</span><span class="sxs-lookup"><span data-stu-id="44275-136">The external user interface handler can monitor for this message, but it should not perform any action that affects the installation .</span></span>

</dd> <dt>

<span data-ttu-id="44275-137"><span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**installmessage \_ FilesInUse**</span><span class="sxs-lookup"><span data-stu-id="44275-137"><span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**INSTALLMESSAGE\_FILESINUSE**</span></span>
</dt> <dd>

<span data-ttu-id="44275-138">Die externe Benutzeroberfläche sollte in Reaktion auf diese Meldung ein [FilesInUse-Dialog](filesinuse-dialog.md) Feld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="44275-138">The external UI should display a [FilesInUse dialog](filesinuse-dialog.md) in response to this message.</span></span>

</dd> <dt>

<span data-ttu-id="44275-139"><span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**installmessage \_ rmfilesinuse**</span><span class="sxs-lookup"><span data-stu-id="44275-139"><span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**INSTALLMESSAGE\_RMFILESINUSE**</span></span>
</dt> <dd>

<span data-ttu-id="44275-140">Die externe Benutzeroberfläche sollte in Reaktion auf diese Meldung ein [msirmfilesinuse-Dialog](msirmfilesinuse-dialog.md) Feld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="44275-140">The external UI should display a [MsiRMFilesInUse dialog](msirmfilesinuse-dialog.md) in response to this message.</span></span> <span data-ttu-id="44275-141">Verfügbar ab Windows Installer Version 4,0.</span><span class="sxs-lookup"><span data-stu-id="44275-141">Available beginning with Windows Installer version 4.0.</span></span> <span data-ttu-id="44275-142">Weitere Informationen zu dieser Meldung finden [Sie unter Verwenden des Neustart-Managers mit einer externen Benutzeroberfläche](using-restart-manager-with-an-external-ui-.md).</span><span class="sxs-lookup"><span data-stu-id="44275-142">For more information about this message see [Using Restart Manager with an External UI](using-restart-manager-with-an-external-ui-.md).</span></span>

</dd> <dt>

<span data-ttu-id="44275-143"><span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**installmessage- \_ Aktions Start**</span><span class="sxs-lookup"><span data-stu-id="44275-143"><span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**INSTALLMESSAGE\_ACTIONSTART**</span></span>
</dt> <dd>

<span data-ttu-id="44275-144">Diese Meldung enthält Informationen über die aktuelle Aktion.</span><span class="sxs-lookup"><span data-stu-id="44275-144">This message gives information about the current action.</span></span> <span data-ttu-id="44275-145">Das Format ist Aktion \[ 1 \] : \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="44275-145">The format is Action \[1\]: \[2\].</span></span> <span data-ttu-id="44275-146">\[3 \] , wobei ein Doppelpunkt verwendet wird, um Feld 1 und Feld 2 zu trennen, und ein Punkt zum Trennen von Feld 2 und Feld 3 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44275-146">\[3\], where a colon is used to separate Field 1 and Field 2 and a period is used to separate Field 2 and Field 3.</span></span> <span data-ttu-id="44275-147">Feld \[ 1 \] enthält den Zeitpunkt, zu dem die Aktion mit dem [**Zeit**](time.md) Eigenschaften Format gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="44275-147">Field \[1\] contains the time the action was started using the [**Time**](time.md) property format.</span></span> <span data-ttu-id="44275-148">Feld \[ 2 \] enthält den Namen der Aktion aus der Sequenz Tabelle.</span><span class="sxs-lookup"><span data-stu-id="44275-148">Field \[2\] contains the action's name from the sequence table.</span></span> <span data-ttu-id="44275-149">Field \[ 3 \] gibt die Beschreibung der Aktion aus der [Action Text-Tabelle](actiontext-table.md) oder aus der [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="44275-149">Field \[3\] gives the action's description from the [ActionText table](actiontext-table.md) or from the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span>

</dd> <dt>

<span data-ttu-id="44275-150"><span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**installmessage- \_ Aktions Daten**</span><span class="sxs-lookup"><span data-stu-id="44275-150"><span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**INSTALLMESSAGE\_ACTIONDATA**</span></span>
</dt> <dd>

<span data-ttu-id="44275-151">Das Format dieser Zeichenfolge wird durch den [Vorlagen](template.md) Wert angegeben, der in der [Tabelle "aktiontext](actiontext-table.md) " oder der Funktion " [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) " bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="44275-151">The format of this string is specified by the [Template](template.md) value provided in the [ActionText table](actiontext-table.md) or by the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span> <span data-ttu-id="44275-152">Nach der Meldung " **installmessage- \_ Aktions Start** " kann eine unbegrenzte Anzahl von **installmessage- \_ Aktions Daten** Nachrichten vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="44275-152">There can be an unlimited number of **INSTALLMESSAGE\_ACTIONDATA** messages after the **INSTALLMESSAGE\_ACTIONSTART** message.</span></span>

</dd> <dt>

<span data-ttu-id="44275-153"><span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**installmessage \_ commondata**</span><span class="sxs-lookup"><span data-stu-id="44275-153"><span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**INSTALLMESSAGE\_COMMONDATA**</span></span>
</dt> <dd>

<span data-ttu-id="44275-154">Diese Meldung enthält drei Untertypen: Sprache, Beschriftung und cancelshow.</span><span class="sxs-lookup"><span data-stu-id="44275-154">This message has three subtypes: Language, Caption, and CancelShow.</span></span> <span data-ttu-id="44275-155">Die Zeichenfolge kann drei Felder enthalten, die durch eine Zahl gefolgt von einem Doppelpunkt getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="44275-155">The string can have three fields delimited by a number followed by a colon.</span></span> <span data-ttu-id="44275-156">Es sind nicht alle Felder erforderlich.</span><span class="sxs-lookup"><span data-stu-id="44275-156">Not all fields are required.</span></span> <span data-ttu-id="44275-157">Die Nachricht kann eine NULL-oder leere Zeichenfolge ("") sein.</span><span class="sxs-lookup"><span data-stu-id="44275-157">The message can be a NULL or empty ("") string.</span></span>

<dl> <dt>

<span data-ttu-id="44275-158"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Kurse</span><span class="sxs-lookup"><span data-stu-id="44275-158"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="44275-159">Feld 1 enthält den Wert 0, um anzugeben, dass diese Zeichenfolge Sprachinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="44275-159">Field 1 contains the value 0 to indicate this string contains language information.</span></span> <span data-ttu-id="44275-160">Feld 2 enthält einen [sprach](language.md) Wert, bei dem es sich um einen numerischen sprach Bezeichner (langid) handelt. Field 3 ist ein Wert, der eine ANSI-Codepage darstellt.</span><span class="sxs-lookup"><span data-stu-id="44275-160">Field 2 contains a [Language](language.md) value that is a numeric language identifier (LANGID.) Field 3 is a value that represents an ANSI code page.</span></span>

</dd> <dt>

<span data-ttu-id="44275-161"><span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>Unter</span><span class="sxs-lookup"><span data-stu-id="44275-161"><span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>Caption</span></span>
</dt> <dd>

<span data-ttu-id="44275-162">Feld 1 enthält den Wert 1, um anzugeben, dass diese Zeichenfolge den Text einer Beschriftung oder eines Titels enthält.</span><span class="sxs-lookup"><span data-stu-id="44275-162">Field 1 contains the value 1 to indicate this string contains the text of a caption or title.</span></span> <span data-ttu-id="44275-163">Feld 2 enthält Text, der von einem externen Benutzeroberflächen Handler als Titel Titel für ein Dialogfeld verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="44275-163">Field 2 contains text that an external UI handler can use as a caption of title for a dialog box.</span></span> <span data-ttu-id="44275-164">Field 3 ist NULL oder eine leere Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="44275-164">Field 3 is NULL or an empty ("") string.</span></span> <span data-ttu-id="44275-165">Feld 3 kann nicht in der Beschriftungs Nachricht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="44275-165">Field 3 can be absent from a the Caption message.</span></span>

</dd> <dt>

<span data-ttu-id="44275-166"><span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>Abbrechen</span><span class="sxs-lookup"><span data-stu-id="44275-166"><span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow</span></span>
</dt> <dd>

<span data-ttu-id="44275-167">Feld 1 enthält den Wert 2, um anzugeben, dass diese Zeichenfolge Informationen darüber enthält, ob die Schaltfläche Abbrechen angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="44275-167">Field 1 contains the value 2 to indicate this string contains information about whether to display the cancel button.</span></span> <span data-ttu-id="44275-168">Wenn die Schaltfläche Abbrechen ausgeblendet werden soll, enthält Feld 2 den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="44275-168">If the cancel button should be hidden, Field 2 contains the value 0.</span></span> <span data-ttu-id="44275-169">Wenn die Schaltfläche Abbrechen sichtbar sein soll, enthält Feld 2 den Wert 1.</span><span class="sxs-lookup"><span data-stu-id="44275-169">If the cancel button should be visible, Field 2 contains the value 1.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="44275-170"><span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>installmessage \_ -Status</span><span class="sxs-lookup"><span data-stu-id="44275-170"><span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>INSTALLMESSAGE\_PROGRESS</span></span>
</dt> <dd>

<span data-ttu-id="44275-171">Diese Nachricht hat vier Untertypen: Reset, AktionInfo, progressreport und progressaddition.</span><span class="sxs-lookup"><span data-stu-id="44275-171">This message has four subtypes: Reset, ActionInfo, ProgressReport, and ProgressAddition.</span></span> <span data-ttu-id="44275-172">Der externe Handler sollte erst dann auf eine dieser Nachrichten reagieren, wenn die erste Statusmeldung zum Zurücksetzen empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="44275-172">The external handler should not act upon any of these messages until the first a Reset progress message is received.</span></span> <span data-ttu-id="44275-173">Dadurch wird eine Schätzung der Gesamtzahl der Ticks für die Statusanzeige bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="44275-173">This provides an estimate of the total number of ticks for the progress bar.</span></span>

<dl> <dt>

<span data-ttu-id="44275-174"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Festlegen</span><span class="sxs-lookup"><span data-stu-id="44275-174"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Reset</span></span>
</dt> <dd>

<span data-ttu-id="44275-175">Feld 1 enthält den Wert 0, um das Zurücksetzen der Statusanzeige anzugeben.</span><span class="sxs-lookup"><span data-stu-id="44275-175">Field 1 contains the value 0 to indicate a reset of the progress bar.</span></span> <span data-ttu-id="44275-176">Feld 2 enthält die Gesamtanzahl der Ticks in der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="44275-176">Field 2 contains the total number of ticks in the progress bar.</span></span> <span data-ttu-id="44275-177">Field 3 enthält den Wert 0 für die Bewegung der vorwärts Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="44275-177">Field 3 contains the value 0 for forward progress bar motion.</span></span> <span data-ttu-id="44275-178">Field 3 enthält den Wert 1 für die Bewegung der rückwärts Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="44275-178">Field 3 contains the value 1 for backward progress bar motion.</span></span> <span data-ttu-id="44275-179">Der Wert 0 in Feld 4 bedeutet, dass die Installation ausgeführt wird und die verbleibende Zeit berechnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="44275-179">The value 0 in Field 4 means the installation is in progress and the time remaining may be calculated.</span></span> <span data-ttu-id="44275-180">Der Wert 1 in Feld 4 bedeutet, dass das Skript ausgeführt wird und ein "Bitte warten..." die Meldung kann angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="44275-180">The value 1 in Field 4 means script is being run and a "Please wait ..." message can be displayed.</span></span> <span data-ttu-id="44275-181">Der Schätzwert für die Gesamtzahl der Ticks ist eine Näherung und möglicherweise ungenau.</span><span class="sxs-lookup"><span data-stu-id="44275-181">The estimate of the total number of ticks is an approximation and may be inaccurate.</span></span>

</dd> <dt>

<span data-ttu-id="44275-182"><span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>Action Info</span><span class="sxs-lookup"><span data-stu-id="44275-182"><span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo</span></span>
</dt> <dd>

<span data-ttu-id="44275-183">Feld 1 enthält den Wert 1, um anzugeben, dass diese Zeichenfolge Aktions Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="44275-183">Field 1 contains the value 1 to indicate this string contains action information.</span></span> <span data-ttu-id="44275-184">Feld 2 enthält die Anzahl der Ticks, die die Statusanzeige für jede von der aktuellen Aktion gesendete Action Data-Nachricht verschiebt.</span><span class="sxs-lookup"><span data-stu-id="44275-184">Field 2 contains the number of ticks the progress bar moves for each ActionData message sent by the current action.</span></span> <span data-ttu-id="44275-185">Wenn Feld 3 den Wert 0 (null) enthält, ignorieren Sie Feld 2.</span><span class="sxs-lookup"><span data-stu-id="44275-185">If Field 3 contains the value 0, ignore Field 2.</span></span> <span data-ttu-id="44275-186">Wenn Feld 3 den Wert 1 enthält, erhöhen Sie die Statusanzeige um die Anzahl der Ticks in Feld 2 für jede von der aktuellen Aktion gesendete Aktion "action Data".</span><span class="sxs-lookup"><span data-stu-id="44275-186">If Field 3 contains the value 1, increment the progress bar by the number of ticks in Field 2 for each ActionData message sent by the current action.</span></span> <span data-ttu-id="44275-187">Field 4 wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="44275-187">Field 4 is unused.</span></span>

</dd> <dt>

<span data-ttu-id="44275-188"><span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>Progressreport</span><span class="sxs-lookup"><span data-stu-id="44275-188"><span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport</span></span>
</dt> <dd>

<span data-ttu-id="44275-189">Feld 1 enthält den Wert 2, um anzugeben, dass diese Zeichenfolge Statusinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="44275-189">Field 1 contains the value 2 to indicate this string contains progress information.</span></span> <span data-ttu-id="44275-190">Feld 2 enthält die Anzahl der Ticks, die die Statusanzeige verschoben hat.</span><span class="sxs-lookup"><span data-stu-id="44275-190">Field 2 contains the number of ticks the progress bar has moved.</span></span> <span data-ttu-id="44275-191">Feld 3 wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="44275-191">Field 3 is unused.</span></span> <span data-ttu-id="44275-192">Field 4 wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="44275-192">Field 4 is unused.</span></span>

</dd> <dt>

<span data-ttu-id="44275-193"><span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>Progressaddition</span><span class="sxs-lookup"><span data-stu-id="44275-193"><span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition</span></span>
</dt> <dd>

<span data-ttu-id="44275-194">Feld 1 enthält den Wert 3, um anzugeben, dass eine Aktion Ticks die Statusanzeige hinzufügen kann.</span><span class="sxs-lookup"><span data-stu-id="44275-194">Field 1 contains the value 3 to indicate that an action can add ticks the progress bar.</span></span> <span data-ttu-id="44275-195">Feld 2 enthält die Anzahl der Ticks, die der Gesamtanzahl der erwarteten Anzahl von Status Ticks hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="44275-195">Field 2 contains the number of ticks to add to total expected count of progress ticks.</span></span> <span data-ttu-id="44275-196">Feld 3 wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="44275-196">Field 3 is unused.</span></span> <span data-ttu-id="44275-197">Field 4 wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="44275-197">Field 4 is unused.</span></span>

</dd> </dl> </dd> </dl>

 

 



