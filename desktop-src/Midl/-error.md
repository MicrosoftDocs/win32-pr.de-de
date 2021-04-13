---
title: /Error-Schalter
description: Der Schalter/Error bestimmt die Typen der Fehlerüberprüfung, die von den generierten stubvorschauen zur Laufzeit ausgeführt werden.
ms.assetid: abd3616a-2d2c-4a7d-bf3a-c84a43387894
keywords:
- /Error-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84a56c1ae3d57ab1931ec175aa8dc9010ea6b8a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389259"
---
# <a name="error-switch"></a><span data-ttu-id="aeb94-104">/Error-Schalter</span><span class="sxs-lookup"><span data-stu-id="aeb94-104">/error switch</span></span>

<span data-ttu-id="aeb94-105">Der Schalter **/Error** bestimmt die Typen der Fehlerüberprüfung, die von den generierten stubvorschauen zur Laufzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="aeb94-105">The **/error** switch determines the types of error checking that the generated stubs will perform at run time.</span></span>

> [!Note]  
> <span data-ttu-id="aeb94-106">Diese Funktion ist veraltet und wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aeb94-106">This feature is obsolete and no longer supported.</span></span> <span data-ttu-id="aeb94-107">Die Verwendung des [**/robust**](-robust.md) -Schalters wird empfohlen.</span><span class="sxs-lookup"><span data-stu-id="aeb94-107">The use of the [**/robust**](-robust.md) switch is recommended.</span></span>

 

``` syntax
midl /error { allocation | stub_data | ref | bounds_check | none | all }
```

## <a name="switch-options"></a><span data-ttu-id="aeb94-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="aeb94-108">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="allocation"></span><span id="ALLOCATION"></span>

<span data-ttu-id="aeb94-109"><span id="allocation"></span><span id="ALLOCATION"></span>Zuordnung \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="aeb94-109"><span id="allocation"></span><span id="ALLOCATION"></span>\*\*\*\*allocation\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="aeb94-110">Überprüft, ob der Wert für die [**mittlere \_ Benutzer \_ Zuteilung**](midl-user-allocate-1.md) einen **null** -Wert zurückgibt, der auf einen Fehler wegen nicht genügend Arbeitsspeichers hinweist.</span><span class="sxs-lookup"><span data-stu-id="aeb94-110">Checks whether [**midl\_user\_allocate**](midl-user-allocate-1.md) returns a **NULL** value, indicating an out-of-memory error.</span></span>

</dd> <dt>

<span id="stub_data"></span><span id="STUB_DATA"></span>

<span data-ttu-id="aeb94-111"><span id="stub_data"></span><span id="STUB_DATA"></span>Stub- \_ Daten \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="aeb94-111"><span id="stub_data"></span><span id="STUB_DATA"></span>\*\*\*\*stub\_data\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="aeb94-112">Generiert einen Stub, der das Marshalling von Ausnahmen auf der Serverseite abfängt und Sie an den Client zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="aeb94-112">Generates a stub that catches unmarshaling exceptions on the server side and propagates them back to the client.</span></span>

</dd> <dt>

<span id="ref"></span><span id="REF"></span>

<span data-ttu-id="aeb94-113"><span id="ref"></span><span id="REF"></span>Ref \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="aeb94-113"><span id="ref"></span><span id="REF"></span>\*\*\*\*ref\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="aeb94-114">Generiert Code, der zur Laufzeit eine Überprüfung ausführt, um sicherzustellen, dass keine **null** -Verweis Zeiger an die clientstubwerte übermittelt werden, und löst eine RPC-X-NULL-Verweis \_ Zeiger Ausnahme aus, \_ \_ \_ Wenn eine gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="aeb94-114">Generates code that runs a check at run time to ensure that no **NULL** reference pointers are being passed to the client stubs and raises an RPC\_X\_NULL\_REF\_POINTER exception if it finds any.</span></span>

</dd> <dt>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>

<span data-ttu-id="aeb94-115"><span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>Begrenzungen \_ Überprüfung \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="aeb94-115"><span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>\*\*\*\*bounds\_check\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="aeb94-116">Überprüft die Größe des konformen und variierenden Arrays anhand der Angabe der Übertragungs Länge.</span><span class="sxs-lookup"><span data-stu-id="aeb94-116">Checks size of conformant-varying and varying arrays against transmission length specification.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="aeb94-117"><span id="none"></span><span id="NONE"></span>keine \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="aeb94-117"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="aeb94-118">Führt keine Fehlerüberprüfung aus.</span><span class="sxs-lookup"><span data-stu-id="aeb94-118">Performs no error checking.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="aeb94-119"><span id="all"></span><span id="ALL"></span>Alle \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="aeb94-119"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="aeb94-120">Führt alle Fehlerprüfungen aus.</span><span class="sxs-lookup"><span data-stu-id="aeb94-120">Performs all error checking.</span></span> <span data-ttu-id="aeb94-121">Dies ist eine standardmäßige Compileroption, die mit der mittleren Version 5,0 wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="aeb94-121">Effective with MIDL version 5.0, this is a default compiler switch.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aeb94-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aeb94-122">Remarks</span></span>

