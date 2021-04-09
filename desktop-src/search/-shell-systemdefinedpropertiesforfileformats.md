---
description: Microsoft Windows bietet eine Reihe von Systemeigenschaften, die Sie für Ihre Dateiformate verwenden können.
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: System-Defined Eigenschaften für benutzerdefinierte Dateiformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1a3645e383ea751298f766eacf60f5ac95ece3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128517"
---
# <a name="system-defined-properties-for-custom-file-formats"></a><span data-ttu-id="df471-103">System-Defined Eigenschaften für benutzerdefinierte Dateiformate</span><span class="sxs-lookup"><span data-stu-id="df471-103">System-Defined Properties for Custom File Formats</span></span>

<span data-ttu-id="df471-104">Microsoft Windows bietet eine Reihe von Systemeigenschaften, die Sie für Ihre Dateiformate verwenden können.</span><span class="sxs-lookup"><span data-stu-id="df471-104">Microsoft Windows supplies a number of system properties that you can use for your file formats.</span></span> <span data-ttu-id="df471-105">Wenn Sie ein benutzerdefiniertes Dateiformat erstellen, sollten Sie beliebig viele System definierte Eigenschaften unterstützen.</span><span class="sxs-lookup"><span data-stu-id="df471-105">If you are creating a custom file format, you should support as many system-defined properties as you can.</span></span> <span data-ttu-id="df471-106">Vor dem Erstellen eines benutzerdefinierten Eigenschaften Handler sollten Sie die vom System bereitgestellten Handler überprüfen, um festzustellen, ob Sie einen verwenden können, anstatt einen eigenen zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="df471-106">Before creating a custom property handler, you should review the system-supplied handlers to see if you can use one instead of writing your own.</span></span>

<span data-ttu-id="df471-107">In der folgenden Tabelle werden die Dateiformate kategorisiert und anschließend die wichtigsten Systemeigenschaften aufgelistet, die ihr Dateiformat unterstützen sollte.</span><span class="sxs-lookup"><span data-stu-id="df471-107">The following table categorizes file formats and then lists the most important system properties your file format should support.</span></span> <span data-ttu-id="df471-108">Um eine gute Benutzer Leistung zu gewährleisten, sollten Sie alle Eigenschaften der Priorität 1 und 2 für die Kategorie des Datei Formats unterstützen.</span><span class="sxs-lookup"><span data-stu-id="df471-108">To provide a good user experience, you should support all priority 1 and 2 properties for your category of file format.</span></span>

