---
title: Sicherheitsaspekte Microsoft Windows-Steuerelemente
description: Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit den Windows-Steuerelementen.
ms.assetid: d5396fa1-452e-40e1-beaf-ae04690048f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29ba986ddd1db980134f428c8abf152321617ef
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104102499"
---
# <a name="security-considerations-microsoft-windows-controls"></a><span data-ttu-id="f0c9a-103">Überlegungen zur Sicherheit: Microsoft Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="f0c9a-103">Security Considerations: Microsoft Windows Controls</span></span>

<span data-ttu-id="f0c9a-104">Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit den Windows-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-104">This topic provides information about security considerations related to the Windows controls.</span></span> <span data-ttu-id="f0c9a-105">Die Informationen in diesem Thema enthalten nicht alles, was Sie über Sicherheitsprobleme wissen müssen – Sie können es als Ausgangspunkt und Referenz für diesen Technologiebereich verwenden.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-105">The information in this topic does not provide all you need to know about security issues—use it as a starting point and reference for this technology area.</span></span>

<span data-ttu-id="f0c9a-106">Die Konnektivität zwischen Computern ist üblich. der Hauptanliegen eines Entwicklers ist die Anwendungssicherheit.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-106">Interconnectivity among computers is common; a developer's chief concern must be application security.</span></span> <span data-ttu-id="f0c9a-107">In den folgenden Abschnitten werden einige mögliche Sicherheitsprobleme erläutert, die beim Programmieren von Windows-Steuerelementen berücksichtigt werden</span><span class="sxs-lookup"><span data-stu-id="f0c9a-107">The following sections discuss some potential security issues to consider when programming Windows controls.</span></span>

