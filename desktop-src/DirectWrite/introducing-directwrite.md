---
title: Einführung in DirectWrite
description: Menschen kommunizieren mit Text in Ihrem täglichen Leben.
ms.assetid: ec7cc4a3-b925-48dc-920f-fd293b4c69f0
keywords:
- DirectWrite, Informationen
- DirectWrite, typografische Features
- Typografie
- DirectWrite, internationaler Text
- DirectWrite, OpenType-Schriftarten
- OpenType-Schriftarten
- DirectWrite, ClearType
- ClearType
- DirectWrite, API-Übersicht
- DirectWrite, idschreitefontface
- Idschreitefontface
- DirectWrite, Text Rendering
- DirectWrite, Renderingmodi
- DirectWrite, GDI-Interoperation
- DirectWrite, Interoperabilität
- Interoperabilität, DirectWrite
- Interoperabilität, Graphics Device Interface (GDI)
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4064feccbdbc03f4b2e4d0118e5ab704013d314e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858447"
---
# <a name="introducing-directwrite"></a><span data-ttu-id="796f8-122">Einführung in DirectWrite</span><span class="sxs-lookup"><span data-stu-id="796f8-122">Introducing DirectWrite</span></span>

<span data-ttu-id="796f8-123">Menschen kommunizieren mit Text in Ihrem täglichen Leben.</span><span class="sxs-lookup"><span data-stu-id="796f8-123">People communicate with text all the time in their daily lives.</span></span> <span data-ttu-id="796f8-124">Dies ist die primäre Methode für Personen, eine zunehmende Menge an Informationen zu verbrauchen.</span><span class="sxs-lookup"><span data-stu-id="796f8-124">It is the primary way for people to consume an increasing volume of information.</span></span> <span data-ttu-id="796f8-125">In der Vergangenheit war die Verwendung von gedruckten Inhalten, hauptsächlich Dokumenten, Zeitungen, Büchern usw.,.</span><span class="sxs-lookup"><span data-stu-id="796f8-125">In the past, it used to be through printed content, primarily documents, newspapers, books, and so on.</span></span> <span data-ttu-id="796f8-126">Es handelt sich immer mehr um Online Inhalte auf Ihrem Windows-PC.</span><span class="sxs-lookup"><span data-stu-id="796f8-126">Increasingly, it is online content on their Windows PC.</span></span> <span data-ttu-id="796f8-127">Ein typischer Windows-Benutzer verbringt viel Zeit mit dem Lesen des Computerbildschirms.</span><span class="sxs-lookup"><span data-stu-id="796f8-127">A typical Windows user spends a lot of time reading from their computer screen.</span></span> <span data-ttu-id="796f8-128">Sie können im Web Surfen, e-Mails scannen, einen Bericht verfassen, eine Kalkulations Tabelle ausfüllen oder Software schreiben, aber tatsächlich wird das Lesen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="796f8-128">They might be surfing the Web, scanning e-mail, composing a report, filling in a spreadsheet, or writing software, but what they're really doing is reading.</span></span> <span data-ttu-id="796f8-129">Obwohl Text und Schriftarten fast jeden Teil der Benutzer Darstellung in Windows durchdringen, ist das Lesen auf dem Bildschirm für die meisten Benutzer nicht so angenehm wie das Lesen der gedruckten Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="796f8-129">Even though text and fonts permeate nearly every part of the user experience in Windows, for most users, reading on the screen is not as enjoyable as reading printed output.</span></span>

<span data-ttu-id="796f8-130">Für Entwickler von Windows-Anwendungen ist das Schreiben von Text Behandlungs Code eine Herausforderung, da die Anforderungen für eine bessere Lesbarkeit, eine ausgereifte Formatierung und Layoutsteuerung sowie die Unterstützung für mehrere Sprachen, die von der Anwendung angezeigt werden müssen, erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="796f8-130">For Windows application developers, writing text-handling code is a challenge because of the increased requirements for better readability, sophisticated formatting and layout control, and support for the multiple languages the application must display.</span></span> <span data-ttu-id="796f8-131">Selbst das grundlegendste Textverarbeitungssystem muss Texteingabe, Layout, Anzeige, Bearbeitung und kopieren und einfügen zulassen.</span><span class="sxs-lookup"><span data-stu-id="796f8-131">Even the most basic text-handling system must allow for text input, layout, display, editing, and copying and pasting.</span></span> <span data-ttu-id="796f8-132">Windows-Benutzer erwarten in der Regel sogar mehr als diese grundlegenden Features, sodass auch einfache Editoren mehrere Schriftarten, verschiedene Absatzformate, eingebettete Bilder, Rechtschreibprüfung und andere Features unterstützen müssen.</span><span class="sxs-lookup"><span data-stu-id="796f8-132">Windows users commonly expect even more than these basic features, requiring even simple editors to support multiple fonts, various paragraph styles, embedded images, spell checking, and other features.</span></span> <span data-ttu-id="796f8-133">Das moderne Design der Benutzeroberfläche ist auch nicht mehr auf das nur-Text-Format beschränkt, sondern muss auch eine bessere Oberfläche mit umfangreichen Schriftarten und Textlayouts bieten.</span><span class="sxs-lookup"><span data-stu-id="796f8-133">Modern UI design is also no longer confined to single format, plain text, but needs to present a better experience with rich fonts and text layouts.</span></span>

<span data-ttu-id="796f8-134">Dies ist eine Einführung in die Art und Weise, wie [DirectWrite](direct-write-portal.md) Windows-Anwendungen ermöglicht, den Text für die Benutzeroberfläche und Dokumente zu verbessern</span><span class="sxs-lookup"><span data-stu-id="796f8-134">This is an introduction to how [DirectWrite](direct-write-portal.md) enables Windows applications to enhance the text experience for UI and documents.</span></span>

## <a name="improving-the-text-experience"></a><span data-ttu-id="796f8-135">Verbessern des Text Erlebnisses</span><span class="sxs-lookup"><span data-stu-id="796f8-135">Improving the Text Experience</span></span>

<span data-ttu-id="796f8-136">Moderne Windows-Anwendungen haben anspruchsvolle Anforderungen an Text in der Benutzeroberfläche und in den Dokumenten.</span><span class="sxs-lookup"><span data-stu-id="796f8-136">Modern Windows applications have sophisticated requirements for text in their UI and documents.</span></span> <span data-ttu-id="796f8-137">Diese umfassen eine bessere Lesbarkeit, Unterstützung für eine Vielzahl von Sprachen und Skripts sowie eine überlegene Renderingleistung.</span><span class="sxs-lookup"><span data-stu-id="796f8-137">These include better readability, support for a large variety of languages and scripts, and superior rendering performance.</span></span> <span data-ttu-id="796f8-138">Außerdem erfordern die meisten vorhandenen Anwendungen eine Möglichkeit, vorhandene Investitionen in die WindowsWin32-Codebasis auszuführen.</span><span class="sxs-lookup"><span data-stu-id="796f8-138">In addition, most existing applications require a way to carry forward existing investments in the WindowsWin32 code base.</span></span>

<span data-ttu-id="796f8-139">[DirectWrite](direct-write-portal.md) bietet die folgenden drei Features, mit denen Entwickler von Windows-Anwendungen die Textdarstellung innerhalb Ihrer Anwendungen verbessern können: Unabhängigkeit vom Renderingsystem, hochwertige Typografie und mehrere Funktionsebenen.</span><span class="sxs-lookup"><span data-stu-id="796f8-139">[DirectWrite](direct-write-portal.md) provides the following three features that enable Windows application developers to improve the text experience within their applications: independence from the rendering system, high-quality typography, and multiple layers of functionality.</span></span>

## <a name="rendering-system-independence"></a><span data-ttu-id="796f8-140">Rendering-System Unabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="796f8-140">Rendering-System Independence</span></span>

