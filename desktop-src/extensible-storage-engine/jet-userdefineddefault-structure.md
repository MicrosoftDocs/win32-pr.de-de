---
description: 'Weitere Informationen finden Sie hier: JET_USERDEFINEDDEFAULT Struktur'
title: JET_USERDEFINEDDEFAULT Struktur
TOCTitle: JET_USERDEFINEDDEFAULT Structure
ms:assetid: 1f0a5419-9fae-4a93-a271-2f9772ecc996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269200(v=EXCHG.10)
ms:contentKeyID: 32765503
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5f588588a1a6769e997264321f8911a86e169c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355387"
---
# <a name="jet_userdefineddefault-structure"></a><span data-ttu-id="3e863-103">JET_USERDEFINEDDEFAULT Struktur</span><span class="sxs-lookup"><span data-stu-id="3e863-103">JET_USERDEFINEDDEFAULT Structure</span></span>


<span data-ttu-id="3e863-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3e863-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_userdefineddefault-structure"></a><span data-ttu-id="3e863-105">JET_USERDEFINEDDEFAULT Struktur</span><span class="sxs-lookup"><span data-stu-id="3e863-105">JET_USERDEFINEDDEFAULT Structure</span></span>

<span data-ttu-id="3e863-106">Die **JET_USERDEFINEDDEFAULT** Struktur wird in Verbindung mit JET_bitColumnUserDefinedDefault angegeben, um einer neuen Spalte einen Standardwert zu übergeben, der mithilfe eines Rückrufs bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="3e863-106">The **JET_USERDEFINEDDEFAULT** structure is specified in conjunction with JET_bitColumnUserDefinedDefault to give a new column a default value that is determined using a callback.</span></span> <span data-ttu-id="3e863-107">Diese Technik kann zum Implementieren berechneter Spalten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e863-107">This technique can be used to implement computed columns.</span></span>

<span data-ttu-id="3e863-108">**Windows XP:** Die **JET_USERDEFINEDDEFAULT** Struktur wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3e863-108">**Windows XP:** The **JET_USERDEFINEDDEFAULT** structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct tag_JET_USERDEFINEDDEFAULT {
      tchar* szCallback;
      unsigned char* pbUserData;
      unsigned long cbUserData;
      tchar* szDependantColumns;
    } JET_USERDEFINEDDEFAULT;
