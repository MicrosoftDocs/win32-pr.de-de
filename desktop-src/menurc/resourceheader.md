---
title: Resourceheader-Struktur
description: Enthält Informationen über den Ressourcen Header selbst und die Daten, die für diese Ressource spezifisch sind.
ms.assetid: e0eba7b3-a275-4ffe-9347-46361213cf48
keywords:
- Resourceheader-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- RESOURCEHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41b436ebd6aeb5dc31f8ed773fbe7b12a1586185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342188"
---
# <a name="resourceheader-structure"></a><span data-ttu-id="94a5b-104">Resourceheader-Struktur</span><span class="sxs-lookup"><span data-stu-id="94a5b-104">RESOURCEHEADER structure</span></span>

<span data-ttu-id="94a5b-105">Enthält Informationen über den Ressourcen Header selbst und die Daten, die für diese Ressource spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="94a5b-105">Contains information about the resource header itself and the data specific to this resource.</span></span> <span data-ttu-id="94a5b-106">Diese Struktur ist keine echte C-Sprachstruktur, da Sie Member variabler Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="94a5b-106">This structure is not a true C-language structure, because it contains variable-length members.</span></span> <span data-ttu-id="94a5b-107">Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="94a5b-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="94a5b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="94a5b-108">Syntax</span></span>


```C++
typedef struct {
  DWORD DataSize;
  DWORD HeaderSize;
  DWORD TYPE;
  DWORD NAME;
  DWORD DataVersion;
  WORD  MemoryFlags;
  WORD  LanguageId;
  DWORD Version;
  DWORD Characteristics;
} RESOURCEHEADER;
```



## <a name="members"></a><span data-ttu-id="94a5b-109">Member</span><span class="sxs-lookup"><span data-stu-id="94a5b-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="94a5b-110">**DataSize**</span><span class="sxs-lookup"><span data-stu-id="94a5b-110">**DataSize**</span></span>
</dt> <dd>

<span data-ttu-id="94a5b-111">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="94a5b-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="94a5b-112">Die Größe (in Bytes) der Daten, die dem Ressourcen Header für diese bestimmte Ressource folgen.</span><span class="sxs-lookup"><span data-stu-id="94a5b-112">The size, in bytes, of the data that follows the resource header for this particular resource.</span></span> <span data-ttu-id="94a5b-113">Es enthält keine Datei Auffüll Zeichen zwischen dieser Ressource und einer beliebigen Ressource in der Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="94a5b-113">It does not include any file padding between this resource and any resource that follows it in the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="94a5b-114">**HeaderSize**</span><span class="sxs-lookup"><span data-stu-id="94a5b-114">**HeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="94a5b-115">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="94a5b-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="94a5b-116">Die Größe der folgenden Ressourcen Header Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="94a5b-116">The size, in bytes, of the resource header data that follows.</span></span>

</dd> <dt>

<span data-ttu-id="94a5b-117">**TYPE**</span><span class="sxs-lookup"><span data-stu-id="94a5b-117">**TYPE**</span></span>
</dt> <dd>

<span data-ttu-id="94a5b-118">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="94a5b-118">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="94a5b-119">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="94a5b-119">The resource type.</span></span> <span data-ttu-id="94a5b-120">Der **Typmember** kann entweder ein numerischer Wert oder eine auf NULL endende Unicode-Zeichenfolge sein, die den Namen des Typs angibt.</span><span class="sxs-lookup"><span data-stu-id="94a5b-120">The **TYPE** member can either be a numeric value or a null-terminated Unicode string that specifies the name of the type.</span></span> <span data-ttu-id="94a5b-121">Im folgenden Abschnitt "Hinweise" finden Sie eine Beschreibung der Member des Typs " **Name** " oder " **Ordinal** ".</span><span class="sxs-lookup"><span data-stu-id="94a5b-121">See the following Remarks section for a description of **Name** or **Ordinal** type members.</span></span>

<span data-ttu-id="94a5b-122">Wenn der **Typmember** ein numerischer Wert ist, kann er entweder einen Standard-oder einen benutzerdefinierten Ressourcentyp angeben.</span><span class="sxs-lookup"><span data-stu-id="94a5b-122">If the **TYPE** member is a numeric value, it can specify either a standard or a user-defined resource type.</span></span> <span data-ttu-id="94a5b-123">Wenn der Member eine Zeichenfolge ist, ist es ein benutzerdefinierter Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="94a5b-123">If the member is a string, then it is a user-defined resource type.</span></span> <span data-ttu-id="94a5b-124">Eine Liste der vordefinierten Ressourcentypen finden Sie unter [Ressourcentypen](/windows/desktop/menurc/resource-types).</span><span class="sxs-lookup"><span data-stu-id="94a5b-124">For a list of the predefined resource types, see [Resource Types](/windows/desktop/menurc/resource-types).</span></span>