<span data-ttu-id="aeb94-123">Der Schalter **/Error** wählt die Anzahl der Fehlerüberprüfungen aus, die von den generierten Stub-Dateien durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="aeb94-123">The **/error** switch selects the number of error checks that the generated stub files will perform.</span></span> <span data-ttu-id="aeb94-124">Gültig mit der mittleren Version 5,0, ist die Standardeinstellung " **/Error all**".</span><span class="sxs-lookup"><span data-stu-id="aeb94-124">Effective with MIDL version 5.0, the default setting is **/error all**.</span></span>

<span data-ttu-id="aeb94-125">Die aktivierten Enumerationsfehler (standardmäßig in allen Versionen von "Mittel l") sind abkürzen, die bei der Umstellung zwischen **langen** Enumerationstypen (32-Bit-Ganzzahlen) und **kurzen** Enumerationstypen (der Netzwerkdaten [**Darstellung der**](enum.md)Enumeration) und der Anzahl der Bezeichner in einer Enumeration, die 32.767 überschreitet, verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="aeb94-125">The enum errors that are checked (by default in all versions of MIDL) are truncation errors caused when converting between **long enum** types (32-bit integers) and **short enum** types (the network-data representation of [**enum**](enum.md)), and the number of identifiers in an enumeration exceeding 32,767.</span></span>

<span data-ttu-id="aeb94-126">Die Speicherzugriffs Fehlerüberprüfung (auch standardmäßig in allen Versionen von "Mittel l") ist für Zeiger vorgesehen, die das Ende des Puffers im Marshalling von Code überschreiten, sowie für konforme Arrays, deren Größe kleiner als 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="aeb94-126">The memory-access error checking (also by default in all versions of MIDL) is for pointers that exceed the end of the buffer in marshaling code and for conformant arrays whose size is less than zero.</span></span> <span data-ttu-id="aeb94-127">Verwenden **\_ Sie das Kontroll Flag/Error Bounds** , um andere ungültige Array Begrenzungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="aeb94-127">Use the **/error bounds\_check** flag to check for other invalid array bounds.</span></span>

<span data-ttu-id="aeb94-128">Wenn Sie die **/Error-Zuordnung** angeben, enthalten die stubsteine Code, der eine Ausnahme auslöst, wenn die [**mittlere \_ Benutzer \_ Zuordnung**](midl-user-allocate-1.md) 0 zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="aeb94-128">When you specify **/error allocation**, the stubs include code that raises an exception when [**midl\_user\_allocate**](midl-user-allocate-1.md) returns 0.</span></span>

<span data-ttu-id="aeb94-129">Mit der **/Error Stub \_ Data** -Option wird verhindert, dass Client Daten während des Unmarshalling auf den Server abstürzen und somit eine stabilere Methode zur Behandlung des nicht Marshallingvorgangs bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="aeb94-129">The **/error stub\_data** option prevents client data from crashing the server during unmarshaling, effectively providing a more robust method of handling the unmarshaling operation.</span></span>

<span data-ttu-id="aeb94-130">Mit Windows-2000 werden die meisten dieser Überprüfungen von der zugrunde liegenden Lauf Zeit-NDR-Mars Hall-Engine ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aeb94-130">Effective with WindowsÂ 2000, the underlying run-time NDR marshaling engine performs most of these checks.</span></span> <span data-ttu-id="aeb94-131">Dies bedeutet Folgendes: Wenn Sie einen der voll interpretierten Modi ([**/Oi**](-oi.md), **/OIF**) der Stub-Generierung verwenden, hat die Auswahl verschiedener Optionen für die Fehlerüberprüfung keine markierte Auswirkung auf die Leistung.</span><span class="sxs-lookup"><span data-stu-id="aeb94-131">This means that if you are using one of the fully-interpreted modes ([**/Oi**](-oi.md), **/Oif**) of stub generation, choosing different error checking options will not have a marked effect on performance.</span></span>

## <a name="examples"></a><span data-ttu-id="aeb94-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aeb94-132">Examples</span></span>

<span data-ttu-id="aeb94-133">**Mittel l/Error Zuordnungs Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="aeb94-133">**midl /error allocation filename.idl**</span></span>

<span data-ttu-id="aeb94-134">**Mittel l/Error keine Datei Name. idl**</span><span class="sxs-lookup"><span data-stu-id="aeb94-134">**midl /error none filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="aeb94-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aeb94-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeb94-136">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="aeb94-136">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="aeb94-137">**/robust**</span><span class="sxs-lookup"><span data-stu-id="aeb94-137">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




