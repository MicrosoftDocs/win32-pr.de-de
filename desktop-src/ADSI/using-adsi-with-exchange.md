---
title: Verwenden von ADSI mit Exchange
description: Für Exchange 2000 sind Informationen zur Verwendung von ADSI mit Exchange im Exchange 2000 SDK enthalten. Weitere Informationen finden Sie unter Verwaltungsaufgaben für ADSI.
ms.assetid: c806ca1b-c97c-4567-af8b-e12cfde2bf70
ms.tgt_platform: multiple
keywords:
- ADSI für Exchange ADSI
- ADSI für Exchange ADSI, Postfächer
- ADSI für Exchange ADSI, Postfächer, erstellen
- ADSI für Exchange ADSI, Postfächer, löschen
- ADSI für Exchange ADSI, Postfächer, Festlegen der Sicherheits Beschreibung für
- ADSI für Exchange ADSI, Postfächer, Suche nach Home Server für
- ADSI für Exchange ADSI, das erhalten und Ändern von Nachrichten
- ADSI für Exchange ADSI, Sicherheits Deskriptoren
- ADSI für Exchange ADSI, Sicherheits Deskriptoren, Bearbeitung
- ADSI für Exchange ADSI, Sicherheits Deskriptoren, festlegen
- ADSI für Exchange ADSI, Empfänger Container
- ADSI für Exchange ADSI, Anzeigen von Exchange-Objekteigenschaften
- ADSI für Exchange ADSI, Empfängers Container, Custom
- ADSI für Exchange ADSI, Exchange Server
- ADSI für Exchange ADSI, Exchange Server, anzeigen und Ändern des Schemas
- ADSI für Exchange ADSI, Exchange Server, Auflisten der Server Version
- ADSI für Exchange ADSI, Exchange Server, Organisation und Website Name
- ADSI für Exchange ADSI, Exchange Server, Suche nach Mailbox Home Server
- ADSI für Exchange ADSI, e-Mail-Adressen, Abrufen
- ADSI für Exchange ADSI, Verteilerlisten, erstellen
- ADSI für Exchange ADSI, verborgene oder gelöschte Einträge
- ADSI für Exchange ADSI, Abrufen von Verzeichnisdienst Änderungen
- ADSI für Exchange ADSI, Nachrichtengröße
- ADSI für Exchange ADSI, Problembehandlung
- Postfächer ADSI
- Postfächer ADSI, erstellen
- Postfächer ADSI, löschen
- Postfächer ADSI, Festlegen der Sicherheits Beschreibung für
- Postfächer ADSI, Suche nach Home Server für
- Nachrichten ADSI, Getting und Modifizierung
- Exchange ADSI
- Exchange ADSI, Postfächer
- Exchange ADSI, Postfächer, erstellen
- Exchange ADSI, Postfächer, löschen
- Exchange ADSI, Postfächer, Festlegen der Sicherheits Beschreibung für
- Exchange ADSI, Postfächer, Suche nach Home Server für
- Exchange ADSI, das erhalten und Ändern von Nachrichten
- Exchange ADSI, Sicherheits Deskriptoren
- Exchange ADSI, Sicherheits Deskriptoren, bearbeiten
- Exchange ADSI, Sicherheits Deskriptoren, festlegen
- Exchange ADSI, Empfänger Container
- Exchange ADSI, Anzeigen von Exchange-Objekteigenschaften
- Exchange ADSI, Empfänger Container, Benutzer definiert
- Exchange ADSI, Exchange Server
- Exchange ADSI, Exchange Server, anzeigen und Ändern des Schemas
- Exchange ADSI, Exchange Server, Auflisten der Server Version
- Exchange ADSI, Exchange Server, Organisation und Website Name
- Exchange ADSI, Exchange Server, Suchen des Postfachs Home Server
- Exchange ADSI, e-Mail-Adressen, Abrufen
- Exchange ADSI, Verteilerlisten, erstellen
- Exchange ADSI, verborgene oder gelöschte Einträge
- Exchange ADSI, Abrufen von Verzeichnisdienst Änderungen
- Exchange ADSI, Nachrichtengröße
- Exchange ADSI, Problembehandlung
- Sicherheits Deskriptoren ADSI für Exchange-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833d60c284a12e759eb74b22c9aa48abc75da463
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337255"
---
# <a name="using-adsi-with-exchange"></a><span data-ttu-id="45931-159">Verwenden von ADSI mit Exchange</span><span class="sxs-lookup"><span data-stu-id="45931-159">Using ADSI with Exchange</span></span>

