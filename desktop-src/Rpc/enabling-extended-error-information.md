---
title: Aktivieren erweiterter Fehlerinformationen
description: Erweiterte Fehlerinformationen für Remote Prozedur Aufruf (RPC) werden aktiviert.
ms.assetid: 73b72d0a-8533-40ac-8b41-8af4d60f9631
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd6579069c840d8f6dba5a9cd0e0d4edc831f6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207017"
---
# <a name="enabling-extended-error-information"></a><span data-ttu-id="25549-103">Aktivieren erweiterter Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="25549-103">Enabling Extended Error Information</span></span>

<span data-ttu-id="25549-104">Führen Sie die folgenden Schritte aus, um erweiterte Fehlerinformationen zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="25549-104">To enable extended error information, take the following steps:</span></span>

<span data-ttu-id="25549-105">Öffnen Sie die Richtlinie für den lokalen Computer mithilfe der Schnittstelle gpeer dit. msc.</span><span class="sxs-lookup"><span data-stu-id="25549-105">Open the local machine policy using the gpedit.msc interface.</span></span>

<span data-ttu-id="25549-106">Navigieren Sie zu der Richtlinie, die unter Computer Konfiguration/administrative Vorlagen/System/remote Prozedur Aufruf/RPC-Problembehandlung bei der Problembehandlung/Weitergabe erweiterter Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="25549-106">Navigate to the policy located at Computer Configuration/Administrative Templates/System/Remote Procedure Call/Rpc Troubleshooting Support/Propagation of extended error information</span></span>

<span data-ttu-id="25549-107">Aktivieren Sie die Richtlinie, und legen Sie die Feld Weitergabe **Erweiterter Fehlerinformationen** auf "on" fest.</span><span class="sxs-lookup"><span data-stu-id="25549-107">Enable the policy, and set the field **Propagation of extended error information** to "On".</span></span>

<span data-ttu-id="25549-108">Durch diesen Vorgang wird die Weitergabe erweiterter Fehlerinformationen für alle Prozesse auf dem Computer eingeschaltet.</span><span class="sxs-lookup"><span data-stu-id="25549-108">This process turns the propagation of extended error information on for all processes on the machine.</span></span>

<span data-ttu-id="25549-109">Um erweiterte Fehlerinformationen nur für bestimmte Prozesse auf einem Computer zu aktivieren oder um nur bestimmte Prozesse auf dem Computer zu deaktivieren, verwenden Sie die Optionen **off with Exceptions** oder **on with Exceptions** .</span><span class="sxs-lookup"><span data-stu-id="25549-109">To enable extended error information for only certain processes on a computer, or to disable it for only certain processes on the computer, use the **Off with exceptions** or **On with exceptions** options.</span></span> <span data-ttu-id="25549-110">Beide Optionen verwenden das Feld **Erweiterte Fehler Informations Ausnahmen** , um anzugeben, welche Prozesse die Standardeinstellung aufweisen und welche Prozesse das Gegenteil der Standardeinstellung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="25549-110">Both options use the field **Extended Error Information Exceptions** to specify which processes have the default setting, and which processes have the opposite of the default setting.</span></span> <span data-ttu-id="25549-111">**Ausnahmen für erweiterte Fehlerinformationen** enthalten eine Liste von Prozessnamen.</span><span class="sxs-lookup"><span data-stu-id="25549-111">**Extended Error Information Exceptions** contains a list of process names.</span></span>

<span data-ttu-id="25549-112">Wenn die Befehlszeile eines Prozesses mit einer Zeichenfolge beginnt, die in den **erweiterten Fehler Informations Ausnahmen** vorliegt, empfängt der Prozess das Gegenteil der Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="25549-112">If the command line of a process starts with a string that is in the **Extended Error Information Exceptions**, the process will receive the opposite of the default setting.</span></span> <span data-ttu-id="25549-113">Wenn Sie z. b. möchten, dass der gesamte Prozess auf dem Computer erweiterte Fehlerinformationen (mit Ausnahme von LSASS) und den Prozess mit dem Namen **Secure Server** weitergibt, legen Sie die Weitergabe **Erweiterter Fehlerinformationen** **auf mit Ausnahmen** fest, und geben Sie im Feld **Erweiterte Fehler Informations Ausnahmen** die folgende Zeichenfolge ein: LSASS "Secure Server".</span><span class="sxs-lookup"><span data-stu-id="25549-113">For example, if you want all the process on your computer to propagate extended error information, except for lsass and the process called **Secure Server**, set the **Propagation of extended error information** to **On with exceptions**, and specify in the **Extended Error Information Exceptions** field the following string: lsass "Secure Server".</span></span>

<span data-ttu-id="25549-114">Zeichen folgen können in doppelte Anführungszeichen eingeschlossen werden. Dies ist jedoch optional, wenn die Zeichenfolge keine Leerzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="25549-114">Strings can be enclosed with double quotes, but doing so is optional if there are no spaces in the string.</span></span> <span data-ttu-id="25549-115">Außerdem kann der Anfang der Verarbeitungs Befehlszeile angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="25549-115">Also, the beginning of the process command line can be specified.</span></span> <span data-ttu-id="25549-116">Wenn beispielsweise in der Weitergabe **von erweiterten Fehlerinformationen** das Feld **aus mit Ausnahmen** angegeben wird und im Feld **Ausnahmen für erweiterte Fehlerinformationen** Folgendes angegeben ist: Win.</span><span class="sxs-lookup"><span data-stu-id="25549-116">For example, if **Off with exceptions** is specified in the **Propagation of extended error information** field, and in the **Extended Error Information Exceptions** field the following is specified: win.</span></span>

<span data-ttu-id="25549-117">Jeder Prozess, der mit "Win" beginnt, überträgt erweiterte Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="25549-117">Each process that begins with "win" propagates extended error information.</span></span> <span data-ttu-id="25549-118">Auf vielen Computern werden diese Prozesse beispielsweise winlogon.exe und WINWORD.EXE.</span><span class="sxs-lookup"><span data-stu-id="25549-118">On many computers, for example, those processes would be winlogon.exe and WINWORD.EXE.</span></span>

 

 




