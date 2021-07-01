---
title: Testfälle für Spiele für Windows; bewährte Methoden für Spiele für Windows XP, Windows Vista, Windows 7 und Windows 8
description: Dieser Artikel enthält Testfälle für Spiele für Windows.
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b13a4934c539579e49c9b00c60f3603bd64c711
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120275"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a><span data-ttu-id="823fb-103">Spiele für Windows-Testfälle: Bewährte Methoden für Spiele unter Windows XP, Windows Vista, Windows 7 und Windows 8</span><span class="sxs-lookup"><span data-stu-id="823fb-103">Games for Windows Test Cases: Best Practices for Games on Windows XP, Windows Vista, Windows 7, and Windows 8</span></span>

<span data-ttu-id="823fb-104">Dieser Artikel enthält Testfälle für Spiele für Windows.</span><span class="sxs-lookup"><span data-stu-id="823fb-104">This article provides test cases for games for Windows.</span></span>

## <a name="how-to-use-this-article"></a><span data-ttu-id="823fb-105">Zur Verwendung dieses Artikels</span><span class="sxs-lookup"><span data-stu-id="823fb-105">How to Use This Article</span></span>

<span data-ttu-id="823fb-106">Dieser Artikel enthält drei Hauptabschnitte:</span><span class="sxs-lookup"><span data-stu-id="823fb-106">There are three main sections to this article:</span></span>

<dl> <dt>

<span data-ttu-id="823fb-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Testanforderungen**</span><span class="sxs-lookup"><span data-stu-id="823fb-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Test Requirements**</span></span>
</dt> <dd>

<span data-ttu-id="823fb-108">Jede Testanforderung in diesem Dokument enthält vier Hauptabschnitte: einen Titel und eine Tabelle mit drei wesentlichen Abschnitten (linke Spalte, rechts oben, rechts unten).</span><span class="sxs-lookup"><span data-stu-id="823fb-108">Each test requirement in this document has four main sections: a title and a table with three notable sections (left column, right top, right bottom).</span></span>

<dl> <dt>

<span data-ttu-id="823fb-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Titel</span><span class="sxs-lookup"><span data-stu-id="823fb-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Title</span></span>
</dt> <dd>

<span data-ttu-id="823fb-110">Name des Testfalles.</span><span class="sxs-lookup"><span data-stu-id="823fb-110">Name of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="823fb-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Feld, spalte ganz links</span><span class="sxs-lookup"><span data-stu-id="823fb-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, far left column</span></span>
</dt> <dd>

<span data-ttu-id="823fb-112">Namen der Betriebssysteme, für die der Testfall gilt.</span><span class="sxs-lookup"><span data-stu-id="823fb-112">Names of the operating systems to which the test case applies.</span></span>

</dd> <dt>

<span data-ttu-id="823fb-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, rechts oben</span><span class="sxs-lookup"><span data-stu-id="823fb-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, right top</span></span>
</dt> <dd>

<span data-ttu-id="823fb-114">Kurze Zusammenfassung des Testfalles.</span><span class="sxs-lookup"><span data-stu-id="823fb-114">Brief summary of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="823fb-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, rechts unten</span><span class="sxs-lookup"><span data-stu-id="823fb-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, right bottom</span></span>
</dt> <dd>

<span data-ttu-id="823fb-116">Details zum tatsächlichen Testfall.</span><span class="sxs-lookup"><span data-stu-id="823fb-116">Details of the actual test case.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="823fb-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Beispieltestskript**</span><span class="sxs-lookup"><span data-stu-id="823fb-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Sample Test Script**</span></span>
</dt> <dd>

<span data-ttu-id="823fb-118">Dieser Abschnitt ist ein Beispiel für die Sequenz, der ein typischer Testlauf folgen würde, wenn die Testanforderungen als Leitfaden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-118">This section is a sample of the sequence that a typical test pass would follow if using the test requirements as a guide.</span></span>

</dd> <dt>

<span data-ttu-id="823fb-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Hinweise zum Testtool**</span><span class="sxs-lookup"><span data-stu-id="823fb-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Test Tool Notes**</span></span>
</dt> <dd>

<span data-ttu-id="823fb-120">Dieser Abschnitt enthält ausführliche Hinweise zu den einzelnen Testtools, die zum Überprüfen von Pass- oder Fail-Bedingungen in den Testanforderungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-120">This section contains detailed notes on each of the test tools used to verify pass or fail conditions in the test requirements.</span></span>

</dd> </dl>

## <a name="test-requirements"></a><span data-ttu-id="823fb-121">Testanforderungen</span><span class="sxs-lookup"><span data-stu-id="823fb-121">Test Requirements</span></span>

### <a name="1-game-requirements"></a><span data-ttu-id="823fb-122">1. Spielanforderungen</span><span class="sxs-lookup"><span data-stu-id="823fb-122">1. Game Requirements</span></span>

