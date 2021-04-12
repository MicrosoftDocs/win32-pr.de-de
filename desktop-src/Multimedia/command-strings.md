---
title: Befehls Zeichenfolgen
description: Befehls Zeichenfolgen
ms.assetid: ca9ca153-f2bf-45ed-84e6-44e86e8efaed
keywords:
- MCI-Befehls Zeichenfolgen, Informationen zu
- MCI-Befehls Zeichenfolgen, Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b62013abff091f668a3b045e9f3ca2e8745f0d9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390152"
---
# <a name="command-strings"></a><span data-ttu-id="a5020-105">Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="a5020-105">Command Strings</span></span>

<span data-ttu-id="a5020-106">Um einen Zeichen folgen Befehl an ein MCI-Gerät zu senden, verwenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion, die Parameter für den Zeichen folgen Befehl und einen Puffer für alle zurückgegebenen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="a5020-106">To send a string command to an MCI device, use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function, which includes parameters for the string command and a buffer for any returned information.</span></span>

<span data-ttu-id="a5020-107">Die **mciSendString** -Funktion gibt bei Erfolg 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="a5020-107">The **mciSendString** function returns zero if successful.</span></span> <span data-ttu-id="a5020-108">Wenn die Funktion fehlschlägt, enthält das nieder wertige Wort des Rückgabewerts einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a5020-108">If the function fails, the low-order word of the return value contains an error code.</span></span> <span data-ttu-id="a5020-109">Sie können diesen Fehlercode an die [**mcigeterrorstring**](/previous-versions//dd757158(v=vs.85)) -Funktion übergeben, um eine Textbeschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a5020-109">You can pass this error code to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function to get a text description of the error.</span></span>

## <a name="syntax-of-command-strings"></a><span data-ttu-id="a5020-110">Syntax von Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="a5020-110">Syntax of Command Strings</span></span>

<span data-ttu-id="a5020-111">MCI-Befehls Zeichenfolgen verwenden eine konsistente Verb-Objekt-Modifier-Syntax.</span><span class="sxs-lookup"><span data-stu-id="a5020-111">MCI command strings use a consistent verb-object-modifier syntax.</span></span> <span data-ttu-id="a5020-112">Jede Befehls Zeichenfolge enthält einen Befehl, einen Geräte Bezeichner und Befehlsargumente.</span><span class="sxs-lookup"><span data-stu-id="a5020-112">Each command string includes a command, a device identifier, and command arguments.</span></span> <span data-ttu-id="a5020-113">Argumente sind für einige Befehle optional und für andere erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a5020-113">Arguments are optional for some commands and required for others.</span></span>

<span data-ttu-id="a5020-114">Eine Befehls Zeichenfolge weist die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="a5020-114">A command string has the following form:</span></span>

<span data-ttu-id="a5020-115">*Argumente der Befehls Geräte- \_ ID*</span><span class="sxs-lookup"><span data-stu-id="a5020-115">*command device\_id arguments*</span></span>

<span data-ttu-id="a5020-116">Diese Komponenten enthalten die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="a5020-116">These components contain the following information:</span></span>

-   <span data-ttu-id="a5020-117">Der *Befehl* gibt einen MCI-Befehl an, z. b. [**Öffnen**](open.md), [**Schließen**](close.md)oder [**abspielen**](play.md).</span><span class="sxs-lookup"><span data-stu-id="a5020-117">The *command* specifies an MCI command, such as [**open**](open.md), [**close**](close.md), or [**play**](play.md).</span></span>
-   <span data-ttu-id="a5020-118">Die *Geräte- \_ ID* identifiziert eine Instanz eines MCI-Treibers.</span><span class="sxs-lookup"><span data-stu-id="a5020-118">The *device\_id* identifies an instance of an MCI driver.</span></span> <span data-ttu-id="a5020-119">Die *Geräte- \_ ID* wird erstellt, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="a5020-119">The *device\_id* is created when the device is opened.</span></span>
-   <span data-ttu-id="a5020-120">Die *Argumente* geben die Flags und Variablen an, die vom Befehl verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5020-120">The *arguments* specify the flags and variables used by the command.</span></span> <span data-ttu-id="a5020-121">Flags sind Schlüsselwörter, die mit dem MCI-Befehl erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="a5020-121">Flags are keywords recognized with the MCI command.</span></span> <span data-ttu-id="a5020-122">Variablen sind Zahlen oder Zeichen folgen, die auf den MCI-Befehl oder das Flag angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5020-122">Variables are numbers or strings that apply to the MCI command or flag.</span></span>

    <span data-ttu-id="a5020-123">Beispielsweise verwendet der **Wiedergabe** Befehl die Argumente "von *Position* " und "an *Position* ", um die Positionen anzugeben, an denen der Wiedergabe-und endwiedergabe angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5020-123">For example, the **play** command uses the arguments "from *position* " and "to *position* " to indicate the positions at which to start and end play.</span></span> <span data-ttu-id="a5020-124">Sie können die Flags auflisten, die mit einem Befehl in beliebiger Reihenfolge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5020-124">You can list the flags used with a command in any order.</span></span> <span data-ttu-id="a5020-125">Wenn Sie ein Flag verwenden, dem eine Variable zugeordnet ist, müssen Sie einen Wert für die Variable angeben.</span><span class="sxs-lookup"><span data-stu-id="a5020-125">When you use a flag that has a variable associated with it, you must supply a value for the variable.</span></span>

    <span data-ttu-id="a5020-126">Nicht angegebene (und optionale) Befehlsargumente nehmen einen Standardwert an.</span><span class="sxs-lookup"><span data-stu-id="a5020-126">Unspecified (and optional) command arguments assume a default value.</span></span>

