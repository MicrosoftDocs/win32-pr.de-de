---
description: Benutzerdefinierte Ice-Aktionen kommunizieren durch Aufrufen von "msiprocessmessage" und Veröffentlichen einer installmessage- \_ benutzertypnachricht.
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: Richtlinien für ICE Message
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4bee7dbf22184883e49da4d5a5f66f9debb577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958887"
---
# <a name="ice-message-guidelines"></a><span data-ttu-id="1d8ac-103">Richtlinien für ICE Message</span><span class="sxs-lookup"><span data-stu-id="1d8ac-103">ICE Message Guidelines</span></span>

<span data-ttu-id="1d8ac-104">Benutzerdefinierte Ice-Aktionen kommunizieren durch Aufrufen von " [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) " und Veröffentlichen einer installmessage- \_ benutzertypnachricht.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-104">ICE custom actions communicate by calling [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) and posting an INSTALLMESSAGE\_USER type message.</span></span>

<span data-ttu-id="1d8ac-105">Beim Erstellen einer Meldungs Zeichenfolge für eine benutzerdefinierte Ice-Aktion formatieren Sie die Zeichenfolge wie folgt.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-105">When authoring a message string for an ICE custom action, format the string as follows.</span></span>

<span data-ttu-id="1d8ac-106">*Name des ICE* <tab> *Nachrichtentyp* <tab> *Beschreibung* <tab> *Hilfe-URL oder-Speicherort* <tab> *Tabellen Name* <tab> *Spalten Name* <tab> *Primärschlüssel* <tab> *Primärschlüssel* <tab> *Primärschlüssel* .</span><span class="sxs-lookup"><span data-stu-id="1d8ac-106">*Name of ICE* <tab> *Message Type* <tab> *Description* <tab> *Help URL or location* <tab> *Table Name* <tab> *Column Name* <tab> *Primary Key* <tab> *Primary Key* <tab> *Primary Key* .</span></span> <span data-ttu-id="1d8ac-107">.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-107">.</span></span> <span data-ttu-id="1d8ac-108">.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-108">.</span></span> <span data-ttu-id="1d8ac-109">(wiederholen Sie dies bei Bedarf für so viele Primärschlüssel).</span><span class="sxs-lookup"><span data-stu-id="1d8ac-109">(repeat for as many primary keys as needed)</span></span>

<span data-ttu-id="1d8ac-110">Die ersten drei Felder der Zeichenfolge sind in jeder Nachricht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-110">The first three fields of the string are required in every message.</span></span>

<span data-ttu-id="1d8ac-111">Das Feld Nachrichtentyp gibt an, ob das Ice einen Fehler, Fehler, eine Warnung oder eine Informations Meldung meldet.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-111">The Message Type field specifies whether the ICE reports a Failure, Error, Warning, or Informational message.</span></span>



| <span data-ttu-id="1d8ac-112">Wert</span><span class="sxs-lookup"><span data-stu-id="1d8ac-112">Value</span></span> | <span data-ttu-id="1d8ac-113">Nachrichtentyp</span><span class="sxs-lookup"><span data-stu-id="1d8ac-113">Message type</span></span>                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d8ac-114">0</span><span class="sxs-lookup"><span data-stu-id="1d8ac-114">0</span></span>     | <span data-ttu-id="1d8ac-115">Fehlermeldung, die den Fehler der benutzerdefinierten Ice-Aktion meldet.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-115">Failure message reporting the failure of the ICE custom action.</span></span>                                                                                                       |
| <span data-ttu-id="1d8ac-116">1</span><span class="sxs-lookup"><span data-stu-id="1d8ac-116">1</span></span>     | <span data-ttu-id="1d8ac-117">Fehlermeldungs Berichterstellung der Datenbank, die falsches Verhalten verursachen.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-117">Error message reporting database authoring that cause incorrect behavior.</span></span>                                                                                             |
| <span data-ttu-id="1d8ac-118">2</span><span class="sxs-lookup"><span data-stu-id="1d8ac-118">2</span></span>     | <span data-ttu-id="1d8ac-119">Warnmeldung Berichterstellung der Datenbank, die in bestimmten Fällen falsches Verhalten verursacht.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-119">Warning message reporting database authoring that causes incorrect behavior in certain cases.</span></span> <span data-ttu-id="1d8ac-120">Warnungen können auch unerwartete Nebeneffekte der Daten Bank Erstellung melden.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-120">Warnings can also report unexpected side-effects of database authoring.</span></span> |
| <span data-ttu-id="1d8ac-121">3</span><span class="sxs-lookup"><span data-stu-id="1d8ac-121">3</span></span>     | <span data-ttu-id="1d8ac-122">Informationsmeldung.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-122">Informational message.</span></span>                                                                                                                                                |



 