<span data-ttu-id="796f8-141">[DirectWrite](direct-write-portal.md) ist unabhängig von einer bestimmten Grafiktechnologie.</span><span class="sxs-lookup"><span data-stu-id="796f8-141">[DirectWrite](direct-write-portal.md) is independent of any particular graphics technology.</span></span> <span data-ttu-id="796f8-142">Anwendungen können die renderingtechnologie verwenden, die für Ihre Anforderungen am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="796f8-142">Applications are free to use the rendering technology best suited to their needs.</span></span> <span data-ttu-id="796f8-143">Dadurch haben Anwendungen die Flexibilität, einige Teile Ihrer Anwendung mithilfe von GDI und anderen Teilen über Direct3D oder [Direct2D](../direct2d/direct2d-portal.md)weiter zurendern.</span><span class="sxs-lookup"><span data-stu-id="796f8-143">This gives applications the flexibility to continue rendering some parts of their application through GDI and other parts through Direct3D or [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="796f8-144">Tatsächlich kann eine Anwendung das Rendern von DirectWrite über einen proprietären renderingstapel auswählen.</span><span class="sxs-lookup"><span data-stu-id="796f8-144">In fact, an application could choose to render DirectWrite through a proprietary rendering stack.</span></span>

## <a name="high-quality-typography"></a><span data-ttu-id="796f8-145">TypografieHigh-Quality</span><span class="sxs-lookup"><span data-stu-id="796f8-145">High-Quality Typography</span></span>

<span data-ttu-id="796f8-146">[DirectWrite](direct-write-portal.md) nutzt die Verbesserungen in der [OpenType](../intl/opentype-font-format.md) -Schriftart Technologie, um qualitativ hochwertige Typografie innerhalb einer Windows-Anwendung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="796f8-146">[DirectWrite](direct-write-portal.md) takes advantage of the advances in [OpenType](../intl/opentype-font-format.md) Font technology to enable high quality typography within a Windows application.</span></span> <span data-ttu-id="796f8-147">Das Schriftart System von DirectWrite bietet Dienste für den Umgang mit Schriftart Enumeration, Schriftart fallback und Schriftart Caching, die alle von Anwendungen zum Verarbeiten von Schriftarten benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="796f8-147">The DirectWrite font system provides services for dealing with font enumeration, font fallback, and font caching, which are all needed by applications for handling fonts.</span></span>

<span data-ttu-id="796f8-148">Die von [DirectWrite](direct-write-portal.md) bereitgestellte [OpenType](../intl/opentype-font-format.md) -Unterstützung ermöglicht es Entwicklern, Ihren Anwendungen Erweiterte typografische Features und Unterstützung für internationalen Text hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="796f8-148">The [OpenType](../intl/opentype-font-format.md) support provided by [DirectWrite](direct-write-portal.md) enables developers to add to their applications advanced typographic features and support for international text.</span></span>

## <a name="support-for-advanced-typographic-features"></a><span data-ttu-id="796f8-149">Unterstützung für erweiterte typografische Features</span><span class="sxs-lookup"><span data-stu-id="796f8-149">Support for Advanced Typographic Features</span></span>

<span data-ttu-id="796f8-150">Mithilfe von [DirectWrite](direct-write-portal.md) können Anwendungsentwickler die Features von OpenType-Schriftarten entsperren, die Sie in WinForms oder GDI nicht verwenden können.</span><span class="sxs-lookup"><span data-stu-id="796f8-150">[DirectWrite](direct-write-portal.md) enables application developers to unlock the features of OpenType fonts that they couldn't use in WinForms or GDI.</span></span> <span data-ttu-id="796f8-151">Das "DirectWrite [**idwrite tetypografie**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) "-Objekt macht viele erweiterte Features von OpenType-Schriftarten verfügbar, wie z. b. Stilvarianten und Swashes.</span><span class="sxs-lookup"><span data-stu-id="796f8-151">The DirectWrite [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) object exposes many of the advanced features of OpenType fonts, such as stylistic alternates and swashes.</span></span> <span data-ttu-id="796f8-152">Das Microsoft Windows Software Development Kit (SDK) bietet eine Reihe von [OpenType](../intl/opentype-font-format.md) -Beispiel Schriftarten, die mit umfangreichen Funktionen wie den Schriftarten "Pericles" und "Pescadero" entworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="796f8-152">The Microsoft Windows Software Development Kit (SDK) provides a set of sample [OpenType](../intl/opentype-font-format.md) fonts that are designed with rich features, such as the Pericles and Pescadero fonts.</span></span> <span data-ttu-id="796f8-153">Weitere Informationen zu OpenType-Funktionen finden Sie unter [OpenType-Schriftart Features](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="796f8-153">For more details on OpenType features, see [OpenType Font Features](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).</span></span>

## <a name="support-for-international-text"></a><span data-ttu-id="796f8-154">Unterstützung für internationalen Text</span><span class="sxs-lookup"><span data-stu-id="796f8-154">Support for International Text</span></span>

<span data-ttu-id="796f8-155">[DirectWrite](direct-write-portal.md) verwendet [OpenType](../intl/opentype-font-format.md) -Schriftarten, um eine umfassende Unterstützung für internationalen Text zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="796f8-155">[DirectWrite](direct-write-portal.md) uses [OpenType](../intl/opentype-font-format.md) fonts to enable broad support for international text.</span></span> <span data-ttu-id="796f8-156">Unicode-Features, wie z. b. Surrogates, Bidi, Zeilenumbruch und UVS, werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="796f8-156">Unicode features such as surrogates, BIDI, line breaking, and UVS are supported.</span></span> <span data-ttu-id="796f8-157">Durch sprachgesteuerte Skripterstellung, Zahlen Ersetzung und Symbol Strukturierung wird sichergestellt, dass der Text in jedem Skript über das richtige Layout und Rendering verfügt.</span><span class="sxs-lookup"><span data-stu-id="796f8-157">Language-guided script itemization, number substitution, and glyph shaping ensure that text in any script has the correct layout and rendering.</span></span>

<span data-ttu-id="796f8-158">Die folgenden Skripts werden zurzeit unterstützt:</span><span class="sxs-lookup"><span data-stu-id="796f8-158">The following scripts are currently supported:</span></span>

> [!Note]  
> <span data-ttu-id="796f8-159">Bei Skripts, die mit einem gekennzeichnet \* sind, gibt es keine standardmäßigen System Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="796f8-159">For scripts marked with an \*, there are no default system fonts.</span></span> <span data-ttu-id="796f8-160">Anwendungen müssen Schriftarten installieren, die diese Skripts unterstützen.</span><span class="sxs-lookup"><span data-stu-id="796f8-160">Applications must install fonts that support these scripts.</span></span>

 

-   <span data-ttu-id="796f8-161">Arabisch</span><span class="sxs-lookup"><span data-stu-id="796f8-161">Arabic</span></span>
-   <span data-ttu-id="796f8-162">Armenisch</span><span class="sxs-lookup"><span data-stu-id="796f8-162">Armenian</span></span>
-   <span data-ttu-id="796f8-163">Bengala</span><span class="sxs-lookup"><span data-stu-id="796f8-163">Bengala</span></span>
-   <span data-ttu-id="796f8-164">Bopomofo</span><span class="sxs-lookup"><span data-stu-id="796f8-164">Bopomofo</span></span>
-   <span data-ttu-id="796f8-165">Braille\*</span><span class="sxs-lookup"><span data-stu-id="796f8-165">Braille\*</span></span>
-   <span data-ttu-id="796f8-166">Kanadische Aborigines-Silben</span><span class="sxs-lookup"><span data-stu-id="796f8-166">Canadian aboriginal syllabics</span></span>
-   <span data-ttu-id="796f8-167">Cherokee</span><span class="sxs-lookup"><span data-stu-id="796f8-167">Cherokee</span></span>
-   <span data-ttu-id="796f8-168">Chinesisch (vereinfacht & traditionell)</span><span class="sxs-lookup"><span data-stu-id="796f8-168">Chinese (Simplified & Traditional)</span></span>
-   <span data-ttu-id="796f8-169">Kyrillisch</span><span class="sxs-lookup"><span data-stu-id="796f8-169">Cyrillic</span></span>
-   <span data-ttu-id="796f8-170">Koptisch\*</span><span class="sxs-lookup"><span data-stu-id="796f8-170">Coptic\*</span></span>
-   <span data-ttu-id="796f8-171">Devanagari</span><span class="sxs-lookup"><span data-stu-id="796f8-171">Devanagari</span></span>
-   <span data-ttu-id="796f8-172">Ethiopic</span><span class="sxs-lookup"><span data-stu-id="796f8-172">Ethiopic</span></span>
-   <span data-ttu-id="796f8-173">Georgisch</span><span class="sxs-lookup"><span data-stu-id="796f8-173">Georgian</span></span>
-   <span data-ttu-id="796f8-174">Glagolitisch\*</span><span class="sxs-lookup"><span data-stu-id="796f8-174">Glagolitic\*</span></span>
-   <span data-ttu-id="796f8-175">Griechisch</span><span class="sxs-lookup"><span data-stu-id="796f8-175">Greek</span></span>
-   <span data-ttu-id="796f8-176">Gujarati</span><span class="sxs-lookup"><span data-stu-id="796f8-176">Gujarati</span></span>
-   <span data-ttu-id="796f8-177">Gurmukhi</span><span class="sxs-lookup"><span data-stu-id="796f8-177">Gurmukhi</span></span>
-   <span data-ttu-id="796f8-178">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="796f8-178">Hebrew</span></span>
-   <span data-ttu-id="796f8-179">Japanisch</span><span class="sxs-lookup"><span data-stu-id="796f8-179">Japanese</span></span>
-   <span data-ttu-id="796f8-180">Kannada</span><span class="sxs-lookup"><span data-stu-id="796f8-180">Kannada</span></span>
-   <span data-ttu-id="796f8-181">Khmer</span><span class="sxs-lookup"><span data-stu-id="796f8-181">Khmer</span></span>
-   <span data-ttu-id="796f8-182">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="796f8-182">Korean</span></span>
-   <span data-ttu-id="796f8-183">Laotisch</span><span class="sxs-lookup"><span data-stu-id="796f8-183">Lao</span></span>
-   <span data-ttu-id="796f8-184">Lateinisch</span><span class="sxs-lookup"><span data-stu-id="796f8-184">Latin</span></span>
-   <span data-ttu-id="796f8-185">Malayalam</span><span class="sxs-lookup"><span data-stu-id="796f8-185">Malayalam</span></span>
-   <span data-ttu-id="796f8-186">Mongolisch</span><span class="sxs-lookup"><span data-stu-id="796f8-186">Mongolian</span></span>
-   <span data-ttu-id="796f8-187">Myanmar</span><span class="sxs-lookup"><span data-stu-id="796f8-187">Myanmar</span></span>
-   <span data-ttu-id="796f8-188">Neue Tai-Lue</span><span class="sxs-lookup"><span data-stu-id="796f8-188">New Tai Lue</span></span>
-   <span data-ttu-id="796f8-189">Ogam\*</span><span class="sxs-lookup"><span data-stu-id="796f8-189">Ogham\*</span></span>
-   <span data-ttu-id="796f8-190">Odia</span><span class="sxs-lookup"><span data-stu-id="796f8-190">Odia</span></span>
-   <span data-ttu-id="796f8-191">"Phags-pa"</span><span class="sxs-lookup"><span data-stu-id="796f8-191">'Phags-pa</span></span>
-   <span data-ttu-id="796f8-192">Runisch\*</span><span class="sxs-lookup"><span data-stu-id="796f8-192">Runic\*</span></span>
-   <span data-ttu-id="796f8-193">Singhalesisch</span><span class="sxs-lookup"><span data-stu-id="796f8-193">Sinhala</span></span>
-   <span data-ttu-id="796f8-194">Syrisch</span><span class="sxs-lookup"><span data-stu-id="796f8-194">Syriac</span></span>
-   <span data-ttu-id="796f8-195">Tai-Le</span><span class="sxs-lookup"><span data-stu-id="796f8-195">Tai Le</span></span>
-   <span data-ttu-id="796f8-196">Tamilisch</span><span class="sxs-lookup"><span data-stu-id="796f8-196">Tamil</span></span>
-   <span data-ttu-id="796f8-197">Telugu</span><span class="sxs-lookup"><span data-stu-id="796f8-197">Telugu</span></span>
-   <span data-ttu-id="796f8-198">Thaana</span><span class="sxs-lookup"><span data-stu-id="796f8-198">Thaana</span></span>
-   <span data-ttu-id="796f8-199">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="796f8-199">Thai</span></span>
-   <span data-ttu-id="796f8-200">Tibetisch</span><span class="sxs-lookup"><span data-stu-id="796f8-200">Tibetan</span></span>
-   <span data-ttu-id="796f8-201">Yi</span><span class="sxs-lookup"><span data-stu-id="796f8-201">Yi</span></span>

## <a name="multiple-layers-of-functionality"></a><span data-ttu-id="796f8-202">Mehrere Funktionsebenen</span><span class="sxs-lookup"><span data-stu-id="796f8-202">Multiple Layers of Functionality</span></span>

<span data-ttu-id="796f8-203">[DirectWrite](direct-write-portal.md) bietet faktorisierte Funktionsebenen, wobei jede Ebene nahtlos mit der nächsten interagiert.</span><span class="sxs-lookup"><span data-stu-id="796f8-203">[DirectWrite](direct-write-portal.md) provides factored layers of functionality, with each layer interacting seamlessly with the next.</span></span> <span data-ttu-id="796f8-204">Der API-Entwurf bietet Anwendungsentwicklern die Freiheit und Flexibilität, individuelle Schichten abhängig von Ihren Anforderungen und dem Zeitplan zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="796f8-204">The API design gives application developers the freedom and flexibility to adopt individual layers depending on their needs and schedule.</span></span> <span data-ttu-id="796f8-205">Das folgende Diagramm zeigt die Beziehung zwischen diesen Ebenen.</span><span class="sxs-lookup"><span data-stu-id="796f8-205">The following diagram shows the relationship between these layers.</span></span>

![Diagramm der DirectWrite-Ebenen und ihrer Kommunikation mit einer Anwendung oder einem UI-Framework und der Grafik-API](images/intro-01.png)

<span data-ttu-id="796f8-207">Die textlayoutapi bietet die Funktionen der höchsten Ebene, die in [DirectWrite](direct-write-portal.md)verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="796f8-207">The text layout API provides the highest level functionality available from [DirectWrite](direct-write-portal.md).</span></span> <span data-ttu-id="796f8-208">Es stellt Dienste für die Anwendung bereit, mit denen umfangreich formatierte Text Zeichenfolgen gemessen, angezeigt und mit ihnen interagieren können.</span><span class="sxs-lookup"><span data-stu-id="796f8-208">It provides services for the application to measure, display, and interact with richly formatted text strings.</span></span> <span data-ttu-id="796f8-209">Diese Text-API kann in Anwendungen verwendet werden, die derzeit Win32's DrawText verwenden, um eine moderne Benutzeroberfläche mit Umfang reichformatiertem Text zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="796f8-209">This text API can be used in applications that currently use Win32's DrawText to build a modern UI with richly formatted text.</span></span>

<span data-ttu-id="796f8-210">Text intensive Anwendungen, die ihre eigene LayoutEngine implementieren, können die nächste Ebene nach unten verwenden: der Skript Prozessor.</span><span class="sxs-lookup"><span data-stu-id="796f8-210">Text-intensive applications that implement their own layout engine may use the next layer down: the script processor.</span></span> <span data-ttu-id="796f8-211">Der Skript Prozessor teilt einen Text Block in Skriptblöcke auf und behandelt die Zuordnung zwischen Unicode-Darstellungen und der entsprechenden Symboldarstellung in der Schriftart, damit der Text des Skripts ordnungsgemäß in der richtigen Sprache angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="796f8-211">The script processor breaks down a chunk of text into script blocks and handles the mapping between Unicode representations to the appropriate glyph representation in the font so the text of the script can be correctly displayed in the correct language.</span></span> <span data-ttu-id="796f8-212">Das Layoutsystem, das von der textlayoutapi-Ebene verwendet wird, basiert auf dem Schriftart-und Skript Verarbeitungssystem.</span><span class="sxs-lookup"><span data-stu-id="796f8-212">The layout system used by the text layout API layer is built upon the font and script processing system.</span></span>

<span data-ttu-id="796f8-213">Die Glyphe-renderingschicht ist die niedrigste Funktionalitäts Ebene und bietet Funktionen zum Rendern von Symbolen für Anwendungen, die ihre eigene Textlayoutengine implementieren.</span><span class="sxs-lookup"><span data-stu-id="796f8-213">The glyph-rendering layer is the lowest layer of functionality and provides glyph-rendering functionality for applications that implement their own text layout engine.</span></span> <span data-ttu-id="796f8-214">Die Symbol Rendering-Ebene ist auch nützlich für Anwendungen, die einen benutzerdefinierten Renderer implementieren, um das Symbol zum Zeichnen von Symbolen durch die Rückruffunktion in der [DirectWrite](direct-write-portal.md) -Text Formatierungs-API zu ändern.</span><span class="sxs-lookup"><span data-stu-id="796f8-214">The glyph rendering layer is also useful for applications that implement a custom renderer to modify the glyph-drawing behavior through the callback function in the [DirectWrite](direct-write-portal.md) text-formatting API.</span></span>

<span data-ttu-id="796f8-215">Das Schriftart System von [DirectWrite](direct-write-portal.md) ist für alle DirectWrite-Funktionsebenen verfügbar und ermöglicht es einer Anwendung, auf Schriftart-und Symbol Informationen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="796f8-215">The [DirectWrite](direct-write-portal.md) font system is available to all the DirectWrite functional layers and enables an application to access font and glyph information.</span></span> <span data-ttu-id="796f8-216">Es wurde entwickelt, um allgemeine Schriftart Technologien und Datenformate zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="796f8-216">It is designed to handle common font technologies and data formats.</span></span> <span data-ttu-id="796f8-217">Das DirectWrite-Schrift Modell folgt der allgemeinen typografischen Praxis, bei der eine beliebige Anzahl von Gewichtungen, Stilen und Strecken in derselben Schriftfamilie unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="796f8-217">The DirectWrite font model follows the common typographic practice of supporting any number of weights, styles, and stretches in the same font family.</span></span> <span data-ttu-id="796f8-218">Dieses Modell, das gleiche Modell, gefolgt von WPF und CSS, gibt an, dass Schriftarten, die sich nur in Gewichtung (Fett, hell usw.), Style (AUFSTEIG, kursiv oder schräg) oder Streckung (schmal, komprimiert, breit usw.) unterscheiden, als Member einer einzelnen Schriftfamilie betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="796f8-218">This model, the same model followed by WPF and CSS, specifies that fonts differing only in weight (bold, light, and so on), style (upright, italic, or oblique) or stretch (narrow, condensed, wide, and so on) are considered to be members of a single font family.</span></span>

### <a name="improved-text-rendering-with-cleartype"></a><span data-ttu-id="796f8-219">Verbessertes Text Rendering mit ClearType</span><span class="sxs-lookup"><span data-stu-id="796f8-219">Improved Text Rendering with ClearType</span></span>

<span data-ttu-id="796f8-220">Das verbessern der Lesbarkeit auf dem Bildschirm ist eine wichtige Voraussetzung für alle Windows-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="796f8-220">Improving readability on the screen is a key requirement for all Windows applications.</span></span> <span data-ttu-id="796f8-221">Der Beweis der Forschung in Cognitive Psychologie deutet darauf hin, dass wir in der Lage sein müssen, jeden Buchstaben genau zu erkennen, und dass sogar der Abstand zwischen Buchstaben für die schnelle Verarbeitung entscheidend ist.</span><span class="sxs-lookup"><span data-stu-id="796f8-221">The evidence from research in cognitive psychology indicates that we need to be able to recognize every letter accurately and that even spacing between letters is critical for fast processing.</span></span> <span data-ttu-id="796f8-222">Buchstaben und Wörter, die nicht symmetrisch sind, werden als hässlich empfunden und beeinträchtigen das Leseverhalten.</span><span class="sxs-lookup"><span data-stu-id="796f8-222">Letters and words that are not symmetrical are perceived as ugly and degrade the reading experience.</span></span> <span data-ttu-id="796f8-223">Kevin Larson, Microsoft Advanced Reading Technologies Group, hat einen Artikel zu dem Thema verfasst, das in "Spektrum IEEE" veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="796f8-223">Kevin Larson, Microsoft Advanced Reading Technologies group, wrote an article on the subject that was published in Spectrum IEEE.</span></span> <span data-ttu-id="796f8-224">Der Artikel wird als "die Technologie von Text" bezeichnet ( https://www.spectrum.ieee.org/print/5049) .</span><span class="sxs-lookup"><span data-stu-id="796f8-224">The article is called "The Technology of Text" (https://www.spectrum.ieee.org/print/5049).</span></span>

<span data-ttu-id="796f8-225">Der Text in [DirectWrite](direct-write-portal.md) wird mithilfe von Microsoft ClearType gerendert, wodurch die Übersichtlichkeit und Lesbarkeit von Text verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="796f8-225">Text in [DirectWrite](direct-write-portal.md) is rendered using Microsoft ClearType, which enhances the clarity and readability of text.</span></span> <span data-ttu-id="796f8-226">ClearType nutzt die Tatsache, dass moderne LCD-Fenster RGB-Streifen für jedes Pixel aufweisen, das einzeln gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="796f8-226">ClearType takes advantage of the fact that modern LCD displays have RGB stripes for each pixel that can be controlled individually.</span></span> <span data-ttu-id="796f8-227">DirectWrite verwendet die neuesten Erweiterungen von ClearType, die zuerst in Windows Vista mit Windows Presentation Foundation enthalten waren, sodass es nicht nur die einzelnen Buchstaben, sondern auch den Abstand zwischen Buchstaben auswerten kann.</span><span class="sxs-lookup"><span data-stu-id="796f8-227">DirectWrite uses the latest enhancements to ClearType, first included with Windows Vista with Windows Presentation Foundation, that enables it to evaluate not just the individual letters but also the spacing between letters.</span></span> <span data-ttu-id="796f8-228">Vor diesen ClearType-Erweiterungen war es schwierig, Text mit einer "Lese"-Größe von 10 oder 12 Punkten anzuzeigen: Wir konnten entweder 1 Pixel zwischen Buchstaben platzieren, was oft zu wenig war, oder 2 Pixel, was oft zu viel war.</span><span class="sxs-lookup"><span data-stu-id="796f8-228">Before these ClearType enhancements, text with a "reading" size of 10 or 12 points was difficult to display: we could place either 1 pixel in between letters, which was often too little, or 2 pixels, which was often too much.</span></span> <span data-ttu-id="796f8-229">Die Verwendung der zusätzlichen Auflösung in den Subpixeln stellt uns einen Bruch Bruch dar, der die Gleichmäßigkeit und Symmetrie der gesamten Seite verbessert.</span><span class="sxs-lookup"><span data-stu-id="796f8-229">Using the extra resolution in the subpixels provides us with fractional spacing, which improves the evenness and symmetry of the entire page.</span></span>

<span data-ttu-id="796f8-230">In der folgenden Abbildung wird gezeigt, wie Symbole bei der Positionierung von Subpixeln an einer beliebigen Subpixelgrenze beginnen können.</span><span class="sxs-lookup"><span data-stu-id="796f8-230">The following two illustration show how glyphs may begin on any sub-pixel boundary when sub-pixel positioning is used.</span></span>

<span data-ttu-id="796f8-231">Die folgende Abbildung wird mithilfe der GDI-Version des ClearType-Renderers gerendert, der keine unter Pixel Positionierung verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="796f8-231">The following illustration is rendered using the GDI version of the ClearType renderer, which did not employ sub-pixel positioning.</span></span>

![Darstellung der "Technologie", die ohne unter Pixel Positionierung gerendert wird](images/intro-03.png)

<span data-ttu-id="796f8-233">Die folgende Abbildung wird mithilfe der [DirectWrite](direct-write-portal.md) -Version des ClearType-Renderers gerendert, der die unter Pixel Positionierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="796f8-233">The following illustration is rendered using the [DirectWrite](direct-write-portal.md) version of the ClearType renderer, which uses sub-pixel positioning.</span></span>

![Abbildung der "Technologie", die mit der unter Pixel Positionierung gerendert wird](images/intro-04.png)

<span data-ttu-id="796f8-235">Beachten Sie, dass der Abstand zwischen den Buchstaben h und n mehr ist, auch im zweiten Bild, und der Buchstabe o wird weiter von dem Buchstaben n entfernt. Dies gilt auch für den Buchstaben l.</span><span class="sxs-lookup"><span data-stu-id="796f8-235">Note that the spacing between the letters h and n is more even in the second image and the letter o is spaced further from the letter n, more even with the letter l.</span></span> <span data-ttu-id="796f8-236">Beachten Sie auch, dass die Stämme auf den Buchstaben l natürlicher aussehen.</span><span class="sxs-lookup"><span data-stu-id="796f8-236">Also note how the stems on the letters l are more natural looking.</span></span>

<span data-ttu-id="796f8-237">Die Positionierung von subpixelcleartype bietet den genauesten Abstand von Zeichen auf dem Bildschirm, insbesondere bei kleinen Größen, bei denen der Unterschied zwischen einem Subpixel und einem ganzen Pixel einen signifikanten Anteil der Glyphe darstellt.</span><span class="sxs-lookup"><span data-stu-id="796f8-237">The subpixel ClearType positioning offers the most accurate spacing of characters on screen, especially at small sizes where the difference between a sub-pixel and a whole pixel represents a significant proportion of glyph width.</span></span> <span data-ttu-id="796f8-238">Sie ermöglicht die Messung von Text im idealen Auflösungs Bereich und wird an seiner natürlichen Position im LCD-Farbstreifen mit der Granularität des Subpixels gerendert.</span><span class="sxs-lookup"><span data-stu-id="796f8-238">It enables text to be measured in ideal resolution space and rendered at its natural position at the LCD color stripe, with subpixel granularity.</span></span> <span data-ttu-id="796f8-239">Text, der mit dieser Technologie gemessen und gerendert wird, ist Definitions unabhängig, d. h., dass genau dasselbe Layout von Text über den Bereich verschiedener Anzeige Auflösungen hinweg erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="796f8-239">Text measured and rendered using this technology is, by definition, resolution-independent, meaning that the exact same layout of text is achieved across the range of various display resolutions.</span></span>

<span data-ttu-id="796f8-240">Im Unterschied zu einem Typ des GDI-ClearType-Renderings bietet Sub-Pixel ClearType die präzisere Breite von Zeichen.</span><span class="sxs-lookup"><span data-stu-id="796f8-240">Unlike either type of GDI ClearType rendering, sub-pixel ClearType offers the most accurate width of characters.</span></span>

<span data-ttu-id="796f8-241">Die Text Zeichenfolgen-API übernimmt standardmäßig das Rendern von subpixeltext, d. h., Sie misst Text in seiner idealen Auflösung unabhängig von der aktuellen Bildschirmauflösung und erzeugt das Ergebnis der Symbol Positionierung basierend auf den wirklich skalierten Symbol Vorgängen und der Positions Offsets.</span><span class="sxs-lookup"><span data-stu-id="796f8-241">The Text String API adopts sub-pixel text rendering by default, which means it measures text at its ideal resolution independent of the current display resolution, and produces the glyph positioning result based on the truly scaled glyph advance widths and positioning offsets.</span></span>

<span data-ttu-id="796f8-242">Bei umfangreichen Text ermöglicht [DirectWrite](direct-write-portal.md) auch das Antialiasing entlang der y-Achse, um die Ränder zu vereinfachen und Buchstaben als den Schriftart-Designer zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="796f8-242">For large-sized text, [DirectWrite](direct-write-portal.md) also enables anti-aliasing along the y-axis to make the edges smoother and render letters as the font designer intended.</span></span> <span data-ttu-id="796f8-243">In der folgenden Abbildung ist das Antialiasing in y-Richtung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="796f8-243">The following illustration shows y-direction anti-aliasing.</span></span>

![Abbildung von "ClearType", die als GDI-Text und als DirectWrite-Text mit y-Richtung-Antialiasing gerendert wird](images/intro-05.png)

<span data-ttu-id="796f8-245">Obwohl [DirectWrite](direct-write-portal.md) -Text standardmäßig mithilfe des untergeordneten Pixels ClearType positioniert und gerendert wird, sind andere Renderingoptionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="796f8-245">Although [DirectWrite](direct-write-portal.md) text is positioned and rendered using sub-pixel ClearType by default, other rendering options are available.</span></span> <span data-ttu-id="796f8-246">Viele vorhandene Anwendungen verwenden GDI zum Rendern der meisten Benutzeroberflächen, und einige Anwendungen verwenden die Steuerelemente für die System Bearbeitung, die GDI weiterhin für das Text Rendering verwenden.</span><span class="sxs-lookup"><span data-stu-id="796f8-246">Many existing applications use GDI to render most of their UI, and some applications use system editing controls that continue to use GDI for text rendering.</span></span> <span data-ttu-id="796f8-247">Wenn Sie diesen Anwendungen DirectWrite-Text hinzufügen, kann es notwendig sein, die Verbesserungen der Lesevorgänge zu Opfern, die von Sub-Pixel ClearType bereitgestellt werden, damit der Text in der gesamten Anwendung einheitlich dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="796f8-247">When adding DirectWrite text to these applications, it may be necessary to sacrifice the reading experience improvements provided by sub-pixel ClearType so that text has a consistent appearance across the application.</span></span>

<span data-ttu-id="796f8-248">Um diese Anforderungen zu erfüllen, unterstützt [DirectWrite](direct-write-portal.md) auch die folgenden Renderingoptionen:</span><span class="sxs-lookup"><span data-stu-id="796f8-248">To meet these requirements, [DirectWrite](direct-write-portal.md) also supports the following rendering options:</span></span>

-   <span data-ttu-id="796f8-249">Sub-Pixel ClearType (Standard).</span><span class="sxs-lookup"><span data-stu-id="796f8-249">Sub-pixel ClearType (default).</span></span>
-   <span data-ttu-id="796f8-250">Unter Pixel-ClearType mit Antialiasing in horizontalen und vertikalen Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="796f8-250">Sub-pixel ClearType with anti-aliasing in both horizontal and vertical dimensions.</span></span>
-   <span data-ttu-id="796f8-251">Alias Text.</span><span class="sxs-lookup"><span data-stu-id="796f8-251">Aliased text.</span></span>
-   <span data-ttu-id="796f8-252">GDI mit natürlicher Breite (z. b. von Microsoft Word Leseansicht).</span><span class="sxs-lookup"><span data-stu-id="796f8-252">GDI natural-width (used by Microsoft Word Reading View, for example).</span></span>
-   <span data-ttu-id="796f8-253">GDI-kompatibel-Breite (einschließlich ostasiatischen eingebetteten Bitmap).</span><span class="sxs-lookup"><span data-stu-id="796f8-253">GDI compatible-width (including East Asian embedded bitmap).</span></span>

<span data-ttu-id="796f8-254">Jeder dieser Renderingmodi kann mithilfe der DirectWrite-API und über den neuen Windows 7-Posteingangs-ClearType-Tuner optimiert werden.</span><span class="sxs-lookup"><span data-stu-id="796f8-254">Each of these rendering modes can be fine-tuned through the DirectWrite API and through the new Windows 7 inbox ClearType tuner.</span></span>

> [!Note]  
> <span data-ttu-id="796f8-255">Ab Windows 8 sollten Sie in den meisten Fällen das Antialiasing für Graustufen Text verwenden.</span><span class="sxs-lookup"><span data-stu-id="796f8-255">Starting with Windows 8, you should use greyscale text antialiasing in most cases.</span></span> <span data-ttu-id="796f8-256">Weitere Informationen finden Sie im nächsten Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="796f8-256">See the next section for more information.</span></span>

 

### <a name="support-for-natural-layout"></a><span data-ttu-id="796f8-257">Unterstützung für natürliches Layout</span><span class="sxs-lookup"><span data-stu-id="796f8-257">Support for Natural Layout</span></span>

<span data-ttu-id="796f8-258">Das natürliche Layout ist auflösungsunabhängig, sodass sich der Abstand von Zeichen nicht ändert, wenn Sie vergrößern oder verkleinern oder abhängig vom dpi-Wert der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="796f8-258">Natural layout is resolution-independent, so the spacing of characters doesn't change as you zoom in or out, or depending on the DPI of the display.</span></span> <span data-ttu-id="796f8-259">Ein sekundärer Vorteil besteht darin, dass der Abstand für den Entwurf der Schriftart true ist.</span><span class="sxs-lookup"><span data-stu-id="796f8-259">A secondary advantage is that spacing is true to the design of the font.</span></span> <span data-ttu-id="796f8-260">Das natürliche Layout wird durch die Unterstützung natürlicher Rendering durch DirectWrite ermöglicht, d. h., einzelne Symbole können auf einen Bruchteil eines Pixels positioniert werden.</span><span class="sxs-lookup"><span data-stu-id="796f8-260">Natural layout is made possible by DirectWrite's support for natural rendering, which means individual glyphs can be positioned to a fraction of a pixel.</span></span>

<span data-ttu-id="796f8-261">Während das natürliche Layout der Standard ist, müssen einige Anwendungen den Text mit dem gleichen Abstand und der gleichen Darstellung wie GDI Rendering.</span><span class="sxs-lookup"><span data-stu-id="796f8-261">While natural layout is the default, some applications need to render text with the same spacing and appearance as GDI.</span></span> <span data-ttu-id="796f8-262">Für solche Anwendungen stellt DirectWrite den klassischen GDI-und GDI-Mess Modus und die entsprechenden Renderingmodi bereit.</span><span class="sxs-lookup"><span data-stu-id="796f8-262">For such applications, DirectWrite provides GDI classic and GDI natural measuring modes and corresponding rendering modes.</span></span>

<span data-ttu-id="796f8-263">Jeder der obigen Renderingmodi kann mit einem der beiden Antialiasing Modi kombiniert werden: ClearType oder Grayscale.</span><span class="sxs-lookup"><span data-stu-id="796f8-263">Any of the above rendering modes can be combined with either of the two antialiasing modes: ClearType or grayscale.</span></span> <span data-ttu-id="796f8-264">ClearType-Antialiasing Simulationen eine höhere Auflösung durch die individuelle Bearbeitung der roten, grünen und blauen Farbwerte jedes Pixels.</span><span class="sxs-lookup"><span data-stu-id="796f8-264">ClearType antialiasing simulations a higher resolution by individually manipulating the red, green, and blue color values of each pixel.</span></span> <span data-ttu-id="796f8-265">Graustufen-Antialiasing berechnet nur einen deckwert (oder einen Alpha Wert) für jedes Pixel.</span><span class="sxs-lookup"><span data-stu-id="796f8-265">Grayscale antialiasing computes only one coverage (or alpha) value for each pixel.</span></span> <span data-ttu-id="796f8-266">ClearType ist die Standardeinstellung, aber Graustufen-Antialiasing wird für Windows Store-Apps empfohlen, da es schneller ist und mit standardantialiasing kompatibel ist, während es immer noch hoch lesbar ist.</span><span class="sxs-lookup"><span data-stu-id="796f8-266">ClearType is the default, but grayscale antialiasing is recommended for Windows Store apps because it is faster and is compatible with standard antialiasing, while still being highly readable.</span></span>

## <a name="api-overview"></a><span data-ttu-id="796f8-267">API-Übersicht</span><span class="sxs-lookup"><span data-stu-id="796f8-267">API Overview</span></span>

<span data-ttu-id="796f8-268">Die [**idschreitefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) -Schnittstelle ist der Ausgangspunkt für die Verwendung von DirectWrite-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="796f8-268">The [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface is the starting point for using DirectWrite functionality.</span></span> <span data-ttu-id="796f8-269">Die Factory ist das Stamm Objekt, das eine Gruppe von Objekten erstellt, die gleichzeitig verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="796f8-269">The factory is the root object that creates a set of objects that can be used together.</span></span>

<span data-ttu-id="796f8-270">Der Formatierungs-und Layoutvorgang ist eine Voraussetzung für die Vorgänge, da Text ordnungsgemäß formatiert und für einen bestimmten Satz von Einschränkungen festgelegt werden muss, bevor er gezeichnet oder auf einen Treffer getestet werden kann.</span><span class="sxs-lookup"><span data-stu-id="796f8-270">The formatting and layout operation is a prerequisite to the operations, as text needs to be properly formatted and laid out to a specified set of constraints before it can be drawn or hit-tested.</span></span> <span data-ttu-id="796f8-271">Zwei wichtige Objekte, die Sie zu diesem Zweck mit [**idwrite tefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) erstellen können, sind [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) und [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span><span class="sxs-lookup"><span data-stu-id="796f8-271">Two key objects that you can create with an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) for this purpose are [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="796f8-272">Ein **idwrite-Textformat** -Objekt stellt die Formatierungsinformationen für einen Textabschnitt dar.</span><span class="sxs-lookup"><span data-stu-id="796f8-272">An **IDWriteTextFormat** object represents the formatting information for a paragraph of text.</span></span> <span data-ttu-id="796f8-273">Die [**idwrite Team Factory:: foratetextlayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) -Funktion nimmt die Eingabe Zeichenfolge, die zugeordneten Einschränkungen, z. b. die Dimension des zu füllenden Speicherplatzes, und das **idwrite-Textformat** -Objekt, und fügt das vollständig analysierte und formatierte Ergebnis in **idschreitetextlayout** ein, das in nachfolgenden Vorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="796f8-273">The [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) function takes the input string, the associated constraints such as the dimension of the space to be filled, and the **IDWriteTextFormat** object, and puts the fully analyzed and formatted result into **IDWriteTextLayout** to use in subsequent operations.</span></span>

<span data-ttu-id="796f8-274">Die Anwendung kann dann den Text mithilfe der von [Direct2D](../direct2d/direct2d-portal.md) bereitgestellten [**drawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Funktion oder durch Implementieren einer Rückruffunktion, die GDI, Direct2D oder andere Grafik Systeme verwenden kann, um die Symbole zu renderhen.</span><span class="sxs-lookup"><span data-stu-id="796f8-274">The application can then render the text using the [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) function provided by [Direct2D](../direct2d/direct2d-portal.md) or by implementing a callback function that can use GDI, Direct2D, or other graphics systems to render the glyphs.</span></span> <span data-ttu-id="796f8-275">Bei einem einzelnen Formatierungs Text bietet die [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Funktion auf Direct2D eine einfachere Möglichkeit, Text zu zeichnen, ohne zuerst ein [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="796f8-275">For a single format text, the [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) function on Direct2D provides a simpler way to draw text without having to first create a [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

## <a name="formatting-and-drawing-hello-world-using-directwrite"></a><span data-ttu-id="796f8-276">Formatieren und Zeichnen von "Hallo Welt" mithilfe von DirectWrite</span><span class="sxs-lookup"><span data-stu-id="796f8-276">Formatting and Drawing "Hello World" Using DirectWrite</span></span>

<span data-ttu-id="796f8-277">Im folgenden Codebeispiel wird veranschaulicht, wie eine Anwendung einen einzelnen Absatz mithilfe von [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) formatieren und mithilfe der [Direct2D](../direct2d/direct2d-portal.md)[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Funktion zeichnen kann.</span><span class="sxs-lookup"><span data-stu-id="796f8-277">The following code example shows how an application can format a single paragraph using [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and draw it using the [Direct2D](../direct2d/direct2d-portal.md)[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) function.</span></span>


```C++
HRESULT DemoApp::DrawHelloWorld(
    ID2D1HwndRenderTarget* pIRenderTarget
    )
{
    HRESULT hr = S_OK;
    ID2D1SolidColorBrush* pIRedBrush = NULL;
    IDWriteTextFormat* pITextFormat = NULL;
    IDWriteFactory* pIDWriteFactory = NULL;

    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED,
                __uuidof(IDWriteFactory),
                reinterpret_cast<IUnknown**>(&pIDWriteFactory));
    }

    if(SUCCEEDED(hr))
    {
        hr = pIDWriteFactory->CreateTextFormat(
            L"Arial", 
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL, 
            DWRITE_FONT_STYLE_NORMAL, 
            DWRITE_FONT_STRETCH_NORMAL, 
            10.0f * 96.0f/72.0f, 
            L"en-US", 
            &pITextFormat
        );
    }

    if(SUCCEEDED(hr))
    {
        hr = pIRenderTarget->CreateSolidColorBrush(
            D2D1:: ColorF(D2D1::ColorF::Red),
            &pIRedBrush
        );
    }
    
   D2D1_RECT_F layoutRect = D2D1::RectF(0.f, 0.f, 100.f, 100.f);

    // Actually draw the text at the origin.
    if(SUCCEEDED(hr))
    {
        pIRenderTarget->DrawText(
            L"Hello World",
            wcslen(L"Hello World"),
            pITextFormat,
            layoutRect, 
            pIRedBrush
        );
    }

    // Clean up.
    SafeRelease(&pIRedBrush);
    SafeRelease(&pITextFormat);
    SafeRelease(&pIDWriteFactory);

    return hr;
}
```



## <a name="accessing-the-font-system"></a><span data-ttu-id="796f8-278">Zugreifen auf das Schriftart System</span><span class="sxs-lookup"><span data-stu-id="796f8-278">Accessing the Font System</span></span>

<span data-ttu-id="796f8-279">Zusätzlich zur Angabe eines Schriftart Familiennamens für die Text Zeichenfolge mithilfe der [**idwrite tetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle im obigen Beispiel bietet [DirectWrite](direct-write-portal.md) Anwendungen mehr Kontrolle über die Schriftart Auswahl durch die Schriftart Enumeration und die Möglichkeit, eine benutzerdefinierte Schriftart Auflistung auf der Grundlage von eingebetteten Dokument Schriftarten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="796f8-279">In addition to specifying a font family name for the text string by using the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface in the example above, [DirectWrite](direct-write-portal.md) provides applications more control over font selection through font enumeration and the ability to create custom font collection based on embedded document fonts.</span></span>

<span data-ttu-id="796f8-280">Das [**idwrite-FontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) -Objekt ist eine Sammlung von Schriftfamilien.</span><span class="sxs-lookup"><span data-stu-id="796f8-280">The [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) object is a collection of font families.</span></span> <span data-ttu-id="796f8-281">DirectWrite ermöglicht den Zugriff auf die auf dem System installierten Schriftarten über eine spezielle Schriftart Sammlung, die als System Schriftart Auflistung bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="796f8-281">DirectWrite provides access to the set of fonts installed on the system through a special font collection called the system font collection.</span></span> <span data-ttu-id="796f8-282">Dies wird durch Aufrufen der [**getsystemfontcollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) -Methode des [**idwrite-Factory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) -Objekts abgerufen.</span><span class="sxs-lookup"><span data-stu-id="796f8-282">This is obtained by calling the [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) method of the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) object.</span></span> <span data-ttu-id="796f8-283">Eine Anwendung kann auch eine benutzerdefinierte Schriftart Auflistung aus einem Satz von Schriftarten erstellen, die durch einen Anwendungs definierten Rückruf, d. h. private Schriftarten, die von einer Anwendung installiert wurden, oder in ein Dokument eingebettete Schriftarten aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="796f8-283">An application can also create a custom font collection from a set of fonts enumerated by an application-defined callback, that is, private fonts installed by an application, or fonts embedded in a document.</span></span>

<span data-ttu-id="796f8-284">Die Anwendung kann dann [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) aufrufen, um ein bestimmtes FontFamily-Objekt innerhalb der Auflistung zu erhalten, und dann [**idschreitefontfamily:: getfirstmatchingfont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) aufrufen, um zu einem bestimmten [**idschreitefont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) -Objekt zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="796f8-284">The application can then call [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) to get to a specific FontFamily object within the collection, and then call [**IDWriteFontFamily::GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) to get to a specific [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object.</span></span> <span data-ttu-id="796f8-285">Das **idwrite-Font** -Objekt stellt eine Schriftart in einer Schriftart Auflistung dar und macht Eigenschaften und einige grundlegende Schriftart Metriken verfügbar.</span><span class="sxs-lookup"><span data-stu-id="796f8-285">The **IDWriteFont** object represents a font in a font collection and exposes properties and a few basic font metrics.</span></span>

<span data-ttu-id="796f8-286">[**Idwrite tefontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) ist ein anderes Objekt, das eine Schriftart darstellt und einen vollständigen Satz von Metriken für eine Schriftart verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="796f8-286">The [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) is another object that represents a font and exposes a full set of metrics on a font.</span></span> <span data-ttu-id="796f8-287">Das **idwrite-fontface** -Element kann direkt über einen Schriftart Namen erstellt werden. eine Anwendung muss keine Schriftart Auflistung abrufen, um darauf zugreifen zu können.</span><span class="sxs-lookup"><span data-stu-id="796f8-287">The **IDWriteFontFace** can be created directly from a font name; an application does not have to get a font collection to access it.</span></span> <span data-ttu-id="796f8-288">Dies ist nützlich für eine Textlayoutanwendung wie z. b. Microsoft Word, die die Details für eine bestimmte Schriftart Abfragen muss.</span><span class="sxs-lookup"><span data-stu-id="796f8-288">It is useful for a text layout application such as Microsoft Word that needs to query the details for a specific font.</span></span>

<span data-ttu-id="796f8-289">Im folgenden Diagramm wird die Beziehung zwischen diesen Objekten veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="796f8-289">The following diagram illustrates the relationship between these objects.</span></span>

![Diagramm der Beziehung zwischen einer Schriftart Auflistung, einer Schriftfamilie und einer Schriftart](images/fontcollection.png)

### <a name="idwritefontface"></a><span data-ttu-id="796f8-291">Idschreitefontface</span><span class="sxs-lookup"><span data-stu-id="796f8-291">IDWriteFontFace</span></span>

<span data-ttu-id="796f8-292">Das [**idwrite-fontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) -Objekt stellt eine Schriftart dar und stellt ausführlichere Informationen über die Schriftart bereit als das [**idwrite-Font**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="796f8-292">The [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object represents a font and provides more detailed information about the font than the [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object does.</span></span> <span data-ttu-id="796f8-293">Die Schriftart-und Glyphe-Metriken aus **idschreitefontface** sind für Anwendungen nützlich, die Text Layout implementieren.</span><span class="sxs-lookup"><span data-stu-id="796f8-293">The font and glyph metrics from the **IDWriteFontFace** are useful for applications that implement text layout.</span></span>

<span data-ttu-id="796f8-294">Die meisten gängigen Anwendungen verwenden diese APIs nicht direkt, sondern verwenden stattdessen [**idwrite-Font**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) oder geben den Namen der Schriftfamilie direkt an.</span><span class="sxs-lookup"><span data-stu-id="796f8-294">Most mainstream applications will not use these APIs directly, and instead will use [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) or specify the font family name directly.</span></span>

<span data-ttu-id="796f8-295">In der folgenden Tabelle werden die Verwendungs Szenarien für die beiden-Objekte zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="796f8-295">The following table summarizes the usage scenarios for the two objects.</span></span>



| <span data-ttu-id="796f8-296">Category</span><span class="sxs-lookup"><span data-stu-id="796f8-296">Category</span></span>                                                                                                         | [<span data-ttu-id="796f8-297">**Idschreiteschriftart**</span><span class="sxs-lookup"><span data-stu-id="796f8-297">**IDWriteFont**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | [<span data-ttu-id="796f8-298">**Idschreitefontface**</span><span class="sxs-lookup"><span data-stu-id="796f8-298">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="796f8-299">APIs zur Unterstützung von Benutzerinteraktionen, z. b. eine Benutzeroberfläche zur Schriftart Auswahl: Beschreibung und andere informative APIs</span><span class="sxs-lookup"><span data-stu-id="796f8-299">APIs to support user interaction such as a font-chooser user interface: description and other informational APIs</span></span> | <span data-ttu-id="796f8-300">Ja</span><span class="sxs-lookup"><span data-stu-id="796f8-300">Yes</span></span>                                        | <span data-ttu-id="796f8-301">Nein</span><span class="sxs-lookup"><span data-stu-id="796f8-301">No</span></span>                                                 |
| <span data-ttu-id="796f8-302">APIs zur Unterstützung der Schriftart Zuordnung: Familie, Stil, Gewichtung, Streckung, Zeichen Abdeckung</span><span class="sxs-lookup"><span data-stu-id="796f8-302">APIs to support font mapping: family, style, weight, stretch, character coverage</span></span>                                 | <span data-ttu-id="796f8-303">Ja</span><span class="sxs-lookup"><span data-stu-id="796f8-303">Yes</span></span>                                        | <span data-ttu-id="796f8-304">Nein</span><span class="sxs-lookup"><span data-stu-id="796f8-304">No</span></span>                                                 |
| <span data-ttu-id="796f8-305">DrawText-API</span><span class="sxs-lookup"><span data-stu-id="796f8-305">DrawText API</span></span>                                                                                                     | <span data-ttu-id="796f8-306">Ja</span><span class="sxs-lookup"><span data-stu-id="796f8-306">Yes</span></span>                                        | <span data-ttu-id="796f8-307">Nein</span><span class="sxs-lookup"><span data-stu-id="796f8-307">No</span></span>                                                 |
| <span data-ttu-id="796f8-308">Zum Rendering verwendete APIs</span><span class="sxs-lookup"><span data-stu-id="796f8-308">APIs used for rendering</span></span>                                                                                          | <span data-ttu-id="796f8-309">Nein</span><span class="sxs-lookup"><span data-stu-id="796f8-309">No</span></span>                                         | <span data-ttu-id="796f8-310">Ja</span><span class="sxs-lookup"><span data-stu-id="796f8-310">Yes</span></span>                                                |
| <span data-ttu-id="796f8-311">APIs, die für das Text Layout verwendet werden: Glyphe Metriken usw.</span><span class="sxs-lookup"><span data-stu-id="796f8-311">APIs used for text layout: glyph metrics, and so on</span></span>                                                              | <span data-ttu-id="796f8-312">Nein</span><span class="sxs-lookup"><span data-stu-id="796f8-312">No</span></span>                                         | <span data-ttu-id="796f8-313">Ja</span><span class="sxs-lookup"><span data-stu-id="796f8-313">Yes</span></span>                                                |
| <span data-ttu-id="796f8-314">APIs für UI-Steuerelement und Text Layout: Schriftart weite Metriken</span><span class="sxs-lookup"><span data-stu-id="796f8-314">APIs for UI control and text layout: font-wide metrics</span></span>                                                           | <span data-ttu-id="796f8-315">Ja</span><span class="sxs-lookup"><span data-stu-id="796f8-315">Yes</span></span>                                        | <span data-ttu-id="796f8-316">Ja</span><span class="sxs-lookup"><span data-stu-id="796f8-316">Yes</span></span>                                                |



 

<span data-ttu-id="796f8-317">Im folgenden finden Sie eine Beispielanwendung, die die Schriftarten in der System Schriftart Auflistung auflistet.</span><span class="sxs-lookup"><span data-stu-id="796f8-317">The following is an example application that enumerates the fonts in the system font collection.</span></span>


```C++
#include <dwrite.h>
#include <string.h>
#include <stdio.h>
#include <new>

// SafeRelease inline function.
template <class T> inline void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

void wmain()
{
    IDWriteFactory* pDWriteFactory = NULL;

    HRESULT hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory)
            );

    IDWriteFontCollection* pFontCollection = NULL;

    // Get the system font collection.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
    }

    UINT32 familyCount = 0;

    // Get the number of font families in the collection.
    if (SUCCEEDED(hr))
    {
        familyCount = pFontCollection->GetFontFamilyCount();
    }

    for (UINT32 i = 0; i < familyCount; ++i)
    {
        IDWriteFontFamily* pFontFamily = NULL;

        // Get the font family.
        if (SUCCEEDED(hr))
        {
            hr = pFontCollection->GetFontFamily(i, &pFontFamily);
        }

        IDWriteLocalizedStrings* pFamilyNames = NULL;
        
        // Get a list of localized strings for the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFontFamily->GetFamilyNames(&pFamilyNames);
        }

        UINT32 index = 0;
        BOOL exists = false;
        
        wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

        if (SUCCEEDED(hr))
        {
            // Get the default locale for this user.
            int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

            // If the default locale is returned, find that locale name, otherwise use "en-us".
            if (defaultLocaleSuccess)
            {
                hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
            }
            if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
            {
                hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
            }
        }
        
        // If the specified locale doesn't exist, select the first on the list.
        if (!exists)
            index = 0;

        UINT32 length = 0;

        // Get the string length.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetStringLength(index, &length);
        }

        // Allocate a string big enough to hold the name.
        wchar_t* name = new (std::nothrow) wchar_t[length+1];
        if (name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Get the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetString(index, name, length+1);
        }
        if (SUCCEEDED(hr))
        {
            // Print out the family name.
            wprintf(L"%s\n", name);
        }

        SafeRelease(&pFontFamily);
        SafeRelease(&pFamilyNames);

        delete [] name;
    }

    SafeRelease(&pFontCollection);
    SafeRelease(&pDWriteFactory);
}

```



## <a name="text-rendering"></a><span data-ttu-id="796f8-318">Rendering von Text</span><span class="sxs-lookup"><span data-stu-id="796f8-318">Text rendering</span></span>

<span data-ttu-id="796f8-319">Die Text Rendering-APIs ermöglichen das Rendern von Symbolen in einer [DirectWrite](direct-write-portal.md) -Schriftart an eine [Direct2D](../direct2d/direct2d-portal.md) -Oberfläche oder eine unabhängige GDI-Geräte Bitmap oder die Konvertierung in-oder-Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="796f8-319">The text rendering APIs enable glyphs in a [DirectWrite](direct-write-portal.md) font to be rendered to a [Direct2D](../direct2d/direct2d-portal.md) surface or to a GDI device independent bitmap, or to be converted to outlines or bitmaps.</span></span> <span data-ttu-id="796f8-320">Das ClearType-Rendering in DirectWrite unterstützt die unter Pixel Positionierung mit verbesserter Schärfe und Kontrast im Vergleich zu vorherigen Implementierungen unter Windows.</span><span class="sxs-lookup"><span data-stu-id="796f8-320">The ClearType rendering in DirectWrite supports sub-pixel positioning with improved sharpness and contrast compared to previous implementations on Windows.</span></span> <span data-ttu-id="796f8-321">DirectWrite unterstützt auch einen schwarz-und weißem Text mit Alias, um Szenarien mit ostasiatischen Schriftarten mit eingebetteten Bitmaps zu unterstützen, oder wenn der Benutzer die Schriftart Glättung eines beliebigen Typs deaktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="796f8-321">DirectWrite also supports aliased black-and-white text to support scenarios involving East Asian fonts with embedded bitmaps, or where the user has disabled font smoothing of any type.</span></span>

<span data-ttu-id="796f8-322">Alle Optionen sind für alle verfügbaren ClearType-Knoten, auf die über die [DirectWrite](direct-write-portal.md) -APIs zugegriffen werden kann, anpassbar und werden auch über das neue System Steuerungs Applet Windows 7 ClearType-Tuner verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="796f8-322">All the options are adjustable by all the available ClearType knobs accessible through the [DirectWrite](direct-write-portal.md) APIs, and also exposed via the new Windows 7 ClearType tuner control panel applet.</span></span>

<span data-ttu-id="796f8-323">Es stehen zwei APIs für das Rendern von Symbolen zur Verfügung, von denen eine Hardware beschleunigtes Rendering über [Direct2D](../direct2d/direct2d-portal.md) und die andere das Software Rendering für eine GDI-Bitmap bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="796f8-323">There are two APIs available for rendering glyphs, one providing hardware-accelerated rendering through [Direct2D](../direct2d/direct2d-portal.md) and the other providing software rendering to a GDI bitmap.</span></span> <span data-ttu-id="796f8-324">Eine Anwendung, die [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) verwendet und den [**idwrite-TextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) -Rückruf implementiert, kann eine dieser Funktionen als Reaktion auf einen [**DrawGlyphRun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Rückruf aufrufen.</span><span class="sxs-lookup"><span data-stu-id="796f8-324">An application using [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) and implementing the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) callback can call either of these functions in response to a [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) callback.</span></span> <span data-ttu-id="796f8-325">Außerdem können Anwendungen, die ein eigenes Layout implementieren oder mit Daten auf Symbolebene umgehen, diese APIs verwenden.</span><span class="sxs-lookup"><span data-stu-id="796f8-325">Also, applications that implement their own layout or deal with glyph-level data can use these APIs.</span></span>

1.  [<span data-ttu-id="796f8-326">**ID2DRenderTarget::D rawglyphrun**</span><span class="sxs-lookup"><span data-stu-id="796f8-326">**ID2DRenderTarget::DrawGlyphRun**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

    <span data-ttu-id="796f8-327">Anwendungen können mit der [Direct2D](../direct2d/direct2d-portal.md) [**-API DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) Hardwarebeschleunigung für das Text Rendering mithilfe der GPU bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="796f8-327">Applications can use the [Direct2D](../direct2d/direct2d-portal.md) API [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) to provide hardware acceleration for text rendering using the GPU.</span></span> <span data-ttu-id="796f8-328">Die Hardware Beschleunigung wirkt sich auf alle Phasen der Textrenderingpipeline aus – von der Zusammenführung von Symbolen in Glyphe und dem Filtern der Glyphe-Run-Bitmap bis zum Anwenden des ClearType-Mischungs Algorithmus auf die endgültige angezeigte Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="796f8-328">Hardware acceleration affects all phases of the text rendering pipeline—from merging glyphs into glyph runs and filtering the glyph-run bitmap, to applying the ClearType blending algorithm to the final displayed output.</span></span> <span data-ttu-id="796f8-329">Dies ist die empfohlene API, um die beste Renderingleistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="796f8-329">This is the recommended API for getting the best rendering performance.</span></span>

2.  [<span data-ttu-id="796f8-330">**Idschreitebitmaprendertarget::D rawglyphrun**</span><span class="sxs-lookup"><span data-stu-id="796f8-330">**IDWriteBitmapRenderTarget::DrawGlyphRun**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)

    <span data-ttu-id="796f8-331">Anwendungen können die [**idschreitebitmaprendertarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) -Methode verwenden, um ein Software Rendering einer Ausführung von Symbolen in eine 32-bpp-Bitmap auszuführen.</span><span class="sxs-lookup"><span data-stu-id="796f8-331">Applications can use the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to perform a software-rendering of a run of glyphs to a 32-bpp bitmap.</span></span> <span data-ttu-id="796f8-332">Das [**idschreitebitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) -Objekt kapselt eine Bitmap und einen Speichergeräte Kontext, der zum Rendern von Glyphen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="796f8-332">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object encapsulates a bitmap and a memory device context that can be used for rendering glyphs.</span></span> <span data-ttu-id="796f8-333">Diese API ist nützlich, wenn Sie GDI beibehalten möchten, da Sie über eine vorhandene Codebasis verfügen, die in GDI gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="796f8-333">This API is useful if you want to stay with GDI because you have an existing code base that renders in GDI.</span></span>

<span data-ttu-id="796f8-334">Wenn Sie über eine Anwendung mit vorhandenem textlayoutcode verfügen, der GDI verwendet, und Sie den vorhandenen Layoutcode beibehalten möchten, aber [DirectWrite](direct-write-portal.md) nur für den letzten Schritt des Renderings von Symbolen verwenden, stellt [**idschreitegdiinterop:: anatefontfacefromhdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) die Brücke zwischen den beiden APIs bereit.</span><span class="sxs-lookup"><span data-stu-id="796f8-334">If you have an application that has existing text layout code that uses GDI, and you want to preserve its existing layout code but use [DirectWrite](direct-write-portal.md) just for the final step of rendering glyphs, [**IDWriteGdiInterop::CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) provides the bridge between the two APIs.</span></span> <span data-ttu-id="796f8-335">Vor dem Aufrufen dieser Funktion verwendet die Anwendung die **idschreitegdiinterop:: createfontfakefromhdc** -Funktion, um einen Schriftart Verweis aus einem Gerätekontext abzurufen.</span><span class="sxs-lookup"><span data-stu-id="796f8-335">Before calling this function, the application will use the **IDWriteGdiInterop::CreateFontFaceFromHdc** function to get a font-face reference from a device context.</span></span>

> [!Note]  
> <span data-ttu-id="796f8-336">In den meisten Szenarien müssen Anwendungen diese Glyphe-Rendering-APIs möglicherweise nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="796f8-336">For most scenarios, applications may not need to use these glyph-rendering APIs.</span></span> <span data-ttu-id="796f8-337">Nachdem eine Anwendung ein [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt erstellt hat, kann Sie die [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode verwenden, um den Text zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="796f8-337">After an application has created an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, it can use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method to render the text.</span></span>

 

## <a name="custom-rendering-modes"></a><span data-ttu-id="796f8-338">Benutzerdefinierte Rendermodi</span><span class="sxs-lookup"><span data-stu-id="796f8-338">Custom Rendering Modes</span></span>

<span data-ttu-id="796f8-339">Eine Reihe von Parametern wirkt sich auf das Text Rendering aus, z. b. Gamma, ClearType-Ebene, Pixelgeometrie und erweiterter Kontrast.</span><span class="sxs-lookup"><span data-stu-id="796f8-339">A number of parameters affect text rendering, such as gamma, ClearType level, pixel geometry, and enhanced contrast.</span></span> <span data-ttu-id="796f8-340">Renderingparameter werden von einem Objekt gekapselt, das die öffentliche [**idschreiterenderingparameterschnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) implementiert.</span><span class="sxs-lookup"><span data-stu-id="796f8-340">Rendering parameters are encapsulated by an object, which implements the public [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) interface.</span></span> <span data-ttu-id="796f8-341">Das renderparametern-Objekt wird automatisch basierend auf Hardware Eigenschaften und/oder Benutzereinstellungen initialisiert, die über das System Steuerungs Applet "ClearType" in Windows 7 angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="796f8-341">The rendering parameters object is automatically initialized based on hardware properties and/or user preferences specified through the ClearType control panel applet in Windows 7.</span></span> <span data-ttu-id="796f8-342">Wenn ein Client die [DirectWrite](direct-write-portal.md) -layoutapi verwendet, wählt DirectWrite im allgemeinen automatisch einen Renderingmodus aus, der dem angegebenen Mess Modus entspricht.</span><span class="sxs-lookup"><span data-stu-id="796f8-342">Generally, if a client uses the [DirectWrite](direct-write-portal.md) layout API, DirectWrite will automatically select a rendering mode that corresponds to the specified measuring mode.</span></span>

<span data-ttu-id="796f8-343">Anwendungen, die mehr Kontrolle wünschen, können " [**idwrite tefactory:: kreatecustomrenderingpara**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) " verwenden, um die verschiedenen Renderingoptionen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="796f8-343">Applications that want more control can use [**IDWriteFactory::CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) to implement the different rendering options.</span></span> <span data-ttu-id="796f8-344">Diese Funktion kann auch zum Festlegen von Gamma, Pixelgeometrie und erweiterter Kontrast verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="796f8-344">This function can also be used to set the gamma, pixel geometry, and enhanced contrast.</span></span>

<span data-ttu-id="796f8-345">Im folgenden sind die verschiedenen verfügbaren Renderingoptionen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="796f8-345">The following are the various rendering options available:</span></span>

-   <span data-ttu-id="796f8-346">Subpixel-Antialiasing</span><span class="sxs-lookup"><span data-stu-id="796f8-346">Sub-pixel anti-aliasing</span></span>

    <span data-ttu-id="796f8-347">Die Anwendung legt den *renderingmode* -Parameter auf "Natural" fest, um das \_ \_ \_ Rendering mit Antialiasing nur in der horizontalen Dimension anzugeben.</span><span class="sxs-lookup"><span data-stu-id="796f8-347">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_NATURAL to specify rendering with anti-aliasing in the horizontal dimension only.</span></span>

-   <span data-ttu-id="796f8-348">Subpixel-Antialiasing in horizontalen und vertikalen Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="796f8-348">Sub-pixel anti-aliasing in both horizontal and vertical dimensions.</span></span>

    <span data-ttu-id="796f8-349">Die Anwendung legt den *renderingmode* -Parameter auf " \_ Natural Symmetric" im dwrite-Renderingmodus fest \_ \_ \_ , um das RENDERING mit Antialiasing in horizontalen und vertikalen Dimensionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="796f8-349">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_NATURAL\_SYMMETRIC to specify rendering with anti-aliasing in both horizontal and vertical dimensions.</span></span> <span data-ttu-id="796f8-350">Dadurch werden Kurven und diagonales Linien auf Kosten einer Weichheit und in der Regel in Größen oberhalb von 16 ppem zu einem reibungsloseren Bild angezeigt.</span><span class="sxs-lookup"><span data-stu-id="796f8-350">This makes curves and diagonal lines look smoother at the expense of some softness, and is typically used at sizes above 16 ppem.</span></span>

-   <span data-ttu-id="796f8-351">Alias Text</span><span class="sxs-lookup"><span data-stu-id="796f8-351">Aliased Text</span></span>

    <span data-ttu-id="796f8-352">Die Anwendung legt den *renderingmode* -Parameter auf den dwrite- \_ Renderingmodus \_ \_ Aliasing fest, um einen Alias Text anzugeben.</span><span class="sxs-lookup"><span data-stu-id="796f8-352">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_ALIASED to specify aliased text.</span></span>

-   <span data-ttu-id="796f8-353">Graustufen Text</span><span class="sxs-lookup"><span data-stu-id="796f8-353">Grayscale Text</span></span>

    <span data-ttu-id="796f8-354">Die Anwendung legt den *Pixel Geometry* -Parameter auf dwrite \_ Pixel \_ Geometry \_ Flat fest, um Graustufen Text anzugeben.</span><span class="sxs-lookup"><span data-stu-id="796f8-354">The application sets the *pixelGeometry* parameter to DWRITE\_PIXEL\_GEOMETRY\_FLAT to specify grayscale text.</span></span>

-   <span data-ttu-id="796f8-355">GDI-kompatibel-Breite (einschließlich ostasiatischen eingebetteten Bitmap)</span><span class="sxs-lookup"><span data-stu-id="796f8-355">GDI compatible-width (including East Asian embedded bitmap)</span></span>

    <span data-ttu-id="796f8-356">Die Anwendung legt den *renderingmode* -Parameter auf den dwrite \_ -Renderingmodus \_ \_ GDI \_ Classic fest, um ein GDI-kompatibles Antialiasing anzugeben.</span><span class="sxs-lookup"><span data-stu-id="796f8-356">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_GDI\_CLASSIC to specify GDI compatible-width anti-aliasing.</span></span>

-   <span data-ttu-id="796f8-357">GDI mit natürlicher Breite</span><span class="sxs-lookup"><span data-stu-id="796f8-357">GDI natural-width</span></span>

    <span data-ttu-id="796f8-358">Die Anwendung legt den *renderingmode* -Parameter auf den dwrite- \_ Renderingmodus \_ \_ GDI \_ Natural fest, um ein GDI-kompatibles Antialiasing mit natürlicher Breite anzugeben.</span><span class="sxs-lookup"><span data-stu-id="796f8-358">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_GDI\_NATURAL to specify GDI natural-width compatible anti-aliasing.</span></span>

-   <span data-ttu-id="796f8-359">Umriss Text</span><span class="sxs-lookup"><span data-stu-id="796f8-359">Outline text</span></span>

    <span data-ttu-id="796f8-360">Zum Rendern in großem Umfang kann es vorkommen, dass ein Anwendungsentwickler das Rendering mithilfe der Schriftart Gliederung anstatt durch rasterierung in eine Bitmap ausstellt.</span><span class="sxs-lookup"><span data-stu-id="796f8-360">For rendering at large sizes, an application developer might prefer to render by using the font outline rather than by rasterizing into a bitmap.</span></span> <span data-ttu-id="796f8-361">Die Anwendung legt den *renderingmode* -Parameter auf den dwrite-renderingmodusumriss fest, um anzugeben, dass das RENDERING den Raster umgehen und die **\_ \_ \_ Kontur** direkt verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="796f8-361">The application sets the *renderingMode* parameter to **DWRITE\_RENDERING\_MODE\_OUTLINE** to specify that rendering should bypass the rasterizer and use the outlines directly.</span></span>

## <a name="gdi-interoperability"></a><span data-ttu-id="796f8-362">GDI-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="796f8-362">GDI Interoperability</span></span>

<span data-ttu-id="796f8-363">Die [**idschreitegdiinterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) -Schnittstelle bietet Interoperabilität mit GDI.</span><span class="sxs-lookup"><span data-stu-id="796f8-363">The [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) interface provides interoperability with GDI.</span></span> <span data-ttu-id="796f8-364">Dadurch können Anwendungen Ihre vorhandenen Investitionen in GDI-Codebasen fortsetzen und [DirectWrite](direct-write-portal.md) selektiv zum Rendern oder Layout verwenden.</span><span class="sxs-lookup"><span data-stu-id="796f8-364">This enables applications to continue their existing investment in GDI code bases and selectively use [DirectWrite](direct-write-portal.md) for either rendering or layout.</span></span>

<span data-ttu-id="796f8-365">Im folgenden finden Sie die APIs, mit denen eine Anwendung zum bzw. aus dem GDI-Schriftart System migriert werden kann:</span><span class="sxs-lookup"><span data-stu-id="796f8-365">The following are the APIs that enable an application to migrate to or from the GDI font system:</span></span>

-   [<span data-ttu-id="796f8-366">**"Kreatefontfromlogfont"**</span><span class="sxs-lookup"><span data-stu-id="796f8-366">**CreateFontFromLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)

    <span data-ttu-id="796f8-367">Erstellt ein [**idwrite-Font**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) -Objekt, das mit den von der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur angegebenen Eigenschaften übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="796f8-367">Creates an [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object that matches the properties specified by the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

-   [<span data-ttu-id="796f8-368">**Convertfonttologfont**</span><span class="sxs-lookup"><span data-stu-id="796f8-368">**ConvertFontToLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)

    <span data-ttu-id="796f8-369">Initialisiert eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur auf Grundlage der GDI-kompatiblen Eigenschaften der angegebenen [**idwrite-Schriftart**](/windows/win32/api/dwrite/nn-dwrite-idwritefont).</span><span class="sxs-lookup"><span data-stu-id="796f8-369">Initializes a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure based on the GDI-compatible properties of the specified [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont).</span></span>

-   [<span data-ttu-id="796f8-370">**Convertfontfaketologfont**</span><span class="sxs-lookup"><span data-stu-id="796f8-370">**ConvertFontFaceToLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)

    <span data-ttu-id="796f8-371">Initialisiert eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur auf Grundlage der GDI-kompatiblen Eigenschaften des angegebenen [**idwrite-fontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface).</span><span class="sxs-lookup"><span data-stu-id="796f8-371">Initializes a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure based on the GDI-compatible properties of the specified [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface).</span></span>

-   [<span data-ttu-id="796f8-372">**"Kreatefontfakefromhdc"**</span><span class="sxs-lookup"><span data-stu-id="796f8-372">**CreateFontFaceFromHdc**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)

    <span data-ttu-id="796f8-373">Erstellt ein [**idwrite-fontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) -Objekt, das dem aktuell ausgewählten **hFont** entspricht.</span><span class="sxs-lookup"><span data-stu-id="796f8-373">Creates an [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object that corresponds to the currently selected **HFONT**.</span></span>

## <a name="conclusion"></a><span data-ttu-id="796f8-374">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="796f8-374">Conclusion</span></span>

<span data-ttu-id="796f8-375">Das verbessern der Lesevorgänge ist für Benutzer ein großartiger Wert, egal ob es sich um einen Bildschirm oder ein Papier handelt.</span><span class="sxs-lookup"><span data-stu-id="796f8-375">Improving the reading experience is of great value to users whether it is on the screen or on paper.</span></span> <span data-ttu-id="796f8-376">[DirectWrite](direct-write-portal.md) bietet die einfache Verwendung und das geschichtete Programmiermodell für Anwendungsentwickler, um die Textdarstellung für Ihre Windows-Anwendungen zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="796f8-376">[DirectWrite](direct-write-portal.md) provides the ease of use and the layered programming model for application developers to improve the text experience for their Windows applications.</span></span> <span data-ttu-id="796f8-377">Anwendungen können mithilfe von DirectWrite umfangreicher formatierten Text für Ihre Benutzeroberfläche und Dokumente mit der Layout-API Rendering.</span><span class="sxs-lookup"><span data-stu-id="796f8-377">Applications can use DirectWrite to render richly formatted text for their UI and documents with the layout API.</span></span> <span data-ttu-id="796f8-378">Für komplexere Szenarien kann eine Anwendung direkt mit Symbolen, Zugriffs Schriftarten usw. arbeiten und die Leistungsfähigkeit von DirectWrite nutzen, um qualitativ hochwertige typografiken bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="796f8-378">For more complex scenarios, an application can work directly with glyphs, access fonts, and so on, and harness the power of DirectWrite to deliver high-quality typography.</span></span>

<span data-ttu-id="796f8-379">Mit den Interoperabilitäts Funktionen von [DirectWrite](direct-write-portal.md) können Anwendungsentwickler ihre vorhandenen Win32-Codebasen weiterleiten und DirectWrite selektiv innerhalb Ihrer Anwendungen übernehmen.</span><span class="sxs-lookup"><span data-stu-id="796f8-379">The interoperability capabilities of [DirectWrite](direct-write-portal.md) enable application developers to carry forward their existing Win32 codebases and adopt DirectWrite selectively within their applications.</span></span>

 

 