<span data-ttu-id="a5020-127">Die folgende Beispiel Funktion sendet den [**Wiedergabe**](play.md) Befehl mit den Flags "from" und "to".</span><span class="sxs-lookup"><span data-stu-id="a5020-127">The following example function sends the [**play**](play.md) command with the "from" and "to" flags.</span></span>


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



## <a name="data-types-for-command-variables"></a><span data-ttu-id="a5020-128">Datentypen für Befehls Variablen</span><span class="sxs-lookup"><span data-stu-id="a5020-128">Data Types for Command Variables</span></span>

<span data-ttu-id="a5020-129">Sie können die folgenden Datentypen für die Variablen in einer Befehls Zeichenfolge verwenden.</span><span class="sxs-lookup"><span data-stu-id="a5020-129">You can use the following data types for the variables in a command string.</span></span>



| <span data-ttu-id="a5020-130">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a5020-130">**Data type**</span></span>        | <span data-ttu-id="a5020-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a5020-131">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5020-132">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="a5020-132">Strings</span></span>              | <span data-ttu-id="a5020-133">Zeichen folgen-Datentypen sind durch führende und nachfolgende Leerzeichen und Anführungszeichen begrenzt.</span><span class="sxs-lookup"><span data-stu-id="a5020-133">String data types are delimited by leading and trailing white spaces and quotation marks.</span></span> <span data-ttu-id="a5020-134">MCI entfernt einfache Anführungszeichen aus einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a5020-134">MCI removes single quotation marks from a string.</span></span> <span data-ttu-id="a5020-135">Wenn Sie ein Anführungszeichen in eine Zeichenfolge einfügen möchten, verwenden Sie einen Satz von zwei Anführungszeichen, in dem Sie das Anführungszeichen einbetten möchten.</span><span class="sxs-lookup"><span data-stu-id="a5020-135">To put a quotation mark in a string, use a set of two quotation marks where you want to embed your quotation mark.</span></span> <span data-ttu-id="a5020-136">Um eine leere Zeichenfolge zu verwenden, verwenden Sie zwei Anführungszeichen, die durch führende und nachfolgende Leerzeichen getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="a5020-136">To use an empty string, use two quotation marks delimited by leading and trailing white spaces.</span></span> |
| <span data-ttu-id="a5020-137">Lange ganze Zahlen mit Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="a5020-137">Signed long integers</span></span> | <span data-ttu-id="a5020-138">Datentypen für ganze Zahlen mit Vorzeichen sind durch führende und nachfolgende Leerzeichen begrenzt.</span><span class="sxs-lookup"><span data-stu-id="a5020-138">Signed long integer data types are delimited by leading and trailing white spaces.</span></span> <span data-ttu-id="a5020-139">Sofern nicht anders angegeben, können ganze Zahlen positiv oder negativ sein.</span><span class="sxs-lookup"><span data-stu-id="a5020-139">Unless otherwise specified, integers can be positive or negative.</span></span> <span data-ttu-id="a5020-140">Wenn Sie negative ganze Zahlen verwenden, sollten Sie das Minuszeichen und die erste Ziffer nicht durch ein Leerzeichen trennen.</span><span class="sxs-lookup"><span data-stu-id="a5020-140">If you use negative integers, you should not separate the minus sign and the first digit with a space.</span></span>                                                                                                    |
| <span data-ttu-id="a5020-141">Rechtecke</span><span class="sxs-lookup"><span data-stu-id="a5020-141">Rectangles</span></span>           | <span data-ttu-id="a5020-142">Rechteck Datentypen sind eine geordnete Liste von vier signierten kurzwerten.</span><span class="sxs-lookup"><span data-stu-id="a5020-142">Rectangle data types are an ordered list of four signed short values.</span></span> <span data-ttu-id="a5020-143">Leerraum begrenzt diesen Datentyp und trennt jede Ganzzahl in der Liste.</span><span class="sxs-lookup"><span data-stu-id="a5020-143">White space delimits this data type and separates each integer in the list.</span></span>                                                                                                                                                                                                              |



 

 

 