---
title: User-Defined-Ressource
description: Eine benutzerdefinierte Ressourcen Definitions Anweisung definiert eine Ressource, die anwendungsspezifische Daten enthält.
ms.assetid: b1cfec71-5733-4900-97f6-c1cbb350c728
keywords:
- benutzerdefinierte Ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909352c7f0643ed67b1d199fafba1ac8f15d2a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206693"
---
# <a name="user-defined-resource"></a><span data-ttu-id="f2237-104">User-Defined-Ressource</span><span class="sxs-lookup"><span data-stu-id="f2237-104">User-Defined Resource</span></span>

<span data-ttu-id="f2237-105">Eine benutzerdefinierte Ressourcen Definitions Anweisung definiert eine Ressource, die anwendungsspezifische Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="f2237-105">A user-defined resource-definition statement defines a resource that contains application-specific data.</span></span> <span data-ttu-id="f2237-106">Die Daten können ein beliebiges Format aufweisen und können entweder als Inhalt einer bestimmten Datei (wenn der *filename* -Parameter angegeben ist) oder als eine Reihe von Zahlen und Zeichen folgen (wenn der *RAW-Data-* Block angegeben ist) definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f2237-106">The data can have any format and can be defined either as the content of a given file (if the *filename* parameter is given) or as a series of numbers and strings (if the *raw-data* block is specified).</span></span>

``` syntax
nameID typeID filename
```

<span data-ttu-id="f2237-107">Der *Dateiname* gibt den Namen einer Datei an, die die Binärdaten der Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="f2237-107">The *filename* specifies the name of a file containing the binary data of the resource.</span></span> <span data-ttu-id="f2237-108">Der Inhalt der Datei ist als Ressource enthalten.</span><span class="sxs-lookup"><span data-stu-id="f2237-108">The contents of the file are included as the resource.</span></span> <span data-ttu-id="f2237-109">RC interpretiert die Binärdaten in keiner Weise.</span><span class="sxs-lookup"><span data-stu-id="f2237-109">RC does not interpret the binary data in any way.</span></span> <span data-ttu-id="f2237-110">Der Programmierer ist dafür verantwortlich, sicherzustellen, dass die Daten für die Zielcomputer Architektur ordnungsgemäß ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="f2237-110">It is the programmer's responsibility to ensure that the data is properly aligned for the target computer architecture.</span></span>

<span data-ttu-id="f2237-111">Eine benutzerdefinierte Ressource kann auch vollständig im Ressourcen Skript definiert werden. verwenden Sie dazu die folgende Syntax:</span><span class="sxs-lookup"><span data-stu-id="f2237-111">A user-defined resource can also be defined completely in the resource script using the following syntax:</span></span>

``` syntax
nameID typeID  {  raw-data  }
```

## <a name="parameters"></a><span data-ttu-id="f2237-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2237-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2237-113"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*</span><span class="sxs-lookup"><span data-stu-id="f2237-113"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="f2237-114">Eindeutiger Name oder eine 16-Bit-Ganzzahl ohne Vorzeichen, die die Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f2237-114">Unique name or a 16-bit unsigned integer that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="f2237-115"><span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*TypeId*</span><span class="sxs-lookup"><span data-stu-id="f2237-115"><span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*typeID*</span></span>
</dt> <dd>

<span data-ttu-id="f2237-116">Eindeutiger Name oder eine 16-Bit-Ganzzahl ohne Vorzeichen, die den Ressourcentyp identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f2237-116">Unique name or a 16-bit unsigned integer that identifies the resource type.</span></span> <span data-ttu-id="f2237-117">Wenn eine Zahl angegeben wird, muss sie größer als 255 sein.</span><span class="sxs-lookup"><span data-stu-id="f2237-117">If a number is given, it must be greater than 255.</span></span> <span data-ttu-id="f2237-118">Die Zahlen 1 bis 255 sind für vorhandene und zukünftige neu definierte Ressourcentypen reserviert.</span><span class="sxs-lookup"><span data-stu-id="f2237-118">The numbers 1 through 255 are reserved for existing and future redefined resource types.</span></span>