```

### <a name="members"></a><span data-ttu-id="3e863-109">Member</span><span class="sxs-lookup"><span data-stu-id="3e863-109">Members</span></span>

<span data-ttu-id="3e863-110">**szcallback**</span><span class="sxs-lookup"><span data-stu-id="3e863-110">**szCallback**</span></span>

<span data-ttu-id="3e863-111">Der Export Name der Funktion, die den Rückruf im Format "Modul \! Funktion" implementiert.</span><span class="sxs-lookup"><span data-stu-id="3e863-111">The export name of the function that implements the callback in "module\!function" format.</span></span>

<span data-ttu-id="3e863-112">Der Rückruf wird als Teil des Spalten Schemas beibehalten.</span><span class="sxs-lookup"><span data-stu-id="3e863-112">The callback persists as a part of the column schema.</span></span> <span data-ttu-id="3e863-113">Die tatsächliche ausführbare Hostdatei und der Export Name der Funktion müssen persistent gespeichert werden, um die Suche nach der tatsächlichen Adresse der Funktion zur Laufzeit zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3e863-113">The actual host executable and export name of the function must persist to enable the lookup of the true address of the function at run time.</span></span>

<span data-ttu-id="3e863-114">Der Modulname ist der Name der Host Binärdatei, die die Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="3e863-114">The module name is the name of the host binary that contains the function.</span></span> <span data-ttu-id="3e863-115">Der Name der Funktion ist der Name des Exports für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="3e863-115">The function name is the name of the export for that function.</span></span> <span data-ttu-id="3e863-116">Diese beiden Informationen werden von der Datenbank-Engine zur Laufzeit verwendet, um die tatsächliche Adresse des Rückrufs zu ermitteln, indem Sie einen [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Befehl für den Modulnamen gefolgt von einem [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Aufrufs für den Funktionsnamen ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e863-116">These two pieces of information will be used by the database engine at runtime to locate the true address of the callback by executing a [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) call on the module name followed by a [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) call on the function name.</span></span>

<span data-ttu-id="3e863-117">Wenn der Rückruf z. b. in einer DLL mit dem Namen MyCallback.DLL implementiert wurde und diese DLL in C: \\ MyApplication gespeichert wurde und die Funktion, die den Rückruf implementiert, als userdefineddefaultcallback von der dll exportiert wurde, lautet die erforderliche Zeichenfolge "C: \\ MyApplication \\MyCallback.DLL\! userdefineddefaultcallback".</span><span class="sxs-lookup"><span data-stu-id="3e863-117">For example, if the callback were implemented in a DLL called MyCallback.DLL and that DLL were stored in C:\\MyApplication and the function implementing the callback were exported from the DLL as UserDefinedDefaultCallback, then the required string would be "C:\\MyApplication\\MyCallback.DLL\!UserDefinedDefaultCallback".</span></span>

<span data-ttu-id="3e863-118">**Hinweis**  Eingebettet " \! "</span><span class="sxs-lookup"><span data-stu-id="3e863-118">**Note**  Embedded "\!"</span></span> <span data-ttu-id="3e863-119">Zeichen im Modulteil des Rückruf namens werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3e863-119">characters in the module portion of the callback name are not supported.</span></span>

<span data-ttu-id="3e863-120">Es wird dringend empfohlen, einen Rückruf Namen zu verwenden, der keine Funktion der Host Architektur ist.</span><span class="sxs-lookup"><span data-stu-id="3e863-120">It is highly recommended that you use a callback name that is not a function of the host architecture.</span></span> <span data-ttu-id="3e863-121">Verwenden Sie beispielsweise keine als stdcall () ergänzten Exporte, UserDefinedDefaultCallback@32 da diese Aufruf Konvention nur auf x86-Computern unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3e863-121">For example, do not use exports decorated as stdcall (UserDefinedDefaultCallback@32) because this calling convention is only supported on x86 machines.</span></span> <span data-ttu-id="3e863-122">Wenn ein solcher Rückruf verwendet wurde, konnte die Datenbank nur auf einem x86-Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e863-122">If such a callback were used then the database could only be used on an x86 machine.</span></span> <span data-ttu-id="3e863-123">Ein Alias sollte in diesem Fall verwendet werden, um einen plattformunabhängigen Export vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="3e863-123">An alias should be used to make a platform-agnostic export in this case.</span></span>

<span data-ttu-id="3e863-124">Es wird dringend empfohlen, dass Sie den vollständigen Pfad des Modul namens verwenden, der den Rückruf implementiert.</span><span class="sxs-lookup"><span data-stu-id="3e863-124">It is highly recommended that you use the full path of the module name that is implementing the callback.</span></span> <span data-ttu-id="3e863-125">Wenn ein relativer Pfad verwendet wird, kann der Prozess, der die Datenbank gehostet, anfällig für Angriffe durch eine nicht autorisierte Binärdatei sein.</span><span class="sxs-lookup"><span data-stu-id="3e863-125">If a relative path is used then the process that is hosting the database might be susceptible to attack by a rogue binary.</span></span>

<span data-ttu-id="3e863-126">Die Anwendung sollte nur vertrauenswürdige Rückrufe an die Datenbank-Engine übergeben.</span><span class="sxs-lookup"><span data-stu-id="3e863-126">The application should pass only trusted callbacks to the database engine.</span></span> <span data-ttu-id="3e863-127">Die Datenbank-Engine lädt die Binärdatei, um deren vorhanden sein zu überprüfen, wenn die zugehörige Spalte erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3e863-127">The database engine will load the binary to verify its existence when the associated column is created.</span></span> <span data-ttu-id="3e863-128">Wenn der Pfad zur Binärdatei nicht überprüft wird oder bekannt ist, dass Sie vertrauenswürdig ist, könnte Sie den Prozess angreifen, der die Datenbank gehostet.</span><span class="sxs-lookup"><span data-stu-id="3e863-128">If the path to the binary is not validated or known to be trusted then it could attack the process that is hosting the database.</span></span>

<span data-ttu-id="3e863-129">**pbuserdata**</span><span class="sxs-lookup"><span data-stu-id="3e863-129">**pbUserData**</span></span>

<span data-ttu-id="3e863-130">Ein eigenständiger Block von benutzerdefinierten Daten, die beim Aufrufen an den Rückruf übermittelt werden sollen. Der bereitgestellte Datenblock wird als Teil des Spalten Schemas beibehalten.</span><span class="sxs-lookup"><span data-stu-id="3e863-130">A self-contained block of user-defined data to be passed to the callback when invoked.The data block that is provided will persist as a part of the column schema.</span></span> <span data-ttu-id="3e863-131">Folglich muss der Datenblock vollständig eigenständig sein und kann nicht auf Daten verweisen, die sich außerhalb des Gültigkeits Bereichs der Datenbank befinden.</span><span class="sxs-lookup"><span data-stu-id="3e863-131">As a result, the data block must be entirely self-contained and cannot refer to any data that is outside the scope of the database.</span></span>

<span data-ttu-id="3e863-132">Wenn **pbuserdata** NULL ist, wird der Wert von **cbUserData** ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3e863-132">If **pbUserData** is zero then the value of **cbUserData** is ignored.</span></span> <span data-ttu-id="3e863-133">In diesem Fall werden keine benutzerdefinierten Daten an den Rückruf übermittelt, wenn Sie aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3e863-133">In this case, no user-defined data will be passed to the callback when invoked.</span></span>

<span data-ttu-id="3e863-134">**cbUserData**</span><span class="sxs-lookup"><span data-stu-id="3e863-134">**cbUserData**</span></span>

<span data-ttu-id="3e863-135">Siehe **pbuserdata**.</span><span class="sxs-lookup"><span data-stu-id="3e863-135">See **pbUserData**.</span></span>

<span data-ttu-id="3e863-136">**szdependantcolumns**</span><span class="sxs-lookup"><span data-stu-id="3e863-136">**szDependantColumns**</span></span>

<span data-ttu-id="3e863-137">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3e863-137">Reserved for future use.</span></span>

<span data-ttu-id="3e863-138">Dieser Member sollte immer auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3e863-138">This member should always be set to NULL.</span></span>

### <a name="requirements"></a><span data-ttu-id="3e863-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e863-139">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e863-140"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3e863-140"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3e863-141">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3e863-141">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e863-142"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3e863-142"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3e863-143">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3e863-143">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e863-144"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="3e863-144"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3e863-145">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="3e863-145">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e863-146"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="3e863-146"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="3e863-147">Wird als <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) und <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="3e863-147">Implemented as <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) and <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="3e863-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3e863-148">See Also</span></span>

[<span data-ttu-id="3e863-149">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="3e863-149">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="3e863-150">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="3e863-150">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="3e863-151">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="3e863-151">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)
