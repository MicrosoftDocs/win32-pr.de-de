---
title: Testfälle für Spiele für Windows; bewährte Methoden für Spiele für Windows XP, Windows Vista, Windows 7 und Windows 8
description: Dieser Artikel enthält Testfälle für Spiele für Windows.
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae26274f199f070ce605227fa19796716df9fbaf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039314"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a><span data-ttu-id="abc41-103">Spiele für Windows-Testfälle: bewährte Methoden für Spiele unter Windows XP, Windows Vista, Windows 7 und Windows 8</span><span class="sxs-lookup"><span data-stu-id="abc41-103">Games for Windows Test Cases: Best Practices for Games on Windows XP, Windows Vista, Windows 7, and Windows 8</span></span>

<span data-ttu-id="abc41-104">Dieser Artikel enthält Testfälle für Spiele für Windows.</span><span class="sxs-lookup"><span data-stu-id="abc41-104">This article provides test cases for games for Windows.</span></span>

## <a name="how-to-use-this-article"></a><span data-ttu-id="abc41-105">Zur Verwendung dieses Artikels</span><span class="sxs-lookup"><span data-stu-id="abc41-105">How to Use This Article</span></span>

<span data-ttu-id="abc41-106">Es gibt drei Hauptabschnitte zu diesem Artikel:</span><span class="sxs-lookup"><span data-stu-id="abc41-106">There are three main sections to this article:</span></span>

<dl> <dt>

<span data-ttu-id="abc41-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Test Anforderungen**</span><span class="sxs-lookup"><span data-stu-id="abc41-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Test Requirements**</span></span>
</dt> <dd>

<span data-ttu-id="abc41-108">Jede Test Anforderung in diesem Dokument umfasst vier Hauptabschnitte: einen Titel und eine Tabelle mit drei wichtigen Abschnitten (linke Spalte, rechts oben, rechts unten).</span><span class="sxs-lookup"><span data-stu-id="abc41-108">Each test requirement in this document has four main sections: a title and a table with three notable sections (left column, right top, right bottom).</span></span>

<dl> <dt>

<span data-ttu-id="abc41-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Tel</span><span class="sxs-lookup"><span data-stu-id="abc41-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Title</span></span>
</dt> <dd>

<span data-ttu-id="abc41-110">Der Name des Testfalls.</span><span class="sxs-lookup"><span data-stu-id="abc41-110">Name of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="abc41-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, Spalte ganz links</span><span class="sxs-lookup"><span data-stu-id="abc41-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, far left column</span></span>
</dt> <dd>

<span data-ttu-id="abc41-112">Die Namen der Betriebssysteme, auf die der Testfall angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-112">Names of the operating systems to which the test case applies.</span></span>

</dd> <dt>

<span data-ttu-id="abc41-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, rechts oben</span><span class="sxs-lookup"><span data-stu-id="abc41-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, right top</span></span>
</dt> <dd>

<span data-ttu-id="abc41-114">Kurze Zusammenfassung des Testfalls.</span><span class="sxs-lookup"><span data-stu-id="abc41-114">Brief summary of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="abc41-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, rechts unten</span><span class="sxs-lookup"><span data-stu-id="abc41-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, right bottom</span></span>
</dt> <dd>

<span data-ttu-id="abc41-116">Details zum eigentlichen Testfall.</span><span class="sxs-lookup"><span data-stu-id="abc41-116">Details of the actual test case.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="abc41-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Beispiel für ein Test Skript**</span><span class="sxs-lookup"><span data-stu-id="abc41-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Sample Test Script**</span></span>
</dt> <dd>

<span data-ttu-id="abc41-118">Dieser Abschnitt ist ein Beispiel für die Sequenz, die bei der Verwendung der Testanforderungen als Leitfaden für einen typischen Test Durchlauf befolgt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-118">This section is a sample of the sequence that a typical test pass would follow if using the test requirements as a guide.</span></span>

</dd> <dt>

<span data-ttu-id="abc41-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Anmerkungen zum Testtool**</span><span class="sxs-lookup"><span data-stu-id="abc41-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Test Tool Notes**</span></span>
</dt> <dd>

<span data-ttu-id="abc41-120">Dieser Abschnitt enthält ausführliche Hinweise zu den einzelnen Test Tools, die zur Überprüfung der Erfolgs-oder Fehlerbedingungen in den Testanforderungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-120">This section contains detailed notes on each of the test tools used to verify pass or fail conditions in the test requirements.</span></span>

</dd> </dl>

## <a name="test-requirements"></a><span data-ttu-id="abc41-121">Test Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abc41-121">Test Requirements</span></span>

### <a name="1-game-requirements"></a><span data-ttu-id="abc41-122">1. Spiel Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abc41-122">1. Game Requirements</span></span>