-   [<span data-ttu-id="f0c9a-108">Mit NULL beendete Steuerungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="f0c9a-108">Null-terminated Control Messages</span></span>](#null-terminated-control-messages)
-   [<span data-ttu-id="f0c9a-109">Zeichen folgen Verwendung</span><span class="sxs-lookup"><span data-stu-id="f0c9a-109">String Use</span></span>](#string-use)
-   [<span data-ttu-id="f0c9a-110">Eingabevalidierung</span><span class="sxs-lookup"><span data-stu-id="f0c9a-110">Input Validation</span></span>](#input-validation)
-   [<span data-ttu-id="f0c9a-111">Kenn Wort Verwendung</span><span class="sxs-lookup"><span data-stu-id="f0c9a-111">Password Use</span></span>](#password-use)
-   [<span data-ttu-id="f0c9a-112">Sicherheitswarnungen</span><span class="sxs-lookup"><span data-stu-id="f0c9a-112">Security Alerts</span></span>](#security-alerts)
-   [<span data-ttu-id="f0c9a-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0c9a-113">Related topics</span></span>](#related-topics)

## <a name="null-terminated-control-messages"></a><span data-ttu-id="f0c9a-114">Mit NULL beendete Steuerungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="f0c9a-114">Null-terminated Control Messages</span></span>

<span data-ttu-id="f0c9a-115">Viele der Steuerungs Meldungen und Makros verfügen über Zeichen folgen Parameter.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-115">Many of the control messages and macros have string parameters.</span></span> <span data-ttu-id="f0c9a-116">Diese Nachrichten überprüfen häufig nicht die Eingabe Zeichenfolgen, insbesondere nicht, um eine abschließende zu überprüfen `'\0'` .</span><span class="sxs-lookup"><span data-stu-id="f0c9a-116">Often these messages do not validate the input strings, in particular, they do not check for a terminating `'\0'`.</span></span> <span data-ttu-id="f0c9a-117">Wenn Sie eine Nachricht aufrufen, die eine Zeichenfolge als Parameter verwendet, geben Sie explizit an, dass die Zeichenfolge NULL-terminiert ist.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-117">When you call a message that uses a string as a parameter, explicitly specify that the string is null-terminated.</span></span>

## <a name="string-use"></a><span data-ttu-id="f0c9a-118">Zeichen folgen Verwendung</span><span class="sxs-lookup"><span data-stu-id="f0c9a-118">String Use</span></span>

<span data-ttu-id="f0c9a-119">Beim Programmieren von Windows-Steuerelementen ist es erforderlich, Zeichen folgen zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-119">When you program Windows controls, it is necessary to manipulate strings.</span></span> <span data-ttu-id="f0c9a-120">Fast jedes Steuerelement erfordert, dass Text eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-120">Almost every control requires text to be inserted.</span></span> <span data-ttu-id="f0c9a-121">Um z. b. ein Listenfeld aufzufüllen, müssen Sie Zeichen folgen in das-Steuerelement laden.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-121">For example, to populate a list box you must load strings into the control.</span></span> <span data-ttu-id="f0c9a-122">Da die Verwendung von Zeichen folgen fälschlicherweise zu Pufferüberläufen führt, sollten Sie Vorkehrungen treffen, um dieses Sicherheitsrisiko zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-122">Because using strings incorrectly often causes buffer overruns, take precautions to avoid this security risk.</span></span>

<span data-ttu-id="f0c9a-123">Weitere Informationen zu Pufferüberläufen finden Sie unter *Schreiben von sicherem Code* von Michael Howard und David LeBlanc, Microsoft Press, 2002 und [bewährten Methoden für die Sicherheits-APIs](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span><span class="sxs-lookup"><span data-stu-id="f0c9a-123">For more information about buffer overruns, see *Writing Secure Code* by Michael Howard and David LeBlanc, Microsoft Press, 2002 and [Best Practices for the Security APIs](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span></span>

## <a name="input-validation"></a><span data-ttu-id="f0c9a-124">Eingabeüberprüfung</span><span class="sxs-lookup"><span data-stu-id="f0c9a-124">Input Validation</span></span>

<span data-ttu-id="f0c9a-125">Die folgenden Steuerungs Meldungen können Sicherheitsprobleme darstellen.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-125">The following control messages can present security problems.</span></span>

-   [<span data-ttu-id="f0c9a-126">**CB \_ getlbtext**</span><span class="sxs-lookup"><span data-stu-id="f0c9a-126">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
-   [<span data-ttu-id="f0c9a-127">**LVM \_ getisearchstring**</span><span class="sxs-lookup"><span data-stu-id="f0c9a-127">**LVM\_GETISEARCHSTRING**</span></span>](lvm-getisearchstring.md)
-   [<span data-ttu-id="f0c9a-128">**SB \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="f0c9a-128">**SB\_GETTEXT**</span></span>](sb-gettext.md)
-   [<span data-ttu-id="f0c9a-129">**SB \_ GetTipText**</span><span class="sxs-lookup"><span data-stu-id="f0c9a-129">**SB\_GETTIPTEXT**</span></span>](sb-gettiptext.md)
-   [<span data-ttu-id="f0c9a-130">**TB \_ getbuttontext**</span><span class="sxs-lookup"><span data-stu-id="f0c9a-130">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
-   [<span data-ttu-id="f0c9a-131">**TTM \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="f0c9a-131">**TTM\_GETTEXT**</span></span>](ttm-gettext.md)
-   [<span data-ttu-id="f0c9a-132">**TVM \_ getisearchstring**</span><span class="sxs-lookup"><span data-stu-id="f0c9a-132">**TVM\_GETISEARCHSTRING**</span></span>](tvm-getisearchstring.md)

<span data-ttu-id="f0c9a-133">Wenn der Text zwischen dem Aufruf zum Abrufen der Textlänge und dem Zeitpunkt, zu dem der Text angezeigt oder verwendet wird, geändert wird, kann ein Pufferüberlauf auftreten.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-133">If the text changes between the call to get the text length and the time the text is displayed or used, a buffer overrun can occur.</span></span> <span data-ttu-id="f0c9a-134">Um dies zu vermeiden, müssen Sie die Zeichenfolge validieren, bevor Sie Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-134">To avoid this, you must validate the string before using it.</span></span> <span data-ttu-id="f0c9a-135">Außerdem verfügen die Nachrichten, die Text, [**CB \_ getlbtext**](cb-getlbtext.md), [**TB \_ getbuttontext**](tb-getbuttontext.md)und [**TTM \_ gettext**](ttm-gettext.md)abrufen, nicht über einen Parameter für die Puffergröße, der das Potenzial für einen Pufferüberlauf darstellt.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-135">In addition, the messages that retrieve text, [**CB\_GETLBTEXT**](cb-getlbtext.md), [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md), and [**TTM\_GETTEXT**](ttm-gettext.md), have no buffer size parameter that presents the potential for a buffer overrun.</span></span>

<span data-ttu-id="f0c9a-136">Wenn Sie [**CB \_ getlbtext**](cb-getlbtext.md) oder [**SB \_ gettext**](sb-gettext.md)verwenden, sollten Sie zuerst [**CB \_ getlbtextlen**](cb-getlbtextlen.md) oder [**SB \_ getTextLength**](sb-gettextlength.md) aufrufen, um die Puffergröße zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-136">When you use [**CB\_GETLBTEXT**](cb-getlbtext.md) or [**SB\_GETTEXT**](sb-gettext.md), you should first call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) or [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to obtain the buffer size.</span></span> <span data-ttu-id="f0c9a-137">Einige dieser Nachrichten, [**TB \_ getbuttontext**](tb-getbuttontext.md), [**LVM \_ getisearchstring**](lvm-getisearchstring.md)und [**TVM \_ getisearchstring**](tvm-getisearchstring.md)können mit einem **null** -Parameterwert aufgerufen werden, um die Länge der Zeichenfolge zu erhalten, bevor die Nachricht zum Abrufen der Zeichenfolge aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-137">Some of these messages, [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md), [**LVM\_GETISEARCHSTRING**](lvm-getisearchstring.md), and [**TVM\_GETISEARCHSTRING**](tvm-getisearchstring.md), can be called with a **NULL** parameter value to obtain the length of the string before invoking the message to retrieve the string.</span></span>

<span data-ttu-id="f0c9a-138">Eine Meldung, auf die Sie besonders achten sollten, ist die Statusleiste [**SB \_ GetTipText**](sb-gettiptext.md) Message.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-138">A message that you should pay particular attention to is the status bar [**SB\_GETTIPTEXT**](sb-gettiptext.md) message.</span></span> <span data-ttu-id="f0c9a-139">Diese Meldung bietet keine Möglichkeit, die Länge der abzurufenden Zeichenfolge abzufragen.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-139">This message provides no way to query the length of the string that is to be retrieved.</span></span>

## <a name="password-use"></a><span data-ttu-id="f0c9a-140">Kenn Wort Verwendung</span><span class="sxs-lookup"><span data-stu-id="f0c9a-140">Password Use</span></span>

<span data-ttu-id="f0c9a-141">Wenn Sie Kenn Wort geschütztes Bearbeitungs Steuerelemente ([**es \_**](edit-control-styles.md) -Kenn Wort Format) verwenden, muss der Puffer, der den abgerufenen Text enthält, so bald wie möglich auf NULL festgelegt werden, um zu vermeiden, dass das Kennwort des Benutzers im Speicher verfügbar gemacht</span><span class="sxs-lookup"><span data-stu-id="f0c9a-141">If you use password-protected edit controls ([**ES\_PASSWORD**](edit-control-styles.md) style), the buffer that contains the retrieved text must be set to zero as soon as possible to avoid exposing the user's password in memory.</span></span>

## <a name="security-alerts"></a><span data-ttu-id="f0c9a-142">Sicherheitswarnungen</span><span class="sxs-lookup"><span data-stu-id="f0c9a-142">Security Alerts</span></span>

<span data-ttu-id="f0c9a-143">In der folgenden Tabelle sind die Funktionen aufgelistet, die bei falscher Verwendung die Sicherheit Ihrer Anwendungen beeinträchtigen können.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-143">The following table lists features that, if used incorrectly, can compromise the security of your applications.</span></span> <span data-ttu-id="f0c9a-144">Die hier aufgeführten Meldungen stellen keinen Parameter bereit, der die Puffergröße angibt.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-144">The messages listed here do not provide a parameter that specifies the buffer size.</span></span>



| <span data-ttu-id="f0c9a-145">Funktion</span><span class="sxs-lookup"><span data-stu-id="f0c9a-145">Feature</span></span>                                               | <span data-ttu-id="f0c9a-146">Minderung</span><span class="sxs-lookup"><span data-stu-id="f0c9a-146">Mitigation</span></span>                                                                                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0c9a-147">**Dlgdirlistcombobox**</span><span class="sxs-lookup"><span data-stu-id="f0c9a-147">**DlgDirListComboBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)      | <span data-ttu-id="f0c9a-148">Stellen Sie sicher, dass der von der Funktion verwendete Puffer in geschrieben werden kann und auf NULL endet.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-148">Make sure the buffer used by the function can be written to and is null-terminated.</span></span>                                                                     |
| [<span data-ttu-id="f0c9a-149">**CB \_ getlbtext**</span><span class="sxs-lookup"><span data-stu-id="f0c9a-149">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)                 | <span data-ttu-id="f0c9a-150">Rufen Sie [**CB \_ getlbtextlen**](cb-getlbtextlen.md) auf, um die Puffergröße zu erhalten, und rufen Sie dann [**CB \_ getlbtext**](cb-getlbtext.md) auf, um die Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-150">Call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) to obtain the buffer size, and then call [**CB\_GETLBTEXT**](cb-getlbtext.md) to retrieve the string.</span></span> |
| [<span data-ttu-id="f0c9a-151">**LVM \_ getisearchstring**</span><span class="sxs-lookup"><span data-stu-id="f0c9a-151">**LVM\_GETISEARCHSTRING**</span></span>](lvm-getisearchstring.md) | <span data-ttu-id="f0c9a-152">Rufen Sie die Nachricht mit einem **null** -Parameterwert auf, um die Puffergröße zu erhalten, und rufen Sie dann die Nachricht ein zweites Mal auf, um die Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-152">Call the message with a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>             |
| [<span data-ttu-id="f0c9a-153">**SB \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="f0c9a-153">**SB\_GETTEXT**</span></span>](sb-gettext.md)                     | <span data-ttu-id="f0c9a-154">Rufen Sie [**SB \_ getTextLength**](sb-gettextlength.md) auf, um die Puffergröße zu erhalten, und rufen Sie dann [**SB \_ gettext**](sb-gettext.md) auf, um die Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-154">Call [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to obtain the buffer size, and then call [**SB\_GETTEXT**](sb-gettext.md) to retrieve the string.</span></span>   |
| [<span data-ttu-id="f0c9a-155">**TB \_ getbuttontext**</span><span class="sxs-lookup"><span data-stu-id="f0c9a-155">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)         | <span data-ttu-id="f0c9a-156">Rufen Sie die Nachricht mit einem **null** -Parameterwert auf, um die Puffergröße zu erhalten, und rufen Sie dann die Nachricht ein zweites Mal auf, um die Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-156">Call the message with a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>             |
| [<span data-ttu-id="f0c9a-157">**TTM \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="f0c9a-157">**TTM\_GETTEXT**</span></span>](ttm-gettext.md)                   | <span data-ttu-id="f0c9a-158">Diese Meldung bietet keine Möglichkeit, die Größe des Puffers zu erkennen oder anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-158">This message does not provide a way for you to know or specify the size of the buffer.</span></span>                                                                  |
| [<span data-ttu-id="f0c9a-159">**TVM \_ getisearchstring**</span><span class="sxs-lookup"><span data-stu-id="f0c9a-159">**TVM\_GETISEARCHSTRING**</span></span>](tvm-getisearchstring.md) | <span data-ttu-id="f0c9a-160">Rufen Sie die Meldung auf, indem Sie einen **null** -Parameterwert übergeben, um die Puffergröße zu erhalten, und dann die Nachricht ein zweites Mal aufrufen, um die Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-160">Call the message by passing a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="f0c9a-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0c9a-161">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f0c9a-162">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="f0c9a-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f0c9a-163">Microsoft Security</span><span class="sxs-lookup"><span data-stu-id="f0c9a-163">Microsoft Security</span></span>](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[<span data-ttu-id="f0c9a-164">Security</span><span class="sxs-lookup"><span data-stu-id="f0c9a-164">Security</span></span>](/windows/desktop/security)
</dt> <dt>

[<span data-ttu-id="f0c9a-165">TechNet-Sicherheitsressourcen</span><span class="sxs-lookup"><span data-stu-id="f0c9a-165">TechNet Security Resources</span></span>](https://www.microsoft.com/technet/security/Bulletin/MS10-059.mspx)
</dt> <dt>

[<span data-ttu-id="f0c9a-166">Bewährte Methoden für die Sicherheits-APIs</span><span class="sxs-lookup"><span data-stu-id="f0c9a-166">Best Practices for the Security APIs</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> </dl>

 

 