<span data-ttu-id="45931-160">Für Exchange 2000 sind Informationen zur Verwendung von ADSI mit Exchange im Exchange 2000 SDK enthalten.</span><span class="sxs-lookup"><span data-stu-id="45931-160">For Exchange 2000, information for using ADSI with Exchange is contained in the Exchange 2000 SDK.</span></span> <span data-ttu-id="45931-161">Weitere Informationen finden Sie unter [Verwaltungsaufgaben für ADSI](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65)).</span><span class="sxs-lookup"><span data-stu-id="45931-161">For more information, see [Management Tasks for ADSI](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65)).</span></span>

<span data-ttu-id="45931-162">Die folgenden Aufgaben finden Sie in diesem Abschnitt:</span><span class="sxs-lookup"><span data-stu-id="45931-162">The following tasks can be found in this section:</span></span>

-   <span data-ttu-id="45931-163">Erstellen einer Benutzer-URL</span><span class="sxs-lookup"><span data-stu-id="45931-163">Creating a user URL</span></span>
-   <span data-ttu-id="45931-164">Active Directory Pfade werden aufgebaut.</span><span class="sxs-lookup"><span data-stu-id="45931-164">Building Active Directory paths</span></span>
-   <span data-ttu-id="45931-165">Auflisten von Exchange 2000-Servern mit ADSI</span><span class="sxs-lookup"><span data-stu-id="45931-165">Enumerating Exchange 2000 servers with ADSI</span></span>
-   <span data-ttu-id="45931-166">Bearbeiten von Erweiterungs Attributen mit ADSI</span><span class="sxs-lookup"><span data-stu-id="45931-166">Manipulating extension attributes with ADSI</span></span>
-   <span data-ttu-id="45931-167">Hinzufügen/Entfernen eines Manager-Objekts mit ADSI</span><span class="sxs-lookup"><span data-stu-id="45931-167">Adding/removing a manager object with ADSI</span></span>
-   <span data-ttu-id="45931-168">Auflisten von Exchange-Objekteigenschaften mit ADSI/ADO</span><span class="sxs-lookup"><span data-stu-id="45931-168">Enumerating Exchange object properties with ADSI/ADO</span></span>
-   <span data-ttu-id="45931-169">Abrufen eines definierten Legacy namens von Exchange mit ADSI</span><span class="sxs-lookup"><span data-stu-id="45931-169">Retrieving a legacy Exchange distinguished name with ADSI</span></span>
-   <span data-ttu-id="45931-170">Suchen des Namens der Exchange-Organisation mit ADSI</span><span class="sxs-lookup"><span data-stu-id="45931-170">Finding the Exchange organization name using ADSI</span></span>
-   <span data-ttu-id="45931-171">Suchen von Exchange-Adresslisten mit ADSI</span><span class="sxs-lookup"><span data-stu-id="45931-171">Finding Exchange address lists with ADSI</span></span>
-   <span data-ttu-id="45931-172">Erstellen einer Verteilerliste mit CDOEXM und ADSI</span><span class="sxs-lookup"><span data-stu-id="45931-172">Creating a distribution list using CDOEXM and ADSI</span></span>
-   <span data-ttu-id="45931-173">Festlegen der Nachrichten Einschränkung auf einem virtuellen SMTP-Server mithilfe von ADSI</span><span class="sxs-lookup"><span data-stu-id="45931-173">Setting message restriction on an SMTP virtual server using ADSI</span></span>

<span data-ttu-id="45931-174">Die ADSI-Referenz und die Verwendung von Informationen für Exchange 5,5 finden Sie im [ADSI Exchange](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) Guide.</span><span class="sxs-lookup"><span data-stu-id="45931-174">For Exchange 5.5, the ADSI reference and using information can be found in the [ADSI Exchange](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) guide.</span></span>