-   [<span data-ttu-id="df471-109">Kommunikation</span><span class="sxs-lookup"><span data-stu-id="df471-109">Communications</span></span>](#communications)
-   [<span data-ttu-id="df471-110">Kontakte</span><span class="sxs-lookup"><span data-stu-id="df471-110">Contacts</span></span>](#contacts)
-   [<span data-ttu-id="df471-111">Dokumente</span><span class="sxs-lookup"><span data-stu-id="df471-111">Documents</span></span>](#documents)
-   [<span data-ttu-id="df471-112">Allgemein</span><span class="sxs-lookup"><span data-stu-id="df471-112">Generic</span></span>](#generic)
-   [<span data-ttu-id="df471-113">Musizieren</span><span class="sxs-lookup"><span data-stu-id="df471-113">Music</span></span>](#music)
-   [<span data-ttu-id="df471-114">Bilder</span><span class="sxs-lookup"><span data-stu-id="df471-114">Pictures</span></span>](#pictures)
-   [<span data-ttu-id="df471-115">Videos</span><span class="sxs-lookup"><span data-stu-id="df471-115">Videos</span></span>](#videos)
-   [<span data-ttu-id="df471-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df471-116">Related topics</span></span>](#related-topics)

## <a name="communications"></a><span data-ttu-id="df471-117">Kommunikation</span><span class="sxs-lookup"><span data-stu-id="df471-117">Communications</span></span>



| <span data-ttu-id="df471-118">Name</span><span class="sxs-lookup"><span data-stu-id="df471-118">Name</span></span>            | <span data-ttu-id="df471-119">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="df471-119">Property</span></span>                               | <span data-ttu-id="df471-120">Priorität</span><span class="sxs-lookup"><span data-stu-id="df471-120">Priority</span></span> |
|-----------------|----------------------------------------|----------|
| <span data-ttu-id="df471-121">Empfangenes Datum</span><span class="sxs-lookup"><span data-stu-id="df471-121">Date received</span></span>   | <span data-ttu-id="df471-122">System. Message. DateReceived</span><span class="sxs-lookup"><span data-stu-id="df471-122">System.Message.DateReceived</span></span>            | <span data-ttu-id="df471-123">1</span><span class="sxs-lookup"><span data-stu-id="df471-123">1</span></span>        |
| <span data-ttu-id="df471-124">Aus Namen</span><span class="sxs-lookup"><span data-stu-id="df471-124">From names</span></span>      | <span data-ttu-id="df471-125">System. Message. FromName</span><span class="sxs-lookup"><span data-stu-id="df471-125">System.Message.FromName</span></span>                | <span data-ttu-id="df471-126">1</span><span class="sxs-lookup"><span data-stu-id="df471-126">1</span></span>        |
| <span data-ttu-id="df471-127">Hat Anlagen</span><span class="sxs-lookup"><span data-stu-id="df471-127">Has attachments</span></span> | <span data-ttu-id="df471-128">System. Message. hasattachments</span><span class="sxs-lookup"><span data-stu-id="df471-128">System.Message.HasAttachments</span></span>          | <span data-ttu-id="df471-129">1</span><span class="sxs-lookup"><span data-stu-id="df471-129">1</span></span>        |
| <span data-ttu-id="df471-130">Mailbox</span><span class="sxs-lookup"><span data-stu-id="df471-130">Mailbox</span></span>         | <span data-ttu-id="df471-131">System. Communication. storeddisplayname</span><span class="sxs-lookup"><span data-stu-id="df471-131">System.Communication.storeddisplayname</span></span> | <span data-ttu-id="df471-132">1</span><span class="sxs-lookup"><span data-stu-id="df471-132">1</span></span>        |
| <span data-ttu-id="df471-133">Name</span><span class="sxs-lookup"><span data-stu-id="df471-133">Name</span></span>            | <span data-ttu-id="df471-134">System. filename</span><span class="sxs-lookup"><span data-stu-id="df471-134">System.FileName</span></span>                        | <span data-ttu-id="df471-135">1</span><span class="sxs-lookup"><span data-stu-id="df471-135">1</span></span>        |
| <span data-ttu-id="df471-136">Subject</span><span class="sxs-lookup"><span data-stu-id="df471-136">Subject</span></span>         | <span data-ttu-id="df471-137">System. Subject</span><span class="sxs-lookup"><span data-stu-id="df471-137">System.Subject</span></span>                         | <span data-ttu-id="df471-138">1</span><span class="sxs-lookup"><span data-stu-id="df471-138">1</span></span>        |
| <span data-ttu-id="df471-139">In Namen</span><span class="sxs-lookup"><span data-stu-id="df471-139">To names</span></span>        | <span data-ttu-id="df471-140">System. Message. ToName</span><span class="sxs-lookup"><span data-stu-id="df471-140">System.Message.ToName</span></span>                  | <span data-ttu-id="df471-141">1</span><span class="sxs-lookup"><span data-stu-id="df471-141">1</span></span>        |
| <span data-ttu-id="df471-142">Category</span><span class="sxs-lookup"><span data-stu-id="df471-142">Category</span></span>        | <span data-ttu-id="df471-143">System. Category</span><span class="sxs-lookup"><span data-stu-id="df471-143">System.Category</span></span>                        | <span data-ttu-id="df471-144">2</span><span class="sxs-lookup"><span data-stu-id="df471-144">2</span></span>        |
| <span data-ttu-id="df471-145">type</span><span class="sxs-lookup"><span data-stu-id="df471-145">Type</span></span>            | <span data-ttu-id="df471-146">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="df471-146">System.PerceivedType</span></span>                   | <span data-ttu-id="df471-147">2</span><span class="sxs-lookup"><span data-stu-id="df471-147">2</span></span>        |



 

## <a name="contacts"></a><span data-ttu-id="df471-148">Kontakte</span><span class="sxs-lookup"><span data-stu-id="df471-148">Contacts</span></span>



| <span data-ttu-id="df471-149">Name</span><span class="sxs-lookup"><span data-stu-id="df471-149">Name</span></span>             | <span data-ttu-id="df471-150">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="df471-150">Property</span></span>                           | <span data-ttu-id="df471-151">Priorität</span><span class="sxs-lookup"><span data-stu-id="df471-151">Priority</span></span> |
|------------------|------------------------------------|----------|
| <span data-ttu-id="df471-152">Kontoname</span><span class="sxs-lookup"><span data-stu-id="df471-152">Account Name</span></span>     | <span data-ttu-id="df471-153">System. Communication. Accountname</span><span class="sxs-lookup"><span data-stu-id="df471-153">System.Communication.AccountName</span></span>   | <span data-ttu-id="df471-154">1</span><span class="sxs-lookup"><span data-stu-id="df471-154">1</span></span>        |
| <span data-ttu-id="df471-155">Telefon (geschäftlich)</span><span class="sxs-lookup"><span data-stu-id="df471-155">Business Phone</span></span>   | <span data-ttu-id="df471-156">System. Contact. businesstelephone</span><span class="sxs-lookup"><span data-stu-id="df471-156">System.Contact.BusinessTelephone</span></span>   | <span data-ttu-id="df471-157">1</span><span class="sxs-lookup"><span data-stu-id="df471-157">1</span></span>        |
| <span data-ttu-id="df471-158">Company</span><span class="sxs-lookup"><span data-stu-id="df471-158">Company</span></span>          | <span data-ttu-id="df471-159">System. Company</span><span class="sxs-lookup"><span data-stu-id="df471-159">System.Company</span></span>                     | <span data-ttu-id="df471-160">1</span><span class="sxs-lookup"><span data-stu-id="df471-160">1</span></span>        |
| <span data-ttu-id="df471-161">E-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="df471-161">Email Address</span></span>    | <span data-ttu-id="df471-162">System. Contact. primaryemailaddress</span><span class="sxs-lookup"><span data-stu-id="df471-162">System.Contact.PrimaryEmailAddress</span></span> | <span data-ttu-id="df471-163">1</span><span class="sxs-lookup"><span data-stu-id="df471-163">1</span></span>        |
| <span data-ttu-id="df471-164">Wichtigkeit</span><span class="sxs-lookup"><span data-stu-id="df471-164">Importance</span></span>       | <span data-ttu-id="df471-165">System. importancetext</span><span class="sxs-lookup"><span data-stu-id="df471-165">System.ImportanceText</span></span>              | <span data-ttu-id="df471-166">1</span><span class="sxs-lookup"><span data-stu-id="df471-166">1</span></span>        |
| <span data-ttu-id="df471-167">Mobiltelefon</span><span class="sxs-lookup"><span data-stu-id="df471-167">Mobile Phone</span></span>     | <span data-ttu-id="df471-168">System. Contact. Mobiletelefon</span><span class="sxs-lookup"><span data-stu-id="df471-168">System.Contact.MobileTelephone</span></span>     | <span data-ttu-id="df471-169">1</span><span class="sxs-lookup"><span data-stu-id="df471-169">1</span></span>        |
| <span data-ttu-id="df471-170">Geschäftliche Adresse</span><span class="sxs-lookup"><span data-stu-id="df471-170">Business address</span></span> | <span data-ttu-id="df471-171">System. Contact. BusinessAddress</span><span class="sxs-lookup"><span data-stu-id="df471-171">System.Contact.BusinessAddress</span></span>     | <span data-ttu-id="df471-172">2</span><span class="sxs-lookup"><span data-stu-id="df471-172">2</span></span>        |
| <span data-ttu-id="df471-173">Geschäftfax</span><span class="sxs-lookup"><span data-stu-id="df471-173">Business fax</span></span>     | <span data-ttu-id="df471-174">System. Contact. businessfaxnummer</span><span class="sxs-lookup"><span data-stu-id="df471-174">System.Contact.BusinessFaxNumber</span></span>   | <span data-ttu-id="df471-175">2</span><span class="sxs-lookup"><span data-stu-id="df471-175">2</span></span>        |
| <span data-ttu-id="df471-176">Category</span><span class="sxs-lookup"><span data-stu-id="df471-176">Category</span></span>         | <span data-ttu-id="df471-177">System. Category</span><span class="sxs-lookup"><span data-stu-id="df471-177">System.Category</span></span>                    | <span data-ttu-id="df471-178">2</span><span class="sxs-lookup"><span data-stu-id="df471-178">2</span></span>        |
| <span data-ttu-id="df471-179">Privatadresse</span><span class="sxs-lookup"><span data-stu-id="df471-179">Home address</span></span>     | <span data-ttu-id="df471-180">System. Contact. HomeAddress</span><span class="sxs-lookup"><span data-stu-id="df471-180">System.Contact.HomeAddress</span></span>         | <span data-ttu-id="df471-181">2</span><span class="sxs-lookup"><span data-stu-id="df471-181">2</span></span>        |
| <span data-ttu-id="df471-182">Telefon (privat)</span><span class="sxs-lookup"><span data-stu-id="df471-182">Home phone</span></span>       | <span data-ttu-id="df471-183">System. Contact. homeTelephone</span><span class="sxs-lookup"><span data-stu-id="df471-183">System.Contact.HomeTelephone</span></span>       | <span data-ttu-id="df471-184">2</span><span class="sxs-lookup"><span data-stu-id="df471-184">2</span></span>        |
| <span data-ttu-id="df471-185">Titel</span><span class="sxs-lookup"><span data-stu-id="df471-185">Title</span></span>            | <span data-ttu-id="df471-186">System.Title</span><span class="sxs-lookup"><span data-stu-id="df471-186">System.Title</span></span>                       | <span data-ttu-id="df471-187">2</span><span class="sxs-lookup"><span data-stu-id="df471-187">2</span></span>        |



 

## <a name="documents"></a><span data-ttu-id="df471-188">Dokumente</span><span class="sxs-lookup"><span data-stu-id="df471-188">Documents</span></span>



| <span data-ttu-id="df471-189">Name</span><span class="sxs-lookup"><span data-stu-id="df471-189">Name</span></span>      | <span data-ttu-id="df471-190">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="df471-190">Property</span></span>             | <span data-ttu-id="df471-191">Priorität</span><span class="sxs-lookup"><span data-stu-id="df471-191">Priority</span></span> |
|-----------|----------------------|----------|
| <span data-ttu-id="df471-192">Authors</span><span class="sxs-lookup"><span data-stu-id="df471-192">Authors</span></span>   | <span data-ttu-id="df471-193">System.Author</span><span class="sxs-lookup"><span data-stu-id="df471-193">System.Author</span></span>        | <span data-ttu-id="df471-194">1</span><span class="sxs-lookup"><span data-stu-id="df471-194">1</span></span>        |
| <span data-ttu-id="df471-195">Volltext</span><span class="sxs-lookup"><span data-stu-id="df471-195">Full Text</span></span> | <span data-ttu-id="df471-196">System. Fulltext</span><span class="sxs-lookup"><span data-stu-id="df471-196">System.FullText</span></span>      | <span data-ttu-id="df471-197">1</span><span class="sxs-lookup"><span data-stu-id="df471-197">1</span></span>        |
| <span data-ttu-id="df471-198">`Tags`</span><span class="sxs-lookup"><span data-stu-id="df471-198">Tags</span></span>      | <span data-ttu-id="df471-199">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="df471-199">System.Keywords</span></span>      | <span data-ttu-id="df471-200">1</span><span class="sxs-lookup"><span data-stu-id="df471-200">1</span></span>        |
| <span data-ttu-id="df471-201">type</span><span class="sxs-lookup"><span data-stu-id="df471-201">Type</span></span>      | <span data-ttu-id="df471-202">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="df471-202">System.PerceivedType</span></span> | <span data-ttu-id="df471-203">1</span><span class="sxs-lookup"><span data-stu-id="df471-203">1</span></span>        |
| <span data-ttu-id="df471-204">Category</span><span class="sxs-lookup"><span data-stu-id="df471-204">Category</span></span>  | <span data-ttu-id="df471-205">System. Category</span><span class="sxs-lookup"><span data-stu-id="df471-205">System.Category</span></span>      | <span data-ttu-id="df471-206">2</span><span class="sxs-lookup"><span data-stu-id="df471-206">2</span></span>        |
| <span data-ttu-id="df471-207">Titel</span><span class="sxs-lookup"><span data-stu-id="df471-207">Title</span></span>     | <span data-ttu-id="df471-208">System.Title</span><span class="sxs-lookup"><span data-stu-id="df471-208">System.Title</span></span>         | <span data-ttu-id="df471-209">2</span><span class="sxs-lookup"><span data-stu-id="df471-209">2</span></span>        |



 

## <a name="generic"></a><span data-ttu-id="df471-210">Allgemein</span><span class="sxs-lookup"><span data-stu-id="df471-210">Generic</span></span>



| <span data-ttu-id="df471-211">Name</span><span class="sxs-lookup"><span data-stu-id="df471-211">Name</span></span>     | <span data-ttu-id="df471-212">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="df471-212">Property</span></span>             | <span data-ttu-id="df471-213">Priorität</span><span class="sxs-lookup"><span data-stu-id="df471-213">Priority</span></span> |
|----------|----------------------|----------|
| <span data-ttu-id="df471-214">Authors</span><span class="sxs-lookup"><span data-stu-id="df471-214">Authors</span></span>  | <span data-ttu-id="df471-215">System.Author</span><span class="sxs-lookup"><span data-stu-id="df471-215">System.Author</span></span>        | <span data-ttu-id="df471-216">1</span><span class="sxs-lookup"><span data-stu-id="df471-216">1</span></span>        |
| <span data-ttu-id="df471-217">Titel</span><span class="sxs-lookup"><span data-stu-id="df471-217">Title</span></span>    | <span data-ttu-id="df471-218">System.Title</span><span class="sxs-lookup"><span data-stu-id="df471-218">System.Title</span></span>         | <span data-ttu-id="df471-219">1</span><span class="sxs-lookup"><span data-stu-id="df471-219">1</span></span>        |
| <span data-ttu-id="df471-220">type</span><span class="sxs-lookup"><span data-stu-id="df471-220">Type</span></span>     | <span data-ttu-id="df471-221">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="df471-221">System.PerceivedType</span></span> | <span data-ttu-id="df471-222">1</span><span class="sxs-lookup"><span data-stu-id="df471-222">1</span></span>        |
| <span data-ttu-id="df471-223">Category</span><span class="sxs-lookup"><span data-stu-id="df471-223">Category</span></span> | <span data-ttu-id="df471-224">System. Category</span><span class="sxs-lookup"><span data-stu-id="df471-224">System.Category</span></span>      | <span data-ttu-id="df471-225">2</span><span class="sxs-lookup"><span data-stu-id="df471-225">2</span></span>        |
| <span data-ttu-id="df471-226">`Tags`</span><span class="sxs-lookup"><span data-stu-id="df471-226">Tags</span></span>     | <span data-ttu-id="df471-227">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="df471-227">System.Keywords</span></span>      | <span data-ttu-id="df471-228">2</span><span class="sxs-lookup"><span data-stu-id="df471-228">2</span></span>        |



 

## <a name="music"></a><span data-ttu-id="df471-229">Musik</span><span class="sxs-lookup"><span data-stu-id="df471-229">Music</span></span>



| <span data-ttu-id="df471-230">Name</span><span class="sxs-lookup"><span data-stu-id="df471-230">Name</span></span>         | <span data-ttu-id="df471-231">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="df471-231">Property</span></span>                     | <span data-ttu-id="df471-232">Priorität</span><span class="sxs-lookup"><span data-stu-id="df471-232">Priority</span></span> |
|--------------|------------------------------|----------|
| \#           | <span data-ttu-id="df471-233">System. Music. tracknumber</span><span class="sxs-lookup"><span data-stu-id="df471-233">System.Music.TrackNumber</span></span>     | <span data-ttu-id="df471-234">1</span><span class="sxs-lookup"><span data-stu-id="df471-234">1</span></span>        |
| <span data-ttu-id="df471-235">Aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="df471-235">Album</span></span>        | <span data-ttu-id="df471-236">System. Music. albumtitle</span><span class="sxs-lookup"><span data-stu-id="df471-236">System.Music.AlbumTitle</span></span>      | <span data-ttu-id="df471-237">1</span><span class="sxs-lookup"><span data-stu-id="df471-237">1</span></span>        |
| <span data-ttu-id="df471-238">Künstler</span><span class="sxs-lookup"><span data-stu-id="df471-238">Artists</span></span>      | <span data-ttu-id="df471-239">System. Music. Artist</span><span class="sxs-lookup"><span data-stu-id="df471-239">System.Music.Artist</span></span>          | <span data-ttu-id="df471-240">1</span><span class="sxs-lookup"><span data-stu-id="df471-240">1</span></span>        |
| <span data-ttu-id="df471-241">Genre</span><span class="sxs-lookup"><span data-stu-id="df471-241">Genre</span></span>        | <span data-ttu-id="df471-242">System. Music. Genre</span><span class="sxs-lookup"><span data-stu-id="df471-242">System.Music.Genre</span></span>           | <span data-ttu-id="df471-243">1</span><span class="sxs-lookup"><span data-stu-id="df471-243">1</span></span>        |
| <span data-ttu-id="df471-244">Rating</span><span class="sxs-lookup"><span data-stu-id="df471-244">Rating</span></span>       | <span data-ttu-id="df471-245">System. Rating</span><span class="sxs-lookup"><span data-stu-id="df471-245">System.Rating</span></span>                | <span data-ttu-id="df471-246">1</span><span class="sxs-lookup"><span data-stu-id="df471-246">1</span></span>        |
| <span data-ttu-id="df471-247">Titel</span><span class="sxs-lookup"><span data-stu-id="df471-247">Title</span></span>        | <span data-ttu-id="df471-248">System.Title</span><span class="sxs-lookup"><span data-stu-id="df471-248">System.Title</span></span>                 | <span data-ttu-id="df471-249">1</span><span class="sxs-lookup"><span data-stu-id="df471-249">1</span></span>        |
| <span data-ttu-id="df471-250">Album-Künstlerin</span><span class="sxs-lookup"><span data-stu-id="df471-250">Album Artist</span></span> | <span data-ttu-id="df471-251">System. Music. albumartist</span><span class="sxs-lookup"><span data-stu-id="df471-251">System.Music.AlbumArtist</span></span>     | <span data-ttu-id="df471-252">2</span><span class="sxs-lookup"><span data-stu-id="df471-252">2</span></span>        |
| <span data-ttu-id="df471-253">Bitrate</span><span class="sxs-lookup"><span data-stu-id="df471-253">Bit Rate</span></span>     | <span data-ttu-id="df471-254">System. Audio. encodingbitrate</span><span class="sxs-lookup"><span data-stu-id="df471-254">System.Audio.EncodingBitrate</span></span> | <span data-ttu-id="df471-255">2</span><span class="sxs-lookup"><span data-stu-id="df471-255">2</span></span>        |
| <span data-ttu-id="df471-256">Chor</span><span class="sxs-lookup"><span data-stu-id="df471-256">Conductors</span></span>   | <span data-ttu-id="df471-257">System. Music. Conductor</span><span class="sxs-lookup"><span data-stu-id="df471-257">System.Music.Conductor</span></span>       | <span data-ttu-id="df471-258">2</span><span class="sxs-lookup"><span data-stu-id="df471-258">2</span></span>        |
| <span data-ttu-id="df471-259">Länge</span><span class="sxs-lookup"><span data-stu-id="df471-259">Length</span></span>       | <span data-ttu-id="df471-260">System. Media. Duration</span><span class="sxs-lookup"><span data-stu-id="df471-260">System.Media.Duration</span></span>        | <span data-ttu-id="df471-261">2</span><span class="sxs-lookup"><span data-stu-id="df471-261">2</span></span>        |
| <span data-ttu-id="df471-262">Protected</span><span class="sxs-lookup"><span data-stu-id="df471-262">Protected</span></span>    | <span data-ttu-id="df471-263">System. DRM. IsProtected</span><span class="sxs-lookup"><span data-stu-id="df471-263">System.DRM.IsProtected</span></span>       | <span data-ttu-id="df471-264">2</span><span class="sxs-lookup"><span data-stu-id="df471-264">2</span></span>        |
| <span data-ttu-id="df471-265">Jahr</span><span class="sxs-lookup"><span data-stu-id="df471-265">Year</span></span>         | <span data-ttu-id="df471-266">System. Media. Year</span><span class="sxs-lookup"><span data-stu-id="df471-266">System.Media.Year</span></span>            | <span data-ttu-id="df471-267">2</span><span class="sxs-lookup"><span data-stu-id="df471-267">2</span></span>        |



 

## <a name="pictures"></a><span data-ttu-id="df471-268">Bilder</span><span class="sxs-lookup"><span data-stu-id="df471-268">Pictures</span></span>



| <span data-ttu-id="df471-269">Name</span><span class="sxs-lookup"><span data-stu-id="df471-269">Name</span></span>          | <span data-ttu-id="df471-270">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="df471-270">Property</span></span>                        | <span data-ttu-id="df471-271">Priorität</span><span class="sxs-lookup"><span data-stu-id="df471-271">Priority</span></span> |
|---------------|---------------------------------|----------|
| <span data-ttu-id="df471-272">Import Datum</span><span class="sxs-lookup"><span data-stu-id="df471-272">Date imported</span></span> | <span data-ttu-id="df471-273">System. dateimportiert</span><span class="sxs-lookup"><span data-stu-id="df471-273">System.DateImported</span></span>             | <span data-ttu-id="df471-274">1</span><span class="sxs-lookup"><span data-stu-id="df471-274">1</span></span>        |
| <span data-ttu-id="df471-275">Datum der Erstellung</span><span class="sxs-lookup"><span data-stu-id="df471-275">Date Taken</span></span>    | <span data-ttu-id="df471-276">System. Photo. DateTaken</span><span class="sxs-lookup"><span data-stu-id="df471-276">System.Photo.DateTaken</span></span>          | <span data-ttu-id="df471-277">1</span><span class="sxs-lookup"><span data-stu-id="df471-277">1</span></span>        |
| <span data-ttu-id="df471-278">Rating</span><span class="sxs-lookup"><span data-stu-id="df471-278">Rating</span></span>        | <span data-ttu-id="df471-279">System. Rating</span><span class="sxs-lookup"><span data-stu-id="df471-279">System.Rating</span></span>                   | <span data-ttu-id="df471-280">1</span><span class="sxs-lookup"><span data-stu-id="df471-280">1</span></span>        |
| <span data-ttu-id="df471-281">`Tags`</span><span class="sxs-lookup"><span data-stu-id="df471-281">Tags</span></span>          | <span data-ttu-id="df471-282">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="df471-282">System.Keywords</span></span>                 | <span data-ttu-id="df471-283">1</span><span class="sxs-lookup"><span data-stu-id="df471-283">1</span></span>        |
| <span data-ttu-id="df471-284">type</span><span class="sxs-lookup"><span data-stu-id="df471-284">Type</span></span>          | <span data-ttu-id="df471-285">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="df471-285">System.PerceivedType</span></span>            | <span data-ttu-id="df471-286">1</span><span class="sxs-lookup"><span data-stu-id="df471-286">1</span></span>        |
| <span data-ttu-id="df471-287">Authors</span><span class="sxs-lookup"><span data-stu-id="df471-287">Authors</span></span>       | <span data-ttu-id="df471-288">System.Author</span><span class="sxs-lookup"><span data-stu-id="df471-288">System.Author</span></span>                   | <span data-ttu-id="df471-289">2</span><span class="sxs-lookup"><span data-stu-id="df471-289">2</span></span>        |
| <span data-ttu-id="df471-290">Kamerahersteller</span><span class="sxs-lookup"><span data-stu-id="df471-290">Camera maker</span></span>  | <span data-ttu-id="df471-291">System. Photo. cameramanufakturer</span><span class="sxs-lookup"><span data-stu-id="df471-291">System.Photo.CameraManufacturer</span></span> | <span data-ttu-id="df471-292">2</span><span class="sxs-lookup"><span data-stu-id="df471-292">2</span></span>        |
| <span data-ttu-id="df471-293">Kameramodell</span><span class="sxs-lookup"><span data-stu-id="df471-293">Camera model</span></span>  | <span data-ttu-id="df471-294">System. Photo. CameraModel</span><span class="sxs-lookup"><span data-stu-id="df471-294">System.Photo.CameraModel</span></span>        | <span data-ttu-id="df471-295">2</span><span class="sxs-lookup"><span data-stu-id="df471-295">2</span></span>        |
| <span data-ttu-id="df471-296">Kommentare</span><span class="sxs-lookup"><span data-stu-id="df471-296">Comments</span></span>      | <span data-ttu-id="df471-297">System. Comment</span><span class="sxs-lookup"><span data-stu-id="df471-297">System.Comment</span></span>                  | <span data-ttu-id="df471-298">2</span><span class="sxs-lookup"><span data-stu-id="df471-298">2</span></span>        |
| <span data-ttu-id="df471-299">Dimensionen</span><span class="sxs-lookup"><span data-stu-id="df471-299">Dimensions</span></span>    | <span data-ttu-id="df471-300">System. Image. Dimensions</span><span class="sxs-lookup"><span data-stu-id="df471-300">System.Image.Dimensions</span></span>         | <span data-ttu-id="df471-301">2</span><span class="sxs-lookup"><span data-stu-id="df471-301">2</span></span>        |



 

## <a name="videos"></a><span data-ttu-id="df471-302">Videos</span><span class="sxs-lookup"><span data-stu-id="df471-302">Videos</span></span>



| <span data-ttu-id="df471-303">Name</span><span class="sxs-lookup"><span data-stu-id="df471-303">Name</span></span>         | <span data-ttu-id="df471-304">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="df471-304">Property</span></span>                 | <span data-ttu-id="df471-305">Priorität</span><span class="sxs-lookup"><span data-stu-id="df471-305">Priority</span></span> |
|--------------|--------------------------|----------|
| <span data-ttu-id="df471-306">Länge</span><span class="sxs-lookup"><span data-stu-id="df471-306">Length</span></span>       | <span data-ttu-id="df471-307">System. Media. Duration</span><span class="sxs-lookup"><span data-stu-id="df471-307">System.Media.Duration</span></span>    | <span data-ttu-id="df471-308">1</span><span class="sxs-lookup"><span data-stu-id="df471-308">1</span></span>        |
| <span data-ttu-id="df471-309">Rating</span><span class="sxs-lookup"><span data-stu-id="df471-309">Rating</span></span>       | <span data-ttu-id="df471-310">System. Rating</span><span class="sxs-lookup"><span data-stu-id="df471-310">System.Rating</span></span>            | <span data-ttu-id="df471-311">1</span><span class="sxs-lookup"><span data-stu-id="df471-311">1</span></span>        |
| <span data-ttu-id="df471-312">`Tags`</span><span class="sxs-lookup"><span data-stu-id="df471-312">Tags</span></span>         | <span data-ttu-id="df471-313">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="df471-313">System.Keywords</span></span>          | <span data-ttu-id="df471-314">1</span><span class="sxs-lookup"><span data-stu-id="df471-314">1</span></span>        |
| <span data-ttu-id="df471-315">type</span><span class="sxs-lookup"><span data-stu-id="df471-315">Type</span></span>         | <span data-ttu-id="df471-316">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="df471-316">System.PerceivedType</span></span>     | <span data-ttu-id="df471-317">1</span><span class="sxs-lookup"><span data-stu-id="df471-317">1</span></span>        |
| <span data-ttu-id="df471-318">Rahmenhöhe</span><span class="sxs-lookup"><span data-stu-id="df471-318">Frame height</span></span> | <span data-ttu-id="df471-319">System. Video. frameheight</span><span class="sxs-lookup"><span data-stu-id="df471-319">System.Video.FrameHeight</span></span> | <span data-ttu-id="df471-320">2</span><span class="sxs-lookup"><span data-stu-id="df471-320">2</span></span>        |
| <span data-ttu-id="df471-321">Rahmenbreite</span><span class="sxs-lookup"><span data-stu-id="df471-321">Frame width</span></span>  | <span data-ttu-id="df471-322">System. Video. framewidth</span><span class="sxs-lookup"><span data-stu-id="df471-322">System.Video.FrameWidth</span></span>  | <span data-ttu-id="df471-323">2</span><span class="sxs-lookup"><span data-stu-id="df471-323">2</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="df471-324">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df471-324">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="df471-325">**Licher**</span><span class="sxs-lookup"><span data-stu-id="df471-325">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="df471-326">Entwickeln von Eigenschaften Handlern für Windows Search</span><span class="sxs-lookup"><span data-stu-id="df471-326">Developing Property Handlers for Windows Search</span></span>](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

<span data-ttu-id="df471-327">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="df471-327">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="df471-328">Eigenschaften System</span><span class="sxs-lookup"><span data-stu-id="df471-328">Property System</span></span>](../properties/building-property-handlers.md)
</dt> <dt>

<span data-ttu-id="df471-329">[System Eigenschaften](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="df471-329">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> </dl>

 

 