<span data-ttu-id="94a5b-125">Werte kleiner als 256 sind für die Verwendung durch das System reserviert.</span><span class="sxs-lookup"><span data-stu-id="94a5b-125">Values less than 256 are reserved for system use.</span></span>

</dd> <dt>

<span data-ttu-id="94a5b-126">**NAME**</span><span class="sxs-lookup"><span data-stu-id="94a5b-126">**NAME**</span></span>
</dt> <dd>

<span data-ttu-id="94a5b-127">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="94a5b-127">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="94a5b-128">Ein Name, der die jeweilige Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="94a5b-128">A name that identifies the particular resource.</span></span> <span data-ttu-id="94a5b-129">Das **Name** -Element kann wie der **Typmember** entweder ein numerischer Wert oder eine auf NULL endende Unicode-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="94a5b-129">The **NAME** member, like the **TYPE** member, can either be a numeric value or a null-terminated Unicode string.</span></span> <span data-ttu-id="94a5b-130">Im folgenden Abschnitt "Hinweise" finden Sie eine Beschreibung der Member des Typs " **Name** " oder " **Ordinal** ".</span><span class="sxs-lookup"><span data-stu-id="94a5b-130">See the following Remarks section for a description of **Name** or **Ordinal** type members.</span></span>

<span data-ttu-id="94a5b-131">Sie müssen keine Auffüll Zeichen für die **DWORD** -Ausrichtung zwischen den **Typen** -und **namens** Elementen hinzufügen, da Sie **Word** -Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="94a5b-131">You do not need to add padding for **DWORD** alignment between the **TYPE** and **NAME** members because they contain **WORD** data.</span></span> <span data-ttu-id="94a5b-132">Sie müssen jedoch möglicherweise nach dem **Name** -Element ein **Wort** zum Auffüllen hinzufügen, um den Rest des Headers an **DWORD** -Grenzen auszurichten.</span><span class="sxs-lookup"><span data-stu-id="94a5b-132">However, you may need to add a **WORD** of padding after the **NAME** member to align the rest of the header on **DWORD** boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="94a5b-133">**DataVersion**</span><span class="sxs-lookup"><span data-stu-id="94a5b-133">**DataVersion**</span></span>
</dt> <dd>

<span data-ttu-id="94a5b-134">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="94a5b-134">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="94a5b-135">Eine vordefinierte Ressourcen Daten Version.</span><span class="sxs-lookup"><span data-stu-id="94a5b-135">A predefined resource data version.</span></span> <span data-ttu-id="94a5b-136">Dadurch wird festgelegt, welche Version der Ressourcen Daten von der Anwendung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="94a5b-136">This will determine which version of the resource data the application should use.</span></span>

</dd> <dt>

<span data-ttu-id="94a5b-137">**Memoryflags**</span><span class="sxs-lookup"><span data-stu-id="94a5b-137">**MemoryFlags**</span></span>
</dt> <dd>

<span data-ttu-id="94a5b-138">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="94a5b-138">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="94a5b-139">Ein Satz von Attributflags, die den Zustand der Ressource beschreiben können.</span><span class="sxs-lookup"><span data-stu-id="94a5b-139">A set of attribute flags that can describe the state of the resource.</span></span> <span data-ttu-id="94a5b-140">Modifiziererer in. RC-Skriptdatei weisen Sie diese Attribute der Ressource zu.</span><span class="sxs-lookup"><span data-stu-id="94a5b-140">Modifiers in the .RC script file assign these attributes to the resource.</span></span> <span data-ttu-id="94a5b-141">Die Skript Bezeichner können die folgenden Flagwerte zuweisen.</span><span class="sxs-lookup"><span data-stu-id="94a5b-141">The script identifiers can assign the following flag values.</span></span>

<span data-ttu-id="94a5b-142">Anwendungen verwenden keines dieser Attribute.</span><span class="sxs-lookup"><span data-stu-id="94a5b-142">Applications do not use any of these attributes.</span></span> <span data-ttu-id="94a5b-143">Die Attribute sind im Skript für die Abwärtskompatibilität mit vorhandenen Skripts zulässig, werden jedoch ignoriert.</span><span class="sxs-lookup"><span data-stu-id="94a5b-143">The attributes are permitted in the script for backward compatibility with existing scripts, but they are ignored.</span></span> <span data-ttu-id="94a5b-144">Ressourcen werden geladen, wenn das entsprechende Modul geladen wird, und werden freigegeben, wenn das Modul entladen wird.</span><span class="sxs-lookup"><span data-stu-id="94a5b-144">Resources are loaded when the corresponding module is loaded, and are freed when the module is unloaded.</span></span>