</dd> <dt>

<span data-ttu-id="f2237-119"><span id="filename"></span><span id="FILENAME"></span>*Einfügen*</span><span class="sxs-lookup"><span data-stu-id="f2237-119"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="f2237-120">Der Name der Datei, die die Ressourcen Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="f2237-120">Name of the file that contains the resource data.</span></span> <span data-ttu-id="f2237-121">Der-Parameter muss ein gültiger Dateiname sein. Es muss sich um einen vollständigen Pfad handeln, wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet.</span><span class="sxs-lookup"><span data-stu-id="f2237-121">The parameter must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span>

</dd> <dt>

<span data-ttu-id="f2237-122"><span id="raw-data"></span><span id="RAW-DATA"></span>*Rohdaten*</span><span class="sxs-lookup"><span data-stu-id="f2237-122"><span id="raw-data"></span><span id="RAW-DATA"></span>*raw-data*</span></span>
</dt> <dd>

<span data-ttu-id="f2237-123">Rohdaten, die aus einer oder mehreren Ganzzahlen oder Zeichen folgen bestehen.</span><span class="sxs-lookup"><span data-stu-id="f2237-123">Raw data consisting of one or more integers or strings of characters.</span></span> <span data-ttu-id="f2237-124">Ganze Zahlen können im Dezimal-, Oktal-oder Hexadezimal Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f2237-124">Integers can be specified in decimal, octal, or hexadecimal format.</span></span> <span data-ttu-id="f2237-125">Um mit 16-Bit-Fenstern kompatibel zu sein, werden ganze Zahlen als Word-Werte gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f2237-125">To be compatible with 16-bit Windows, integers are stored as WORD values.</span></span> <span data-ttu-id="f2237-126">Sie können eine ganze Zahl als DWORD-Wert speichern, indem Sie die ganze Zahl mit dem Suffix "L" qualifizieren.</span><span class="sxs-lookup"><span data-stu-id="f2237-126">You can store an integer as a DWORD value by qualifying the integer with the "L" suffix.</span></span>

<span data-ttu-id="f2237-127">Zeichen folgen werden in Anführungszeichen eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f2237-127">Strings are enclosed in quotation marks.</span></span> <span data-ttu-id="f2237-128">RC fügt kein abschließendes NULL-Zeichen automatisch an eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="f2237-128">RC does not automatically append a terminating null character to a string.</span></span> <span data-ttu-id="f2237-129">Jede Zeichenfolge ist eine Sequenz der angegebenen ANSI-Zeichen, es sei denn, Sie qualifizieren Sie als breit Zeichen-Zeichenfolge mit dem Präfix "L".</span><span class="sxs-lookup"><span data-stu-id="f2237-129">Each string is a sequence of the specified ANSI characters, unless you qualify it as a wide-character string with the "L" prefix.</span></span>

<span data-ttu-id="f2237-130">Der Datenblock beginnt an einer **DWORD** -Grenze, und RC führt keine Auffüll-oder Ausrichtungs Daten im *RAW-Data-* Block aus.</span><span class="sxs-lookup"><span data-stu-id="f2237-130">The block of data begins on a **DWORD** boundary and RC performs no padding or alignment of data within the *raw-data* block.</span></span> <span data-ttu-id="f2237-131">Der Programmierer ist dafür verantwortlich, die ordnungsgemäße Ausrichtung der Daten innerhalb des Blocks sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="f2237-131">It is the programmer's responsibility to ensure the proper alignment of data within the block.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="f2237-132">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f2237-132">Example</span></span>

<span data-ttu-id="f2237-133">Das folgende Beispiel zeigt mehrere benutzerdefinierte-Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="f2237-133">The following example shows several user-defined statements:</span></span>

``` syntax
array   MYRES   data.res
14      300     custom.res
18 MYRES2
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

 

 




