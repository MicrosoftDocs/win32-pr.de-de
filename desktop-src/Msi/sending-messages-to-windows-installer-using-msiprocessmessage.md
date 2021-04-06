---
description: Bei den mithilfe von "msiprocessmessage" gesendeten Nachrichten handelt es sich um dieselben Nachrichten, die von der installui- \_ handlerrückruf-Funktion empfangen werden, wenn msisettexternalui
ms.assetid: ca73bd0a-6f4e-453c-9e38-14cfd602d42c
title: Senden von Nachrichten an Windows Installer mithilfe von "msiprocessmessage"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd8c8a704c1f4dd24763f7f47ff0d8898a95c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960825"
---
# <a name="sending-messages-to-windows-installer-using-msiprocessmessage"></a><span data-ttu-id="19754-103">Senden von Nachrichten an Windows Installer mithilfe von "msiprocessmessage"</span><span class="sxs-lookup"><span data-stu-id="19754-103">Sending Messages to Windows Installer Using MsiProcessMessage</span></span>

<span data-ttu-id="19754-104">Bei den mithilfe von " [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) " gesendeten Nachrichten handelt es sich um dieselben Nachrichten, die von der [**installui- \_ handlerrückruf**](/windows/desktop/api/Msi/nc-msi-installui_handlera) -Funktion empfangen werden, wenn [**msisettexternalui**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)</span><span class="sxs-lookup"><span data-stu-id="19754-104">The messages sent using [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) are the same messages that are received by the [**INSTALLUI\_HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera) callback function if [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) was called.</span></span> <span data-ttu-id="19754-105">Andernfalls verarbeitet Windows Installer die Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="19754-105">Otherwise, Windows Installer handles the messages.</span></span> <span data-ttu-id="19754-106">Weitere Informationen finden Sie unter [Windows Installer-Nachrichten](parsing-windows-installer-messages.md).</span><span class="sxs-lookup"><span data-stu-id="19754-106">For details, see [Parsing Windows Installer Messages](parsing-windows-installer-messages.md).</span></span>

<span data-ttu-id="19754-107">Um z. b. eine installmessage \_ -Fehlermeldung mit dem \_ Symbol "MB iconwarning" und den Schaltflächen "MB \_ abortretrycancel" zu senden:</span><span class="sxs-lookup"><span data-stu-id="19754-107">For example, to send an INSTALLMESSAGE\_ERROR message with the MB\_ICONWARNING icon and the MB\_ABORTRETRYCANCEL buttons:</span></span>


```C++
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING), hRec);
```



<span data-ttu-id="19754-108">Dabei *ist hinstall* das Handle für die Installation, das für eine benutzerdefinierte Aktion oder das *hproduct* -Handle von [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) oder [**msiopenpackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)bereitgestellt wird, und *hrec* ist der Datensatz, der die zu formatierenden Fehlerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="19754-108">Where *hInstall* is the handle to the installation, provided to a custom action or the *hProduct* handle from [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) or [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea), and *hRec* is the record containing the error information to format.</span></span> <span data-ttu-id="19754-109">Weitere Informationen zur Formatierung finden Sie unter [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).</span><span class="sxs-lookup"><span data-stu-id="19754-109">For information on how formatting is performed, see [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).</span></span>

<span data-ttu-id="19754-110">Wenn ein installmessage- \_ Fehler oder eine installmessage-Nachricht " \_ fatalexit" gesendet wird, ohne den Schalt Flächentyp oder die Symboltypen anzugeben, werden standardmäßig MB \_ OK, kein Symbol und MB \_ DEFBUTTON1 verwendet.</span><span class="sxs-lookup"><span data-stu-id="19754-110">By default, if an INSTALLMESSAGE\_ERROR or INSTALLMESSAGE\_FATALEXIT message is sent without specifying button type or icon types, MB\_OK, no icon, and MB\_DEFBUTTON1 are used.</span></span>

<span data-ttu-id="19754-111">Windows Installer die Schaltfläche **Abbrechen** nicht mit der Zeichenfolge "Abort" beschriftet, wenn eine MessageBox mit der Schaltflächen Spezifikation "MB \_ AbortRetryIgnore" angezeigt wird, wird die Schaltfläche mit der Zeichenfolge "Cancel" beschriftet.</span><span class="sxs-lookup"><span data-stu-id="19754-111">Windows Installer does not label the **ABORT** button with the "Abort" string when displaying a MessageBox with the MB\_ABORTRETRYIGNORE button specification, instead it labels the button with the "Cancel" string.</span></span> <span data-ttu-id="19754-112">Bei allen Fehlermeldungen wird das Wort "Abort" nicht verwendet, sondern stattdessen das Wort "Cancel" verwendet.</span><span class="sxs-lookup"><span data-stu-id="19754-112">All error messages refrain from using the word "Abort" and instead use the word "Cancel".</span></span>