### <a name="11-windows-games-explorer"></a><span data-ttu-id="abc41-123">1,1 Windows Games Explorer</span><span class="sxs-lookup"><span data-stu-id="abc41-123">1.1 Windows Games Explorer</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-124">Windows 7</span></span><br/> <span data-ttu-id="abc41-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-125">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="abc41-126">Das Spiel muss im Spiele-Explorer unter Windows Vista und Windows 7 sichtbar sein.</span><span class="sxs-lookup"><span data-stu-id="abc41-126">The game must be visible within the Games Explorer on Windows Vista and Windows 7.</span></span> <span data-ttu-id="abc41-127">Wenn diese Option ausgewählt ist, muss das Spiel auch korrekte Metadaten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="abc41-127">When selected, the game must also display correct metadata.</span></span> <span data-ttu-id="abc41-128">Bei der Installation darf keine Verknüpfung erstellt werden, um das Spiel auf dem Desktop, im Startmenü oder an einem anderen Speicherort zu starten.</span><span class="sxs-lookup"><span data-stu-id="abc41-128">The installation must not create a shortcut to launch the game on the desktop, in the Start menu, or in any other location.</span></span> <span data-ttu-id="abc41-129">Aufgaben und Verknüpfungen zum Entfernen dürfen nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-129">Tasks and shortcuts for removal must not be created.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="abc41-130">Nachdem Sie das Spiel installiert haben, öffnen Sie Games Explorer.</span><span class="sxs-lookup"><span data-stu-id="abc41-130">After installing the game, open Games Explorer.</span></span></li>
<li><span data-ttu-id="abc41-131">Stellen Sie sicher, dass das Symbol "Spiel" in Games Explorer angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="abc41-131">Verify that the game icon displays in Games Explorer.</span></span></li>
<li><span data-ttu-id="abc41-132">Klicken Sie mit der rechten Maustaste auf das Symbol, und testen Sie jede Anwendungs definierte Wiedergabe & Unterstützungs Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="abc41-132">Right-click the icon and test each application-defined play & support task.</span></span></li>
<li><span data-ttu-id="abc41-133">Klicken Sie auf das Symbol, und überprüfen Sie, ob die Metadaten (Verleger, Entwickler, Genre, Veröffentlichungsdatum, Version) unten angezeigt werden und korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="abc41-133">Click the icon and verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct.</span></span></li>
<li><span data-ttu-id="abc41-134">Stellen Sie sicher, dass das Symbol "Spiel" Informationen zu Windows-Erfahrungs Index (Wei) in Games Explorer anzeigt.</span><span class="sxs-lookup"><span data-stu-id="abc41-134">Verify that the game icon displays Windows Experience Index (WEI) information in Games Explorer.</span></span></li>
<li><span data-ttu-id="abc41-135">Überprüfen Sie, ob die Spiel Hyperlinks für Metadaten im Spiele-Explorer ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="abc41-135">Verify that game hyperlinks for metadata work correctly in Games Explorer.</span></span> <span data-ttu-id="abc41-136">(Wenn Hyperlinks nicht angezeigt werden, ist dies ein mögliches Vorzeichen, dass die exe-Seite nicht signiert ist. Weitere Informationen finden Sie im <a href="#23-sign-files">Abschnitt 2,3</a>.)</span><span class="sxs-lookup"><span data-stu-id="abc41-136">(If hyperlinks don't show up, then this is a possible sign that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="abc41-137">Stellen Sie sicher, dass das Spiel in Games Explorer eine genaue Bewertung der Jugend Teuerung anzeigt.</span><span class="sxs-lookup"><span data-stu-id="abc41-137">Verify that the game displays accurate parental control rating in Games Explorer.</span></span> <span data-ttu-id="abc41-138">(Wenn er als nicht bewertet eingestuft wird, überprüfen Sie, ob es sich um ein nicht bewertetes Spiel handelt; andernfalls handelt es sich hierbei um einen Indikator, dass die exe-Datei nicht signiert ist. siehe <a href="#23-sign-files">Abschnitt 2,3</a></span><span class="sxs-lookup"><span data-stu-id="abc41-138">(If it says unrated, then verify that this is an unrated game; otherwise, this is an indicator that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="abc41-139">Vergewissern Sie sich, dass das Spiel keine Start Verknüpfungen auf dem Benutzer Desktop platziert.</span><span class="sxs-lookup"><span data-stu-id="abc41-139">Verify that the game does not place launch shortcuts on user desktop.</span></span></li>
<li><span data-ttu-id="abc41-140">Klicken Sie auf Start-> alle Programme.</span><span class="sxs-lookup"><span data-stu-id="abc41-140">Click Start -> All Programs.</span></span></li>
<li><span data-ttu-id="abc41-141">Vergewissern Sie sich, dass das Spiel keine Start Verknüpfungen im Startmenü platziert.</span><span class="sxs-lookup"><span data-stu-id="abc41-141">Verify that the game does not place launch shortcuts in the Start Menu.</span></span></li>
<li><span data-ttu-id="abc41-142">Vergewissern Sie sich, dass das Spiel keine Deinstallations Verknüpfungen im Startmenü außerhalb der Systemsteuerung platziert.</span><span class="sxs-lookup"><span data-stu-id="abc41-142">Verify that the game does not place uninstall shortcuts in Start Menu outside of Control Panel.</span></span></li>
<li><span data-ttu-id="abc41-143">Wenn das Spiel Digital verteilt ist, überprüfen Sie, ob der Dienstanbieter in Windows Games Explorer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-143">If the game is distributed digitally, verify that the service provider appears in Windows Games Explorer.</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a><span data-ttu-id="abc41-144">1,2 Windows-Familien Sicherheit/Eltern Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="abc41-144">1.2 Windows Family Safety / Parental Controls</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-145">Windows 7</span></span><br/> <span data-ttu-id="abc41-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-146">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="abc41-147">Das Spiel muss im Kontext eines &quot; Standard Benutzers ausgeführt werden &quot; .</span><span class="sxs-lookup"><span data-stu-id="abc41-147">Game must execute within the context of a &quot;Standard User&quot;.</span></span> <span data-ttu-id="abc41-148">Eltern Steuerelemente müssen in der Lage sein, das Spiel zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="abc41-148">Parental Controls must be able to block the game.</span></span> <span data-ttu-id="abc41-149">Vergewissern Sie sich, dass die GDF über exe-Namen verfügt.</span><span class="sxs-lookup"><span data-stu-id="abc41-149">Verify that the GDF has EXE names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="abc41-150">Erstellen Sie ein Standard Benutzerkonto in Windows Vista oder Windows 7 namens Toby.</span><span class="sxs-lookup"><span data-stu-id="abc41-150">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="abc41-151">Start->-Systemsteuerung-> Benutzerkonten hinzufügen oder entfernen-> neues Konto erstellen</span><span class="sxs-lookup"><span data-stu-id="abc41-151">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span></li>
<li><span data-ttu-id="abc41-152">Als Andrea haben Sie aus dem Administrator Konto Eltern Steuerelemente für das Spiel eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="abc41-152">As Jane, from Administrator account set up Parental Controls for the game.</span></span> <span data-ttu-id="abc41-153">Start->-Systemsteuerung-> richten Sie die Jugendschutz Steuerelemente für alle Benutzer ></span><span class="sxs-lookup"><span data-stu-id="abc41-153">Start -> Control Panel -> Set Up Parental Controls for Any User -> Toby</span></span>
<ol>
<li><span data-ttu-id="abc41-154">Überprüfen Sie, ob das Spiel über das Symbol für Spiele-Explorer gestartet wird</span><span class="sxs-lookup"><span data-stu-id="abc41-154">Verify that the game launches from the Games Explorer icon.</span></span></li>
<li><span data-ttu-id="abc41-155">Vergewissern Sie sich, dass das Spiel unter dem Spieltitel in der Systemsteuerung für Eltern Steuerelemente eine genaue Bewertung des Eltern Steuer Elements anzeigt.</span><span class="sxs-lookup"><span data-stu-id="abc41-155">Verify that the game displays accurate Parental Control Rating below the game title in the Parental Controls Control Panel.</span></span></li>
<li><span data-ttu-id="abc41-156">Vergewissern Sie sich vor dem Anwenden der Jugend Steuerungsmechanismen, dass das Spiel beim Start keine Administrator Anmelde Informationen auffordert.</span><span class="sxs-lookup"><span data-stu-id="abc41-156">Before applying Parental Controls, verify that the game does not prompt for Administrator Credentials on launch.</span></span></li>
<li><span data-ttu-id="abc41-157">Legen Sie Eltern Steuerelemente auf ein fest &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="abc41-157">Set Parental Controls to &quot;On&quot;.</span></span></li>
<li><span data-ttu-id="abc41-158">Klicken Sie im Abschnitt Windows-Einstellungen auf Games.</span><span class="sxs-lookup"><span data-stu-id="abc41-158">In the Windows Settings section, click Games.</span></span></li>
<li><span data-ttu-id="abc41-159">Klicken Sie auf OK (die Einstellung sollte jetzt &quot; Ao/alle Spiele lauten &quot; ).</span><span class="sxs-lookup"><span data-stu-id="abc41-159">Click OK (setting should now be &quot;AO / all games&quot;).</span></span></li>
<li><span data-ttu-id="abc41-160">Stellen Sie sicher, dass das Spiel mit diesen Einstellungen ausgeführt wird, wie User Jane.</span><span class="sxs-lookup"><span data-stu-id="abc41-160">Verify that the game runs with these settings as User Jane.</span></span></li>
<li><span data-ttu-id="abc41-161">Melden Sie sich als Andrea ab, und melden Sie sich als Toby an.</span><span class="sxs-lookup"><span data-stu-id="abc41-161">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="abc41-162">Stellen Sie sicher, dass das Spiel mit diesen Einstellungen als Benutzer-zu-Ende ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-162">Verify that the game runs with these settings as User Toby.</span></span></li>
<li><span data-ttu-id="abc41-163">Melden Sie sich als Toby ab, und melden Sie sich als Jane an.</span><span class="sxs-lookup"><span data-stu-id="abc41-163">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="abc41-164">Kehren Sie zum vorherigen Bildschirm zurück, und wählen Sie &quot; Spiel Bewertungen festlegen aus &quot; .</span><span class="sxs-lookup"><span data-stu-id="abc41-164">Go back to the previous screen and select &quot;Set Game Ratings&quot;.</span></span></li>
<li><p><span data-ttu-id="abc41-165">Wählen Sie eine Bewertung aus, die niedriger als die ESRB-Bewertung des Spiels ist.</span><span class="sxs-lookup"><span data-stu-id="abc41-165">Select a rating lower than the game's ESRB Rating.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="abc41-166">Wenn das Spiel nicht bewertet wird, überspringen Sie diesen Schritt, und fahren Sie mit dem nächsten Teil dieses Tests fort.</span><span class="sxs-lookup"><span data-stu-id="abc41-166">If the game is not rated, then skip this step and move onto the next part of this test.</span></span> <span data-ttu-id="abc41-167">Es kann erforderlich sein, ein anderes Bewertungssystem auszuwählen, um eine Spiel Bewertung zu finden. Dies hängt vom Gebiets Schema der zu testenden SKU ab.</span><span class="sxs-lookup"><span data-stu-id="abc41-167">It may be necessary to choose a different rating system to find a game rating, depending on the language locale of the SKU being tested.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="abc41-168">Melden Sie sich als Andrea ab, und melden Sie sich als Toby an.</span><span class="sxs-lookup"><span data-stu-id="abc41-168">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="abc41-169">Stellen Sie sicher, dass das Spiel für den Benutzer "um" nicht gestartet wird, wenn ESRB von Benutzer Jane blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-169">Verify that the game does not launch for User Toby when ESRB is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="abc41-170">Melden Sie sich als Toby ab, und melden Sie sich als Jane an.</span><span class="sxs-lookup"><span data-stu-id="abc41-170">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="abc41-171">Wenn Sie zuvor geändert haben, stellen Sie die ESRB-Einstellungen wieder her</span><span class="sxs-lookup"><span data-stu-id="abc41-171">If changed previously, restore the ESRB settings.</span></span></li>
<li><span data-ttu-id="abc41-172">Wenn keine ESRB-Einstellungen vorhanden sind, wählen Sie &quot; bestimmte Spiele blockieren oder zulassen &quot; aus, und wählen Sie das Spiel nach Name aus.</span><span class="sxs-lookup"><span data-stu-id="abc41-172">If there are no ESRB settings, then select &quot;Block or Allow Specific Games&quot; and select the game by name.</span></span></li>
<li><span data-ttu-id="abc41-173">Melden Sie sich als Andrea ab, und melden Sie sich als Toby an.</span><span class="sxs-lookup"><span data-stu-id="abc41-173">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="abc41-174">Stellen Sie sicher, dass das Spiel für den Benutzer "" nicht gestartet wird, wenn "exe/Name" von Benutzer Jane blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-174">Verify that the game does not launch for User Toby when EXE/Name is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="abc41-175">Melden Sie sich als "Toby" und "zurück" als Andrea ab.</span><span class="sxs-lookup"><span data-stu-id="abc41-175">Log off as Toby and back on as Jane.</span></span></li>
<li><span data-ttu-id="abc41-176">Öffnen Sie als Andrea die Benutzer Steuerelemente > Anwendungs Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="abc41-176">As Jane, open User Controls -> Application Restrictions.</span></span></li>
<li><span data-ttu-id="abc41-177">Klicken Sie auf "durch Klicken" &quot; können Sie nur die Programme verwenden, die ich zulässt &quot; , und klicken Sie auf "OK" (keine exe-Datei zulassen)</span><span class="sxs-lookup"><span data-stu-id="abc41-177">Click &quot;Toby can only use the programs I allow&quot; and click OK (that is, allow no exes).</span></span></li>
<li><span data-ttu-id="abc41-178">Gehe zu Benutzer Steuerelementen | Games steuert und ermöglicht das jeweilige Spiel, das die ESRB-Bewertung verwendet.</span><span class="sxs-lookup"><span data-stu-id="abc41-178">Go to User Controls | Games Controls and allow the specific game using the ESRB rating.</span></span></li>
<li><span data-ttu-id="abc41-179">Melden Sie sich als Andrea ab, und melden Sie sich als Toby an, und versuchen Sie, das Spiel zu spielen.</span><span class="sxs-lookup"><span data-stu-id="abc41-179">Log off as Jane, and log on as Toby and try to play the game.</span></span></li>
<li><span data-ttu-id="abc41-180">Stellen Sie sicher, dass das Spiel nicht blockiert ist und dass es von "tby" wiedergegeben werden kann, wenn " &quot; keine exe-Datei zulassen &quot;</span><span class="sxs-lookup"><span data-stu-id="abc41-180">Verify that the game is NOT blocked and that Toby can play it when &quot;allow no exes&quot; is set.</span></span></li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a><span data-ttu-id="abc41-181">1,3 in Windows Vista umfassende gespeicherte Spiele</span><span class="sxs-lookup"><span data-stu-id="abc41-181">1.3 Windows Vista Rich Saved Games</span></span>

<span data-ttu-id="abc41-182">Diese Anforderung wurde zurückgezogen.</span><span class="sxs-lookup"><span data-stu-id="abc41-182">This requirement has been retired.</span></span>

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a><span data-ttu-id="abc41-183">1,4 Xbox 360 allgemeiner Controller für Windows \[ bedingte Anforderung\]</span><span class="sxs-lookup"><span data-stu-id="abc41-183">1.4 Xbox 360 Common Controller for Windows \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-184">Windows 7</span></span><br/> <span data-ttu-id="abc41-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-185">Windows Vista</span></span><br/> <span data-ttu-id="abc41-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-186">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-187">Spiele, die Gamepad-Controller unterstützen, müssen den Xbox 360-Controller für Windows mithilfe der xinput-API unterstützen.</span><span class="sxs-lookup"><span data-stu-id="abc41-187">Games that support gamepad controllers must support the Xbox 360 Controller for Windows using the XInput API.</span></span> <span data-ttu-id="abc41-188">Alle Verweise auf allgemeine Controller Trigger und-Schaltflächen müssen die Xbox 360-Namen verwenden.</span><span class="sxs-lookup"><span data-stu-id="abc41-188">All references to common controller triggers and buttons must use the Xbox 360 names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="abc41-189">Starten Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="abc41-189">Launch the game.</span></span></li>
<li><span data-ttu-id="abc41-190">Wechseln Sie zu den Controller Optionen.</span><span class="sxs-lookup"><span data-stu-id="abc41-190">Go into the controller options.</span></span> **</li>
<li><span data-ttu-id="abc41-191">Vergewissern Sie sich, dass das Spiel Xbox 360-Controller für Windows als Eingabegerät erkennt.</span><span class="sxs-lookup"><span data-stu-id="abc41-191">Verify that the game recognizes Xbox 360 Controller for Windows as an input device.</span></span></li>
<li><span data-ttu-id="abc41-192">Spielen Sie das Spiel, und überprüfen Sie, ob das Spiel und das Menüsystem mit Xbox 360 Controller für Windows steuerbar sind.</span><span class="sxs-lookup"><span data-stu-id="abc41-192">Play the game and verify that the game and menu system are controllable with Xbox 360 Controller for Windows.</span></span></li>
<li><span data-ttu-id="abc41-193">Vergewissern Sie sich, dass sich der Xbox 360-Controller für Windows gemäß den akzeptierten Standards verhält.</span><span class="sxs-lookup"><span data-stu-id="abc41-193">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards.</span></span> <span data-ttu-id="abc41-194">(B für "zurück", "A" für "Accept", "Start" im Menü "Spiel", "anhalten", "annehmen</span><span class="sxs-lookup"><span data-stu-id="abc41-194">(B for back, A for accept, Start for in game menu/pause or accept, etc.)</span></span></li>
<li><span data-ttu-id="abc41-195">Stellen Sie sicher, dass sich das Spiel auf die Controller Schaltflächen und Trigger mit Xbox 360-Namen bezieht.</span><span class="sxs-lookup"><span data-stu-id="abc41-195">Verify that the game refers to the controller buttons and triggers using Xbox 360 names.</span></span></li>
</ol>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="abc41-196">Wenn das Spiel keinen Spiele Controller unterstützt und/oder nur Tastatur/Maus unterstützt, überspringen Sie diesen Testfall.</span><span class="sxs-lookup"><span data-stu-id="abc41-196">If the game does not support a game controller and/or only supports keyboard/mouse, then skip this test case.</span></span>
</blockquote>
<br/> <span data-ttu-id="abc41-197">\* \* Einstellungen für den Controller befinden sich möglicherweise außerhalb des Spiels.</span><span class="sxs-lookup"><span data-stu-id="abc41-197">\*\* Settings for the controller might be located outside of the game.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a><span data-ttu-id="abc41-198">1,5 mehrere Seitenverhältnisse und Auflösungen</span><span class="sxs-lookup"><span data-stu-id="abc41-198">1.5 Multiple Aspect Ratios and Resolutions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-199">Windows 7</span></span><br/> <span data-ttu-id="abc41-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-200">Windows Vista</span></span><br/> <span data-ttu-id="abc41-201">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-201">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-202">Das Spiel muss mindestens die folgenden Seitenverhältnisse und zugeordneten Bildschirmauflösungen unterstützen:</span><span class="sxs-lookup"><span data-stu-id="abc41-202">The game must support at least the following aspect ratios and associated screen resolutions:</span></span> <br/>
<ul>
<li><span data-ttu-id="abc41-203">4:3 &quot; Normal &quot; (800 600 oder 1024 768)</span><span class="sxs-lookup"><span data-stu-id="abc41-203">4:3 &quot;normal&quot; (800 600 or 1024 768)</span></span></li>
<li><span data-ttu-id="abc41-204">16:9- &quot; Breitbild &quot; (1280 720)</span><span class="sxs-lookup"><span data-stu-id="abc41-204">16:9 &quot;widescreen&quot; (1280 720)</span></span></li>
<li><span data-ttu-id="abc41-205">16:10- &quot; Breitbild &quot; (1152 720, 1680 1050 oder 800 480)</span><span class="sxs-lookup"><span data-stu-id="abc41-205">16:10 &quot;widescreen&quot; (1152 720, 1680 1050, or 800 480)</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="abc41-206">Suchen Sie die Video Optionen für das Spiel (diese sind möglicherweise im Spiel).</span><span class="sxs-lookup"><span data-stu-id="abc41-206">Locate the Video Options for the game (this may be in our out of game).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="abc41-207">Die folgenden Tests müssen auf einem Breitbild Schirm ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-207">The following tests must be done on a widescreen monitor.</span></span>
</blockquote>
<br/>
<ol>
<li><span data-ttu-id="abc41-208">Wählen Sie im Abschnitt Videoauflösung die Option 800 600 oder 1024 768 aus.</span><span class="sxs-lookup"><span data-stu-id="abc41-208">In the video resolution section, select 800 600 or 1024 768.</span></span></li>
<li><span data-ttu-id="abc41-209">Überprüfen Sie, ob das Spiel bei einer 4:3-Seitenverhältnis Auflösung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-209">Verify that the game runs at a 4:3 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="abc41-210">Wählen Sie im Abschnitt Videoauflösung die Option 1280 720 aus.</span><span class="sxs-lookup"><span data-stu-id="abc41-210">In the video resolution section, select 1280 720.</span></span></li>
<li><span data-ttu-id="abc41-211">Überprüfen Sie, ob das Spiel bei einer 16:9-Seitenverhältnis Auflösung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-211">Verify that the game runs at a 16:9 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="abc41-212">Wählen Sie im Abschnitt Videoauflösung die Option 1680 1050, 800 480 oder 1152 720 aus.</span><span class="sxs-lookup"><span data-stu-id="abc41-212">In the video resolution section, select 1680 1050, 800 480, or 1152 720.</span></span></li>
<li><span data-ttu-id="abc41-213">Überprüfen Sie, ob das Spiel bei einer 16:10-Seitenverhältnis Auflösung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-213">Verify that the game runs at a 16:10 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="abc41-214">Stellen Sie sicher, dass das Spiel das Bild nicht Strecken und wiederum einen breiteren Bereich der Ansicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="abc41-214">Verify that the game does not stretch the picture and in turn presents a wider area of view.</span></span></li>
<li><span data-ttu-id="abc41-215">Überprüfen Sie, ob das Spiel den Benutzer auffordert, wenn eine Änderung an der Auflösung vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-215">Verify that the game prompts the user when a change is made to the resolution.</span></span></li>
<li><span data-ttu-id="abc41-216">Wenn der Benutzer nicht innerhalb von 15 Sekunden akzeptiert, vergewissern Sie sich, dass die Anzeige auf die vorherige Einstellung zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-216">If the user does not accept within 15 seconds, verify that the display reverts to the previous setting.</span></span></li>
<li><span data-ttu-id="abc41-217">Vergewissern Sie sich, dass das Spiel keine schwarzen Balken Links und rechts im Spielbereich des Spiels hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="abc41-217">Verify that the game does not add black bars to the left and right of the game play area.</span></span> <span data-ttu-id="abc41-218">(In diesem Fall wird der Spielbereich in einem 4:3-Verhältnis in der Mitte des Bildschirms angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="abc41-218">(In this case, you will see the game area still in a 4:3 ratio in the middle of the screen.)</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a><span data-ttu-id="abc41-219">1,6 Windows Media Center</span><span class="sxs-lookup"><span data-stu-id="abc41-219">1.6 Windows Media Center</span></span>

<span data-ttu-id="abc41-220">Diese Anforderung wurde zurückgezogen.</span><span class="sxs-lookup"><span data-stu-id="abc41-220">This requirement has been retired.</span></span>

### <a name="17-direct3d-conditional-requirement"></a><span data-ttu-id="abc41-221">1,7 Direct3D \[ bedingte Anforderung\]</span><span class="sxs-lookup"><span data-stu-id="abc41-221">1.7 Direct3D \[Conditional Requirement\]</span></span>



|                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abc41-222">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-222">Windows 7</span></span><br/> <span data-ttu-id="abc41-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-223">Windows Vista</span></span><br/> <span data-ttu-id="abc41-224">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-224">Windows XP</span></span><br/> | <span data-ttu-id="abc41-225">Wenn das Spiel Direct3D verwendet, muss die mindestens unterstützte Version Direct3D 9 sein, und Direct3D muss der Standardwert für jede Anzeige Konfigurationsoption sein.</span><span class="sxs-lookup"><span data-stu-id="abc41-225">If the game uses Direct3D, the minimum version supported must be Direct3D 9, and Direct3D must be the default for any display configuration option.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|                                                                     | <dl> <span data-ttu-id="abc41-226"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuell</dt></span><span class="sxs-lookup"><span data-stu-id="abc41-226"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt></span></span> <dd> <span data-ttu-id="abc41-227">Starten Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="abc41-227">Launch the game.</span></span> <span data-ttu-id="abc41-228">Überprüfen Sie in den Videooptionen, ob die Optionen "Rendering", "D3D" und "OpenGL" vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="abc41-228">In the video options, check to see if there are render options, D3D and/or OpenGL.</span></span> <span data-ttu-id="abc41-229">Wenn dies der Fall ist, überprüfen Sie, ob die spielend-Optionen standardmäßig auf Direct3D</span><span class="sxs-lookup"><span data-stu-id="abc41-229">If there are, verify that the game render options default to Direct3D.</span></span> <span data-ttu-id="abc41-230">Wenn Sie nicht überprüfen können, ob d3d9 die verwendete Version von DirectX ist, fahren Sie mit dem automatisierten Test fort.</span><span class="sxs-lookup"><span data-stu-id="abc41-230">If you are unable to verify that D3D9 is the version of DirectX that is being used, then proceed to Automated Test.</span></span> <br/> </dd> <span data-ttu-id="abc41-231"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automatisierter Test</dt></span><span class="sxs-lookup"><span data-stu-id="abc41-231"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt></span></span> <dd> <span data-ttu-id="abc41-232">Tool verwenden: Depends.exe</span><span class="sxs-lookup"><span data-stu-id="abc41-232">Use tool: Depends.exe</span></span> <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a><span data-ttu-id="abc41-233">1,8 Aktivieren von High-dpi-Werten</span><span class="sxs-lookup"><span data-stu-id="abc41-233">1.8 Enable High-DPI Aware</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-234">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-234">Windows 7</span></span><br/> <span data-ttu-id="abc41-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-235">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="abc41-236">Spiele und deren Installer müssen ohne visuelle Probleme ordnungsgemäß ausgeführt werden, wenn die DPI-Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="abc41-236">Games and their installers must run correctly without visual problems when DPI scaling is enabled.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="abc41-237"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuell</dt> </span><span class="sxs-lookup"><span data-stu-id="abc41-237"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="abc41-238">Legen Sie das System auf dpi 150% fest:</span><span class="sxs-lookup"><span data-stu-id="abc41-238">Set the system to DPI 150%:</span></span> <br/> <span data-ttu-id="abc41-239">Windows Vista: Systemsteuerung: Personalisierung, Schriftart anpassen (dpi), benutzerdefinierter dpi-Code.</span><span class="sxs-lookup"><span data-stu-id="abc41-239">Windows Vista: Control Panel: Personalization, Adjust font size (DPI), Custom DPI.</span></span> <span data-ttu-id="abc41-240">Auf 150% festgelegt.</span><span class="sxs-lookup"><span data-stu-id="abc41-240">Set to 150%.</span></span><br/> <span data-ttu-id="abc41-241">Windows 7: Systemsteuerung: Anzeige, Festlegung auf größer-150%.</span><span class="sxs-lookup"><span data-stu-id="abc41-241">Windows 7: Control Panel: Display, Set to Larger - 150%.</span></span><br/></li>
<li><span data-ttu-id="abc41-242">Führen Sie den Installationsprozess und das Spiel aus, um sicherzustellen, dass keine Probleme mit ausgeschnittenen Bildschirmen oder Dialogfeldern vorliegen.</span><span class="sxs-lookup"><span data-stu-id="abc41-242">Run the installation process and game to verify there are no problems with clipped screens or dialog boxes.</span></span></li>
</ol>
</dd> <span data-ttu-id="abc41-243"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automatisierter Test</dt> </span><span class="sxs-lookup"><span data-stu-id="abc41-243"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="abc41-244">Vergewissern Sie sich, dass das Element <dpiAware>true</dpiAware> im eingebetteten Manifest enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="abc41-244">Verify that element <dpiAware>true</dpiAware> is contained in the embedded manifest.</span></span><br/> <span data-ttu-id="abc41-245">Tool verwenden: Mt.exe</span><span class="sxs-lookup"><span data-stu-id="abc41-245">Use tool: Mt.exe</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a><span data-ttu-id="abc41-246">2. Sicherheit und Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="abc41-246">2. Security and Compatibility</span></span>

### <a name="21-follow-user-account-control-guidelines"></a><span data-ttu-id="abc41-247">2,1 befolgen Sie die Richtlinien zur Benutzerkontensteuerung</span><span class="sxs-lookup"><span data-stu-id="abc41-247">2.1 Follow User Account Control Guidelines</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-248">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-248">Windows 7</span></span><br/> <span data-ttu-id="abc41-249">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-249">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="abc41-250">Jede ausführbare Datei (. EXE-Erweiterung), die in einer Anwendung enthalten ist, muss ein eingebettetes Manifest aufweisen, das die Ausführungs Ebene definiert:</span><span class="sxs-lookup"><span data-stu-id="abc41-250">Every executable file (.EXE extension) included with an application must have an embedded manifest that defines its execution level:</span></span>
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="abc41-251">Für Spiele und Spiel Installationsprogramme sollte UIAccess immer auf false festgelegt werden &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="abc41-251">For games and game installers, uiAccess should always be set to &quot;false&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="abc41-252">Überprüfen, ob ausführbare Spieldateien Manifeste enthalten.</span><span class="sxs-lookup"><span data-stu-id="abc41-252">Verify game executable files contain manifests.</span></span></li>
<li><span data-ttu-id="abc41-253">Überprüfen der ausführbaren Datei des ausführbaren Datei Manifests requestedExecutionLevel ist &quot; asInvoker &quot; .</span><span class="sxs-lookup"><span data-stu-id="abc41-253">Verify game executable file manifest requestedExecutionLevel is &quot;AsInvoker&quot;.</span></span></li>
</ol>
<span data-ttu-id="abc41-254">Tool verwenden: Mt.exe</span><span class="sxs-lookup"><span data-stu-id="abc41-254">Use tool: Mt.exe</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a><span data-ttu-id="abc41-255">2,2 Unterstützung von x64-Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="abc41-255">2.2 Support x64 Versions of Windows</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-256">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-256">Windows 7</span></span><br/> <span data-ttu-id="abc41-257">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-257">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="abc41-258">So gewährleisten Sie die Kompatibilität mit x64-Versionen von Windows:</span><span class="sxs-lookup"><span data-stu-id="abc41-258">To maintain compatibility with x64 versions of Windows:</span></span> <br/>
<ul>
<li><span data-ttu-id="abc41-259">Titel und Titel-Installer dürfen keinen 16-Bit-Code enthalten oder auf eine 16-Bit-Komponente zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="abc41-259">Titles and title installers must not contain any 16-bit code or rely on any 16-bit component.</span></span></li>
<li><span data-ttu-id="abc41-260">Wenn das Spiel von Kernelmodustreibern für den Betrieb abhängt, müssen x64-Versionen dieser Treiber verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="abc41-260">If the game is dependent on kernel-mode drivers for operation, x64 versions of these drivers must be available.</span></span> <span data-ttu-id="abc41-261">Die Spiel Einrichtung muss die richtigen Treiber und Komponenten für die 64-Bit-Editionen von Windows erkennen und installieren.</span><span class="sxs-lookup"><span data-stu-id="abc41-261">The game setup must detect and install the proper drivers and components for 64-bit editions of Windows.</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="abc41-262">Die Unterstützung für die 64-Bit-Edition von Windows XP Professional ist optional.</span><span class="sxs-lookup"><span data-stu-id="abc41-262">Support for the 64-bit Edition of Windows XP Professional is optional.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="abc41-263">Manueller Test</span><span class="sxs-lookup"><span data-stu-id="abc41-263">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="abc41-264">Führen Sie das Spiel auf 64-Bit-Editionen von Windows aus.</span><span class="sxs-lookup"><span data-stu-id="abc41-264">Run the game on 64-bit editions of Windows.</span></span> <span data-ttu-id="abc41-265">Vergewissern Sie sich, dass der Spiele Installationsprozess auf 64-Bit-Editionen von Windows Vista oder Windows 7 normal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-265">Verify that the game installation process runs normally on 64-bit editions of Windows Vista or Windows 7.</span></span></li>
<li><span data-ttu-id="abc41-266">Stellen Sie sicher, dass für das Spiel in den 64-Bit-Editionen von Windows Vista oder Windows 7 kein Fehler aufgrund von 16-Bit-ausführbaren Dateien auftritt.</span><span class="sxs-lookup"><span data-stu-id="abc41-266">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista or Windows 7.</span></span> <span data-ttu-id="abc41-267">Der Fehler wird die 16-Bit-Anwendung im Fehler Fenster erwähnen.</span><span class="sxs-lookup"><span data-stu-id="abc41-267">The error will mention the 16-bit application in the error window.</span></span></li>
<li><span data-ttu-id="abc41-268">Wenn das Spiel über eine systemeigene ausführbare 64-Bit-Datei verfügt, verwenden Sie diese ebenfalls.</span><span class="sxs-lookup"><span data-stu-id="abc41-268">If the game has a native 64-bit executable, then use that as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a><span data-ttu-id="abc41-269">2,3 Signier Dateien</span><span class="sxs-lookup"><span data-stu-id="abc41-269">2.3 Sign Files</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-270">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-270">Windows 7</span></span><br/> <span data-ttu-id="abc41-271">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-271">Windows Vista</span></span><br/> <span data-ttu-id="abc41-272">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-272">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-273">Alle ausführbaren Code Dateien (z. b. exe-und dll-Erweiterungen) müssen mit einem Authenticode-Zertifikat signiert werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-273">All executable code files (for example, .exe and .dll extensions) must be signed with an Authenticode certificate.</span></span> <br/> <span data-ttu-id="abc41-274">Wenn Sie Windows Installer verwenden, müssen die Paketdateien (MSI-Dateien) des Installers signiert sein.</span><span class="sxs-lookup"><span data-stu-id="abc41-274">If you are using Windows Installer, the installer's package files (.msi files) must be signed.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="abc41-275">Manueller Test</span><span class="sxs-lookup"><span data-stu-id="abc41-275">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="abc41-276">Navigieren Sie zum Spielverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="abc41-276">Navigate to the game directory.</span></span></li>
<li><span data-ttu-id="abc41-277">Suchen Sie alle exe-und dll-Dateien.</span><span class="sxs-lookup"><span data-stu-id="abc41-277">Locate all of the .exe and .dll files.</span></span></li>
<li><span data-ttu-id="abc41-278">Klicken Sie mit der rechten Maustaste auf Eigenschaften für jede Datei.</span><span class="sxs-lookup"><span data-stu-id="abc41-278">Right-click Properties on each file.</span></span></li>
<li><span data-ttu-id="abc41-279">Vergewissern Sie sich, dass die ausführbaren Dateien des Spiels eine digitale Signatur enthalten.</span><span class="sxs-lookup"><span data-stu-id="abc41-279">Verify that the game executable files contain a digital signature.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a><span data-ttu-id="abc41-280">2,4-Signatur Treiber</span><span class="sxs-lookup"><span data-stu-id="abc41-280">2.4 Sign Drivers</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-281">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-281">Windows 7</span></span><br/> <span data-ttu-id="abc41-282">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-282">Windows Vista</span></span><br/> <span data-ttu-id="abc41-283">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-283">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-284">Jeder Kernelmodustreiber, der durch das Spiel installiert wird, muss mit einem öffentlich gültigen Authenticode-Zertifikat signiert werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-284">Any kernel-mode driver that is installed by the game must be signed with a publicly valid Authenticode certificate.</span></span> <br/> <span data-ttu-id="abc41-285">Jeder vom Spiel installierte Kernel Modus-Hardware Gerätetreiber muss über eine Microsoft-Signatur verfügen, die über das Windows Hardware Quality Labs (WHQL) oder das DRS-Programm (Driver Zuverlässigkeits Signature) abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-285">Any kernel-mode hardware device driver that is installed by the game must have a Microsoft signature obtained through the Windows Hardware Quality Labs (WHQL) or Driver Reliability Signature (DRS) program.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="abc41-286">Manueller Test</span><span class="sxs-lookup"><span data-stu-id="abc41-286">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="abc41-287">Installieren Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="abc41-287">Install the game.</span></span></li>
<li><span data-ttu-id="abc41-288">Vergewissern Sie sich, dass bei der Spiele Installation nicht signierte Treiber Dialogfelder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-288">Verify that the game install process does not display unsigned driver dialog(s).</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a><span data-ttu-id="abc41-289">2,5 Ausführen der Versions Überprüfung ordnungsgemäß</span><span class="sxs-lookup"><span data-stu-id="abc41-289">2.5 Perform Version Checking Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-290">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-290">Windows 7</span></span><br/> <span data-ttu-id="abc41-291">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-291">Windows Vista</span></span><br/> <span data-ttu-id="abc41-292">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-292">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-293">Spiele dürfen nicht für zukünftige Betriebssysteme ausgeführt werden, die durch Änderungen der Windows-Versionsnummer angegeben werden, es sei denn, der Endbenutzer-Lizenzvertrag untersagt die Verwendung bei zukünftigen Betriebssystemen.</span><span class="sxs-lookup"><span data-stu-id="abc41-293">Games must not fail to run on future operating systems as indicated by changes in the Windows version number, unless the End User License Agreement prohibits use on future operating systems.</span></span> <span data-ttu-id="abc41-294">Wenn das Spiel fehlschlagen soll, muss es ordnungsgemäß ausgeführt werden, indem eine Meldung für den Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-294">If the game is supposed to fail, it must do so gracefully by displaying a message to the user.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="abc41-295"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuell</dt> </span><span class="sxs-lookup"><span data-stu-id="abc41-295"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="abc41-296">Installieren Sie das Spiel unter Windows XP, auf 32-Bit-Editionen von Windows Vista und Windows 7 und auf 64-Bit-Editionen von Windows Vista und Windows 7.</span><span class="sxs-lookup"><span data-stu-id="abc41-296">Install the game on Windows XP, on 32-bit editions of Windows Vista and Windows 7, and on 64-bit editions of Windows Vista and Windows 7.</span></span></li>
<li><span data-ttu-id="abc41-297">Vergewissern Sie sich, dass bei der Spiele Installation kein Fehler in Bezug auf die Betriebssystemversion auftritt.</span><span class="sxs-lookup"><span data-stu-id="abc41-297">Verify that the game installation process does not encounter an error regarding OS version.</span></span></li>
</ol>
</dd> <span data-ttu-id="abc41-298"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automatisierter Test</dt> </span><span class="sxs-lookup"><span data-stu-id="abc41-298"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="abc41-299">Tool verwenden: Application Verifier</span><span class="sxs-lookup"><span data-stu-id="abc41-299">Use tool: Application Verifier</span></span><br/>
<ol>
<li><span data-ttu-id="abc41-300">Starten Sie Application Verifier.</span><span class="sxs-lookup"><span data-stu-id="abc41-300">Launch Application Verifier.</span></span></li>
<li><span data-ttu-id="abc41-301">Aktivieren Sie die Option Kompatibilität: highversionlie Test, nachdem Sie die INSTALL.EXE ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="abc41-301">Enable the Compatibility:HighVersionLie test after selecting the INSTALL.EXE.</span></span></li>
<li><span data-ttu-id="abc41-302">Installieren Sie das Spiel, und stellen Sie sicher, dass es die Installation nicht basierend auf der Betriebssystemversion blockiert.</span><span class="sxs-lookup"><span data-stu-id="abc41-302">Install the game and ensure that it does not block installation based on the OS version.</span></span></li>
<li><span data-ttu-id="abc41-303">Aktivieren Sie die Option Kompatibilität: highversionlie Test, nachdem Sie die GAME.EXE ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="abc41-303">Enable the Compatibility:HighVersionLie test after selecting the GAME.EXE.</span></span></li>
<li><span data-ttu-id="abc41-304">Führen Sie das Spiel aus, und stellen Sie sicher, dass die Ausführung auf Basis der Betriebssystemversion nicht blockiert wird</span><span class="sxs-lookup"><span data-stu-id="abc41-304">Run the game and ensure it does not block execution based on the OS version.</span></span></li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a><span data-ttu-id="abc41-305">2,6 Unterstützung von gleichzeitigen Benutzersitzungen</span><span class="sxs-lookup"><span data-stu-id="abc41-305">2.6 Support Concurrent User Sessions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-306">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-306">Windows 7</span></span><br/> <span data-ttu-id="abc41-307">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-307">Windows Vista</span></span><br/> <span data-ttu-id="abc41-308">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-308">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-309">Spiele müssen Windows-Multitasking-Standardszenarien unterstützen.</span><span class="sxs-lookup"><span data-stu-id="abc41-309">Games must support standard Windows multitasking scenarios.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="abc41-310">Erstellen Sie ein Standard Benutzerkonto in Windows Vista oder Windows 7 namens Toby.</span><span class="sxs-lookup"><span data-stu-id="abc41-310">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="abc41-311">Start->-Systemsteuerung-> Benutzerkonten hinzufügen oder entfernen-> neues Konto erstellen</span><span class="sxs-lookup"><span data-stu-id="abc41-311">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span> <br/>
<ol>
<li><span data-ttu-id="abc41-312">Starten Sie das Spiel als Benutzer Jane.</span><span class="sxs-lookup"><span data-stu-id="abc41-312">Launch the game as User Jane.</span></span></li>
<li><span data-ttu-id="abc41-313">Alt + Tab zurück zum Desktop.</span><span class="sxs-lookup"><span data-stu-id="abc41-313">ALT+TAB back to the desktop.</span></span></li>
<li><span data-ttu-id="abc41-314">Überprüfen Sie, ob das Spiel ordnungsgemäß alt + Tabstopps zum Windows-Desktop ist.</span><span class="sxs-lookup"><span data-stu-id="abc41-314">Verify that the game properly ALT+TABs to the Windows desktop.</span></span></li>
<li><span data-ttu-id="abc41-315">Klicken Sie auf Start-> [Pfeil rechts von Lock]-> Switch User.</span><span class="sxs-lookup"><span data-stu-id="abc41-315">Click Start -> [arrow to the right of Lock] -> Switch User.</span></span></li>
<li><span data-ttu-id="abc41-316">Melden Sie sich als Benutzer Toby an.</span><span class="sxs-lookup"><span data-stu-id="abc41-316">Log on as User Toby.</span></span></li>
<li><span data-ttu-id="abc41-317">Stellen Sie sicher, dass das Spiel als Benutzer-zu-Ende gestartet wird, während es weiterhin als Benutzer Jane ausgeführt</span><span class="sxs-lookup"><span data-stu-id="abc41-317">Verify that the game launches as User Toby while still running as User Jane.</span></span></li>
<li><span data-ttu-id="abc41-318">Stellen Sie sicher, dass für das Spiel während der benutzerswitchverarbeitung keine Fehler für Benutzer-oder Benutzer-Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-318">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process.</span></span></li>
<li><span data-ttu-id="abc41-319">Wenn Sie eine weitere Spielsitzung starten können, stellen Sie sicher, dass Sie kein Audiomaterial aus der ursprünglichen Spielsitzung hören können.</span><span class="sxs-lookup"><span data-stu-id="abc41-319">If you can launch another game session, verify that you cannot hear audio from the original game session.</span></span></li>
<li><span data-ttu-id="abc41-320">Schließen Sie das Spiel, und wechseln Sie zurück zum ursprünglichen Benutzer und Spiel.</span><span class="sxs-lookup"><span data-stu-id="abc41-320">Close the game and switch back to the original user and game.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a><span data-ttu-id="abc41-321">2,7 Unterstützung von langen Namen</span><span class="sxs-lookup"><span data-stu-id="abc41-321">2.7 Support Long Names</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-322">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-322">Windows 7</span></span><br/> <span data-ttu-id="abc41-323">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-323">Windows Vista</span></span><br/> <span data-ttu-id="abc41-324">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-324">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-325">Wenn ein Spiel das Speichern von Dateien unterstützt, muss es in der Lage sein, Dateien mit langen Namen und Pfaden zu speichern.</span><span class="sxs-lookup"><span data-stu-id="abc41-325">If a game supports saving files, it must be able to save files that have long names and paths.</span></span> <span data-ttu-id="abc41-326">Das Spiel muss spezielle Dateisystem Zeichen, wie z. b. \/: \*, ordnungsgemäß verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="abc41-326">The game must properly handle special file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="abc41-327">&quot; < oder > in den Benutzereingabe Feldern, die zum Erstellen von Dateinamen oder Pfaden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-327">&quot; < or > in any user input fields used to create file names or paths.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="abc41-328">Starten Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="abc41-328">Launch the game.</span></span></li>
<li><span data-ttu-id="abc41-329">Starten Sie ein neues Spiel.</span><span class="sxs-lookup"><span data-stu-id="abc41-329">Start a new game.</span></span></li>
<li><span data-ttu-id="abc41-330">Speichern Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="abc41-330">Save the game.</span></span> <span data-ttu-id="abc41-331">Überprüfen Sie während des Speicher Vorgangs, ob das Spiel mit dem Speichern-Namen: mein erstes Save-Spiel gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-331">During the save process, verify that the game saves using the save name: My First Save Game.</span></span></li>
<li><span data-ttu-id="abc41-332">Kehren Sie zurück zum Hauptmenü.</span><span class="sxs-lookup"><span data-stu-id="abc41-332">Exit back to the main menu.</span></span></li>
<li><span data-ttu-id="abc41-333">Versuchen Sie, das neu gespeicherte Spiel zu laden.</span><span class="sxs-lookup"><span data-stu-id="abc41-333">Attempt to load the newly saved game.</span></span></li>
<li><span data-ttu-id="abc41-334">Stellen Sie sicher, dass beim Umgang mit nicht unterstützten Dateisystem Zeichen, wie z. b. \/: \*, keine Fehler im Spiel auftreten.</span><span class="sxs-lookup"><span data-stu-id="abc41-334">Verify that the game does not encounter errors when handling unsupported file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="abc41-335">&quot; < oder > Wenn Sie das Spiel zulässt, benennen Sie das gespeicherte Spiel.</span><span class="sxs-lookup"><span data-stu-id="abc41-335">&quot; < or > If the game allows you, name the saved game.</span></span></li>
<li><span data-ttu-id="abc41-336">Wenn der Benutzer das Profil und/oder das Zeichen benennen oder Spiele speichern darf, vergewissern Sie sich, dass beim Verwenden von langen Dateinamen auch bei dem Spiel keine Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="abc41-336">If the user is allowed to name their profile and/or character or save games, verify that the game does not encounter errors when using long file names here as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a><span data-ttu-id="abc41-337">3. Installation</span><span class="sxs-lookup"><span data-stu-id="abc41-337">3. Installation</span></span>

### <a name="31-easy-install"></a><span data-ttu-id="abc41-338">3,1 einfache Installation</span><span class="sxs-lookup"><span data-stu-id="abc41-338">3.1 Easy Install</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-339">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-339">Windows 7</span></span><br/> <span data-ttu-id="abc41-340">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-340">Windows Vista</span></span><br/> <span data-ttu-id="abc41-341">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-341">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-342">Spiele mit einer herkömmlichen Installation müssen einen vereinfachten Pfad in der Setup-Benutzeroberfläche bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="abc41-342">Games with a traditional installation must provide a simplified path in their setup user interface.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="abc41-343">Legen Sie die Spiel-CD ein.</span><span class="sxs-lookup"><span data-stu-id="abc41-343">Insert the game disc.</span></span></li>
<li><span data-ttu-id="abc41-344">Stellen Sie sicher, dass das Spiel nicht mehr als einen End-User Lizenzvertrag (EULA) anzeigt.</span><span class="sxs-lookup"><span data-stu-id="abc41-344">Verify that the game does not display more than one End-User License Agreement (EULA).</span></span></li>
<li><span data-ttu-id="abc41-345">Wenn das Spiel eine benutzerdefinierte oder erweiterte Installationsoption unterstützt, überprüfen Sie, ob diese Option während des Installationsvorgangs verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="abc41-345">If the game supports a custom or advanced installation option, verify that this option is accessible during the installation process.</span></span></li>
<li><span data-ttu-id="abc41-346">Überprüfen Sie, ob die Standard Installationsoption die gesamte Benutzereingabe Auswahl für den Installationsvorgang umgeht (Auswahl von Installationsordner, Komponentenauswahl usw.).</span><span class="sxs-lookup"><span data-stu-id="abc41-346">Verify that the Default installation option bypasses all user input selections for the installation process (selection of installation folder, components selection, and so on).</span></span></li>
<li><span data-ttu-id="abc41-347">Stellen Sie sicher, dass bei der Spiele Installation keine Eingabeaufforderung für das Setup der Betriebssystem Komponente (DirectX-Setup, Visual C-Runtimes usw.) angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-347">Verify that the game installation process does not prompt for OS component setup (DirectX setup, Visual C Runtimes, and so on).</span></span></li>
<li><span data-ttu-id="abc41-348">Vergewissern Sie sich, dass bei der Spiele Installation keine Firewall-Interaktion angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-348">Verify that the game installation process does not prompt for firewall interaction.</span></span></li>
<li><span data-ttu-id="abc41-349">Überprüfen Sie, ob das Spiel automatisch ausgeführt wird oder ob ein Start Programm Menü am Ende des Installationsvorgangs vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="abc41-349">Verify that the game automatically runs or that a launcher menu is present at the end of the install process.</span></span></li>
<li><span data-ttu-id="abc41-350">Vergewissern Sie sich, dass bei der Deinstallation des Spiels alle installierten, nicht neu verteilten Betriebssystem-Komponenten Dateien entfernt werden und alle Einstellungen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-350">Verify that the game uninstallation process removes all installed, non-redistributed OS component files and clears all settings.</span></span> <span data-ttu-id="abc41-351">Das Bereinigen aller benutzerspezifischen Einstellungen und Daten (z. b. gespeicherter Spiele) ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="abc41-351">Cleaning up all per-user settings and data (such as saved games) is not required.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a><span data-ttu-id="abc41-352">3,2 Unterstützung der Benutzerkontensteuerung für die Installation</span><span class="sxs-lookup"><span data-stu-id="abc41-352">3.2 Support User Account Control for Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-353">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-353">Windows 7</span></span><br/> <span data-ttu-id="abc41-354">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-354">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="abc41-355">Der Game Installer darf nicht davon ausgehen, dass er im gleichen Kontext wie der Benutzer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-355">The game installer must not assume it is running in the same context as the user.</span></span> <span data-ttu-id="abc41-356">Spiele müssen daher benutzerspezifische Aufgaben bei der ersten Ausführung separat von der Installation ausführen.</span><span class="sxs-lookup"><span data-stu-id="abc41-356">Games must therefore perform per-user tasks on first-run separately from the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="abc41-357">Vergewissern Sie sich, dass Sie das Spiel als Benutzer Jane installieren können.</span><span class="sxs-lookup"><span data-stu-id="abc41-357">Verify that you can install the game as User Jane.</span></span> <span data-ttu-id="abc41-358">(Dies erfordert erhöhte Rechte während des Setup-/Installationsprozesses.)</span><span class="sxs-lookup"><span data-stu-id="abc41-358">(This will require elevated rights during the setup/installation process.)</span></span></li>
<li><span data-ttu-id="abc41-359">Vergewissern Sie sich, dass der Spiel Installationsprozess Benutzer Jane auffordert, Rechte über Administrator Anmelde Informationen zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="abc41-359">Verify that the game installation process prompts User Jane to elevate through Administrator Credentials.</span></span> <span data-ttu-id="abc41-360">(Die Aufforderung zur Erhöhung der Rechte wird angezeigt, wenn der Benutzer versucht, zu installieren.)</span><span class="sxs-lookup"><span data-stu-id="abc41-360">(The prompt to elevate will come up when the user attempts to install.)</span></span></li>
<li><span data-ttu-id="abc41-361">Deaktivieren Sie das Spiel am Ende der Installation, falls dies noch nicht der Fall ist, oder starten Sie es über das Menü, das angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-361">Opt to Autorun the game at the end of installation, if it does not already do so, or launch it from the menu that appears.</span></span></li>
<li><span data-ttu-id="abc41-362">Erstellen Sie ein neues Profil, und spielen Sie ein Spiel, und speichern Sie es.</span><span class="sxs-lookup"><span data-stu-id="abc41-362">Once in-game, create a new profile, play and save a game.</span></span></li>
<li><span data-ttu-id="abc41-363">Beenden Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="abc41-363">Exit the game.</span></span></li>
<li><span data-ttu-id="abc41-364">Starten Sie das Spiel neu, und stellen Sie sicher, dass das Benutzer-und die gespeicherten Spiele vom Benutzer-Jane-Konto aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-364">Restart the game and verify that User Profiles and Saved Games can be accessed by the User Jane account.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a><span data-ttu-id="abc41-365">3,3 in richtigen Ordnern installieren</span><span class="sxs-lookup"><span data-stu-id="abc41-365">3.3 Install to Correct Folders</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-366">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-366">Windows 7</span></span><br/> <span data-ttu-id="abc41-367">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-367">Windows Vista</span></span><br/> <span data-ttu-id="abc41-368">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-368">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-369">Spiele müssen standardmäßig im Ordner "Programme" installiert werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-369">Games must be installed to the Program Files folder by default.</span></span> <span data-ttu-id="abc41-370">Benutzerdaten müssen bei der ersten Testlauf und nicht während der Installation geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-370">User data must be written at first run and not during the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="abc41-371">Installieren Sie das Spiel mit dem Standard Installationstyp.</span><span class="sxs-lookup"><span data-stu-id="abc41-371">Install the game using the Default install type.</span></span></li>
<li><span data-ttu-id="abc41-372">Vergewissern Sie sich, dass das Spiel für die Programmdateien installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="abc41-372">Verify that the game was installed to Program Files.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="abc41-373">Wenn bei diesem Test ein Fehler auftritt, überprüfen Sie, ob das Spiel für alle Benutzer installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="abc41-373">If this test fails, verify that the game is intended to install for All Users.</span></span> <span data-ttu-id="abc41-374">Wenn dies der Fall ist, ist dies ein Fehler.</span><span class="sxs-lookup"><span data-stu-id="abc41-374">If so, this is a failure.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a><span data-ttu-id="abc41-375">3,4 Windows-Ressourcen ordnungsgemäß installieren</span><span class="sxs-lookup"><span data-stu-id="abc41-375">3.4 Install Windows Resources Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-376">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-376">Windows 7</span></span><br/> <span data-ttu-id="abc41-377">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-377">Windows Vista</span></span><br/> <span data-ttu-id="abc41-378">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-378">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-379">Anwendungen dürfen nicht versuchen, Dateien oder Registrierungsschlüssel zu installieren, die durch Windows-Ressourcenschutz (WRP) geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="abc41-379">Applications must not attempt to install files or registry keys that are protected by Windows Resource Protection (WRP).</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="abc41-380">Vergewissern Sie sich, dass während des Installationsvorgangs keine Windows-Ressourcenschutz WRP-Dialogfelder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-380">Verify that no Windows Resource Protection WRP dialog boxes appear during the installation process.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a><span data-ttu-id="abc41-381">3,5 vermeiden Neustarts während der Installation</span><span class="sxs-lookup"><span data-stu-id="abc41-381">3.5 Avoid Reboots During Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-382">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-382">Windows 7</span></span><br/> <span data-ttu-id="abc41-383">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-383">Windows Vista</span></span><br/> <span data-ttu-id="abc41-384">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-384">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-385">Der Game Installer sollte nicht davon ausgehen, dass die Installation von Windows-Komponenten aus weitergabepaketen einen Neustart erfordert, es sei denn, der Neustart wird durch ein Rückgabe Ergebnis oder von der Microsoft-Dokumentation angegeben.</span><span class="sxs-lookup"><span data-stu-id="abc41-385">The game installer should not assume that installation of Windows components from redistribution packages requires a reboot, unless the reboot is indicated by a return result or by Microsoft documentation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="abc41-386">Installieren Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="abc41-386">Install the game.</span></span></li>
<li><span data-ttu-id="abc41-387">Vergewissern Sie sich, dass das System nach der Installation nicht neu gestartet werden muss.</span><span class="sxs-lookup"><span data-stu-id="abc41-387">Verify that the game does not require the system to be rebooted after installation.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="abc41-388">Wenn ein Microsoft System Update Redist einen Neustart erfordert, führen Sie die folgenden Schritte aus: Beenden Sie die Spiele Installation, deinstallieren Sie das Spiel, und installieren Sie das Spiel ein zweites Mal.</span><span class="sxs-lookup"><span data-stu-id="abc41-388">If a Microsoft system update REDIST requires a reboot, then do the following: Complete the game installation, uninstall the game, and reinstall the game a second time.</span></span> <span data-ttu-id="abc41-389">Bei der Installation des Spiels sollte bei dieser zweiten Installation kein Neustart erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="abc41-389">The game installation process should not require a reboot on this second installation.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a><span data-ttu-id="abc41-390">3,6 verwenden Sie die Datei Versionsverwaltung ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="abc41-390">3.6 Use File Versioning Correctly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-391">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-391">Windows 7</span></span><br/> <span data-ttu-id="abc41-392">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-392">Windows Vista</span></span><br/> <span data-ttu-id="abc41-393">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-393">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-394">Das Spiel Installationsprogramm muss ordnungsgemäß überprüft werden, um sicherzustellen, dass die aktuellsten Dateiversionen installiert sind.</span><span class="sxs-lookup"><span data-stu-id="abc41-394">The game installation program must properly check to ensure that the latest file versions are installed.</span></span> <span data-ttu-id="abc41-395">Bei der Installation eines Spiels dürfen keine Dateien erneut verwendet werden, die Sie nicht erstellt haben oder die von nicht erzeugten Anwendungen gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-395">Installing a game must never regress any files that you do not produce or that are shared by applications that you do not produce.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="abc41-396">Erstellen Sie vor der Installation des Spiels eine Vorinstallations Momentaufnahme von system32.</span><span class="sxs-lookup"><span data-stu-id="abc41-396">Prior to installing the game, create a pre-install snapshot of System32.</span></span><br/>
<ol>
<li><span data-ttu-id="abc41-397">Erstellen Sie ein Verzeichnis mit dem Namen G4Wtest.</span><span class="sxs-lookup"><span data-stu-id="abc41-397">Make a directory called G4Wtest.</span></span></li>
<li><span data-ttu-id="abc41-398">Öffnen Sie ein Befehlsfenster (Start-> Run-> cmd).</span><span class="sxs-lookup"><span data-stu-id="abc41-398">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="abc41-399">Navigieren Sie zu "c:\Windows\System32.".</span><span class="sxs-lookup"><span data-stu-id="abc41-399">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="abc41-400">Geben Sie dir/o:-g/o:-d >> c:\G4Wtest\pregame.txt ein.</span><span class="sxs-lookup"><span data-stu-id="abc41-400">Type dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt.</span></span></li>
</ol></li>
<li><span data-ttu-id="abc41-401">Erstellen Sie eine Momentaufnahme nach der Installation von system32.</span><span class="sxs-lookup"><span data-stu-id="abc41-401">Create a post-install snapshot of System32.</span></span> <br/>
<ol>
<li><span data-ttu-id="abc41-402">Öffnen Sie ein Befehlsfenster (Start-> Run-> cmd).</span><span class="sxs-lookup"><span data-stu-id="abc41-402">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="abc41-403">Navigieren Sie zu "c:\Windows\System32.".</span><span class="sxs-lookup"><span data-stu-id="abc41-403">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="abc41-404">Geben Sie dir/o:-g/o:-d >> c:\G4Wtest\postgame.txt ein.</span><span class="sxs-lookup"><span data-stu-id="abc41-404">Type dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt.</span></span></li>
<li><span data-ttu-id="abc41-405">Stellen Sie sicher, dass das Spiel keine Dateiversionen von Dateien, die das Spiel nicht erstellt hat (... der Dateien, die in den beiden Dokumenten aufgeführt sind, indem pregame.txt mit postgame.txt) verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-405">Verify that the game does not regress any file versions of files that the game did not produce (...of the files listed in the two documents by comparing pregame.txt to postgame.txt).</span></span></li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a><span data-ttu-id="abc41-406">3,7 Unterstützung für die bedingte Anforderung von Autorun \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-406">3.7 Support Autorun \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-407">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-407">Windows 7</span></span><br/> <span data-ttu-id="abc41-408">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-408">Windows Vista</span></span><br/> <span data-ttu-id="abc41-409">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-409">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-410">Bei spielen, die auf CD, DVD oder anderen Wechselmedien verteilt sind, die Autorun unterstützen, muss die Anwendung automatisch ausgeführt werden, um den Benutzer zur Installation des Spiels aufzufordern, wenn die Festplatte zum ersten Mal eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-410">For games distributed on CD, DVD, or other removable media that support Autorun, when the disc is inserted for the first time, the application must automatically run or prompt the user to install the game.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="abc41-411">Für autorun-Programme, die für Windows-Versionen vor Windows Vista geschrieben wurden, sollte die .NET-Laufzeit nicht verwendet werden, da diese Technologie nicht in Windows XP oder älteren Versionen von Windows enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="abc41-411">Autorun programs that were written for use on versions of Windows prior to Windows Vista should not use the .NET runtime, because this technology is not included with Windows XP or older versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="abc41-412">Weitere Anleitungen finden Sie unter <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3,7, Support Autorun.</span><span class="sxs-lookup"><span data-stu-id="abc41-412">For further guidance, please refer to <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3.7, Support Autorun.</span></span> <br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="abc41-413">Fügen Sie die Spiel-CD oder die Medien ein.</span><span class="sxs-lookup"><span data-stu-id="abc41-413">Insert the game disc or media.</span></span></li>
<li><span data-ttu-id="abc41-414">Überprüfen Sie, ob das Dialogfeld installieren/ausführen automatisch angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-414">Verify that the install / run dialog box comes up automatically.</span></span></li>
<li><span data-ttu-id="abc41-415">Windows Vista oder Windows 7: Vergewissern Sie sich, dass das Spiel Autorun-Programm selbst Benutzer Jane nicht auffordert, die Rechte über Administrator Anmelde Informationen zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="abc41-415">Windows Vista or Windows 7: Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials.</span></span></li>
<li><span data-ttu-id="abc41-416">Vergewissern Sie sich, dass die ausführbare Datei Autorun keine standardmäßig erforderlichen Redist-Komponenten wie .NET 3,5, C Run-Time-Bibliotheken usw. benötigt.</span><span class="sxs-lookup"><span data-stu-id="abc41-416">Verify that the Autorun executable doesn't need out-of-box REDIST components, such as .NET 3.5, C Run-Time libraries, and so on.</span></span></li>
<li><span data-ttu-id="abc41-417">Vergewissern Sie sich, dass die Installation des Laufwerks nach der Installation nicht automatisch startet.</span><span class="sxs-lookup"><span data-stu-id="abc41-417">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a><span data-ttu-id="abc41-418">4. Zuverlässigkeit</span><span class="sxs-lookup"><span data-stu-id="abc41-418">4. Reliability</span></span>

### <a name="41-eliminate-unnecessary-reboots"></a><span data-ttu-id="abc41-419">4,1 Entfernen unnötiger Neustarts</span><span class="sxs-lookup"><span data-stu-id="abc41-419">4.1 Eliminate Unnecessary Reboots</span></span>



|                                               |                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abc41-420">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-420">Windows 7</span></span><br/> <span data-ttu-id="abc41-421">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-421">Windows Vista</span></span><br/> | <span data-ttu-id="abc41-422">Alle Anwendungsinstallations Programme müssen die APIs für den Neustart-Manager nutzen, um Systemneustarts zu vermeiden (siehe [Anforderung 3,5](#35-avoid-reboots-during-installation)).</span><span class="sxs-lookup"><span data-stu-id="abc41-422">All application installers must take advantage of the Restart Manager APIs to avoid system reboots (see [requirement 3.5](#35-avoid-reboots-during-installation)).</span></span> |



 

### <a name="42-eliminate-application-verifier-failures"></a><span data-ttu-id="abc41-423">4,2 Vermeiden von Application Verifier Fehlern</span><span class="sxs-lookup"><span data-stu-id="abc41-423">4.2 Eliminate Application Verifier Failures</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-424">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-424">Windows 7</span></span><br/> <span data-ttu-id="abc41-425">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-425">Windows Vista</span></span><br/> <span data-ttu-id="abc41-426">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-426">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-427">Das Spiel muss in den folgenden Tests keine Fehler erzeugen, die unter Microsoft Application Verifier (AppVerifier), Version 4,0 oder höher, ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="abc41-427">The game must generate no failures running under Microsoft Application Verifier (AppVerifier), version 4.0 or later, in the following tests:</span></span> <br/>
<ul>
<li><span data-ttu-id="abc41-428">Grundlagen: Handles, Heaps, sperren, Arbeitsspeicher, TLS</span><span class="sxs-lookup"><span data-stu-id="abc41-428">Basics: Handles, Heaps, Locks, Memory, TLS</span></span></li>
<li><span data-ttu-id="abc41-429">Sonstige: dangerousapis, dirtystacks</span><span class="sxs-lookup"><span data-stu-id="abc41-429">Miscellaneous: DangerousAPIs, DirtyStacks</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="abc41-430">Tool verwenden: AppVerifier 4,0 (oder höher)</span><span class="sxs-lookup"><span data-stu-id="abc41-430">Use Tool: AppVerifier 4.0 (or later)</span></span><br/>
<ol>
<li><span data-ttu-id="abc41-431">Installieren Sie AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="abc41-431">Install AppVerifier.</span></span></li>
<li><span data-ttu-id="abc41-432">Starten Sie AppVerifier, und wählen Sie Datei-> Anwendung hinzufügen aus.</span><span class="sxs-lookup"><span data-stu-id="abc41-432">Launch AppVerifier and select File -> Add Application.</span></span></li>
<li><span data-ttu-id="abc41-433">Suchen Sie die ausführbare Datei, wählen Sie Sie aus, und klicken Sie auf die &quot; &quot; Schaltfläche Öffnen</span><span class="sxs-lookup"><span data-stu-id="abc41-433">Locate the game executable, select it, and click the &quot;Open&quot; button.</span></span></li>
<li><span data-ttu-id="abc41-434">&quot; &quot; Wählen Sie im Abschnitt Anwendungen die ausführbare Datei für das Spiel aus.</span><span class="sxs-lookup"><span data-stu-id="abc41-434">In the &quot;Applications&quot; section, select the game executable.</span></span></li>
<li><span data-ttu-id="abc41-435">&quot; &quot; Wählen Sie im Abschnitt Tests die oben aufgeführten Tests unter den Kategorien &quot; Grundlagen &quot; und &quot; Sonstiges aus &quot; (deaktivieren Sie Thread Pool und timerollover), und stellen Sie sicher, dass keine anderen Tests ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="abc41-435">In the &quot;Tests&quot; section, select the tests listed above under the categories &quot;Basics&quot; and &quot;Miscellaneous&quot; (uncheck ThreadPool and TimeRollOver), and ensure all other tests are not selected.</span></span></li>
<li><span data-ttu-id="abc41-436">Starten Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="abc41-436">Launch the game.</span></span></li>
<li><span data-ttu-id="abc41-437">Vergewissern Sie sich, dass das Spiel keine Fehler generiert, wenn es unter Application Verifier ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-437">Verify that the game does not generate failures when run under Application Verifier.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="abc41-438">Für einige Tests muss ein Debugger vollständig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-438">Some tests require a debugger to be fully run.</span></span> <span data-ttu-id="abc41-439">Dies erfordert möglicherweise eine ungeschützte Releaseversion der ausführbaren Datei des Spiels, da die Anticheat-/anticodeingtechnologie mit appverifer beeinträchtigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="abc41-439">This may require an unprotected release version of the game executable, since anti-cheat/anti-piracy technology may interfere with AppVerifer.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a><span data-ttu-id="abc41-440">4,3 Support Windows-Fehlerberichterstattung</span><span class="sxs-lookup"><span data-stu-id="abc41-440">4.3 Support Windows Error Reporting</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-441">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-441">Windows 7</span></span><br/> <span data-ttu-id="abc41-442">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-442">Windows Vista</span></span><br/> <span data-ttu-id="abc41-443">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-443">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-444">Spiele müssen nur bekannte Ausnahmen behandeln, und Windows-Fehlerberichterstattung dürfen nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-444">Games must handle only exceptions that are known and expected, and Windows Error Reporting must not be disabled.</span></span> <span data-ttu-id="abc41-445">Wenn ein Fehler (z. b. eine Zugriffsverletzung) in ein Spiel eingefügt wird, muss Windows-Fehlerberichterstattung den Absturz melden können.</span><span class="sxs-lookup"><span data-stu-id="abc41-445">If a fault (such as an Access Violation) is injected into a game, it must allow Windows Error Reporting to report the crash.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="abc41-446">Tool verwenden: Thread-Hijacker</span><span class="sxs-lookup"><span data-stu-id="abc41-446">Use Tool: Thread Hijacker</span></span> <br/>
<ul>
<li><span data-ttu-id="abc41-447">Wenn die Anwendung beim Testen abstürzt, vergewissern Sie sich, dass das Spiel Windows-Fehlerberichterstattung ordnungsgemäß angezeigt wird, und sammelt Absturz Daten.</span><span class="sxs-lookup"><span data-stu-id="abc41-447">If the application crashes while testing, verify that the game displays Windows Error Reporting properly and collects crash data.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-448">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-448">Windows 7</span></span><br/> <span data-ttu-id="abc41-449">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-449">Windows Vista</span></span><br/> <span data-ttu-id="abc41-450">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-450">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-451">Alle ausführbaren Dateien (z. b. exe-oder DLL-Dateien) müssen einen exakten Produktnamen, den Firmennamen und die Datei Version enthalten.</span><span class="sxs-lookup"><span data-stu-id="abc41-451">All executable files (for example, .exe or .dll files) must contain an accurate Product Name, Company Name, and File Version.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="abc41-452"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Manueller Test:</dt> </span><span class="sxs-lookup"><span data-stu-id="abc41-452"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Manual test:</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="abc41-453">Klicken Sie mit der rechten Maustaste auf die ausführbaren Dateien des Spiels auf den Installationsmedien und auf den Computern, die auf der Computer Festplatte installiert sind.</span><span class="sxs-lookup"><span data-stu-id="abc41-453">Right-click the game's executable file(s) on both the installation media and those installed to the computer hard drive.</span></span></li>
<li><span data-ttu-id="abc41-454">Wählen Sie „Eigenschaften“.</span><span class="sxs-lookup"><span data-stu-id="abc41-454">Select Properties.</span></span></li>
<li><span data-ttu-id="abc41-455">Windows XP: Klicken Sie auf die Registerkarte <strong>Version</strong> . Überprüfen Sie, ob die Felder Produktname, Firmenname und Datei Version ordnungsgemäß ausgefüllt sind.</span><span class="sxs-lookup"><span data-stu-id="abc41-455">Windows XP: Click the <strong>Version</strong> tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span></li>
<li><span data-ttu-id="abc41-456">Windows Vista oder Windows 7: Klicken Sie auf die Registerkarte <strong>Details</strong> . Überprüfen Sie, ob die Felder Product Name und File Version ordnungsgemäß aufgefüllt sind.</span><span class="sxs-lookup"><span data-stu-id="abc41-456">Windows Vista or Windows 7: Click the <strong>Details</strong> tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="abc41-457">Der Name des Unternehmens ist auf der Eigenschaften Seite von Windows Vista oder Windows 7 nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="abc41-457">Company Name is not visible in the Windows Vista or Windows 7 properties page.</span></span></li>
</ol>
</dd> <span data-ttu-id="abc41-458"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Automatisierter Test:</dt> </span><span class="sxs-lookup"><span data-stu-id="abc41-458"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Automated test:</dt> </span></span><dd>
<ul>
<li><span data-ttu-id="abc41-459">Verwenden Sie das Microsoft Games for Windows-Testtool; siehe <a href="#64-microsoft-games-for-windows-test-tool">Abschnitt 6,4</a>.</span><span class="sxs-lookup"><span data-stu-id="abc41-459">Use the Microsoft Games for Windows Test Tool; see <a href="#64-microsoft-games-for-windows-test-tool">section 6.4</a>.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abc41-460">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-460">Windows 7</span></span><br/> <span data-ttu-id="abc41-461">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abc41-461">Windows Vista</span></span><br/> <span data-ttu-id="abc41-462">Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-462">Windows XP</span></span><br/></td>
<td><span data-ttu-id="abc41-463">Der normale Beenden des Spiels darf keinen unbekannten Ausnahme Fehler verursachen.</span><span class="sxs-lookup"><span data-stu-id="abc41-463">Normal exit of the game must not result in an unknown exception fault.</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="abc41-464">Nachdem Sie das Spiel für eine normale Gaming-Sitzung abgespielt haben, stellen Sie sicher, dass das Spiel beim Beenden keine Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="abc41-464">After playing the game for a normal gaming session, verify that the game does not generate errors on exit.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a><span data-ttu-id="abc41-465">5. Beispiel Test Skript</span><span class="sxs-lookup"><span data-stu-id="abc41-465">5. Sample Test Script</span></span>

<span data-ttu-id="abc41-466">Dies ist ein Beispiel für einen typischen Test Durchlauf, bei dem die vorangehenden Testanforderungen als Leitfaden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-466">This is an example of a typical test pass using the preceding test requirements as a guide.</span></span>

### <a name="51-tools"></a><span data-ttu-id="abc41-467">5,1-Tools</span><span class="sxs-lookup"><span data-stu-id="abc41-467">5.1 Tools</span></span>

-   <span data-ttu-id="abc41-468">32-Bit-Edition von Windows Vista SP1 und/oder Windows 7 auf einer AMD-CPU</span><span class="sxs-lookup"><span data-stu-id="abc41-468">32-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="abc41-469">32-Bit-Edition von Windows Vista SP1 und/oder Windows 7 auf einer Intel-CPU</span><span class="sxs-lookup"><span data-stu-id="abc41-469">32-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="abc41-470">64-Bit-Edition von Windows Vista SP1 und/oder Windows 7 auf einer AMD-CPU</span><span class="sxs-lookup"><span data-stu-id="abc41-470">64-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="abc41-471">64-Bit-Edition von Windows Vista SP1 und/oder Windows 7 auf einer Intel-CPU</span><span class="sxs-lookup"><span data-stu-id="abc41-471">64-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="abc41-472">32-Bit Edition Windows XP SP2 auf einer AMD-CPU</span><span class="sxs-lookup"><span data-stu-id="abc41-472">32-bit edition Windows XP SP2 on an AMD CPU</span></span>
-   <span data-ttu-id="abc41-473">32-Bit Edition Windows XP SP2 auf einer Intel CPU</span><span class="sxs-lookup"><span data-stu-id="abc41-473">32-bit edition Windows XP SP2 on an Intel CPU</span></span>
-   <span data-ttu-id="abc41-474">Monitor für Breite Bildschirm, der 1680 1050 unterstützt</span><span class="sxs-lookup"><span data-stu-id="abc41-474">Wide Screen Monitor that supports 1680 1050</span></span>
-   <span data-ttu-id="abc41-475">Xbox 360-Controller für Windows</span><span class="sxs-lookup"><span data-stu-id="abc41-475">Xbox 360 Controller for Windows</span></span>

### <a name="52-pre-install"></a><span data-ttu-id="abc41-476">5,2 vor der Installation</span><span class="sxs-lookup"><span data-stu-id="abc41-476">5.2 Pre-Install</span></span>

1.  <span data-ttu-id="abc41-477">Windows Vista und Windows 7: Erstellen Sie zwei Standard Benutzer: Jane und Deby</span><span class="sxs-lookup"><span data-stu-id="abc41-477">Windows Vista and Windows 7: Create two Standard Users: Jane and Toby</span></span>
2.  <span data-ttu-id="abc41-478">Windows Vista und Windows 7: Stellen Sie sicher, dass die Benutzerkontensteuerung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="abc41-478">Windows Vista and Windows 7: Ensure User Account Control is enabled</span></span>
3.  <span data-ttu-id="abc41-479">Erstellen einer Vorinstallations Momentaufnahme von system32</span><span class="sxs-lookup"><span data-stu-id="abc41-479">Create a pre-install snapshot of System32</span></span>

    1.  <span data-ttu-id="abc41-480">Erstellen Sie ein Verzeichnis mit dem Namen G4Wtest</span><span class="sxs-lookup"><span data-stu-id="abc41-480">Make a directory called G4Wtest</span></span>
    2.  <span data-ttu-id="abc41-481">Öffnen Sie ein Befehlsfenster (Start-> Run-> cmd).</span><span class="sxs-lookup"><span data-stu-id="abc41-481">Bring up a command Window (Start -> Run -> cmd)</span></span>
    3.  <span data-ttu-id="abc41-482">Navigieren Sie zu "c: \\ Windows System32". \\</span><span class="sxs-lookup"><span data-stu-id="abc41-482">Navigate to c:\\windows\\system32</span></span>
    4.  <span data-ttu-id="abc41-483">Geben Sie dir/o:-g/o:-d >> c: \\ G4Wtest \\pregame.txt</span><span class="sxs-lookup"><span data-stu-id="abc41-483">Type dir /o:-g /o:-d >> c:\\G4Wtest\\pregame.txt</span></span>

4.  <span data-ttu-id="abc41-484">Windows Vista und Windows 7: auf 150% dpi \[ 1,8 festlegen\]</span><span class="sxs-lookup"><span data-stu-id="abc41-484">Windows Vista and Windows 7: Set to 150% DPI \[1.8\]</span></span>
5.  <span data-ttu-id="abc41-485">Mit der [Installation](#3-installation) fortfahren</span><span class="sxs-lookup"><span data-stu-id="abc41-485">Proceed to [Install](#3-installation)</span></span>

### <a name="53-install"></a><span data-ttu-id="abc41-486">5,3-Installation</span><span class="sxs-lookup"><span data-stu-id="abc41-486">5.3 Install</span></span>

1.  <span data-ttu-id="abc41-487">Anmelden als Benutzer Jane</span><span class="sxs-lookup"><span data-stu-id="abc41-487">Log on as User Jane</span></span>
2.  <span data-ttu-id="abc41-488">Legen Sie den Spiel Datenträger in das CD/DVD-Laufwerk ein, vergewissern Sie sich, dass das Dialogfeld installieren/ausführen automatisch angezeigt wird \[ 3,7\]</span><span class="sxs-lookup"><span data-stu-id="abc41-488">Insert the game disc into the CD/DVD drive, verify that the install / run dialog box comes up automatically \[3.7\]</span></span>
3.  <span data-ttu-id="abc41-489">Vergewissern Sie sich, dass der Spiel Installationsprozess Benutzer Jane auffordert, Administrator Anmelde Informationen zu erhöhen \[ 3,2\]</span><span class="sxs-lookup"><span data-stu-id="abc41-489">Verify that the game installation process prompts User Jane to elevate Administrator Credentials \[3.2\]</span></span>
4.  <span data-ttu-id="abc41-490">Stellen Sie sicher, dass das Spiel Autorun-Programm selbst Benutzer Jane nicht auffordert, die Rechte über Administrator Anmelde Informationen zu erhöhen \[ 3,7\]</span><span class="sxs-lookup"><span data-stu-id="abc41-490">Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials \[3.7\]</span></span>
5.  <span data-ttu-id="abc41-491">Vergewissern Sie sich, dass das Spiel nicht mehr als einen End-User Lizenzvertrag (EULA) 3,1 anzeigt. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-491">Verify that the game does not display more than one End-User License Agreement (EULA) \[3.1\]</span></span>
6.  <span data-ttu-id="abc41-492">Stellen Sie sicher, dass das Spiel die Optionen default/Easy und Custom/Advanced Installation \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="abc41-492">Verify that the game displays Default/Easy and Custom/Advanced installation options \[3.1\]</span></span>
7.  <span data-ttu-id="abc41-493">Vergewissern Sie sich, dass die Option Standard/einfache Installation alle Benutzereingabe-Auswahl Optionen für den Installationsvorgang umgeht (Auswahl von Installationsordner, Komponentenauswahl usw.) \[ . 3,1\]</span><span class="sxs-lookup"><span data-stu-id="abc41-493">Verify that the Default/Easy installation option bypasses all user input selections for the install process (selection of installation folder, components selection, and so on.) \[3.1\]</span></span>
8.  <span data-ttu-id="abc41-494">Vergewissern Sie sich, dass bei der Spiele Installation keine Eingabeaufforderung für das Setup der Betriebssystem Komponente (DirectX-Setup, C Run-Time-Bibliotheken usw.) \[ angezeigt wird. 3,1\]</span><span class="sxs-lookup"><span data-stu-id="abc41-494">Verify that the game installation process does not prompt for OS component setup (DirectX setup, C Run-Time libraries, and so on.) \[3.1\]</span></span>
9.  <span data-ttu-id="abc41-495">Stellen Sie sicher, dass bei der Spiele Installation keine Aufforderung zur firewallinteraktion 3,1 angezeigt wird. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-495">Verify that the game installation process does not prompt for firewall interaction \[3.1\]</span></span>
10. <span data-ttu-id="abc41-496">Vergewissern Sie sich, dass bei der Spiele Installation kein Fehler in Bezug auf die Betriebssystem Version \[ 2,5 \] \[ 4,2 auftritt.\]</span><span class="sxs-lookup"><span data-stu-id="abc41-496">Verify that the game installation process does not encounter an error regarding OS Version \[2.5\] \[4.2\]</span></span>
11. <span data-ttu-id="abc41-497">Stellen Sie sicher, dass bei der Spiele Installation nicht signierte Treiber Dialog (e) 2,4 angezeigt werden. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-497">Verify that the game installation process does not display unsigned driver dialog(s) \[2.4\]</span></span>
12. <span data-ttu-id="abc41-498">Vergewissern Sie sich, dass während des Installationsvorgangs 3,4 keine Windows-Ressourcenschutz (WRP)-Dialogfelder angezeigt werden. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-498">Verify that no Windows Resource Protection (WRP) dialogs appear during the install process \[3.4\]</span></span>
13. <span data-ttu-id="abc41-499">Vergewissern Sie sich, dass die Installation des Laufwerks nach der Installation nicht automatisch startet.</span><span class="sxs-lookup"><span data-stu-id="abc41-499">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again</span></span>
14. <span data-ttu-id="abc41-500">Vergewissern Sie sich, dass das System nach der Installation 3,5 nicht neu gestartet werden muss. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-500">Verify that the game does not require the system to be rebooted after installation \[3.5\]</span></span>
15. <span data-ttu-id="abc41-501">Vergewissern Sie sich, dass Sie das Spiel als Benutzer Jane 3,2 installieren können. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-501">Verify that you can install the game as User Jane \[3.2\]</span></span>
16. <span data-ttu-id="abc41-502">Überprüfen Sie, ob das Spiel automatisch ausgeführt wird oder ob ein Start Programm Menü am Ende des Installationsvorgangs 3,1 vorhanden ist. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-502">Verify that the game automatically runs or that a launcher menu is present at the end of the installation process \[3.1\]</span></span>
17. <span data-ttu-id="abc41-503">Wenn das Spiel nach der Installation automatisch ausgeführt wird, springen Sie zur [Laufzeit](#55-runtime) .</span><span class="sxs-lookup"><span data-stu-id="abc41-503">If the game does auto-run after installation, skip to [Runtime](#55-runtime)</span></span>
18. <span data-ttu-id="abc41-504">Wenn das Spiel ein Startmenü geöffnet hat oder die Deinstallation fehlgeschlagen ist, lesen Sie den Abschnitt [nach der Installation](#54-post-install) .</span><span class="sxs-lookup"><span data-stu-id="abc41-504">If the game left a launch menu up, or failed to uninstall see section [Post-Install](#54-post-install)</span></span>

### <a name="54-post-install"></a><span data-ttu-id="abc41-505">5,4 nach der Installation</span><span class="sxs-lookup"><span data-stu-id="abc41-505">5.4 Post-Install</span></span>

1.  <span data-ttu-id="abc41-506">Stellen Sie sicher, dass das Spiel keine Start Verknüpfungen auf dem Benutzer Desktop 1,1 platziert. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-506">Verify that the game does not place launch shortcuts on user desktop \[1.1\]</span></span>
2.  <span data-ttu-id="abc41-507">Stellen Sie sicher, dass das Spiel keine Start Verknüpfungen im Startmenü \[ 1,1.\]</span><span class="sxs-lookup"><span data-stu-id="abc41-507">Verify that the game does not place launch shortcuts in the Start Menu \[1.1\]</span></span>
3.  <span data-ttu-id="abc41-508">Überprüfen Sie, ob das Spiel Symbol in Windows Games Explorer 1,1 angezeigt wird. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-508">Verify that the game icon displays in Windows Games Explorer \[1.1\]</span></span>
4.  <span data-ttu-id="abc41-509">Vergewissern Sie sich, dass die Metadaten (Verleger, Entwickler, Genre, Veröffentlichungsdatum, Version) unten angezeigt werden und korrekt \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="abc41-509">Verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct \[1.1\]</span></span>
5.  <span data-ttu-id="abc41-510">Überprüfen Sie, ob das Symbol "Spiel" Informationen zum Windows-Erfahrungs Index (Wei) in Windows Games Explorer \[ 1,1 anzeigt\]</span><span class="sxs-lookup"><span data-stu-id="abc41-510">Verify that the game icon displays Windows Experience Index (WEI) information in Windows Games Explorer \[1.1\]</span></span>
6.  <span data-ttu-id="abc41-511">Überprüfen Sie, ob die Spiel Hyperlinks für Metadaten in Windows Games Explorer 1,1 ordnungsgemäß funktionieren. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-511">Verify that game hyperlinks for metadata work correctly in Windows Games Explorer \[1.1\]</span></span>
7.  <span data-ttu-id="abc41-512">Stellen Sie sicher, dass das Spiel in Windows Games Explorer 1,1 eine genaue Bewertung der Jugend Steuerung anzeigt. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-512">Verify that the game displays accurate parental control rating in Windows Games Explorer \[1.1\]</span></span>
8.  <span data-ttu-id="abc41-513">Erstellen einer nach Installations Momentaufnahme von system32</span><span class="sxs-lookup"><span data-stu-id="abc41-513">Create a post-install snapshot of System32</span></span>

    1.  <span data-ttu-id="abc41-514">Öffnen Sie ein Befehlsfenster (Start-> Run-> cmd).</span><span class="sxs-lookup"><span data-stu-id="abc41-514">Bring up a command Window (Start -> Run -> cmd)</span></span>
    2.  <span data-ttu-id="abc41-515">Navigieren Sie zu "c: \\ Windows System32". \\</span><span class="sxs-lookup"><span data-stu-id="abc41-515">Navigate to c:\\windows\\system32</span></span>
    3.  <span data-ttu-id="abc41-516">Geben Sie dir/o:-g/o:-d >> c: \\ G4Wtest \\postgame.txt</span><span class="sxs-lookup"><span data-stu-id="abc41-516">Type dir /o:-g /o:-d >> c:\\G4Wtest\\postgame.txt</span></span>
    4.  <span data-ttu-id="abc41-517">Stellen Sie sicher, dass das Spiel keine Dateiversionen von Dateien, die in den beiden Dokumenten aufgeführt sind, wiederholt, indem Sie pregame.txt mit postgame.txt 3,6 vergleichen. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-517">Verify that the game does not regress any file versions of files listed in the two documents by comparing pregame.txt to postgame.txt \[3.6\]</span></span>

9.  <span data-ttu-id="abc41-518">Zur [Laufzeit](#55-runtime) fortfahren</span><span class="sxs-lookup"><span data-stu-id="abc41-518">Proceed to [Runtime](#55-runtime)</span></span>

### <a name="55-runtime"></a><span data-ttu-id="abc41-519">5,5-Laufzeit</span><span class="sxs-lookup"><span data-stu-id="abc41-519">5.5 Runtime</span></span>

1.  <span data-ttu-id="abc41-520">Laufzeit 1: Wenn das Startmenü vorhanden ist, starten Sie das Spiel von dort aus.</span><span class="sxs-lookup"><span data-stu-id="abc41-520">RUNTIME 1: If the launch menu is present, launch the game from there.</span></span> <span data-ttu-id="abc41-521">Wenn das Spiel automatisch ausgeführt wurde oder nach der Installation über das Spiel Startmenü gestartet wurde, führen Sie Folgendes aus: Wenn nicht, fahren Sie mit Laufzeit 2 fort:</span><span class="sxs-lookup"><span data-stu-id="abc41-521">If the game auto-ran or was launched from the game launcher menu after install, perform the following; if not, skip to RUNTIME 2:</span></span>

    1.  <span data-ttu-id="abc41-522">Erstellen eines Profils (wenn das Spiel zulässt)</span><span class="sxs-lookup"><span data-stu-id="abc41-522">Create a profile (if the game allows)</span></span>
    2.  <span data-ttu-id="abc41-523">Neues Spiel starten</span><span class="sxs-lookup"><span data-stu-id="abc41-523">Start a new game</span></span>
    3.  <span data-ttu-id="abc41-524">Speichern des Spiels</span><span class="sxs-lookup"><span data-stu-id="abc41-524">Save the game</span></span>
    4.  <span data-ttu-id="abc41-525">Beenden des Spiels</span><span class="sxs-lookup"><span data-stu-id="abc41-525">Exit the game</span></span>
    5.  <span data-ttu-id="abc41-526">Starten Sie das Spiel im Spiele-Explorer.</span><span class="sxs-lookup"><span data-stu-id="abc41-526">Launch the game from Games Explorer</span></span>
    6.  <span data-ttu-id="abc41-527">Überprüfen Sie, ob das Spiel über das 1,2 Symbol "Games Explorer" gestartet wird \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-527">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    7.  <span data-ttu-id="abc41-528">Stellen Sie sicher, dass das Spiel beim Start 1,2 keine Administrator Anmelde Informationen auffordert. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-528">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    8.  <span data-ttu-id="abc41-529">Stellen Sie sicher, dass Benutzer Jane Account 3,2 auf Benutzerprofile und Save Games zugreifen können. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-529">Verify that User Profiles and Save Games can be accessed by User Jane account \[3.2\]</span></span>
    9.  <span data-ttu-id="abc41-530">Mit Laufzeit 3 fortfahren</span><span class="sxs-lookup"><span data-stu-id="abc41-530">Proceed to RUNTIME 3</span></span>

2.  <span data-ttu-id="abc41-531">Laufzeit 2: Wenn das Spiel nicht automatisch ausgeführt wurde oder einen Start über das Spiel Startmenü anzeigt, ist dies ein Fehler von \[ 3,1 \] ; das Testen kann jedoch normal fortgesetzt werden:</span><span class="sxs-lookup"><span data-stu-id="abc41-531">RUNTIME 2: If the game did not auto-run or display a launch from the game launcher menu, this is a failure of \[3.1\]; however, testing can continue normally:</span></span>

    1.  <span data-ttu-id="abc41-532">Starten Sie das Spiel im Spiele-Explorer.</span><span class="sxs-lookup"><span data-stu-id="abc41-532">Launch the game from Games Explorer</span></span>
    2.  <span data-ttu-id="abc41-533">Überprüfen Sie, ob das Spiel über das 1,2 Symbol "Games Explorer" gestartet wird \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-533">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    3.  <span data-ttu-id="abc41-534">Stellen Sie sicher, dass das Spiel beim Start 1,2 keine Administrator Anmelde Informationen auffordert. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-534">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    4.  <span data-ttu-id="abc41-535">Mit Laufzeit 3 fortfahren</span><span class="sxs-lookup"><span data-stu-id="abc41-535">Proceed to RUNTIME 3</span></span>

3.  <span data-ttu-id="abc41-536">Laufzeit 3: Wenn das Spiel einen Spielblock unterstützt, vergewissern Sie sich, dass das Spiel Xbox 360-Controller für Windows als Eingabegerät (1,4) erkennt. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-536">RUNTIME 3: If the game supports a game pad, verify that the game recognizes Xbox 360 Controller for Windows as an input device \[1.4\]</span></span>

    1.  <span data-ttu-id="abc41-537">Aktivieren Sie den Controller bei Bedarf über das Menü "Optionen".</span><span class="sxs-lookup"><span data-stu-id="abc41-537">If needed, enable the controller via the options menu</span></span>
    2.  <span data-ttu-id="abc41-538">Stellen Sie sicher, dass das Spiel auf die Controller Schaltflächen und Trigger mit Xbox 360-Namen verweist.</span><span class="sxs-lookup"><span data-stu-id="abc41-538">Verify that the game refers to the controller buttons and triggers using Xbox 360 names</span></span>
    3.  <span data-ttu-id="abc41-539">Überprüfen Sie, ob das Spiel und das Menüsystem mit dem Xbox 360-Controller für Windows steuerbar sind.</span><span class="sxs-lookup"><span data-stu-id="abc41-539">Verify that the game and menu system are controllable with the Xbox 360 Controller for Windows</span></span>
    4.  <span data-ttu-id="abc41-540">Stellen Sie sicher, dass sich der Xbox 360-Controller für Windows gemäß den akzeptierten Standards verhält.</span><span class="sxs-lookup"><span data-stu-id="abc41-540">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards</span></span>

4.  <span data-ttu-id="abc41-541">Legen Sie das Video auf \[ 1,5 fest \] :</span><span class="sxs-lookup"><span data-stu-id="abc41-541">Set the video to \[1.5\]:</span></span>

    1.  <span data-ttu-id="abc41-542">Überprüfen Sie, ob das Spiel bei einer 4:3-Seitenverhältnis Auflösung (800 600 oder 1024 768) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-542">Verify that the game runs at a 4:3 Aspect Ratio resolution (800 600 or 1024 768)</span></span>
    2.  <span data-ttu-id="abc41-543">Überprüfen Sie, ob das Spiel bei einer 16:9-Seitenverhältnis Auflösung (1280 720) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-543">Verify that the game runs at a 16:9 Aspect Ratio resolution (1280 720)</span></span>
    3.  <span data-ttu-id="abc41-544">Überprüfen Sie, ob das Spiel bei einer 16:10-Seitenverhältnis Auflösung (1680 1050, 800 480 oder 1152 720) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-544">Verify that the game runs at a 16:10 Aspect Ratio resolution (1680 1050, 800 480, or 1152 720)</span></span>
    4.  <span data-ttu-id="abc41-545">Überprüfen Sie, ob das Spiel den Benutzer auffordert, wenn eine Änderung an der Auflösung vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-545">Verify that the game prompts the user when a change is made to the resolution</span></span>
    5.  <span data-ttu-id="abc41-546">Vergewissern Sie sich, dass die Anzeige auf die vorherige Einstellung zurückgesetzt wird, wenn Sie Sie nicht innerhalb von 15 Sekunden akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="abc41-546">Verify that the display reverts to the previous setting if you do not accept within 15 seconds</span></span>
    6.  <span data-ttu-id="abc41-547">Stellen Sie sicher, dass das Spiel das Bild nicht gestreckt und wiederum einen breiteren Bereich der Ansicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="abc41-547">Verify that the game does not stretch the picture and in turn presents a wider area of view</span></span>
    7.  <span data-ttu-id="abc41-548">Stellen Sie sicher, dass das Spiel keine schwarzen Balken Links und rechts im Spielbereich des Spiels hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="abc41-548">Verify that the game does not add black bars to the left and right of the game play area</span></span>

5.  <span data-ttu-id="abc41-549">Wenn Sie in den Videoeinstellungen verfügbar sind, überprüfen Sie, ob die Optionen für das spielrendering standardmäßig Direct3D \[ 1,7 sind \] ; andernfalls fahren Sie mit [automatisierte Tests](#58-automated-tests) fort</span><span class="sxs-lookup"><span data-stu-id="abc41-549">If available in the video settings, verify that the game render options default to Direct3D \[1.7\]; otherwise, proceed to [Automated Tests](#58-automated-tests)</span></span>
6.  <span data-ttu-id="abc41-550">Wenn Sie dazu aufgefordert werden oder wenn die Option verfügbar ist, erstellen Sie ein Benutzerprofil.</span><span class="sxs-lookup"><span data-stu-id="abc41-550">If prompted or if the option is available, create a user profile.</span></span> <span data-ttu-id="abc41-551">Stellen Sie sicher, dass für das Spiel keine Fehler auftreten, wenn Sie lange Dateinamen 2,7 verwenden. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-551">Verify that the game does not encounter errors when using long file names \[2.7\]</span></span>
7.  <span data-ttu-id="abc41-552">Starten Sie ein neues Spiel, erstellen Sie ein Spiel, und stellen Sie sicher, dass das Spiel bei der Behandlung nicht unterstützter Dateisystem Zeichen nicht fehlerhaft ist \[ 2,7\]</span><span class="sxs-lookup"><span data-stu-id="abc41-552">Start a new game, create a game save, and verify that the game does not encounter errors when handling unsupported file system characters \[2.7\]</span></span>
8.  <span data-ttu-id="abc41-553">Überprüfen Sie, ob das Spiel ordnungsgemäß alt + Tabstopps zum Windows-Desktop \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="abc41-553">Verify that the game properly ALT+TABs to the Windows desktop \[2.6\]</span></span>

    1.  <span data-ttu-id="abc41-554">Benutzer mit dem Spiel wechseln, indem Sie auf Start > Switch-Benutzer klicken</span><span class="sxs-lookup"><span data-stu-id="abc41-554">Switch users with the game running by clicking Start -> Switch User</span></span>
    2.  <span data-ttu-id="abc41-555">Anmelden als Toby</span><span class="sxs-lookup"><span data-stu-id="abc41-555">Log on as Toby</span></span>
    3.  <span data-ttu-id="abc41-556">Stellen Sie sicher, dass das Spiel als Benutzer-zu-Ende gestartet wird, während es weiterhin als Benutzer Jane \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="abc41-556">Verify that the game launches as User Toby while still running as User Jane \[2.6\]</span></span>
    4.  <span data-ttu-id="abc41-557">Stellen Sie sicher, dass das Spiel während des Benutzer Umschalters nicht Fehler für Benutzer-oder Benutzer-Jane-Vorgang \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="abc41-557">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process \[2.6\]</span></span>
    5.  <span data-ttu-id="abc41-558">Vergewissern Sie sich, dass Sie Audiodaten aus der ursprünglichen Spielsitzung 2,6 nicht hören können. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-558">Verify that you cannot hear audio from the original game session \[2.6\]</span></span>
    6.  <span data-ttu-id="abc41-559">Beenden des Spiels</span><span class="sxs-lookup"><span data-stu-id="abc41-559">Exit the game</span></span>
    7.  <span data-ttu-id="abc41-560">Abmelden bei Toby</span><span class="sxs-lookup"><span data-stu-id="abc41-560">Log off Toby</span></span>
    8.  <span data-ttu-id="abc41-561">Wechseln Sie zurück zum ursprünglichen Benutzer, auf dem das Spiel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-561">Switch back to the original user where the game is running</span></span>
    9.  <span data-ttu-id="abc41-562">Alt + Tab zurück zum Spiel</span><span class="sxs-lookup"><span data-stu-id="abc41-562">ALT+TAB back into the game</span></span>

9.  <span data-ttu-id="abc41-563">Beenden des Spiels</span><span class="sxs-lookup"><span data-stu-id="abc41-563">Exit the game</span></span>
10. <span data-ttu-id="abc41-564">Mit der [Post-Laufzeit](#56-post-runtime) fortfahren</span><span class="sxs-lookup"><span data-stu-id="abc41-564">Proceed to [Post-Runtime](#56-post-runtime)</span></span>

### <a name="56-post-runtime"></a><span data-ttu-id="abc41-565">5,6 nach der Laufzeit</span><span class="sxs-lookup"><span data-stu-id="abc41-565">5.6 Post-Runtime</span></span>

1.  <span data-ttu-id="abc41-566">Stellen Sie sicher, dass das Spiel bei Exit 4,3 keine Fehler generiert. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-566">Verify that the game does not generate errors on exit \[4.3\]</span></span>
2.  <span data-ttu-id="abc41-567">Überprüfen Sie, ob das auf den Programmdateien 3,3 installierte Spiel \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-567">Verify that the game installed to Program Files \[3.3\]</span></span>
3.  <span data-ttu-id="abc41-568">Mit [Eltern Steuerungs](/windows) Maßnahmen fortfahren</span><span class="sxs-lookup"><span data-stu-id="abc41-568">Proceed to [Parental Controls](/windows)</span></span>

### <a name="57-parental-controls"></a><span data-ttu-id="abc41-569">5,7 Eltern Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="abc41-569">5.7 Parental Controls</span></span>

1.  <span data-ttu-id="abc41-570">Öffnen Sie in der Systemsteuerung die Option Jugendschutz</span><span class="sxs-lookup"><span data-stu-id="abc41-570">Open Parental Controls in Control Panel</span></span>
2.  <span data-ttu-id="abc41-571">Stellen Sie sicher, dass das Spiel unter dem Spieltitel in der Systemsteuerung \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="abc41-571">Verify that the game displays accurate Parental Control Rating below the game title in Parental Controls Control Panel \[1.2\]</span></span>
3.  <span data-ttu-id="abc41-572">Weitere Informationen finden Sie unter Testfall \[ 1,2 \] für die folgenden Tests:</span><span class="sxs-lookup"><span data-stu-id="abc41-572">See Test Case \[1.2\] for the following tests:</span></span>

    1.  <span data-ttu-id="abc41-573">Überprüfen Sie nach dem Festlegen der Jugend Steuerelemente auf "ein", ob das Spiel mit diesen Einstellungen ausgeführt wird, als Benutzer Jane \[ 1,2.\]</span><span class="sxs-lookup"><span data-stu-id="abc41-573">After setting Parental Controls to "On", verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    2.  <span data-ttu-id="abc41-574">Abmelden und Anmelden als Toby</span><span class="sxs-lookup"><span data-stu-id="abc41-574">Log off and log on as Toby</span></span>
    3.  <span data-ttu-id="abc41-575">Stellen Sie sicher, dass das Spiel mit diesen Einstellungen als Benutzer-/1,2 ausgeführt wird. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-575">Verify that the game runs with these settings as User Toby \[1.2\]</span></span>
    4.  <span data-ttu-id="abc41-576">Melden Sie sich ab, und melden Sie sich als Jane an</span><span class="sxs-lookup"><span data-stu-id="abc41-576">Log off and log on as Jane</span></span>
    5.  <span data-ttu-id="abc41-577">Blockieren Sie im Abschnitt "Jugendschutz" den Benutzer damit, dass Spiele eine ESRB-Ebene von dem soeben installierten Spiel sehen.</span><span class="sxs-lookup"><span data-stu-id="abc41-577">In the Parental Control section, block User Toby from seeing games one ESRB level up and higher from the game that you just installed</span></span>

        <span data-ttu-id="abc41-578">Beispiel: Wenn das Spiel mit E bewertet wird, legen Sie es so fest, dass "tby" nur Spiele abspielen kann, die als "C</span><span class="sxs-lookup"><span data-stu-id="abc41-578">Example: If the game is rated E, set it so Toby can only play games that are rated C</span></span>

    6.  <span data-ttu-id="abc41-579">Überprüfen Sie, ob das Spiel mit diesen Einstellungen ausgeführt wird, als Benutzer Jane \[ 1,2.\]</span><span class="sxs-lookup"><span data-stu-id="abc41-579">Verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    7.  <span data-ttu-id="abc41-580">Melden Sie sich ab, und melden Sie sich als Benutzer Toby an</span><span class="sxs-lookup"><span data-stu-id="abc41-580">Log off and log on as user Toby</span></span>
    8.  <span data-ttu-id="abc41-581">Stellen Sie sicher, dass das Spiel nicht für Benutzer "Deby" gestartet wird, wenn ESRB durch den Benutzer Jane 1,2 blockiert wird. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-581">Verify that the game does not launch on User Toby when ESRB is blocked by User Jane \[1.2\]</span></span>
    9.  <span data-ttu-id="abc41-582">Melden Sie sich als Benutzer Toby und wieder als Benutzer Jane an.</span><span class="sxs-lookup"><span data-stu-id="abc41-582">Log off as user Toby and back on as user Jane</span></span>
    10. <span data-ttu-id="abc41-583">Stellen Sie die ESRB-Einstellungen wieder her</span><span class="sxs-lookup"><span data-stu-id="abc41-583">If changed previously, restore the ESRB settings</span></span>
    11. <span data-ttu-id="abc41-584">Wenn keine ESRB-Einstellungen vorhanden sind, wählen Sie "bestimmte Spiele blockieren oder zulassen" aus, und wählen Sie das Spiel nach Name aus.</span><span class="sxs-lookup"><span data-stu-id="abc41-584">If there are no ESRB settings, then select "Block or Allow Specific Games" and select the game by name</span></span>
    12. <span data-ttu-id="abc41-585">Melden Sie sich als Andrea und als Toby ab.</span><span class="sxs-lookup"><span data-stu-id="abc41-585">Log off as Jane and on as Toby</span></span>
    13. <span data-ttu-id="abc41-586">Stellen Sie sicher, dass das Spiel nicht für Benutzer "Deby" gestartet wird, wenn "exe/Name" vom Benutzer Jane 1,2 blockiert wird \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-586">Verify that the game does not launch on User Toby when EXE/Name is blocked by User Jane \[1.2\]</span></span>
    14. <span data-ttu-id="abc41-587">Melden Sie sich als "Toby" und "zurück" als Andrea an</span><span class="sxs-lookup"><span data-stu-id="abc41-587">Log off as Toby and back on as Jane</span></span>
    15. <span data-ttu-id="abc41-588">Als Andrea öffnen Sie die Benutzer Steuerelemente > Anwendungs Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="abc41-588">As Jane, open User Controls -> Application Restrictions</span></span>
    16. <span data-ttu-id="abc41-589">Klicken Sie auf "auf" kann nur die von mir zugelassenen Programme verwendet werden ", und klicken Sie dann auf" OK "(keine exe-Datei zulassen).</span><span class="sxs-lookup"><span data-stu-id="abc41-589">Click "Toby can only use the programs I allow", and then click OK (i.e. allow no exes)</span></span>
    17. <span data-ttu-id="abc41-590">Aktivieren Sie das Kontrollkästchen Alle deaktivieren, und klicken Sie dann auf OK.</span><span class="sxs-lookup"><span data-stu-id="abc41-590">Click the Uncheck All box, and then click OK</span></span>
    18. <span data-ttu-id="abc41-591">Wechseln Sie zu Benutzer Steuerelemente \| Spiele Steuerelemente, und lassen Sie das jeweilige Spiel mithilfe der ESRB-Bewertung zu</span><span class="sxs-lookup"><span data-stu-id="abc41-591">Go to User Controls \| Games Controls and allow the specific game using the ESRB rating</span></span>
    19. <span data-ttu-id="abc41-592">Melden Sie sich als Andrea ab, und melden Sie sich als Toby an, und wiederholen Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="abc41-592">Log off as Jane and log on as Toby and try to play the game</span></span>
    20. <span data-ttu-id="abc41-593">1,2 Stellen Sie sicher, dass das Spiel nicht blockiert ist, und dass es von "von" (keine exe-Datei zulassen) wiedergegeben werden kann. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-593">Verify that the game is NOT blocked and that Toby can play it when "allow no exes" is set \[1.2\]</span></span>
    21. <span data-ttu-id="abc41-594">Melden Sie sich als Benutzer Toby und wieder als Benutzer Jane an.</span><span class="sxs-lookup"><span data-stu-id="abc41-594">Log off as user Toby and back on as user Jane</span></span>
    22. <span data-ttu-id="abc41-595">Wechseln Sie in der Systemsteuerung zu Jugendschutz, und entfernen Sie die Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="abc41-595">Go to Parental Controls in Control Panel and remove the restrictions</span></span>
    23. <span data-ttu-id="abc41-596">Stellen Sie sicher, dass beide Benutzer jetzt das Spiel abspielen können.</span><span class="sxs-lookup"><span data-stu-id="abc41-596">Verify that both users can now play the game</span></span>

4.  <span data-ttu-id="abc41-597">Mit [automatisierten Tests](#58-automated-tests) fortfahren</span><span class="sxs-lookup"><span data-stu-id="abc41-597">Proceed to [Automated Tests](#58-automated-tests)</span></span>

### <a name="58-automated-tests"></a><span data-ttu-id="abc41-598">5,8 automatisierte Tests</span><span class="sxs-lookup"><span data-stu-id="abc41-598">5.8 Automated Tests</span></span>

1.  <span data-ttu-id="abc41-599">Stellen Sie 4,2 sicher, dass das Spiel keine Fehler generiert, wenn Sie es unter Application Verifier ausführen \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-599">Verify that the game does not generate failures when run under Application Verifier - See Branding Test Tool Documentation \[4.2\]</span></span>
2.  <span data-ttu-id="abc41-600">Vergewissern Sie sich, dass die ausführbaren Dateien des Spiels Manifeste enthalten. siehe Branding-Test Tool Dokumentation \[ 2,1\]</span><span class="sxs-lookup"><span data-stu-id="abc41-600">Verify that the game executable files contain manifests - see Branding Test Tool Documentation \[2.1\]</span></span>
3.  <span data-ttu-id="abc41-601">Vergewissern Sie sich, dass das ausführbare Datei Manifest requestedExecutionLevel "asInvoker" ist. Informationen hierzu finden Sie unter Branding Test Tool-Dokumentation \[ 2,1\]</span><span class="sxs-lookup"><span data-stu-id="abc41-601">Verify that the game executable file manifest requestedExecutionLevel is "AsInvoker" - see Branding Test Tool Documentation \[2.1\]</span></span>
4.  <span data-ttu-id="abc41-602">Mit [anderen Tests](#59-other-tests) fortfahren</span><span class="sxs-lookup"><span data-stu-id="abc41-602">Proceed to [Other Tests](#59-other-tests)</span></span>

### <a name="59-other-tests"></a><span data-ttu-id="abc41-603">5,9 andere Tests</span><span class="sxs-lookup"><span data-stu-id="abc41-603">5.9 Other Tests</span></span>

1.  <span data-ttu-id="abc41-604">Überprüfen Sie, ob die ausführbaren Dateien des Spiels eine digitale Signatur \[ 2,3 enthalten\]</span><span class="sxs-lookup"><span data-stu-id="abc41-604">Verify that the game executable files contain a digital signature \[2.3\]</span></span>
2.  <span data-ttu-id="abc41-605">Überprüfen Sie, ob der Spiel Installationsprozess auf 64-Bit-Editionen von Windows Vista und/oder Windows 7 2,3 normal ausgeführt wird. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-605">Verify that the game installation process runs normally on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
3.  <span data-ttu-id="abc41-606">Stellen Sie sicher, dass das Spiel aufgrund von 16-Bit-ausführbaren Dateien auf 64-Bit-Editionen von Windows Vista und/oder Windows 7 2,3 keinen Fehler verursacht. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-606">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
4.  <span data-ttu-id="abc41-607">Erzwingen Sie einen Absturz der Anwendung beim Testen, und vergewissern Sie sich, dass das Spiel Windows-Fehlerberichterstattung ordnungsgemäß angezeigt wird, und erfasst die Absturz Daten \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="abc41-607">Force the application to crash while testing, and verify that the game displays Windows Error Reporting properly and collects crash data \[4.3\]</span></span>
5.  <span data-ttu-id="abc41-608">Ordnungsgemäße Datei Zusammenfassungen \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="abc41-608">Ensure proper file summaries \[4.3\]</span></span>

    1.  <span data-ttu-id="abc41-609">Klicken Sie auf Start-> Computer.</span><span class="sxs-lookup"><span data-stu-id="abc41-609">Click Start -> Computer</span></span>
    2.  <span data-ttu-id="abc41-610">Navigieren Sie zum Spielverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="abc41-610">Navigate to the game directory</span></span>
    3.  <span data-ttu-id="abc41-611">Geben Sie im Suchfenster " \* . dll" ein.</span><span class="sxs-lookup"><span data-stu-id="abc41-611">In the search window, type \*.dll</span></span>
    4.  <span data-ttu-id="abc41-612">Klicken Sie mit der rechten Maustaste auf die Datei, und klicken Sie dann auf Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="abc41-612">For each file: Right-click the file and click Properties</span></span>

        -   <span data-ttu-id="abc41-613">Unter Windows XP: Klicken Sie auf die Registerkarte Version. Überprüfen Sie, ob die Felder Produktname, Firmenname und Datei Version ordnungsgemäß ausgefüllt sind.</span><span class="sxs-lookup"><span data-stu-id="abc41-613">In Windows XP: Click the Version tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span> <span data-ttu-id="abc41-614">\[4.3\]</span><span class="sxs-lookup"><span data-stu-id="abc41-614">\[4.3\]</span></span>
        -   <span data-ttu-id="abc41-615">In Windows Vista und Windows 7: Klicken Sie auf die Registerkarte Details. Überprüfen Sie, ob die Felder Product Name und File Version ordnungsgemäß aufgefüllt sind.</span><span class="sxs-lookup"><span data-stu-id="abc41-615">In Windows Vista and Windows 7: Click the Details tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="abc41-616">Der Name des Unternehmens ist auf der Eigenschaften 4,3 Seite von Windows Vista oder Windows 7 nicht sichtbar. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-616">Company Name is not visible in the Windows Vista or Windows 7 properties page \[4.3\]</span></span>

    5.  <span data-ttu-id="abc41-617">Wiederholen Sie diese Prüfung auf exe-Dateien.</span><span class="sxs-lookup"><span data-stu-id="abc41-617">Repeat this check for .exe files</span></span>

6.  <span data-ttu-id="abc41-618">Starten Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="abc41-618">Launch the game.</span></span>

    1.  <span data-ttu-id="abc41-619">STRG + ALT + ENTF drücken</span><span class="sxs-lookup"><span data-stu-id="abc41-619">Press CTRL+ALT+DEL</span></span>
    2.  <span data-ttu-id="abc41-620">Klicken Sie auf den Pfeil "Optionen für das Herunterfahren"</span><span class="sxs-lookup"><span data-stu-id="abc41-620">Click the "Shutdown Options" arrow</span></span>
    3.  <span data-ttu-id="abc41-621">Klicken Sie auf Neustart</span><span class="sxs-lookup"><span data-stu-id="abc41-621">Click Restart</span></span>
    4.  <span data-ttu-id="abc41-622">Überprüfen, ob das Spiel das Herunterfahren \[ 3,1 blockiert\]</span><span class="sxs-lookup"><span data-stu-id="abc41-622">Verify game does not block shutdown \[3.1\]</span></span>

7.  <span data-ttu-id="abc41-623">[Deinstallation](#510-uninstall) fortsetzen</span><span class="sxs-lookup"><span data-stu-id="abc41-623">Proceed to [Uninstall](#510-uninstall)</span></span>

### <a name="510-uninstall"></a><span data-ttu-id="abc41-624">5,10 deinstallieren</span><span class="sxs-lookup"><span data-stu-id="abc41-624">5.10 Uninstall</span></span>

-   <span data-ttu-id="abc41-625">Überprüfen Sie, ob bei der Deinstallation des Spiels alle installierten, nicht verteilbaren Betriebssystem-Komponenten Dateien entfernt werden, und löschen Sie alle Einstellungen \[ 3,1.\]</span><span class="sxs-lookup"><span data-stu-id="abc41-625">Verify that the game uninstallation process removes all installed, non-redistributed operating system component files and clears all settings \[3.1\]</span></span>

    -   <span data-ttu-id="abc41-626">Überprüfen Sie unter Windows Vista oder Windows 7, dass die Systemsteuerung die einzige Möglichkeit zum Entfernen des Programms 1,1 ist. \[\]</span><span class="sxs-lookup"><span data-stu-id="abc41-626">Verify in Windows Vista or Windows 7 that Control Panel is the only way to remove the program \[1.1\]</span></span>

## <a name="test-tool-notes"></a><span data-ttu-id="abc41-627">Anmerkungen zum Testtool</span><span class="sxs-lookup"><span data-stu-id="abc41-627">Test Tool Notes</span></span>

<span data-ttu-id="abc41-628">Dies sind Hinweise für die einzelnen Testtools, die in den obigen Testanforderungen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="abc41-628">These are notes for each of the test tools listed in the above test requirements.</span></span>

### <a name="61-appverifier-40-or-higher"></a><span data-ttu-id="abc41-629">6,1 AppVerifier 4,0 (oder höher)</span><span class="sxs-lookup"><span data-stu-id="abc41-629">6.1 Appverifier 4.0 (or higher)</span></span>

<span data-ttu-id="abc41-630">**Testfall: 2,5, 4,2**</span><span class="sxs-lookup"><span data-stu-id="abc41-630">**Test Case: 2.5, 4.2**</span></span>

> [!Note]  
> <span data-ttu-id="abc41-631">Einige Anwendungen können aufgrund des Kopierschutzes nicht mit AppVerifier ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-631">Some applications fail to run with AppVerifier running, because of copy protection.</span></span> <span data-ttu-id="abc41-632">Dies kann durch Ausführen von mit einer ungeschützten Releaseversion der ausführbaren Spieldatei behoben werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-632">This can be resolved by running with an unprotected release version of the game executable.</span></span>

 

1.  <span data-ttu-id="abc41-633">Installieren von AppVerifier 4,0 (oder höher) auf einem Computer mit Windows XP</span><span class="sxs-lookup"><span data-stu-id="abc41-633">Install AppVerifier 4.0 (or higher) on a computer running Windows XP</span></span>
2.  <span data-ttu-id="abc41-634">Starten Sie AppVerifier, und klicken Sie auf Datei > Anwendung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="abc41-634">Launch AppVerifier and click File -> Add Application</span></span>
3.  <span data-ttu-id="abc41-635">Suchen Sie die ausführbare Datei, wählen Sie Sie aus, und klicken Sie</span><span class="sxs-lookup"><span data-stu-id="abc41-635">Locate the game executable, select it and click Open</span></span>
4.  <span data-ttu-id="abc41-636">Wählen Sie im Abschnitt "Anwendungen" die ausführbare Datei für das Spiel aus.</span><span class="sxs-lookup"><span data-stu-id="abc41-636">In the "Applications" section, select the game executable</span></span>
5.  <span data-ttu-id="abc41-637">Wählen Sie im Abschnitt "Grundlagen" die folgenden Tests aus:</span><span class="sxs-lookup"><span data-stu-id="abc41-637">Select the following tests in the "Basics" section:</span></span>

    -   <span data-ttu-id="abc41-638">Ziehpunkte</span><span class="sxs-lookup"><span data-stu-id="abc41-638">Handles</span></span>
    -   <span data-ttu-id="abc41-639">Heaps</span><span class="sxs-lookup"><span data-stu-id="abc41-639">Heaps</span></span>
    -   <span data-ttu-id="abc41-640">Locks</span><span class="sxs-lookup"><span data-stu-id="abc41-640">Locks</span></span>
    -   <span data-ttu-id="abc41-641">Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="abc41-641">Memory</span></span>
    -   <span data-ttu-id="abc41-642">TLS</span><span class="sxs-lookup"><span data-stu-id="abc41-642">TLS</span></span>

6.  <span data-ttu-id="abc41-643">Wählen Sie im Abschnitt "Verschiedenes" die folgenden Tests aus:</span><span class="sxs-lookup"><span data-stu-id="abc41-643">Select the following tests in the "Miscellaneous" section:</span></span>

    -   <span data-ttu-id="abc41-644">Dangerousapis</span><span class="sxs-lookup"><span data-stu-id="abc41-644">DangerousAPIs</span></span>
    -   <span data-ttu-id="abc41-645">Dirtystacks</span><span class="sxs-lookup"><span data-stu-id="abc41-645">DirtyStacks</span></span>

7.  <span data-ttu-id="abc41-646">Stellen Sie sicher, dass keine anderen Tests ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="abc41-646">Ensure all other tests are not selected</span></span>
8.  <span data-ttu-id="abc41-647">Starten des Spiels</span><span class="sxs-lookup"><span data-stu-id="abc41-647">Launch the game</span></span>
9.  <span data-ttu-id="abc41-648">Spielen Sie das Spiel</span><span class="sxs-lookup"><span data-stu-id="abc41-648">Play the game</span></span>
10. <span data-ttu-id="abc41-649">Schließen Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="abc41-649">Close the game</span></span>
11. <span data-ttu-id="abc41-650">Wählen Sie in AppVerifier > Protokolle anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="abc41-650">In AppVerifier select View -> Logs</span></span>
12. <span data-ttu-id="abc41-651">Wählen Sie im Abschnitt "Anwendungen" die Datei "App. exe" aus.</span><span class="sxs-lookup"><span data-stu-id="abc41-651">In the "Applications" section select the app .exe file</span></span>
13. <span data-ttu-id="abc41-652">Wählen Sie im Abschnitt "Protokolle" die Protokolldatei aus, und beobachten Sie die Fehler Anzahl.</span><span class="sxs-lookup"><span data-stu-id="abc41-652">In the "Logs" section, select the log file and observe the error count.</span></span> <span data-ttu-id="abc41-653">Wenn keine Fehler vorliegen, beenden Sie AppVerifier-Tests.</span><span class="sxs-lookup"><span data-stu-id="abc41-653">If there are no errors, then end AppVerifier tests.</span></span> <span data-ttu-id="abc41-654">Wenn Fehler auftreten, klicken Sie auf die Schaltfläche "Ansicht".</span><span class="sxs-lookup"><span data-stu-id="abc41-654">If there are errors, click the View button</span></span>
14. <span data-ttu-id="abc41-655">Durchsuchen Sie das Dokument (STRG + F) nach Schweregrad = "Fehler</span><span class="sxs-lookup"><span data-stu-id="abc41-655">Search the document (CTRL+F) for Severity="Error</span></span>
15. <span data-ttu-id="abc41-656">Erstellen von Fehlern basierend auf dem "Layername ="-Teil des Fehlers</span><span class="sxs-lookup"><span data-stu-id="abc41-656">Create bugs based on the LayerName= portion of the failure</span></span>

### <a name="62-manifest-test---mtexe"></a><span data-ttu-id="abc41-657">6,2 Manifest-Test-mt.exe</span><span class="sxs-lookup"><span data-stu-id="abc41-657">6.2 Manifest Test - mt.exe</span></span>

<span data-ttu-id="abc41-658">**Testfall: 1,8, 2,1**</span><span class="sxs-lookup"><span data-stu-id="abc41-658">**Test Case: 1.8, 2.1**</span></span>

<span data-ttu-id="abc41-659">Dieses Tool wird an einer Eingabeaufforderung ausgeführt, in der sich MT.exe befindet.</span><span class="sxs-lookup"><span data-stu-id="abc41-659">This tool is run from a command prompt where MT.exe is located.</span></span>

<span data-ttu-id="abc41-660">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="abc41-660">Example:</span></span>

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  <span data-ttu-id="abc41-661">Klicken Sie auf Start-> Run-> type cmd, und klicken Sie auf die Schaltfläche OK.</span><span class="sxs-lookup"><span data-stu-id="abc41-661">Click Start -> Run -> type cmd and click the OK button</span></span>
2.  <span data-ttu-id="abc41-662">Führen Sie das mt.exe Tool aus, um für jede exe-Datei, die mit dem Spiel installiert wird, eine Manifest-Datei zu generieren.</span><span class="sxs-lookup"><span data-stu-id="abc41-662">Run the mt.exe tool to generate a .manifest file for each .exe file that installs with the game</span></span>
3.  <span data-ttu-id="abc41-663">Öffnen Sie die generierte Manifest-Datei.</span><span class="sxs-lookup"><span data-stu-id="abc41-663">Open the generated .manifest file</span></span>
4.  <span data-ttu-id="abc41-664">Stellen Sie sicher, dass jede exe-Datei Folgendes enthält (angefordert:</span><span class="sxs-lookup"><span data-stu-id="abc41-664">Ensure that each .exe file contains the following (requested:</span></span>

    ``` syntax
    <description>Example Game Name</description>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v2">
      <security>
        <requestedPrivileges>
          <requestedExecutionLevel level="asInvoker"></requestedExecutionLevel>
        </requestedPrivileges>
      </security>
    </trustInfo>
      <asmv3:windowsSettings xmlns=http://schemas.microsoft.com/SMI/2005/WindowsSettings>
        <dpiAware>true<dpiAware>
      </asmv3:windowsSettings>
    </asmv3:application>
    ```

> [!Note]  
> <span data-ttu-id="abc41-665">Die angeforderte Ausführungs Ebene sollte für jede Datei vorhanden sein, und für mindestens die ausführbare Datei des Spiels muss dpiaware vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="abc41-665">Requested execution level should be present for every file, and dpiAware should be present for at least the game s executable file.</span></span>

 

### <a name="63-thread-hijacker---threadhijackerexe"></a><span data-ttu-id="abc41-666">6,3 Thread-Hijacker-threadhijacker.exe</span><span class="sxs-lookup"><span data-stu-id="abc41-666">6.3 Thread Hijacker - threadhijacker.exe</span></span>

<span data-ttu-id="abc41-667">Dieses Tool wird an einer Eingabeaufforderung ausgeführt, in der sich threadhijacker.exe befindet.</span><span class="sxs-lookup"><span data-stu-id="abc41-667">This tool is run from a command prompt where threadhijacker.exe is located.</span></span>

<span data-ttu-id="abc41-668">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="abc41-668">Example:</span></span>

``` syntax
threadhijacker.exe /process:str
```

<span data-ttu-id="abc41-669">Dabei ist Str der Name \_ \_program.exe</span><span class="sxs-lookup"><span data-stu-id="abc41-669">Where str is the name\_of\_program.exe</span></span>

1.  <span data-ttu-id="abc41-670">Rufen Sie den Task-Manager auf, klicken Sie auf die Registerkarte Prozesse, und suchen Sie den Namen des ausführbaren Spiels.</span><span class="sxs-lookup"><span data-stu-id="abc41-670">Bring up Task Manager, click the Processes tab, and locate the name of the game executable.</span></span>
2.  <span data-ttu-id="abc41-671">Öffnen Sie eine Eingabeaufforderung im Administrator Modus.</span><span class="sxs-lookup"><span data-stu-id="abc41-671">Open a command prompt in Admin mode</span></span>
3.  <span data-ttu-id="abc41-672">Navigieren Sie zu dem Verzeichnis, in dem threadhijacker.exe</span><span class="sxs-lookup"><span data-stu-id="abc41-672">Navigate to the directory where threadhijacker.exe is</span></span>
4.  <span data-ttu-id="abc41-673">Type: **threadhijacker.exe/Process:** Str, wobei Str der Name der ausführbaren Datei ist, die Sie erreichen möchten.</span><span class="sxs-lookup"><span data-stu-id="abc41-673">Type: **threadhijacker.exe /process:** str, where str is the name of the executable that you want to hit</span></span>

### <a name="64-microsoft-games-for-windows-test-tool"></a><span data-ttu-id="abc41-674">6,4 Microsoft Games for Windows-Testtool</span><span class="sxs-lookup"><span data-stu-id="abc41-674">6.4 Microsoft Games for Windows Test Tool</span></span>

<span data-ttu-id="abc41-675">Dieses Tool befindet sich im DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="abc41-675">This tool is located in the DirectX SDK.</span></span> <span data-ttu-id="abc41-676">Sobald das SDK auf einem Computer installiert ist, kann das Installationsprogramm für das Testtool Games for Windows auf dem Testcomputer abgelegt und installiert werden.</span><span class="sxs-lookup"><span data-stu-id="abc41-676">Once the SDK is installed on a computer, the installer for the Games for Windows Test Tool can be placed on the test computer and installed.</span></span>

<span data-ttu-id="abc41-677">Suchen Sie auf dem Entwicklungs Computer, auf dem das DirectX SDK installiert ist, das Installationsprogramm für Microsoft Games for Windows Test Tool.</span><span class="sxs-lookup"><span data-stu-id="abc41-677">Locate the Microsoft Games for Windows Test Tool installer on the development computer where the DirectX SDK is installed.</span></span> <span data-ttu-id="abc41-678">Standardmäßig wird Sie an folgendem Speicherort platziert:</span><span class="sxs-lookup"><span data-stu-id="abc41-678">By default, it is placed in the following location:</span></span>

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  <span data-ttu-id="abc41-679">Kopieren Sie das Installationsprogramm (MicrosoftGFWTestTool.msi/setup.exe) auf den Testcomputer.</span><span class="sxs-lookup"><span data-stu-id="abc41-679">Copy the installer (MicrosoftGFWTestTool.msi / setup.exe) to the test computer.</span></span>
2.  <span data-ttu-id="abc41-680">Führen Sie das Installationsprogramm aus.</span><span class="sxs-lookup"><span data-stu-id="abc41-680">Run the installer.</span></span>
3.  <span data-ttu-id="abc41-681">Starten Sie das Testtool Microsoft Games for Windows.</span><span class="sxs-lookup"><span data-stu-id="abc41-681">Launch the Microsoft Games for Windows Test Tool.</span></span>
4.  <span data-ttu-id="abc41-682">Ersetzen Sie im Feld **Projektliste** das Feld **Neues Projekt** durch ihren Titel Namen erstellen, und klicken Sie auf **neu erstellen**.</span><span class="sxs-lookup"><span data-stu-id="abc41-682">In the **Project List** field replace **Create New Project** with your title name and click **Create New**.</span></span>

    <span data-ttu-id="abc41-683">Warten Sie, bis die Baseline fertiggestellt ist.</span><span class="sxs-lookup"><span data-stu-id="abc41-683">Wait for the Baseline to complete.</span></span>

5.  <span data-ttu-id="abc41-684">Geben Sie alle Informationen ein, die Sie möglicherweise im Abschnitt " **Spielinformationen** " haben, und klicken Sie auf " **Spielinformationen aktualisieren**".</span><span class="sxs-lookup"><span data-stu-id="abc41-684">Fill in any information that you may have in the **Game Information** section, and click **Update Game Information**.</span></span>
6.  <span data-ttu-id="abc41-685">Klicken Sie auf die Registerkarte **Testfälle** .</span><span class="sxs-lookup"><span data-stu-id="abc41-685">Click on **Test Cases** tab.</span></span>
7.  <span data-ttu-id="abc41-686">Beginnen Sie im oberen Bereich mit den Testfällen, und klicken Sie nach Bedarf auf **übergeben** oder **fehlschlagen** .</span><span class="sxs-lookup"><span data-stu-id="abc41-686">Starting at the top, proceed through the test cases, clicking **Pass** or **Fail** as appropriate.</span></span>

    <span data-ttu-id="abc41-687">Weitere Informationen zum Einschließen eines Fehlers in den Bericht finden Sie unter "Schreiben eines Fehlers" weiter unten in diesem Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="abc41-687">See "Writing a Bug", later in this section, for details on including a bug in the report.</span></span>

8.  <span data-ttu-id="abc41-688">Kehren Sie nach dem Überprüfen des Berichts zur Registerkarte **Projekte** zurück (durch Überprüfen der Registerkarten **Bericht** und **Fehler Bearbeitung** ).</span><span class="sxs-lookup"><span data-stu-id="abc41-688">Return to the **Projects** tab after reviewing the report (by checking the **Report** and **Bug Edit** tabs).</span></span>
9.  <span data-ttu-id="abc41-689">Klicken Sie auf **Bericht kompilieren**.</span><span class="sxs-lookup"><span data-stu-id="abc41-689">Click **Compile Report**.</span></span>

    <span data-ttu-id="abc41-690">Ein Fenster wird geöffnet, wenn die Kompilierung des Berichts abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="abc41-690">A window will open when the report is finished compiling.</span></span> <span data-ttu-id="abc41-691">Hier finden Sie eine. ZIP-Dateinamen *Projektname* \_report.zip.</span><span class="sxs-lookup"><span data-stu-id="abc41-691">Here you will find a .ZIP file names *ProjectName*\_report.zip.</span></span> <span data-ttu-id="abc41-692">Diese Datei enthält alle Protokolle und Ergebnisse, die während des Tests erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="abc41-692">This file contains all of the logs and results collected during the test pass.</span></span>

### <a name="writing-a-bug"></a><span data-ttu-id="abc41-693">Schreiben eines Fehlers</span><span class="sxs-lookup"><span data-stu-id="abc41-693">Writing a Bug</span></span>

<span data-ttu-id="abc41-694">Es gibt zwei Möglichkeiten, einen Fehlerbericht zu schreiben: Sie können die Testfälle durchlaufen und auf "Fehler" klicken, wenn der Titel einen Testfall fehlschlägt, oder Sie können auf die Registerkarte " **Fehler Bearbeitung** **" klicken und** manuell einen Fehlerbericht hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="abc41-694">There are two ways to write a bug report: you can go through the test cases and click **Fail** when the title fails a test case, or you can click the **Bug Edit** tab and manually add a bug report.</span></span>

### <a name="clicking-fail-on-a-test-case"></a><span data-ttu-id="abc41-695">Klicken auf "Fehler" bei einem Testfall</span><span class="sxs-lookup"><span data-stu-id="abc41-695">Clicking Fail on a test case</span></span>

1.  <span data-ttu-id="abc41-696">Wenn Sie bei einem Testfall **auf "Fehler" klicken,** wird die Dropdown Liste " **Problemtyp** " automatisch auf den Testfall-Typ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="abc41-696">When you click **Fail** on a test case, the **Issue Type** drop-down list will automatically be set to the test case type.</span></span>
2.  <span data-ttu-id="abc41-697">Fügen Sie dem Feld **Title** eine kurze Beschreibung hinzu, in der das Problem kurz beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="abc41-697">Add a short description to the **Title** field that briefly describes the issue.</span></span>
3.  <span data-ttu-id="abc41-698">Fügen Sie dem Feld " **beobachteter Verhalten** " eine ausführliche Beschreibung des Problems hinzu.</span><span class="sxs-lookup"><span data-stu-id="abc41-698">Add a detailed description of the issue to the **Observed Behavior** field.</span></span>
4.  <span data-ttu-id="abc41-699">Fügen Sie ggf. das erwartete Verhalten (im Gegensatz zu einer Beschreibung des Problems) dem Feld **erwartetes Verhalten** hinzu.</span><span class="sxs-lookup"><span data-stu-id="abc41-699">As appropriate, add what was expected (as opposed to a description of the issue) to the **Expected Behavior** field.</span></span>
5.  <span data-ttu-id="abc41-700">Fügen Sie eine ausführliche Beschreibung der Reproduktion des Problems im Feld **Reproduktions Schritte** hinzu.</span><span class="sxs-lookup"><span data-stu-id="abc41-700">Add a detailed description of how to reproduce the issue to the **Repro-Steps** field.</span></span>
6.  <span data-ttu-id="abc41-701">Klicken Sie abschließend auf die Schaltfläche **Speichern** .</span><span class="sxs-lookup"><span data-stu-id="abc41-701">When done, click the **Save** button.</span></span>

### <a name="manually-adding-a-bug"></a><span data-ttu-id="abc41-702">Manuelles Hinzufügen eines Fehlers</span><span class="sxs-lookup"><span data-stu-id="abc41-702">Manually Adding a Bug</span></span>

<span data-ttu-id="abc41-703">Dieser Prozess ist identisch mit dem Klicken auf " **fehl** geschlagen", mit Ausnahme der automatisch aufgefüllten Dropdown Liste.</span><span class="sxs-lookup"><span data-stu-id="abc41-703">This process is the same as clicking **Fail**, with the exception of the auto-populated drop-down list.</span></span> <span data-ttu-id="abc41-704">Wählen Sie in diesem Fall entweder den entsprechenden TCR-Fehlertyp aus, oder wählen Sie ein **\* \* nicht-TR-Problem \* \*** für Fehler aus, die außerhalb des TR-Bereichs liegen, aber trotzdem gemeldet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="abc41-704">In this case, either select the appropriate TCR failure type or select **\*\* Non-TR Issue \*\*** for bugs that fall outside of the TR range but should still be reported.</span></span>

## <a name="resources"></a><span data-ttu-id="abc41-705">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="abc41-705">Resources</span></span>

<dl> <dt>

<span data-ttu-id="abc41-706"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Spiele für Windows: technische Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abc41-706"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Games for Windows: Technical Requirements</span></span>
</dt> <dd>

[<span data-ttu-id="abc41-707">Spiele für technische Windows-Anforderungen: bewährte Methoden für Spiele unter Windows XP, Windows Vista und Windows 7</span><span class="sxs-lookup"><span data-stu-id="abc41-707">Games for Windows Technical Requirements: Best Practices for Games on Windows XP, Windows Vista, and Windows 7</span></span>](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span data-ttu-id="abc41-708"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span><span class="sxs-lookup"><span data-stu-id="abc41-708"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span></span>
</dt> <dd>

[<span data-ttu-id="abc41-709">Windows sdche</span><span class="sxs-lookup"><span data-stu-id="abc41-709">Windows SDKs</span></span>](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span data-ttu-id="abc41-710"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Richtlinien für die Benutzerkontensteuerung</span><span class="sxs-lookup"><span data-stu-id="abc41-710"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>User Account Control Guidelines</span></span>
</dt> <dd>

<span data-ttu-id="abc41-711">[Windows Vista-Anwendungs Entwicklungsanforderungen für die Kompatibilität mit der Benutzerkontensteuerung](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="abc41-711">[Windows Vista Application Development Requirements for User Account Control Compatibility](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span></span>

</dd> <dt>

<span data-ttu-id="abc41-712"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer Informationen</span><span class="sxs-lookup"><span data-stu-id="abc41-712"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer Information</span></span>
</dt> <dd>

[<span data-ttu-id="abc41-713">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="abc41-713">Windows Installer</span></span>](../msi/windows-installer-portal.md)

</dd> <dt>

<span data-ttu-id="abc41-714"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>Winqual-Entwickler Portal</span><span class="sxs-lookup"><span data-stu-id="abc41-714"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Developer Portal</span></span> 
</dt> <dd>

[<span data-ttu-id="abc41-715">Windows Quality Online Services (Winqual)</span><span class="sxs-lookup"><span data-stu-id="abc41-715">Windows Quality Online Services (Winqual)</span></span>](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span data-ttu-id="abc41-716"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX-Entwickler Portal</span><span class="sxs-lookup"><span data-stu-id="abc41-716"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX Developer Portal</span></span>
</dt> <dd>

<span data-ttu-id="abc41-717">[DirectX-Entwickler Center](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="abc41-717">[DirectX Developer Center](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>

</dd> <dt>

<span data-ttu-id="abc41-718"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog zu spielen für Windows und DirectX SDK</span><span class="sxs-lookup"><span data-stu-id="abc41-718"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Games for Windows and DirectX SDK Blog</span></span>
</dt> <dd>

[<span data-ttu-id="abc41-719">Spiele für Windows und das DirectX SDK</span><span class="sxs-lookup"><span data-stu-id="abc41-719">Games for Windows and the DirectX SDK</span></span>](https://walbourn.github.io/)

</dd> <dt>

<span data-ttu-id="abc41-720"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Weitere DirectX-Artikel</span><span class="sxs-lookup"><span data-stu-id="abc41-720"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Additional DirectX Articles</span></span>
</dt> <dd>

[<span data-ttu-id="abc41-721">Technische Artikel zu DirectX</span><span class="sxs-lookup"><span data-stu-id="abc41-721">DirectX Technical Articles</span></span>](./dx9-technical-articles.md)

</dd> </dl>

 