<span data-ttu-id="1d8ac-123">Wenn die Hilfe nicht verfügbar ist, kann das Feld "Hilfe-URL" eine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-123">If help is not available, the Help URL field may be the empty string.</span></span>

<span data-ttu-id="1d8ac-124">Fehler-und Warnmeldungen sollten den Tabellennamen, Spaltennamen und Primärschlüssel Felder bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-124">Error and Warning messages should provide the Table Name, Column Name, and Primary Key fields.</span></span> <span data-ttu-id="1d8ac-125">Wenn eines dieser Felder weggelassen wird, müssen alle Felder, die dem ersten leeren Feld folgen, nicht aus der Nachricht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-125">If any of these fields are omitted, all of the fields following the first blank field must be left out of the message.</span></span> <span data-ttu-id="1d8ac-126">Beispielsweise wird ein Tabellenname ohne einen Spaltennamen und Primärschlüssel oder einen Tabellennamen bereitgestellt, und ein Spaltenname wird ohne Primärschlüssel bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-126">For example, a table name is provided without a column name and primary keys or a table name and a column name is provided with no primary keys.</span></span> <span data-ttu-id="1d8ac-127">Ein Spaltenname und Primärschlüssel können jedoch nicht ohne einen Tabellennamen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-127">However a column name and primary keys cannot be used without a table name.</span></span> <span data-ttu-id="1d8ac-128">Es können mehrere Primärschlüssel aufgelistet werden, bis allen primär Schlüsseln in dieser Tabelle Werte zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-128">Multiple primary keys may be listed until all the primary keys in that table have been given values.</span></span>

## <a name="examples"></a><span data-ttu-id="1d8ac-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d8ac-129">Examples</span></span>

<span data-ttu-id="1d8ac-130">Die erste Meldung, die durch das [Sample Ice in C++](sample-ice-in-c-.md)veranschaulicht wird:</span><span class="sxs-lookup"><span data-stu-id="1d8ac-130">The first message illustrated by the [Sample ICE in C++](sample-ice-in-c-.md):</span></span>

<span data-ttu-id="1d8ac-131">"ICE01 \\ T3 \\ tcreated 04/29/1998 by <hier den Namen des Autors einfügen>."</span><span class="sxs-lookup"><span data-stu-id="1d8ac-131">"ICE01\\t3\\tCreated 04/29/1998 by <insert author's name here>."</span></span>

<span data-ttu-id="1d8ac-132">Die zweite Nachricht, die von dem Sample Ice gepostet wurde:</span><span class="sxs-lookup"><span data-stu-id="1d8ac-132">The second message posted by the sample ICE:</span></span>

<span data-ttu-id="1d8ac-133">"ICE01 \\ T3 \\ tlast modified 05/06/1999 by <hier den Namen des Autors einfügen>."</span><span class="sxs-lookup"><span data-stu-id="1d8ac-133">"ICE01\\t3\\tLast modified 05/06/1999 by <insert author's name here>."</span></span>

<span data-ttu-id="1d8ac-134">Die dritte Nachricht, die von dem Sample Ice gepostet wurde.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-134">The third message posted by the sample ICE.</span></span>

<span data-ttu-id="1d8ac-135">"ICE01 \\ T3 \\ tsimple Ice, um das eiskonzept zu veranschaulichen".</span><span class="sxs-lookup"><span data-stu-id="1d8ac-135">"ICE01\\t3\\tSimple ICE to illustrating the ICE concept".</span></span>

 

 