<dt>

<span id="MOVEABLE"></span><span id="moveable"></span>

<span data-ttu-id="94a5b-145">**Verschiebbare** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="94a5b-145">**MOVEABLE** (0x0010)</span></span>


</dt> <dd></dd> <dt>

<span id="FIXED"></span><span id="fixed"></span>

<span data-ttu-id="94a5b-146">**korrigiert** (~-fähig)</span><span class="sxs-lookup"><span data-stu-id="94a5b-146">**FIXED** (~MOVEABLE)</span></span>


</dt> <dd></dd> <dt>

<span id="PURE"></span><span id="pure"></span>

<span data-ttu-id="94a5b-147">**Pure** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="94a5b-147">**PURE** (0x0020)</span></span>


</dt> <dd></dd> <dt>

<span id="IMPURE"></span><span id="impure"></span>

<span data-ttu-id="94a5b-148">**Impure** (~ Pure)</span><span class="sxs-lookup"><span data-stu-id="94a5b-148">**IMPURE** (~PURE)</span></span>


</dt> <dd></dd> <dt>

<span id="PRELOAD"></span><span id="preload"></span>

<span data-ttu-id="94a5b-149">**Vorab laden** (0x0040)</span><span class="sxs-lookup"><span data-stu-id="94a5b-149">**PRELOAD** (0x0040)</span></span>


</dt> <dd></dd> <dt>

<span id="LOADONCALL"></span><span id="loadoncall"></span>

<span data-ttu-id="94a5b-150">**LOADONCALL(** ~ preload)</span><span class="sxs-lookup"><span data-stu-id="94a5b-150">**LOADONCALL** (~PRELOAD)</span></span>


</dt> <dd></dd> <dt>

<span id="DISCARDABLE"></span><span id="discardable"></span>

<span data-ttu-id="94a5b-151">**Verwerfen** (0x1000)</span><span class="sxs-lookup"><span data-stu-id="94a5b-151">**DISCARDABLE** (0x1000)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="94a5b-152">**LanguageID**</span><span class="sxs-lookup"><span data-stu-id="94a5b-152">**LanguageId**</span></span>
</dt> <dd>

<span data-ttu-id="94a5b-153">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="94a5b-153">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="94a5b-154">Die Sprache für die Ressource oder den Satz von Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="94a5b-154">The language for the resource or set of resources.</span></span> <span data-ttu-id="94a5b-155">Legen Sie den Wert für diesen Member mit der optionalen [Language](./language-statement.md) Resource Definition-Anweisung fest.</span><span class="sxs-lookup"><span data-stu-id="94a5b-155">Set the value for this member with the optional [LANGUAGE](./language-statement.md) resource definition statement.</span></span> <span data-ttu-id="94a5b-156">Die Parameter sind Konstanten aus der Datei "Winnt. h".</span><span class="sxs-lookup"><span data-stu-id="94a5b-156">The parameters are constants from the Winnt.h file.</span></span>

<span data-ttu-id="94a5b-157">Jede Ressource enthält eine sprach Kennung, damit das System oder die Anwendung eine Sprache auswählen kann, die für das aktuelle Gebiets Schema des Systems geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="94a5b-157">Each resource includes a language identifier so the system or application can select a language appropriate for the current locale of the system.</span></span> <span data-ttu-id="94a5b-158">Wenn mehrere Ressourcen desselben Typs und Namens vorhanden sind, die sich nur in der Sprache der Zeichen folgen innerhalb der Ressourcen unterscheiden, müssen Sie für jeden eine **LanguageID** angeben.</span><span class="sxs-lookup"><span data-stu-id="94a5b-158">If there are multiple resources of the same type and name that differ only in the language of the strings within the resources, you will need to specify a **LanguageId** for each one.</span></span>

</dd> <dt>

<span data-ttu-id="94a5b-159">**Version**</span><span class="sxs-lookup"><span data-stu-id="94a5b-159">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="94a5b-160">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="94a5b-160">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="94a5b-161">Eine benutzerdefinierte Versionsnummer für die Ressourcen Daten, die Tools zum Lesen und Schreiben von Ressourcen Dateien verwenden können.</span><span class="sxs-lookup"><span data-stu-id="94a5b-161">A user-defined version number for the resource data that tools can use to read and write resource files.</span></span> <span data-ttu-id="94a5b-162">Legen Sie diesen Wert mit der optionalen [Version](./version-statement.md) Resource Definition-Anweisung fest.</span><span class="sxs-lookup"><span data-stu-id="94a5b-162">Set this value with the optional [VERSION](./version-statement.md) resource definition statement.</span></span>