<span data-ttu-id="19754-113">Der *hrecord* -Parameter der [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) -Funktion hängt von dem Nachrichtentyp ab, der an die [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="19754-113">The *hRecord* parameter of the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function depends upon the message type sent to the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span></span> <span data-ttu-id="19754-114">In der folgenden Liste sind die Anforderungen des Datensatzes in Bezug auf den Nachrichtentyp aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="19754-114">The following list details the requirements of the record in relation to the message type:</span></span>

<span data-ttu-id="19754-115">installmessage \_ fatalexit</span><span class="sxs-lookup"><span data-stu-id="19754-115">INSTALLMESSAGE\_FATALEXIT</span></span>

 

<span data-ttu-id="19754-116">installmessage- \_ Info</span><span class="sxs-lookup"><span data-stu-id="19754-116">INSTALLMESSAGE\_INFO</span></span>

 

<span data-ttu-id="19754-117">installmessage \_ oudeatdiskspace</span><span class="sxs-lookup"><span data-stu-id="19754-117">INSTALLMESSAGE\_OUTOFDISKSPACE</span></span>



| <span data-ttu-id="19754-118">Feld</span><span class="sxs-lookup"><span data-stu-id="19754-118">Field</span></span>         | <span data-ttu-id="19754-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19754-119">Description</span></span>                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19754-120">0</span><span class="sxs-lookup"><span data-stu-id="19754-120">0</span></span>             | <span data-ttu-id="19754-121">Vorlage für die Formatierung der resultierenden Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="19754-121">Template for the formatting of the resultant string.</span></span> <span data-ttu-id="19754-122">Weitere Informationen finden Sie unter [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) .</span><span class="sxs-lookup"><span data-stu-id="19754-122">See [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) for more information.</span></span> <span data-ttu-id="19754-123">Auf die Felder des Datensatzes wird mithilfe \[ \] von 1 für Feld 1, \[ 2 \] für Feld 2 usw. verwiesen.</span><span class="sxs-lookup"><span data-stu-id="19754-123">The fields of the record are referenced using \[1\] for field 1, \[2\] for field 2, etc.</span></span> |
| <span data-ttu-id="19754-124">1 bis *n*</span><span class="sxs-lookup"><span data-stu-id="19754-124">1 through *n*</span></span> | <span data-ttu-id="19754-125">Alle nachfolgenden Felder sind direkt mit den Feldern verknüpft, auf die die Vorlage in Feld 0 verweist.</span><span class="sxs-lookup"><span data-stu-id="19754-125">All subsequent fields are directly related to the fields referenced by the template in field 0.</span></span>                                                                                                                    |



 

<span data-ttu-id="19754-126">Wenn Field 0 den Wert NULL aufweist, wird die vom UI-Handler empfangene Zeichenfolge wie folgt formatiert: 1: \[ Daten aus Feld 1 \] 2: \[ Daten aus Feld 2 \] . Dies bedeutet, dass die Zeichenfolge die Feldnummer und die im Feld gespeicherten Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="19754-126">If field 0 is null, the string received by the UI handler is formatted as: 1: \[data from field 1\] 2: \[data from field 2\] meaning that for each field of the record, the string contains the field number followed by the data stored in the field.</span></span>

<span data-ttu-id="19754-127">Informationsmeldungen von [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) werden protokolliert, wenn [**msienablelog**](/windows/desktop/api/Msi/nf-msi-msienableloga), die [Befehlszeilenoption](command-line-options.md)"/l" oder die [Protokollierungs Richtlinie](logging.md) die Informationen "I" oder "installlogmode" angeben \_ .</span><span class="sxs-lookup"><span data-stu-id="19754-127">Information messages from [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) are logged when [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), the '/l' [command line option](command-line-options.md), or the [logging policy](logging.md) specify 'I' or INSTALLLOGMODE\_INFO.</span></span>

<span data-ttu-id="19754-128">installmessage- \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="19754-128">INSTALLMESSAGE\_ERROR</span></span>

 

<span data-ttu-id="19754-129">installmessage- \_ Warnung</span><span class="sxs-lookup"><span data-stu-id="19754-129">INSTALLMESSAGE\_WARNING</span></span>

 

<span data-ttu-id="19754-130">installmessage- \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="19754-130">INSTALLMESSAGE\_USER</span></span>

<span data-ttu-id="19754-131">, Wenn eine Meldung aus der Fehler Tabelle verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="19754-131">To use a message from the Error table.</span></span>



| <span data-ttu-id="19754-132">Feld</span><span class="sxs-lookup"><span data-stu-id="19754-132">Field</span></span>         | <span data-ttu-id="19754-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19754-133">Description</span></span>                                           |
|---------------|-------------------------------------------------------|
| <span data-ttu-id="19754-134">0</span><span class="sxs-lookup"><span data-stu-id="19754-134">0</span></span>             | <span data-ttu-id="19754-135">Muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="19754-135">Must be null.</span></span>                                         |
| <span data-ttu-id="19754-136">1</span><span class="sxs-lookup"><span data-stu-id="19754-136">1</span></span>             | <span data-ttu-id="19754-137">Die Nachrichtennummer in der [Fehler Tabelle](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="19754-137">Message number in the [Error table](error-table.md).</span></span> |
| <span data-ttu-id="19754-138">2 bis *n*</span><span class="sxs-lookup"><span data-stu-id="19754-138">2 through *n*</span></span> | <span data-ttu-id="19754-139">Bezieht sich auf die angegebene Meldung in der Fehler Tabelle.</span><span class="sxs-lookup"><span data-stu-id="19754-139">Related to the specified message in the Error table.</span></span>  |



 

<span data-ttu-id="19754-140">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="19754-140">For example.</span></span>



| <span data-ttu-id="19754-141">Feld</span><span class="sxs-lookup"><span data-stu-id="19754-141">Field</span></span> | <span data-ttu-id="19754-142">Typ</span><span class="sxs-lookup"><span data-stu-id="19754-142">Type</span></span>   | <span data-ttu-id="19754-143">Daten</span><span class="sxs-lookup"><span data-stu-id="19754-143">Data</span></span>       |
|-------|--------|------------|
| <span data-ttu-id="19754-144">0</span><span class="sxs-lookup"><span data-stu-id="19754-144">0</span></span>     | <span data-ttu-id="19754-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="19754-145">string</span></span> | <span data-ttu-id="19754-146">NULL</span><span class="sxs-lookup"><span data-stu-id="19754-146">null</span></span>       |
| <span data-ttu-id="19754-147">1</span><span class="sxs-lookup"><span data-stu-id="19754-147">1</span></span>     | <span data-ttu-id="19754-148">INT</span><span class="sxs-lookup"><span data-stu-id="19754-148">int</span></span>    | <span data-ttu-id="19754-149">1304</span><span class="sxs-lookup"><span data-stu-id="19754-149">1304</span></span>       |
| <span data-ttu-id="19754-150">2</span><span class="sxs-lookup"><span data-stu-id="19754-150">2</span></span>     | <span data-ttu-id="19754-151">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="19754-151">string</span></span> | <span data-ttu-id="19754-152">Myfile.txt</span><span class="sxs-lookup"><span data-stu-id="19754-152">Myfile.txt</span></span> |



 

<span data-ttu-id="19754-153">Die resultierende Nachricht, die vom Benutzeroberflächen Handler empfangen wurde, lautet:</span><span class="sxs-lookup"><span data-stu-id="19754-153">The resulting message received from the UI handler is:</span></span>

<span data-ttu-id="19754-154">Fehler 1304.</span><span class="sxs-lookup"><span data-stu-id="19754-154">Error 1304.</span></span> <span data-ttu-id="19754-155">Fehler beim Schreiben in die Datei: Myfile.txt.</span><span class="sxs-lookup"><span data-stu-id="19754-155">Error writing to file: Myfile.txt.</span></span> <span data-ttu-id="19754-156">Vergewissern Sie sich, dass Sie Zugriff auf dieses Verzeichnis haben.</span><span class="sxs-lookup"><span data-stu-id="19754-156">Verify that you have access to that directory.</span></span>

<span data-ttu-id="19754-157">Wenn Field 0 nicht NULL ist, wird die Meldung aus der Fehler Tabelle überschrieben.</span><span class="sxs-lookup"><span data-stu-id="19754-157">If field 0 is not null, the message from the error table is overridden.</span></span> <span data-ttu-id="19754-158">Stattdessen bestimmt die Vorlage Field 0 das Format der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="19754-158">Instead, the field 0 template determines the format of the message.</span></span>

<span data-ttu-id="19754-159">In der Meldung können auch die Schaltflächen, einschließlich der Standard Schaltfläche, und das Symbol für die Verwendung mit der Meldung wie oben beschrieben angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="19754-159">The message may also specify the buttons, including the default button, and the icon for use with the message as mentioned above.</span></span> <span data-ttu-id="19754-160">Die Schaltflächen-und Symboltypen werden im [**installlui- \_ Handler**](/windows/desktop/api/Msi/nc-msi-installui_handlera)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="19754-160">The button and icon types are listed in [**INSTALLUI\_HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera).</span></span>

<span data-ttu-id="19754-161">installmessage \_ commondata</span><span class="sxs-lookup"><span data-stu-id="19754-161">INSTALLMESSAGE\_COMMONDATA</span></span>

<span data-ttu-id="19754-162">Diese Meldung wird gesendet, um die Schaltfläche **Abbrechen** in einem Status Dialogfeld zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="19754-162">This message is sent to enable or disable the **Cancel** button in a progress dialog box.</span></span>



| <span data-ttu-id="19754-163">Feld</span><span class="sxs-lookup"><span data-stu-id="19754-163">Field</span></span> | <span data-ttu-id="19754-164">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19754-164">Description</span></span>                                                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19754-165">0</span><span class="sxs-lookup"><span data-stu-id="19754-165">0</span></span>     | <span data-ttu-id="19754-166">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="19754-166">Unused.</span></span>                                                                                                                                      |
| <span data-ttu-id="19754-167">1</span><span class="sxs-lookup"><span data-stu-id="19754-167">1</span></span>     | <span data-ttu-id="19754-168">2 verweist auf die Schaltfläche " **Abbrechen** ".</span><span class="sxs-lookup"><span data-stu-id="19754-168">2 refers to the **Cancel** button.</span></span>                                                                                                           |
| <span data-ttu-id="19754-169">2</span><span class="sxs-lookup"><span data-stu-id="19754-169">2</span></span>     | <span data-ttu-id="19754-170">Der Wert 1 gibt an, dass die Schaltfläche **Abbrechen** sichtbar sein soll.</span><span class="sxs-lookup"><span data-stu-id="19754-170">A value of 1 indicates the **Cancel** button should be visible.</span></span> <span data-ttu-id="19754-171">Der Wert 0 gibt an, dass die Schaltfläche **Abbrechen** unsichtbar sein sollte.</span><span class="sxs-lookup"><span data-stu-id="19754-171">A value of 0 indicates the **Cancel** button should be invisible.</span></span><br/> |



 

<span data-ttu-id="19754-172">Zum Deaktivieren oder Ausblenden der Schaltfläche **Abbrechen** würde der Datensatz z. b. wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="19754-172">For example, to disable or hide the **Cancel** button, the record would appear as follows.</span></span>



| <span data-ttu-id="19754-173">Feld</span><span class="sxs-lookup"><span data-stu-id="19754-173">Field</span></span> | <span data-ttu-id="19754-174">Typ</span><span class="sxs-lookup"><span data-stu-id="19754-174">Type</span></span>   | <span data-ttu-id="19754-175">Daten</span><span class="sxs-lookup"><span data-stu-id="19754-175">Data</span></span> |
|-------|--------|------|
| <span data-ttu-id="19754-176">0</span><span class="sxs-lookup"><span data-stu-id="19754-176">0</span></span>     | <span data-ttu-id="19754-177">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="19754-177">string</span></span> | <span data-ttu-id="19754-178">NULL</span><span class="sxs-lookup"><span data-stu-id="19754-178">null</span></span> |
| <span data-ttu-id="19754-179">1</span><span class="sxs-lookup"><span data-stu-id="19754-179">1</span></span>     | <span data-ttu-id="19754-180">INT</span><span class="sxs-lookup"><span data-stu-id="19754-180">int</span></span>    | <span data-ttu-id="19754-181">2</span><span class="sxs-lookup"><span data-stu-id="19754-181">2</span></span>    |
| <span data-ttu-id="19754-182">2</span><span class="sxs-lookup"><span data-stu-id="19754-182">2</span></span>     | <span data-ttu-id="19754-183">INT</span><span class="sxs-lookup"><span data-stu-id="19754-183">int</span></span>    | <span data-ttu-id="19754-184">0</span><span class="sxs-lookup"><span data-stu-id="19754-184">0</span></span>    |



 

<span data-ttu-id="19754-185">installmessage- \_ Aktions Start</span><span class="sxs-lookup"><span data-stu-id="19754-185">INSTALLMESSAGE\_ACTIONSTART</span></span>

 

<span data-ttu-id="19754-186">installmessage- \_ Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="19754-186">INSTALLMESSAGE\_ACTIONDATA</span></span>

<span data-ttu-id="19754-187">Der installmessage- \_ Aktions Daten Satz bestimmt das Format des Aktions Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="19754-187">The INSTALLMESSAGE\_ACTIONSTART record determines the format of the ActionData record.</span></span>



| <span data-ttu-id="19754-188">Feld</span><span class="sxs-lookup"><span data-stu-id="19754-188">Field</span></span> | <span data-ttu-id="19754-189">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19754-189">Description</span></span>                                                                                                   |
|-------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19754-190">0</span><span class="sxs-lookup"><span data-stu-id="19754-190">0</span></span>     | <span data-ttu-id="19754-191">NULL</span><span class="sxs-lookup"><span data-stu-id="19754-191">null</span></span>                                                                                                          |
| <span data-ttu-id="19754-192">1</span><span class="sxs-lookup"><span data-stu-id="19754-192">1</span></span>     | <span data-ttu-id="19754-193">Der Aktionsname.</span><span class="sxs-lookup"><span data-stu-id="19754-193">Action name.</span></span> <span data-ttu-id="19754-194">Der Name in diesem Feld darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="19754-194">The name in this field must be non-null.</span></span>                                                         |
| <span data-ttu-id="19754-195">2</span><span class="sxs-lookup"><span data-stu-id="19754-195">2</span></span>     | <span data-ttu-id="19754-196">Aktions Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="19754-196">Action description.</span></span>                                                                                           |
| <span data-ttu-id="19754-197">3</span><span class="sxs-lookup"><span data-stu-id="19754-197">3</span></span>     | <span data-ttu-id="19754-198">Aktions Vorlage.</span><span class="sxs-lookup"><span data-stu-id="19754-198">Action template.</span></span> <span data-ttu-id="19754-199">Diese wird für die Aktions Daten verwendet, deren Nachricht entsprechend dieser Vorlage formatiert wird.</span><span class="sxs-lookup"><span data-stu-id="19754-199">This is used for the ActionData whose message is being formatted according to this template.</span></span> |



 

<span data-ttu-id="19754-200">Verweisen Sie in der Aktions Vorlagen Nachricht nicht auf Feld 0.</span><span class="sxs-lookup"><span data-stu-id="19754-200">Do not reference field 0 in the Action template message.</span></span>

<span data-ttu-id="19754-201">Der "installmessage"- \_ Aktions Daten Satz ist wie folgt formatiert.</span><span class="sxs-lookup"><span data-stu-id="19754-201">The INSTALLMESSAGE\_ACTIONDATA record is formatted as follows.</span></span>



| <span data-ttu-id="19754-202">Feld</span><span class="sxs-lookup"><span data-stu-id="19754-202">Field</span></span>         | <span data-ttu-id="19754-203">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19754-203">Description</span></span>                                                                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19754-204">0</span><span class="sxs-lookup"><span data-stu-id="19754-204">0</span></span>             | <span data-ttu-id="19754-205">NULL</span><span class="sxs-lookup"><span data-stu-id="19754-205">null</span></span>                                                                                                                                               |
| <span data-ttu-id="19754-206">1 bis *n*</span><span class="sxs-lookup"><span data-stu-id="19754-206">1 through *n*</span></span> | <span data-ttu-id="19754-207">Abhängig von Feld 3 der entsprechenden installmessage- \_ Aktions Meldung oder-Vorlage, die in der [Tabelle "aktiontext](actiontext-table.md)" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="19754-207">Dependent upon field 3 of the corresponding INSTALLMESSAGE\_ACTIONSTART message or template specified in [ActionText table](actiontext-table.md).</span></span> |



 

<span data-ttu-id="19754-208">Beispielsweise der "installmessage"- \_ Aktions Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="19754-208">For example, the INSTALLMESSAGE\_ACTIONSTART record.</span></span>



| <span data-ttu-id="19754-209">Feld</span><span class="sxs-lookup"><span data-stu-id="19754-209">Field</span></span> | <span data-ttu-id="19754-210">Typ</span><span class="sxs-lookup"><span data-stu-id="19754-210">Type</span></span>   | <span data-ttu-id="19754-211">Daten</span><span class="sxs-lookup"><span data-stu-id="19754-211">Data</span></span>                                                            |
|-------|--------|-----------------------------------------------------------------|
| <span data-ttu-id="19754-212">0</span><span class="sxs-lookup"><span data-stu-id="19754-212">0</span></span>     | <span data-ttu-id="19754-213">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="19754-213">string</span></span> | <span data-ttu-id="19754-214">NULL</span><span class="sxs-lookup"><span data-stu-id="19754-214">null</span></span>                                                            |
| <span data-ttu-id="19754-215">1</span><span class="sxs-lookup"><span data-stu-id="19754-215">1</span></span>     | <span data-ttu-id="19754-216">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="19754-216">string</span></span> | <span data-ttu-id="19754-217">Myaction</span><span class="sxs-lookup"><span data-stu-id="19754-217">MyAction</span></span>                                                        |
| <span data-ttu-id="19754-218">2</span><span class="sxs-lookup"><span data-stu-id="19754-218">2</span></span>     | <span data-ttu-id="19754-219">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="19754-219">string</span></span> | <span data-ttu-id="19754-220">Dies ist die Beschreibung von "myaction".</span><span class="sxs-lookup"><span data-stu-id="19754-220">This is the description of "MyAction"</span></span>                           |
| <span data-ttu-id="19754-221">3</span><span class="sxs-lookup"><span data-stu-id="19754-221">3</span></span>     | <span data-ttu-id="19754-222">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="19754-222">string</span></span> | <span data-ttu-id="19754-223">Vorlage myaction: field1 Data ist \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="19754-223">MyAction template: field1 data is \[1\].</span></span> <span data-ttu-id="19754-224">die Daten des Felds 2 sind \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="19754-224">field 2 data is \[2\].</span></span> |



 

<span data-ttu-id="19754-225">Die Vorlage für installmessage- \_ Aktions Start (Field 3) verweist auf die Felder 1 und 2. der installmessage- \_ Aktions Daten Satz sollte 2 Felder mit den berechtigten Daten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="19754-225">The template for INSTALLMESSAGE\_ACTIONSTART (field 3) references fields 1 and 2, the INSTALLMESSAGE\_ACTIONDATA record should have 2 fields containing the warranted data.</span></span> <span data-ttu-id="19754-226">Die Felder können entweder Zeichen folgen-oder ganzzahlige Felder sein.</span><span class="sxs-lookup"><span data-stu-id="19754-226">The fields could be either string or integer fields.</span></span>

<span data-ttu-id="19754-227">Installmessage- \_ Aktions Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="19754-227">INSTALLMESSAGE\_ACTIONDATA record.</span></span>



| <span data-ttu-id="19754-228">Feld</span><span class="sxs-lookup"><span data-stu-id="19754-228">Field</span></span> | <span data-ttu-id="19754-229">Typ</span><span class="sxs-lookup"><span data-stu-id="19754-229">Type</span></span>   | <span data-ttu-id="19754-230">Daten</span><span class="sxs-lookup"><span data-stu-id="19754-230">Data</span></span>                    |
|-------|--------|-------------------------|
| <span data-ttu-id="19754-231">0</span><span class="sxs-lookup"><span data-stu-id="19754-231">0</span></span>     | <span data-ttu-id="19754-232">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="19754-232">string</span></span> | <span data-ttu-id="19754-233">NULL</span><span class="sxs-lookup"><span data-stu-id="19754-233">null</span></span>                    |
| <span data-ttu-id="19754-234">1</span><span class="sxs-lookup"><span data-stu-id="19754-234">1</span></span>     | <span data-ttu-id="19754-235">INT</span><span class="sxs-lookup"><span data-stu-id="19754-235">int</span></span>    | <span data-ttu-id="19754-236">2</span><span class="sxs-lookup"><span data-stu-id="19754-236">2</span></span>                       |
| <span data-ttu-id="19754-237">2</span><span class="sxs-lookup"><span data-stu-id="19754-237">2</span></span>     | <span data-ttu-id="19754-238">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="19754-238">string</span></span> | <span data-ttu-id="19754-239">Action Data für myaction</span><span class="sxs-lookup"><span data-stu-id="19754-239">ActionData for MyAction</span></span> |



 

<span data-ttu-id="19754-240">installmessage \_ FilesInUse</span><span class="sxs-lookup"><span data-stu-id="19754-240">INSTALLMESSAGE\_FILESINUSE</span></span>

<span data-ttu-id="19754-241">Der FilesInUse-Datensatz ist ein Datensatz variabler Länge.</span><span class="sxs-lookup"><span data-stu-id="19754-241">The FILESINUSE record is a variable length record.</span></span>



| <span data-ttu-id="19754-242">Feld</span><span class="sxs-lookup"><span data-stu-id="19754-242">Field</span></span> | <span data-ttu-id="19754-243">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19754-243">Description</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19754-244">0</span><span class="sxs-lookup"><span data-stu-id="19754-244">0</span></span>     | <span data-ttu-id="19754-245">Dieses Feld kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="19754-245">This field can be null.</span></span> <span data-ttu-id="19754-246">Für eine Installation mit einer einfachen Benutzeroberfläche kann in diesem Feld statischer Text für die Anzeige im [ListBox-Steuer](listbox-control.md) Element des [Dialog Felds FilesInUse](filesinuse-dialog.md)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="19754-246">For an installation using a basic UI, this field may specify static text for display in the [ListBox control](listbox-control.md) of the [FilesInUse dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="19754-247">Für eine Installation mit einer vollständigen Benutzeroberfläche hat dieses Feld keine Auswirkung, da der Text durch die Erstellung des benutzerdefinierten FilesInUse-Dialog Felds angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="19754-247">For an installation using a full UI, this field has no effect because the text is specified by the authoring of the custom FilesInUse dialog box.</span></span> |
| <span data-ttu-id="19754-248">1</span><span class="sxs-lookup"><span data-stu-id="19754-248">1</span></span>     | <span data-ttu-id="19754-249">Der Name der verwendeten Datei.</span><span class="sxs-lookup"><span data-stu-id="19754-249">Name of the file in use.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="19754-250">2</span><span class="sxs-lookup"><span data-stu-id="19754-250">2</span></span>     | <span data-ttu-id="19754-251">Dieses Feld identifiziert den Prozess, der die verwendete Datei enthält. **Windows Installer Version 4,0:** Die Prozess-ID (PID) des Prozesses oder der Titel des Fensters für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="19754-251">This field identifies the process holding the file in use.**Windows Installer version 4.0:** The process id (PID) of the process, or the title of the window for the process.</span></span><br/> <span data-ttu-id="19754-252">**Windows Installer Version 3,1 und früher:** Dieses Feld muss die Prozess-ID (PID) des Prozesses sein.</span><span class="sxs-lookup"><span data-stu-id="19754-252">**Windows Installer version 3.1 and earlier:** This field must be the process id (PID) of the process.</span></span><br/>                                                      |



 

<span data-ttu-id="19754-253">Um z. b. eine FilesInUse-Nachricht mit zwei verwendeten Dateien zu senden, red.exe und blue.exe, verfügt der Datensatz über vier Felder und das Feld 0.</span><span class="sxs-lookup"><span data-stu-id="19754-253">For example, to send a FilesInUse message showing two files in use, red.exe and blue.exe, the record has four fields plus the 0 field.</span></span> <span data-ttu-id="19754-254">Das Format des Datensatzes wäre wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="19754-254">The format of the record would be as shown in the following table.</span></span> <span data-ttu-id="19754-255">Für dieses Beispiel ist Windows Installer Version 4,0 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="19754-255">This example requires Windows Installer version 4.0.</span></span>

<span data-ttu-id="19754-256">**Windows Installer Version 3,1 und früher:** Die Felder 2 und 4 im folgenden Beispiel müssen die PIDs der Prozesse enthalten, in denen red.exe und blue.exe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19754-256">**Windows Installer version 3.1 and earlier:** Fields 2 and 4 in the following example must contain the PIDs of the processes holding red.exe and blue.exe in use.</span></span>



| <span data-ttu-id="19754-257">Feld</span><span class="sxs-lookup"><span data-stu-id="19754-257">Field</span></span> | <span data-ttu-id="19754-258">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19754-258">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="19754-259">0</span><span class="sxs-lookup"><span data-stu-id="19754-259">0</span></span>     | <span data-ttu-id="19754-260">NULL</span><span class="sxs-lookup"><span data-stu-id="19754-260">null</span></span>              |
| <span data-ttu-id="19754-261">1</span><span class="sxs-lookup"><span data-stu-id="19754-261">1</span></span>     | <span data-ttu-id="19754-262">Red.exe</span><span class="sxs-lookup"><span data-stu-id="19754-262">Red.exe</span></span>           |
| <span data-ttu-id="19754-263">2</span><span class="sxs-lookup"><span data-stu-id="19754-263">2</span></span>     | <span data-ttu-id="19754-264">Titel des roten Fensters</span><span class="sxs-lookup"><span data-stu-id="19754-264">Red Window Title</span></span>  |
| <span data-ttu-id="19754-265">3</span><span class="sxs-lookup"><span data-stu-id="19754-265">3</span></span>     | <span data-ttu-id="19754-266">Blue.exe</span><span class="sxs-lookup"><span data-stu-id="19754-266">Blue.exe</span></span>          |
| <span data-ttu-id="19754-267">4</span><span class="sxs-lookup"><span data-stu-id="19754-267">4</span></span>     | <span data-ttu-id="19754-268">Titel des blauen Fensters</span><span class="sxs-lookup"><span data-stu-id="19754-268">Blue Window Title</span></span> |



 

> [!Note]  
> <span data-ttu-id="19754-269">Wenn die von dem Dienst übergebenen PID in Windows Installer Version 4,0 keinen Fenstertitel aufweist, wie z. b. eine Task leisten Anwendung, wird die Datei nicht angezeigt, und das ausführliche Protokoll enthält die folgenden Meldungen.</span><span class="sxs-lookup"><span data-stu-id="19754-269">On Windows Installer version 4.0, if the PID passed from the service does not have a window title, such as a system tray application, the file is not be displayed and the verbose log contains the following messages.</span></span>

 

``` syntax
File In Use: -<FileName>- Window could not be found. Process ID: <PID>
No window with title could be found for FilesInUse
```

<span data-ttu-id="19754-270">installmessage \_ ResolveSource</span><span class="sxs-lookup"><span data-stu-id="19754-270">INSTALLMESSAGE\_RESOLVESOURCE</span></span>

<span data-ttu-id="19754-271">Der installmessage \_ ResolveSource-Datensatz enthält sieben Felder.</span><span class="sxs-lookup"><span data-stu-id="19754-271">The INSTALLMESSAGE\_RESOLVESOURCE record has seven fields.</span></span> <span data-ttu-id="19754-272">Damit installmessage \_ ResolveSource ordnungsgemäß funktioniert, wird die installmessage ResolveSource-Nachricht möglicherweise nicht von einem externen Benutzeroberflächen Handler verarbeitet \_ .</span><span class="sxs-lookup"><span data-stu-id="19754-272">For INSTALLMESSAGE\_RESOLVESOURCE to work correctly, an external UI handler may not handle the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="19754-273">Windows Installer müssen die installmessage \_ ResolveSource-Nachricht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="19754-273">Windows Installer must handle the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="19754-274">Das heißt, der externe UI-Handler gibt 0 zurück, um anzugeben, dass keine Aktion ausgeführt wird, wenn die installmessage \_ ResolveSource-Nachricht gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="19754-274">That is, the external UI handler returns 0 to indicate "no action taken" when filtering the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="19754-275">Es wird empfohlen, keine ResolveSource-Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="19754-275">The best practice is to avoid sending a RESOLVESOURCE message.</span></span>



| <span data-ttu-id="19754-276">Feld</span><span class="sxs-lookup"><span data-stu-id="19754-276">Field</span></span> | <span data-ttu-id="19754-277">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19754-277">Description</span></span>                                                                                                                                                        |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19754-278">0</span><span class="sxs-lookup"><span data-stu-id="19754-278">0</span></span>     | <span data-ttu-id="19754-279">NULL</span><span class="sxs-lookup"><span data-stu-id="19754-279">null</span></span>                                                                                                                                                               |
| <span data-ttu-id="19754-280">1</span><span class="sxs-lookup"><span data-stu-id="19754-280">1</span></span>     | <span data-ttu-id="19754-281">NULL</span><span class="sxs-lookup"><span data-stu-id="19754-281">null</span></span>                                                                                                                                                               |
| <span data-ttu-id="19754-282">2</span><span class="sxs-lookup"><span data-stu-id="19754-282">2</span></span>     | <span data-ttu-id="19754-283">Name des Pakets.</span><span class="sxs-lookup"><span data-stu-id="19754-283">Package name.</span></span>                                                                                                                                                      |
| <span data-ttu-id="19754-284">3</span><span class="sxs-lookup"><span data-stu-id="19754-284">3</span></span>     | <span data-ttu-id="19754-285">Produktcode.</span><span class="sxs-lookup"><span data-stu-id="19754-285">Product code.</span></span>                                                                                                                                                      |
| <span data-ttu-id="19754-286">4</span><span class="sxs-lookup"><span data-stu-id="19754-286">4</span></span>     | <span data-ttu-id="19754-287">Relativer Pfad, sofern bekannt, kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="19754-287">Relative path if known, can be null.</span></span>                                                                                                                               |
| <span data-ttu-id="19754-288">5</span><span class="sxs-lookup"><span data-stu-id="19754-288">5</span></span>     | <span data-ttu-id="19754-289">0</span><span class="sxs-lookup"><span data-stu-id="19754-289">0</span></span>                                                                                                                                                                  |
| <span data-ttu-id="19754-290">6</span><span class="sxs-lookup"><span data-stu-id="19754-290">6</span></span>     | <span data-ttu-id="19754-291">Gibt an, ob der Paketcode überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="19754-291">Whether to validate the package code.</span></span> <span data-ttu-id="19754-292">Der Wert "1" gibt an, dass der Paketcode überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="19754-292">A value of '1' indicates the package code should be validated.</span></span> <span data-ttu-id="19754-293">Der Wert ' 0 ' gibt an, dass das Paket nicht überprüft werden sollte.</span><span class="sxs-lookup"><span data-stu-id="19754-293">A value of '0' indicates the package should not be validated.</span></span> |
| <span data-ttu-id="19754-294">7</span><span class="sxs-lookup"><span data-stu-id="19754-294">7</span></span>     | <span data-ttu-id="19754-295">Erforderlicher Datenträger aus der Medien Tabelle.</span><span class="sxs-lookup"><span data-stu-id="19754-295">Required disk from media table.</span></span> <span data-ttu-id="19754-296">Der Wert ' 0 ' gibt an, dass ein beliebiger Datenträger zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="19754-296">A value of '0' indicates that any disk is acceptable.</span></span>                                                                              |



 

 

 




