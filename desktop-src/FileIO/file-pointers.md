---
description: Ein Dateizeiger ist ein 64-Bit-Offset Wert, der das nächste Byte angibt, das gelesen werden soll, oder der Speicherort, an dem das nächste geschriebene Byte empfangen werden soll.
ms.assetid: 1e8bc657-affa-4a17-8435-c93de5075a1d
title: Dateizeiger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4fc804711665c045361d40c69fb71a4959b4c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215380"
---
# <a name="file-pointers"></a><span data-ttu-id="904e2-103">Dateizeiger</span><span class="sxs-lookup"><span data-stu-id="904e2-103">File Pointers</span></span>

<span data-ttu-id="904e2-104">Wenn eine Datei geöffnet wird, ordnet Windows einen *Dateizeiger* dem Standardstream zu.</span><span class="sxs-lookup"><span data-stu-id="904e2-104">When a file is opened, Windows associates a *file pointer* with the default stream.</span></span> <span data-ttu-id="904e2-105">Dieser Dateizeiger ist ein 64-Bit-Offset Wert, der das nächste Byte angibt, das gelesen werden soll, oder der Speicherort, an dem das nächste geschriebene Byte empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="904e2-105">This file pointer is a 64-bit offset value that specifies the next byte to be read or the location to receive the next byte written.</span></span> <span data-ttu-id="904e2-106">Jedes Mal, wenn eine Datei geöffnet wird, platziert das System den Dateizeiger am Anfang der Datei, der Offset 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="904e2-106">Each time a file is opened, the system places the file pointer at the beginning of the file, which is offset zero.</span></span> <span data-ttu-id="904e2-107">Jeder Lese-und Schreibvorgang verschiebt den Dateizeiger um die Anzahl der gelesenen und geschriebenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="904e2-107">Each read and write operation advances the file pointer by the number of bytes being read and written.</span></span> <span data-ttu-id="904e2-108">Wenn sich der Dateizeiger z. b. am Anfang der Datei befindet und ein Lesevorgang von 5 Bytes angefordert wird, befindet sich der Dateizeiger unmittelbar nach dem Lesevorgang am Offset 5.</span><span class="sxs-lookup"><span data-stu-id="904e2-108">For example, if the file pointer is at the beginning of the file and a read operation of 5 bytes is requested, the file pointer will be located at offset 5 immediately after the read operation.</span></span> <span data-ttu-id="904e2-109">Wenn jedes Byte gelesen oder geschrieben wird, verschiebt das System den Dateizeiger.</span><span class="sxs-lookup"><span data-stu-id="904e2-109">As each byte is read or written, the system advances the file pointer.</span></span> <span data-ttu-id="904e2-110">Der Dateizeiger kann auch durch Aufrufen der [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) -Funktion neu positioniert werden.</span><span class="sxs-lookup"><span data-stu-id="904e2-110">The file pointer can also be repositioned by calling the [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) function.</span></span>

<span data-ttu-id="904e2-111">Wenn der Dateizeiger das Ende einer Datei erreicht und die Anwendung versucht, aus der Datei zu lesen, tritt kein Fehler auf, aber es werden keine Bytes gelesen.</span><span class="sxs-lookup"><span data-stu-id="904e2-111">When the file pointer reaches the end of a file and the application attempts to read from the file, no error occurs, but no bytes are read.</span></span> <span data-ttu-id="904e2-112">Daher bedeutet das Lesen von 0 Bytes ohne Fehler, dass die Anwendung das Ende der Datei erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="904e2-112">Therefore, reading zero bytes without an error means the application has reached the end of the file.</span></span> <span data-ttu-id="904e2-113">Das Schreiben von 0 Bytes bewirkt nichts.</span><span class="sxs-lookup"><span data-stu-id="904e2-113">Writing zero bytes does nothing.</span></span>

<span data-ttu-id="904e2-114">Eine Anwendung kann eine Datei mithilfe der [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) -Funktion abschneiden oder erweitern.</span><span class="sxs-lookup"><span data-stu-id="904e2-114">An application can truncate or extend a file by using the [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) function.</span></span> <span data-ttu-id="904e2-115">Diese Funktion legt das Ende der Datei auf die aktuelle Position des Dateizeigers fest.</span><span class="sxs-lookup"><span data-stu-id="904e2-115">This function sets the end of file to the current position of the file pointer.</span></span>

 

 



