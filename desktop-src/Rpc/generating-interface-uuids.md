---
title: Erstellen von Schnittstellen-UUIDs
description: Erstellen von Universal Unique Identifier (UUIDs) der Schnittstelle und Verwenden von uuidgen.
ms.assetid: a973b7f9-71c5-46a0-aa0c-51f150560dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c5f727ed3e37139d4da50f84c3929bff333156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710205"
---
# <a name="generating-interface-uuids"></a><span data-ttu-id="8dca0-103">Erstellen von Schnittstellen-UUIDs</span><span class="sxs-lookup"><span data-stu-id="8dca0-103">Generating Interface UUIDs</span></span>

<span data-ttu-id="8dca0-104">Dieser Abschnitt enthält Informationen zu universellen eindeutigen Bezeichnerzeichen (UUIDs) und zum uuidgen-Hilfsprogramm in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="8dca0-104">This section presents information on Universal Unique Identifiers (UUIDs) and the Uuidgen utility in the following topics:</span></span>

-   [<span data-ttu-id="8dca0-105">Was ist eine UUID?</span><span class="sxs-lookup"><span data-stu-id="8dca0-105">What is a UUID?</span></span>](#what-is-a-uuid)
-   [<span data-ttu-id="8dca0-106">Verwenden von uuidgen</span><span class="sxs-lookup"><span data-stu-id="8dca0-106">Using Uuidgen</span></span>](#using-uuidgen)

## <a name="what-is-a-uuid"></a><span data-ttu-id="8dca0-107">Was ist eine UUID?</span><span class="sxs-lookup"><span data-stu-id="8dca0-107">What is a UUID?</span></span>

<span data-ttu-id="8dca0-108">Alle Schnittstellen müssen in einem Netzwerk eindeutig identifiziert werden, damit Sie von Clients gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="8dca0-108">All interfaces must be uniquely identified on a network so that clients can find them.</span></span> <span data-ttu-id="8dca0-109">In kleinen Netzwerken kann der Name der Schnittstelle allein ausreichen, um Sie zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8dca0-109">On small networks, the interface's name alone may be sufficient to identify it.</span></span> <span data-ttu-id="8dca0-110">Dies ist jedoch in großen Netzwerken in der Regel nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="8dca0-110">However, that is usually not feasible on large networks.</span></span> <span data-ttu-id="8dca0-111">Daher weisen Entwickler in der Regel jeder Schnittstelle einen universellen eindeutigen Bezeichner (UUID, austauschbar mit dem Begriff GUID oder einen global eindeutigen Bezeichner) zu.</span><span class="sxs-lookup"><span data-stu-id="8dca0-111">Therefore, developers typically assign a Universal Unique Identifier (UUID, interchangeable with the term GUID, or Globally Unique Identifier) to each interface.</span></span> <span data-ttu-id="8dca0-112">Eine UUID ist eine Zeichenfolge, die eine Reihe von hexadezimalen Ziffern enthält.</span><span class="sxs-lookup"><span data-stu-id="8dca0-112">A UUID is a string that contains a set of hexadecimal digits.</span></span> <span data-ttu-id="8dca0-113">Jede Schnittstelle hat eine andere UUID.</span><span class="sxs-lookup"><span data-stu-id="8dca0-113">Each interface has a different UUID.</span></span> <span data-ttu-id="8dca0-114">Weitere Informationen finden Sie unter [Zeichenfolge UUID](string-uuid.md).</span><span class="sxs-lookup"><span data-stu-id="8dca0-114">For details, see [String UUID](string-uuid.md).</span></span>

<span data-ttu-id="8dca0-115">Die Textdarstellung einer UUID ist eine Zeichenfolge, die aus 8 hexadezimalen Ziffern gefolgt von einem Bindestrich gefolgt von drei durch Trennzeichen getrennten Gruppen von vier hexadezimalen Ziffern gefolgt von einem Bindestrich gefolgt von 12 hexadezimal Ziffern besteht.</span><span class="sxs-lookup"><span data-stu-id="8dca0-115">The textual representation of a UUID is a string consisting of 8 hexadecimal digits followed by a hyphen, followed by three hyphen-separated groups of 4 hexadecimal digits, followed by a hyphen, followed by 12 hexadecimal digits.</span></span> <span data-ttu-id="8dca0-116">Das folgende Beispiel ist eine gültige UUID-Zeichenfolge:</span><span class="sxs-lookup"><span data-stu-id="8dca0-116">The following example is a valid UUID string:</span></span>

<span data-ttu-id="8dca0-117">ba209999-0c6c-11d2-97cf-00c04f8eea45</span><span class="sxs-lookup"><span data-stu-id="8dca0-117">ba209999-0c6c-11d2-97cf-00c04f8eea45</span></span>

<span data-ttu-id="8dca0-118">Leere UUIDs werden als NULL UUIDs anstelle von **null** UUIDs bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8dca0-118">Empty UUIDs are referred to as nil UUIDs rather than **NULL** UUIDs.</span></span> <span data-ttu-id="8dca0-119">Der Begriff Nil gibt alles an, das NULL, leer, leer oder nicht initialisiert ist.</span><span class="sxs-lookup"><span data-stu-id="8dca0-119">The term nil indicates anything that is zero, blank, empty, or uninitialized.</span></span> <span data-ttu-id="8dca0-120">Eine leere Zeichenfolge, ein leerer Datenbankdaten Satz oder eine nicht initialisierte UUID sind Beispiele für Nil-Werte.</span><span class="sxs-lookup"><span data-stu-id="8dca0-120">An empty string, an empty database record, or an uninitialized UUID are all examples of nil values.</span></span>

> [!Note]  
> <span data-ttu-id="8dca0-121">Der Wert **null** ist der spezifische Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="8dca0-121">The value **NULL** is the specific value zero.</span></span> <span data-ttu-id="8dca0-122">Sie wird häufig in der C-und C++-Programmierung zusammen mit Zeigern verwendet.</span><span class="sxs-lookup"><span data-stu-id="8dca0-122">It is often used in C and C++ programming in conjunction with pointers.</span></span> <span data-ttu-id="8dca0-123">Nil ist ein allgemeinerer Begriff als **null**.</span><span class="sxs-lookup"><span data-stu-id="8dca0-123">Nil is a more general term than **NULL**.</span></span> <span data-ttu-id="8dca0-124">Nicht initialisierte UUIDs der Objektschnittstelle sollten immer als NULL-UUIDs und nicht als **null** -UUIDs bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="8dca0-124">Uninitialized object interface UUIDs should always be referred to as nil UUIDs rather than **NULL** UUIDs.</span></span>

 

## <a name="using-uuidgen"></a><span data-ttu-id="8dca0-125">Verwenden von uuidgen</span><span class="sxs-lookup"><span data-stu-id="8dca0-125">Using Uuidgen</span></span>

<span data-ttu-id="8dca0-126">Microsoft stellt ein hilfsprogrammprogramm mit dem Namen uuidgen zum Generieren der UUIDs zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="8dca0-126">Microsoft provides a utility program called Uuidgen to generate your UUIDs.</span></span> <span data-ttu-id="8dca0-127">Das Hilfsprogramm uuidgen generiert die UUID im IDL-Dateiformat oder im C-sprach Format.</span><span class="sxs-lookup"><span data-stu-id="8dca0-127">The Uuidgen utility generates the UUID in IDL file format or C-language format.</span></span>

<span data-ttu-id="8dca0-128">Wenn Sie das Hilfsprogramm uuidgen von der Befehlszeile ausführen, können Sie die folgenden Befehls Schalter verwenden.</span><span class="sxs-lookup"><span data-stu-id="8dca0-128">When you run the Uuidgen utility from the command line, you can use the following command switches.</span></span>



| <span data-ttu-id="8dca0-129">Uuidgen-Switch</span><span class="sxs-lookup"><span data-stu-id="8dca0-129">Uuidgen switch</span></span>           | <span data-ttu-id="8dca0-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8dca0-130">Description</span></span>                                                                |
|--------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="8dca0-131">**/I**</span><span class="sxs-lookup"><span data-stu-id="8dca0-131">**/I**</span></span>                   | <span data-ttu-id="8dca0-132">Gibt UUID an eine IDL-Schnittstellen Vorlage aus.</span><span class="sxs-lookup"><span data-stu-id="8dca0-132">Outputs UUID to an IDL interface template.</span></span>                                 |
| <span data-ttu-id="8dca0-133">**/s**</span><span class="sxs-lookup"><span data-stu-id="8dca0-133">**/s**</span></span>                   | <span data-ttu-id="8dca0-134">Gibt UUID als initialisierte C-Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="8dca0-134">Outputs UUID as an initialized C structure.</span></span>                                |
| <span data-ttu-id="8dca0-135">**/o** < *Dateiname*></span><span class="sxs-lookup"><span data-stu-id="8dca0-135">**/o**<*filename*></span></span> | <span data-ttu-id="8dca0-136">Leitet die Ausgabe in eine Datei um. wird unmittelbar nach dem **/o** -Schalter angegeben.</span><span class="sxs-lookup"><span data-stu-id="8dca0-136">Redirects output to a file; specified immediately after the **/o** switch.</span></span> |
| <span data-ttu-id="8dca0-137">**/n** < *Zahl*></span><span class="sxs-lookup"><span data-stu-id="8dca0-137">**/n**<*number*></span></span>   | <span data-ttu-id="8dca0-138">Gibt die Anzahl der zu generierenden UUIDs an.</span><span class="sxs-lookup"><span data-stu-id="8dca0-138">Specifies the number of UUIDs to generate.</span></span>                                 |
| <span data-ttu-id="8dca0-139">**/v**</span><span class="sxs-lookup"><span data-stu-id="8dca0-139">**/v**</span></span>                   | <span data-ttu-id="8dca0-140">Zeigt Versionsinformationen zu uuidgen an.</span><span class="sxs-lookup"><span data-stu-id="8dca0-140">Displays version information about Uuidgen.</span></span>                                |
| <span data-ttu-id="8dca0-141">**/h** oder **?**</span><span class="sxs-lookup"><span data-stu-id="8dca0-141">**/h** or **?**</span></span>          | <span data-ttu-id="8dca0-142">Zeigt die Zusammenfassung der Befehls Option an.</span><span class="sxs-lookup"><span data-stu-id="8dca0-142">Displays command-option summary.</span></span>                                           |



 

<span data-ttu-id="8dca0-143">In der Regel verwenden Sie das Hilfsprogramm uuidgen, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8dca0-143">Typically, you will use the Uuidgen utility as shown in the following example.</span></span>

<span data-ttu-id="8dca0-144">**"uuidgen-i-omyapp. idl**</span><span class="sxs-lookup"><span data-stu-id="8dca0-144">**uuidgen -i -oMyApp.idl**</span></span>

<span data-ttu-id="8dca0-145">Dieser Befehl generiert eine UUID und speichert Sie in einer Mittel l-Datei, die Sie als Vorlage verwenden können.</span><span class="sxs-lookup"><span data-stu-id="8dca0-145">This command generates a UUID and stores it in a MIDL file that you can use as a template.</span></span> <span data-ttu-id="8dca0-146">Wenn der vorherige Befehl ausgeführt wird, ähnelt der Inhalt von "MyApp. idl" folgendem:</span><span class="sxs-lookup"><span data-stu-id="8dca0-146">When the preceding command is executed, the contents of MyApp.idl are similar to the following:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

<span data-ttu-id="8dca0-147">Der nächste Schritt besteht darin, den Platzhalter Namen "interfakename" durch den tatsächlichen Namen der Schnittstelle zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="8dca0-147">The next step would be to replace the placeholder name, INTERFACENAME, with the actual name of your interface.</span></span>

 

 




