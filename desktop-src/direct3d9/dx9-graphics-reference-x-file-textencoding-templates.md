---
description: Vorlagen definieren, wie der Datenstrom interpretiert wird. die Daten werden von der Vorlagen Definition moduliert. In diesem Abschnitt werden die folgenden Aspekte einer Vorlage erläutert und eine Beispiel Vorlage bereitstellt.
ms.assetid: f84978a8-8315-4626-be68-f00f3a72e5ac
title: Vorlagen (X-Dateiformat, Text Codierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fccec46e72a73bb5ed4434fd252595e1b072ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745392"
---
# <a name="templates-x-file-format-text-encoding"></a><span data-ttu-id="c80dd-104">Vorlagen (X-Dateiformat, Text Codierung)</span><span class="sxs-lookup"><span data-stu-id="c80dd-104">Templates (X file format, text encoding)</span></span>

<span data-ttu-id="c80dd-105">Vorlagen definieren, wie der Datenstrom interpretiert wird. die Daten werden von der Vorlagen Definition moduliert.</span><span class="sxs-lookup"><span data-stu-id="c80dd-105">Templates define how the data stream is interpreted - the data is modulated by the template definition.</span></span> <span data-ttu-id="c80dd-106">In diesem Abschnitt werden die folgenden Aspekte einer Vorlage erläutert und eine Beispiel Vorlage bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c80dd-106">This section discusses the following aspects of a template and provides an example template.</span></span>

<span data-ttu-id="c80dd-107">Es gibt eine besondere Vorlage (die Header Vorlage).</span><span class="sxs-lookup"><span data-stu-id="c80dd-107">There is one special template - the header template.</span></span> <span data-ttu-id="c80dd-108">Es wird empfohlen, dass jede Anwendung eine Header Vorlage definiert und Sie zum Definieren von anwendungsspezifischen Informationen verwendet, z. b. Versionsinformationen.</span><span class="sxs-lookup"><span data-stu-id="c80dd-108">It is recommended that each application define a header template and use it to define application-specific information, such as version information.</span></span> <span data-ttu-id="c80dd-109">Wenn dieser Header vorhanden ist, wird er von der. x-Dateiformat-API gelesen.</span><span class="sxs-lookup"><span data-stu-id="c80dd-109">If present, this header is read by the .x file format API.</span></span> <span data-ttu-id="c80dd-110">Wenn ein Flags-Member verfügbar ist, wird er verwendet, um zu bestimmen, wie die folgenden Daten interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="c80dd-110">If a flags member is available, it is used to determine how the following data is interpreted.</span></span> <span data-ttu-id="c80dd-111">Der Flags-Member sollte, falls definiert, ein DWORD-Element sein.</span><span class="sxs-lookup"><span data-stu-id="c80dd-111">The flags member, if defined, should be a DWORD.</span></span> <span data-ttu-id="c80dd-112">Zurzeit ist ein Bit definiert-Bit 0.</span><span class="sxs-lookup"><span data-stu-id="c80dd-112">One bit is currently defined - bit 0.</span></span> <span data-ttu-id="c80dd-113">Wenn dieses Bit eindeutig ist, sind die folgenden Daten in der Datei binär.</span><span class="sxs-lookup"><span data-stu-id="c80dd-113">If this bit is clear, the following data in the file is binary.</span></span> <span data-ttu-id="c80dd-114">Wenn festgelegt, sind die folgenden Daten Text.</span><span class="sxs-lookup"><span data-stu-id="c80dd-114">If set, the following data is text.</span></span> <span data-ttu-id="c80dd-115">Sie können mehrere Header Datenobjekte verwenden, um zwischen Binärdateien und Text in der Datei zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="c80dd-115">You can use multiple header data objects to switch between binary and text within the file.</span></span>

## <a name="template-form-name-and-uuid"></a><span data-ttu-id="c80dd-116">Vorlagen Formular, Name und UUID</span><span class="sxs-lookup"><span data-stu-id="c80dd-116">Template Form, Name, and UUID</span></span>

<span data-ttu-id="c80dd-117">Eine Vorlage weist das folgende Format auf.</span><span class="sxs-lookup"><span data-stu-id="c80dd-117">A template has the following form.</span></span>


```
template <template-name> {
<UUID>
    <member 1>;
...
    <member n>;
[restrictions]
}
```



<span data-ttu-id="c80dd-118">Der Vorlagen Name ist ein alphanumerischer Name, der den Unterstrich () enthalten kann \_ .</span><span class="sxs-lookup"><span data-stu-id="c80dd-118">The template name is an alphanumeric name that can include the underscore character (\_).</span></span> <span data-ttu-id="c80dd-119">Er darf nicht mit einer Ziffer beginnen.</span><span class="sxs-lookup"><span data-stu-id="c80dd-119">It must not begin with a digit.</span></span> <span data-ttu-id="c80dd-120">Die UUID ist ein universell eindeutiger Bezeichner, der für den Standard der verteilten Computing-Umgebung von Open Software Foundation formatiert und durch eckige Klammern (< >) eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="c80dd-120">The UUID is a universally unique identifier formatted to the Open Software Foundation's Distributed Computing Environment standard and enclosed by angle brackets (< >).</span></span> <span data-ttu-id="c80dd-121">Beispiel: <3d82ab43-62da-11CF-ab39-0020af71e433>.</span><span class="sxs-lookup"><span data-stu-id="c80dd-121">For example: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.</span></span>

## <a name="template-members"></a><span data-ttu-id="c80dd-122">Vorlagen Mitglieder</span><span class="sxs-lookup"><span data-stu-id="c80dd-122">Template Members</span></span>

<span data-ttu-id="c80dd-123">Vorlagen Elemente bestehen aus einem benannten Datentyp, gefolgt von einem optionalen Namen oder einem Array eines benannten Datentyps.</span><span class="sxs-lookup"><span data-stu-id="c80dd-123">Template members consist of a named data type followed by an optional name or an array of a named data type.</span></span> <span data-ttu-id="c80dd-124">Gültige primitive Datentypen sind in der folgenden Tabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="c80dd-124">Valid primitive data types are defined in the following table.</span></span>



| <span data-ttu-id="c80dd-125">type</span><span class="sxs-lookup"><span data-stu-id="c80dd-125">Type</span></span>    | <span data-ttu-id="c80dd-126">Size</span><span class="sxs-lookup"><span data-stu-id="c80dd-126">Size</span></span>                               |
|---------|------------------------------------|
| <span data-ttu-id="c80dd-127">WORD</span><span class="sxs-lookup"><span data-stu-id="c80dd-127">WORD</span></span>    | <span data-ttu-id="c80dd-128">16 Bit</span><span class="sxs-lookup"><span data-stu-id="c80dd-128">16 bits</span></span>                            |
| <span data-ttu-id="c80dd-129">DWORD</span><span class="sxs-lookup"><span data-stu-id="c80dd-129">DWORD</span></span>   | <span data-ttu-id="c80dd-130">32 Bit</span><span class="sxs-lookup"><span data-stu-id="c80dd-130">32 bits</span></span>                            |
| <span data-ttu-id="c80dd-131">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="c80dd-131">FLOAT</span></span>   | <span data-ttu-id="c80dd-132">IEEE Float</span><span class="sxs-lookup"><span data-stu-id="c80dd-132">IEEE float</span></span>                         |
| <span data-ttu-id="c80dd-133">Double</span><span class="sxs-lookup"><span data-stu-id="c80dd-133">DOUBLE</span></span>  | <span data-ttu-id="c80dd-134">64 Bit</span><span class="sxs-lookup"><span data-stu-id="c80dd-134">64 bits</span></span>                            |
| <span data-ttu-id="c80dd-135">CHAR</span><span class="sxs-lookup"><span data-stu-id="c80dd-135">CHAR</span></span>    | <span data-ttu-id="c80dd-136">8 Bit</span><span class="sxs-lookup"><span data-stu-id="c80dd-136">8 bits</span></span>                             |
| <span data-ttu-id="c80dd-137">UCHAR</span><span class="sxs-lookup"><span data-stu-id="c80dd-137">UCHAR</span></span>   | <span data-ttu-id="c80dd-138">8 Bit</span><span class="sxs-lookup"><span data-stu-id="c80dd-138">8 bits</span></span>                             |
| <span data-ttu-id="c80dd-139">BYTE</span><span class="sxs-lookup"><span data-stu-id="c80dd-139">BYTE</span></span>    | <span data-ttu-id="c80dd-140">8 Bit</span><span class="sxs-lookup"><span data-stu-id="c80dd-140">8 bits</span></span>                             |
| <span data-ttu-id="c80dd-141">STRING</span><span class="sxs-lookup"><span data-stu-id="c80dd-141">STRING</span></span>  | <span data-ttu-id="c80dd-142">NULL beendete Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c80dd-142">NULL terminated string</span></span>             |
| <span data-ttu-id="c80dd-143">CSTRING</span><span class="sxs-lookup"><span data-stu-id="c80dd-143">CSTRING</span></span> | <span data-ttu-id="c80dd-144">Formatierte C-Zeichenfolge (nicht unterstützt)</span><span class="sxs-lookup"><span data-stu-id="c80dd-144">Formatted C string (not supported)</span></span> |
| <span data-ttu-id="c80dd-145">UNICODE</span><span class="sxs-lookup"><span data-stu-id="c80dd-145">UNICODE</span></span> | <span data-ttu-id="c80dd-146">Unicode-Zeichenfolge (nicht unterstützt)</span><span class="sxs-lookup"><span data-stu-id="c80dd-146">Unicode string (not supported)</span></span>     |



 

<span data-ttu-id="c80dd-147">Auf zusätzliche Datentypen, die durch Vorlagen definiert werden, die zuvor im Datenstrom definiert wurden, kann auch innerhalb einer Vorlagen Definition referenziert werden.</span><span class="sxs-lookup"><span data-stu-id="c80dd-147">Additional data types defined by templates encountered earlier in the data stream can also be referenced within a template definition.</span></span> <span data-ttu-id="c80dd-148">Es sind keine vorwärts Verweise zulässig.</span><span class="sxs-lookup"><span data-stu-id="c80dd-148">No forward references are allowed.</span></span>

<span data-ttu-id="c80dd-149">Jeder gültige Datentyp kann als Array in der Vorlagen Definition ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="c80dd-149">Any valid data type can be expressed as an array in the template definition.</span></span> <span data-ttu-id="c80dd-150">Die grundlegende Syntax wird im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c80dd-150">The basic syntax is shown in the following example.</span></span>


```
array <data-type> <name>[<dimension-size>];
```



<span data-ttu-id="c80dd-151"><Dimensions Größe> kann entweder eine ganze Zahl oder ein benannter Verweis auf einen anderen Vorlagen Member sein, dessen Wert dann ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c80dd-151"><dimension-size> can either be an integer or a named reference to another template member whose value is then substituted.</span></span> <span data-ttu-id="c80dd-152">Arrays können n-dimensional sein, wobei n durch die Anzahl der gekoppelten eckigen Klammern bestimmt wird, die der Anweisung folgen, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c80dd-152">Arrays can be n-dimensional, where n is determined by the number of paired square brackets trailing the statement, as in the following example.</span></span>


```
array DWORD FixedHerd[24];
array DWORD Herd[nCows];
array FLOAT Matrix4x4[4][4];
```



## <a name="template-restrictions"></a><span data-ttu-id="c80dd-153">Vorlagen Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="c80dd-153">Template Restrictions</span></span>

<span data-ttu-id="c80dd-154">Vorlagen können offen, geschlossen oder eingeschränkt sein.</span><span class="sxs-lookup"><span data-stu-id="c80dd-154">Templates can be open, closed, or restricted.</span></span> <span data-ttu-id="c80dd-155">Diese Einschränkungen legen fest, welche Datentypen in der unmittelbaren Hierarchie eines von der Vorlage definierten Datenobjekts vorkommen können.</span><span class="sxs-lookup"><span data-stu-id="c80dd-155">These restrictions determine which data types can appear in the immediate hierarchy of a data object defined by the template.</span></span> <span data-ttu-id="c80dd-156">Eine geöffnete Vorlage hat keine Einschränkungen, eine geschlossene Vorlage lehnt alle Datentypen ab, und eine eingeschränkte Vorlage lässt eine benannte Liste von Datentypen zu.</span><span class="sxs-lookup"><span data-stu-id="c80dd-156">An open template has no restrictions, a closed template rejects all data types, and a restricted template allows a named list of data types.</span></span>

<span data-ttu-id="c80dd-157">Die Syntax zum Angeben einer geöffneten Vorlage besteht aus drei Punkten, die in eckigen Klammern eingeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="c80dd-157">The syntax for indicating an open template is three periods enclosed by square brackets.</span></span>


```
[ ... ]
```



<span data-ttu-id="c80dd-158">Eine durch Trennzeichen getrennte Liste benannter Datentypen, gefolgt von ihren UUIDs, die in eckigen Klammern eingeschlossen sind, deutet auf eine eingeschränkte Vorlage hin.</span><span class="sxs-lookup"><span data-stu-id="c80dd-158">A comma-separated list of named data types followed optionally by their UUIDs enclosed by square brackets indicates a restricted template.</span></span>


```
[ { data-type [ UUID ] , } ... ]
```



<span data-ttu-id="c80dd-159">Das Fehlen einer der obigen Optionen deutet auf eine geschlossene Vorlage hin.</span><span class="sxs-lookup"><span data-stu-id="c80dd-159">The absence of either of the above indicates a closed template.</span></span>

## <a name="template-example"></a><span data-ttu-id="c80dd-160">Vorlagen Beispiel</span><span class="sxs-lookup"><span data-stu-id="c80dd-160">Template Example</span></span>

<span data-ttu-id="c80dd-161">Das folgende Beispiel zeigt eine Beispiel Vorlage.</span><span class="sxs-lookup"><span data-stu-id="c80dd-161">The following shows an example template.</span></span>


```
template Mesh {
<3D82AB44-62DA-11cf-AB39-0020AF71E433>
DWORD nVertices;
array Vector vertices[nVertices];
DWORD nFaces;
array MeshFace faces[nFaces];
 [ ... ]                // An open template
}
template Vector {
<3D82AB5E-62DA-11cf-AB39-0020AF71E433>
FLOAT x;
FLOAT y;
FLOAT z;
}                        // A closed template
template FileSystem {
<UUID>
STRING name;
[ Directory <UUID>, File <UUID> ]    // A restricted template
}
```



## <a name="related-topics"></a><span data-ttu-id="c80dd-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c80dd-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c80dd-163">Text Codierung</span><span class="sxs-lookup"><span data-stu-id="c80dd-163">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