<span data-ttu-id="45931-175">Die folgenden Aufgaben finden Sie in diesem Abschnitt:</span><span class="sxs-lookup"><span data-stu-id="45931-175">The following tasks can be found in this section:</span></span>

-   <span data-ttu-id="45931-176">Anzeigen und Ändern des Exchange Server-Schemas</span><span class="sxs-lookup"><span data-stu-id="45931-176">Viewing and modifying the Exchange Server Schema</span></span>
-   <span data-ttu-id="45931-177">Anzeigen der roheigenschaften eines Exchange-Objekts</span><span class="sxs-lookup"><span data-stu-id="45931-177">Viewing the raw properties of an Exchange object</span></span>
-   <span data-ttu-id="45931-178">Erstellen eines Exchange-Postfachs</span><span class="sxs-lookup"><span data-stu-id="45931-178">Creating an Exchange mailbox</span></span>
-   <span data-ttu-id="45931-179">Festlegen der Sicherheits Beschreibung für ein Exchange-Postfach</span><span class="sxs-lookup"><span data-stu-id="45931-179">Setting the security descriptor on an Exchange mailbox</span></span>
-   <span data-ttu-id="45931-180">Manipulieren von Sicherheits Deskriptoren und SIDs</span><span class="sxs-lookup"><span data-stu-id="45931-180">Manipulating security descriptors and SIDs</span></span>
-   <span data-ttu-id="45931-181">Löschen eines Post Fach Objekts</span><span class="sxs-lookup"><span data-stu-id="45931-181">Deleting a mailbox object</span></span>
-   <span data-ttu-id="45931-182">Erstellen eines benutzerdefinierten Empfängers</span><span class="sxs-lookup"><span data-stu-id="45931-182">Creating a custom recipient</span></span>
-   <span data-ttu-id="45931-183">Erstellen eines Empfänger Containers</span><span class="sxs-lookup"><span data-stu-id="45931-183">Creating a recipients container</span></span>
-   <span data-ttu-id="45931-184">Die Organisation und der Standort Name werden von einem Server erhalten.</span><span class="sxs-lookup"><span data-stu-id="45931-184">Getting the organization and site name from a server</span></span>
-   <span data-ttu-id="45931-185">Auflisten der Exchange Server-Version aller Server in der Organisation</span><span class="sxs-lookup"><span data-stu-id="45931-185">Listing the Exchange server version of all the servers in the organization</span></span>
-   <span data-ttu-id="45931-186">Suchen des Basis Servers eines Postfachs</span><span class="sxs-lookup"><span data-stu-id="45931-186">Finding the home server of a mailbox</span></span>
-   <span data-ttu-id="45931-187">Abrufen von e-Mail-Adressen</span><span class="sxs-lookup"><span data-stu-id="45931-187">Retrieving email addresses</span></span>
-   <span data-ttu-id="45931-188">Zugreifen auf verborgene oder gelöschte Einträge</span><span class="sxs-lookup"><span data-stu-id="45931-188">Accessing hidden or deleted entries</span></span>
-   <span data-ttu-id="45931-189">Abrufen von Änderungen, die an den Verzeichnisdienst vorgenommen wurden</span><span class="sxs-lookup"><span data-stu-id="45931-189">Retrieving changes made to the directory service</span></span>
-   <span data-ttu-id="45931-190">Erstellen einer Verteilerliste aus den Ergebnissen einer Abfrage</span><span class="sxs-lookup"><span data-stu-id="45931-190">Creating a distribution list from the results of a query</span></span>
-   <span data-ttu-id="45931-191">Erhalten oder Ändern der Nachrichtengröße</span><span class="sxs-lookup"><span data-stu-id="45931-191">Getting or modifying message size</span></span>
-   <span data-ttu-id="45931-192">Verwenden von LDAP-Fehlercodes zum Beheben von Problemen</span><span class="sxs-lookup"><span data-stu-id="45931-192">Using LDAP error codes to troubleshoot problems</span></span>

 

 