</dd> <dt>

<span data-ttu-id="94a5b-163">**Characteristics**</span><span class="sxs-lookup"><span data-stu-id="94a5b-163">**Characteristics**</span></span>
</dt> <dd>

<span data-ttu-id="94a5b-164">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="94a5b-164">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="94a5b-165">Gibt benutzerdefinierte Informationen über die Ressource an, die Tools zum Lesen und Schreiben von Ressourcen Dateien verwenden können.</span><span class="sxs-lookup"><span data-stu-id="94a5b-165">Specifies user-defined information about the resource that tools can use to read and write resource files.</span></span> <span data-ttu-id="94a5b-166">Legen Sie diesen Wert mit der optionalen [Merkmale](./characteristics-statement.md) Resource Definition-Anweisung fest.</span><span class="sxs-lookup"><span data-stu-id="94a5b-166">Set this value with the optional [CHARACTERISTICS](./characteristics-statement.md) resource definition statement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94a5b-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94a5b-167">Remarks</span></span>

<span data-ttu-id="94a5b-168">Ein variablentypmember wird als **Name** oder **ordinalmember** bezeichnet und wird an den meisten Stellen in der Ressourcen Datei verwendet, in der ein Bezeichner angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="94a5b-168">A variable type member is called a **Name** or **Ordinal** member, and it is used in most places in the resource file where an identifier appears.</span></span> <span data-ttu-id="94a5b-169">Das erste **Wort** eines **namens** oder eines **ordinaltypmembers** gibt an, ob der Member ein numerischer Wert oder eine Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="94a5b-169">The first **WORD** of a **Name** or **Ordinal** type member indicates whether the member is a numeric value or a string.</span></span> <span data-ttu-id="94a5b-170">Wenn das erste **Wort** im Member gleich dem Wert 0xFFFF ist, bei dem es sich um ein ungültiges Unicode-Zeichen handelt, ist das folgende **Wort** eine Typnummer.</span><span class="sxs-lookup"><span data-stu-id="94a5b-170">If the first **WORD** in the member is equal to the value 0xffff, which is an invalid Unicode character, then the following **WORD** is a type number.</span></span> <span data-ttu-id="94a5b-171">Andernfalls enthält der Member eine Unicode-Zeichenfolge, und das erste **Wort** im Member ist das erste Zeichen in der namens Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="94a5b-171">Otherwise, the member contains a Unicode string and the first **WORD** in the member is the first character in the name string.</span></span> <span data-ttu-id="94a5b-172">Weitere Informationen zu Ressourcen Definitions Anweisungen finden Sie unter [Ressourcen Definitions Anweisungen](./resource-definition-statements.md).</span><span class="sxs-lookup"><span data-stu-id="94a5b-172">For additional information about resource definition statements, see [Resource-Definition Statements](./resource-definition-statements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94a5b-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94a5b-173">Requirements</span></span>



| <span data-ttu-id="94a5b-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94a5b-174">Requirement</span></span> | <span data-ttu-id="94a5b-175">Wert</span><span class="sxs-lookup"><span data-stu-id="94a5b-175">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="94a5b-176">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94a5b-176">Minimum supported client</span></span><br/> | <span data-ttu-id="94a5b-177">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94a5b-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="94a5b-178">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94a5b-178">Minimum supported server</span></span><br/> | <span data-ttu-id="94a5b-179">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94a5b-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="94a5b-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94a5b-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="94a5b-181">**Licher**</span><span class="sxs-lookup"><span data-stu-id="94a5b-181">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="94a5b-182">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="94a5b-182">Resources</span></span>](resources.md)
</dt> <dt>

<span data-ttu-id="94a5b-183">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="94a5b-183">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="94a5b-184">Merkmale-Anweisung</span><span class="sxs-lookup"><span data-stu-id="94a5b-184">CHARACTERISTICS Statement</span></span>](./characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="94a5b-185">Language-Anweisung</span><span class="sxs-lookup"><span data-stu-id="94a5b-185">LANGUAGE Statement</span></span>](./language-statement.md)
</dt> <dt>

[<span data-ttu-id="94a5b-186">Versions Anweisung</span><span class="sxs-lookup"><span data-stu-id="94a5b-186">VERSION Statement</span></span>](./version-statement.md)
</dt> </dl>

 

