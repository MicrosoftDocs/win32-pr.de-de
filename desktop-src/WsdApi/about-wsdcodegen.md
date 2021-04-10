---
description: Beschreibt die von wsdcodegen verwendeten Eingabedateien und die von wsdcodegen generierten Ausgabedateien.
ms.assetid: 990511ca-a918-460b-91e0-c1454e242f17
title: Informationen zu wsdcodegen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073530560e7923f0e67ba888f168a669d6ba5561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042054"
---
# <a name="about-wsdcodegen"></a><span data-ttu-id="ae1da-103">Informationen zu wsdcodegen</span><span class="sxs-lookup"><span data-stu-id="ae1da-103">About WsdCodeGen</span></span>

<span data-ttu-id="ae1da-104">Wsdcodegen verwendet eine XML-Konfigurationsdatei, um den Speicherort der Dienst Metadaten zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="ae1da-104">WsdCodeGen uses an XML configuration file to determine the location of the service metadata.</span></span> <span data-ttu-id="ae1da-105">Die Konfigurationsdatei wird auch zum Definieren von Schnittstellennamen, Schnittstellen-GUIDs, Klassennamen, Methodennamen und anderen Bezeichnerzeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ae1da-105">The configuration file is also used to define interface names, interface GUIDs, class names, method names, and other identifiers.</span></span> <span data-ttu-id="ae1da-106">Weitere Informationen zu dieser Datei finden Sie unter [wsdcodegen-Konfigurationsdatei](wsdcodegen-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="ae1da-106">For more information about this file, see [WsdCodeGen Configuration File](wsdcodegen-configuration-file.md).</span></span>

<span data-ttu-id="ae1da-107">Wsdcodegen erfordert zwei Arten von Eingabedateien: eine XML-Konfigurationsdatei und eine oder mehrere Dienst Beschreibungsdateien (WSDL-und/oder XSD-Dateien).</span><span class="sxs-lookup"><span data-stu-id="ae1da-107">WsdCodeGen requires two types of input files: an XML configuration file and one or more service description files (WSDL and/or XSD files).</span></span> <span data-ttu-id="ae1da-108">Wsdcodegen verarbeitet diese Eingabedateien und generiert zwei Arten von Ausgabedateien: Schnittstellen Dateien und Header/Quelldateien.</span><span class="sxs-lookup"><span data-stu-id="ae1da-108">WsdCodeGen processes these input files and generates two type of output files: interface files and header/source files.</span></span>

## <a name="input-files"></a><span data-ttu-id="ae1da-109">Eingabedateien</span><span class="sxs-lookup"><span data-stu-id="ae1da-109">Input Files</span></span>



| <span data-ttu-id="ae1da-110">type</span><span class="sxs-lookup"><span data-stu-id="ae1da-110">Type</span></span>                      | <span data-ttu-id="ae1da-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae1da-111">Description</span></span>                                                                                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae1da-112">Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="ae1da-112">Configuration file</span></span>        | <span data-ttu-id="ae1da-113">Eine XML-Datei, die den Speicherort der Dienst Metadaten angibt und Schnittstellennamen, Schnittstellen-GUIDs, Klassennamen, Methodennamen und andere Bezeichner definiert.</span><span class="sxs-lookup"><span data-stu-id="ae1da-113">An XML file that indicates the location of the service metadata and defines interface names, interface GUIDs, class names, method names, and other identifiers.</span></span> |
| <span data-ttu-id="ae1da-114">Dienst Beschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="ae1da-114">Service description files</span></span> | <span data-ttu-id="ae1da-115">Mindestens eine WSDL-oder XSD-Datei, die die auf dem Gerät zu implementierenden Dienste beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ae1da-115">One or more WSDL or XSD files that describes the services to implement on the device.</span></span>                                                                           |



 

## <a name="output-files"></a><span data-ttu-id="ae1da-116">Ausgabedateien</span><span class="sxs-lookup"><span data-stu-id="ae1da-116">Output Files</span></span>



| <span data-ttu-id="ae1da-117">type</span><span class="sxs-lookup"><span data-stu-id="ae1da-117">Type</span></span>                        | <span data-ttu-id="ae1da-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae1da-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae1da-119">Schnittstellen Dateien</span><span class="sxs-lookup"><span data-stu-id="ae1da-119">Interface files</span></span>             | <span data-ttu-id="ae1da-120">Eine IDL-Datei (Interface Definition Language), die mit dem Mittelwert Compiler verwendet werden kann, um eine Schnittstellen Header Datei zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="ae1da-120">An IDL (Interface Definition Language) file that can be used with the MIDL compiler to produce an interface header file.</span></span> <span data-ttu-id="ae1da-121">WSDAPI-Clients und WSDAPI-Dienste können diese Schnittstellen Datei verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae1da-121">WSDAPI clients and WSDAPI services can use this interface file.</span></span>                                                                                                                                                           |
| <span data-ttu-id="ae1da-122">C++-Header und-Quelldateien</span><span class="sxs-lookup"><span data-stu-id="ae1da-122">C++ header and source files</span></span> | <span data-ttu-id="ae1da-123">C++-Dateien, die den Nachrichten Vertrag, den Namespace und die Typinformationen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ae1da-123">C++ files that describe the message contract, namespace, and type information.</span></span> <span data-ttu-id="ae1da-124">Sie enthalten möglicherweise Proxycode und/oder Stub-Code.</span><span class="sxs-lookup"><span data-stu-id="ae1da-124">They may contain proxy code and/or stub code.</span></span> <span data-ttu-id="ae1da-125">Der Proxycode implementiert die-Schnittstelle eines Dienstanbieter und übersetzt Dienst Methodenaufrufe in WSDAPI-Vorgänge, die Service Requests ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae1da-125">Proxy code implements a service's interface and translates service method calls into WSDAPI operations that make service requests.</span></span> <span data-ttu-id="ae1da-126">Der Stubcode übersetzt WSDAPI-Dienst Anforderungen in Code, der Dienst Methoden aufruft.</span><span class="sxs-lookup"><span data-stu-id="ae1da-126">Stub code translates WSDAPI service requests into code that calls service methods.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ae1da-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ae1da-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae1da-128">Code-Generator für Webdienste auf Geräten</span><span class="sxs-lookup"><span data-stu-id="ae1da-128">Web Services on Devices Code Generator</span></span>](web-services-for-devices-code-generator.md)
</dt> <dt>

[<span data-ttu-id="ae1da-129">Verwenden von wsdcodegen</span><span class="sxs-lookup"><span data-stu-id="ae1da-129">Using WsdCodeGen</span></span>](using-wsdcodegen.md)
</dt> </dl>

 

 



