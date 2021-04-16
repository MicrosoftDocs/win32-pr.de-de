---
description: Dieses Thema enthält Informationen zum Schreiben eines Protokoll Parsers und enthält Beispiele für die Exportfunktionen, die von der Parser-DLL implementiert werden müssen.
ms.assetid: 0be87b33-aab0-4986-8a86-914e0a7b8f2d
title: Schreiben eines Protokoll Parsers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338c224dd036df747af6ab805dae273f6ad3f510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528733"
---
# <a name="writing-a-protocol-parser"></a><span data-ttu-id="f66fd-103">Schreiben eines Protokoll Parsers</span><span class="sxs-lookup"><span data-stu-id="f66fd-103">Writing a Protocol Parser</span></span>

<span data-ttu-id="f66fd-104">Dieses Thema enthält Informationen zum Schreiben eines Protokoll Parsers und enthält Beispiele für die Exportfunktionen, die von der Parser-DLL implementiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f66fd-104">This topic contains information about writing a protocol parser, and includes examples of the export functions that the parser DLL must implement.</span></span>

<span data-ttu-id="f66fd-105">Die folgenden Themen sind in diesem Abschnitt enthalten.</span><span class="sxs-lookup"><span data-stu-id="f66fd-105">The following topics are included in this section.</span></span>



| <span data-ttu-id="f66fd-106">Begriff</span><span class="sxs-lookup"><span data-stu-id="f66fd-106">Term</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="f66fd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f66fd-107">Description</span></span>                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f66fd-108"><span id="Programming_Considerations"></span><span id="programming_considerations"></span><span id="PROGRAMMING_CONSIDERATIONS"></span>[Überlegungen zur Programmierung](programming-considerations.md)</span><span class="sxs-lookup"><span data-stu-id="f66fd-108"><span id="Programming_Considerations"></span><span id="programming_considerations"></span><span id="PROGRAMMING_CONSIDERATIONS"></span>[Programming Considerations](programming-considerations.md)</span></span><br/>                                                   | <span data-ttu-id="f66fd-109">Gibt Aufschluss über die grundlegenden Programmiertipps, die Ihnen beim Schreiben einer Parser-DLL helfen.</span><span class="sxs-lookup"><span data-stu-id="f66fd-109">Identifies the basic programming tips to help you write a parser DLL.</span></span><br/>                                                                                    |
| <span data-ttu-id="f66fd-110"><span id="Implementing_Parser_Export_Functions"></span><span id="implementing_parser_export_functions"></span><span id="IMPLEMENTING_PARSER_EXPORT_FUNCTIONS"></span>[Implementieren von parserexportfunktionen](implementing-parser-export-functions.md)</span><span class="sxs-lookup"><span data-stu-id="f66fd-110"><span id="Implementing_Parser_Export_Functions"></span><span id="implementing_parser_export_functions"></span><span id="IMPLEMENTING_PARSER_EXPORT_FUNCTIONS"></span>[Implementing Parser Export Functions](implementing-parser-export-functions.md)</span></span><br/> | <span data-ttu-id="f66fd-111">Enthält Beispiele für das Implementieren von Exportfunktionen.</span><span class="sxs-lookup"><span data-stu-id="f66fd-111">Provides examples of implementing export functions.</span></span><br/>                                                                                                      |
| <span data-ttu-id="f66fd-112"><span id="Formatting_Displayed_Data"></span><span id="formatting_displayed_data"></span><span id="FORMATTING_DISPLAYED_DATA"></span>[Formatieren der angezeigten Daten](formatting-displayed-data.md)</span><span class="sxs-lookup"><span data-stu-id="f66fd-112"><span id="Formatting_Displayed_Data"></span><span id="formatting_displayed_data"></span><span id="FORMATTING_DISPLAYED_DATA"></span>[Formatting Displayed Data](formatting-displayed-data.md)</span></span><br/>                                                        | <span data-ttu-id="f66fd-113">Gibt den Prozess der Formatierung von Daten an, die im Detailbereich der Netzwerkmonitor-Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f66fd-113">Identifies the process of formatting data that is displayed in the details pane of the Network Monitor UI.</span></span><br/>                                               |
| <span data-ttu-id="f66fd-114"><span id="Specifying_a_Follow_Set"></span><span id="specifying_a_follow_set"></span><span id="SPECIFYING_A_FOLLOW_SET"></span>[Angeben eines folgenden Satzes](specifying-a-follow-set.md)</span><span class="sxs-lookup"><span data-stu-id="f66fd-114"><span id="Specifying_a_Follow_Set"></span><span id="specifying_a_follow_set"></span><span id="SPECIFYING_A_FOLLOW_SET"></span>[Specifying a Follow Set](specifying-a-follow-set.md)</span></span><br/>                                                                  | <span data-ttu-id="f66fd-115">Identifiziert den Prozess der Angabe eines nachfolgenden Satzes und zeigt, wie Netzwerkmonitor auf den folgenden Satz eines Parsers zugreift, um das nächste Protokoll zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="f66fd-115">Identifies the process of specifying a follow set, and shows you how Network Monitor accesses the follow set of a parser to determine the next protocol.</span></span><br/> |
| <span data-ttu-id="f66fd-116"><span id="Specifying_a_Handoff_Set"></span><span id="specifying_a_handoff_set"></span><span id="SPECIFYING_A_HANDOFF_SET"></span>[Angeben einer Übergabe Gruppe](specifying-a-handoff-set.md)</span><span class="sxs-lookup"><span data-stu-id="f66fd-116"><span id="Specifying_a_Handoff_Set"></span><span id="specifying_a_handoff_set"></span><span id="SPECIFYING_A_HANDOFF_SET"></span>[Specifying a Handoff Set](specifying-a-handoff-set.md)</span></span><br/>                                                             | <span data-ttu-id="f66fd-117">Gibt den Prozess der Angabe einer Übergabe-Menge an und zeigt, wie der Parser auf seine Handzettel zugreift, um ein Handle für das nächste Protokoll zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f66fd-117">Identifies the process of specifying a handoff set, and shows you how the parser accesses its handoff set to get a handle to the next protocol.</span></span><br/>          |



 

 

 