### <a name="11-windows-games-explorer"></a><span data-ttu-id="823fb-123">1.1 Windows Games Explorer</span><span class="sxs-lookup"><span data-stu-id="823fb-123">1.1 Windows Games Explorer</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-124">Windows 7</span></span><br/> <span data-ttu-id="823fb-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-125">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="823fb-126">Das Spiel muss im Spiele-Explorer unter Windows Vista und Windows 7 sichtbar sein.</span><span class="sxs-lookup"><span data-stu-id="823fb-126">The game must be visible within the Games Explorer on Windows Vista and Windows 7.</span></span> <span data-ttu-id="823fb-127">Wenn diese Option ausgewählt ist, muss das Spiel auch die richtigen Metadaten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="823fb-127">When selected, the game must also display correct metadata.</span></span> <span data-ttu-id="823fb-128">Die Installation darf keine Verknüpfung erstellen, um das Spiel auf dem Desktop, in der Startmenü oder an einem anderen Ort zu starten.</span><span class="sxs-lookup"><span data-stu-id="823fb-128">The installation must not create a shortcut to launch the game on the desktop, in the Start menu, or in any other location.</span></span> <span data-ttu-id="823fb-129">Tasks und Verknüpfungen zum Entfernen dürfen nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-129">Tasks and shortcuts for removal must not be created.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="823fb-130">Öffnen Sie nach der Installation des Spiels den Spiele-Explorer.</span><span class="sxs-lookup"><span data-stu-id="823fb-130">After installing the game, open Games Explorer.</span></span></li>
<li><span data-ttu-id="823fb-131">Vergewissern Sie sich, dass das Spielsymbol im Spiele-Explorer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-131">Verify that the game icon displays in Games Explorer.</span></span></li>
<li><span data-ttu-id="823fb-132">Klicken Sie mit der rechten Maustaste auf das Symbol, und testen Sie jede anwendungsdefinierte Wiedergabe & Supportaufgabe.</span><span class="sxs-lookup"><span data-stu-id="823fb-132">Right-click the icon and test each application-defined play & support task.</span></span></li>
<li><span data-ttu-id="823fb-133">Klicken Sie auf das Symbol, und überprüfen Sie, ob die Metadaten (Herausgeber, Entwickler, Genre, Veröffentlichungsdatum, Version) unten angezeigt werden und richtig sind.</span><span class="sxs-lookup"><span data-stu-id="823fb-133">Click the icon and verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct.</span></span></li>
<li><span data-ttu-id="823fb-134">Vergewissern Sie sich, dass auf dem Spielsymbol WeI-Informationen (Windows Experience Index) im Spiele-Explorer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-134">Verify that the game icon displays Windows Experience Index (WEI) information in Games Explorer.</span></span></li>
<li><span data-ttu-id="823fb-135">Vergewissern Sie sich, dass Die Spiellinks für Metadaten im Spiele-Explorer ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="823fb-135">Verify that game hyperlinks for metadata work correctly in Games Explorer.</span></span> <span data-ttu-id="823fb-136">(Wenn Links nicht angezeigt werden, ist dies ein mögliches Zeichen dafür, dass die EXE-Datei nicht signiert ist. Weitere Informationen finden Sie in Abschnitt <a href="#23-sign-files">2.3.)</a></span><span class="sxs-lookup"><span data-stu-id="823fb-136">(If hyperlinks don't show up, then this is a possible sign that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="823fb-137">Vergewissern Sie sich, dass das Spiel im Spiele-Explorer eine genaue Bewertung der Jugendkontrolle anzeigt.</span><span class="sxs-lookup"><span data-stu-id="823fb-137">Verify that the game displays accurate parental control rating in Games Explorer.</span></span> <span data-ttu-id="823fb-138">(Wenn es nicht wert ist, überprüfen Sie, ob es sich um ein nichtratiertes Spiel handelt. Andernfalls ist dies ein Indikator dafür, dass die EXE-Datei nicht signiert ist. Weitere Informationen finden Sie in Abschnitt <a href="#23-sign-files">2.3.)</a></span><span class="sxs-lookup"><span data-stu-id="823fb-138">(If it says unrated, then verify that this is an unrated game; otherwise, this is an indicator that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="823fb-139">Stellen Sie sicher, dass das Spiel keine Startverknüpfungen auf dem Benutzerdesktop abspielt.</span><span class="sxs-lookup"><span data-stu-id="823fb-139">Verify that the game does not place launch shortcuts on user desktop.</span></span></li>
<li><span data-ttu-id="823fb-140">Klicken Sie auf Start -> Alle Programme.</span><span class="sxs-lookup"><span data-stu-id="823fb-140">Click Start -> All Programs.</span></span></li>
<li><span data-ttu-id="823fb-141">Stellen Sie sicher, dass das Spiel keine Startverknüpfungen im Startmenü abspielt.</span><span class="sxs-lookup"><span data-stu-id="823fb-141">Verify that the game does not place launch shortcuts in the Start Menu.</span></span></li>
<li><span data-ttu-id="823fb-142">Stellen Sie sicher, dass das Spiel keine Deinstallationsverknüpfungen außerhalb des Startmenüs Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="823fb-142">Verify that the game does not place uninstall shortcuts in Start Menu outside of Control Panel.</span></span></li>
<li><span data-ttu-id="823fb-143">Wenn das Spiel digital verteilt wird, überprüfen Sie, ob der Dienstanbieter im Windows Games Explorer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-143">If the game is distributed digitally, verify that the service provider appears in Windows Games Explorer.</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a><span data-ttu-id="823fb-144">1.2 Windows Family Safety/Jugendschutz</span><span class="sxs-lookup"><span data-stu-id="823fb-144">1.2 Windows Family Safety / Parental Controls</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-145">Windows 7</span></span><br/> <span data-ttu-id="823fb-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-146">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="823fb-147">Das Spiel muss im Kontext eines &quot; Standardbenutzers ausgeführt &quot; werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-147">Game must execute within the context of a &quot;Standard User&quot;.</span></span> <span data-ttu-id="823fb-148">Die Jugendschutzkontrollen müssen in der Lage sein, das Spiel zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="823fb-148">Parental Controls must be able to block the game.</span></span> <span data-ttu-id="823fb-149">Stellen Sie sicher, dass die GDF ÜBER EXE-Namen verfügt.</span><span class="sxs-lookup"><span data-stu-id="823fb-149">Verify that the GDF has EXE names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="823fb-150">Erstellen Sie in Windows Vista oder Windows 7 ein Standardbenutzerkonto namens Toby.</span><span class="sxs-lookup"><span data-stu-id="823fb-150">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="823fb-151">Start -> Systemsteuerung -> Add or Remove User Accounts -> Create New Account</span><span class="sxs-lookup"><span data-stu-id="823fb-151">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span></li>
<li><span data-ttu-id="823fb-152">Richten Sie als Jane über das Administratorkonto die Jugendschutzkontrollen für das Spiel ein.</span><span class="sxs-lookup"><span data-stu-id="823fb-152">As Jane, from Administrator account set up Parental Controls for the game.</span></span> <span data-ttu-id="823fb-153">Start -> Systemsteuerung -> Einrichten von Jugendschutz für jeden Benutzer – > Toby</span><span class="sxs-lookup"><span data-stu-id="823fb-153">Start -> Control Panel -> Set Up Parental Controls for Any User -> Toby</span></span>
<ol>
<li><span data-ttu-id="823fb-154">Vergewissern Sie sich, dass das Spiel über das Symbol "Spiele-Explorer" gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-154">Verify that the game launches from the Games Explorer icon.</span></span></li>
<li><span data-ttu-id="823fb-155">Vergewissern Sie sich, dass das Spiel eine genaue Jugendkontrollbewertung unterhalb des Spieltitels im Jugendkontrollfenster Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="823fb-155">Verify that the game displays accurate Parental Control Rating below the game title in the Parental Controls Control Panel.</span></span></li>
<li><span data-ttu-id="823fb-156">Vergewissern Sie sich vor dem Anwenden von Jugendschutz, dass das Spiel beim Start nicht zur Eingabe von Administratoranmeldeinformationen aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-156">Before applying Parental Controls, verify that the game does not prompt for Administrator Credentials on launch.</span></span></li>
<li><span data-ttu-id="823fb-157">Legen Sie Jugendschutz auf &quot; Ein &quot; fest.</span><span class="sxs-lookup"><span data-stu-id="823fb-157">Set Parental Controls to &quot;On&quot;.</span></span></li>
<li><span data-ttu-id="823fb-158">Klicken Sie im Abschnitt Windows-Einstellungen auf Spiele.</span><span class="sxs-lookup"><span data-stu-id="823fb-158">In the Windows Settings section, click Games.</span></span></li>
<li><span data-ttu-id="823fb-159">Klicken Sie auf OK (die Einstellung sollte jetzt &quot; AO/alle Spiele &quot; sein).</span><span class="sxs-lookup"><span data-stu-id="823fb-159">Click OK (setting should now be &quot;AO / all games&quot;).</span></span></li>
<li><span data-ttu-id="823fb-160">Vergewissern Sie sich, dass das Spiel mit diesen Einstellungen als User Jane ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-160">Verify that the game runs with these settings as User Jane.</span></span></li>
<li><span data-ttu-id="823fb-161">Melden Sie sich als Jane ab, und melden Sie sich als Toby an.</span><span class="sxs-lookup"><span data-stu-id="823fb-161">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="823fb-162">Vergewissern Sie sich, dass das Spiel mit diesen Einstellungen als User Toby ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-162">Verify that the game runs with these settings as User Toby.</span></span></li>
<li><span data-ttu-id="823fb-163">Melden Sie sich als Toby ab, und melden Sie sich als Jane an.</span><span class="sxs-lookup"><span data-stu-id="823fb-163">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="823fb-164">Wechseln Sie zurück zum vorherigen Bildschirm, und wählen &quot; Sie Spielbewertungen festlegen &quot; aus.</span><span class="sxs-lookup"><span data-stu-id="823fb-164">Go back to the previous screen and select &quot;Set Game Ratings&quot;.</span></span></li>
<li><p><span data-ttu-id="823fb-165">Wählen Sie eine Bewertung aus, die niedriger als die ESRB-Bewertung des Spiels ist.</span><span class="sxs-lookup"><span data-stu-id="823fb-165">Select a rating lower than the game's ESRB Rating.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="823fb-166">Wenn das Spiel nicht bewertet wird, überspringen Sie diesen Schritt, und fahren Sie mit dem nächsten Teil dieses Tests fort.</span><span class="sxs-lookup"><span data-stu-id="823fb-166">If the game is not rated, then skip this step and move onto the next part of this test.</span></span> <span data-ttu-id="823fb-167">Es kann erforderlich sein, ein anderes Bewertungssystem zu wählen, um eine Spielbewertung zu finden. Dies hängt vom Sprachdirigenz der zu testenden SKU ab.</span><span class="sxs-lookup"><span data-stu-id="823fb-167">It may be necessary to choose a different rating system to find a game rating, depending on the language locale of the SKU being tested.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="823fb-168">Melden Sie sich als Jane ab, und melden Sie sich als Toby an.</span><span class="sxs-lookup"><span data-stu-id="823fb-168">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="823fb-169">Vergewissern Sie sich, dass das Spiel für User Toby nicht gestartet wird, wenn ESRB von User Jane blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-169">Verify that the game does not launch for User Toby when ESRB is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="823fb-170">Melden Sie sich als Toby ab, und melden Sie sich als Jane an.</span><span class="sxs-lookup"><span data-stu-id="823fb-170">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="823fb-171">Wiederherstellen Sie die ESRB-Einstellungen, wenn Sie dies zuvor geändert haben.</span><span class="sxs-lookup"><span data-stu-id="823fb-171">If changed previously, restore the ESRB settings.</span></span></li>
<li><span data-ttu-id="823fb-172">Wenn es keine ESRB-Einstellungen gibt, wählen Sie Blockieren oder Bestimmte Spiele zulassen aus, &quot; und wählen Sie das Spiel nach Namen &quot; aus.</span><span class="sxs-lookup"><span data-stu-id="823fb-172">If there are no ESRB settings, then select &quot;Block or Allow Specific Games&quot; and select the game by name.</span></span></li>
<li><span data-ttu-id="823fb-173">Melden Sie sich als Jane ab, und melden Sie sich als Toby an.</span><span class="sxs-lookup"><span data-stu-id="823fb-173">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="823fb-174">Vergewissern Sie sich, dass das Spiel für User Toby nicht gestartet wird, wenn EXE/Name von User Jane blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-174">Verify that the game does not launch for User Toby when EXE/Name is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="823fb-175">Melden Sie sich als Toby ab, und melden Sie sich wieder als Jane an.</span><span class="sxs-lookup"><span data-stu-id="823fb-175">Log off as Toby and back on as Jane.</span></span></li>
<li><span data-ttu-id="823fb-176">Öffnen Sie als Jane benutzersteuerelemente -> Anwendungseinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="823fb-176">As Jane, open User Controls -> Application Restrictions.</span></span></li>
<li><span data-ttu-id="823fb-177">Klicken Sie auf Toby kann nur die von mir zulässigen Programme verwenden, und klicken Sie auf &quot; &quot; OK (d. h. keine EXE-Dateien zulassen).</span><span class="sxs-lookup"><span data-stu-id="823fb-177">Click &quot;Toby can only use the programs I allow&quot; and click OK (that is, allow no exes).</span></span></li>
<li><span data-ttu-id="823fb-178">Wechseln Sie zu Benutzersteuerelemente | Spiele steuert und lässt das spezifische Spiel mit der ESRB-Bewertung zu.</span><span class="sxs-lookup"><span data-stu-id="823fb-178">Go to User Controls | Games Controls and allow the specific game using the ESRB rating.</span></span></li>
<li><span data-ttu-id="823fb-179">Melden Sie sich als Jane ab, melden Sie sich als Toby an, und versuchen Sie, das Spiel zu spielen.</span><span class="sxs-lookup"><span data-stu-id="823fb-179">Log off as Jane, and log on as Toby and try to play the game.</span></span></li>
<li><span data-ttu-id="823fb-180">Vergewissern Sie sich, dass das Spiel NICHT blockiert ist und dass Toby es spielen kann, wenn &quot; allow no exes &quot; festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="823fb-180">Verify that the game is NOT blocked and that Toby can play it when &quot;allow no exes&quot; is set.</span></span></li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a><span data-ttu-id="823fb-181">1.3 Windows Vista Rich Saved Games</span><span class="sxs-lookup"><span data-stu-id="823fb-181">1.3 Windows Vista Rich Saved Games</span></span>

<span data-ttu-id="823fb-182">Diese Anforderung wurde nicht mehr erfüllt.</span><span class="sxs-lookup"><span data-stu-id="823fb-182">This requirement has been retired.</span></span>

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a><span data-ttu-id="823fb-183">1.4 Xbox 360 Common Controller für bedingte \[ Windows-Anforderungen\]</span><span class="sxs-lookup"><span data-stu-id="823fb-183">1.4 Xbox 360 Common Controller for Windows \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-184">Windows 7</span></span><br/> <span data-ttu-id="823fb-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-185">Windows Vista</span></span><br/> <span data-ttu-id="823fb-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-186">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-187">Spiele, die Gamepad-Controller unterstützen, müssen den Xbox 360 Controller für Windows mithilfe der XInput-API unterstützen.</span><span class="sxs-lookup"><span data-stu-id="823fb-187">Games that support gamepad controllers must support the Xbox 360 Controller for Windows using the XInput API.</span></span> <span data-ttu-id="823fb-188">Alle Verweise auf allgemeine Controllertrigger und Schaltflächen müssen die Xbox 360 verwenden.</span><span class="sxs-lookup"><span data-stu-id="823fb-188">All references to common controller triggers and buttons must use the Xbox 360 names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="823fb-189">Starten Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="823fb-189">Launch the game.</span></span></li>
<li><span data-ttu-id="823fb-190">Wechseln Sie zu den Controlleroptionen.</span><span class="sxs-lookup"><span data-stu-id="823fb-190">Go into the controller options.</span></span> **</li>
<li><span data-ttu-id="823fb-191">Stellen Sie sicher, dass das Spiel Xbox 360 Controller für Windows als Eingabegerät erkennt.</span><span class="sxs-lookup"><span data-stu-id="823fb-191">Verify that the game recognizes Xbox 360 Controller for Windows as an input device.</span></span></li>
<li><span data-ttu-id="823fb-192">Spielen Sie das Spiel, und überprüfen Sie, ob das Spiel- und Menüsystem mit dem Xbox 360 Controller für Windows steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="823fb-192">Play the game and verify that the game and menu system are controllable with Xbox 360 Controller for Windows.</span></span></li>
<li><span data-ttu-id="823fb-193">Vergewissern Sie sich Xbox 360 dass sich der Xbox 360-Controller für Windows gemäß den akzeptierten Standards verhält.</span><span class="sxs-lookup"><span data-stu-id="823fb-193">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards.</span></span> <span data-ttu-id="823fb-194">(B für "Zurück", "A" für "Akzeptieren", "Starten" für im Spielmenü/Anhalten oder Akzeptieren usw.)</span><span class="sxs-lookup"><span data-stu-id="823fb-194">(B for back, A for accept, Start for in game menu/pause or accept, etc.)</span></span></li>
<li><span data-ttu-id="823fb-195">Stellen Sie sicher, dass das Spiel auf die Controllerschaltflächen und Trigger verweist, Xbox 360 verwenden.</span><span class="sxs-lookup"><span data-stu-id="823fb-195">Verify that the game refers to the controller buttons and triggers using Xbox 360 names.</span></span></li>
</ol>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="823fb-196">Wenn das Spiel keinen Gamecontroller unterstützt und/oder nur Tastatur/Maus unterstützt, überspringen Sie diesen Testfall.</span><span class="sxs-lookup"><span data-stu-id="823fb-196">If the game does not support a game controller and/or only supports keyboard/mouse, then skip this test case.</span></span>
</blockquote>
<br/> <span data-ttu-id="823fb-197">\*\* Einstellungen für den Controller befinden sich möglicherweise außerhalb des Spiels.</span><span class="sxs-lookup"><span data-stu-id="823fb-197">\*\* Settings for the controller might be located outside of the game.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a><span data-ttu-id="823fb-198">1.5 Mehrere Seitenverhältnisse und Auflösungen</span><span class="sxs-lookup"><span data-stu-id="823fb-198">1.5 Multiple Aspect Ratios and Resolutions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-199">Windows 7</span></span><br/> <span data-ttu-id="823fb-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-200">Windows Vista</span></span><br/> <span data-ttu-id="823fb-201">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-201">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-202">Das Spiel muss mindestens die folgenden Seitenverhältnisse und die zugehörigen Bildschirmauflösungen unterstützen:</span><span class="sxs-lookup"><span data-stu-id="823fb-202">The game must support at least the following aspect ratios and associated screen resolutions:</span></span> <br/>
<ul>
<li><span data-ttu-id="823fb-203">4:3 &quot; normal &quot; (800 600 oder 1024 768)</span><span class="sxs-lookup"><span data-stu-id="823fb-203">4:3 &quot;normal&quot; (800 600 or 1024 768)</span></span></li>
<li><span data-ttu-id="823fb-204">16:9 &quot; Widescreen &quot; (1280 720)</span><span class="sxs-lookup"><span data-stu-id="823fb-204">16:9 &quot;widescreen&quot; (1280 720)</span></span></li>
<li><span data-ttu-id="823fb-205">16:10 &quot; Widescreen &quot; (1152 720, 1680 1050 oder 800 480)</span><span class="sxs-lookup"><span data-stu-id="823fb-205">16:10 &quot;widescreen&quot; (1152 720, 1680 1050, or 800 480)</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="823fb-206">Suchen Sie nach den Videooptionen für das Spiel (dies kann in unserem Out-of-Game sein).</span><span class="sxs-lookup"><span data-stu-id="823fb-206">Locate the Video Options for the game (this may be in our out of game).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="823fb-207">Die folgenden Tests müssen auf einem Widescreen-Monitor durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-207">The following tests must be done on a widescreen monitor.</span></span>
</blockquote>
<br/>
<ol>
<li><span data-ttu-id="823fb-208">Wählen Sie im Abschnitt Videoauflösung die Option 800 600 oder 1024 768 aus.</span><span class="sxs-lookup"><span data-stu-id="823fb-208">In the video resolution section, select 800 600 or 1024 768.</span></span></li>
<li><span data-ttu-id="823fb-209">Überprüfen Sie, ob das Spiel mit einer Auflösung von 4:3 Seitenverhältnis ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-209">Verify that the game runs at a 4:3 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="823fb-210">Wählen Sie im Abschnitt video resolution (Videoauflösung) die Option 1280 720 aus.</span><span class="sxs-lookup"><span data-stu-id="823fb-210">In the video resolution section, select 1280 720.</span></span></li>
<li><span data-ttu-id="823fb-211">Vergewissern Sie sich, dass das Spiel mit einer Auflösung von 16:9 Seitenverhältnis ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-211">Verify that the game runs at a 16:9 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="823fb-212">Wählen Sie im Abschnitt Videoauflösung die Option 1680 1050, 800 480 oder 1152 720 aus.</span><span class="sxs-lookup"><span data-stu-id="823fb-212">In the video resolution section, select 1680 1050, 800 480, or 1152 720.</span></span></li>
<li><span data-ttu-id="823fb-213">Stellen Sie sicher, dass das Spiel mit einer Auflösung von 16:10 Seitenverhältnis ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-213">Verify that the game runs at a 16:10 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="823fb-214">Stellen Sie sicher, dass das Spiel das Bild nicht streckt und wiederum einen breiteren Ansichtsbereich zeigt.</span><span class="sxs-lookup"><span data-stu-id="823fb-214">Verify that the game does not stretch the picture and in turn presents a wider area of view.</span></span></li>
<li><span data-ttu-id="823fb-215">Stellen Sie sicher, dass der Benutzer vom Spiel aufgefordert wird, wenn eine Änderung an der Lösung vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-215">Verify that the game prompts the user when a change is made to the resolution.</span></span></li>
<li><span data-ttu-id="823fb-216">Wenn der Benutzer nicht innerhalb von 15 Sekunden akzeptiert, stellen Sie sicher, dass die Anzeige auf die vorherige Einstellung zurückverwendet wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-216">If the user does not accept within 15 seconds, verify that the display reverts to the previous setting.</span></span></li>
<li><span data-ttu-id="823fb-217">Stellen Sie sicher, dass das Spiel links und rechts vom Spielbereich keine schwarzen Balken hinzufüge.</span><span class="sxs-lookup"><span data-stu-id="823fb-217">Verify that the game does not add black bars to the left and right of the game play area.</span></span> <span data-ttu-id="823fb-218">(In diesem Fall wird der Spielbereich in der Mitte des Bildschirms noch im Verhältnis 4:3 angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="823fb-218">(In this case, you will see the game area still in a 4:3 ratio in the middle of the screen.)</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a><span data-ttu-id="823fb-219">1.6 Windows Media Center</span><span class="sxs-lookup"><span data-stu-id="823fb-219">1.6 Windows Media Center</span></span>

<span data-ttu-id="823fb-220">Diese Anforderung wurde nicht mehr erfüllt.</span><span class="sxs-lookup"><span data-stu-id="823fb-220">This requirement has been retired.</span></span>

### <a name="17-direct3d-conditional-requirement"></a><span data-ttu-id="823fb-221">1.7 Bedingte \[ Direct3D-Anforderung\]</span><span class="sxs-lookup"><span data-stu-id="823fb-221">1.7 Direct3D \[Conditional Requirement\]</span></span>



| <span data-ttu-id="823fb-222">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="823fb-222">OS</span></span>                                                                    | <span data-ttu-id="823fb-223">Anforderung</span><span class="sxs-lookup"><span data-stu-id="823fb-223">Requirement</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="823fb-224">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-224">Windows 7</span></span><br/> <span data-ttu-id="823fb-225">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-225">Windows Vista</span></span><br/> <span data-ttu-id="823fb-226">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-226">Windows XP</span></span><br/> | <span data-ttu-id="823fb-227">Wenn das Spiel Direct3D verwendet, muss die unterstützte Mindestversion Direct3D 9 und Direct3D der Standard für jede Anzeigekonfigurationsoption sein.</span><span class="sxs-lookup"><span data-stu-id="823fb-227">If the game uses Direct3D, the minimum version supported must be Direct3D 9, and Direct3D must be the default for any display configuration option.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|     <dl> <span data-ttu-id="823fb-228"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuell</dt></span><span class="sxs-lookup"><span data-stu-id="823fb-228"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt></span></span> <dd> <span data-ttu-id="823fb-229">Starten Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="823fb-229">Launch the game.</span></span> <span data-ttu-id="823fb-230">Überprüfen Sie in den Videooptionen, ob Renderoptionen wie D3D und/oder OpenGL verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="823fb-230">In the video options, check to see if there are render options, D3D and/or OpenGL.</span></span> <span data-ttu-id="823fb-231">Wenn dies der Standard ist, überprüfen Sie, ob die Renderoptionen für das Spiel direct3D sind.</span><span class="sxs-lookup"><span data-stu-id="823fb-231">If there are, verify that the game render options default to Direct3D.</span></span> <span data-ttu-id="823fb-232">Wenn Sie nicht überprüfen können, ob D3D9 die verwendete DirectX-Version ist, fahren Sie mit Automatisierter Test fort.</span><span class="sxs-lookup"><span data-stu-id="823fb-232">If you are unable to verify that D3D9 is the version of DirectX that is being used, then proceed to Automated Test.</span></span> <br/> </dd> <span data-ttu-id="823fb-233"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automatisierter Test</dt></span><span class="sxs-lookup"><span data-stu-id="823fb-233"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt></span></span> <dd> <span data-ttu-id="823fb-234">Tool verwenden: Depends.exe</span><span class="sxs-lookup"><span data-stu-id="823fb-234">Use tool: Depends.exe</span></span> <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a><span data-ttu-id="823fb-235">1.8 Aktivieren von "High-DPI Aware" (Hohe DPI-Leistung)</span><span class="sxs-lookup"><span data-stu-id="823fb-235">1.8 Enable High-DPI Aware</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-236">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-236">Windows 7</span></span><br/> <span data-ttu-id="823fb-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-237">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="823fb-238">Spiele und ihre Installationsprogramme müssen ohne visuelle Probleme ordnungsgemäß ausgeführt werden, wenn die DPI-Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="823fb-238">Games and their installers must run correctly without visual problems when DPI scaling is enabled.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="823fb-239"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuell</dt> </span><span class="sxs-lookup"><span data-stu-id="823fb-239"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="823fb-240">Legen Sie das System auf DPI 150 % fest:</span><span class="sxs-lookup"><span data-stu-id="823fb-240">Set the system to DPI 150%:</span></span> <br/> <span data-ttu-id="823fb-241">Windows Vista: Systemsteuerung: Personalisierung, Anpassen des Schriftgrads (DPI), BenutzerdefinierteR DPI.</span><span class="sxs-lookup"><span data-stu-id="823fb-241">Windows Vista: Control Panel: Personalization, Adjust font size (DPI), Custom DPI.</span></span> <span data-ttu-id="823fb-242">Legen Sie auf 150 % fest.</span><span class="sxs-lookup"><span data-stu-id="823fb-242">Set to 150%.</span></span><br/> <span data-ttu-id="823fb-243">Windows 7: Systemsteuerung: Display, Set to Larger - 150%.</span><span class="sxs-lookup"><span data-stu-id="823fb-243">Windows 7: Control Panel: Display, Set to Larger - 150%.</span></span><br/></li>
<li><span data-ttu-id="823fb-244">Führen Sie den Installationsvorgang und das Spiel aus, um sicherzustellen, dass keine Probleme mit abgeschnittenen Bildschirmen oder Dialogfeldern auftreten.</span><span class="sxs-lookup"><span data-stu-id="823fb-244">Run the installation process and game to verify there are no problems with clipped screens or dialog boxes.</span></span></li>
</ol>
</dd> <span data-ttu-id="823fb-245"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automatisierter Test</dt> </span><span class="sxs-lookup"><span data-stu-id="823fb-245"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="823fb-246">Stellen Sie sicher, <dpiAware>dass das Element true</dpiAware> im eingebetteten Manifest enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="823fb-246">Verify that element <dpiAware>true</dpiAware> is contained in the embedded manifest.</span></span><br/> <span data-ttu-id="823fb-247">Tool verwenden: Mt.exe</span><span class="sxs-lookup"><span data-stu-id="823fb-247">Use tool: Mt.exe</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a><span data-ttu-id="823fb-248">2. Sicherheit und Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="823fb-248">2. Security and Compatibility</span></span>

### <a name="21-follow-user-account-control-guidelines"></a><span data-ttu-id="823fb-249">2.1 Befolgen Sie die Richtlinien für die Benutzerkontensteuerung.</span><span class="sxs-lookup"><span data-stu-id="823fb-249">2.1 Follow User Account Control Guidelines</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-250">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-250">Windows 7</span></span><br/> <span data-ttu-id="823fb-251">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-251">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="823fb-252">Jede ausführbare Datei (.EXE Erweiterung), die in einer Anwendung enthalten ist, muss über ein eingebettetes Manifest verfügen, das die Ausführungsebene definiert:</span><span class="sxs-lookup"><span data-stu-id="823fb-252">Every executable file (.EXE extension) included with an application must have an embedded manifest that defines its execution level:</span></span>
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="823fb-253">Bei Spielen und Spieleinstallern sollte uiAccess immer auf FALSE festgelegt &quot; &quot; werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-253">For games and game installers, uiAccess should always be set to &quot;false&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="823fb-254">Überprüfen Sie, ob ausführbare Dateien des Spiels Manifeste enthalten.</span><span class="sxs-lookup"><span data-stu-id="823fb-254">Verify game executable files contain manifests.</span></span></li>
<li><span data-ttu-id="823fb-255">Vergewissern Sie sich, dass das ausführbare Dateimanifest des Spiels requestedExecutionLevel &quot; auf AsInvokerfestlegt &quot; ist.</span><span class="sxs-lookup"><span data-stu-id="823fb-255">Verify game executable file manifest requestedExecutionLevel is &quot;AsInvoker&quot;.</span></span></li>
</ol>
<span data-ttu-id="823fb-256">Tool verwenden: Mt.exe</span><span class="sxs-lookup"><span data-stu-id="823fb-256">Use tool: Mt.exe</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a><span data-ttu-id="823fb-257">2.2 Unterstützung von x64-Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="823fb-257">2.2 Support x64 Versions of Windows</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-258">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-258">Windows 7</span></span><br/> <span data-ttu-id="823fb-259">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-259">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="823fb-260">So gewährleisten Sie die Kompatibilität mit x64-Versionen von Windows:</span><span class="sxs-lookup"><span data-stu-id="823fb-260">To maintain compatibility with x64 versions of Windows:</span></span> <br/>
<ul>
<li><span data-ttu-id="823fb-261">Titel- und Titelinstallationsprogramme dürfen keinen 16-Bit-Code enthalten oder 16-Bit-Komponenten verwenden.</span><span class="sxs-lookup"><span data-stu-id="823fb-261">Titles and title installers must not contain any 16-bit code or rely on any 16-bit component.</span></span></li>
<li><span data-ttu-id="823fb-262">Wenn das Spiel für den Betrieb von Kernelmodustreibern abhängig ist, müssen x64-Versionen dieser Treiber verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="823fb-262">If the game is dependent on kernel-mode drivers for operation, x64 versions of these drivers must be available.</span></span> <span data-ttu-id="823fb-263">Das Spielsetup muss die richtigen Treiber und Komponenten für 64-Bit-Editionen von Windows erkennen und installieren.</span><span class="sxs-lookup"><span data-stu-id="823fb-263">The game setup must detect and install the proper drivers and components for 64-bit editions of Windows.</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="823fb-264">Die Unterstützung für die 64-Bit-Edition von Windows XP Professional ist optional.</span><span class="sxs-lookup"><span data-stu-id="823fb-264">Support for the 64-bit Edition of Windows XP Professional is optional.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="823fb-265">Manueller Test</span><span class="sxs-lookup"><span data-stu-id="823fb-265">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="823fb-266">Führen Sie das Spiel auf 64-Bit-Editionen von Windows aus.</span><span class="sxs-lookup"><span data-stu-id="823fb-266">Run the game on 64-bit editions of Windows.</span></span> <span data-ttu-id="823fb-267">Stellen Sie sicher, dass der Spielinstallationsprozess normal auf 64-Bit-Editionen von Windows Vista oder Windows 7 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-267">Verify that the game installation process runs normally on 64-bit editions of Windows Vista or Windows 7.</span></span></li>
<li><span data-ttu-id="823fb-268">Stellen Sie sicher, dass für das Spiel kein Fehler als Ergebnis von ausführbaren 16-Bit-Dateien in 64-Bit-Editionen von Windows Vista oder Windows 7 auftritt.</span><span class="sxs-lookup"><span data-stu-id="823fb-268">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista or Windows 7.</span></span> <span data-ttu-id="823fb-269">Der Fehler erwähnt die 16-Bit-Anwendung im Fehlerfenster.</span><span class="sxs-lookup"><span data-stu-id="823fb-269">The error will mention the 16-bit application in the error window.</span></span></li>
<li><span data-ttu-id="823fb-270">Wenn das Spiel über eine native ausführbare 64-Bit-Datei verfügt, verwenden Sie diese auch.</span><span class="sxs-lookup"><span data-stu-id="823fb-270">If the game has a native 64-bit executable, then use that as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a><span data-ttu-id="823fb-271">2.3 Signieren von Dateien</span><span class="sxs-lookup"><span data-stu-id="823fb-271">2.3 Sign Files</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-272">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-272">Windows 7</span></span><br/> <span data-ttu-id="823fb-273">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-273">Windows Vista</span></span><br/> <span data-ttu-id="823fb-274">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-274">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-275">Alle ausführbaren Codedateien (z. B. .exe erweiterungen .dll) müssen mit einem Authenticode-Zertifikat signiert sein.</span><span class="sxs-lookup"><span data-stu-id="823fb-275">All executable code files (for example, .exe and .dll extensions) must be signed with an Authenticode certificate.</span></span> <br/> <span data-ttu-id="823fb-276">Wenn Sie Windows Installer, müssen die Paketdateien (.msi Dateien) des Installationsprogramms signiert sein.</span><span class="sxs-lookup"><span data-stu-id="823fb-276">If you are using Windows Installer, the installer's package files (.msi files) must be signed.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="823fb-277">Manueller Test</span><span class="sxs-lookup"><span data-stu-id="823fb-277">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="823fb-278">Navigieren Sie zum Spielverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="823fb-278">Navigate to the game directory.</span></span></li>
<li><span data-ttu-id="823fb-279">Suchen Sie nach allen .exe und .dll Dateien.</span><span class="sxs-lookup"><span data-stu-id="823fb-279">Locate all of the .exe and .dll files.</span></span></li>
<li><span data-ttu-id="823fb-280">Klicken Sie für jede Datei mit der rechten Maustaste auf Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="823fb-280">Right-click Properties on each file.</span></span></li>
<li><span data-ttu-id="823fb-281">Überprüfen Sie, ob die ausführbaren Dateien des Spiels eine digitale Signatur enthalten.</span><span class="sxs-lookup"><span data-stu-id="823fb-281">Verify that the game executable files contain a digital signature.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a><span data-ttu-id="823fb-282">2.4 Signieren von Treibern</span><span class="sxs-lookup"><span data-stu-id="823fb-282">2.4 Sign Drivers</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-283">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-283">Windows 7</span></span><br/> <span data-ttu-id="823fb-284">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-284">Windows Vista</span></span><br/> <span data-ttu-id="823fb-285">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-285">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-286">Jeder Kernelmodustreiber, der vom Spiel installiert wird, muss mit einem öffentlich gültigen Authenticode-Zertifikat signiert werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-286">Any kernel-mode driver that is installed by the game must be signed with a publicly valid Authenticode certificate.</span></span> <br/> <span data-ttu-id="823fb-287">Jeder Hardwaregerätetreiber im Kernelmodus, der vom Spiel installiert wird, muss über eine Microsoft-Signatur verfügen, die über das Windows Hardware Quality Labs-Programm (WHQL) oder drS-Programm (Driver Reliability Signature) erworben wurde.</span><span class="sxs-lookup"><span data-stu-id="823fb-287">Any kernel-mode hardware device driver that is installed by the game must have a Microsoft signature obtained through the Windows Hardware Quality Labs (WHQL) or Driver Reliability Signature (DRS) program.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="823fb-288">Manueller Test</span><span class="sxs-lookup"><span data-stu-id="823fb-288">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="823fb-289">Installieren Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="823fb-289">Install the game.</span></span></li>
<li><span data-ttu-id="823fb-290">Vergewissern Sie sich, dass bei der Installation des Spiels keine Dialogfelder mit nicht signierten Treibern angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-290">Verify that the game install process does not display unsigned driver dialog(s).</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a><span data-ttu-id="823fb-291">2.5 Ordnungsgemäßes Durchführen der Versionsüberprüfung</span><span class="sxs-lookup"><span data-stu-id="823fb-291">2.5 Perform Version Checking Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-292">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-292">Windows 7</span></span><br/> <span data-ttu-id="823fb-293">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-293">Windows Vista</span></span><br/> <span data-ttu-id="823fb-294">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-294">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-295">Spiele dürfen nicht auf zukünftigen Betriebssystemen ausgeführt werden, wie durch Änderungen an der Windows-Versionsnummer angegeben, es sei denn, der Endbenutzer-Lizenzvertrag untersagt die Verwendung auf zukünftigen Betriebssystemen.</span><span class="sxs-lookup"><span data-stu-id="823fb-295">Games must not fail to run on future operating systems as indicated by changes in the Windows version number, unless the End User License Agreement prohibits use on future operating systems.</span></span> <span data-ttu-id="823fb-296">Wenn das Spiel fehlschlagen soll, muss es dies ordnungsgemäß tun, indem dem Benutzer eine Meldung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-296">If the game is supposed to fail, it must do so gracefully by displaying a message to the user.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="823fb-297"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuell</dt> </span><span class="sxs-lookup"><span data-stu-id="823fb-297"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="823fb-298">Installieren Sie das Spiel unter Windows XP, auf 32-Bit-Editionen von Windows Vista und Windows 7 sowie auf 64-Bit-Editionen von Windows Vista und Windows 7.</span><span class="sxs-lookup"><span data-stu-id="823fb-298">Install the game on Windows XP, on 32-bit editions of Windows Vista and Windows 7, and on 64-bit editions of Windows Vista and Windows 7.</span></span></li>
<li><span data-ttu-id="823fb-299">Stellen Sie sicher, dass bei der Spieleinstallation kein Fehler in Bezug auf die Betriebssystemversion auftritt.</span><span class="sxs-lookup"><span data-stu-id="823fb-299">Verify that the game installation process does not encounter an error regarding OS version.</span></span></li>
</ol>
</dd> <span data-ttu-id="823fb-300"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automatisierter Test</dt> </span><span class="sxs-lookup"><span data-stu-id="823fb-300"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="823fb-301">Tool verwenden: Application Verifier</span><span class="sxs-lookup"><span data-stu-id="823fb-301">Use tool: Application Verifier</span></span><br/>
<ol>
<li><span data-ttu-id="823fb-302">Starten Application Verifier.</span><span class="sxs-lookup"><span data-stu-id="823fb-302">Launch Application Verifier.</span></span></li>
<li><span data-ttu-id="823fb-303">Aktivieren Sie den Test Compatibility:HighVersionLie, nachdem Sie die INSTALL.EXE.</span><span class="sxs-lookup"><span data-stu-id="823fb-303">Enable the Compatibility:HighVersionLie test after selecting the INSTALL.EXE.</span></span></li>
<li><span data-ttu-id="823fb-304">Installieren Sie das Spiel, und stellen Sie sicher, dass die Installation nicht basierend auf der Betriebssystemversion blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-304">Install the game and ensure that it does not block installation based on the OS version.</span></span></li>
<li><span data-ttu-id="823fb-305">Aktivieren Sie den Test Compatibility:HighVersionLie, nachdem Sie die GAME.EXE.</span><span class="sxs-lookup"><span data-stu-id="823fb-305">Enable the Compatibility:HighVersionLie test after selecting the GAME.EXE.</span></span></li>
<li><span data-ttu-id="823fb-306">Führen Sie das Spiel aus, und stellen Sie sicher, dass die Ausführung nicht basierend auf der Betriebssystemversion blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-306">Run the game and ensure it does not block execution based on the OS version.</span></span></li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a><span data-ttu-id="823fb-307">2.6 Unterstützung gleichzeitiger Benutzersitzungen</span><span class="sxs-lookup"><span data-stu-id="823fb-307">2.6 Support Concurrent User Sessions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-308">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-308">Windows 7</span></span><br/> <span data-ttu-id="823fb-309">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-309">Windows Vista</span></span><br/> <span data-ttu-id="823fb-310">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-310">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-311">Spiele müssen Standardmäßige Windows-Multitaskingszenarien unterstützen.</span><span class="sxs-lookup"><span data-stu-id="823fb-311">Games must support standard Windows multitasking scenarios.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="823fb-312">Erstellen Sie in Windows Vista oder Windows 7 ein Standardbenutzerkonto namens Toby.</span><span class="sxs-lookup"><span data-stu-id="823fb-312">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="823fb-313">Start -> Systemsteuerung -> Add or Remove User Accounts -> Create New Account</span><span class="sxs-lookup"><span data-stu-id="823fb-313">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span> <br/>
<ol>
<li><span data-ttu-id="823fb-314">Starten Sie das Spiel als User Jane.</span><span class="sxs-lookup"><span data-stu-id="823fb-314">Launch the game as User Jane.</span></span></li>
<li><span data-ttu-id="823fb-315">ALT+TAB zurück zum Desktop.</span><span class="sxs-lookup"><span data-stu-id="823fb-315">ALT+TAB back to the desktop.</span></span></li>
<li><span data-ttu-id="823fb-316">Vergewissern Sie sich, dass das Spiel ordnungsgemäß ALT+TABs auf dem Windows-Desktop installiert.</span><span class="sxs-lookup"><span data-stu-id="823fb-316">Verify that the game properly ALT+TABs to the Windows desktop.</span></span></li>
<li><span data-ttu-id="823fb-317">Klicken Sie auf Start -> [Pfeil rechts neben Sperren] -> Benutzer wechseln.</span><span class="sxs-lookup"><span data-stu-id="823fb-317">Click Start -> [arrow to the right of Lock] -> Switch User.</span></span></li>
<li><span data-ttu-id="823fb-318">Melden Sie sich als User Toby an.</span><span class="sxs-lookup"><span data-stu-id="823fb-318">Log on as User Toby.</span></span></li>
<li><span data-ttu-id="823fb-319">Vergewissern Sie sich, dass das Spiel als User Toby gestartet wird, während es weiterhin als User Jane ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-319">Verify that the game launches as User Toby while still running as User Jane.</span></span></li>
<li><span data-ttu-id="823fb-320">Stellen Sie sicher, dass im Spiel während des Benutzerwechselvorgangs keine Fehler für User Toby oder User Jane auftreten.</span><span class="sxs-lookup"><span data-stu-id="823fb-320">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process.</span></span></li>
<li><span data-ttu-id="823fb-321">Wenn Sie eine weitere Spielsitzung starten können, vergewissern Sie sich, dass Sie keine Audiodaten aus der ursprünglichen Spielsitzung hören können.</span><span class="sxs-lookup"><span data-stu-id="823fb-321">If you can launch another game session, verify that you cannot hear audio from the original game session.</span></span></li>
<li><span data-ttu-id="823fb-322">Schließen Sie das Spiel, und wechseln Sie zurück zum ursprünglichen Benutzer und Spiel.</span><span class="sxs-lookup"><span data-stu-id="823fb-322">Close the game and switch back to the original user and game.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a><span data-ttu-id="823fb-323">2.7 Unterstützung für lange Namen</span><span class="sxs-lookup"><span data-stu-id="823fb-323">2.7 Support Long Names</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-324">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-324">Windows 7</span></span><br/> <span data-ttu-id="823fb-325">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-325">Windows Vista</span></span><br/> <span data-ttu-id="823fb-326">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-326">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-327">Wenn ein Spiel das Speichern von Dateien unterstützt, muss es in der Lage sein, Dateien mit langen Namen und Pfaden zu speichern.</span><span class="sxs-lookup"><span data-stu-id="823fb-327">If a game supports saving files, it must be able to save files that have long names and paths.</span></span> <span data-ttu-id="823fb-328">Das Spiel muss spezielle Dateisystemzeichen ordnungsgemäß verarbeiten, z. B. \ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="823fb-328">The game must properly handle special file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="823fb-329">&quot; < oder > in allen Benutzereingabefeldern, die zum Erstellen von Dateinamen oder Pfaden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-329">&quot; < or > in any user input fields used to create file names or paths.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="823fb-330">Starten Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="823fb-330">Launch the game.</span></span></li>
<li><span data-ttu-id="823fb-331">Starten Sie ein neues Spiel.</span><span class="sxs-lookup"><span data-stu-id="823fb-331">Start a new game.</span></span></li>
<li><span data-ttu-id="823fb-332">Speichern Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="823fb-332">Save the game.</span></span> <span data-ttu-id="823fb-333">Vergewissern Sie sich während des Speichervorgangs, dass das Spiel mit dem Speichernamen "My First Save Game" (Mein erstes Spiel speichern) speichert.</span><span class="sxs-lookup"><span data-stu-id="823fb-333">During the save process, verify that the game saves using the save name: My First Save Game.</span></span></li>
<li><span data-ttu-id="823fb-334">Beenden Sie zurück zum Hauptmenü.</span><span class="sxs-lookup"><span data-stu-id="823fb-334">Exit back to the main menu.</span></span></li>
<li><span data-ttu-id="823fb-335">Versuchen Sie, das neu gespeicherte Spiel zu laden.</span><span class="sxs-lookup"><span data-stu-id="823fb-335">Attempt to load the newly saved game.</span></span></li>
<li><span data-ttu-id="823fb-336">Stellen Sie sicher, dass beim Behandeln von nicht unterstützten Dateisystemzeichen keine Fehler auftreten, z. B. \ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="823fb-336">Verify that the game does not encounter errors when handling unsupported file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="823fb-337">&quot; < oder > Wenn das Spiel Es zulässt, benennen Sie das gespeicherte Spiel.</span><span class="sxs-lookup"><span data-stu-id="823fb-337">&quot; < or > If the game allows you, name the saved game.</span></span></li>
<li><span data-ttu-id="823fb-338">Wenn der Benutzer sein Profil benennen und/oder Zeichen verwenden oder Spiele speichern darf, stellen Sie sicher, dass beim Spiel auch hier keine Fehler auftreten, wenn lange Dateinamen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-338">If the user is allowed to name their profile and/or character or save games, verify that the game does not encounter errors when using long file names here as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a><span data-ttu-id="823fb-339">3. Installation</span><span class="sxs-lookup"><span data-stu-id="823fb-339">3. Installation</span></span>

### <a name="31-easy-install"></a><span data-ttu-id="823fb-340">3.1 Einfache Installation</span><span class="sxs-lookup"><span data-stu-id="823fb-340">3.1 Easy Install</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-341">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-341">Windows 7</span></span><br/> <span data-ttu-id="823fb-342">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-342">Windows Vista</span></span><br/> <span data-ttu-id="823fb-343">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-343">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-344">Spiele mit einer herkömmlichen Installation müssen einen vereinfachten Pfad in ihrer Setup-Benutzeroberfläche bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="823fb-344">Games with a traditional installation must provide a simplified path in their setup user interface.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="823fb-345">Fügen Sie den Spiel-Datenträger ein.</span><span class="sxs-lookup"><span data-stu-id="823fb-345">Insert the game disc.</span></span></li>
<li><span data-ttu-id="823fb-346">Vergewissern Sie sich, dass im Spiel nicht mehr als ein lizenzvertrag End-User angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-346">Verify that the game does not display more than one End-User License Agreement (EULA).</span></span></li>
<li><span data-ttu-id="823fb-347">Wenn das Spiel eine benutzerdefinierte oder erweiterte Installationsoption unterstützt, überprüfen Sie, ob während des Installationsvorgangs auf diese Option zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="823fb-347">If the game supports a custom or advanced installation option, verify that this option is accessible during the installation process.</span></span></li>
<li><span data-ttu-id="823fb-348">Stellen Sie sicher, dass die Option Standardinstallation alle Benutzereingabeauswahlen für den Installationsvorgang umgeht (Auswahl des Installationsordners, Auswahl von Komponenten und so weiter).</span><span class="sxs-lookup"><span data-stu-id="823fb-348">Verify that the Default installation option bypasses all user input selections for the installation process (selection of installation folder, components selection, and so on).</span></span></li>
<li><span data-ttu-id="823fb-349">Stellen Sie sicher, dass bei der Spieleinstallation keine Aufforderung zur Einrichtung von Betriebssystemkomponenten angezeigt wird (DirectX-Setup, Visual C-Runtimes und so weiter).</span><span class="sxs-lookup"><span data-stu-id="823fb-349">Verify that the game installation process does not prompt for OS component setup (DirectX setup, Visual C Runtimes, and so on).</span></span></li>
<li><span data-ttu-id="823fb-350">Stellen Sie sicher, dass bei der Spieleinstallation keine Aufforderung zur Firewallinteraktion angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-350">Verify that the game installation process does not prompt for firewall interaction.</span></span></li>
<li><span data-ttu-id="823fb-351">Vergewissern Sie sich, dass das Spiel automatisch ausgeführt wird oder dass am Ende des Installationsprozesses ein Startmenü vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="823fb-351">Verify that the game automatically runs or that a launcher menu is present at the end of the install process.</span></span></li>
<li><span data-ttu-id="823fb-352">Stellen Sie sicher, dass beim Deinstallationsprozess des Spiels alle installierten, nicht neu verteilten Betriebssystemkomponentendateien entfernt und alle Einstellungen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-352">Verify that the game uninstallation process removes all installed, non-redistributed OS component files and clears all settings.</span></span> <span data-ttu-id="823fb-353">Das Bereinigen aller Einstellungen und Daten pro Benutzer (z. B. gespeicherte Spiele) ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="823fb-353">Cleaning up all per-user settings and data (such as saved games) is not required.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a><span data-ttu-id="823fb-354">3.2 Unterstützung der Benutzerkontensteuerung für die Installation</span><span class="sxs-lookup"><span data-stu-id="823fb-354">3.2 Support User Account Control for Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-355">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-355">Windows 7</span></span><br/> <span data-ttu-id="823fb-356">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-356">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="823fb-357">Der Spieleinstaller darf nicht davon ausgehen, dass er im gleichen Kontext wie der Benutzer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-357">The game installer must not assume it is running in the same context as the user.</span></span> <span data-ttu-id="823fb-358">Spiele müssen daher aufgaben pro Benutzer bei der ersten Ausführung getrennt von der Installation ausführen.</span><span class="sxs-lookup"><span data-stu-id="823fb-358">Games must therefore perform per-user tasks on first-run separately from the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="823fb-359">Vergewissern Sie sich, dass Sie das Spiel als User Jane installieren können.</span><span class="sxs-lookup"><span data-stu-id="823fb-359">Verify that you can install the game as User Jane.</span></span> <span data-ttu-id="823fb-360">(Dies erfordert erhöhte Rechte während des Setup-/Installationsprozesses.)</span><span class="sxs-lookup"><span data-stu-id="823fb-360">(This will require elevated rights during the setup/installation process.)</span></span></li>
<li><span data-ttu-id="823fb-361">Vergewissern Sie sich, dass benutzerin Jane während der Spieleinstallation aufgefordert wird, die Rechte mit Administratoranmeldeinformationen zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="823fb-361">Verify that the game installation process prompts User Jane to elevate through Administrator Credentials.</span></span> <span data-ttu-id="823fb-362">(Die Aufforderung zum Erhöhen der Rechte wird angezeigt, wenn der Benutzer versucht, die Installation zu versuchen.)</span><span class="sxs-lookup"><span data-stu-id="823fb-362">(The prompt to elevate will come up when the user attempts to install.)</span></span></li>
<li><span data-ttu-id="823fb-363">Entscheiden Sie sich dafür, das Spiel am Ende der Installation automatisch zu erstellen, falls dies noch nicht der Dere ist, oder starten Sie es über das angezeigte Menü.</span><span class="sxs-lookup"><span data-stu-id="823fb-363">Opt to Autorun the game at the end of installation, if it does not already do so, or launch it from the menu that appears.</span></span></li>
<li><span data-ttu-id="823fb-364">Erstellen Sie nach dem Spiel ein neues Profil, spielen Sie ein Spiel, und speichern Sie es.</span><span class="sxs-lookup"><span data-stu-id="823fb-364">Once in-game, create a new profile, play and save a game.</span></span></li>
<li><span data-ttu-id="823fb-365">Beenden Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="823fb-365">Exit the game.</span></span></li>
<li><span data-ttu-id="823fb-366">Starten Sie das Spiel neu, und überprüfen Sie, ob das User Jane-Konto auf Benutzerprofile und gespeicherte Spiele zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="823fb-366">Restart the game and verify that User Profiles and Saved Games can be accessed by the User Jane account.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a><span data-ttu-id="823fb-367">3.3 Installieren in korrekten Ordnern</span><span class="sxs-lookup"><span data-stu-id="823fb-367">3.3 Install to Correct Folders</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-368">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-368">Windows 7</span></span><br/> <span data-ttu-id="823fb-369">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-369">Windows Vista</span></span><br/> <span data-ttu-id="823fb-370">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-370">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-371">Spiele müssen standardmäßig im Ordner "Programme" installiert werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-371">Games must be installed to the Program Files folder by default.</span></span> <span data-ttu-id="823fb-372">Benutzerdaten müssen bei der ersten Ausführung und nicht während der Installation geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-372">User data must be written at first run and not during the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="823fb-373">Installieren Sie das Spiel mithilfe des Standard-Installationstyps.</span><span class="sxs-lookup"><span data-stu-id="823fb-373">Install the game using the Default install type.</span></span></li>
<li><span data-ttu-id="823fb-374">Vergewissern Sie sich, dass das Spiel unter Programme installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="823fb-374">Verify that the game was installed to Program Files.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="823fb-375">Wenn dieser Test fehlschlägt, überprüfen Sie, ob das Spiel für alle Benutzer installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="823fb-375">If this test fails, verify that the game is intended to install for All Users.</span></span> <span data-ttu-id="823fb-376">Wenn dies der Fall ist, ist dies ein Fehler.</span><span class="sxs-lookup"><span data-stu-id="823fb-376">If so, this is a failure.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a><span data-ttu-id="823fb-377">3.4 Ordnungsgemäßes Installieren von Windows-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="823fb-377">3.4 Install Windows Resources Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-378">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-378">Windows 7</span></span><br/> <span data-ttu-id="823fb-379">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-379">Windows Vista</span></span><br/> <span data-ttu-id="823fb-380">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-380">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-381">Anwendungen dürfen nicht versuchen, Dateien oder Registrierungsschlüssel zu installieren, die durch Windows-Ressourcenschutz (WRP) geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="823fb-381">Applications must not attempt to install files or registry keys that are protected by Windows Resource Protection (WRP).</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="823fb-382">Stellen Sie sicher, Windows-Ressourcenschutz WRP-Dialogfelder während des Installationsprozesses nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-382">Verify that no Windows Resource Protection WRP dialog boxes appear during the installation process.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a><span data-ttu-id="823fb-383">3.5 Vermeiden von Neustarts während der Installation</span><span class="sxs-lookup"><span data-stu-id="823fb-383">3.5 Avoid Reboots During Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-384">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-384">Windows 7</span></span><br/> <span data-ttu-id="823fb-385">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-385">Windows Vista</span></span><br/> <span data-ttu-id="823fb-386">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-386">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-387">Das Spieleinstallationsprogramm sollte nicht davon ausgehen, dass die Installation von Windows-Komponenten aus Weiterverteilungspaketen einen Neustart erfordert, es sei denn, der Neustart wird durch ein Rückgabeergebnis oder in der Microsoft-Dokumentation angegeben.</span><span class="sxs-lookup"><span data-stu-id="823fb-387">The game installer should not assume that installation of Windows components from redistribution packages requires a reboot, unless the reboot is indicated by a return result or by Microsoft documentation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="823fb-388">Installieren Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="823fb-388">Install the game.</span></span></li>
<li><span data-ttu-id="823fb-389">Stellen Sie sicher, dass das System nach der Installation nicht neu gestartet werden muss.</span><span class="sxs-lookup"><span data-stu-id="823fb-389">Verify that the game does not require the system to be rebooted after installation.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="823fb-390">Wenn ein Microsoft-Systemupdate REDIST einen Neustart erfordert, führen Sie folgende Schritte aus: Schließen Sie die Spieleinstallation ab, deinstallieren Sie das Spiel, und installieren Sie das Spiel ein zweites Mal neu.</span><span class="sxs-lookup"><span data-stu-id="823fb-390">If a Microsoft system update REDIST requires a reboot, then do the following: Complete the game installation, uninstall the game, and reinstall the game a second time.</span></span> <span data-ttu-id="823fb-391">Der Spielinstallationsprozess sollte bei dieser zweiten Installation keinen Neustart erfordern.</span><span class="sxs-lookup"><span data-stu-id="823fb-391">The game installation process should not require a reboot on this second installation.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a><span data-ttu-id="823fb-392">3.6 Verwenden sie die Dateiversionsierung ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="823fb-392">3.6 Use File Versioning Correctly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-393">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-393">Windows 7</span></span><br/> <span data-ttu-id="823fb-394">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-394">Windows Vista</span></span><br/> <span data-ttu-id="823fb-395">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-395">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-396">Das Spielinstallationsprogramm muss ordnungsgemäß überprüfen, um sicherzustellen, dass die neuesten Dateiversionen installiert sind.</span><span class="sxs-lookup"><span data-stu-id="823fb-396">The game installation program must properly check to ensure that the latest file versions are installed.</span></span> <span data-ttu-id="823fb-397">Die Installation eines Spiels darf niemals Dateien zurückdrennen, die Sie nicht erzeugen oder die von Anwendungen freigegeben werden, die Sie nicht erstellen.</span><span class="sxs-lookup"><span data-stu-id="823fb-397">Installing a game must never regress any files that you do not produce or that are shared by applications that you do not produce.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="823fb-398">Erstellen Sie vor der Installation des Spiels eine Vorabmomentaufnahme von System32.</span><span class="sxs-lookup"><span data-stu-id="823fb-398">Prior to installing the game, create a pre-install snapshot of System32.</span></span><br/>
<ol>
<li><span data-ttu-id="823fb-399">Erstellen Sie ein Verzeichnis mit dem Namen G4Wtest.</span><span class="sxs-lookup"><span data-stu-id="823fb-399">Make a directory called G4Wtest.</span></span></li>
<li><span data-ttu-id="823fb-400">Öffnen Sie ein Befehlsfenster (Start -> Run -> cmd).</span><span class="sxs-lookup"><span data-stu-id="823fb-400">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="823fb-401">Navigieren Sie zu c:\windows\system32.</span><span class="sxs-lookup"><span data-stu-id="823fb-401">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="823fb-402">Geben Sie dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt ein.</span><span class="sxs-lookup"><span data-stu-id="823fb-402">Type dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt.</span></span></li>
</ol></li>
<li><span data-ttu-id="823fb-403">Erstellen Sie eine Momentaufnahme von System32 nach der Installation.</span><span class="sxs-lookup"><span data-stu-id="823fb-403">Create a post-install snapshot of System32.</span></span> <br/>
<ol>
<li><span data-ttu-id="823fb-404">Öffnen Sie ein Befehlsfenster (Start -> Run -> cmd).</span><span class="sxs-lookup"><span data-stu-id="823fb-404">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="823fb-405">Navigieren Sie zu c:\windows\system32.</span><span class="sxs-lookup"><span data-stu-id="823fb-405">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="823fb-406">Geben Sie dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt ein.</span><span class="sxs-lookup"><span data-stu-id="823fb-406">Type dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt.</span></span></li>
<li><span data-ttu-id="823fb-407">Stellen Sie sicher, dass das Spiel keine Dateiversionen von Dateien zurückzieht, die das Spiel nicht erzeugt hat (... der in den beiden Dokumenten aufgeführten Dateien, indem pregame.txt mit postgame.txt) verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-407">Verify that the game does not regress any file versions of files that the game did not produce (...of the files listed in the two documents by comparing pregame.txt to postgame.txt).</span></span></li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a><span data-ttu-id="823fb-408">3.7 Unterstützung von bedingten \[ Autorun-Anforderungen\]</span><span class="sxs-lookup"><span data-stu-id="823fb-408">3.7 Support Autorun \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-409">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-409">Windows 7</span></span><br/> <span data-ttu-id="823fb-410">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-410">Windows Vista</span></span><br/> <span data-ttu-id="823fb-411">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-411">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-412">Bei Spielen, die auf CD, DVD oder anderen Wechselmedien verteilt werden, die Autorun unterstützen, muss die Anwendung automatisch ausgeführt werden oder den Benutzer auffordern, das Spiel zu installieren, wenn der Datenträger zum ersten Mal eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-412">For games distributed on CD, DVD, or other removable media that support Autorun, when the disc is inserted for the first time, the application must automatically run or prompt the user to install the game.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="823fb-413">Autorun-Programme, die für die Verwendung in Windows-Versionen vor Windows Vista geschrieben wurden, sollten nicht die .NET-Runtime verwenden, da diese Technologie nicht in Windows XP oder älteren Versionen von Windows enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="823fb-413">Autorun programs that were written for use on versions of Windows prior to Windows Vista should not use the .NET runtime, because this technology is not included with Windows XP or older versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="823fb-414">Weitere Informationen finden Sie unter <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3.7, Support Autorun.</span><span class="sxs-lookup"><span data-stu-id="823fb-414">For further guidance, please refer to <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3.7, Support Autorun.</span></span> <br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="823fb-415">Fügen Sie die Spieldatenträger oder -medien ein.</span><span class="sxs-lookup"><span data-stu-id="823fb-415">Insert the game disc or media.</span></span></li>
<li><span data-ttu-id="823fb-416">Vergewissern Sie sich, dass das Dialogfeld "Installieren/Ausführen" automatisch angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-416">Verify that the install / run dialog box comes up automatically.</span></span></li>
<li><span data-ttu-id="823fb-417">Windows Vista oder Windows 7: Vergewissern Sie sich, dass das Autorun-Programm für das Spiel selbst Benutzer Jane nicht auffordert, die Rechte über Administratoranmeldeinformationen zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="823fb-417">Windows Vista or Windows 7: Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials.</span></span></li>
<li><span data-ttu-id="823fb-418">Vergewissern Sie sich, dass die ausführbare Datei Autorun keine vordefinierten REDIST-Komponenten wie .NET 3.5, C Run-Time Bibliotheken usw. benötigt.</span><span class="sxs-lookup"><span data-stu-id="823fb-418">Verify that the Autorun executable doesn't need out-of-box REDIST components, such as .NET 3.5, C Run-Time libraries, and so on.</span></span></li>
<li><span data-ttu-id="823fb-419">Stellen Sie sicher, dass das erneute Einfügen des Datenträgers auf dem Laufwerk nach der Installation nicht dazu führt, dass die Installation automatisch erneut gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-419">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a><span data-ttu-id="823fb-420">4. Zuverlässigkeit</span><span class="sxs-lookup"><span data-stu-id="823fb-420">4. Reliability</span></span>

### <a name="41-eliminate-unnecessary-reboots"></a><span data-ttu-id="823fb-421">4.1 Vermeiden unnötiger Neustarts</span><span class="sxs-lookup"><span data-stu-id="823fb-421">4.1 Eliminate Unnecessary Reboots</span></span>



| <span data-ttu-id="823fb-422">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="823fb-422">OS</span></span>                                              | <span data-ttu-id="823fb-423">Anforderung</span><span class="sxs-lookup"><span data-stu-id="823fb-423">Requirement</span></span>                                                                                                                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="823fb-424">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-424">Windows 7</span></span><br/> <span data-ttu-id="823fb-425">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-425">Windows Vista</span></span><br/> | <span data-ttu-id="823fb-426">Alle Anwendungsinstallationsprogramme müssen die Neustart-Manager-APIs nutzen, um Systemneustarts zu vermeiden (siehe [Anforderung 3.5).](#35-avoid-reboots-during-installation)</span><span class="sxs-lookup"><span data-stu-id="823fb-426">All application installers must take advantage of the Restart Manager APIs to avoid system reboots (see [requirement 3.5](#35-avoid-reboots-during-installation)).</span></span> |



 

### <a name="42-eliminate-application-verifier-failures"></a><span data-ttu-id="823fb-427">4.2 Beseitigen von Application Verifier Fehlern</span><span class="sxs-lookup"><span data-stu-id="823fb-427">4.2 Eliminate Application Verifier Failures</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-428">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-428">Windows 7</span></span><br/> <span data-ttu-id="823fb-429">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-429">Windows Vista</span></span><br/> <span data-ttu-id="823fb-430">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-430">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-431">Das Spiel darf in den folgenden Tests keine Fehler generieren, die unter Microsoft Application Verifier (AppVerifier), Version 4.0 oder höher, ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="823fb-431">The game must generate no failures running under Microsoft Application Verifier (AppVerifier), version 4.0 or later, in the following tests:</span></span> <br/>
<ul>
<li><span data-ttu-id="823fb-432">Grundlagen: Handles, Heaps, Sperren, Arbeitsspeicher, TLS</span><span class="sxs-lookup"><span data-stu-id="823fb-432">Basics: Handles, Heaps, Locks, Memory, TLS</span></span></li>
<li><span data-ttu-id="823fb-433">Sonstiges: DangerousAPIs, DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="823fb-433">Miscellaneous: DangerousAPIs, DirtyStacks</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="823fb-434">Tool verwenden: AppVerifier 4.0 (oder höher)</span><span class="sxs-lookup"><span data-stu-id="823fb-434">Use Tool: AppVerifier 4.0 (or later)</span></span><br/>
<ol>
<li><span data-ttu-id="823fb-435">Installieren Sie AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="823fb-435">Install AppVerifier.</span></span></li>
<li><span data-ttu-id="823fb-436">Starten Sie AppVerifier, und wählen Sie Datei -> Anwendung hinzufügen aus.</span><span class="sxs-lookup"><span data-stu-id="823fb-436">Launch AppVerifier and select File -> Add Application.</span></span></li>
<li><span data-ttu-id="823fb-437">Suchen Sie die ausführbare Spieldatei, wählen Sie sie aus, und klicken Sie auf die &quot; &quot; Schaltfläche Öffnen.</span><span class="sxs-lookup"><span data-stu-id="823fb-437">Locate the game executable, select it, and click the &quot;Open&quot; button.</span></span></li>
<li><span data-ttu-id="823fb-438">Wählen Sie im &quot; Abschnitt Anwendungen die ausführbare &quot; Spieldatei aus.</span><span class="sxs-lookup"><span data-stu-id="823fb-438">In the &quot;Applications&quot; section, select the game executable.</span></span></li>
<li><span data-ttu-id="823fb-439">Wählen Sie im &quot; Abschnitt Tests unter den Kategorien Grundlagen und &quot; Sonstiges die oben aufgeführten Tests aus &quot; &quot; &quot; &quot; (deaktivieren Sie ThreadPool und TimeRollOver), und stellen Sie sicher, dass nicht alle anderen Tests ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="823fb-439">In the &quot;Tests&quot; section, select the tests listed above under the categories &quot;Basics&quot; and &quot;Miscellaneous&quot; (uncheck ThreadPool and TimeRollOver), and ensure all other tests are not selected.</span></span></li>
<li><span data-ttu-id="823fb-440">Starten Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="823fb-440">Launch the game.</span></span></li>
<li><span data-ttu-id="823fb-441">Vergewissern Sie sich, dass das Spiel keine Fehler generiert, wenn es unter Application Verifier ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-441">Verify that the game does not generate failures when run under Application Verifier.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="823fb-442">Einige Tests erfordern, dass ein Debugger vollständig ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-442">Some tests require a debugger to be fully run.</span></span> <span data-ttu-id="823fb-443">Dies kann eine ungeschützte Releaseversion der ausführbaren Spieldatei erfordern, da die Antispickzettel-/Anti-Anti- antivirus-Technologie AppVerifer beeinträchtigen kann.</span><span class="sxs-lookup"><span data-stu-id="823fb-443">This may require an unprotected release version of the game executable, since anti-cheat/anti-piracy technology may interfere with AppVerifer.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a><span data-ttu-id="823fb-444">4.3 Unterstützung Windows-Fehlerberichterstattung</span><span class="sxs-lookup"><span data-stu-id="823fb-444">4.3 Support Windows Error Reporting</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="823fb-445">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-445">Windows 7</span></span><br/> <span data-ttu-id="823fb-446">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-446">Windows Vista</span></span><br/> <span data-ttu-id="823fb-447">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-447">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-448">Spiele dürfen nur Ausnahmen behandeln, die bekannt und erwartet sind, und Windows-Fehlerberichterstattung dürfen nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-448">Games must handle only exceptions that are known and expected, and Windows Error Reporting must not be disabled.</span></span> <span data-ttu-id="823fb-449">Wenn ein Fehler (z. B. eine Zugriffsverletzung) in ein Spiel eingefügt wird, muss es Windows-Fehlerberichterstattung ermöglichen, den Absturz zu melden.</span><span class="sxs-lookup"><span data-stu-id="823fb-449">If a fault (such as an Access Violation) is injected into a game, it must allow Windows Error Reporting to report the crash.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="823fb-450">Verwenden des Tools: Thread Auserzählen</span><span class="sxs-lookup"><span data-stu-id="823fb-450">Use Tool: Thread Hijacker</span></span> <br/>
<ul>
<li><span data-ttu-id="823fb-451">Wenn die Anwendung beim Testen abstürzt, überprüfen Sie, ob das Spiel Windows-Fehlerberichterstattung ordnungsgemäß anzeigt und Absturzdaten sammelt.</span><span class="sxs-lookup"><span data-stu-id="823fb-451">If the application crashes while testing, verify that the game displays Windows Error Reporting properly and collects crash data.</span></span></li>
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
<td><span data-ttu-id="823fb-452">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-452">Windows 7</span></span><br/> <span data-ttu-id="823fb-453">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-453">Windows Vista</span></span><br/> <span data-ttu-id="823fb-454">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-454">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-455">Alle ausführbaren Dateien (z. B. .exe- oder .dll dateien) müssen einen genauen Produktnamen, Einen Firmennamen und eine Dateiversion enthalten.</span><span class="sxs-lookup"><span data-stu-id="823fb-455">All executable files (for example, .exe or .dll files) must contain an accurate Product Name, Company Name, and File Version.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="823fb-456"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Manueller Test:</dt> </span><span class="sxs-lookup"><span data-stu-id="823fb-456"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Manual test:</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="823fb-457">Klicken Sie mit der rechten Maustaste auf die ausführbaren Dateien des Spiels sowohl auf dem Installationsmedium als auch auf den auf der Computerfestplatte installierten Dateien.</span><span class="sxs-lookup"><span data-stu-id="823fb-457">Right-click the game's executable file(s) on both the installation media and those installed to the computer hard drive.</span></span></li>
<li><span data-ttu-id="823fb-458">Wählen Sie „Eigenschaften“.</span><span class="sxs-lookup"><span data-stu-id="823fb-458">Select Properties.</span></span></li>
<li><span data-ttu-id="823fb-459">Windows XP: Klicken Sie auf die Registerkarte <strong>Version.</strong> Stellen Sie sicher, dass die Felder Produktname, Unternehmensname und Dateiversion ordnungsgemäß ausgefüllt sind.</span><span class="sxs-lookup"><span data-stu-id="823fb-459">Windows XP: Click the <strong>Version</strong> tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span></li>
<li><span data-ttu-id="823fb-460">Windows Vista oder Windows 7: Klicken Sie auf die Registerkarte <strong>Details.</strong> Vergewissern Sie sich, dass die Felder Produktname und Dateiversion ordnungsgemäß ausgefüllt sind.</span><span class="sxs-lookup"><span data-stu-id="823fb-460">Windows Vista or Windows 7: Click the <strong>Details</strong> tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="823fb-461">Der Unternehmensname ist auf der Eigenschaftenseite von Windows Vista oder Windows 7 nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="823fb-461">Company Name is not visible in the Windows Vista or Windows 7 properties page.</span></span></li>
</ol>
</dd> <span data-ttu-id="823fb-462"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Automatisierter Test:</dt> </span><span class="sxs-lookup"><span data-stu-id="823fb-462"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Automated test:</dt> </span></span><dd>
<ul>
<li><span data-ttu-id="823fb-463">Verwenden sie das Microsoft Games for Windows Test Tool. siehe <a href="#64-microsoft-games-for-windows-test-tool">Abschnitt 6.4.</a></span><span class="sxs-lookup"><span data-stu-id="823fb-463">Use the Microsoft Games for Windows Test Tool; see <a href="#64-microsoft-games-for-windows-test-tool">section 6.4</a>.</span></span></li>
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
<td><span data-ttu-id="823fb-464">Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-464">Windows 7</span></span><br/> <span data-ttu-id="823fb-465">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823fb-465">Windows Vista</span></span><br/> <span data-ttu-id="823fb-466">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-466">Windows XP</span></span><br/></td>
<td><span data-ttu-id="823fb-467">Das normale Beenden des Spiels darf nicht zu einem unbekannten Ausnahmefehler führen.</span><span class="sxs-lookup"><span data-stu-id="823fb-467">Normal exit of the game must not result in an unknown exception fault.</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="823fb-468">Überprüfen Sie nach dem Spielen für eine normale Spielsitzung, ob das Spiel beim Beenden keine Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="823fb-468">After playing the game for a normal gaming session, verify that the game does not generate errors on exit.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a><span data-ttu-id="823fb-469">5. Beispieltestskript</span><span class="sxs-lookup"><span data-stu-id="823fb-469">5. Sample Test Script</span></span>

<span data-ttu-id="823fb-470">Dies ist ein Beispiel für einen typischen Testdurchlauf, der die oben genannten Testanforderungen als Leitfaden verwendet.</span><span class="sxs-lookup"><span data-stu-id="823fb-470">This is an example of a typical test pass using the preceding test requirements as a guide.</span></span>

### <a name="51-tools"></a><span data-ttu-id="823fb-471">5.1 Tools</span><span class="sxs-lookup"><span data-stu-id="823fb-471">5.1 Tools</span></span>

-   <span data-ttu-id="823fb-472">32-Bit-Edition von Windows Vista SP1 und/oder Windows 7 auf einer AMD-CPU</span><span class="sxs-lookup"><span data-stu-id="823fb-472">32-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="823fb-473">32-Bit-Edition von Windows Vista SP1 und/oder Windows 7 auf einer Intel-CPU</span><span class="sxs-lookup"><span data-stu-id="823fb-473">32-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="823fb-474">64-Bit-Edition von Windows Vista SP1 und/oder Windows 7 auf einer AMD-CPU</span><span class="sxs-lookup"><span data-stu-id="823fb-474">64-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="823fb-475">64-Bit-Edition von Windows Vista SP1 und/oder Windows 7 auf einer Intel-CPU</span><span class="sxs-lookup"><span data-stu-id="823fb-475">64-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="823fb-476">32-Bit-Edition Windows XP SP2 auf einer AMD-CPU</span><span class="sxs-lookup"><span data-stu-id="823fb-476">32-bit edition Windows XP SP2 on an AMD CPU</span></span>
-   <span data-ttu-id="823fb-477">32-Bit-Edition Windows XP SP2 auf einer Intel-CPU</span><span class="sxs-lookup"><span data-stu-id="823fb-477">32-bit edition Windows XP SP2 on an Intel CPU</span></span>
-   <span data-ttu-id="823fb-478">Breitbildschirmmonitor, der 1680 1050 unterstützt</span><span class="sxs-lookup"><span data-stu-id="823fb-478">Wide Screen Monitor that supports 1680 1050</span></span>
-   <span data-ttu-id="823fb-479">Xbox 360 Controller für Windows</span><span class="sxs-lookup"><span data-stu-id="823fb-479">Xbox 360 Controller for Windows</span></span>

### <a name="52-pre-install"></a><span data-ttu-id="823fb-480">5.2 Vorinstallation</span><span class="sxs-lookup"><span data-stu-id="823fb-480">5.2 Pre-Install</span></span>

1.  <span data-ttu-id="823fb-481">Windows Vista und Windows 7: Erstellen von zwei Standardbenutzern: Jane und Toby</span><span class="sxs-lookup"><span data-stu-id="823fb-481">Windows Vista and Windows 7: Create two Standard Users: Jane and Toby</span></span>
2.  <span data-ttu-id="823fb-482">Windows Vista und Windows 7: Sicherstellen, dass die Benutzerkontensteuerung aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="823fb-482">Windows Vista and Windows 7: Ensure User Account Control is enabled</span></span>
3.  <span data-ttu-id="823fb-483">Erstellen einer Vorinstallationsmomentaufnahme von System32</span><span class="sxs-lookup"><span data-stu-id="823fb-483">Create a pre-install snapshot of System32</span></span>

    1.  <span data-ttu-id="823fb-484">Erstellen eines Verzeichnisses mit dem Namen G4Wtest</span><span class="sxs-lookup"><span data-stu-id="823fb-484">Make a directory called G4Wtest</span></span>
    2.  <span data-ttu-id="823fb-485">Aufrufen eines Befehlsfensters (Start -> Run -> cmd)</span><span class="sxs-lookup"><span data-stu-id="823fb-485">Bring up a command Window (Start -> Run -> cmd)</span></span>
    3.  <span data-ttu-id="823fb-486">Navigieren Sie zu c: \\ windows \\ system32.</span><span class="sxs-lookup"><span data-stu-id="823fb-486">Navigate to c:\\windows\\system32</span></span>
    4.  <span data-ttu-id="823fb-487">Geben Sie dir /o:-g /o:-d >> c: \\ G4Wtest \\pregame.txt</span><span class="sxs-lookup"><span data-stu-id="823fb-487">Type dir /o:-g /o:-d >> c:\\G4Wtest\\pregame.txt</span></span>

4.  <span data-ttu-id="823fb-488">Windows Vista und Windows 7: Auf 150 % DPI \[ 1.8 festgelegt\]</span><span class="sxs-lookup"><span data-stu-id="823fb-488">Windows Vista and Windows 7: Set to 150% DPI \[1.8\]</span></span>
5.  <span data-ttu-id="823fb-489">Fahren Sie mit [der Installation](#3-installation) fort.</span><span class="sxs-lookup"><span data-stu-id="823fb-489">Proceed to [Install](#3-installation)</span></span>

### <a name="53-install"></a><span data-ttu-id="823fb-490">5.3 Installieren</span><span class="sxs-lookup"><span data-stu-id="823fb-490">5.3 Install</span></span>

1.  <span data-ttu-id="823fb-491">Melden Sie sich als Benutzerin Jane an.</span><span class="sxs-lookup"><span data-stu-id="823fb-491">Log on as User Jane</span></span>
2.  <span data-ttu-id="823fb-492">Fügen Sie die Spieldatenträger in das CD/DVD-Laufwerk ein, und vergewissern Sie sich, dass das Dialogfeld "Installieren/Ausführen" automatisch \[ 3.7 angezeigt wird.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-492">Insert the game disc into the CD/DVD drive, verify that the install / run dialog box comes up automatically \[3.7\]</span></span>
3.  <span data-ttu-id="823fb-493">Vergewissern Sie sich, dass der Spielinstallationsvorgang Benutzer Jane auffordert, die Administratoranmeldeinformationen \[ 3.2 zu erhöhen.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-493">Verify that the game installation process prompts User Jane to elevate Administrator Credentials \[3.2\]</span></span>
4.  <span data-ttu-id="823fb-494">Vergewissern Sie sich, dass das Autorun-Programm für das Spiel selbst Benutzer Jane nicht dazu auffordert, die Rechte über Administratoranmeldeinformationen \[ 3.7 zu erhöhen.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-494">Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials \[3.7\]</span></span>
5.  <span data-ttu-id="823fb-495">Vergewissern Sie sich, dass im Spiel nicht mehr als ein End-User Lizenzvertrag (EULA) \[ 3.1 angezeigt wird.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-495">Verify that the game does not display more than one End-User License Agreement (EULA) \[3.1\]</span></span>
6.  <span data-ttu-id="823fb-496">Vergewissern Sie sich, dass das Spiel die Installationsoptionen Standard/Einfach und Benutzerdefiniert/Erweitert \[ 3.1 anzeigt.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-496">Verify that the game displays Default/Easy and Custom/Advanced installation options \[3.1\]</span></span>
7.  <span data-ttu-id="823fb-497">Stellen Sie sicher, dass die Option Standardinstallation/Einfache Installation alle Benutzereingabeauswahlen für den Installationsvorgang umgeht (Auswahl des Installationsordners, Komponentenauswahl usw.). \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="823fb-497">Verify that the Default/Easy installation option bypasses all user input selections for the install process (selection of installation folder, components selection, and so on.) \[3.1\]</span></span>
8.  <span data-ttu-id="823fb-498">Vergewissern Sie sich, dass der Spielinstallationsvorgang nicht zur Einrichtung von Betriebssystemkomponenten auffordert (DirectX-Setup, C Run-Time Bibliotheken usw.). \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="823fb-498">Verify that the game installation process does not prompt for OS component setup (DirectX setup, C Run-Time libraries, and so on.) \[3.1\]</span></span>
9.  <span data-ttu-id="823fb-499">Vergewissern Sie sich, dass der Spielinstallationsvorgang nicht zur Eingabe der Firewallinteraktion \[ 3.1 auffordert.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-499">Verify that the game installation process does not prompt for firewall interaction \[3.1\]</span></span>
10. <span data-ttu-id="823fb-500">Vergewissern Sie sich, dass bei der Spieleinstallation kein Fehler in Bezug auf Betriebssystemversion \[ 2.5 \] \[ 4.2 auftritt.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-500">Verify that the game installation process does not encounter an error regarding OS Version \[2.5\] \[4.2\]</span></span>
11. <span data-ttu-id="823fb-501">Vergewissern Sie sich, dass bei der Spieleinstallation keine Dialogfelder für nicht signierte Treiber \[ 2.4 angezeigt werden.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-501">Verify that the game installation process does not display unsigned driver dialog(s) \[2.4\]</span></span>
12. <span data-ttu-id="823fb-502">Vergewissern Sie sich, dass während des Installationsvorgangs 3.4 keine WRP-Dialoge (Windows-Ressourcenschutz) angezeigt werden. \[\]</span><span class="sxs-lookup"><span data-stu-id="823fb-502">Verify that no Windows Resource Protection (WRP) dialogs appear during the install process \[3.4\]</span></span>
13. <span data-ttu-id="823fb-503">Vergewissern Sie sich, dass das erneute Einfügen des Datenträgers auf dem Laufwerk nach der Installation nicht dazu führt, dass die Installation automatisch erneut gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-503">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again</span></span>
14. <span data-ttu-id="823fb-504">Vergewissern Sie sich, dass das System nach Installation von 3.5 nicht neu gestartet werden muss. \[\]</span><span class="sxs-lookup"><span data-stu-id="823fb-504">Verify that the game does not require the system to be rebooted after installation \[3.5\]</span></span>
15. <span data-ttu-id="823fb-505">Vergewissern Sie sich, dass Sie das Spiel als Benutzerin Jane \[ 3.2 installieren können.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-505">Verify that you can install the game as User Jane \[3.2\]</span></span>
16. <span data-ttu-id="823fb-506">Stellen Sie sicher, dass das Spiel automatisch ausgeführt wird oder dass am Ende des Installationsvorgangs 3.1 ein Startmenü vorhanden ist. \[\]</span><span class="sxs-lookup"><span data-stu-id="823fb-506">Verify that the game automatically runs or that a launcher menu is present at the end of the installation process \[3.1\]</span></span>
17. <span data-ttu-id="823fb-507">Wenn das Spiel nach der Installation automatisch ausgeführt wird, fahren Sie mit [Runtime](#55-runtime)</span><span class="sxs-lookup"><span data-stu-id="823fb-507">If the game does auto-run after installation, skip to [Runtime](#55-runtime)</span></span>
18. <span data-ttu-id="823fb-508">Wenn das Spiel ein Startmenü verlassen hat oder nicht deinstalliert werden konnte, finden Sie weitere Informationen im Abschnitt [Nach der Installation.](#54-post-install)</span><span class="sxs-lookup"><span data-stu-id="823fb-508">If the game left a launch menu up, or failed to uninstall see section [Post-Install](#54-post-install)</span></span>

### <a name="54-post-install"></a><span data-ttu-id="823fb-509">5.4 Nach der Installation</span><span class="sxs-lookup"><span data-stu-id="823fb-509">5.4 Post-Install</span></span>

1.  <span data-ttu-id="823fb-510">Vergewissern Sie sich, dass das Spiel keine Startverknüpfungen auf benutzerdesktop \[ 1.1 eingibt.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-510">Verify that the game does not place launch shortcuts on user desktop \[1.1\]</span></span>
2.  <span data-ttu-id="823fb-511">Vergewissern Sie sich, dass das Spiel keine Startverknüpfungen im Startmenü \[ 1.1 einsortiert.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-511">Verify that the game does not place launch shortcuts in the Start Menu \[1.1\]</span></span>
3.  <span data-ttu-id="823fb-512">Überprüfen Sie, ob das Spielsymbol in Windows Games Explorer \[ 1.1 angezeigt wird.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-512">Verify that the game icon displays in Windows Games Explorer \[1.1\]</span></span>
4.  <span data-ttu-id="823fb-513">Überprüfen Sie, ob die Metadaten (Herausgeber, Entwickler, Genre, Veröffentlichungsdatum, Version) unten angezeigt werden und richtig \[ 1.1 sind.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-513">Verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct \[1.1\]</span></span>
5.  <span data-ttu-id="823fb-514">Überprüfen Sie, ob das Spielsymbol WeI-Informationen (Windows Experience Index) in Windows Games Explorer \[ 1.1 anzeigt.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-514">Verify that the game icon displays Windows Experience Index (WEI) information in Windows Games Explorer \[1.1\]</span></span>
6.  <span data-ttu-id="823fb-515">Überprüfen, ob Gamelinks für Metadaten in Windows Games Explorer \[ 1.1 ordnungsgemäß funktionieren\]</span><span class="sxs-lookup"><span data-stu-id="823fb-515">Verify that game hyperlinks for metadata work correctly in Windows Games Explorer \[1.1\]</span></span>
7.  <span data-ttu-id="823fb-516">Überprüfen Sie, ob das Spiel in Windows Games Explorer 1.1 eine genaue Bewertung der Jugendschutzsteuerung anzeigt. \[\]</span><span class="sxs-lookup"><span data-stu-id="823fb-516">Verify that the game displays accurate parental control rating in Windows Games Explorer \[1.1\]</span></span>
8.  <span data-ttu-id="823fb-517">Erstellen einer Momentaufnahme von System32 nach der Installation</span><span class="sxs-lookup"><span data-stu-id="823fb-517">Create a post-install snapshot of System32</span></span>

    1.  <span data-ttu-id="823fb-518">Aufrufen eines Befehlsfensters (Start -> Run -> cmd)</span><span class="sxs-lookup"><span data-stu-id="823fb-518">Bring up a command Window (Start -> Run -> cmd)</span></span>
    2.  <span data-ttu-id="823fb-519">Navigieren Sie zu c: \\ windows \\ system32.</span><span class="sxs-lookup"><span data-stu-id="823fb-519">Navigate to c:\\windows\\system32</span></span>
    3.  <span data-ttu-id="823fb-520">Geben Sie dir /o:-g /o:-d >> c: \\ G4Wtest \\postgame.txt</span><span class="sxs-lookup"><span data-stu-id="823fb-520">Type dir /o:-g /o:-d >> c:\\G4Wtest\\postgame.txt</span></span>
    4.  <span data-ttu-id="823fb-521">Stellen Sie sicher, dass das Spiel keine Dateiversionen der in den beiden Dokumenten aufgeführten Dateien zurückzieht, indem Sie pregame.txt mit postgame.txt \[ 3.6 vergleichen.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-521">Verify that the game does not regress any file versions of files listed in the two documents by comparing pregame.txt to postgame.txt \[3.6\]</span></span>

9.  <span data-ttu-id="823fb-522">Fahren Sie mit [runtime fort.](#55-runtime)</span><span class="sxs-lookup"><span data-stu-id="823fb-522">Proceed to [Runtime](#55-runtime)</span></span>

### <a name="55-runtime"></a><span data-ttu-id="823fb-523">5.5 Runtime</span><span class="sxs-lookup"><span data-stu-id="823fb-523">5.5 Runtime</span></span>

1.  <span data-ttu-id="823fb-524">RUNTIME 1: Wenn das Startmenü vorhanden ist, starten Sie das Spiel von dort aus.</span><span class="sxs-lookup"><span data-stu-id="823fb-524">RUNTIME 1: If the launch menu is present, launch the game from there.</span></span> <span data-ttu-id="823fb-525">Wenn das Spiel nach der Installation automatisch ausgeführt oder nach der Installation über das Menü des Spielstarts gestartet wurde, führen Sie Folgendes aus: Falls nicht, fahren Sie mit RUNTIME 2:</span><span class="sxs-lookup"><span data-stu-id="823fb-525">If the game auto-ran or was launched from the game launcher menu after install, perform the following; if not, skip to RUNTIME 2:</span></span>

    1.  <span data-ttu-id="823fb-526">Erstellen eines Profils (wenn das Spiel dies zulässt)</span><span class="sxs-lookup"><span data-stu-id="823fb-526">Create a profile (if the game allows)</span></span>
    2.  <span data-ttu-id="823fb-527">Starten eines neuen Spiels</span><span class="sxs-lookup"><span data-stu-id="823fb-527">Start a new game</span></span>
    3.  <span data-ttu-id="823fb-528">Speichern des Spiels</span><span class="sxs-lookup"><span data-stu-id="823fb-528">Save the game</span></span>
    4.  <span data-ttu-id="823fb-529">Beenden des Spiels</span><span class="sxs-lookup"><span data-stu-id="823fb-529">Exit the game</span></span>
    5.  <span data-ttu-id="823fb-530">Starten des Spiels im Spiele-Explorer</span><span class="sxs-lookup"><span data-stu-id="823fb-530">Launch the game from Games Explorer</span></span>
    6.  <span data-ttu-id="823fb-531">Überprüfen Sie, ob das Spiel über das Symbol "Spiele-Explorer \[ 1.2" gestartet wird.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-531">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    7.  <span data-ttu-id="823fb-532">Vergewissern Sie sich, dass das Spiel beim Start 1.2 nicht zur Eingabe von Administratoranmeldeinformationen auffordert. \[\]</span><span class="sxs-lookup"><span data-stu-id="823fb-532">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    8.  <span data-ttu-id="823fb-533">Vergewissern Sie sich, dass auf Benutzerprofile und Spiele speichern über das Benutzer-Jane-Konto 3.2 zugegriffen werden kann. \[\]</span><span class="sxs-lookup"><span data-stu-id="823fb-533">Verify that User Profiles and Save Games can be accessed by User Jane account \[3.2\]</span></span>
    9.  <span data-ttu-id="823fb-534">Fahren Sie mit RUNTIME 3 fort.</span><span class="sxs-lookup"><span data-stu-id="823fb-534">Proceed to RUNTIME 3</span></span>

2.  <span data-ttu-id="823fb-535">RUNTIME 2: Wenn das Spiel nicht automatisch ausgeführt wurde oder einen Start über das Startmenü des Spiels anzeigte, ist dies ein Fehler von \[ 3.1. Die \] Tests können jedoch normal fortgesetzt werden:</span><span class="sxs-lookup"><span data-stu-id="823fb-535">RUNTIME 2: If the game did not auto-run or display a launch from the game launcher menu, this is a failure of \[3.1\]; however, testing can continue normally:</span></span>

    1.  <span data-ttu-id="823fb-536">Starten des Spiels im Spiele-Explorer</span><span class="sxs-lookup"><span data-stu-id="823fb-536">Launch the game from Games Explorer</span></span>
    2.  <span data-ttu-id="823fb-537">Überprüfen Sie, ob das Spiel über das Symbol "Spiele-Explorer \[ 1.2" gestartet wird.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-537">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    3.  <span data-ttu-id="823fb-538">Vergewissern Sie sich, dass das Spiel beim Start 1.2 nicht zur Eingabe von Administratoranmeldeinformationen auffordert. \[\]</span><span class="sxs-lookup"><span data-stu-id="823fb-538">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    4.  <span data-ttu-id="823fb-539">Fahren Sie mit RUNTIME 3 fort.</span><span class="sxs-lookup"><span data-stu-id="823fb-539">Proceed to RUNTIME 3</span></span>

3.  <span data-ttu-id="823fb-540">RUNTIME 3: Wenn das Spiel ein Spielpad unterstützt, überprüfen Sie, ob das Spiel Xbox 360 Controller für Windows als Eingabegerät \[ erkennt 1.4\]</span><span class="sxs-lookup"><span data-stu-id="823fb-540">RUNTIME 3: If the game supports a game pad, verify that the game recognizes Xbox 360 Controller for Windows as an input device \[1.4\]</span></span>

    1.  <span data-ttu-id="823fb-541">Aktivieren Sie bei Bedarf den Controller über das Menü "Optionen".</span><span class="sxs-lookup"><span data-stu-id="823fb-541">If needed, enable the controller via the options menu</span></span>
    2.  <span data-ttu-id="823fb-542">Überprüfen Sie, ob das Spiel auf die Controllerschaltflächen und Trigger verweist, indem Sie Xbox 360 Namen verwenden.</span><span class="sxs-lookup"><span data-stu-id="823fb-542">Verify that the game refers to the controller buttons and triggers using Xbox 360 names</span></span>
    3.  <span data-ttu-id="823fb-543">Überprüfen Sie, ob spiel- und menüsystem mit dem Xbox 360 Controller für Windows steuerbar sind.</span><span class="sxs-lookup"><span data-stu-id="823fb-543">Verify that the game and menu system are controllable with the Xbox 360 Controller for Windows</span></span>
    4.  <span data-ttu-id="823fb-544">Überprüfen Sie, ob sich der Xbox 360 Controller für Windows gemäß den akzeptierten Standards verhält.</span><span class="sxs-lookup"><span data-stu-id="823fb-544">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards</span></span>

4.  <span data-ttu-id="823fb-545">Legen Sie das Video auf \[ 1.5 \] fest:</span><span class="sxs-lookup"><span data-stu-id="823fb-545">Set the video to \[1.5\]:</span></span>

    1.  <span data-ttu-id="823fb-546">Überprüfen Sie, ob das Spiel mit einer Seitenverhältnisauflösung von 4:3 (800 600 oder 1024 768) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-546">Verify that the game runs at a 4:3 Aspect Ratio resolution (800 600 or 1024 768)</span></span>
    2.  <span data-ttu-id="823fb-547">Überprüfen Sie, ob das Spiel mit einer Seitenverhältnisauflösung von 16:9 (1280 720) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-547">Verify that the game runs at a 16:9 Aspect Ratio resolution (1280 720)</span></span>
    3.  <span data-ttu-id="823fb-548">Überprüfen Sie, ob das Spiel mit einer Seitenverhältnisauflösung von 16:10 (1680 1050, 800 480 oder 1152 720) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-548">Verify that the game runs at a 16:10 Aspect Ratio resolution (1680 1050, 800 480, or 1152 720)</span></span>
    4.  <span data-ttu-id="823fb-549">Vergewissern Sie sich, dass das Spiel den Benutzer auffordert, wenn eine Änderung an der Auflösung vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-549">Verify that the game prompts the user when a change is made to the resolution</span></span>
    5.  <span data-ttu-id="823fb-550">Stellen Sie sicher, dass die Anzeige auf die vorherige Einstellung zurückgesetzt wird, wenn Sie nicht innerhalb von 15 Sekunden akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="823fb-550">Verify that the display reverts to the previous setting if you do not accept within 15 seconds</span></span>
    6.  <span data-ttu-id="823fb-551">Stellen Sie sicher, dass das Spiel das Bild nicht gestreckt und wiederum einen breiteren Ansichtsbereich darstellt.</span><span class="sxs-lookup"><span data-stu-id="823fb-551">Verify that the game does not stretch the picture and in turn presents a wider area of view</span></span>
    7.  <span data-ttu-id="823fb-552">Vergewissern Sie sich, dass das Spiel links und rechts vom Spielbereich keine schwarzen Balken hinzufüge.</span><span class="sxs-lookup"><span data-stu-id="823fb-552">Verify that the game does not add black bars to the left and right of the game play area</span></span>

5.  <span data-ttu-id="823fb-553">Falls in den Videoeinstellungen verfügbar, überprüfen Sie, ob die Spielrenderoptionen standardmäßig Direct3D \[ 1.7 \] verwenden. Fahren Sie andernfalls mit [automatisierten Tests](#58-automated-tests) fort.</span><span class="sxs-lookup"><span data-stu-id="823fb-553">If available in the video settings, verify that the game render options default to Direct3D \[1.7\]; otherwise, proceed to [Automated Tests](#58-automated-tests)</span></span>
6.  <span data-ttu-id="823fb-554">Wenn Sie dazu aufgefordert werden oder die Option verfügbar ist, erstellen Sie ein Benutzerprofil.</span><span class="sxs-lookup"><span data-stu-id="823fb-554">If prompted or if the option is available, create a user profile.</span></span> <span data-ttu-id="823fb-555">Vergewissern Sie sich, dass beim Spiel keine Fehler auftreten, wenn lange Dateinamen \[ 2.7 verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-555">Verify that the game does not encounter errors when using long file names \[2.7\]</span></span>
7.  <span data-ttu-id="823fb-556">Starten Sie ein neues Spiel, erstellen Sie ein Spiel, und überprüfen Sie, ob beim Behandeln von nicht unterstützten Dateisystemzeichen 2.7 keine Fehler auftreten. \[\]</span><span class="sxs-lookup"><span data-stu-id="823fb-556">Start a new game, create a game save, and verify that the game does not encounter errors when handling unsupported file system characters \[2.7\]</span></span>
8.  <span data-ttu-id="823fb-557">Vergewissern Sie sich, dass das Spiel ordnungsgemäß ALT+TABs für Windows Desktop \[ 2.6 verwendet.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-557">Verify that the game properly ALT+TABs to the Windows desktop \[2.6\]</span></span>

    1.  <span data-ttu-id="823fb-558">Wechseln Sie die Benutzer mit dem ausgeführten Spiel, indem Sie auf Start -> Switch User (Benutzer wechseln) klicken.</span><span class="sxs-lookup"><span data-stu-id="823fb-558">Switch users with the game running by clicking Start -> Switch User</span></span>
    2.  <span data-ttu-id="823fb-559">Anmelden als Toby</span><span class="sxs-lookup"><span data-stu-id="823fb-559">Log on as Toby</span></span>
    3.  <span data-ttu-id="823fb-560">Vergewissern Sie sich, dass das Spiel als User Toby gestartet wird, während es weiterhin als Benutzerin Jane \[ 2.6 ausgeführt wird.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-560">Verify that the game launches as User Toby while still running as User Jane \[2.6\]</span></span>
    4.  <span data-ttu-id="823fb-561">Vergewissern Sie sich, dass beim Benutzerwechselprozess 2.6 keine Fehler für "User Toby" oder "User Jane" \[ auftreten.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-561">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process \[2.6\]</span></span>
    5.  <span data-ttu-id="823fb-562">Vergewissern Sie sich, dass Sie keine Audiodaten aus der ursprünglichen Spielsitzung \[ 2.6 hören können.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-562">Verify that you cannot hear audio from the original game session \[2.6\]</span></span>
    6.  <span data-ttu-id="823fb-563">Beenden des Spiels</span><span class="sxs-lookup"><span data-stu-id="823fb-563">Exit the game</span></span>
    7.  <span data-ttu-id="823fb-564">Abmelden von Toby</span><span class="sxs-lookup"><span data-stu-id="823fb-564">Log off Toby</span></span>
    8.  <span data-ttu-id="823fb-565">Wechseln Sie zurück zum ursprünglichen Benutzer, auf dem das Spiel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-565">Switch back to the original user where the game is running</span></span>
    9.  <span data-ttu-id="823fb-566">ALT+TAB zurück ins Spiel</span><span class="sxs-lookup"><span data-stu-id="823fb-566">ALT+TAB back into the game</span></span>

9.  <span data-ttu-id="823fb-567">Beenden des Spiels</span><span class="sxs-lookup"><span data-stu-id="823fb-567">Exit the game</span></span>
10. <span data-ttu-id="823fb-568">Fahren Sie mit [Post-Runtime](#56-post-runtime) fort.</span><span class="sxs-lookup"><span data-stu-id="823fb-568">Proceed to [Post-Runtime](#56-post-runtime)</span></span>

### <a name="56-post-runtime"></a><span data-ttu-id="823fb-569">5.6 Nach der Laufzeit</span><span class="sxs-lookup"><span data-stu-id="823fb-569">5.6 Post-Runtime</span></span>

1.  <span data-ttu-id="823fb-570">Vergewissern Sie sich, dass das Spiel keine Fehler beim Beenden \[ von 4.3 generiert.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-570">Verify that the game does not generate errors on exit \[4.3\]</span></span>
2.  <span data-ttu-id="823fb-571">Überprüfen Sie, ob das Spiel in Program Files \[ 3.3 installiert ist.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-571">Verify that the game installed to Program Files \[3.3\]</span></span>
3.  <span data-ttu-id="823fb-572">Fahren Sie mit [Jugendschutz fort.](/windows)</span><span class="sxs-lookup"><span data-stu-id="823fb-572">Proceed to [Parental Controls](/windows)</span></span>

### <a name="57-parental-controls"></a><span data-ttu-id="823fb-573">5.7 Jugendschutz</span><span class="sxs-lookup"><span data-stu-id="823fb-573">5.7 Parental Controls</span></span>

1.  <span data-ttu-id="823fb-574">Öffnen der Jugendschutzfunktionen in Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="823fb-574">Open Parental Controls in Control Panel</span></span>
2.  <span data-ttu-id="823fb-575">Vergewissern Sie sich, dass das Spiel unter dem Spieltitel in Der Jugendschutz Systemsteuerung 1.2 eine genaue Bewertung der Jugendschutzprüfung anzeigt. \[\]</span><span class="sxs-lookup"><span data-stu-id="823fb-575">Verify that the game displays accurate Parental Control Rating below the game title in Parental Controls Control Panel \[1.2\]</span></span>
3.  <span data-ttu-id="823fb-576">Die folgenden Tests finden Sie unter Testfall \[ 1.2: \]</span><span class="sxs-lookup"><span data-stu-id="823fb-576">See Test Case \[1.2\] for the following tests:</span></span>

    1.  <span data-ttu-id="823fb-577">Nachdem Sie Die Jugendschutz auf "Ein" festgelegt haben, überprüfen Sie, ob das Spiel mit diesen Einstellungen als Benutzerin Jane \[ 1.2 ausgeführt wird.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-577">After setting Parental Controls to "On", verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    2.  <span data-ttu-id="823fb-578">Melden Sie sich ab, und melden Sie sich als Toby an.</span><span class="sxs-lookup"><span data-stu-id="823fb-578">Log off and log on as Toby</span></span>
    3.  <span data-ttu-id="823fb-579">Überprüfen Sie, ob das Spiel mit diesen Einstellungen als User Toby \[ 1.2 ausgeführt wird.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-579">Verify that the game runs with these settings as User Toby \[1.2\]</span></span>
    4.  <span data-ttu-id="823fb-580">Melden Sie sich ab, und melden Sie sich als Jane an.</span><span class="sxs-lookup"><span data-stu-id="823fb-580">Log off and log on as Jane</span></span>
    5.  <span data-ttu-id="823fb-581">Blockieren Sie im Abschnitt Jugendschutz, dass Benutzer Toby keine Spiele mehr oder höher als das soeben installierte Spiel mit einer ESRB-Ebene sehen kann.</span><span class="sxs-lookup"><span data-stu-id="823fb-581">In the Parental Control section, block User Toby from seeing games one ESRB level up and higher from the game that you just installed</span></span>

        <span data-ttu-id="823fb-582">Beispiel: Wenn das Spiel mit E bewertet wird, legen Sie es so fest, dass Toby nur Spiele mit der Bewertung "C" spielen kann.</span><span class="sxs-lookup"><span data-stu-id="823fb-582">Example: If the game is rated E, set it so Toby can only play games that are rated C</span></span>

    6.  <span data-ttu-id="823fb-583">Vergewissern Sie sich, dass das Spiel mit diesen Einstellungen als Benutzerin Jane \[ 1.2 ausgeführt wird.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-583">Verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    7.  <span data-ttu-id="823fb-584">Melden Sie sich ab, und melden Sie sich als Benutzer toby an.</span><span class="sxs-lookup"><span data-stu-id="823fb-584">Log off and log on as user Toby</span></span>
    8.  <span data-ttu-id="823fb-585">Vergewissern Sie sich, dass das Spiel nicht auf User Toby gestartet wird, wenn ESRB von Benutzerin Jane \[ 1.2 blockiert wird.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-585">Verify that the game does not launch on User Toby when ESRB is blocked by User Jane \[1.2\]</span></span>
    9.  <span data-ttu-id="823fb-586">Melden Sie sich als Benutzer Toby an, und melden Sie sich wieder als Benutzerin Jane an.</span><span class="sxs-lookup"><span data-stu-id="823fb-586">Log off as user Toby and back on as user Jane</span></span>
    10. <span data-ttu-id="823fb-587">Wenn sie zuvor geändert wurden, stellen Sie die ESRB-Einstellungen wieder her.</span><span class="sxs-lookup"><span data-stu-id="823fb-587">If changed previously, restore the ESRB settings</span></span>
    11. <span data-ttu-id="823fb-588">Wenn keine ESRB-Einstellungen vorhanden sind, wählen Sie "Bestimmte Spiele blockieren oder zulassen" aus, und wählen Sie das Spiel anhand des Namens aus.</span><span class="sxs-lookup"><span data-stu-id="823fb-588">If there are no ESRB settings, then select "Block or Allow Specific Games" and select the game by name</span></span>
    12. <span data-ttu-id="823fb-589">Melden Sie sich als Jane und als Toby an.</span><span class="sxs-lookup"><span data-stu-id="823fb-589">Log off as Jane and on as Toby</span></span>
    13. <span data-ttu-id="823fb-590">Vergewissern Sie sich, dass das Spiel nicht auf User Toby gestartet wird, wenn EXE/Name von Benutzerin Jane \[ 1.2 blockiert wird.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-590">Verify that the game does not launch on User Toby when EXE/Name is blocked by User Jane \[1.2\]</span></span>
    14. <span data-ttu-id="823fb-591">Melden Sie sich als Toby und wieder als Jane an.</span><span class="sxs-lookup"><span data-stu-id="823fb-591">Log off as Toby and back on as Jane</span></span>
    15. <span data-ttu-id="823fb-592">Öffnen Sie als Jane Benutzersteuerelemente -> Anwendungseinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="823fb-592">As Jane, open User Controls -> Application Restrictions</span></span>
    16. <span data-ttu-id="823fb-593">Klicken Sie auf "Toby kann nur die Programme verwenden, die ich zulässt", und klicken Sie dann auf OK (d.h. keine Exe-Dateien zulassen).</span><span class="sxs-lookup"><span data-stu-id="823fb-593">Click "Toby can only use the programs I allow", and then click OK (i.e. allow no exes)</span></span>
    17. <span data-ttu-id="823fb-594">Klicken Sie auf das Kontrollkästchen Alle deaktivieren und dann auf OK.</span><span class="sxs-lookup"><span data-stu-id="823fb-594">Click the Uncheck All box, and then click OK</span></span>
    18. <span data-ttu-id="823fb-595">Wechseln Sie zu Benutzersteuerelemente \| Spielesteuerelemente, und lassen Sie das jeweilige Spiel mit der ESRB-Bewertung zu.</span><span class="sxs-lookup"><span data-stu-id="823fb-595">Go to User Controls \| Games Controls and allow the specific game using the ESRB rating</span></span>
    19. <span data-ttu-id="823fb-596">Melden Sie sich als Jane an, melden Sie sich als Toby an, und versuchen Sie, das Spiel zu spielen.</span><span class="sxs-lookup"><span data-stu-id="823fb-596">Log off as Jane and log on as Toby and try to play the game</span></span>
    20. <span data-ttu-id="823fb-597">Stellen Sie sicher, dass das Spiel NICHT blockiert ist und dass Toby es spielen kann, wenn "Keine Exes zulassen" \[ auf 1.2 festgelegt ist.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-597">Verify that the game is NOT blocked and that Toby can play it when "allow no exes" is set \[1.2\]</span></span>
    21. <span data-ttu-id="823fb-598">Melden Sie sich als Benutzer Toby an, und melden Sie sich wieder als Benutzerin Jane an.</span><span class="sxs-lookup"><span data-stu-id="823fb-598">Log off as user Toby and back on as user Jane</span></span>
    22. <span data-ttu-id="823fb-599">Wechseln Sie in Systemsteuerung zu Jugendschutz, und entfernen Sie die Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="823fb-599">Go to Parental Controls in Control Panel and remove the restrictions</span></span>
    23. <span data-ttu-id="823fb-600">Vergewissern Sie sich, dass beide Benutzer jetzt das Spiel spielen können.</span><span class="sxs-lookup"><span data-stu-id="823fb-600">Verify that both users can now play the game</span></span>

4.  <span data-ttu-id="823fb-601">Fahren Sie mit [automatisierten Tests](#58-automated-tests) fort.</span><span class="sxs-lookup"><span data-stu-id="823fb-601">Proceed to [Automated Tests](#58-automated-tests)</span></span>

### <a name="58-automated-tests"></a><span data-ttu-id="823fb-602">5.8 Automatisierte Tests</span><span class="sxs-lookup"><span data-stu-id="823fb-602">5.8 Automated Tests</span></span>

1.  <span data-ttu-id="823fb-603">Überprüfen Sie, ob das Spiel keine Fehler generiert, wenn es unter Application Verifier ausgeführt wird. Weitere Informationen finden Sie in der Dokumentation zum Brandingtesttool \[ 4.2.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-603">Verify that the game does not generate failures when run under Application Verifier - See Branding Test Tool Documentation \[4.2\]</span></span>
2.  <span data-ttu-id="823fb-604">Überprüfen Sie, ob die ausführbaren Dateien des Spiels Manifeste enthalten. Weitere Informationen finden Sie unter Branding Test Tool Documentation 2.1 (Dokumentation zum Brandingtesttool \[ 2.1).\]</span><span class="sxs-lookup"><span data-stu-id="823fb-604">Verify that the game executable files contain manifests - see Branding Test Tool Documentation \[2.1\]</span></span>
3.  <span data-ttu-id="823fb-605">Vergewissern Sie sich, dass das ausführbare Dateimanifest für das Spiel "RequestedExecutionLevel" "AsInvoker" lautet. Weitere Informationen finden Sie in der Dokumentation zum Brandingtesttool \[ 2.1.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-605">Verify that the game executable file manifest requestedExecutionLevel is "AsInvoker" - see Branding Test Tool Documentation \[2.1\]</span></span>
4.  <span data-ttu-id="823fb-606">Fahren Sie mit [anderen Tests](#59-other-tests) fort.</span><span class="sxs-lookup"><span data-stu-id="823fb-606">Proceed to [Other Tests](#59-other-tests)</span></span>

### <a name="59-other-tests"></a><span data-ttu-id="823fb-607">5.9 Weitere Tests</span><span class="sxs-lookup"><span data-stu-id="823fb-607">5.9 Other Tests</span></span>

1.  <span data-ttu-id="823fb-608">Überprüfen Sie, ob die ausführbaren Dateien des Spiels eine digitale Signatur \[ 2.3 enthalten.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-608">Verify that the game executable files contain a digital signature \[2.3\]</span></span>
2.  <span data-ttu-id="823fb-609">Überprüfen Sie, ob der Spielinstallationsvorgang normal in 64-Bit-Editionen von Windows Vista und/oder Windows 7 \[ 2.3 ausgeführt wird.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-609">Verify that the game installation process runs normally on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
3.  <span data-ttu-id="823fb-610">Vergewissern Sie sich, dass beim Spiel kein Fehler aufgrund von ausführbaren 16-Bit-Dateien in 64-Bit-Editionen von Windows Vista und/oder Windows 7 \[ 2.3 auftritt.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-610">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
4.  <span data-ttu-id="823fb-611">Erzwingen des Absturzes der Anwendung beim Testen, überprüfen Sie, ob das Spiel Windows-Fehlerberichterstattung ordnungsgemäß anzeigt und Absturzdaten \[ 4.3 sammelt.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-611">Force the application to crash while testing, and verify that the game displays Windows Error Reporting properly and collects crash data \[4.3\]</span></span>
5.  <span data-ttu-id="823fb-612">Sicherstellen der richtigen Dateizusammenfassungen \[ 4.3\]</span><span class="sxs-lookup"><span data-stu-id="823fb-612">Ensure proper file summaries \[4.3\]</span></span>

    1.  <span data-ttu-id="823fb-613">Klicken Sie auf Start -> Computer.</span><span class="sxs-lookup"><span data-stu-id="823fb-613">Click Start -> Computer</span></span>
    2.  <span data-ttu-id="823fb-614">Navigieren Sie zum Spielverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="823fb-614">Navigate to the game directory</span></span>
    3.  <span data-ttu-id="823fb-615">Geben Sie im Suchfenster \*.dll</span><span class="sxs-lookup"><span data-stu-id="823fb-615">In the search window, type \*.dll</span></span>
    4.  <span data-ttu-id="823fb-616">Für jede Datei: Klicken Sie mit der rechten Maustaste auf die Datei, und klicken Sie auf Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="823fb-616">For each file: Right-click the file and click Properties</span></span>

        -   <span data-ttu-id="823fb-617">In Windows XP: Klicken Sie auf die Registerkarte Version. Stellen Sie sicher, dass die Felder Produktname, Unternehmensname und Dateiversion ordnungsgemäß aufgefüllt sind.</span><span class="sxs-lookup"><span data-stu-id="823fb-617">In Windows XP: Click the Version tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span> <span data-ttu-id="823fb-618">\[4.3\]</span><span class="sxs-lookup"><span data-stu-id="823fb-618">\[4.3\]</span></span>
        -   <span data-ttu-id="823fb-619">Unter Windows Vista und Windows 7: Klicken Sie auf die Registerkarte Details. Vergewissern Sie sich, dass die Felder Produktname und Dateiversion ordnungsgemäß ausgefüllt sind.</span><span class="sxs-lookup"><span data-stu-id="823fb-619">In Windows Vista and Windows 7: Click the Details tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="823fb-620">Der Unternehmensname ist auf der Eigenschaftenseite 4.3 von Windows Vista oder Windows 7 nicht sichtbar. \[\]</span><span class="sxs-lookup"><span data-stu-id="823fb-620">Company Name is not visible in the Windows Vista or Windows 7 properties page \[4.3\]</span></span>

    5.  <span data-ttu-id="823fb-621">Wiederholen Sie diese Überprüfung für .exe Dateien.</span><span class="sxs-lookup"><span data-stu-id="823fb-621">Repeat this check for .exe files</span></span>

6.  <span data-ttu-id="823fb-622">Starten Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="823fb-622">Launch the game.</span></span>

    1.  <span data-ttu-id="823fb-623">Drücken Sie STRG+ALT+ENTF.</span><span class="sxs-lookup"><span data-stu-id="823fb-623">Press CTRL+ALT+DEL</span></span>
    2.  <span data-ttu-id="823fb-624">Klicken Sie auf den Pfeil "Optionen zum Herunterfahren".</span><span class="sxs-lookup"><span data-stu-id="823fb-624">Click the "Shutdown Options" arrow</span></span>
    3.  <span data-ttu-id="823fb-625">Klicken Sie auf Neu starten.</span><span class="sxs-lookup"><span data-stu-id="823fb-625">Click Restart</span></span>
    4.  <span data-ttu-id="823fb-626">Vergewissern Sie sich, dass das Herunterfahren 3.1 durch das Spiel nicht blockiert \[ wird.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-626">Verify game does not block shutdown \[3.1\]</span></span>

7.  <span data-ttu-id="823fb-627">Fahren Sie mit [der Deinstallation fort.](#510-uninstall)</span><span class="sxs-lookup"><span data-stu-id="823fb-627">Proceed to [Uninstall](#510-uninstall)</span></span>

### <a name="510-uninstall"></a><span data-ttu-id="823fb-628">5.10 Deinstallieren</span><span class="sxs-lookup"><span data-stu-id="823fb-628">5.10 Uninstall</span></span>

-   <span data-ttu-id="823fb-629">Stellen Sie sicher, dass beim Deinstallationsprozess des Spiels alle installierten, nicht neu verteilten Betriebssystemkomponentendateien entfernt werden und alle Einstellungen \[ 3.1 gelöscht werden.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-629">Verify that the game uninstallation process removes all installed, non-redistributed operating system component files and clears all settings \[3.1\]</span></span>

    -   <span data-ttu-id="823fb-630">Vergewissern Sie sich in Windows Vista oder Windows 7, dass Systemsteuerung die einzige Möglichkeit ist, das Programm \[ 1.1 zu entfernen.\]</span><span class="sxs-lookup"><span data-stu-id="823fb-630">Verify in Windows Vista or Windows 7 that Control Panel is the only way to remove the program \[1.1\]</span></span>

## <a name="test-tool-notes"></a><span data-ttu-id="823fb-631">Testtoolhinweise</span><span class="sxs-lookup"><span data-stu-id="823fb-631">Test Tool Notes</span></span>

<span data-ttu-id="823fb-632">Dies sind Hinweise für jedes der Testtools, die in den obigen Testanforderungen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="823fb-632">These are notes for each of the test tools listed in the above test requirements.</span></span>

### <a name="61-appverifier-40-or-higher"></a><span data-ttu-id="823fb-633">6.1 Appverifier 4.0 (oder höher)</span><span class="sxs-lookup"><span data-stu-id="823fb-633">6.1 Appverifier 4.0 (or higher)</span></span>

<span data-ttu-id="823fb-634">**Testfall: 2.5, 4.2**</span><span class="sxs-lookup"><span data-stu-id="823fb-634">**Test Case: 2.5, 4.2**</span></span>

> [!Note]  
> <span data-ttu-id="823fb-635">Einige Anwendungen können aufgrund des Kopierschutzes nicht mit AppVerifier ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-635">Some applications fail to run with AppVerifier running, because of copy protection.</span></span> <span data-ttu-id="823fb-636">Dies kann durch Ausführen einer nicht geschützten Releaseversion der ausführbaren Spieldatei behoben werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-636">This can be resolved by running with an unprotected release version of the game executable.</span></span>

 

1.  <span data-ttu-id="823fb-637">Installieren von AppVerifier 4.0 (oder höher) auf einem Computer mit Windows XP</span><span class="sxs-lookup"><span data-stu-id="823fb-637">Install AppVerifier 4.0 (or higher) on a computer running Windows XP</span></span>
2.  <span data-ttu-id="823fb-638">Starten Sie AppVerifier, und klicken Sie auf Datei -> Anwendung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="823fb-638">Launch AppVerifier and click File -> Add Application</span></span>
3.  <span data-ttu-id="823fb-639">Suchen Sie die ausführbare Spieldatei, wählen Sie sie aus, und klicken Sie auf Öffnen.</span><span class="sxs-lookup"><span data-stu-id="823fb-639">Locate the game executable, select it and click Open</span></span>
4.  <span data-ttu-id="823fb-640">Wählen Sie im Abschnitt "Anwendungen" die ausführbare Spieldatei aus.</span><span class="sxs-lookup"><span data-stu-id="823fb-640">In the "Applications" section, select the game executable</span></span>
5.  <span data-ttu-id="823fb-641">Wählen Sie im Abschnitt "Grundlagen" die folgenden Tests aus:</span><span class="sxs-lookup"><span data-stu-id="823fb-641">Select the following tests in the "Basics" section:</span></span>

    -   <span data-ttu-id="823fb-642">Ziehpunkte</span><span class="sxs-lookup"><span data-stu-id="823fb-642">Handles</span></span>
    -   <span data-ttu-id="823fb-643">Heaps</span><span class="sxs-lookup"><span data-stu-id="823fb-643">Heaps</span></span>
    -   <span data-ttu-id="823fb-644">Locks</span><span class="sxs-lookup"><span data-stu-id="823fb-644">Locks</span></span>
    -   <span data-ttu-id="823fb-645">Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="823fb-645">Memory</span></span>
    -   <span data-ttu-id="823fb-646">TLS</span><span class="sxs-lookup"><span data-stu-id="823fb-646">TLS</span></span>

6.  <span data-ttu-id="823fb-647">Wählen Sie im Abschnitt "Sonstiges" die folgenden Tests aus:</span><span class="sxs-lookup"><span data-stu-id="823fb-647">Select the following tests in the "Miscellaneous" section:</span></span>

    -   <span data-ttu-id="823fb-648">DangerousAPIs</span><span class="sxs-lookup"><span data-stu-id="823fb-648">DangerousAPIs</span></span>
    -   <span data-ttu-id="823fb-649">DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="823fb-649">DirtyStacks</span></span>

7.  <span data-ttu-id="823fb-650">Sicherstellen, dass nicht alle anderen Tests ausgewählt sind</span><span class="sxs-lookup"><span data-stu-id="823fb-650">Ensure all other tests are not selected</span></span>
8.  <span data-ttu-id="823fb-651">Starten des Spiels</span><span class="sxs-lookup"><span data-stu-id="823fb-651">Launch the game</span></span>
9.  <span data-ttu-id="823fb-652">Spielen Sie das Spiel.</span><span class="sxs-lookup"><span data-stu-id="823fb-652">Play the game</span></span>
10. <span data-ttu-id="823fb-653">Schließen des Spiels</span><span class="sxs-lookup"><span data-stu-id="823fb-653">Close the game</span></span>
11. <span data-ttu-id="823fb-654">Wählen Sie in AppVerifier die Option -> Protokolle anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="823fb-654">In AppVerifier select View -> Logs</span></span>
12. <span data-ttu-id="823fb-655">Wählen Sie im Abschnitt "Anwendungen" die App-.exe datei aus.</span><span class="sxs-lookup"><span data-stu-id="823fb-655">In the "Applications" section select the app .exe file</span></span>
13. <span data-ttu-id="823fb-656">Wählen Sie im Abschnitt "Protokolle" die Protokolldatei aus, und beobachten Sie die Fehleranzahl.</span><span class="sxs-lookup"><span data-stu-id="823fb-656">In the "Logs" section, select the log file and observe the error count.</span></span> <span data-ttu-id="823fb-657">Wenn keine Fehler auftreten, beenden Sie AppVerifier-Tests.</span><span class="sxs-lookup"><span data-stu-id="823fb-657">If there are no errors, then end AppVerifier tests.</span></span> <span data-ttu-id="823fb-658">Wenn Fehler auftreten, klicken Sie auf die Schaltfläche Ansicht.</span><span class="sxs-lookup"><span data-stu-id="823fb-658">If there are errors, click the View button</span></span>
14. <span data-ttu-id="823fb-659">Durchsuchen Sie das Dokument (STRG+F) nach Severity="Error</span><span class="sxs-lookup"><span data-stu-id="823fb-659">Search the document (CTRL+F) for Severity="Error</span></span>
15. <span data-ttu-id="823fb-660">Erstellen von Fehlern basierend auf dem LayerName=-Teil des Fehlers</span><span class="sxs-lookup"><span data-stu-id="823fb-660">Create bugs based on the LayerName= portion of the failure</span></span>

### <a name="62-manifest-test---mtexe"></a><span data-ttu-id="823fb-661">6.2 Manifesttest – mt.exe</span><span class="sxs-lookup"><span data-stu-id="823fb-661">6.2 Manifest Test - mt.exe</span></span>

<span data-ttu-id="823fb-662">**Testfall: 1.8, 2.1**</span><span class="sxs-lookup"><span data-stu-id="823fb-662">**Test Case: 1.8, 2.1**</span></span>

<span data-ttu-id="823fb-663">Dieses Tool wird über eine Eingabeaufforderung ausgeführt, in der sich MT.exe befindet.</span><span class="sxs-lookup"><span data-stu-id="823fb-663">This tool is run from a command prompt where MT.exe is located.</span></span>

<span data-ttu-id="823fb-664">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="823fb-664">Example:</span></span>

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  <span data-ttu-id="823fb-665">Klicken Sie auf Start -> Run -> geben Sie cmd ein, und klicken Sie auf die Schaltfläche OK.</span><span class="sxs-lookup"><span data-stu-id="823fb-665">Click Start -> Run -> type cmd and click the OK button</span></span>
2.  <span data-ttu-id="823fb-666">Führen Sie das mt.exe Tool aus, um eine MANIFEST-Datei für jede .exe-Datei zu generieren, die mit dem Spiel installiert wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-666">Run the mt.exe tool to generate a .manifest file for each .exe file that installs with the game</span></span>
3.  <span data-ttu-id="823fb-667">Öffnen der generierten MANIFEST-Datei</span><span class="sxs-lookup"><span data-stu-id="823fb-667">Open the generated .manifest file</span></span>
4.  <span data-ttu-id="823fb-668">Stellen Sie sicher, dass jede .exe Datei Folgendes enthält (angefordert:</span><span class="sxs-lookup"><span data-stu-id="823fb-668">Ensure that each .exe file contains the following (requested:</span></span>

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
> <span data-ttu-id="823fb-669">Die angeforderte Ausführungsebene sollte für jede Datei vorhanden sein, und dpiAware sollte mindestens für die ausführbare Datei des Spiels vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="823fb-669">Requested execution level should be present for every file, and dpiAware should be present for at least the game s executable file.</span></span>

 

### <a name="63-thread-hijacker---threadhijackerexe"></a><span data-ttu-id="823fb-670">6.3 Thread- und threadhijacker.exe</span><span class="sxs-lookup"><span data-stu-id="823fb-670">6.3 Thread Hijacker - threadhijacker.exe</span></span>

<span data-ttu-id="823fb-671">Dieses Tool wird über eine Eingabeaufforderung ausgeführt, in der sich threadhijacker.exe befindet.</span><span class="sxs-lookup"><span data-stu-id="823fb-671">This tool is run from a command prompt where threadhijacker.exe is located.</span></span>

<span data-ttu-id="823fb-672">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="823fb-672">Example:</span></span>

``` syntax
threadhijacker.exe /process:str
```

<span data-ttu-id="823fb-673">Dabei ist str der Name \_ der \_program.exe</span><span class="sxs-lookup"><span data-stu-id="823fb-673">Where str is the name\_of\_program.exe</span></span>

1.  <span data-ttu-id="823fb-674">Öffnen Sie Task-Manager, klicken Sie auf die Registerkarte Prozesse, und suchen Sie den Namen der ausführbaren Spieldatei.</span><span class="sxs-lookup"><span data-stu-id="823fb-674">Bring up Task Manager, click the Processes tab, and locate the name of the game executable.</span></span>
2.  <span data-ttu-id="823fb-675">Öffnen einer Eingabeaufforderung im Administratormodus</span><span class="sxs-lookup"><span data-stu-id="823fb-675">Open a command prompt in Admin mode</span></span>
3.  <span data-ttu-id="823fb-676">Navigieren Sie zu dem Verzeichnis, in dem sich threadhijacker.exe befindet.</span><span class="sxs-lookup"><span data-stu-id="823fb-676">Navigate to the directory where threadhijacker.exe is</span></span>
4.  <span data-ttu-id="823fb-677">Typ: **threadhijacker.exe /process:** str, wobei str der Name der ausführbaren Datei ist, die Sie erreichen möchten.</span><span class="sxs-lookup"><span data-stu-id="823fb-677">Type: **threadhijacker.exe /process:** str, where str is the name of the executable that you want to hit</span></span>

### <a name="64-microsoft-games-for-windows-test-tool"></a><span data-ttu-id="823fb-678">6.4 Microsoft Games for Windows Test Tool</span><span class="sxs-lookup"><span data-stu-id="823fb-678">6.4 Microsoft Games for Windows Test Tool</span></span>

<span data-ttu-id="823fb-679">Dieses Tool befindet sich im DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="823fb-679">This tool is located in the DirectX SDK.</span></span> <span data-ttu-id="823fb-680">Sobald das SDK auf einem Computer installiert ist, kann das Installationsprogramm für das Games for Windows Test Tool auf dem Testcomputer platziert und installiert werden.</span><span class="sxs-lookup"><span data-stu-id="823fb-680">Once the SDK is installed on a computer, the installer for the Games for Windows Test Tool can be placed on the test computer and installed.</span></span>

<span data-ttu-id="823fb-681">Suchen Sie den Installer für das Microsoft Games for Windows Test Tool auf dem Entwicklungscomputer, auf dem das DirectX SDK installiert ist.</span><span class="sxs-lookup"><span data-stu-id="823fb-681">Locate the Microsoft Games for Windows Test Tool installer on the development computer where the DirectX SDK is installed.</span></span> <span data-ttu-id="823fb-682">Standardmäßig wird sie an folgendem Speicherort platziert:</span><span class="sxs-lookup"><span data-stu-id="823fb-682">By default, it is placed in the following location:</span></span>

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  <span data-ttu-id="823fb-683">Kopieren Sie das Installationsprogramm (MicrosoftGFWTestTool.msi/setup.exe) auf den Testcomputer.</span><span class="sxs-lookup"><span data-stu-id="823fb-683">Copy the installer (MicrosoftGFWTestTool.msi / setup.exe) to the test computer.</span></span>
2.  <span data-ttu-id="823fb-684">Führen Sie das Installationsprogramm aus.</span><span class="sxs-lookup"><span data-stu-id="823fb-684">Run the installer.</span></span>
3.  <span data-ttu-id="823fb-685">Starten Sie das Testtool Microsoft Games for Windows.</span><span class="sxs-lookup"><span data-stu-id="823fb-685">Launch the Microsoft Games for Windows Test Tool.</span></span>
4.  <span data-ttu-id="823fb-686">Ersetzen Sie im Feld **Projektliste** das Feld **Neues Projekt erstellen** durch Ihren Titelnamen, und klicken Sie auf Neu **erstellen.**</span><span class="sxs-lookup"><span data-stu-id="823fb-686">In the **Project List** field replace **Create New Project** with your title name and click **Create New**.</span></span>

    <span data-ttu-id="823fb-687">Warten Sie, bis die Baseline abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="823fb-687">Wait for the Baseline to complete.</span></span>

5.  <span data-ttu-id="823fb-688">Geben Sie alle Informationen ein, die Sie möglicherweise im Abschnitt **Spielinformationen** haben, und klicken Sie auf **Spielinformationen aktualisieren.**</span><span class="sxs-lookup"><span data-stu-id="823fb-688">Fill in any information that you may have in the **Game Information** section, and click **Update Game Information**.</span></span>
6.  <span data-ttu-id="823fb-689">Klicken Sie auf die Registerkarte **Testfälle.**</span><span class="sxs-lookup"><span data-stu-id="823fb-689">Click on **Test Cases** tab.</span></span>
7.  <span data-ttu-id="823fb-690">Beginnen Sie oben mit den Testfällen, und klicken Sie je nach Bedarf auf **Erfolgreich** oder **Fehler.**</span><span class="sxs-lookup"><span data-stu-id="823fb-690">Starting at the top, proceed through the test cases, clicking **Pass** or **Fail** as appropriate.</span></span>

    <span data-ttu-id="823fb-691">Weitere Informationen zum Einschließen eines Fehlers in den Bericht finden Sie weiter unten in diesem Abschnitt unter "Schreiben eines Fehlers".</span><span class="sxs-lookup"><span data-stu-id="823fb-691">See "Writing a Bug", later in this section, for details on including a bug in the report.</span></span>

8.  <span data-ttu-id="823fb-692">Kehren Sie zur Registerkarte **Projekte** zurück, nachdem Sie den Bericht überprüft haben (durch Überprüfen der Registerkarten **Bericht** und **Fehlerbearbeitung).**</span><span class="sxs-lookup"><span data-stu-id="823fb-692">Return to the **Projects** tab after reviewing the report (by checking the **Report** and **Bug Edit** tabs).</span></span>
9.  <span data-ttu-id="823fb-693">Klicken Sie auf **Bericht kompilieren.**</span><span class="sxs-lookup"><span data-stu-id="823fb-693">Click **Compile Report**.</span></span>

    <span data-ttu-id="823fb-694">Wenn die Kompilierung des Berichts abgeschlossen ist, wird ein Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="823fb-694">A window will open when the report is finished compiling.</span></span> <span data-ttu-id="823fb-695">Hier finden Sie einen .ZIP Dateinamen *ProjectName* \_report.zip.</span><span class="sxs-lookup"><span data-stu-id="823fb-695">Here you will find a .ZIP file names *ProjectName*\_report.zip.</span></span> <span data-ttu-id="823fb-696">Diese Datei enthält alle Protokolle und Ergebnisse, die während des Testdurchlaufs gesammelt wurden.</span><span class="sxs-lookup"><span data-stu-id="823fb-696">This file contains all of the logs and results collected during the test pass.</span></span>

### <a name="writing-a-bug"></a><span data-ttu-id="823fb-697">Schreiben eines Fehlers</span><span class="sxs-lookup"><span data-stu-id="823fb-697">Writing a Bug</span></span>

<span data-ttu-id="823fb-698">Es gibt zwei Möglichkeiten, einen Fehlerbericht zu schreiben: Sie können die Testfälle durchlaufen und auf **Fehler** klicken, wenn der Titel bei einem Testfall fehlschlägt, oder Sie können auf die Registerkarte **Fehlerbearbeitung** klicken und manuell einen Fehlerbericht hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="823fb-698">There are two ways to write a bug report: you can go through the test cases and click **Fail** when the title fails a test case, or you can click the **Bug Edit** tab and manually add a bug report.</span></span>

### <a name="clicking-fail-on-a-test-case"></a><span data-ttu-id="823fb-699">Klicken auf Fehler bei einem Testfall</span><span class="sxs-lookup"><span data-stu-id="823fb-699">Clicking Fail on a test case</span></span>

1.  <span data-ttu-id="823fb-700">Wenn Sie bei einem Testfall auf **Fehler** klicken, wird die Dropdownliste **Problemtyp** automatisch auf den Testfalltyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="823fb-700">When you click **Fail** on a test case, the **Issue Type** drop-down list will automatically be set to the test case type.</span></span>
2.  <span data-ttu-id="823fb-701">Fügen Sie dem Feld **Titel** eine kurze Beschreibung hinzu, in der das Problem kurz beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="823fb-701">Add a short description to the **Title** field that briefly describes the issue.</span></span>
3.  <span data-ttu-id="823fb-702">Fügen Sie dem Feld **Beobachtetes Verhalten** eine ausführliche Beschreibung des Problems hinzu.</span><span class="sxs-lookup"><span data-stu-id="823fb-702">Add a detailed description of the issue to the **Observed Behavior** field.</span></span>
4.  <span data-ttu-id="823fb-703">Fügen Sie ggf. das erwartete Verhalten (im Gegensatz zu einer Beschreibung des Problems) zum Feld **Erwartetes Verhalten** hinzu.</span><span class="sxs-lookup"><span data-stu-id="823fb-703">As appropriate, add what was expected (as opposed to a description of the issue) to the **Expected Behavior** field.</span></span>
5.  <span data-ttu-id="823fb-704">Fügen Sie dem Feld **Reproduktionsschritte** eine ausführliche Beschreibung der Reproduktion des Problems hinzu.</span><span class="sxs-lookup"><span data-stu-id="823fb-704">Add a detailed description of how to reproduce the issue to the **Repro-Steps** field.</span></span>
6.  <span data-ttu-id="823fb-705">Klicken Sie anschließend auf die Schaltfläche **Speichern.**</span><span class="sxs-lookup"><span data-stu-id="823fb-705">When done, click the **Save** button.</span></span>

### <a name="manually-adding-a-bug"></a><span data-ttu-id="823fb-706">Manuelles Hinzufügen eines Fehlers</span><span class="sxs-lookup"><span data-stu-id="823fb-706">Manually Adding a Bug</span></span>

<span data-ttu-id="823fb-707">Dieser Vorgang entspricht dem Klicken auf **Fehler**, mit Ausnahme der automatisch aufgefüllten Dropdownliste.</span><span class="sxs-lookup"><span data-stu-id="823fb-707">This process is the same as clicking **Fail**, with the exception of the auto-populated drop-down list.</span></span> <span data-ttu-id="823fb-708">Wählen Sie in diesem Fall entweder den entsprechenden TCR-Fehlertyp aus, oder wählen Sie **\* \* Nicht-TR-Problem \* \*** für Fehler aus, die außerhalb des TR-Bereichs liegen, aber trotzdem gemeldet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="823fb-708">In this case, either select the appropriate TCR failure type or select **\*\* Non-TR Issue \*\*** for bugs that fall outside of the TR range but should still be reported.</span></span>

## <a name="resources"></a><span data-ttu-id="823fb-709">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="823fb-709">Resources</span></span>

<dl> <dt>

<span data-ttu-id="823fb-710"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Spiele für Windows: Technische Anforderungen</span><span class="sxs-lookup"><span data-stu-id="823fb-710"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Games for Windows: Technical Requirements</span></span>
</dt> <dd>

[<span data-ttu-id="823fb-711">Technische Anforderungen für Spiele für Windows: Bewährte Methoden für Spiele unter Windows XP, Windows Vista und Windows 7</span><span class="sxs-lookup"><span data-stu-id="823fb-711">Games for Windows Technical Requirements: Best Practices for Games on Windows XP, Windows Vista, and Windows 7</span></span>](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span data-ttu-id="823fb-712"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span><span class="sxs-lookup"><span data-stu-id="823fb-712"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span></span>
</dt> <dd>

[<span data-ttu-id="823fb-713">Windows SDKs</span><span class="sxs-lookup"><span data-stu-id="823fb-713">Windows SDKs</span></span>](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span data-ttu-id="823fb-714"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Richtlinien für die Benutzerkontensteuerung</span><span class="sxs-lookup"><span data-stu-id="823fb-714"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>User Account Control Guidelines</span></span>
</dt> <dd>

<span data-ttu-id="823fb-715">[Anforderungen an die Windows Vista-Anwendungsentwicklung für die Kompatibilität der Benutzerkontensteuerung](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="823fb-715">[Windows Vista Application Development Requirements for User Account Control Compatibility](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span></span>

</dd> <dt>

<span data-ttu-id="823fb-716"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer Informationen</span><span class="sxs-lookup"><span data-stu-id="823fb-716"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer Information</span></span>
</dt> <dd>

[<span data-ttu-id="823fb-717">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="823fb-717">Windows Installer</span></span>](../msi/windows-installer-portal.md)

</dd> <dt>

<span data-ttu-id="823fb-718"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Entwicklerportal</span><span class="sxs-lookup"><span data-stu-id="823fb-718"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Developer Portal</span></span> 
</dt> <dd>

[<span data-ttu-id="823fb-719">Windows Quality Online Services (Winqual)</span><span class="sxs-lookup"><span data-stu-id="823fb-719">Windows Quality Online Services (Winqual)</span></span>](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span data-ttu-id="823fb-720"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX Entwicklerportal</span><span class="sxs-lookup"><span data-stu-id="823fb-720"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX Developer Portal</span></span>
</dt> <dd>

<span data-ttu-id="823fb-721">[DirectX Developer Center](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="823fb-721">[DirectX Developer Center](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>

</dd> <dt>

<span data-ttu-id="823fb-722"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Games for Windows and DirectX SDK Blog</span><span class="sxs-lookup"><span data-stu-id="823fb-722"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Games for Windows and DirectX SDK Blog</span></span>
</dt> <dd>

[<span data-ttu-id="823fb-723">Spiele für Windows und das DirectX SDK</span><span class="sxs-lookup"><span data-stu-id="823fb-723">Games for Windows and the DirectX SDK</span></span>](https://walbourn.github.io/)

</dd> <dt>

<span data-ttu-id="823fb-724"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Zusätzliche DirectX-Artikel</span><span class="sxs-lookup"><span data-stu-id="823fb-724"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Additional DirectX Articles</span></span>
</dt> <dd>

[<span data-ttu-id="823fb-725">Technische Artikel zu DirectX</span><span class="sxs-lookup"><span data-stu-id="823fb-725">DirectX Technical Articles</span></span>](./dx9-technical-articles.md)

</dd> </dl>

 

